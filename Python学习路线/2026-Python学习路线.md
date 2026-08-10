# 2026 年 Python 学习路线图

> 版本：2026 年 8 月更新 ｜ 基于 Python 3.14 稳定版 ｜ 推荐周期：4~6 个月，每周 10~15 小时

这份路线图把 Python 学习拆成 18 个阶段、80+ 个知识点。每个知识点都包含：

- **🎯 学习目标**：学完这个点之后"应该会什么"，是可衡量的描述；
- **✅ 掌握程度**：明确"学到什么程度算过关"，通常用"能独立完成某某事"来验收；
- **📚 参考资源**：对应这个知识点的视频 / 官网 / 文档地址。

建议的用法：**每个阶段先看总览 → 逐条过知识点 → 做完实战项目再进入下一阶段**。不要跳阶段，也不要在一个阶段里追求完美。

---

## 一、路线总览

| 阶段 | 主题 | 建议周期 | 里程碑产出 |
| --- | --- | --- | --- |
| 0 | 环境搭建 | 1~2 天 | 能运行第一个 Python 脚本 |
| 1 | 基础语法 | 1~2 周 | 命令行小游戏（猜数字） |
| 2 | 核心数据结构 | 1~2 周 | 学生成绩管理系统（内存版） |
| 3 | 文件与异常处理 | 1 周 | 日志分析器、数据可持久化 |
| 4 | 面向对象编程 | 2 周 | 银行账户系统 / 简单游戏 |
| 5 | 进阶特性 | 2 周 | 带装饰器的工具库、大文件生成器 |
| 6 | 标准库常用模块 | 1~2 周 | 命令行文件整理工具 |
| 7 | 包管理与工程规范 | 1 周 | 把自己的工具打包成可安装包 |
| 8 | 调试与测试 | 1~2 周 | 项目测试覆盖率 ≥ 80% |
| 9 | 算法与数据结构基础 | 2~3 周 | LeetCode 简单题 30+ 道 |
| 10 | 并发编程 | 1~2 周 | 并发批量下载工具 |
| 11 | 网络与爬虫 | 2 周 | 公开网站数据采集 + 存储 |
| 12 | 数据库 | 1~2 周 | 爬虫数据入库并提供查询 |
| 13 | Web 开发 | 3~4 周 | TODO 应用 / 个人博客 API |
| 14 | 数据分析与可视化 | 2~3 周 | 公开数据集分析报告 |
| 15 | AI / 机器学习 / 大模型 | 3~4 周 | 房价预测 + LLM 小工具 |
| 16 | 工程化与部署 | 2 周 | Web 项目容器化并上线 |
| 17 | 综合项目 | 3~4 周 | 一个可展示的完整作品集项目 |
| 18 | 方向分支与持续成长 | 长期 | 选定主攻方向并深入学习 |

> 说明：如果时间紧张（每天只有 1 小时），按 6~8 个月执行；如果每天能投入 3 小时以上，可压缩到 3~4 个月。**质量比速度重要。**

---

## 二、阶段 0：开发环境搭建（1~2 天）

### 0.1 安装与运行 Python

🎯 **学习目标**：安装 Python 3.14（或当前 3.12+ 稳定版），理解"解释器"概念，掌握脚本运行和交互式命令行（REPL）两种运行方式。

✅ **掌握程度**：能解释 `python --version` 的输出含义；能用 `python hello.py` 运行脚本；能在交互式环境里逐行执行表达式并立刻看到结果；遇到"找不到 python 命令"能独立排查 PATH 问题。

📚 **参考资源**：
- Python 官网下载：[https://www.python.org/downloads/](https://www.python.org/downloads/)
- 官方教程"开始使用"（中文）：[https://docs.python.org/zh-cn/3/tutorial/interpreter.html](https://docs.python.org/zh-cn/3/tutorial/interpreter.html)
- 视频：黑马程序员《Python+AI 零基础入门》第 1~3 集（[https://www.bilibili.com/video/BV1sHU9BmEne](https://www.bilibili.com/video/BV1sHU9BmEne)），2025 年官方新版，基于当前主流 Python 3 语法；
- 视频（可选·经典）：小甲鱼《零基础入门学习Python》第 1~3 集（[https://www.bilibili.com/video/BV1Ef421B7dR](https://www.bilibili.com/video/BV1Ef421B7dR)），风格轻松，但基于早期 Python 3 版本

### 0.2 代码编辑器（VS Code）

🎯 **学习目标**：安装 VS Code 和 Python 扩展，配置语法高亮、自动补全、运行按钮、断点调试。

✅ **掌握程度**：能用 VS Code 打开项目文件夹；一键运行单文件；运行报错时能根据红色波浪线和"终端里的 Traceback"定位到具体行号。

📚 **参考资源**：
- VS Code 官网：[https://code.visualstudio.com](https://code.visualstudio.com)
- VS Code 官方 Python 文档：[https://code.visualstudio.com/docs/python/python-tutorial](https://code.visualstudio.com/docs/python/python-tutorial)

### 0.3 虚拟环境与 pip（先会用，细节到阶段 7 再深挖）

🎯 **学习目标**：理解虚拟环境解决"不同项目依赖冲突"的作用；会用 `venv` 创建、激活、退出虚拟环境；会用 `pip` 安装和卸载第三方包。

✅ **掌握程度**：能独立为每个新项目创建独立虚拟环境；能解释"为什么每个项目都要有自己的环境"；能分清 `pip install` 与 `requirements.txt` 的关系。

📚 **参考资源**：
- venv 官方文档：[https://docs.python.org/zh-cn/3/library/venv.html](https://docs.python.org/zh-cn/3/library/venv.html)
- pip 官方文档：[https://pip.pypa.io/en/stable/](https://pip.pypa.io/en/stable/)

---

## 三、阶段 1：Python 基础语法（1~2 周）

> 本阶段是所有内容的地基，宁可慢一点。学完验收标准：**不查资料能独立写出"猜数字游戏"和"BMI 计算器"。**

### 1.1 变量与基本数据类型（int / float / str / bool）

🎯 **学习目标**：理解变量的赋值语义，掌握四种基本类型的定义和互相转换（`int()` / `float()` / `str()` / `bool()`）。

✅ **掌握程度**：能写出 `type()` 判断一个值的类型；能解释为什么 `0.1 + 0.2 != 0.3` 并知道用 `round()` 或 `Decimal` 处理；遇到 `TypeError` 能说出是"类型不匹配"并修正。

### 1.2 输入输出与字符串格式化

🎯 **学习目标**：掌握 `input()` 和 `print()`，掌握 f-string（推荐）、`format()`、`%` 三种格式化方式。

✅ **掌握程度**：能写出"输入姓名和年龄，输出一句话介绍"的程序；知道 `input()` 返回的一定是字符串，需要数值时必须显式转换；f-string 能处理对齐、小数位数（如 `{pi:.2f}`）。

### 1.3 运算符与表达式

🎯 **学习目标**：掌握算术、比较、逻辑、赋值运算符，理解运算符优先级和括号的作用。

✅ **掌握程度**：能解释 `and` / `or` 的短路求值；能写出"判断闰年"的复合条件；能读懂 `+=`、`//`、`%`、`**` 的用法。

### 1.4 条件判断：if / elif / else

🎯 **学习目标**：掌握分支逻辑，学会用嵌套条件和"先排除最简单情况"的写法。

✅ **掌握程度**：能独立写出"成绩分级（A/B/C/D）"程序；能把自然语言需求（如"周六周日休息"）翻译成条件表达式；能主动避免冗余的 `if ... return ... else return` 写法。

### 1.5 循环：for / while / break / continue

🎯 **学习目标**：掌握两种循环的适用场景，理解 `break`、`continue`、`else`（循环正常结束）的语义。

✅ **掌握程度**：能用 `for i in range(1, 101)` 求和；能写"猜数字"游戏（含次数限制和退出条件）；能说出"什么时候该用 while（不确定次数）而不是 for"。

### 1.6 列表 list：增删改查

🎯 **学习目标**：掌握列表的索引、切片、`append` / `extend` / `insert` / `remove` / `pop` / `sort` / `reverse`，理解"引用"概念。

✅ **掌握程度**：能实现"最大值、最小值、平均值"；能解释 `list1 = list2` 后修改 list1 会连累 list2 的原因，并用 `.copy()` 或切片避免；能用切片反转列表。

### 1.7 元组 tuple 与不可变性

🎯 **学习目标**：理解元组与列表的区别，掌握解包（`a, b = b, a`）。

✅ **掌握程度**：能说出元组适合存"不该被修改的数据"；能用解包优雅地交换两个变量或拆分 `x, y = point`。

### 1.8 字典 dict：键值对

🎯 **学习目标**：掌握字典的创建、增删改查、遍历（`items()` / `keys()` / `values()`），理解键必须可哈希。

✅ **掌握程度**：能实现"统计一段文本中每个字符出现次数"（用字典计数）；能安全地获取不存在的键（`get` 带默认值）；能遍历字典并同时拿到键和值。

### 1.9 集合 set 与去重

🎯 **学习目标**：掌握集合的创建、交集/并集/差集运算和去重用途。

✅ **掌握程度**：能一行代码对列表去重；能判断"两个列表有哪些共同元素"；能说出集合比列表快的原因（哈希查找）。

### 1.10 字符串进阶：切片与常用方法

🎯 **学习目标**：掌握字符串切片、`split` / `join` / `strip` / `replace` / `find` / `startswith` / `count` / `upper` / `lower`。

✅ **掌握程度**：能把 `"a,b,c"` 拆成列表再拼回字符串；能清洗用户输入（去空格、统一大小写）；能解释字符串不可变意味着什么。

### 1.11 函数：定义、参数与返回值

🎯 **学习目标**：掌握 `def`、位置参数、关键字参数、默认参数、`*args` / `**kwargs`、返回值。

✅ **掌握程度**：能写出"一个函数只做一件事"的代码；能说出默认参数不能用可变对象（如 `def f(x=[])` 是坑）以及原因；能使用 `return` 返回多个值（实际是元组）。

### 1.12 作用域与全局变量

🎯 **学习目标**：理解局部作用域、全局作用域、`global` / `nonlocal`。

✅ **掌握程度**：能解释"函数内为什么读不到/读得到外部变量"；能写出一个计数器闭包（为阶段 5 打底）；知道滥用 `global` 是坏味道。

### 1.13 模块与 import

🎯 **学习目标**：理解模块化思想，掌握 `import`、`from ... import ...`、`as` 别名，会使用标准库模块。

✅ **掌握程度**：能独立查官方文档找到 `random` / `math` 的常用函数；能解释 `if __name__ == "__main__":` 的作用；能把一个 200 行的脚本拆成两个模块。

### 1.14 异常处理入门：try / except / finally

🎯 **学习目标**：理解异常是"程序运行时的错误信号"，掌握捕获、抛出（`raise`）和 `finally` 清理。

✅ **掌握程度**：能给"用户输入数字"的代码加上异常处理，输入非数字时不崩溃而是提示重试；能区分"该捕获的异常"和"不该吞掉的异常"。

### 阶段 1 实战验收

✅ 独立完成两个项目：
1. **猜数字游戏**：随机 1~100，提示大了/小了，限制次数，记录用时；
2. **BMI 计算器**：输入身高体重，输出 BMI 和分级，非法输入不崩溃。

📚 **阶段 1 资源**：
- 视频（主推）：黑马程序员《Python+AI 零基础入门》1~100 集（[https://www.bilibili.com/video/BV1sHU9BmEne](https://www.bilibili.com/video/BV1sHU9BmEne)），2025 年 11 月官方新版，基于当前主流 Python 3（3.10+）语法；
- 视频（主推）：2026 最新 Python 全栈教程（400 集）前 80 集（[https://www.bilibili.com/video/BV1dDj96REkD](https://www.bilibili.com/video/BV1dDj96REkD)），2026 年 6 月发布，紧跟最新版；
- 视频（可选·经典）：小甲鱼《零基础入门学习Python》全集（[https://www.bilibili.com/video/BV1Ef421B7dR](https://www.bilibili.com/video/BV1Ef421B7dR)），幽默易上手，但基于早期 Python 3 版本，仅作兴趣补充；
- 图文：廖雪峰 Python 教程"Python 基础"章节（[https://liaoxuefeng.com/books/python/basic/index.html](https://liaoxuefeng.com/books/python/basic/index.html)）；
- 官网：Python 官方教程第 3~8 章（[https://docs.python.org/zh-cn/3/tutorial/](https://docs.python.org/zh-cn/3/tutorial/)）；
- 备查：菜鸟教程（[https://www.runoob.com/python3/python3-tutorial.html](https://www.runoob.com/python3/python3-tutorial.html)）。

---

## 四、阶段 2：核心数据结构与算法基础（1~2 周）

> 本阶段从"会用"升级到"用对"：开始关注数据结构的性能和典型场景。

### 2.1 数据结构的性能直觉

🎯 **学习目标**：理解 list 按索引取快、`in` 查找慢；dict / set 查找接近 O(1)。

✅ **掌握程度**：能解释"为什么在大数据量下 `x in list` 比 `x in set` 慢很多"；在需要频繁查找时主动选 set / dict。

### 2.2 推导式：list / dict / set comprehension

🎯 **学习目标**：掌握三种推导式的写法与嵌套，理解其可读性边界。

✅ **掌握程度**：能一行写出 `[i*i for i in range(10) if i % 2 == 0]`；能写字典推导式；知道"超过两层的嵌套推导式应该拆成循环"。

### 2.3 排序与查找

🎯 **学习目标**：掌握 `sort()` / `sorted()` 及 `key` 参数，理解二分查找 `bisect`，了解冒泡/选择排序思想。

✅ **掌握程度**：能按字典的某个值排序（`sorted(d.items(), key=lambda x: x[1])`）；能对复杂对象按属性排序；能说出内置排序的时间复杂度。

### 2.4 递归

🎯 **学习目标**：理解递归的"基线条件 + 递归条件"，会用递归解决树状/分治问题。

✅ **掌握程度**：能独立写阶乘、斐波那契、文件树遍历；能解释递归深度限制（`sys.setrecursionlimit`）和"递归改循环"的思路。

### 2.5 时间与空间复杂度入门

🎯 **学习目标**：掌握大 O 记号，能分析常见代码的复杂度。

✅ **掌握程度**：能判断冒泡排序是 O(n²)、二分是 O(log n)、哈希查找是 O(1)；能说出"为什么能接受"或"为什么必须优化"。

### 阶段 2 实战验收

✅ 在 [力扣](https://leetcode.cn)（或 [LeetCode](https://leetcode.com)）完成 **30 道简单题**，覆盖数组、字符串、哈希表、双指针、简单递归。重点是"独立想出来 + 能讲解"，而不是背题。

📚 **阶段 2 资源**：
- 图文：廖雪峰"高级特性"章节（[https://liaoxuefeng.com/books/python/advanced/index.html](https://liaoxuefeng.com/books/python/advanced/index.html)）；
- 视频：黑马程序员 Python 教程中"数据结构与算法"部分；
- 刷题：力扣题库（[https://leetcode.cn/problemset/](https://leetcode.cn/problemset/)），推荐"热题 HOT 100"里的简单题；
- 可视化算法学习：Visualgo（[https://visualgo.net/zh](https://visualgo.net/zh)）。

---

## 五、阶段 3：文件与异常处理（1 周）

### 3.1 文件读写与 with 语句

🎯 **学习目标**：掌握文本文件与二进制文件的读写，理解 `with` 自动关闭文件的原理。

✅ **掌握程度**：能读写 UTF-8 文本文件；能解释 `open()` 的 `r / w / a / b` 模式；知道"必须用 with 或手动 close"的原因（资源泄漏）。

### 3.2 pathlib 路径处理

🎯 **学习目标**：掌握 `Path` 的拼接、`exists()`、`mkdir()`、`glob()`、`read_text()` / `write_text()`。

✅ **掌握程度**：能写出跨平台的文件路径操作，不写死 `\` 或 `/`；能用 `glob` 批量匹配文件（如 `*.log`）。

### 3.3 异常体系与自定义异常

🎯 **学习目标**：掌握常见异常类型（`ValueError` / `TypeError` / `KeyError` / `FileNotFoundError` 等）和继承关系，学会自定义异常类。

✅ **掌握程度**：能捕获"最精确"的异常而不是裸 `except:`；能定义 `class MyError(Exception)` 并在业务中抛出；理解 `try / except / else / finally` 的执行顺序。

### 3.4 编码问题

🎯 **学习目标**：理解 Unicode 与 UTF-8，掌握"读文件指定编码"。

✅ **掌握程度**：遇到"乱码"能说出大概率是编码不一致，并能用 `encoding="utf-8"` 修复；知道为什么写代码时文件头要统一 UTF-8。

### 阶段 3 实战验收

✅ 写一个**日志分析器**：读一个日志文件，统计每小时的请求数/错误数，输出 CSV 报告；文件不存在时给出友好提示而不崩溃。

📚 **阶段 3 资源**：
- 官方文档：文件读写（[https://docs.python.org/zh-cn/3/tutorial/inputoutput.html](https://docs.python.org/zh-cn/3/tutorial/inputoutput.html)）；
- 官方文档：pathlib（[https://docs.python.org/zh-cn/3/library/pathlib.html](https://docs.python.org/zh-cn/3/library/pathlib.html)）；
- 图文：廖雪峰"文件读写"与"错误处理"章节（[https://liaoxuefeng.com/books/python/io/index.html](https://liaoxuefeng.com/books/python/io/index.html)）。

---

## 六、阶段 4：面向对象编程（2 周）

### 4.1 类与对象

🎯 **学习目标**：理解"类是模板，对象是实例"，掌握 `__init__`、实例属性/方法、类属性/方法（`@classmethod`）与静态方法（`@staticmethod`）。

✅ **掌握程度**：能设计一个 `Student` 类（姓名、成绩、平均分方法）并创建实例；能说出三种方法（实例/类/静态）各自的使用场景。

### 4.2 继承、多态与 super()

🎯 **学习目标**：掌握单继承、方法重写、`super()` 调用父类方法，理解多态（同一方法不同表现）。

✅ **掌握程度**：能写出 `Cat` / `Dog` 继承 `Animal` 并各自重写 `speak()`；能用父类引用统一调用子类方法；能画出简单的继承关系图。

### 4.3 魔术方法

🎯 **学习目标**：掌握 `__str__` / `__repr__` / `__eq__` / `__lt__` / `__len__` / `__getitem__` 等常用魔术方法。

✅ **掌握程度**：能让对象 `print` 输出可读信息；能让两个对象直接比较大小、判断相等；知道"为什么自定义对象放进 set 需要 `__hash__`"。

### 4.4 属性封装：property

🎯 **学习目标**：掌握 `@property` 的只读属性和 setter 校验。

✅ **掌握程度**：能写出"年龄为负时报错"的类；能解释 property 与直接暴露属性的取舍。

### 4.5 dataclasses 数据类

🎯 **学习目标**：掌握 `@dataclass` 自动生成 `__init__` / `__repr__` / `__eq__`。

✅ **掌握程度**：能用 dataclass 重构之前的 `Student` 类，代码量明显减少；知道何时该用普通类、何时用 dataclass。

### 4.6 设计原则入门

🎯 **学习目标**：理解单一职责、开闭原则、组合优于继承（简单层面）。

✅ **掌握程度**：能说出"一个类职责过多时怎么拆"；面对"要不要加继承"能先考虑组合。

### 阶段 4 实战验收

✅ 独立实现 **银行账户系统**：`Account` 基类 + `SavingsAccount` / `CheckingAccount` 子类，含存款、取款（余额不足抛异常）、利息计算、流水记录；用 pytest 写出 5 个以上测试。

📚 **阶段 4 资源**：
- 图文：廖雪峰"面向对象编程"与"面向对象高级编程"（[https://liaoxuefeng.com/books/python/oop/index.html](https://liaoxuefeng.com/books/python/oop/index.html)）；
- 官方教程第 9 章"类"（[https://docs.python.org/zh-cn/3/tutorial/classes.html](https://docs.python.org/zh-cn/3/tutorial/classes.html)）；
- 视频：黑马程序员教程中"面向对象"部分。

---

## 七、阶段 5：Python 进阶特性（2 周）

> 本阶段结束，你的 Python 就"脱离新手感"了。这四样东西（闭包、装饰器、生成器、上下文管理器）是面试和读源码的高频点。

### 5.1 lambda 与闭包

🎯 **学习目标**：掌握 lambda 的用法边界，理解闭包（函数记住外部变量）。

✅ **掌握程度**：能写出 `sorted(..., key=lambda x: ...)`；能解释闭包为什么能记住外部变量；知道"循环里用 lambda 的经典坑"（延迟绑定）及修复方式。

### 5.2 装饰器

🎯 **学习目标**：掌握装饰器语法糖 `@`，会写带参装饰器，会用 `functools.wraps`。

✅ **掌握程度**：能独立写计时器、日志、权限校验装饰器；能解释 `@wraps` 为什么必要；能看懂第三方库中装饰器的使用。

### 5.3 迭代器与生成器

🎯 **学习目标**：理解可迭代对象（iterable）与迭代器（iterator）的区别，掌握 `yield` 生成器和生成器表达式。

✅ **掌握程度**：能写一个"逐行读大文件"的生成器（不一次性载入内存）；能解释"生成器是惰性的"；知道 `next()` 和 `for` 的关系。

### 5.4 上下文管理器

🎯 **学习目标**：理解 `with` 背后的 `__enter__` / `__exit__`，掌握 `contextlib.contextmanager`。

✅ **掌握程度**：能自定义一个"计时上下文"；能说出 `with open(...)` 之外上下文管理器的用途（如数据库连接、临时目录）。

### 5.5 高阶函数与 functools

🎯 **学习目标**：掌握 `map` / `filter` / `reduce`（及"为什么推荐推导式"）、`functools.partial` / `lru_cache`。

✅ **掌握程度**：能说出 map/filter 与推导式的等价写法；能用 `lru_cache` 优化递归斐波那契；会用 partial 固定参数。

### 5.6 类型注解入门

🎯 **学习目标**：掌握 `int` / `str` / `list[int]` / `dict[str, int]` / `Optional` / `Union` / `Callable` 等基础注解。

✅ **掌握程度**：能给自写函数加上完整注解；理解注解"不强制但能配合 mypy 检查"；能读懂常见库的注解签名。

### 阶段 5 实战验收

✅ 给阶段 1 的"猜数字"或阶段 4 的项目加：计时装饰器、`lru_cache` 优化、日志上下文管理器；再写一个"逐行处理 100 万行文件"的生成器版本并对比内存占用。

📚 **阶段 5 资源**：
- 图文：廖雪峰"函数式编程"章节（[https://liaoxuefeng.com/books/python/functional/index.html](https://liaoxuefeng.com/books/python/functional/index.html)）；
- 官方教程第 9 章"生成器"部分（[https://docs.python.org/zh-cn/3/tutorial/classes.html](https://docs.python.org/zh-cn/3/tutorial/classes.html)）；
- Real Python 装饰器详解（英文）：[https://realpython.com/primer-on-python-decorators/](https://realpython.com/primer-on-python-decorators/)；
- typing 官方文档：[https://docs.python.org/zh-cn/3/library/typing.html](https://docs.python.org/zh-cn/3/library/typing.html)。

---

## 八、阶段 6：标准库常用模块（1~2 周）

### 6.1 os / sys / shutil

🎯 **学习目标**：掌握环境变量、系统参数、目录遍历、文件复制移动删除。

✅ **掌握程度**：能用 `os.walk` 遍历目录树；用 `shutil.copy2` / `move` 批量整理文件；能写出"按扩展名把文件分类到不同文件夹"的小工具。

### 6.2 datetime / time

🎯 **学习目标**：掌握日期运算、格式化、时区基础。

✅ **掌握程度**：能计算"两个日期相差几天"；能格式化输出 `2026-08-10 14:30:00`；理解 naive 与 aware datetime 的区别（简单层面）。

### 6.3 re 正则表达式

🎯 **学习目标**：掌握元字符、字符类、分组、量词、`re.findall` / `re.sub` / `re.search` / `re.compile`。

✅ **掌握程度**：能提取文本中的手机号/邮箱/URL；能解释贪婪与非贪婪匹配（`.*?`）；能写出"验证 11 位手机号"的正则。

### 6.4 json / csv

🎯 **学习目标**：掌握 JSON 与 CSV 的读写，理解与 Python 数据结构的对应关系。

✅ **掌握程度**：能 `json.dumps` / `json.loads` 处理嵌套数据；能处理 CSV 表头、中文编码；能把字典列表写入 CSV 再读回。

### 6.5 collections

🎯 **学习目标**：掌握 `Counter`、`defaultdict`、`namedtuple`、`OrderedDict`、`deque`。

✅ **掌握程度**：能用 `Counter` 一行统计词频；用 `defaultdict` 给"分组统计"省去判空；能说出 deque 与 list 在头部操作上的性能差异。

### 6.6 itertools

🎯 **学习目标**：掌握 `chain`、`combinations`、`permutations`、`groupby` 等常用工具。

✅ **掌握程度**：能列出"3 个字母取 2 个"的所有组合；能用 `chain` 拼接多个列表；知道 `groupby` 需要先排序。

### 6.7 random / math

🎯 **学习目标**：掌握随机数、随机抽样、常用数学函数。

✅ **掌握程度**：能写随机密码生成器（含大小写数字符号）；能 `random.sample` 不重复抽样；能用 `math` 做常用计算。

### 6.8 argparse 命令行参数

🎯 **学习目标**：掌握命令行参数解析，让脚本可配置。

✅ **掌握程度**：能把阶段 3 的日志分析器改造成支持 `--input`、`--output`、`--verbose` 的命令行工具，并带 `-h` 帮助信息。

### 阶段 6 实战验收

✅ 完成**命令行文件整理工具**：指定目录，按扩展名/日期分类移动文件，生成 CSV 清单，支持 `--dry-run` 预览模式。

📚 **阶段 6 资源**：
- Python 标准库官方文档（中文，建议养成"不会就查"的习惯）：[https://docs.python.org/zh-cn/3/library/index.html](https://docs.python.org/zh-cn/3/library/index.html)；
- 正则练习工具：regex101（[https://regex101.com](https://regex101.com)）；
- 图文：菜鸟教程标准库部分（[https://www.runoob.com/python3/python3-stdlib.html](https://www.runoob.com/python3/python3-stdlib.html)）。

---

## 九、阶段 7：包管理与工程规范（1 周）

### 7.1 pip 进阶与依赖管理

🎯 **学习目标**：掌握 `pip freeze`、`requirements.txt`、`pyproject.toml` 的基本结构。

✅ **掌握程度**：能导出/复现项目依赖；能读懂一个第三方库的 `pyproject.toml` 关键字段；知道 `pip install -e .` 的开发模式。

### 7.2 uv / conda 等现代工具（可选）

🎯 **学习目标**：了解 uv（2026 年流行的超快包管理器）和 conda（数据科学常用）。

✅ **掌握程度**：能用 uv 创建项目并安装依赖；能说出"什么时候用 pip+venv、什么时候用 conda"。

### 7.3 模块与包结构

🎯 **学习目标**：理解"包 = 带 `__init__.py` 的文件夹"，掌握 `from package.module import xxx` 的相对/绝对导入。

✅ **掌握程度**：能把之前的项目重组成规范目录（`src/`、`tests/`）；能解决常见的"导入失败"问题。

### 7.4 代码规范：PEP 8、Black、ruff

🎯 **学习目标**：掌握 PEP 8 核心规则，学会用 Black 自动格式化、ruff 做静态检查。

✅ **掌握程度**：写出的代码能通过 `ruff check .` 无错误；能解释命名规范（`snake_case`、类名 `CamelCase`、常量全大写）。

### 7.5 文档字符串 docstring

🎯 **学习目标**：掌握 Google / NumPy 风格的 docstring。

✅ **掌握程度**：给每个公共函数写清楚"做什么、参数、返回、异常"；能用 `help()` 查看自己写的文档。

### 阶段 7 实战验收

✅ 把阶段 6 的文件整理工具打包成可安装包：`pyproject.toml` + `src` 布局 + `pip install -e .`，命令行入口可用 `tool_name --help` 调用。

📚 **阶段 7 资源**：
- PEP 8 规范（中文翻译可搜索）：[https://peps.python.org/pep-0008/](https://peps.python.org/pep-0008/)；
- ruff 文档：[https://docs.astral.sh/ruff/](https://docs.astral.sh/ruff/)；
- Black 文档：[https://black.readthedocs.io/en/stable/](https://black.readthedocs.io/en/stable/)；
- uv 文档：[https://docs.astral.sh/uv/](https://docs.astral.sh/uv/)；
- Python 官方打包指南：[https://packaging.python.org/en/latest/tutorials/packaging-projects/](https://packaging.python.org/en/latest/tutorials/packaging-projects/)。

---

## 十、阶段 8：调试与测试（1~2 周）

### 8.1 调试：断点、单步、pdb

🎯 **学习目标**：掌握 IDE 断点调试（变量监视、调用栈、单步执行）和 `pdb` 基本命令。

✅ **掌握程度**：遇到 bug 能"打断点看变量"而不是到处 `print`；能读调用栈定位"错误发生在哪一层"；会 `pdb.set_trace()`。

### 8.2 logging 日志

🎯 **学习目标**：掌握 `logging` 的级别（DEBUG/INFO/WARNING/ERROR）、配置、文件输出。

✅ **掌握程度**：能写出"控制台 + 文件双输出、按级别过滤"的日志配置；能说出为什么生产环境用 logging 而不是 print。

### 8.3 pytest 基础

🎯 **学习目标**：掌握测试函数、断言、`fixture`、`parametrize`、异常断言（`pytest.raises`）。

✅ **掌握程度**：能给现有项目补测试并运行 `pytest`；会用 `parametrize` 覆盖边界值；能用 `pytest-cov` 查看覆盖率。

### 8.4 TDD 思想入门

🎯 **学习目标**：理解"先写失败测试 → 写实现 → 重构"的循环。

✅ **掌握程度**：能为新功能先写 2~3 个测试再实现；能说出 TDD 的收益与适用场景（不是所有代码都适合）。

### 阶段 8 实战验收

✅ 给阶段 4 的银行账户系统或阶段 3 的日志分析器补测试：**行覆盖率 ≥ 80%**，包含正常、边界、异常三类用例。

📚 **阶段 8 资源**：
- pytest 官方文档：[https://docs.pytest.org/en/stable/](https://docs.pytest.org/en/stable/)；
- logging 官方文档：[https://docs.python.org/zh-cn/3/howto/logging.html](https://docs.python.org/zh-cn/3/howto/logging.html)；
- pdb 官方文档：[https://docs.python.org/zh-cn/3/library/pdb.html](https://docs.python.org/zh-cn/3/library/pdb.html)。

---

## 十一、阶段 9：算法与数据结构基础（2~3 周）

> 如果目标是"数据分析/AI 应用"，本阶段可减量到 15 道题；如果目标是"后端开发/面试"，请完整完成 40+ 题。

### 9.1 必会数据结构

🎯 **学习目标**：掌握数组、链表（概念）、栈、队列、哈希表、树的典型使用场景。

✅ **掌握程度**：能说出每种结构"擅长什么、不擅长什么"；能用 Python 内置结构模拟栈（list）和队列（deque）。

### 9.2 必会算法模式

🎯 **学习目标**：掌握二分查找、双指针、滑动窗口、哈希表优化、简单回溯。

✅ **掌握程度**：见到"有序数组查找"能想到二分；"两数之和"能写出 O(n) 哈希解法；"连续子数组"能想到滑动窗口。

### 9.3 字符串与数组经典题

🎯 **学习目标**：通过刷题巩固阶段 2 的复杂度分析。

✅ **掌握程度**：LeetCode 简单题能 15 分钟内独立写出；中等题能看懂题解并复现（不强求独立）。

### 阶段 9 实战验收

✅ 力扣简单题累计 **30~40 道**，每道题能向别人讲清思路和复杂度。

📚 **阶段 9 资源**：
- 力扣题库：[https://leetcode.cn/problemset/](https://leetcode.cn/problemset/)；
- 算法图解（书 + 博客版）《算法图解》；
- Visualgo 动画演示：[https://visualgo.net/zh](https://visualgo.net/zh)；
- 代码随想录（中文刷题路线）：[https://programmercarl.com](https://programmercarl.com)。

---

## 十二、阶段 10：并发编程（1~2 周）

### 10.1 进程、线程、协程与 GIL

🎯 **学习目标**：理解三者区别，理解 GIL 对 CPU 密集和 IO 密集任务的不同影响。

✅ **掌握程度**：能说出"IO 密集用多线程/协程，CPU 密集用多进程"的理由；能解释 GIL 是什么、为什么存在（简单层面）。

### 10.2 threading 与 concurrent.futures

🎯 **学习目标**：掌握 `ThreadPoolExecutor` 提交任务、获取结果，理解线程安全与锁。

✅ **掌握程度**：能把串行下载改成线程池并发并对比耗时；能说出"多个线程同时改一个变量"的问题及 `Lock` 的解法。

### 10.3 multiprocessing

🎯 **学习目标**：掌握 `ProcessPoolExecutor` 和 CPU 密集任务的加速。

✅ **掌握程度**：能写一个多进程计算示例并实测加速比；理解进程间内存不共享。

### 10.4 asyncio 协程

🎯 **学习目标**：掌握 `async` / `await`、事件循环、`asyncio.gather`。

✅ **掌握程度**：能用 `asyncio` 并发发起多个 HTTP 请求（配合 httpx/aiohttp）；能说出"协程适合高并发 IO"的原因。

### 阶段 10 实战验收

✅ 写一个**并发下载器**：从公开站点下载 50 个文件，串行 vs 线程池 vs 协程各跑一遍，记录耗时并解释差异。

📚 **阶段 10 资源**：
- asyncio 官方文档：[https://docs.python.org/zh-cn/3/library/asyncio.html](https://docs.python.org/zh-cn/3/library/asyncio.html)；
- 廖雪峰"进程和线程"章节（[https://liaoxuefeng.com/books/python/process-thread/index.html](https://liaoxuefeng.com/books/python/process-thread/index.html)）；
- Real Python 并发教程（英文）：[https://realpython.com/python-concurrency/](https://realpython.com/python-concurrency/)。

---

## 十三、阶段 11：网络与爬虫（2 周）

> ⚠️ 合规提醒：只爬公开数据、遵守 robots.txt、控制请求频率、不爬取个人隐私数据、不用于商业牟利。2026 年尤其注意数据合规与网站条款。

### 11.1 HTTP 原理

🎯 **学习目标**：理解请求方法（GET/POST）、状态码、请求头、响应体、会话（Cookie）概念。

✅ **掌握程度**：能用浏览器开发者工具（F12）查看任意网页的请求与响应；能说出 200 / 301 / 403 / 404 / 500 的含义。

### 11.2 requests / httpx

🎯 **学习目标**：掌握 GET/POST、查询参数、请求头、超时、Session 保持。

✅ **掌握程度**：能请求公开 API 并解析 JSON；能带 headers 和 timeout 请求网页；能处理请求失败（重试、异常捕获）。

### 11.3 HTML 解析：BeautifulSoup / lxml

🎯 **学习目标**：掌握 `find` / `find_all` / CSS 选择器 / 属性提取。

✅ **掌握程度**：能从公开网页提取标题、链接、表格数据；能清洗文本（去空白、去标签）。

### 11.4 数据清洗与存储

🎯 **学习目标**：掌握"抓取 → 清洗 → 存 csv/json"的完整流程。

✅ **掌握程度**：能把爬取结果规范化后写入 CSV 或 JSON，字段统一、无重复、可被阶段 12 的数据库读入。

### 11.5 反爬与合规（了解）

🎯 **学习目标**：了解频率限制、User-Agent、登录态、验证码等概念（**了解即可，不建议学绕过手段**）。

✅ **掌握程度**：能说出"为什么爬虫要限速和模拟浏览器"；能判断哪些行为违法/违约。

### 阶段 11 实战验收

✅ 爬取一个允许爬取的公开网站（如天气数据、豆瓣图书榜单、新闻标题），存成 CSV，至少 100 条有效数据。

📚 **阶段 11 资源**：
- requests 官方文档（中文）：[https://requests.readthedocs.io/projects/cn/zh-cn/latest/](https://requests.readthedocs.io/projects/cn/zh-cn/latest/)；
- httpx 官方文档：[https://www.python-httpx.org](https://www.python-httpx.org)；
- BeautifulSoup 中文文档：[https://beautifulsoup.readthedocs.io/zh_CN/latest/](https://beautifulsoup.readthedocs.io/zh_CN/latest/)；
- 视频：黑马程序员 Python 教程中"爬虫"部分。

---

## 十四、阶段 12：数据库（1~2 周）

### 12.1 SQL 基础

🎯 **学习目标**：掌握 `SELECT / INSERT / UPDATE / DELETE`、`WHERE`、`ORDER BY`、`GROUP BY`、`JOIN`、聚合函数。

✅ **掌握程度**：能在 SQLite 中建两张有关联的表，完成"按条件查询 + 分组统计 + 多表联查"。

### 12.2 SQLite 内置库

🎯 **学习目标**：掌握 `sqlite3` 的 `connect` / `execute` / `commit` / 参数化查询。

✅ **掌握程度**：能解释"为什么必须用 `?` 参数化而不是拼字符串"（SQL 注入）；能把 CSV 数据导入数据库。

### 12.3 SQLAlchemy ORM 入门

🎯 **学习目标**：理解 ORM 概念，掌握模型定义、会话、基础 CRUD。

✅ **掌握程度**：能用 SQLAlchemy 定义 `User` / `Post` 模型并完成增删改查；能说出 ORM 与原生 SQL 各自的优势。

### 阶段 12 实战验收

✅ 把阶段 11 的爬虫数据存入 SQLite（用参数化插入），写 5 个查询：按条件筛选、分组统计、联查。

📚 **阶段 12 资源**：
- SQLite 官方文档（英文）：[https://www.sqlite.org/docs.html](https://www.sqlite.org/docs.html)；
- SQLAlchemy 官方文档：[https://www.sqlalchemy.org](https://www.sqlalchemy.org)；
- 免费练习 SQL：SQLBolt（[https://sqlbolt.com](https://sqlbolt.com)）。

---

## 十五、阶段 13：Web 开发（3~4 周）

> 2026 年建议顺序：**FastAPI（主学）→ Flask（了解）→ Django（按需）**。如果目标是"快速出全栈作品"，可先学 Flask 再补 FastAPI。

### 13.1 Web 基础概念

🎯 **学习目标**：理解 HTTP 请求-响应循环、路由、模板、表单、Cookie/Session、前后端分离。

✅ **掌握程度**：能画出一个请求从浏览器到服务器的完整流程；能解释 GET 与 POST 的区别和适用场景。

### 13.2 FastAPI 入门

🎯 **学习目标**：掌握路由、路径参数、查询参数、请求体（Pydantic 模型）、自动 API 文档（`/docs`）。

✅ **掌握程度**：能写出带类型校验和自动文档的 CRUD API；能用 `uvicorn` 启动并调试；能处理表单和文件上传（了解）。

### 13.3 Flask 入门（了解）

🎯 **学习目标**：掌握最小应用、路由、`render_template`、`request` / `session`、`flash`。

✅ **掌握程度**：能做出一个带登录态的小型网页应用；能说出 Flask 与 FastAPI 的核心差异。

### 13.4 Django 了解（按需）

🎯 **学习目标**：了解 Django 的 MVT 架构、admin 后台、自带 ORM。

✅ **掌握程度**：能跑通官方入门教程（投票应用）；能说出"什么时候选 Django（大而全）而不是 FastAPI（轻快）"。

### 13.5 RESTful API 设计

🎯 **学习目标**：理解资源、URL 设计、状态码语义、鉴权基础（JWT 概念）。

✅ **掌握程度**：能设计一个 TODO 资源的标准 REST API（GET/POST/PUT/DELETE）；能解释 Token 鉴权的基本流程。

### 阶段 13 实战验收

✅ 用 FastAPI 实现 **TODO 应用**：增删改查 + 数据存 SQLite + `/docs` 可调试；再做一个带模板页面的版本（Flask 或 FastAPI + Jinja2）。

📚 **阶段 13 资源**：
- FastAPI 官方中文文档：[https://fastapi.tiangolo.com/zh/](https://fastapi.tiangolo.com/zh/)；
- Flask 官方文档（中文）：[https://flask.palletsprojects.com/zh-cn/](https://flask.palletsprojects.com/zh-cn/)；
- Django 官方文档（中文）：[https://docs.djangoproject.com/zh-hans/](https://docs.djangoproject.com/zh-hans/)；
- 视频：B站 2026 年 Python 全栈教程（含 Web 部分，[https://www.bilibili.com/video/BV1dDj96REkD](https://www.bilibili.com/video/BV1dDj96REkD)）。

---

## 十六、阶段 14：数据分析与可视化（2~3 周）

### 14.1 NumPy

🎯 **学习目标**：掌握 ndarray、形状操作、索引切片、广播、向量化计算。

✅ **掌握程度**：能用 NumPy 完成矩阵运算和批量计算；能解释"为什么向量化比 for 循环快"；会 `reshape` / `transpose` / 条件筛选。

### 14.2 Pandas 核心

🎯 **学习目标**：掌握 Series / DataFrame、读写 CSV/Excel、缺失值处理、筛选、分组聚合（`groupby`）、合并（`merge` / `concat`）、透视表。

✅ **掌握程度**：能独立完成"读 CSV → 清洗（去重/补缺失）→ 分组统计 → 输出结论"的完整流程；会 `apply` 自定义函数。

### 14.3 Matplotlib / Seaborn 可视化

🎯 **学习目标**：掌握折线、柱状、散点、直方图、箱线图，掌握中文显示配置。

✅ **掌握程度**：能把分析结论画成 3 张以上清晰图表（含标题、轴标签、图例）；知道何时用哪种图。

### 14.4 数据分析流程

🎯 **学习目标**：理解"提出问题 → 收集数据 → 清洗 → 分析 → 可视化 → 结论"的完整闭环。

✅ **掌握程度**：能对着一个数据集提出 3 个可回答的问题并逐一回答。

### 阶段 14 实战验收

✅ 分析一份公开数据集（推荐 Kaggle 泰坦尼克或本地公开数据），输出一份含 3+ 张图和结论的分析报告（Markdown 或 Notebook）。

📚 **阶段 14 资源**：
- Pandas 官方文档：[https://pandas.pydata.org/docs/](https://pandas.pydata.org/docs/)；
- Pandas 中文教程：[https://www.runoob.com/pandas/pandas-tutorial.html](https://www.runoob.com/pandas/pandas-tutorial.html)；
- NumPy 官方文档：[https://numpy.org/doc/stable/](https://numpy.org/doc/stable/)；
- Matplotlib 官方文档：[https://matplotlib.org](https://matplotlib.org)；
- Seaborn 官方文档：[https://seaborn.pydata.org](https://seaborn.pydata.org)；
- Kaggle 数据集：[https://www.kaggle.com/datasets](https://www.kaggle.com/datasets)；
- 视频：B站"黑马程序员 Python 数据分析"系列。

---

## 十七、阶段 15：AI / 机器学习 / 大模型（3~4 周）

> 2026 年的 Python 学习绕不开 AI。**先做应用（会调用、会调参），再补原理**，这个顺序对大多数人最友好。

### 15.1 机器学习基础概念

🎯 **学习目标**：理解特征、标签、训练集/测试集、过拟合/欠拟合、评估指标（准确率、MSE 等）。

✅ **掌握程度**：能用通俗语言解释"模型在学什么"；能说出一套标准流程：划分数据 → 训练 → 评估 → 调参。

### 15.2 scikit-learn 常用模型

🎯 **学习目标**：掌握线性回归、逻辑回归、决策树、KNN 的调用与评估。

✅ **掌握程度**：能独立完成一个"房价预测"回归任务和一个"鸢尾花分类"分类任务；会 `train_test_split` 和交叉验证（了解）。

### 15.3 PyTorch 入门

🎯 **学习目标**：掌握张量、自动求导（`autograd`）、构建简单神经网络、训练循环。

✅ **掌握程度**：能训练一个手写数字（MNIST）分类器并跑通训练/评估流程；能读懂模型代码的基本结构。

### 15.4 大模型应用（2026 重点）

🎯 **学习目标**：掌握调用大模型 API 完成文本任务、理解提示词工程、了解 RAG（检索增强）与 Agent 概念。

✅ **掌握程度**：能用 API 写出"总结文章 / 问答机器人"小工具；能通过提示词显著改善输出质量；能说出 RAG 解决"模型不知道最新/私有信息"的基本原理。

### 阶段 15 实战验收

✅ 完成两个项目：1）scikit-learn 房价/分类预测；2）一个调用大模型 API 的实用小工具（如"会议纪要整理器"）。

📚 **阶段 15 资源**：
- scikit-learn 官方文档：[https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)；
- PyTorch 官方教程：[https://pytorch.org/tutorials/](https://pytorch.org/tutorials/)；
- 大模型应用入门：各厂商平台文档（OpenAI：[https://platform.openai.com/docs](https://platform.openai.com/docs) 及国内大模型开放平台）；
- 中文学习路线：B站搜索"2026 大模型应用开发教程"。

---

## 十八、阶段 16：工程化与部署（2 周）

### 16.1 Git 与 GitHub

🎯 **学习目标**：掌握 `init / add / commit / push / pull / clone / branch / merge`，理解"提交信息规范"和 `.gitignore`。

✅ **掌握程度**：能把自己的项目推到 GitHub；遇到冲突能解决；能用分支开发新功能再合并；能写规范的 README。

### 16.2 Docker 基础

🎯 **学习目标**：理解镜像与容器，掌握写 `Dockerfile`、`docker build` / `docker run`、端口映射。

✅ **掌握程度**：能把阶段 13 的 Web 项目容器化并本地运行；能解释"为什么部署要用容器"。

### 16.3 部署上线

🎯 **学习目标**：掌握"本地开发 → 服务器/云平台部署"的流程，了解 Nginx + Gunicorn/Uvicorn 组合。

✅ **掌握程度**：能把 Web 应用部署到免费平台（如 Render / Railway / 国内云轻量服务器）并访问成功；能看日志排查部署问题。

### 16.4 CI/CD 入门

🎯 **学习目标**：了解 GitHub Actions 实现"推送代码自动跑测试/构建"。

✅ **掌握程度**：能写一个简单的 workflow：push 时自动 `pip install -r requirements.txt` + `pytest`。

### 阶段 16 实战验收

✅ 把阶段 13 的 TODO 应用：推 GitHub → 写 Dockerfile → 容器化 → 部署上线，给出可访问的 URL。

📚 **阶段 16 资源**：
- Git 官方中文书《Pro Git》：[https://git-scm.com/book/zh/v2](https://git-scm.com/book/zh/v2)；
- GitHub 官方教程：[https://docs.github.com/zh/get-started](https://docs.github.com/zh/get-started)；
- Docker 官方入门教程：[https://docs.docker.com/get-started/](https://docs.docker.com/get-started/)；
- GitHub Actions 文档：[https://docs.github.com/zh/actions](https://docs.github.com/zh/actions)。

---

## 十九、阶段 17：综合项目（3~4 周）

🎯 **学习目标**：把前 16 个阶段的能力串起来，独立完成一个"拿得出手"的完整项目。

✅ **掌握程度**：项目具备以下全部要素：
1. 清晰的 README（项目介绍、安装方式、使用方式、截图）；
2. 规范的代码结构（包、虚拟环境、配置）；
3. 自动化测试（覆盖率 ≥ 70%）；
4. Git 提交历史规范、代码托管在 GitHub；
5. 可演示的运行效果（截图 / 录屏 / 在线地址）。

### 项目选题参考

| 方向 | 项目示例 | 覆盖阶段 |
| --- | --- | --- |
| 工具类 | 个人记账本（命令行 + CSV/SQLite + 统计图表） | 1~8, 12, 14 |
| Web 类 | 在线 Todo / 博客系统（FastAPI + 数据库 + 部署） | 1~13, 16 |
| 数据类 | 天气/电影数据分析报告（爬虫 + Pandas + 可视化） | 11~14 |
| AI 类 | 简历筛选助手 / 文档问答机器人（LLM API + FastAPI） | 13~15 |
| 自动化类 | 自动整理下载目录 + 日报生成（定时 + 邮件/机器人通知） | 3, 6, 10 |

---

## 二十、阶段 18：方向分支与持续成长（长期）

完成综合项目后，根据兴趣选一个主攻方向深入：

### 方向 A：后端开发工程师
- 深入学习 FastAPI/Django 源码级理解、微服务概念、消息队列（Redis/RabbitMQ）、数据库优化、系统设计入门。
- 资源：FastAPI 官方文档进阶、Django 官方文档、Redis 官方文档（[https://redis.io/docs/](https://redis.io/docs/)）。

### 方向 B：数据分析 / 数据科学 / 量化
- 深入学习 Pandas 进阶、SQL 进阶、统计学基础、机器学习系统学习（吴恩达课程）、数据仓库概念。
- 资源：Kaggle 竞赛练习（[https://www.kaggle.com](https://www.kaggle.com)）、可汗学院统计学（[https://zh.khanacademy.org](https://zh.khanacademy.org)）。

### 方向 C：AI / 机器学习工程师
- 系统学习线性代数、概率统计、深度学习（PyTorch 进阶）、大模型微调（LoRA）、RAG 工程化。
- 资源：吴恩达《机器学习》、PyTorch 官方教程、Hugging Face 中文镜像（[https://hf-mirror.com](https://hf-mirror.com)）。

### 方向 D：自动化 / 爬虫 / 运维开发
- 深入学习 Scrapy 框架、Selenium 自动化、定时任务（APScheduler）、运维工具开发。
- 资源：Scrapy 官方文档（[https://docs.scrapy.org/en/latest/](https://docs.scrapy.org/en/latest/)）、Selenium 官方文档（[https://www.selenium.dev](https://www.selenium.dev)）。

### 方向 E：安全 / 逆向（兴趣向）
- 学习网络安全基础、Python 在安全领域的应用（注意合规与法律边界）。
- 资源：可搜索"2026 Python 网络安全入门"专题课程。

---

## 二十一、学习资源总表

### 官方文档与官网（最高优先级，遇到问题先查这里）

| 资源 | 地址 | 用途 |
| --- | --- | --- |
| Python 官网 | [https://www.python.org](https://www.python.org) | 下载安装、版本信息 |
| Python 官方教程（中文） | [https://docs.python.org/zh-cn/3/tutorial/](https://docs.python.org/zh-cn/3/tutorial/) | 系统过一遍基础 |
| Python 官方文档（中文） | [https://docs.python.org/zh-cn/3/](https://docs.python.org/zh-cn/3/) | 查标准库、语法细节 |
| Python 打包指南 | [https://packaging.python.org/en/latest/](https://packaging.python.org/en/latest/) | 打包、发布 |
| PEP 8 代码规范 | [https://peps.python.org/pep-0008/](https://peps.python.org/pep-0008/) | 编码风格 |

### 视频教程（B站，全部免费）

> 💡 **版本对齐说明**：截至 2026 年 8 月，Python 最新稳定版为 3.14。下面推荐的都是 2025~2026 年发布、基于 Python 3.10+ 语法讲解的课程，与 3.14 基础语法完全兼容。学习时直接安装最新版即可；遇到个别新特性差异，以 [官方文档](https://docs.python.org/zh-cn/3/) 为准。

| 资源 | 地址 | 适用阶段 | 特点 |
| --- | --- | --- | --- |
| 黑马程序员《Python+AI 零基础入门》 | [https://www.bilibili.com/video/BV1sHU9BmEne](https://www.bilibili.com/video/BV1sHU9BmEne) | 0~13 | 2025-11 官方新版，基于当前主流 Python 3（3.10+），体系全 |
| 2026 最新 Python 全栈教程（400 集） | [https://www.bilibili.com/video/BV1dDj96REkD](https://www.bilibili.com/video/BV1dDj96REkD) | 0~16 | 2026-06 发布，紧跟最新 Python 3 版本 |
| 2026 Python 零基础教程（300 集） | [https://www.bilibili.com/video/BV1eHMb6FECg](https://www.bilibili.com/video/BV1eHMb6FECg) | 0~14 | 2026-07 发布，最新版（备选） |
| 小甲鱼《零基础入门学习Python》 | [https://www.bilibili.com/video/BV1Ef421B7dR](https://www.bilibili.com/video/BV1Ef421B7dR) | 0~5 | 经典趣味入门，基于早期 Python 3 版本（兴趣补充，非首选） |
| B站搜索"2026 Python 教程" | 自行搜索最新合集 | 全部 | 优先选 2026 年发布、简介标注 Python 3.12+ 的课程 |

### 图文教程

| 资源 | 地址 | 特点 |
| --- | --- | --- |
| 廖雪峰 Python 教程 | [https://liaoxuefeng.com/books/python/introduction/index.html](https://liaoxuefeng.com/books/python/introduction/index.html) | 中文免费、示例完整、适合系统阅读 |
| 菜鸟教程 | [https://www.runoob.com/python3/python3-tutorial.html](https://www.runoob.com/python3/python3-tutorial.html) | 速查手册 |
| W3Schools Python | [https://www.w3schools.com/python/](https://www.w3schools.com/python/) | 英文互动式，每节带在线练习 |
| Real Python | [https://realpython.com](https://realpython.com) | 英文高质量进阶文章 |
| Automate the Boring Stuff（免费在线阅读） | [https://automatetheboringstuff.com](https://automatetheboringstuff.com) | 自动化办公场景实战 |

### 系统性课程（英文，适合想打牢基础的同学）

| 资源 | 地址 | 说明 |
| --- | --- | --- |
| Harvard CS50P（Python 入门） | [https://cs50.harvard.edu/python/](https://cs50.harvard.edu/python/) | 哈佛免费课，有作业和答题卡 |
| freeCodeCamp | [https://www.freecodecamp.org](https://www.freecodecamp.org) | 免费认证 + YouTube 完整课程（含 CS50 系列 2026 版） |
| 微软 Learn Python 入门 | [https://learn.microsoft.com/zh-cn/training/paths/beginner-python/](https://learn.microsoft.com/zh-cn/training/paths/beginner-python/) | 微软官方中文互动课程 |

### 练习与社区

| 资源 | 地址 | 用途 |
| --- | --- | --- |
| 力扣（LeetCode 中文） | [https://leetcode.cn](https://leetcode.cn) | 刷算法题 |
| Kaggle | [https://www.kaggle.com](https://www.kaggle.com) | 数据集、数据科学竞赛 |
| GitHub | [https://github.com](https://github.com) | 看开源项目源码、托管代码 |
| Stack Overflow | [https://stackoverflow.com](https://stackoverflow.com) | 提问与搜索报错 |
| 知乎 / 掘金 / 博客园 | 站内搜索"Python 学习路线" | 中文经验帖 |

---

## 二十二、每周学习计划建议

以"每周 10~15 小时"为例：

| 时间 | 安排 |
| --- | --- |
| 周一~周三（每天 1.5h） | 看视频/读文档学新知识点，边看边敲代码 |
| 周四（2h） | 做该阶段的小练习 / 力扣题 |
| 周五（2h） | 写实战项目的新功能 |
| 周六（3h） | 集中写项目、修 bug、补测试 |
| 周日（1h） | 复习本周知识点，用"费曼学习法"讲给自己听 |

**核心原则**：
1. **代码量 > 视频量**：看 1 小时视频至少要配 1 小时敲代码；
2. **以项目验收为准**：每个阶段做不完实战验收，就不进入下一阶段；
3. **官方文档优先**：视频看不懂的地方，去查官方文档；
4. **写笔记**：用 Markdown 记录每个知识点的"是什么、怎么用、坑在哪"，形成自己的速查手册；
5. **公开输出**：把项目发到 GitHub、把笔记发到博客，逼自己讲清楚。

---

## 二十三、常见误区

1. **只看不写**：看视频很爽，不动手等于白看。每个示例都要自己敲一遍。
2. **贪多嚼不烂**：同时学 5 个框架、收藏 100 个教程，不如老老实实完成一个项目。
3. **跳过基础直接上框架**：还没搞懂函数和类就学 Django，会越学越痛苦。
4. **不查官方文档**：只靠百度/博客碎片化学习，遇到问题先查官方文档（中文版也有）。
5. **项目抄完不消化**：抄项目时每行都要问"为什么这么写"，改一改、加个功能，才算学会。
6. **过早追求"高深"**：阶段 0~8 没扎实就学 asyncio / 元类，性价比极低。
7. **忽视代码规范**：2026 年 AI 辅助编码已经很普及，但"能读代码、会改代码、懂规范"仍然是核心竞争力。

---

## 二十四、常见问题 FAQ

**Q1：完全没有编程基础，能学 Python 吗？**
可以。本路线阶段 0~3 就是为零基础设计，建议选择黑马程序员或 2026 年新课程视频 + 廖雪峰图文搭配。

**Q2：学完要多久？**
每天 2 小时左右，约 4~6 个月；想速成就业方向需再加大项目投入，一般 6~9 个月更扎实。

**Q3：需要买课吗？**
不需要。本路线里的免费资源足够学到就业/实战水平。买课的主要价值是"监督"和"答疑"。

**Q4：2026 年还需要学传统爬虫吗？**
很多数据可以直接用官方 API 获取，但爬虫仍是理解 HTTP 和数据处理的好训练场。建议学但不要作为唯一方向。

**Q5：学了基础之后，先学数据分析还是 Web？**
看你目标：想走数据/AI 方向先学数据分析（阶段 14）；想走后端先学 Web（阶段 13）；两条路都离不开阶段 9~12。

**Q6：AI 时代学 Python 还有必要吗？**
很有必要。AI 工具能帮你写代码，但"读懂代码、拆解问题、设计结构、调试修复"这些能力都建立在扎实的 Python 基础上。本路线的重点正是这些 AI 替代不了的能力。

**Q7：我装的是最新的 Python 3.14，但教程可能是基于 Python 3.10~3.13 讲的，能学吗？**
能。Python 基础语法在 3.10~3.14 之间保持兼容，教程里的代码在最新版上都能运行；新版本主要是性能提升和新增特性，不改变基础语法。判断课程是否过时看两点：是否基于 Python 3（而不是 2）、是否还在讲 2.x 时代的旧写法；尽量选 2025 年以后发布的课程即可。

---

> 最后一句：**路线图只是地图，走路的是你。** 每完成一个阶段，把产出发到 GitHub，你回头看时会感谢自己。祝 2026 年学习顺利！
