
<!-- # PA2 - 简单复杂的机器: 冯诺依曼计算机系统 -->
# PA2 - Simple and complex machines: von Neumann computer systems

<!-- > #### flag::世界诞生的故事 - 第二章
> 先驱已经创造了图灵机.
> 但区区几个数字电路模块搭成的如此简单的机器, 又能做些什么呢?
> 先驱说, 一切无限的可能, 都蕴含于其中. -->
> #### flag::The Story of the Birth of the World - Chapter 2
> Pioneers have created Turing machines But what can a simple machine built with just a few digital circuit modules do? The pioneer said that all infinite possibilities are contained within it.

<!-- > #### danger::代码管理
> 在进行本PA前, 请在工程目录下执行以下命令进行分支整理, 否则将影响你的成绩:-->
> #### danger::Code Management
> Before proceeding with this PA, please execute the following command in the engineering directory to branch and organize, otherwise it will affect your grades:
```
git commit --allow-empty -am "before starting pa2"
git checkout master
git merge pa1
git checkout -b pa2
```

<!-- #### danger::提交要求(请认真阅读以下内容, 若有违反, 后果自负)
> **<u>预计平均耗时</u>**: 40小时
>
> **<u>阶段性安排</u>**:
> * task PA2.1: 实现更多的指令, 在NEMU中运行大部分`cpu-tests`
> * task PA2.2: 实现klib和基础设施
> * task PA2.3: 运行FCEUX, 提交完整的实验报告 -->
> #### danger::Submission requirements (please carefully read the following content. If there is any violation, the consequences will be borne by oneself)
> **<u>Expected average time</u>**: 40 hours
>
> **<u>Periodic arrangements</u>**:
> * Task PA2.1: Implement more instructions to run most `cpu-tests` in NEMU
> * Task PA2.2: Implementing klib and infrastructure
> * Task PA2.3: Run FCEUX and submit a complete experimental report
