1、非法内存访问 空指针，野指针访问 数组越界
2、栈溢出  无限递归  超大局部变量char buf[100*1024*1024];
3、非法指令 执行了cpu不支持的指令 __asm__("ud2");
4、除零错误
5、Abort 程序主动终止 abort(); assert(false);
6、未捕获异常
7、多线程问题  访问已释放对象 多线程未加锁
8、内存破坏
9、double free
10、使用已释放内存
11、OOM内存耗尽
12、信号导致
    SIGSEGV	非法内存访问
    SIGABRT	abort/assert
    SIGFPE	除零
    SIGILL	非法指令
    SIGBUS	总线错误
    SIGTRAP	调试断点
    SIGSYS	非法系统调用