类型

# fexcept_t (C++11)

#### 浮点异常类型

可以表示所有 _浮点状态标志_ 的类型，包括有效的 _浮点异常_ 和任何实现相关状态的附加信息。

这个类型的具体细节取决与库实现：它的值会被 [fegetexceptflag](fegetexceptflag.md) 设置，还可以被应用于 [fesetexceptflag](fesetexceptflag.md) 的调用。


## 另请参阅

函数/类型               | 描述
----------------------- | ---------------------
[fegetenv](fegetenv.md) | 获取浮点环境 (_函数_)
[fesetenv](fesetenv.md) | 设置浮点环境 (_函数_)
[fenv_t](fenv_t.md)     | 浮点环境类型 (_类型_)
