---
tags:
  - Computer-science
  - Python
---
# 包的导入
在考试过程中，一定要提前写入包。一般来说

```python
from math import sin # 导入一个函数
from math import sin as ss # 这是一个导入后重新命名
```

如果我们要导入所有的对象则 

```python
from math import * # 这样其中的就都能用了
```

# 基本运算

| 运算符号                           | 功能说明                                                              | 注意                                                         |
| ------------------------------ | ----------------------------------------------------------------- | ---------------------------------------------------------- |
| :=                             | 赋值运算                                                              |                                                            |
| or ,and ,not                   | 一些逻辑用词，表述或（并），都（交），否（补）                                           | 布尔型运算                                                      |
| in ， not in                    | 测试运算符，if and only if x $\in$ y , output True                      |                                                            |
| is , is not                    | 看不懂，不知道                                                           |                                                            |
| <,<=,>,>=,$\text{==}$ , !=     | 表示比较大小                                                            | 同时作用于集合的比较                                                 |
| \|                             | 并集 A\|B                                                           | 不是整除                                                       |
| ^                              | 对称差集 i.e. $A\Delta B=(A\cup B)-(A \cap B)$                        |                                                            |
| &                              | 交集                                                                |                                                            |
| <<、>>                          | 左移位and右移位                                                         | 似乎没用到过                                                     |
| +、-                            | +：算数，列表，元组，字符串合并连接 -：算数，集合的差集                                     |                                                            |
| $\text{*}$ ,/,//,%,$\text{**}$ | 乘法，除法，取整，取余，乘方                                                    | 注意到：乘方可以拿来开方；此外，% 运算的结果符号与除数相同 **ex** -17%4=3 (若为-4 则为 -1) |
| $[]$ . ( )                     | $[]$ 这里表示下标、切片。句号表示属性访问或者成员访问。（）则是函数的定义与调用，修改表达式的计算顺序，声明多行代码为一个语句 | 相对而言较为生疏，因为用的不多                                            |
| $[]\ \{  \}\ ()$               | 详见后续                                                              |                                                            |
关于各种 **除法** ：

```python
>>> 3 / 2 # 就是除法，会自动将整型转为浮点型
1.5
>>> 15 // 4 # 这里表示取整，最终结果为 保留整数
3
>>> 15.0 // 4  # 此处由于有浮点型，输出结果也为浮点型
3.0
>>> -15.0 /4 # python 所遵循的原则都是比原来要小，所以这里是 
-4.0
>>> -17 % 4 # 我们的取余数也是同理，更小
3 
>>> -17 / -4 # 且为正数，但是如果我们的除数也是负数呢？那就比原来的大，为负数
-1
```

`pow` 语法 ：

```python
pow(a,b,c) # 这是不得不品鉴的一环，这三个数分别代表 原初的数字，乘多少次方，除多少取余数，等价的
a**b % c
```

 逻辑运算符
```python
>>> 1>6<math.sqrt(9) # 逻辑运算符号有惰性的特点，此时我们没有导入 math 库，但是它直接给了判定
False
>>> "Hello" > "world" # 这里也是惰性的体现。原则上来说，我们要做到每项都比后来者大才能输出 Ture ，此时有一项则输出 False , H < w
False 
>>> [2,9] > [1,666,66666] # 同理的，这里也是一眼出结果
True
>>> [2,2] > [2,2,5] # 但是并不是完全的长度无关
False
>>> "3" < 3 # 字符串和数字不能比较
TypeError: '<' not supported between instances of 'str' and 'int'
>>> {a,b,c,d}<{a,b,c,r} # 这个符号用在集合则表示是否具有包含关系，集合判断维持集合的无序性。此时 "<" & ">" 就是 subset 或者 supset
False
>>> 3 > 5 and a < 5 # 我们的 and 表示逻辑交，翻译为且，符合我们的惰性，此处并未定义 a 也输出结果
False
>>>  3 > 5 or a < 5 # 这里的 or 表示逻辑并，翻译为或，也受到惰性的控制，但是第一个比较逻辑真，进行后一个判断。
NameError: name 'a' is not defined
>>> 3 and 5 # and 和 or 的运算不一定返回布尔型，逻辑运算的最后一个值为其赋值
5
>>> 3 is not 5 # 但是 not 的返回必须为布尔型后续比较缓存 3 
True
>>> not 3
False
```

`abs()` 函数

```python
>>> abs(-10) # 传入负数，直接去掉负号变成正数，最基础的操作
10
>>> abs(3.14) # 浮点数保持不变，原样返回
3.14
>>> abs(3 + 4j) # 复数比较特殊，返回的是模（根号下 3²+4²=5），结果为浮点数
5.0
>>> abs("-5") # 传入字符串会报错，和之前 "3" < 3 报错性质一样，类型不兼容
TypeError: bad operand type for abs(): 'str'
>>> abs(int("-5")) # 正确姿势：先把字符串转成 int，再取绝对值，输出 5
5
>>> abs(88 - 100) # 实战中最常用的场景：计算差值，无论正负都取正数，结果为 12
12
```

进制转换函数 

`bin()` 常见词汇bijective 表示双射，其函数为转换二进制
`oct()` 常见词汇 Octopus 表示章鱼，其函数为转换八进制
`hex()` 常见词汇 Hexagon 表示十六宫格，其函数为转换为十六进制
`format` 可以消除前缀，同时保留 `bin` `oct` `hex` 的转换功能，语法为 
```python
>>> foramt(number,"base")
```
这里的 `base` 用缩写 `b` `o` `x` 分别表示二进制，八进制，十六进制
以上的输出都为字符串，被 `""` 包围，如果需要进行与数字的运算，我们需要用 `int` 为其化为整型
`int` 常也可以用作转换，将其他进制转化为十进制
```python
>>> int("string",base)
```
这里的 `base` 表示 `string` 的进制，我们 `"string"` 可以不带进制前缀，直接由 `base` 来判断，若 `"string"` 带了前缀，`base` 也可以直接填为 `0` 供程序自行判断。如果带了前缀且与后 `base` 不符则会报错。
```python
>>>int("0b110",0)
6
>>>int("110",2)
6
>>>int("0x110",2)
ValueError: invalid literal for int() with base 2: '0x110'
```

```python
>>> bin(3.14) # 和前文 abs("-5") 报错性质一样，类型不兼容，它只认整数不认浮点数
TypeError: 'float' object cannot be interpreted as an integer
>>> bin("10") # 字符串更不行，和前文的 abs 一样，遇到类型不对直接报错
TypeError: 'str' object cannot be interpreted as an integer
>>> format(10, 'b') # 如果不想要前面的 0b 前缀，用 format 最干净，输出纯数字字符串 '1010'
'1010'
>>> format(10, 'o') # 对应 oct，去掉前缀 0o，输出 '12'
'12'
>>> format(10, 'x') # 对应 hex，去掉前缀 0x，输出 'a'
'a'
>>> # 注意：这三个函数返回值都是字符串，不能直接当数字用
>>> bin(10) + 5 # 字符串和数字相加，必报错
TypeError: can only concatenate str (not "int") to str
>>> int('0b1010', 2) # 正确姿势：用 int() 指定基数为 2，把二进制字符串转回十进制 10
10
>>> int('0o12', 8)   # 八进制转回十进制，输出 10
10
>>> int('0xa', 16)   # 十六进制转回十进制，输出 10
10
```

排序 `sorted()` 和逆序 `reversed()` 

```python
>>> x=list(range(11))
>>> import random
>>> random.shuffle (x) # 创建无序列表
>>> x
[2,4,0,6,10,7,8,3,9,1,5]
>>>sorted(x) # 默认采用升序排列
[0,1,2,3,4,5,6,7,8,9,10]
>>>sorted(x,key=lambda item : len(str(item)),reverse=True) # 将列表元素转化为字符串后由其长度排序，用到 lambda 函数
[10,2,4,0,6,7,8,3,9,1,5]
>>>sorted(x,key=str) # 按字符串大小排序，符合惰性原则
[0,1,10,2,3,4,5,6,7,8,9]
>>> x # 以上排序均不改变初始顺序——不赋值
[2,4,0,6,10,7,8,3,9,1,5]
>>> list(reversed(x)) # reversed 对象得是可迭代对象，可以理解为直接再for循环中可用.元组虽然为不可变化对象，但是可迭代
[5,1,9,3,8,7,10,6,0,4,2]
>>> result=[['Bob',95.0,'A'],
			['Alan',86.0,'C'],
			['Manday',83.5,'A'],
			['Rob',89.3,'E']]
>>> from operator import itemgetter # 调用 itemgetter 可以进行更加智能的排序
>>> sorted(result,key=itemgetter(2)) # 由评级排序
[['Bob', 95.0, 'A'], ['Manday', 83.5, 'A'], ['Alan', 86.0, 'C'], ['Rob', 89.3, 'E']]
>>> sorted(result,key=itemgetter(2,0)) # 现按第三元素排列，后按第一元素排列（如果第一给同级的话）；加上 reverse=True 就有逆序排列
[['Bob', 95.0, 'A'], ['Manday', 83.5, 'A'], ['Alan', 86.0, 'C'], ['Rob', 89.3, 'E']]
>>>x=['a','bbv','bvvd','114','514','1919810']
>>>sorted(x,key=lambda item:(len(item),item)) # lambda 也有类似的排序效果
['a', '114', '514', 'bbv', 'bvvd', '1919810']
>>> reversed(x) # reverse为惰性返回，想要查看得用 list
<list_reverseiterator object at 0x...>
>>> list(reversed(x)) # 消耗迭代器，得到新列表 
['1919810', '514', '114', 'bvvd', 'bbv', 'a']
>>> x=[[1,2,3],[2,1,4],[2,2,1]]
>>> sorted(x,key=lambda item: (ltem[1],-item[2])) # 第二个升序，后第三个降序，'-' 只用于数值型
[[2, 1, 4], [1, 2, 3], [2, 2, 1]]
>>>list1 = ['Let','We','learn','Algebra']
>>>list2 = ['Geometry','Done','Right','Dude']
>>>pairs=zip(list1,list2) # 这里的操作是将list1和list2的对应元素打包成一个个元组，长度不一则最短优先。
>>># 可以采用 list（pairs）展开得到 [(,),(,)…]
>>>[item[1] for item in sorted(pairs,reverse=True)] # 这个pairs 只能迭代一次，再运行一次就返回空列表了
['Right', 'Done', 'Geometry', 'Dude']
>>>[item[1] for item in sorted(pairs,reverse=True)]
[]
>>>
```

`enumerate()` 枚举

`enumerate()` 可用于枚举可迭代对象中的元素，返回可迭代的 `enumerate` 对象，这个对象是包含索引和值的元组

```python
>>>list(enumerate('abcd'))
[(0, 'a'), (1, 'b'), (2, 'c'), (3, 'd')]
>>>list(enumerate(list(enumerate('abcd'))))
[(0, (0, 'a')), (1, (1, 'b')), (2, (2, 'c')), (3, (3, 'd'))]
>>> for index, value in enumerate(range(10,15)):
	print((index,value),end=" ") # 每次打印元组都以空格结尾（不换行）
>>> (0, 10) (1, 11) (2, 12) (3, 13) (4, 14) 
```

`map()` `reduce()` `filter()` 函数的使用

`map()` 表现为对可迭代对象的批量处理，具体语法为 
```python
map(function,objection)
# ex
map(str,[1,2,3])
```

```python
>>> nums = [1, 2, 3, 4]
>>> map(abs, nums)  # 直接打印是个迭代器对象，看不见具体值
<map object at 0x...>
>>> list(map(abs, nums))  # 必须用 list() 把它“拽”出来才能看到
[1, 2, 3, 4]
>>> # 场景：把字符串数字转成整数（和 int("114") 道理一样，但批量操作）
>>> str_nums = ['1', '2', '3']
>>> list(map(int, str_nums))
[1, 2, 3]
>>> # 注意！如果字符串里混了字母，会触发和 int("0x110",2) 同款 ValueError
>>> list(map(int, ['1', 'a', '3']))
ValueError: invalid literal for int() with base 10: 'a'
```

`reduce()` 为库 `functools` 中的函数，要调用得现加载库 
```python
from functools import reduce
```

`reduce(func, sequence[, initial])` 先把前两个元素扔进函数运算，得到结果后再和第三个元素运算，如此反复，直到最后只剩一个值。通常我们会用 `lambda` 来定义函数
```python
>>> from functools import reduce
>>> reduce(lambda x, y: x + y, [1, 2, 3, 4, 5]) # 累加
15
# ((((1+2)+3)+4)+5) = 15

>>> # 计算阶乘（1*2*3*4*5）
>>> reduce(lambda x, y: x * y, [1, 2, 3, 4, 5])
120
>>> reduce(lambda x,y: x * y,[1,2,3],10)
60
>>> # 处理空列表（必须给初始值，否则报错，和列表越界同理）
>>> reduce(lambda x, y: x + y, [], 0)  # 给个初始值 0，就不报错了
0
>>> reduce(lambda x, y: x + y, [])
TypeError: reduce() of empty sequence with no initial value

```

`fliter()` 就是筛子，通过布尔型值来判断

若返回 `False` 那么就直接剔除

```python
>>> nums = [-5, 3, -1, 8, 0]

>>> # 只保留正数（大于 0 的）
>>> list(filter(lambda x: x > 0, nums))
[3, 8]

>>> # 过滤掉空字符串
>>> words = ['Hello', '', 'World', '']
>>> list(filter(None, words))  # 直接传 None，它会自动滤掉所有布尔值为 False 的元素
['Hello', 'World']
```

元素的添加与删除

```python
>>> lst = [1, 2]
>>> # 1. append：把整个 [3,4] 当做一个元素塞进去（嵌套了）
>>> lst.append([3, 4])
>>> lst
[1, 2, [3, 4]]  
>>> # 长度变成了 3，注意不是 4！
>>> # 2. extend：把 [5,6] 拆开，逐个加进去（和 append 完全不同！）
>>> lst = [1, 2]
>>> lst.extend([3, 4])
>>> lst
[1, 2, 3, 4]  
>>> # 长度变成了 4
>>> # 3. insert：在 0 号位置插入 0
>>> lst.insert(0, 0)
>>> lst
[0, 1, 2, 3, 4]
```

```python
>>> lst = [1, 2, 3, 2, 4]
>>> # 1. remove：只删掉第一个 2
>>> lst.remove(2)
>>> lst
[1, 3, 2, 4]
>>> # remove 删不存在的值
>>> lst.remove(99)
ValueError: list.remove(x): x not in list
>>> # 2. pop：删掉索引 0 的元素，并返回它
>>> lst = [1, 2, 3]
>>> popped = lst.pop(0)
>>> popped
1
>>> lst
[2, 3]
>>> # pop 默认删最后一个
>>> lst.pop()
3
>>> lst
[2]
>>> # 3. del：直接删掉索引位置，不返回任何东西
>>> lst = [1, 2, 3]
>>> del lst[1]
>>> lst
[1, 3]
>>> # 4. clear：瞬间清空
>>> lst.clear()
>>> lst
[]
```

对列表对象的直接排序 `sort()` `reverse()`

在括号中我们可以设置排序的原则，`sort(key=str)` `sort(key=lambda item:(str(item)),reversed=True)` 等

```python
>>> lst = [3, 1, 4, 2]
>>> lst.sort()      # 直接动手排，不返回任何东西
>>> lst             # 看，原列表被改成了从小到大
[1, 2, 3, 4]
>>> lst = [3, 1, 4, 2] # 注意，我们的列表元素得用能互相比较的值
>>> lst.sort(reverse=True) 
>>> lst
[4, 3, 2, 1]
>>> lst = [1, 2, 3, 4]
>>> lst.reverse()    # 直接掉头，不返回东西 ：如果我们令变量 a= 其 >>>a 返回 None
>>> lst
[4, 3, 2, 1]
>>> mix = [1, 'a', [2, 3]]
>>> mix.reverse()
>>> mix
[[2, 3], 'a', 1]   # 完美掉头，绝不报错！
```

列表推导式

即用推导式来推导列表，如我们此前创建列表时候的一些函数 `map` `filter` 等可以不使用，而直接在 `[]` 中操作。
```python
>>> nums = [1, 2, 3, 4]
>>> # 用 map 写
>>> list(map(lambda x: x**2, nums))
[1, 4, 9, 16]
>>> # 用列表推导式写（更直观！）
>>> [x**2 for x in nums]
[1, 4, 9, 16]
>>> nums = [-5, 3, -1, 8]
>>> # 用 filter + map 写（有点绕，要先 filter 再 map）
>>> list(map(lambda x: x**2, filter(lambda x: x > 0, nums)))
[9, 64]
>>> # 用列表推导式写（条件直接跟在后面，一目了然！）
>>> [x**2 for x in nums if x > 0]
[9, 64]
```

当然我们可以玩点变态的

```python
>>> vec = [[1,2,3],[4,5,6],[7,8,9]]
>>> result = []
>>> for elem in vec:
        result.extend(elem)  
>>> result
[1,2,3,4,5,6,7,8,9]
>>> [num for elem in vec for num in elem]
[1,2,3,4,5,6,7,8,9]
```

```python
>>> [(x,y) for x in [1,2,3] for y in [3,1,4] if x != y]
[(1,3), (1,4), (2,3), (2,1), (2,4), (3,1), (3,4)]
>>> result = [] # 上面的和这个等价
>>> for x in [1,2,3]:
...     for y in [3,1,4]:
...         if x != y:
...             result.append((x,y))
... 
>>> result
[(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
>>> [(x,y) for x in [1,2,3] if x == 1 for y in [3,1,4] if y != x]
[(1,3), (1,4)]

```

```python
>>> def f(v):
...     if v % 2 == 0:
...         v = v ** 2
...     else:
...         v = v + 1
...     return v
... 
>>> print([f(v) for v in [2, 3, 4, -1] if v > 0])
[4, 4, 16]
>>> print([v ** 2 if v % 2 == 0 else v + 1 for v in [2, 3, 4, -1] if v > 0])
[4, 4, 16]
```

切片
切片操作由 `[start:end:step]` 来完成，目的在于选取原先的列表进行重排和节选（简单的重排）`start` 和 `end` 遵循左闭右开的原则，某些情况下的设计要在右侧 `+1` 

```python
>>> aList = [3, 4, 5, 6, 7, 9, 11, 13, 15, 17]
>>> aList[::]
# 返回包含原列表中所有元素的新列表
[3, 4, 5, 6, 7, 9, 11, 13, 15, 17]
>>> aList[::-1]
# 返回包含原列表中所有元素的逆序列表
[17, 15, 13, 11, 9, 7, 6, 5, 4, 3]
>>> aList[::2]
# 隔一个取一个，获取偶数位置的元素（索引0,2,4,...）
[3, 5, 7, 11, 15]
>>> aList[1::2]
# 隔一个取一个，获取奇数位置的元素（索引1,3,5,...）
[4, 6, 9, 13, 17]
>>> aList[3:6]
# 指定切片的开始和结束位置（左闭右开，取索引3,4,5）
[6, 7, 9]
>>> aList[0:100]
# 切片结束位置大于列表长度时，从列表尾部截断，不会报错
[3, 4, 5, 6, 7, 9, 11, 13, 15, 17]
>>> aList[100]
# 单个索引越界会抛出异常（和切片不同！）
IndexError: list index out of range
>>> aList[100:]
# 切片开始位置大于列表长度时，返回空列表
[]
>>> aList[-15:3]
# 切片索引超出范围时会自动截断（这里 -15 被截断为 0）
[3, 4, 5]
>>> len(aList)
10
>>> aList[3:-10:-1]
# 位置 3 在位置 -10 的右侧，步长 -1 表示反向切片，取索引3,2,1（不包含-10）
[6, 5, 4]
>>> aList[3:-5]
# 位置 3 在位置 -5 的左侧，正向切片，取索引3,4（因为 -5 对应索引5，左闭右开）
[6, 7]
```

字典
```python
>>> # 方法1：使用 dict() 构造函数创建空字典
>>> x = dict()
>>> x
{}

>>> # 方法2：使用花括号 {} 创建空字典（最常用）
>>> x = {}
>>> x
{}

>>> # 方法3：使用 zip() 将两个列表合并成字典
>>> keys = ['a', 'b', 'c', 'd']
>>> values = [1, 2, 3, 4]
>>> dictionary = dict(zip(keys, values))
>>> dictionary
{'a': 1, 'b': 2, 'c': 3, 'd': 4}

>>> # 方法4：使用关键字参数直接创建字典（键名必须是合法标识符）
>>> d = dict(name='Dong', age=39)
>>> d
{'name': 'Dong', 'age': 39}

>>> # 方法5：使用 fromkeys() 根据键列表创建字典，值统一设为 None
>>> aDict = dict.fromkeys(['name', 'age', 'sex'])
>>> aDict
{'name': None, 'age': None, 'sex': None}
```

字典元素的访问

```python
>>> # 先创建一个示例字典
>>> aDict = {'age': 39, 'score': [98, 97], 'name': 'Dong', 'sex': 'male'}

>>> # 键存在时，返回对应的值
>>> aDict['age']
39
>>> # 键不存在时，抛出 KeyError 异常（和列表索引越界 IndexError 是同类错误）
>>> aDict['address']
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'address'

>>> # 用 get() 方法安全访问 
>>> # 键存在时，和 [] 一样返回对应的值
>>> aDict.get('age')
39

>>> # 键不存在时，不会报错，而是返回 None（默认）
>>> aDict.get('address')
None

>>> # 可以指定键不存在时返回自定义的默认值
>>> aDict.get('address', 'Not Exists.')
'Not Exists.'

>>> # 也可以指定其他默认值，比如数字 0、空列表等
>>> aDict.get('salary', 0)
0
```

字典的更新

字典的 "键" 和 值 具有一定的唯一性，即更新为替旧迎新

```python
>>> # 先搞一个原始字典
>>> d = {'a': 1, 'b': 2}

>>> # ---------- 姿势一：用另一个字典去更新 ----------
>>> d.update({'b': 3, 'c': 4})  # 把 {'b':3, 'c':4} 贴进去
>>> d
{'a': 1, 'b': 3, 'c': 4}        # 注意：b 从 2 变成了 3（覆盖），c 是新增

>>> # ---------- 姿势二：用“键值对元组列表”去更新 ----------
>>> d.update([('d', 5), ('e', 6)])  # 列表里套元组，就像拉链一样
>>> d
{'a': 1, 'b': 3, 'c': 4, 'd': 5, 'e': 6}

>>> # ---------- 姿势三：直接传关键字参数（最直观） ----------
>>> d.update(f=7, g=8)  # 等价于 update({'f':7, 'g':8})
>>> d
{'a': 1, 'b': 3, 'c': 4, 'd': 5, 'e': 6, 'f': 7, 'g': 8}
```

集合方法和运算 `intersection()` `intersection_update()`

`intersection()` 取交集返回一个新集合，不改变原来的赋值

```python
>>> set1 = {1, 2, 3, 4}
>>> set2 = {3, 4, 5, 6}
>>> set3 = {4, 6, 8}

>>> # 取 set1 和 set2 的交集，返回新集合
>>> new_set = set1.intersection(set2)
>>> new_set
{3, 4}
>>> set1  # 原集合纹丝不动！
{1, 2, 3, 4}

>>> # 也可以一次取多个集合的交集
>>> set1.intersection(set2, set3)
{4}  # 因为只有 4 是三个集合共有的
```

`intersection_update()` 则直接对原来的集合更新，此时无法赋值到一个新变量上,或者说是 None

```python
>>> set1 = {1, 2, 3, 4}
>>> set2 = {3, 4, 5, 6}

>>> result = set1.intersection_update(set2)  # 注意！这是在原地动手
>>> print(result)  # 天大的误会！它返回的是 None
None
>>> set1  # 原集合已经被残忍地修改了，只剩交集
{3, 4}
```

快速计算符号 and `&` 以及 and equad `&=`

```python
>>> set1 = {1, 2, 3, 4}
>>> set2 = {3, 4, 5, 6}
>>> set1 & set2  # 完全等价于 set1.intersection(set2)
{3, 4}
>>> set1 & set2 & set3
{4}
>>> set1 &= set2  # 完全等价于 set1.intersection_update(set2)
>>> set1
{3, 4}
```

> 题外话：定义函数时，实参和形参的顺序可以不一致

break和continue

```python
>>> # 场景：在列表里找第一个偶数，找到了就立刻收工（不用再往后找了）
>>> nums = [1, 3, 5, 8, 9, 10]
>>> for n in nums:
...     if n % 2 == 0:
...         print(f"找到偶数了：{n}")
...         break  # 找到了！立刻结束循环，后面的 9 和 10 不用看了
...     print(f"{n} 是奇数，跳过")
... 
1 是奇数，跳过
3 是奇数，跳过
5 是奇数，跳过
找到偶数了：8
# 注意：9 和 10 没有被打印，因为 break 强行终止了循环
```

```python
>>> # 在 while 无限循环中，break 是唯一的退路
>>> i = 0
>>> while True:  # 这本来是个死循环
...     i += 1
...     if i > 3:
...         break  # i 变成 4 时，直接掀桌子跳出循环
...     print(i)
... 
1
2
3
```

这个直接跳出循环结构，就算是存在 else 也被暴力退出（优先级大于 else）

```python
>>> # 场景：打印 1 到 5，但遇到偶数就跳过不打印（只打奇数）
>>> for i in range(1, 6):
...     if i % 2 == 0:
...         continue  # 偶数！跳过本轮剩余的 print，直接进入下一轮
...     print(i)
... 
1
3
5
# 注意：2 和 4 没打印，但循环还在继续，所以 3 和 5 正常打印了
```

这里是跳过本轮循环，进入下一轮循环

`break` 和 `continue` **只作用于它们所在的最近一层循环**，外层循环不受影响

```python
>>> for x in range(1, 3):  # 外层
...     print(f"外层第 {x} 轮")
...     for y in range(1, 4):  # 内层
...         if y == 2:
...             break  # 注意！这个 break 只炸掉内层循环，外层不受影响！
...         print(f"  内层 y={y}")
... 
外层第 1 轮
  内层 y=1
外层第 2 轮
  内层 y=1
# 虽然内层每次只打印了 1，但外层依然坚挺地跑完了两轮
```

可变长度参数

`*` 和 `**` 为前缀的函数我们成为可变长度参数

不知道调用者会传几个位置参数时，用 `*args` 一把全兜住。
```python
>>> def my_sum(*args):
...     print(f"我收到了：{args}")
...     return sum(args)
... 
>>> my_sum(1, 2)          # 传 2 个
我收到了：(1, 2)
3
>>> my_sum(1, 2, 3, 4, 5) # 传 5 个
我收到了：(1, 2, 3, 4, 5)
15
>>> my_sum()              # 传 0 个也行，得到空元组
我收到了：()
0
```

需要处理 `key=value` 形式的参数时，用 `**kwargs`。
```python
>>> def show_info(**kwargs):
...     print(f"我收到了：{kwargs}")
... 
>>> show_info(name='Dong', age=39, city='Beijing')
我收到了：{'name': 'Dong', 'age': 39, 'city': 'Beijing'}
>>> show_info()  # 传 0 个也行，得到空字典
我收到了：{}
```

`lambda` 表达式

用列表调用 `lambda` 函数
```python
>>> # 定义一组运算，放进列表
>>> calc = [
...     lambda x: x + 1,   # 索引 0：加 1
...     lambda x: x * 2,   # 索引 1：乘 2
...     lambda x: x ** 2   # 索引 2：平方
... ]

>>> # 通过下标取出来调用
>>> calc[0](5)   # 取第 0 个 lambda，把 5 传进去
6
>>> calc[1](5)   # 取第 1 个，乘以 2
10
>>> calc[2](5)   # 取第 2 个，平方
25

>>> # 甚至可以循环调用（批量自动化）
>>> [func(3) for func in calc]
[4, 6, 9]
```

用字典调用 `lambda` 函数

```python
>>> # 以字符串为键，lambda 为值
>>> operation = {
...     'add': lambda x, y: x + y,
...     'sub': lambda x, y: x - y,
...     'mul': lambda x, y: x * y,
...     'div': lambda x, y: x / y
... }

>>> # 通过键取 lambda，再传入参数
>>> operation['add'](10, 5)
15
>>> operation['mul'](10, 5)
50

>>> # 实战：动态选择运算
>>> op_name = 'sub'
>>> result = operation[op_name](100, 30)  # 想用哪个用哪个
>>> result
70
```

`lambda` 表达式作为函数参数

```Python
>>> list(map(lambda x: x+10, L))
# lambda 表达式作为函数参数
[11, 12, 13, 14, 15]

>>> def demo(n):
...     return n * n
...
>>> demo(5)
25

>>> a_list = [1, 2, 3, 4, 5]
>>> list(map(lambda x: demo(x), a_list))    # 在 lambda 表达式中可以调用函数
[1, 4, 9, 16, 25]

>>> data = list(range(20))
>>> import random
>>> random.shuffle(data)
>>> data
[4, 3, 11, 13, 12, 15, 9, 2, 10, 6, 19, 18, 14, 8, 0, 7, 5, 17, 1, 16]

>>> data.sort(key=lambda x: x)    # 用在列表的 sort() 方法中，作为函数参数
>>> data
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]

>>> data.sort(key=lambda x: len(str(x)))    # 使用 lambda 表达式指定排序规则
>>> data
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]

>>> data.sort(key=lambda x: len(str(x)), reverse=True)
>>> data
[10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

`format` 的使用指南

```python
>>> # 最简单的替换（按顺序）
>>> "My name is {} and I am {} years old".format("Dong", 39)
'My name is Dong and I am 39 years old'

>>> # 给占位符编号（可以打乱顺序）
>>> "My name is {1} and I am {0} years old".format(39, "Dong")
'My name is Dong and I am 39 years old'

>>> "My name is {name}, age {age}".format(name="Dong", age=39)
'My name is Dong, age 39'

>>> # 甚至可以直接把字典拆开传进去（和你学的 **kwargs 梦幻联动！）
>>> info = {"name": "Dong", "age": 39}
>>> "Name: {name}, Age: {age}".format(**info)
'Name: Dong, Age: 39'

>>> # 左对齐（<），右对齐（>），居中对齐（^），后面跟宽度
>>> "{:<10}".format("左")    # 左对齐，占10个宽度
'左        '
>>> "{:>10}".format("右")    # 右对齐
'        右'
>>> "{:^10}".format("中")    # 居中对齐
'    中    '

>>> # 数字补零（比如显示日期）
>>> "{:0>5}".format(12)      # 右对齐，宽度5，不足补0
'00012'
>>> "{:0<5}".format(12)      # 左对齐补0
'12000'

>>> # 保留两位小数（四舍五入）
>>> "{:.2f}".format(3.1415926)
'3.14'

>>> # 带千位分隔符（处理大数字）
>>> "{:,}".format(1234567890)
'1,234,567,890'

>>> # 百分比显示（自动乘以100并加 %）
>>> "{:.2%}".format(0.2567)
'25.67%'

>>> # 转二进制、八进制、十六进制（不用单独记 bin/oct/hex 的带前缀格式）
>>> "{:b}".format(10)   # 二进制，输出 '1010'
'1010'
>>> "{:#b}".format(10)  # 加 # 前缀，输出 '0b1010'（和你之前学的 bin(10) 效果一样！）
'0b1010'

>>> data = ["Dong", 39]
>>> "Name: {}, Age: {}".format(*data)   # *data 拆成两个参数
'Name: Dong, Age: 39'

>>> # 访问列表/字典的索引（在占位符里直接取下标）
>>> info = ["Dong", 39]
>>> "Name: {0[0]}, Age: {0[1]}".format(info)
'Name: Dong, Age: 39'

```

格式化输出的有同样的 `f""` 更加简单

```python
>>> name = "Dong"
>>> age = 39
>>> score = 95.5

>>> f"姓名：{name}，年龄：{age}，分数：{score}"
'姓名：Dong，年龄：39，分数：95.5'

>>> a, b = 10, 20
>>> f"{a} + {b} = {a + b}"          # 直接算加法
'10 + 20 = 30'

>>> f"明年我就 {age + 1} 岁了"       # 直接算加减
'明年我就 40 岁了'

>>> f"我的名字大写是 {name.upper()}"  # 直接调字符串方法
'我的名字大写是 DONG'

>>> import math
>>> f"圆周率约等于 {math.pi:.2f}"    # 直接调模块 + 格式控制
'圆周率约等于 3.14'

>>> pi = 3.1415926
>>> f"{pi:.2f}"           # 保留两位小数
'3.14'
>>> f"{pi:.4f}"           # 保留四位
'3.1416'

>>> num = 12
>>> f"{num:0>5}"          # 右对齐，宽度5，补0（打印时间或编号常用）
'00012'

>>> big = 1234567890
>>> f"{big:,}"            # 千位分隔符
'1,234,567,890'

>>> # 对齐排版（左< 右> 中^）
>>> f"|{'左':<5}|{'中':^5}|{'右':>5}|"
'|左    |  中  |    右|'

```

字符串切片
```python
>>> s = "大家都用AIAGENT了 手写代码有前途吗？"
>>> # 取前 3 个字（索引 0~2）
>>> s[:3]
'大家都'

>>> # 取中间的 "AIAGENT"（索引 4~10？注意：索引4是I，索引10是T）
>>> s[4:11]  # 左闭右开，取 4 到 10
'AIAGENT'     
>>> # 取后半句 "手写代码有前途吗？"
>>> s[13:]   # 索引13 是 '手'
'手写代码有前途吗？'

>>> # 隔一个取一个（全句取偶数位）
>>> s[::2]
'大都AAET 写码前吗''   # 取出 "大家都用AIAGENT了..." 的奇数位特征

>>> # 终极逆序（把这句话倒过来读）
>>> s[::-1]
'？吗途前有乎码代写手 了TNEGAIA用都家大'
>>> s[10:3:-1]
'TNEGAIA'
>>> s[:3:-1]
'？吗途前有码代写手 了TNEGAIA'

```
