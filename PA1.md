<!-- # PA1 - 开天辟地的篇章: 最简单的计算机 -->

# PA1 - The Chapter of Creating the Universe: The Simplest Computer

<!-- > #### flag::世界诞生的故事 - 第一章
> 先驱已经准备好了创造计算机世界的工具.
> 为了迈出第一步, 他运用了一些数字电路的知识, 就已经创造出了一个最小的计算机 -- 图灵机.
> 让我们来看看其中的奥妙. -->

> #### flag::The Story of World Birth - Chapter One
> The pioneer has prepared the tools to create the world of computers. In order to take the first step, he applied his knowledge of digital circuits and has already created the smallest computer - the Turing machine. Let's explore the wonders of this creation.

<!-- > #### danger::代码管理
> 在进行本PA前, 请在工程目录下执行以下命令进行分支整理, 否则将影响你的成绩: -->

> #### danger::Code Management
> Before starting this PA, please execute the following commands in the project directory to organize the branches. Failure to do so may affect your grade:
```
git commit --allow-empty -am "before starting pa1"
git checkout master
git merge pa0
git checkout -b pa1
```

<!-- > #### danger::提交要求(请认真阅读以下内容, 若有违反, 后果自负)
> 预计平均耗时</u>**: 30小时
>
> **<u>阶段性安排</u>**:
> * task PA1.1: 实现单步执行, 打印寄存器状态, 扫描内存
> * task PA1.2: 实现算术表达式求值
> * task PA1.3: 实现所有要求, 提交完整的实验报告 -->

> #### danger::Submission Requirements (Please read the following content carefully. Any violation will be your own responsibility)
> **<u>Estimated average time required</u>**: 30 hours
>
> **<u>Phase Schedule</u>**:
> * Task PA1.1: Implement single-step execution, print register states, and scan memory.
> * Task PA1.2: Implement arithmetic expression evaluation.
> * Task PA1.3: Implement all requirements and submit a complete lab report.