# Savages_And_Missionaries 第一次小组作业安排
## 题目
请用**状态空间搜索法**求解野人与传教士问题：

某条河流的岸边有N个传教士、N个野人和一条船，传教士们想用这条船把所有人都运到河的对岸去，但有以下条件限制：
1. 传教士和野人都会划船，但船每次最多只能运K个人；
2. 在任何时刻保证传教士安全。野人数目如果超过传教士，则传教士会被野人吃掉。
假设野人会服从任何一种过河安排，请规划出一个确保传教士以及野人安全过河的计划，并进行可视化演示，同时讨论无解时N与K的取值情况。

**具体实施要求：**
- 分组：共5组，每组10人，分别加入团队中的需求分析组、系统设计组、美工设计组、程序开发组、测试组与技术服务组；
- 形成完整规范的软件开发文档；
- 每组需选择其他小组的部分成员进行体验，并根据体验反馈的结果修改，同时形成用户体验报告；
下周五课堂分组现场演示。


## 分工

> **算法** 
> ：徐康民 徐哲豪

负责协商并用Java语言完成算法设计，提供数据产出。暂定的数据结构为一个 `int[][]` 数组，以行表示每一轮的状态和行为，行的数量就是轮数+1（因为末状态不占用行为，但是仍占用一行），野人和传教士的当前轮次开始前人数记为A和B，当前轮次进行时船上的野人人数记为△A，船上的传教士人数记为△B，每一行的应该是一个长度为6的数组：` [A, B, N-A, N-B△A, △B]` 。船上的人数均用正数表示，用偶数轮次表示驶向对岸，奇数轮次表示驶回出发点，两者交替，故不必使用正负数表示。
Java语言数组自带长度属性，当界面设计组用Java语言构造的时候，只需要传出一个数组；当界面设计组使用其他语言的时候，可能需要传出数组的一维长度（总状态的数量，即划船的轮数+1）。

> **测试**
> ：余祥

由算法组提供 public 类型的api，进行测试。为界面设计提供算法组未生成最终数据时的伪数据进行界面设计，伪数据的数据结构同正式数据。

> **界面设计**
> ：辛嘉宇
>
使用算法组提供的数据进行界面构造，应该假定算法组能传出的数据只有一个大数组和附属数据。使用测试组提供的测试数据在界面设计上进行测试。
> **文档**
> ：刘沛凡
 
查询相关资料，和其它设计人员沟通，形成设计文档。
> **交互体验**
> ：包云开

对整个应用设计进行评估，与界面设计组沟通，对界面设计在交互易用方面、美观程度、界面设计一体化程度提出指正。