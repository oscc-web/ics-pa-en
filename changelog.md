
<!-- ## 更新日志 -->
## ChangeLog

### ICS2023

#### nemu

### ICS2024

#### nemu

1. 特性
* 提升在AM上运行时的随机性
([补丁](https://github.com/NJU-ProjectN/nemu/commit/fa6e67fcbbdddab62c738962072ea62b2c9e3938))
* 使用capstone替换LLVM进行反汇编
([补丁](https://github.com/NJU-ProjectN/nemu/commit/1a493f9c0b433af2fbddabeb9c186bd55ccd4ad1))
1. 性能
* 物理内存的初始化只采用1个随机字节, 大幅提升该步骤的性能
([补丁](https://github.com/NJU-ProjectN/nemu/commit/4fbe3ab3ba70a2cc6af0e2698a4041e89ac4dfc0))
1. 修复
* 修复在AM上无法调用文件操作的问题
  ([补丁](https://github.com/NJU-ProjectN/nemu/commit/feea23db1987c80b3447c7966cc11a40b9f96a51))
  * 修复关闭窗口后仍无法退出的问题
([补丁](https://github.com/NJU-ProjectN/nemu/commit/da81fe5054d69c8d14d511bdcdca816fb1bcc5fd))
* 修复将NEMU编译到`riscv64-nemu`时, NEMU中的ISA为`riscv32`的错误
([补丁](https://github.com/NJU-ProjectN/nemu/commit/7b57ba5d759fa6c18f7923ef985ae89d138b6196))
* 修复在打开日志文件前调用`Log`导致段错误的问题
([补丁](https://github.com/NJU-ProjectN/nemu/commit/fc81a8f7b4e9da6c3dff68943082e8094f41bc3c))
* 修复`utils.h`中`ANSI_BG_MAGENTA`的定义错误
([补丁](https://github.com/NJU-ProjectN/nemu/commit/bbbf9e3ac1cbf53ae754d19a5dcf406b630d4e1e))
1. 构建
* 源文件无变化时无需重新链接
  ([补丁](https://github.com/NJU-ProjectN/nemu/commit/f2e7323a2fa3a110f46780fd3b41365fefa39960))
  * 修复`CONFIG_CC`为空时导致编译失败的问题
([补丁](https://github.com/NJU-ProjectN/nemu/commit/7972a459ba5932cb291057167cb3242416fcde6c))
* 修复在macOS上SDL2库路径错误的问题

#### abstract-machine

([补丁](https://github.com/NJU-ProjectN/nemu/commit/2fd67c07edff1f60dc4cef57d1df41f353581485))
1. 文档
 * 修复`config.mk`中的文字错误
([补丁](https://github.com/NJU-ProjectN/nemu/commit/d0ca3cfda4cd96ded866a520b13a0829029a675f))

#### abstract-machine

1. 特性
* 在native中添加UART
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/493a0650ce0960e52e56d6d7500dccb56142bd08))
* 为npc添加`uart_config`函数
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/c383159000a2975dabde43f221deae3d54bc48b0))
* 为`riscv??-nemu`的`_start`符号添加大小属性
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/90ae4830e39a69c8652061a1758551a63098afb8))
* 添加`riscv32mini-nemu`
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/56d4ae7165293bdbb06aa386d904e6a3e4621b23))
* 为native新增其他架构
* aarch64([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/fe84c58450fd50f38bc500220b24c1f3bfbb5e70))
* riscv64([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/a7b830fedd86505e8accba8f4b928084542c841a))
1. 修复
* 修复`riscv??-nemu`的`trap.S`中的寄存器数量错误
  ([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/f198eb6073383c1e0a5201be42b43c609082264e))
  * 修复使用clang时libgcc中的编译错误
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/62ca04d426865cce1ab55483a8b1ae6a6cf71f62))
* 修复编译预处理指示符
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/acd889e89c8f043f74af96a3f060db777f821ee3))
* 修复链接时`jal`跳转距离不够的错误
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/031dd9d93104468c7681ce3c72b1a3d1d33f6dea))
* 修复`x86-qemu`中boot相关的strict aliasing bug

#### am-kernels

([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/de78d6ca0a5d399c55f9bae489239f5542d20fe7))
1. 重构
* 去除klib中的无用代码

#### navy-apps

([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/bcdbc4e249627e7a65eb0de51ec7507c1f9bbaf1))
* 简单重构native GPU中`W`和`H`相关的代码
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/e6f833c3b93f42080ee90bdf286c76fa364b4df5))
1. 构建
* 去除`Makefile`的`image-dep`规则中的冗余依赖
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/3ba0c6afd76fffe249f5d076d9f631a6e6d4fe36))
* 避免Linux上的其他动态库链接到ELF中的符号
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/fa82955135ef6b93b711ec8c3b4e30c3a75c6fc7))
* 重构依赖规则
* 修复源文件无变化时仍然重新链接的问题
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/c3ffbc97c39d5374c3e4f182eaaa8ae7bdc0e98e))
* 将`mainargs`注入到bin文件, 避免重复编译`trm.c`

### ICS2022

#### nemu

([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/c52a41181f8ea5d0e970008e51f58867a3ce65bb))
* 将链接脚本添加到依赖规则
[补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/84051a9071557010554b6535408a15293ffa5892))
* 不显示native的链接命令
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/befa0459648bdf3821dc71e46673f443977ec337))
* 让native的IOE通过`sdl2-config`找到`SDL.h`
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/61a35370c9ea634aeef69c5faacf2bb146a50230))
* 修复`x86-qemu`中`array subscript 0 is outside array bounds`的警告
([补丁](https://github.com/NJU-ProjectN/abstract-machine/commit/0e37b474981568f2790f75f5d1105bbb2509515c))


#### am-kernels

1. 特性
* 新增若干测试
* `yiels-os`([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/6f4a47afb9d6ca1872b52ec5ebaa0351d3549c71))
* `bad-apple`([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/7bb7b1a94fb13729dcc8ce4b384fff47caeb04ec))
* `blockchain`([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/3bdc2529639606a92d23e921542fc1ec95c68af6)和
[补丁](https://github.com/NJU-ProjectN/am-kernels/commit/a799b79f5f470986e1cdd2b594ef1300927da0e3))

#### abstract-machine

* 假设`uptime`不从0开始, 从而支持`typing-game`的重新运行
([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/ade50b257ac81f21f82fdba6c2e9c80cc2b7a17b))
* 让benchmark出错时向TRM返回非0值
([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/2e7c5934eda067ca2b116d23fb567b7090ef0a44))
1. 性能
* 加速`typing-game`清屏的过程
  ([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/d41f447c17f387a10dee3ad750a7b5d8d0c2d264))
  1. 修复

#### am-kernels

* 修复`keyboard-test`中`char`符号问题
([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/33c0dd0d8510c27678f230b9c2799a7fe91324a0))

#### nanos-lite

* 修复`game of life`的栈溢出问题
([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/0c1f038ad0f50de57f806d24343ea93b102be732))

#### navy-apps

* 修复`hanoi`中屏幕不刷新的问题
([补丁](https://github.com/NJU-ProjectN/am-kernels/commit/3c50c2eae3d9d001f33cae089c87cf9a51630669))
