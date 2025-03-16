# 🖥️ OS-Principles-Demo | 操作系统原理演示

[![Java Version](https://img.shields.io/badge/Java-17%2B-blue)](https://www.oracle.com/java/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

> 基于Java实现的操作系统核心原理演示系统，包含进程调度、内存管理等核心模块的模拟实现

## 🌟 核心特性
### 🚦 进程调度模块
- **抢占式优先级调度算法**  
  _动态调整进程优先级，支持实时队列状态可视化_
- 进程状态管理（就绪/运行/阻塞）
- 时间片轮转机制
- 优先级动态衰减策略

### 🧠 内存管理模块
- **LRU页面置换算法**  
  _实现位移寄存器模拟访问频次统计_
- 分页式内存管理
- 缺页中断处理
- 物理块分配策略

### 🧩 系统模拟
```text
+-- org.example
    +-- entity
    │   ├── Order.java       # 指令实体（READ/WRITE/INPUT/OUTPUT）
    │   ├── PageTable.java   # 页表管理（页号/块号/状态位）
    │   └── PCB.java         # 进程控制块（优先级/指令集/页表）
    +-- simulate
    │   └── Simulate.java    # 系统主控模块
    +-- util
        ├── InitUtil.java    # 内存&进程初始化
        ├── RunUtil.java     # 调度算法实现
        └── ShowUtil.java    # 系统状态可视化
```

## 🛠️ 技术栈

|     组件     |             技术实现            |
|:------------:|:------------------------------:|
|   编程语言   |            Java 17             |
|   调度算法   |     抢占式优先级调度            |
|   内存管理   |    LRU页面置换算法              |
|   开发工具   |        IntelliJ IDEA          |


## 🎮 输出示例
```text
------------------------Time Slice 5------------------------

Ready Processes:
-------------------------------------------------------------
PID     Process Name    Priority    Status      Running Time
0       p1              52          READY           2
1       p2              33          READY           1

Running Process:
-------------------------------------------------------------
PID     Process Name    Priority    Status      Running Time
2       p3              11          RUNNING         3

Page Table:
-------------------------------------------------------------
Page Number     Block Number    Status      Access
0               25              1           0
1               -1              0           0

[SYSTEM] Process p3 executed WRITE operation on page 2
[ALERT] Page fault occurred, replacing page 1 with page 2
```
## ⭐ 如果本项目对你有帮助，请点击 Star 支持！If this project helps you, please give it a star!

<div align="center">

[![Star History Chart](https://api.star-history.com/svg?repos=yukito0209/simple-demonstration-of-operating-system-principles&type=Date)](https://star-history.com/#yukito0209/simple-demonstration-of-operating-system-principles&Date)

</div>