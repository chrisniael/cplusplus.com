宏

# FE_OVERFLOW (C++11)

`int`

#### 上溢错误异常

这个宏展开成一个 _int_ 型的值，用来表示触发 _上溢错误_ 时的 _浮点异常_ 。

_上溢错误_ 出现在因为操作结果的数量级太大（符号为正或负）而不能被返回值类型表示的时候。

上溢的操作返回一个正或负的 [HUGE_VAL](../cmath/HUGE_VAL.md) （或 [HUGE_VALF](../cmath/HUGE_VALF.md)），或 [HUGE_VALL](../cmath/HUGE_VALL.md)，并且会影响默认的 _舍入模式_ 。

_FE_OVERFLOW_ 被定义为 2 的整数次方，允许和多个 _浮点异常_ 组合（使用按位 OR 操作：| ）成为单个值：

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

库可能定义在 [&lt;fenv.h&gt;](README.md)，仅仅支持上面这些宏值（其他可能没有被定义）。  
_FE_OVERFLOW_ 总是被定义，如果 [math_errhandling](../cmath/math_errhandling.md) 有 _MATH_ERREXCEPT_ 集合。

#### C++11

至少上面所有的宏值都定义在 [&lt;fenv.h&gt;](README.md) 中（即使实现不支持）。


## 另请参见

宏名                                | 描述
----------------------------------- | -----------------------
[FE_DIVBYZERO](FE_DIVBYZERO.md)    | 极异常 (_宏_)
[FE_INEXACT](FE_INEXACT.md)        | 不精确的结果异常 (_宏_)
[FE_INVALID](FE_INVALID.md)        | 无效参数异常 (_宏_)
[FE_UNDERFLOW](FE_UNDERFOW.md)     | 向下溢出错误异常 (_宏_)
[FE_ALL_EXCEPT](FE_ALL_EXCEPT.md) | 所有异常 (_宏_)
