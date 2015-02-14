函数

# feholdexcept (C++11)

`int feholdexcept(fenv_t *envp);`

#### 保留浮点异常

保存 _浮点环境_ 的当前状态至 _envp_ 指向的对象中。然后会重置当前状态，并且如果支持的话会设置环境为 _non-stop_ 模式。

调用这个函数的程序需要确保在本次函数调用时，编译指示 [FENV_ACCESS](FENV_ACCESS.md) 已经开启。


## 参数

`envp`

要么是指向 [fenv_t](fenv_t.md) 对象的指针，要么是 _浮点环境_ 的宏值之一：


## 返回值
