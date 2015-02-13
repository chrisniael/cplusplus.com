函数

# fegetexeptflag (C++11)

`int fegetexeptflag(fexcept_t *flagp, int excepts);`

#### 获取浮点异常标志

尝试把浮点异常 _excepts_ 存储在 [fexcept_t](fexcept_t.md) 对象 _flagp_ 中。

## 参数

`flagp`

指明存储标志的 [fexcept_t](fexcept_t.md) 对象。

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

如果标志被成功存储的话（或者 _excepts_ 为 0 ），则返回 0 ，否则返回非 0 。


## 数据竞争

同时调用这个函数是安全的，不导致数据竞争。


## 异常

不抛出异常的保证：这个函数从不抛出异常。  


## 另请参见

函数                                  | 描述
------------------------------------- | -------------------------
[fesetexceptflag](fesetexceptflag.md) | 设置浮点异常标志 (_函数_)
[feholdexcept](feholdexcept.md)       | 保留浮点异常 (_函数_)
