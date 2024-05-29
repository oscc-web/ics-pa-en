
<!-- # PA4 - 虚实交错的魔法: 分时多任务 -->

# PA4 - The magic of reality and fiction: Time-sharing multitasking

<!-- > #### flag::世界诞生的故事 - 第四章
> 先驱已经创造了一个足够强大的计算机, 甚至能支撑操作系统和真实应用程序的运行.
> 但这还不够, 先驱决定向计算机施以虚拟化的魔法. -->

> #### flag::The story of the birth of the world - Chapter 4
> Pioneers have created a computer powerful enough to run even the web and real-world applications.
> But that wasn't enough, the pioneers decided to implement the magic of virtualization on computers.

<!-- > #### danger::代码管理
> 在进行本PA前, 请在工程目录下执行以下命令进行分支整理, 否则将影响你的成绩: -->

> #### danger::code management
> Before proceeding with this PA, please execute the following command in the project directory to organize branches, otherwise your score will be affected:
```
git commit --allow-empty -am "before starting pa4"
git checkout master
git merge pa3
git checkout -b pa4
```


<!-- > #### danger::提交要求(请认真阅读以下内容, 若有违反, 后果自负)
> **<u>预计平均耗时</u>**: 40小时
>
> **<u>阶段性安排</u>**:
> * task PA4.1: 实现基本的多道程序系统, 支持带参数的仙剑奇侠传与Hello内核线程的分时运行
> * task PA4.2: 实现支持虚存管理的多道程序系统
> * task PA4.3: 实现抢占式分时多任务系统, 并提交完整的实验报告 -->

> #### danger::Submit requirements (please read the following carefully, if you violate it, you will be responsible for the consequences)
> **<u>Estimated average time</u>**: 40 hours
>
> **<u>Phase Arrangement</u>**:
> * task PA4.1: Implement a basic multi-programming system and support time-sharing running of PAL with parameters and kernel thread Hello
> * task PA4.2: Implement a multiprogramming system that supports virtual memory management
> * task PA4.3: Implement a preemptive time-sharing multi-task system and submit a complete experimental report