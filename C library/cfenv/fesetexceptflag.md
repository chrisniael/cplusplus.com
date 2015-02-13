函数

# fesetexceptflag (C++11)

`int fesetexceptflag(const fexcept_t *flagp, int excepts);`

#### 设置浮点异常标志

Attempts to set the exceptions indicated by excepts with the states stored in the object pointed by flagp.

如果成功，则函数会改变当前 _浮点环境_ 的状态，设置请求的异常标志，但不会真正 _触发_ 异常。

调用这个函数的程序需要确保在本次函数调用时，编译指示 [FENV_ACCESS](FENV_ACCESS.md) 已经开启。


## 参数

`flagp`

指向 [fexcept_t](fexcept_t.md) 对象的指针，用来表示浮点异常。_flagp_ 指向的对象应该在之前被函数 [fegetexceptflag](fegetexceptflag.md) 通过参数 _excepts_ 已经设置了值。

`excepts`

位掩码值：支持的任何浮点异常数字的组合（按位 OR）：

宏值                              | 描述
--------------------------------- | --------------------------------------------------------------
[FE_DIVBYZERO](FE_DIVBYZERO.md)   | 极错误：被 0 除，或一些其他渐进无限的结果（从有限的参数）。
[FE_INEXACT](FE_INEXACT.md)       | 不精确：结果不准确。
[FE_INVALID](FE_INVALID.md)       | 作用域错误：至少一个参数是函数没有定义的值。
[FE_OVERFLOW](FE_OVERFLOW.md)     | 上溢错误：结果太大了，超出了返回值类型能表示的数量级。
[FE_UNDERFLOW](FE_UNDERFLOW.md)   | 下一错误：结果太小了，超出了返回值类型能表示的数量级。
[FE_ALL_EXCEPT](FE_ALL_EXCEPT.md) | 所有异常（选择实现支持的所有异常）

特定的库实现可能会支持附加的 _浮点异常_ 值（它们对应的宏同样以 FE_ 开头的宏）。

#### C99

库可能定义在 [\<fenv.h\>](README.md)，仅仅支持上面这些宏值（其他可能没有被定义）。

#### C++11

至少上面所有的宏值都定义在 [\<fenv.h\>](README.md) 中（即使实现不支持）。


## 返回值

如果函数成功 set the flags in the (or if _excepts_ was zero)，则返回 0 ，否则返回非 0 。


## 数据竞争

每个线程都保持着分离的、拥有自己状态的 _浮点环境_ 。产生一个新线程就复制当前状态。[ 这个适用于 C11 和 C++11 的实现 ]


## 异常

不抛出异常的保证：这个函数从不抛出异常。  
注意 C _浮点环境异常_ 不是 C++ 异常，因此不能被 _try/catch_ 块捕捉。  
调用这个函数的时候，如果编译指示 [FENV_ACCESS](FENV_ACCESS.md) 关闭的话，则会导致未定义行为。


## 另请参见

函数                                  | 描述
------------------------------------- | -------------------------
[fegetexceptflag](fegetexceptflag.md) | 获取浮点异常标志 (_函数_)
[feraiseexcept](feraiseexcept.md)     | 触发浮点异常 (_函数_)
