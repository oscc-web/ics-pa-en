
<!-- # 南京大学 计算机科学与技术系 计算机系统基础 课程实验 2024 -->

# Department of Computer Science and Technology, Nanjing University, Programming assignments of Introduction to Computer System, 2024 


<!-- ## 实验前阅读 -->

## Pre-Laboratory Reading

[how to ask]: https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/master/README-zh_CN.md
[stop ask]: https://github.com/tangx/Stop-Ask-Questions-The-Stupid-Ways/blob/master/README.md
[jyy]: http://ics.nju.edu.cn/~jyy
[ics2020-mainpage]: http://jyywiki.cn/ICS/2020/
[ics2021-mainpage]: http://jyywiki.cn/ICS/2021/
[ics2022-mainpage]: http://why.ink:8080/ICS/2022/
[ics2023-mainpage]: http://why.ink:8080/ICS/2023/
[bilibili]: https://www.bilibili.com/video/BV1qa4y1j7xk/
[mooc1]: https://www.icourse163.org/course/NJU-1001625001
[mooc2]: https://www.icourse163.org/course/NJU-1001964032
[mooc3]: https://www.icourse163.org/course/NJU-1002532004
[sicp]: https://nju-sicp.bitbucket.io/
[os-jyywiki]: http://jyywiki.cn/OS/2023/
[why]: https://cocowhy1013.github.io/


<!-- > #### info::最新消息(请每天至少关注一次)
> * [学术诚信(什么事情能做, 什么不能)](http://integrity.mit.edu/)
> * [常见问题(对PA的各种困惑)](FAQ.md)
> * 如何正确求助: [提问的智慧][how to ask]和[别像弱智一样提问][stop ask]
> * 外部资源
>   * PA习题课 (2023 秋季学期, [王慧妍][why]老师): [课程资料][ics2023-mainpage]
>   * 中国大学MOOC的ICS理论课 (袁春风老师): [上][mooc1], [中][mooc2], [下][mooc3]
>   * [南大SICP编程课][sicp]
>     * <font color=red>如果你觉得自己的编程基础不过关, 墙裂推荐自学这门课</font>
>     * 虽然它教的是python, 但语言的语法是次要的, 对编程思维的锻炼才是最重要的
>   * [OS课][os-jyywiki] (2023 春季学期, [蒋炎岩][jyy]老师)
>   * PA往期习题课
>     * 2022 秋季学期, [王慧妍][why]老师: [课程资料][ics2022-mainpage]
>     * 2021 秋季学期, [王慧妍][why]老师: [课程资料][ics2021-mainpage]
>     * 2020 秋季学期, [蒋炎岩][jyy]老师: [课程资料][ics2020-mainpage], [B站录播][bilibili]
> ---
> * 2024/01/25
>  * 本讲义目前处于测试阶段, 在2024年秋季学期开始前, 将被视为往届讲义材料.
>    如果你是修读2024年秋季ICS课程的学生, 请勿使用本讲义代替2024年秋季ICS课程的PA实验讲义,
>    提交本实验内容将被视为没有提交. -->

> #### info::Latest News (please check at least once a day)
> * [Academic Integrity (What is permissible and what is not)](http://integrity.mit.edu/)
> * [FAQ (Various questions about PA)](FAQ.md)
> * How to Seek Help Properly: [How To Ask Questions The Smart Way][how to ask]和[Stop-Ask-Questions-The-Stupid-Ways][stop ask]
> * External Resources
>   * PA tutorials (Fall 2023, [Wang Huiyan][why] Instructor): [Course Materials][ics2023-mainpage]
>   * ICS Theory Course on China University MOOC (Instructor Yuan Chunfeng): [Part 1][mooc1], [Part 2][mooc2], [Part 3][mooc3]
>   * [SICP of Nanjing University][sicp]
>     * <font color=red>If you feel your programming foundation is not strong enough, it is highly recommended to self-study this course</font>
>     * Although it teaches Python, the syntax of the language is secondary; the most important aspect is the training of programming thinking
>   * [OS][os-jyywiki] (Spring 2023, Instructor: [Jiang Yanyan][jyy])
>   * Past PA tutorials
>     * Fall 2022, [Wang Huiyan][why] Instructor: [Course Materials][ics2022-mainpage]
>     * Fall 2021, [Wang Huiyan][why] Instructor: [Course Materials][ics2021-mainpage]
>     * Fall 2020, [Jiang Yanyan][jyy] Instructor: [Course Materials][ics2020-mainpage], [Bilibili Recordings][bilibili]
> ---
> * 2024/01/25
>  * This handout is currently in the testing phase and will be considered as past handout material before the start of the Fall 2024 semester.
>    If you are a student enrolled in the Fall 2024 ICS course, please do not use this handout as a substitute for the Fall 2024 ICS course PA lab handout.
>    Submitting this experiment content will be considered as not submitted.

<!-- > #### info::离线阅读实验讲义
> 实验讲义页面通过github page发布, 但其网络可能不稳定.
> 你可以把[这个仓库][ics pa gitbook]克隆到本地, 然后通过浏览器来离线阅读讲义.
>
> 但随着讲义内容的更新, 你将无法自动地阅读到最新版本的内容.
> 你需要在仓库路径中手动执行`bash update.sh`来将最新版本的内容同步到本地.
> 再次强调, <font color=red>如果你选择了离线阅读方式, 将由你来负责获取最新的讲义内容. </font> -->

> #### info::Read the handout offline
> Handout pages of this lab are published through GitHub Pages, but the network may be unstable.
> You can clone [this repository][ics pa gitbook] to your local machine, and read the handouts offline through your browser.
>
> However, as the handout content is updated, you will not be able to automatically access the latest version.
> You need to manually execute `bash update.sh` in the repository path to synchronize the latest version of the content to your local machine.
> Again, <font color=red>if you choose the offline reading method, then it is your responsibility to obtain the latest handout content.</font>

[ics pa gitbook]: https://github.com/NJU-ProjectN/ics-pa-gitbook

<!-- > #### hint::如何求助
> * 实验前请先仔细阅读[本页面](.)以及[为什么要学习计算机系统基础](why.md).
> * 如果你在实验过程中遇到了困难, 并打算向我们寻求帮助,
> 请先阅读[提问的智慧][how to ask]和[别像弱智一样提问][stop ask]这两篇文章.
> * 如果你发现了实验讲义和材料的错误或者对实验内容有疑问或建议,
> 请通过邮件的方式联系余子濠(zihaoyu.x#gmail.com) -->

> #### hint::How to Seek Help
> * Please read [this page](.) and [Why Study the Fundamentals of Computer Systems](why.md) carefully before the lab.
> * If you encounter difficulties during the lab and plan to seek our help, please first read [How to Ask Questions the Smart Way][how to ask] and [How Not to Ask Stupid Questions][stop ask].
> * If you find errors in the lab handouts and materials or have questions or suggestions about the lab content, please contact Zihao Yu via email (zihaoyu.x#gmail.com).


<!-- -->
<!-- > #### hint::小百合系版"有像我一样不会写代码的cser么?"回复节选
> * 我们都是活生生的人, 从小就被不由自主地教导用最小的付出获得最大的得到, 经常会忘记我们究竟要的是什么.
> 我承认我完美主义, 但我想每个人心中都有那一份求知的渴望和对真理的向往,
> "大学"的灵魂也就在于超越世俗, 超越时代的纯真和理想
>  -- 我们不是要讨好企业的毕业生, 而是要寻找改变世界的力量. -- jyy
> * 教育除了知识的记忆之外, 更本质的是能力的训练, 即所谓的training.
> 而但凡training就必须克服一定的难度, 否则你就是在做重复劳动, 能力也不会有改变.
> 如果遇到难度就选择退缩, 或者让别人来替你克服本该由你自己克服的难度,
> 等于是自动放弃了获得training的机会, 而这其实是大学专业教育最宝贵的部分. -- etone
> * 这种"只要不影响我现在survive, 就不要紧"的想法其实非常的利己和短视:
> 你在专业上的技不如人, 迟早有一天会找上来, 会影响到你个人职业生涯的长远的发展;
> 更严重的是, 这些以得过且过的态度来对待自己专业的学生,
> 他们的survive其实是以透支南大教育的信誉为代价的 -- 如果我们一定比例的毕业生都是这种情况,
> 那么过不了多久, 不但那些混到毕业的学生也没那么容易survive了,
> 而且那些真正自己刻苦努力的学生, 他们的前途也会受到影响. -- etone -->

#### hint::Some quotes
> * We are all living beings, taught from a young age to get the most out of the least effort, often forgetting what we truly want.
>  I admit I am a perfectionist, but I believe everyone has a thirst for knowledge and a longing for truth in their hearts.
>  The soul of "university" lies in transcending the mundane and timeless innocence and ideals.
>  -- We are not here to please corporate graduates, but to seek the power to change the world. -- jyy
> * Education, beyond the memorization of knowledge, is essentially the training of abilities, the so-called training.
>  And any training must overcome certain difficulties; otherwise, you are merely doing repetitive work, and your abilities will not improve.
>  If you choose to retreat when encountering difficulties or let others overcome the difficulties you should overcome yourself,
> you are essentially giving up the opportunity for training, which is actually the most valuable part of professional education in  university. -- etone
> * The idea that "as long as it doesn't affect my current survival, it's not a problem" is actually very selfish and short-sighted:
>  Your lack of skills in your profession will eventually catch up to you and affect the long-term development of your career.
>  More seriously, students who approach their profession with a passable attitude,
>  their survival is at the expense of the reputation of Nanjing University's education -- if a significant proportion of our graduates are like this,
>  it won't be long before not only those who muddle through to graduation find it hard to survive,
>  but also those who truly work hard will see their prospects affected. -- etone


<!-- ## 实验方案

理解"程序如何在计算机上运行"的根本途径是从"零"开始实现一个完整的计算机系统.
南京大学计算机科学与技术系`计算机系统基础`课程的小型项目
(Programming Assignment, PA)将提出x86/mips32/riscv32(64)架构相应的教学版子集,
指导学生实现一个经过简化但功能完备的x86/mips32/riscv32(64)模拟器NEMU(NJU EMUlator),
最终在NEMU上运行游戏"仙剑奇侠传", 来让学生探究"程序在计算机上运行"的基本原理.
NEMU受到了[QEMU][qemu]的启发, 并去除了大量与课程内容差异较大的部分.
PA包括一个准备实验(配置实验环境)以及5部分连贯的实验内容:
* 图灵机与简易调试器
* 冯诺依曼计算机系统
* 批处理系统
* 分时多任务
* 程序性能优化 -->

## Syllabus

The fundamental way to understand the idea that "how programs run on a computer" is to build a complete computer system from scratch.
The small projects (Programming Assignment, PA) of the "Fundamentals of Computer Systems" course at the Department of Computer Science and Technology, Nanjing University, will present a corresponding teaching subset of the x86/mips32/riscv32(64) architecture.
Students will be guided to implement a simplified yet functionally complete x86/mips32/riscv32(64) emulator, NEMU (NJU EMUlator).
Ultimately, students will run the game "仙剑奇侠传" on NEMU to explore the basic principles of "how programs run on a computer."
NEMU is inspired by [QEMU][qemu] and removes many parts that differ significantly from the course content.
The PA includes a preparatory lab (setting up the lab environment) and five coherent parts:

* Turing Machine and Simple Debugger
* Von Neumann Computer System
* Batch Processing System
* Time-sharing Multitasking
* Program Performance Optimization

[qemu]: http://www.qemu.org

<!-- ## 实验环境

* CPU架构: x64
* 操作系统: GNU/Linux
* 编译器: GCC
* 编程语言: C语言 -->

## Environment of the Programming Assignment

* CPU Architecture: x64
* Operating System: GNU/Linux
* Compiler: GCC
* Programming language: C Programming Language


<!-- ## 如何获得帮助

在学习和实验的过程中, 你会遇到大量的问题.
除了参考课本内容之外, 你需要掌握如何获取其它参考资料.

但在此之前, 你需要适应查阅英文资料.
和以往程序设计课上遇到的问题不同, 你会发现你不太容易搜索到相关的中文资料.
回顾计算机科学层次抽象图, 计算机系统基础处于程序设计的下层.
这意味着, 懂系统基础的人不如懂程序设计的人多, 相应地, 系统基础的中文资料也会比程序设计的中文资料少.

如何适应查阅英文资料? 方法是<font color="red">尝试并坚持查阅英文资料</font>. -->

## How to Get Help

During your study and experiments, you will encounter numerous problems.
In addition to referring to the textbook, you need to know how to access other reference materials.

However, before doing so, you need to adapt to searching for English materials.
Unlike the problems encountered in previous programming courses, you will find it difficult to find relevant Chinese materials.
Reviewing the hierarchy of computer science abstractions, the introduction to computer system is at a lower level than programming language course.
This means that there are fewer people who understand system fundamentals compared to those who understand programming, and accordingly, there are fewer Chinese materials on system fundamentals.

How do you adapt to searching for English materials? The method is to <font color="red">try and persist in searching for English materials</font>.


<!-- ### 搜索引擎, 百科和问答网站

为了查找英文资料, 你应该使用下表中推荐的网站:

| | 搜索引擎 | 百科 | 问答网站|
| --- | --- | --- | --- |
| 推荐使用 | [这里][google]有google搜索镜像 | http://en.wikipedia.org | http://stackoverflow.com |
| 不推荐使用 | ~~http://www.baidu.com~~ | ~~http://baike.baidu.com~~ | ~~http://zhidao.baidu.com~~ <br> ~~http://bbs.csdn.net~~ | -->

### Search Engines, Encyclopedias and Q&A Websites

To find English materials, you should use the websites recommended in the table below:

| | Search Engine | Encyclopedia | Q&A Website |
| --- | --- | --- | --- |
| Recommended | [Here][google] for a mirror of Google search | http://en.wikipedia.org | http://stackoverflow.com |
| Not Recommended | ~~http://www.baidu.com~~ | ~~http://baike.baidu.com~~ | ~~http://zhidao.baidu.com~~ <br> ~~http://bbs.csdn.net~~ |


[google]: https://dir.scmor.com

<!-- 一些说明:
* 一般来说, 百度对英文关键词的处理能力比不上Google.
* 通常来说, 英文维基百科比中文维基百科和百度百科包含更丰富的内容.
为了说明为什么要使用英文维基百科, 请你对比词条`前束范式`分别在[百度百科][baike],
[中文维基百科][wikipedia zh]和[英文维基百科][wikipedia en]中的内容.
* stackoverflow是一个程序设计领域的问答网站,
里面除了技术性的问题([What is ":-!!" in C code?][so1])之外,
也有一些学术性([Is there a regular expression to detect a valid regular expression?][so2])
和一些有趣的问题([What is the “” operator in C++?][so3]). -->

Some explanations:
* Generally, Baidu's ability to handle English keywords is not as good as Google's.
* Typically, English Wikipedia contains richer content compared to Chinese Wikipedia and Baidu Baike.
To illustrate why you should use English Wikipedia, please compare the entry "前束范式" (quantifier phrase) in [Baidu Baike][baike],
[Chinese Wikipedia][wikipedia zh], and [English Wikipedia][wikipedia en].
* Stack Overflow is a Q&A website in the field of programming,
where besides technical questions ([What is ":-!!" in C code?][so1]),
there are also some academic ([Is there a regular expression to detect a valid regular expression?][so2])
and interesting questions ([What is the “-->” operator in C++?][so3]).


[baike]: http://baike.baidu.com/view/143343.htm
[wikipedia zh]: http://zh.wikipedia.org/wiki/%E5%89%8D%E6%9D%9F%E8%8C%83%E5%BC%8F
[wikipedia en]: http://en.wikipedia.org/wiki/Prenex_normal_form
[so1]: http://stackoverflow.com/questions/9229601/what-is-in-c-code/9229793
[so2]: http://stackoverflow.com/questions/172303/is-there-a-regular-expression-to-detect-a-valid-regular-expression
[so3]: https://stackoverflow.com/questions/1642028/what-is-the-operator-in-c

<!-- ### 官方手册

官方手册包含了查找对象的<font color="red">所有</font>信息,
关于查找对象的<font color="red">一切</font>问题都可以在官方手册中找到答案.
通常官方手册的内容十分详细, 在短时间内通读一遍基本上不太可能, 因此你需要懂得"如何使用目录来定位你所关心的问题".
如果你希望寻找一些用于快速入门的例子, 你应该使用搜索引擎.

这里列出一些本课程中可能会用到的手册:
* x86
  * Intel 80386 Programmer's Reference Manual ([PDF][i386 pdf])([HTML][i386 html])
  * [System V ABI for i386][i386 abi]
* mips32
  * MIPS32 Architecture For Programmers ([Volume I][mips32 I], [Volume II][mips32 II], [Volume III][mips32 III])
  * [System V ABI for mips32][mips32 abi]
* riscv32(64)
  * The RISC-V Instruction Set Manual ([Volume I][riscv I], [Volume II][riscv II])
  * [ABI for riscv][riscv abi]
* ISA无关的手册
  * [System V generic ABI](https://refspecs.linuxfoundation.org/elf/gabi41.pdf)
  * [C99 Standard](http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1570.pdf)
  * [GCC 10.3.0 Manual](https://gcc.gnu.org/onlinedocs/gcc-10.3.0/gcc.pdf)
  * [GDB User Manual](https://sourceware.org/gdb/current/onlinedocs/gdb)
  * [GNU Make Manual](http://www.gnu.org/software/make/manual/make.pdf)
  * On-line Manual Pager (即man, [这里](man.md)有一个入门教程)
-->

### Official Manuals

The official manuals contain <font color="red">all</font> the information about the objects you are searching for,
and <font color="red">all</font> questions about the objects can be found in the official manuals.
Usually, the content of official manuals is very detailed, and it is unlikely that you can read through it all in a short time.
Therefore, you need to know "how to use the table of contents to locate the issues you care about."
If you are looking for some examples for quick reference, you should use a search engine.

Here are some manuals that may be used in this course:
* x86
  * Intel 80386 Programmer's Reference Manual ([PDF][i386 pdf])([HTML][i386 html])
  * [System V ABI for i386][i386 abi]
* mips32
  * MIPS32 Architecture For Programmers ([Volume I][mips32 I], [Volume II][mips32 II], [Volume III][mips32 III])
  * [System V ABI for mips32][mips32 abi]
* riscv32(64)
  * The RISC-V Instruction Set Manual ([Volume I][riscv I], [Volume II][riscv II])
  * [ABI for riscv][riscv abi]
* manuals that is unrelated to ISA
  * [System V generic ABI](https://refspecs.linuxfoundation.org/elf/gabi41.pdf)
  * [C99 Standard](http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1570.pdf)
  * [GCC 10.3.0 Manual](https://gcc.gnu.org/onlinedocs/gcc-10.3.0/gcc.pdf)
  * [GDB User Manual](https://sourceware.org/gdb/current/onlinedocs/gdb)
  * [GNU Make Manual](http://www.gnu.org/software/make/manual/make.pdf)
  * On-line Manual Pager (known as man, there is a beginner's tutorial [here](man.md))

[i386 pdf]: http://css.csail.mit.edu/6.858/2013/readings/i386.pdf
[i386 html]: https://nju-projectn.github.io/i386-manual/toc.htm
[i386 abi]: http://math-atlas.sourceforge.net/devel/assembly/abi386-4.pdf
[mips32 I]: http://www.cs.cornell.edu/courses/cs3410/2008fa/MIPS_Vol1.pdf
[mips32 II]: http://www.cs.cornell.edu/courses/cs3410/2008fa/MIPS_Vol2.pdf
[mips32 III]: http://www.cs.cornell.edu/courses/cs3410/2008fa/MIPS_Vol3.pdf
[mips32 abi]: http://math-atlas.sourceforge.net/devel/assembly/mipsabi32.pdf
[riscv I]: https://github.com/riscv/riscv-isa-manual/releases/download/riscv-isa-release-382fd8b-2024-04-11/unpriv-isa-asciidoc.pdf
[riscv II]: https://github.com/riscv/riscv-isa-manual/releases/download/riscv-isa-release-382fd8b-2024-04-11/priv-isa-asciidoc.pdf
[riscv abi]: https://github.com/riscv-non-isa/riscv-elf-psabi-doc

<!-- ### GNU/Linux入门教程

jyy为我们准备了一些GNU/Linux入门教程, 如果你是第一次使用GNU/Linux, 请阅读以下材料
* [流传自远古时代的OS实验课程网站中的Linux入门教程](linux.md)
* [The Missing Semester of Your CS Education(墙裂推荐)][missing] -->

### GNU/Linux introductory tutorial

jyy has prepared some introductory tutorials on GNU/Linux for us. If you are using GNU/Linux for the first time, please read the following materials:
* [Linux introductory tutorial from the OS experiment course website, passed down from ancient times](linux.md)
* [The Missing Semester of Your CS Education (highly recommended)][missing]

[missing]: https://missing.csail.mit.edu/

<!-- ## 许可协议

本作品采用`知识共享 署名-非商业性使用-相同方式共享 3.0 中国大陆`许可协议进行许可.
要查看该许可协议, 可访问[这里][license],
或者写信到 Creative Commons, PO Box 1866, Mountain View, CA 94042, USA. -->

## License Agreement

This work is licensed under `the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Mainland China License`.
To view this license agreement, you can visit [here][license],
or write to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

[license]: http://creativecommons.org/licenses/by-nc-sa/3.0/cn/

