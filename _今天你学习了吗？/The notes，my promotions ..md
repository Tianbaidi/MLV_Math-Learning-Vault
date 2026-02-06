##### 笔记热力图

```dataviewjs
// 表情评级配置
const moonEmoji = {
    20:"😢",
    40:"😓", 
    60:"🥺",
    80:"😆",
    100:"🥳"
};

const trackerData = {
    entries: [],
    colorScheme: {
        customColors: [
            "rgb(153,225,229)",
            "rgb(243,232,203)",
            "rgb(242,198,180)",  
            "rgb(251,175,175)",   
            "rgb(255, 84, 26)"
        ]
    },
    heatmapTitle: "📚 每日获得五谷鱼粉 📚",
    heatmapSubtitle: "五谷鱼粉🌾，在五谷🌰，在火候🔥，在匠心✨，在决心💪。",
    intensityScaleStart: 1,
    intensityScaleEnd: 5
}

// 改进的字段解析函数
function parseFieldValue(field, defaultValue, min, max) {
    if (field === undefined || field === null) return defaultValue;
    
    let value;
    if (typeof field === 'number') {
        value = field;
    } else if (typeof field === 'string') {
        // 移除可能的空格和非数字字符
        const numMatch = field.toString().replace(/\s/g, '').match(/-?\d+/);
        value = numMatch ? parseInt(numMatch[0]) : defaultValue;
    } else {
        // 尝试转换为数字
        const num = Number(field);
        value = isNaN(num) ? defaultValue : num;
    }
    
    return Math.min(Math.max(value, min), max);
}

// 获取表情函数
function getEmojiForMoon(moonValue) {
    moonValue = Math.min(Math.max(moonValue, 1), 100);
    
    if (moonValue <= 20) return moonEmoji[20];
    if (moonValue <= 40) return moonEmoji[40];
    if (moonValue <= 60) return moonEmoji[60];
    if (moonValue <= 80) return moonEmoji[80];
    return moonEmoji[100];
}

// 首先，获取所有daily notes页面
const allDailyNotes = dv.pages('"daily notes"');

// 调试：显示找到的页面数量


// 遍历所有页面，不只是有特定字段的
for(let page of allDailyNotes){
    // 解析字段值，如果字段不存在则使用默认值
    const learningValue = parseFieldValue(page.learning, 1, 1, 5);
    const moonValue = parseFieldValue(page.moon, 1, 1, 100);
    
    // 记录到热力图数据中
    trackerData.entries.push({
        date: page.file.name,
        filePath: page.file.path,
        intensity: learningValue,
        content: getEmojiForMoon(moonValue),
        // 保存原始值用于调试
        rawLearning: page.learning,
        rawMoon: page.moon
    })  
}

// 调试：显示处理了多少条目


trackerData.basePath = 'daily notes';

renderHeatmapTracker(this.container, trackerData);
```

```dataviewjs

const trackerData = {
    
    entries: [],
    colorScheme: {
        customColors: [
            "rgb(204, 255, 255)", // 强度1
            "rgb(203, 241, 245)", // 强度2
            "rgb(166, 227, 233)",  // 强度3
            "rgb(113, 201, 206)",   // 强度4
            "rgb(70, 205, 207)",   // 强度5
            "rgb(48,227,202)",   // 强度4
            "rgb(0,184,169)",   // 强度4
            "rgb(17,153,158)",   // 强度4
            "rgb(24,145,172)",   // 强度4
            "rgb(246,114,128)",   // 强度4
        ]
    },
    heatmapTitle: "🤫 今天码了多少字？ 🖊",
    heatmapSubtitle: "码字能吃吗？（疑惑）？.",
    intensityScaleStart: 1,
    intensityScaleEnd: 20000
}

for(let page of dv.pages('"daily notes"').where(p=>p.writing)){
    // 获取学习强度值，确保在1-5范围内
    let writingValue = parseInt(page.writing) || 1
    
    
    trackerData.entries.push({
        date: page.file.name,
        filePath: page.file.path,
        intensity: writingValue,
        
    })  
}

trackerData.basePath = 'daily notes';

renderHeatmapTracker(this.container, trackerData)
```



``` dataviewjs 
// 获取所有有效笔记（排除模板和系统文件）
const allNotes = dv.pages()
    .filter(p => p.file && 
           p.file.path.endsWith(".md") && 
           !p.file.path.includes("Ⅲ 实用转换工具/") &&
           !p.file.path.includes("_今天你学习了吗？/") &&
           !p.file.path.includes("C⋰图片资料/") &&
           !p.file.path.includes("1.AAA最前索引/") &&
           !p.file.path.includes("daily notes/"))
    .map(p => p.file);

// 基于当天日期生成随机种子（确保每日结果一致）
const today = new Date().toISOString().slice(0, 10); // "YYYY-MM-DD"
const seed = parseInt(today.replace(/-/g, "")); 

// 生成随机索引（修复负数问题）
const randomValue = Math.abs(Math.sin(seed) * 10000) % 1;
const randomIndex = Math.floor(randomValue * allNotes.length);

// 俏皮的标题和提示语数组
const playfulTitles = [
    "🎯 今日知识彩蛋",
    "✨ 幸运笔记发现",
    "🔮 知识盲盒时间",
    "🌟 今日特别推荐",
    "💫 随机智慧掉落",
    "🎁 每日知识惊喜",
    "📚 脑洞大开时间"
];

const playfulPrompts = [
    "嘿，今天该复习这个了！",
    "猜猜我今天给你选了啥？",
    "缘分让你看到这个笔记～",
    "叮！你的每日知识已送达",
    "这个笔记在向你招手呢 👋",
    "今日份的灵感来源在此！",
    "哇哦，发现了一个宝藏！"
];

// 选择随机的俏皮元素
const randomTitleIndex = Math.abs(Math.floor(Math.sin(seed * 2) * 10000)) % playfulTitles.length;
const randomPromptIndex = Math.abs(Math.floor(Math.sin(seed * 3) * 10000)) % playfulPrompts.length;

// 安全检查
if (allNotes.length === 0) {
    dv.paragraph("😴 今天没有笔记可以推荐，快去创造些知识吧！");
} else {
    // 获取随机笔记
    const randomNote = allNotes[randomIndex];
    
    // 安全地获取文件夹路径
    const folderPath = randomNote.path.split("/").slice(0, -1).join("/");
    const locationText = folderPath ? `藏在"${folderPath}"里` : "在根目录躺着";
    
    // 显示可点击的链接（带俏皮提示）
    dv.header(2, playfulTitles[randomTitleIndex]);
    dv.paragraph(`**${playfulPrompts[randomPromptIndex]}**`);
    dv.paragraph(`🎉 [[${randomNote.path}|${randomNote.name}]]`);
    dv.paragraph(`*${locationText}的小可爱，快去看看吧~*`);
    
    // 添加一些随机的结束语
    const endings = [
        "祝您阅读愉快！📖",
        "学习使我快乐！",
        "知识就是力量！💪",
        "每天进步一点点~ 🌱",
        "保持好奇，永远年轻！🎈"
    ];
    
    // 修复结束语随机索引计算
    const randomEndingValue = Math.abs(Math.sin(seed * 4) * 10000) % 1;
    const randomEndingIndex = Math.floor(randomEndingValue * endings.length);
    const randomEnding = endings[randomEndingIndex];
    
    // 确保结束语被输出
    dv.paragraph(`*${randomEnding}*`);
}

// 确保最后不返回 undefined
""
```

```dataviewjs
// ================ 配置区域 (可按需修改) ================
const startDate = moment().subtract(7, 'days').toDate(); // 统计过去7天
const targetFolders = ['"Ⅰ我的数学学习物语果然有问题！"','"Ⅱ物理的与邪恶曾是敌对（）"',]; // 空数组表示全库，如只想查特定文件夹：['"Inbox"', '"Projects"']
const ebookExtensions = [".pdf", ".epub", ".mobi", ".azw3", ".djvu"]; // 要统计的电子书格式

// ================ 核心逻辑 ================
// 初始化数组
const mdFiles = [];
const ebookFiles = [];

// 1. 获取符合条件的笔记文件 (md)
let pages;
if (targetFolders.length > 0) {
    pages = dv.pages(targetFolders.join(' or '));
} else {
    pages = dv.pages();
}

for (let page of pages) {
    if (page.file.cday >= startDate) {
        mdFiles.push({
            name: page.file.name,
            path: page.file.path,
            cday: page.file.cday,
            type: "笔记"
        });
    }
}

// 2. 获取符合条件的电子书文件
for (let file of app.vault.getFiles()) {
    const ext = "." + file.extension.toLowerCase();
    if (ebookExtensions.includes(ext)) {
        const fileCreationDate = moment(file.stat.ctime).toDate();
        if (fileCreationDate >= startDate) {
            const sizeMB = file.stat.size / (1024 * 1024);
            ebookFiles.push({
                name: file.name,
                path: file.path,
                cday: fileCreationDate,
                type: "电子书",
                size: sizeMB < 0.1 ? (file.stat.size / 1024).toFixed(1) + " KB" : sizeMB.toFixed(2) + " MB"
            });
        }
    }
}

// ================ 渲染输出 ================
// 3. 检查是否有数据，无数据时显示提示
if (mdFiles.length === 0 && ebookFiles.length === 0) {
    dv.paragraph(`> [!info] 统计结果\n> 在最近7天（自 ${moment(startDate).format("YYYY-MM-DD")} 起）内，没有找到新增的笔记或电子书。`);
} else {
    // 有数据时，渲染完整报告
    dv.header(2, `📈 七日内新增内容统计 (${moment(startDate).format("MM-DD")} 至 ${moment().format("MM-DD")})`);

    // 3.1 渲染笔记表格
    if (mdFiles.length > 0) {
        dv.header(3, `📝 新建笔记 (${mdFiles.length} 篇)`);
        dv.table(["笔记名称", "创建日期", "所在路径"],
            mdFiles.sort((a, b) => b.cday - a.cday).map(f => [
                `[[${f.path}\\|${f.name.replace(/.md$/, "")}]]`,
                moment(f.cday).format("MM-DD ddd"),
                f.path.split("/").slice(0, -1).join("/") || "/"
            ])
        );
    }

    // 3.2 渲染电子书表格
    if (ebookFiles.length > 0) {
        dv.header(3, `📚 新增电子书 (${ebookFiles.length} 本)`);
        dv.table(["电子书名称", "添加日期", "文件大小"],
            ebookFiles.sort((a, b) => b.cday - a.cday).map(f => [
                `[[${f.path}\\|${f.name}]]`,
                moment(f.cday).format("MM-DD ddd"),
                f.size
            ])
        );
    }

    // 4. 渲染分类统计与进度条
    dv.header(3, "📊 输入分布统计");
    const total = mdFiles.length + ebookFiles.length;
    const mdPercent = total > 0 ? Math.round((mdFiles.length / total) * 100) : 0;
    const ebookPercent = total > 0 ? Math.round((ebookFiles.length / total) * 100) : 0;

    // 创建文本进度条函数
    function createBar(percent, width = 20) {
        const filledCount = Math.round(percent / 100 * width);
        const filled = "█".repeat(filledCount);
        const empty = "░".repeat(width - filledCount);
        return `${filled}${empty} ${percent}%`;
    }

    // 使用Markdown表格输出统计
    dv.paragraph(`
| 内容类型 | 数量 | 占比 | 可视化进度 |
|:---|:---:|:---:|:---|
| **笔记 (MD)** | ${mdFiles.length} | ${mdPercent}% | ${createBar(mdPercent)} |
| **电子书** | ${ebookFiles.length} | ${ebookPercent}% | ${createBar(ebookPercent)} |
| **总计** | **${total}** | 100% | ${createBar(100)} |
`);

    // 5. 添加一段总结性文字
    const dayRange = moment().diff(startDate, 'days');
    dv.paragraph(`> [!summary] 小结\n> 过去 ${dayRange} 天里，你共新增了 **${total}** 个知识文件，平均每天 **${(total/dayRange).toFixed(1)}** 个。继续保持输入与积累！`);
}
```


