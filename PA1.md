# 关于PA1的絮絮叨叨

PA1了（喘气、擦汗）

## 作业

### 1. 尝试理解计算机如何计算

计算机分为计算和控制，RISC架构cpu通过将复杂的计算分解为简单的计算，在加上流程控制，实现复杂的运算；并且通过对内存空间的读写完成数据交互和IO操作

### 2. 从状态机视角理解程序运行

(0, x, x) -> (1, 0, x) -> (2, 0, 0) -> (3, 0, 1) -> (4, 1, 1) 
                       -> (2, 1, 1) -> (3, 1, 2) -> (4, 3, 2) 

                       -> ...
                       
                       -> (2, 4751, 98) -> (3, 4751, 99) ->(4, 4850, 99) 
                       -> (2, 4850, 99) -> (3, 4850, 100) ->(4, 4950, 100) 

### 3.  优美地退出(代码已修改)
为了测试大家是否已经理解框架代码, 我们给大家设置一个练习: 如果在运行NEMU之后直接键入q退出, 你会发现终端输出了一些错误信息. 请分析这个错误信息是什么原因造成的, 然后尝试在NEMU中修复它.

### 4.  实现单步执行, 打印寄存器, 扫描内存
熟悉了NEMU的框架之后, 这些功能实现起来都很简单, 同时我们对输出的格式不作硬性规定, 就当做是熟悉GNU/Linux编程的一次练习吧.

NEMU默认会把单步执行的指令打印出来(这里面埋了一些坑, 你需要RTFSC看看指令是在哪里被打印的), 这样你就可以验证单步执行的效果了.

不知道如何下手? 嗯, 看来你需要再阅读一遍RTFSC小节的内容了. 如果你已经忘记了某些注意事项, 重新去阅读一遍也是应该的.