---
cssclasses:
  - forest-home
---

# 今天你学习了吗？

> *温柔的雨夜，雨水划过宽厚的叶片，透过橘红的晚灯，滋润土地的种子*

%% col-start %%

%% col-break:33 %%

````dataviewjs
const today = window.moment().format('YYYY-MM-DD');
const dailyPath = `daily notes/${today}.md`;
const dailyTemplate = `---
date: ${today}
learning:
moon:
writing:
tags: daily
---

# ${today} 的五谷鱼粉（学习目标！） 🌾

- **记录时间**: ${window.moment().format('HH:mm')}

## 🌾 五谷记录


## 🔥 火候掌控（心情吐槽）


## 📈 数据追踪
~~~dataview
TABLE learning as "学习强度", moon as "心情指数"
FROM "daily notes"
WHERE file.name = this.file.name
~~~
`;

try {
  if (!app.vault.getAbstractFileByPath(dailyPath)) {
    await app.vault.create(dailyPath, dailyTemplate);
  }
  const gateway = this.container.createDiv({ cls: 'forest-daily-gateway' });
  const gatewayCopy = gateway.createDiv({ cls: 'forest-daily-gateway-copy' });
  gatewayCopy.createEl('span', { cls: 'forest-daily-gateway-kicker', text: '今晚的记录' });
  gatewayCopy.createEl('strong', { text: `${today} 的五谷鱼粉` });
  gatewayCopy.createEl('small', { text: '留下一点学习、心情与写作的痕迹。' });
  gateway.createEl('a', { cls: 'internal-link forest-daily-gateway-link', href: dailyPath, text: '打开日记  →' });
} catch (error) {
  console.error('无法创建今日日记', error);
  dv.paragraph('> [!error] 今日日记创建失败\n> 请检查 `daily notes` 文件夹是否可写。');
}
````


```dataviewjs
const poemIndexPath = '诗库/诗库索引.md';
const poems = Array.from(dv.pages('"诗库"').where((page) => page.type === 'poem' && !page.file.path.startsWith('诗库/模板/')));
const poemSeed = Number(window.moment().format('YYYYMMDD'));
const poem = poems.length ? poems[Math.abs(Math.floor(Math.sin(poemSeed) * 10000)) % poems.length] : null;
const poemCard = this.container.createDiv({ cls: 'forest-poem-card' });
poemCard.createEl('small', { text: '今夜的一首诗' });
const poemLink = poemCard.createEl('a', { cls: 'internal-link forest-poem-title', href: poem ? poem.file.path : poemIndexPath, text: poem?.file.name ?? '诗库索引' });
poemLink.dataset.href = poem ? poem.file.path : poemIndexPath;
const rawPoem = poem ? await dv.io.load(poem.file.path) : '';
const poemBody = rawPoem
  .replace(/^---[\s\S]*?---\s*/, '')
  .replace(/^#.*\r?\n+/, '')
  .trim();
const poemBodyEl = poemCard.createEl('div', { cls: 'forest-poem-body' });
const visiblePoem = poemBody.replace(/<!--[\s\S]*?-->/g, '').trim();
const poemLines = (visiblePoem || '诗库还没有作品。').split(/\r?\n/);
poemLines.forEach((line, index) => {
  poemBodyEl.createEl('span', { text: line || '　' });
  if (index < poemLines.length - 1) poemBodyEl.createEl('br');
});
poemCard.createEl('span', { text: '  ·  ' });
const indexLink = poemCard.createEl('a', { cls: 'internal-link', href: poemIndexPath, text: '诗库索引 ↗' });
indexLink.dataset.href = poemIndexPath;
```

## 🌾 每日状态自评

```dataviewjs
const dailyPages = dv.pages('"daily notes"');
const numberValue = (value) => {
  if (typeof value === 'number') return value;
  if (typeof value === 'string' && value.trim() !== '') {
    const result = Number(value.match(/-?\d+(?:\.\d+)?/)?.[0]);
    return Number.isFinite(result) ? result : null;
  }
  return null;
};
const learningEntries = [];
const moodEntries = [];
const heatmapRow = this.container.createDiv({ cls: 'forest-heatmap-row' });

for (const page of dailyPages) {
  const learning = numberValue(page.learning);
  const mood = numberValue(page.moon);
  if (learning !== null && learning >= 1 && learning <= 5) {
    learningEntries.push({ date: page.file.name, filePath: page.file.path, intensity: learning });
  }
  if (mood !== null && mood >= 1 && mood <= 100) {
    moodEntries.push({ date: page.file.name, filePath: page.file.path, intensity: mood });
  }
}

const makeHeatmap = (entries, title, subtitle, palette, end) => {
  if (!entries.length) {
    dv.paragraph(`> [!info] ${title}\n> 填写今日日记里的对应字段后，这里会自动出现记录。`);
    return;
  }
  const card = heatmapRow.createDiv({ cls: 'forest-heatmap-card forest-daily-card forest-rain-mist-card' });
  const stat = card.createDiv({ cls: 'forest-card-stat' });
  const average = entries.reduce((sum, entry) => sum + entry.intensity, 0) / entries.length;
  stat.setText(`近期待平均 ${end === 5 ? average.toFixed(1) + ' / 5' : Math.round(average) + ' / 100'}`);
  const container = card.createDiv();
  renderHeatmapTracker(container, {
    entries,
    basePath: 'daily notes',
    colorScheme: { customColors: palette },
    heatmapTitle: title,
    heatmapSubtitle: subtitle,
    intensityScaleStart: 1,
    intensityScaleEnd: end,
  });
  const sortedDates = entries.map((e) => e.date).sort();
  const todayStr = window.moment().format('YYYY-MM-DD');
  const centerDate = sortedDates.includes(todayStr) ? todayStr : [...sortedDates].reverse().find((d) => d <= todayStr) || sortedDates[0];
  const graph = card.querySelector('.heatmap-tracker-graph');
  const centerCell = graph?.querySelector(`[data-htp-date="${centerDate}"]`);
  if (graph && centerCell) {
    graph.scrollLeft = Math.max(0, centerCell.getBoundingClientRect().left - graph.getBoundingClientRect().left - (graph.clientWidth - centerCell.offsetWidth) / 2);
  }
};

makeHeatmap(learningEntries, '学习强度', '雨雾散开，苔色慢慢显现。', ['#26383A', '#385652', '#4F7568', '#6F9B87', '#A9C6A4'], 5);
makeHeatmap(moodEntries, '心情指数', '从雨夜到灯下，慢慢看见自己。', ['#3C3548', '#695568', '#95677A', '#C98786', '#E1B48D'], 100);
```

%% col-break:67 %%

## 🕋 沉积泥炭

```dataviewjs
const dataPath = '.obsidian/plugins/vault-writing-tracker/data.json';
const colors = ['#DCE8D6', '#C6D8C1', '#ADC59D', '#90AD7B', '#728F62', '#55795A', '#3B6652', '#285347', '#E6A75C', '#FFD58A'];
const writingEmojis = ['💧', '🌱', '☘️', '🌿', '🍃', '🌳', '🌲', '🌙', '✨', '🪔'];

// 合并两条数据源（插件自动记录优先，手记兜底）：
//   插件有记录的日期 → 用插件字数（自动统计，更准确）
//   插件没记录的日期 → 用日记 frontmatter 手记的 writing 字段
const merged = new Map();
const units = new Map(); // 日期 → 计量单位（'词'/'字'），悬停提示用

const parseAmount = (value) => {
  if (typeof value === 'number') return Number.isFinite(value) ? value : null;
  if (typeof value === 'string' && value.trim() !== '') {
    const n = Number(value.match(/-?\d+(?:\.\d+)?/)?.[0]);
    return Number.isFinite(n) ? n : null;
  }
  return null;
};

for (const page of dv.pages('"daily notes"')) {
  const amount = parseAmount(page.writing);
  if (amount !== null && amount > 0) {
    merged.set(page.file.name, amount);
    units.set(page.file.name, '词'); // 手记是词数估计
  }
}

try {
  const raw = await app.vault.adapter.read(dataPath);
  const data = JSON.parse(raw);
  if (data.version === 1 && data.days && typeof data.days === 'object') {
    for (const [date, value] of Object.entries(data.days)) {
      const amount = Number(value?.addedWords ?? value?.addedCharacters);
      if (Number.isFinite(amount) && amount > 0) {
        merged.set(date, amount);
        units.set(date, value?.addedWords != null ? '词' : '字'); // 旧记录是字符口径
      }
    }
  }
} catch (error) {
  console.warn('[主页] 插件写入数据不可用，仅用日记手记数据', error);
}

// 色阶上限：固定 16000（历史词数峰值）。08-08 的 26738 是字符口径异类，顶格饱和显示；
// 开方色阶：低档拉开梯度（中位数 1200 不再糊在最低档）。想改线性可去掉 Math.sqrt
const WRITING_SCALE_MAX = 25600;
const writingEmoji = (amount) => {
  const ratio = Math.max(0, Math.min(1, Math.sqrt(amount / WRITING_SCALE_MAX)));
  return writingEmojis[Math.min(writingEmojis.length - 1, Math.floor(ratio * writingEmojis.length))];
};

const entries = [...merged.entries()]
  .map(([date, amount]) => {
    const ratio = Math.sqrt(Math.max(1, amount) / WRITING_SCALE_MAX); // 与 emoji 同口径
    return { date, intensity: Math.max(1, ratio * WRITING_SCALE_MAX), content: writingEmoji(amount) };
  })
  .sort((a, b) => a.date.localeCompare(b.date));

if (typeof renderHeatmapTracker !== 'function') {
  dv.paragraph('> [!warning] 缺少渲染组件\n> 请启用社区插件 **Heatmap Tracker**，否则热力图无法渲染。');
} else if (!entries.length) {
  dv.paragraph('> [!info] 写入记录尚未产生\n> 在日记 frontmatter 填写 writing 字段，或编辑保存普通笔记后，这里会出现热力图。');
} else {
  const writingCard = this.container.createDiv({ cls: 'forest-heatmap-card forest-writing-card' });
  renderHeatmapTracker(writingCard, {
    entries,
    basePath: '',
    colorScheme: { customColors: colors },
    heatmapTitle: '✍️ 雨后写作',
    heatmapSubtitle: '雾、苔藓、深林与一盏晚归的灯。',
    intensityScaleStart: 1,
    intensityScaleEnd: WRITING_SCALE_MAX,
  });
  // 悬停小窗显示当日写入字数：原生 title/aria-label 贴着鼠标会重叠，改为自绘小窗弹在格子左上方
  let tooltip = document.getElementById('forest-htp-tooltip');
  if (!tooltip) {
    tooltip = document.createElement('div');
    tooltip.id = 'forest-htp-tooltip';
    document.body.appendChild(tooltip);
  }
  for (const [date, amount] of merged.entries()) {
    const cell = writingCard.querySelector(`[data-htp-date="${date}"]`);
    if (!cell) continue;
    cell.removeAttribute('title');
    cell.removeAttribute('aria-label');
    cell.addEventListener('mouseenter', () => {
      tooltip.textContent = `${amount.toLocaleString('zh-CN')} ${units.get(date) || '词'}`;
      tooltip.style.display = 'block';
      const rect = cell.getBoundingClientRect();
      tooltip.style.left = `${rect.left}px`;
      tooltip.style.top = `${rect.top - tooltip.offsetHeight - 6}px`;
    });
    cell.addEventListener('mouseleave', () => {
      tooltip.style.display = 'none';
    });
  }
  // 视口以今天为中心；今天无数据时贴到最近的有数据日期（避免居中到空白）
  const sortedDates = entries.map((e) => e.date).sort();
  const todayStr = window.moment().format('YYYY-MM-DD');
  const centerDate = sortedDates.includes(todayStr) ? todayStr : [...sortedDates].reverse().find((d) => d <= todayStr) || sortedDates[0];
  const graph = writingCard.querySelector('.heatmap-tracker-graph');
  const centerCell = graph?.querySelector(`[data-htp-date="${centerDate}"]`);
  if (graph && centerCell) {
    graph.scrollLeft = Math.max(0, centerCell.getBoundingClientRect().left - graph.getBoundingClientRect().left - (graph.clientWidth - centerCell.offsetWidth) / 2);
  }
}
```

## 🍃 落叶飘临

```dataviewjs
const candidates = dv.pages()
  .where((page) => page.file?.path?.endsWith('.md'))
  .where((page) => !page.file.path.startsWith('.obsidian/') && !page.file.path.startsWith('daily notes/') && page.file.path !== dv.current().file.path);
const notes = Array.from(candidates);
const seed = Number(window.moment().format('YYYYMMDD'));
const index = notes.length ? Math.abs(Math.floor(Math.sin(seed) * 10000)) % notes.length : 0;

if (notes.length) {
  const note = notes[index];
  const keepsake = this.container.createDiv({ cls: 'forest-knowledge-keepsake' });
  const makeKeepsakeLink = (parent, path, text) => {
    const anchor = parent.createEl('a', { cls: 'internal-link', href: path, text });
    anchor.dataset.href = path;
    return anchor;
  };
  keepsake.createEl('span', { cls: 'forest-keepsake-mark', text: '⌁' });
  const copy = keepsake.createDiv();
  copy.createEl('small', { text: '拾得一片叶子' });
  const recommendation = copy.createEl('span', { text: '今天不妨重访：' });
  makeKeepsakeLink(recommendation, note.file.path, note.file.name);
  keepsake.createEl('span', { cls: 'forest-keepsake-arrow', text: '↗' });
} else {
  dv.paragraph('> [!info] 还没有可推荐的笔记。');
}
```

## 🏕️ 步步为营

```dataviewjs
// 两栏待办：Tasks 插件块放进 HTML div 不会渲染，故用 dataviewjs 自渲染
const allTasks = [];
for (const page of dv.pages()) {
  for (const t of (page.file.tasks ?? [])) allTasks.push(t);
}
const dayStart = window.moment().startOf('day').valueOf();
const dayEnd = window.moment().add(1, 'day').startOf('day').valueOf();

const pending = allTasks
  .filter((t) => !t.checked && t.due?.ts !== undefined && t.due.ts < dayEnd)
  .sort((a, b) => a.due.ts - b.due.ts)
  .slice(0, 10);

const doneToday = allTasks
  .filter((t) => t.checked && t.completed?.ts >= dayStart && t.completed?.ts < dayEnd)
  .sort((a, b) => b.completed.ts - a.completed.ts)
  .slice(0, 10);

const row = this.container.createDiv({ cls: 'forest-tasks-row' });

const makeCol = (title, items, done) => {
  const col = row.createDiv({ cls: 'forest-tasks-col' });
  col.createEl('h3', { text: title });
  if (!items.length) {
    col.createEl('p', { cls: 'forest-task-empty', text: done ? '今天还没有完成的任务。' : '没有到期或逾期的任务。' });
    return;
  }
  const ul = col.createEl('ul', { cls: 'forest-task-list' });
  for (const t of items) {
    const li = ul.createEl('li', { cls: 'forest-task-item' });
    li.createEl('span', { cls: 'forest-task-mark', text: done ? '✅' : '☐' });
    const a = li.createEl('a', { cls: 'internal-link', href: t.link.path, text: t.visual ?? t.text });
    if (done && t.completed) a.title = `完成于 ${t.completed.toFormat('MM-dd HH:mm')}`;
    if (!done && t.due) {
      const dueClass = t.due.ts < dayStart ? 'forest-task-due is-overdue' : 'forest-task-due';
      li.createEl('span', { cls: dueClass, text: `📅 ${t.due.toFormat('MM-dd')}` });
    }
  }
};

makeCol('🔥 燃起篝火', pending, false);
makeCol('♨️ 留下火种', doneToday, true);
```

## 👣 林间印迹

```dataviewjs
const homepagePath = dv.current().file.path;
const cutoff = window.moment().subtract(7, 'days').startOf('day').valueOf();
const excludePath = (path) => path === homepagePath || path.startsWith('.obsidian/') || path.startsWith('daily notes/') || path.includes('/templates/');
const changed = dv.pages()
  .where((page) => page.file?.path?.endsWith('.md') && !excludePath(page.file.path))
  .where((page) => page.file.mtime.ts >= cutoff)
  .sort((page) => page.file.mtime, 'desc')
  .limit(12);
const created = dv.pages()
  .where((page) => page.file?.path?.endsWith('.md') && !excludePath(page.file.path))
  .where((page) => page.file.ctime.ts >= cutoff)
  .sort((page) => page.file.ctime, 'desc')
  .limit(12);

const ebookExtensions = new Set(['pdf', 'epub', 'mobi', 'azw3', 'djvu']);
const ebooks = app.vault.getFiles()
  .filter((file) => ebookExtensions.has(file.extension.toLowerCase()) && file.stat.mtime >= cutoff)
  .sort((a, b) => b.stat.mtime - a.stat.mtime)
  .slice(0, 12);

const timeline = this.container.createDiv({ cls: 'forest-activity-timeline' });
const makeInternalLink = (parent, path, text) => {
  const anchor = parent.createEl('a', { cls: 'internal-link', href: path, text });
  anchor.dataset.href = path;
  return anchor;
};
const addActivity = (kind, label, path, text, time) => {
  const item = timeline.createDiv({ cls: `forest-activity-item is-${kind}` });
  item.createEl('span', { cls: 'forest-activity-dot' });
  const body = item.createDiv({ cls: 'forest-activity-body' });
  body.createEl('small', { text: label });
  makeInternalLink(body, path, text);
  item.createEl('time', { text: time });
};
const activities = [
  ...created.map((page) => ({ kind: 'new', label: '新建笔记', path: page.file.path, text: page.file.name, time: page.file.ctime.toFormat('MM-dd HH:mm'), sort: page.file.ctime.ts })),
  ...changed.map((page) => ({ kind: 'edit', label: '最近修改', path: page.file.path, text: page.file.name, time: page.file.mtime.toFormat('MM-dd HH:mm'), sort: page.file.mtime.ts })),
  ...ebooks.map((file) => ({ kind: 'book', label: '电子书变动', path: file.path, text: file.name, time: window.moment(file.stat.mtime).format('MM-dd HH:mm'), sort: file.stat.mtime }))
].sort((a, b) => b.sort - a.sort).slice(0, 14);
if (activities.length) activities.forEach((item) => addActivity(item.kind, item.label, item.path, item.text, item.time));
else timeline.createEl('p', { cls: 'forest-activity-empty', text: '最近七天，林间还没有新的脚印。' });
```

%% col-end %%
