类型

# fenv_t (C++11)

#### 浮点环境类型

表示整个 _浮点环境_ 状态的类型，包括它的 _状态标志_（例如有效的 _浮点异常_ ）和 _控制模式_ （例如 _舍入方向_ ）。

这个类型的具体细节取决与库实现：它的值会被 [fegetenv](fegetenv.md) 或 [feholdexcept](feholdexcept.md) 设置，还可以被应用于 [fesetenv](fesetenv.md) 或 [feupdateenv](feupdateenv.md) 的调用。


## 另请参阅

函数/类型                 | 描述
------------------------- | ---------------------
[fegetenv](fegetenv.md)   | 获取浮点环境 (_函数_)
[fesetenv](fesetenv.md)   | 设置浮点环境 (_函数_)
[fexcept_t](fexcept_t.md) | 浮点异常类型 (_类型_)
