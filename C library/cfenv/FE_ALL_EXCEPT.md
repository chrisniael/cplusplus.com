宏

# FE_ALL_EXCEPT (C++11)

`int`

#### 所有异常

这个宏展开成一个 _int_ 型的值，它组合了所有定义在 [&lt;cfenv&gt;](../README.md) 中的 _浮点异常_ 值（用按位 OR  ）。

如果实现不支持 _浮点异常_ ，那么这个宏被定义为 0 。

它可以被用于哪些期望用 _浮点异常_ 的位掩码作为参数的函数：  
[feclearexcept](feclearexcept.md)，[fegetexceptflag](fegetexceptflag.md)，[feraiseexcept](feraiseexcept.md)，[fesetexceptflag](fesetexceptflag.md)，或者 [fetestexcept](fetestexcept.md)。


#### C99

它是所有实现的 _浮点异常_ 宏值的组合，可能包括下面这些（加上其他特定实现的异常）：

#### C++11

它是所有实现的 _浮点异常_ 宏值的组合，包括下面这些（加上其他特定实现的异常）：

宏值                              | 描述
--------------------------------- | --------------------------------------------------------------
[FE_DIVBYZERO](FE_DIVBYZERO.md)   | 极错误：被 0 除，或一些其他渐进无限的结果（从有限的参数）。
[FE_INEXACT](FE_INEXACT.md)       | 不精确：结果不准确。
[FE_INVALID](FE_INVALID.md)       | 作用域错误：至少一个参数是函数没有定义的值。
[FE_OVERFLOW](FE_OVERFLOW.md)     | 上溢错误：结果太大了，超出了返回值类型能表示的数量级。
[FE_UNDERFLOW](FE_UNDERFLOW.md)   | 下一错误：结果太小了，超出了返回值类型能表示的数量级。
[FE_ALL_EXCEPT](FE_ALL_EXCEPT.md) | 所有异常（选择实现支持的所有异常）


## 另请参见

宏名                              | 描述
--------------------------------- | -----------------------
[FE_DIVBYZERO](FE_DIVBYZERO.md)  | 极异常 (_宏_)
[FE_INEXACT](FE_INEXACT.md)      | 不精确的结果异常 (_宏_)
[FE_INVALID](FE_INVALID.md)      | 无效参数异常 (_宏_)
[FE_OVERFLOW](FE_OVERFLOW.md)    | 向上溢出错误异常 (_宏_)
[FE_UNDERFLOW](FE_UNDERFOW.md)   | 向下溢出错误异常 (_宏_)
[feraiseexcept](feraiseexcept.md) | 触发浮点异常 (_函数_)
