noexcept 不会抛异常 // 提升性能

const 不允许修改成员变量 保证接口安全

mutable 突破const 例如mutable int cache; 即使在const函数中也能修改

explicit 构造函数 避免隐式转换

override 重写检查 编译器检查你是否真的重写了父类函数

final  禁止进程/重写检查

inline  内联函数，减少函数调用开销

static 成员函数，没有this指针，不能访问非static成员

= default 默认实现

= delete 禁止使用

volatile 变量可能被外部修改，硬件、中断 volatile int x;

constexpr 编译器就完成计算



