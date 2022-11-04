# dailySchedule

## 任务清单

- [ ] **rust**
- [x] rustlings
- [x] rust trait
- [x] 32 Rust Quizes
- [ ] rust [宏小册](https://danielkeep.github.io/tlborm/book/index.html)
- [ ] rust [宏小册续写](https://veykril.github.io/tlborm/)
- [ ] [exercisms.io](https://exercism.org/) 快速练习
- [ ] **risc-v**
- [x] risc-v 特权架构
- [x] risc-v 指令集指南
- [ ] 计算机组成与设计 risc-v版
- [ ] riscv-privileged-20211203
- [ ] riscv-spec-20191213
- [ ] **rCore-Tutorial-Book-v3**
- [x] ch_0
- [x] ch_1
- [x] ch_2
- [ ] **lab**
- [x] lab_0_0
- [x] lab_0_1

## 第一天（2022.10.24）

- 开始刷rustlings

## 第二天（2022.10.25）

- 刷完rustlings
- 遇上的trait和marcos不太熟悉，明天再学

## 第三天 (2022.10.26)

- 复习了一些trait
- Any trait, Hash trait, Error trait等
- 大致翻阅了RISC-V 特权指令级架构，没看懂。

## 第四天 (2022.10.27)

- 去官网找到了原版的特权架构文档，看完CSR
- 学习marco, 做完quiz, 了解到捕获字符的一些特殊行为
- 智能指针找方法顺序-> 先在当前变量找,再在当前变量引用找,最后在解引用里找,由于存在自动解引用这一行为,可以套娃
- drop的顺序是反序,变量越靠后越先drop
- marco展开的变量有不会影响当前作用域,也不会被影响, 但是和当前作用域同一个lifetime

## 第五天 (2022.10.28)

- 把特权架构文档后续扫了一遍，导致知道在干什么，但细节没法理解。
- 翻看中文的RISC-V指令集指南，挺好理解的，目前看到第四章

## 第六天 (2022.10.29)

- 看完中文的RISC-V指令集指南，最重要的第十章大致明白了。
- 前面章节的其实有点模糊，需要搭建实验实践才能明白其中的细节
- 用docker生成的容器配置实验环境，启动容器挂载宿主机的git仓库。
- 使用docker时发现宿主机的git全局设置中也会移植到容器中，导致容器出现网络问题。

## 第七天 (2022.10.30)

- 看了《计算机组成与设计》的前两章，有点理解前几天看的东西了

## 第八天 (2022.11.2)

- `这个方法负责将参数 app_id 对应的应用程序的二进制镜像加载到物理内存以 0x80400000 起始的位置， 这个位置是批处理操作系统和应用程序之间约定的常数地址`
- 看完lab_0_1, 大致理解整个工程的流程，不过得回去看书，不然后面跟不上

## 第九天 (2022.11.3)

- 花了半天学rescript, 晚上再看rCore(一开始还以为rCore tutorial和lab是一样的)
- Qemu 模拟的启动流程则可以分为三个阶段：第一个阶段由固化在 Qemu 内的一小段汇编程序负责；第二个阶段由 bootloader 负责；第三个阶段则由内核镜像负责
- 看完第1章，对段有比较深的理解，还有了解到rustsbi这个中间的接口
- rust的asm!宏比较诡异，明天看看

## 第十天 (2022.11.4)

- 对于linker语法不太理解，大概学了一点基本语法。[一个简单的介绍](https://blog.csdn.net/m0_47799526/article/details/108765403)(看起来质量还可以)
- 看完了rcore第二章，对用户态和内核态有了进一步的理解，