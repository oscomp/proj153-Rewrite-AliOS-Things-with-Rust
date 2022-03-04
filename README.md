# 用Rust重写AliOS Things内核

### 项目描述

[AliOS Things](https://github.com/alibaba/AliOS-Things/) 是阿里云IoT事业部发布的面向IoT领域的、高可伸缩的物联网操作系统。拥有弹性内核rhino，和丰富的云端一体的IoT组件，以及HaaS Python/JS框架以支持利用Python/JS语言进行开发。目前已被广泛应用于智能音箱、IP摄像头等智能家居、安防等领域。 其中内核rhino是用C语言自主设计实现的，主要包括调度、任务管理、内存管理、任务同步（互斥量、信号量、事件）、消息队列、时间管理、软件定时器等功能。

本项目旨在用Rust语言重新设计与实现AliOS Things的内核rhino的基础功能。由于Rust语言的高性能，与C语言的交互性，特别是Rust语言的数据类型和所有权的内存模型，以及强大的静态分析能力，这些语言特性将天然地给底层系统带来强大的稳定性。

### 所属赛道

2022全国大学生操作系统比赛的“OS功能挑战”赛道

### 参赛要求

* 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的学生（本科生/研究生均可）
* 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖

* 请遵循“2022国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

* 李进良
* email: ljl150821@alibaba-inc.com

### 难度

中等 

### 特征

* 使用 Rust 语言实现AliOS Things内核rhino
* 至少支持RISC-V 32/64平台
* 支持QEMU RISC-V仿真和Kendryte K210开发板

### 参考实现

* [Rewritten Free RTOS in RUST](https://github.com/OSH-2019/x-rust-freertos)

### License

* Apache 2.0 license (<https://www.apache.org/licenses/LICENSE-2.0>)

## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

### 第一题：从零开始

* 参考AliOS Things内核rhino的C语言版本(<https://github.com/alibaba/AliOS-Things/tree/master/kernel/rhino>)， 实现rhino中的调度（必选FIFO调度策略，可选RR/CFS调度）、任务管理、内存管理、互斥量、信号量、消息队列、时间管理模块。
* 提供基本的测试用例（Rust语言）, 覆盖所实现的功能模块

* 支持RISCV平台 (AliOS Things已支持RISC-V架构 <https://github.com/alibaba/AliOS-Things/tree/master/hardware/arch/riscv>)
* 支持AliOS Things的aos C语言接口( [https://haas.iot.aliyun.com/aliosthings/aos\_kernel.html](https://haas.iot.aliyun.com/aliosthings/aos_kernel.html))

* 支持QEMU RISC-V仿真器，可验证

### 第二题：丰富内核功能

* 更进一步用Rust语言实现内核rhino的全部功能

### 第三题：实现对各种上层应用的支持

* 通过常见的C库（newlib）
* 支持常见应用程序，例如AliOS Things的linksdk组件。

### 第四题：移植到其它各种开发板上

* Kendryte K210开发板
* D1哪吒开发板
* 其他ARM开发板（HaaS EDU K1/HaaS200）
