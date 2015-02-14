宏

# FE_INVALID (C++11)

`int`

#### 无效参数异常

这个宏展开成一个 _int_ 型的值，用来表示触发 _无效参数_ 时的 _浮点异常_ 。

_无效参数异常_ 被触发用来提醒 传递给函数的参数超出了它的定义域（也就是，函数不是为那个值而定义的），比如 [sqrt](../cmath/sqrt.md)(-1.0)。

触发这个异常的函数的返回值是不明确的。

_FE_INVALID_ 被定义为 2 的整数次方，允许和多个 _浮点异常_ 组合（使用按位 OR 操作：| ）成为单个值：

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
_FE_DIVBYZERO_ 总是被定义，如果 [math_errhandling](../cmath/math_errhandling.md) 有 _MATH_ERREXCEPT_ 集合。 

#### C++11

至少上面所有的宏值都定义在 [\<fenv.h\>](README.md) 中（即使实现不支持）。


## 另请参见

宏名                                | 描述
----------------------------------- | -----------------------
[FE\_DIVBYZERO](FE_DIVBYZERO.md)    | 极异常 (_宏_)
[FE\_INEXACT](FE_INEXACT.md)        | 不精确的结果异常 (_宏_)
[FE\_OVERFLOW](FE_OVERFLOW.md)      | 向上溢出错误异常 (_宏_)
[FE\_UNDERFLOW](FE_UNDERFOW.md)     | 向下溢出错误异常 (_宏_)
[FE\_ALL\_EXCEPT](FE_ALL_EXCEPT.md) | 所有异常 (_宏_)
