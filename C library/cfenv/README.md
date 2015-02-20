头文件

# \<cfenv\> (fenv.h) (C++11)

#### 浮点环境

这个头文件声明了一系列函数和宏来访问浮点环境，以及特定类型。

这个浮点环境维持了一系列 _状态标志_ 和特定的 _控制模式_ 。浮点环境的特定内容依赖于实现，但 _状态标志_ 通常包含了 _浮点异常_ 和它们关联的信息， _控制模式_ 至少包含了舍入方向。


## 函数

### 浮点异常

函数名                                | 描述
------------------------------------- | -------------------------
[feclearexcept](feclearexcept.md)     | 清除浮点异常 (_函数_)
[feraiseexcept](feraiseexcept.md)     | 触发浮点异常 (_函数_)
[fegetexceptflag](fegetexceptflag.md) | 获得浮点异常标志 (_函数_)
[fesetexceptflag](fesetexceptflag.md) | 设置浮点异常标志 (_函数_)

### 舍入方向

函数                        | 描述
--------------------------- | -------------------------
[fegetround](fegetround.md) | 获得舍入方向模式 (_函数_)
[fesetround](fesetround.md) | 设置舍入方向模式 (_函数_)

### 整个环境

函数名                          | 描述
------------------------------- | ---------------------
[fegetenv](fegetenv.md)         | 获得浮点环境 (_函数_)
[fesetenv](fesetenv.md)         | 设置浮点环境 (_函数_)
[feholdexcept](feholdexcept.md) | 保留浮点环境 (_函数_)
[feupdateenv](feupdateenv.md)   | 更新浮点环境 (_函数_)

### 其他

函数名                          | 描述
------------------------------- | -------------------------
[fetestexcept](fetestexcept.md) | 测试浮点环境异常 (_函数_)


## 类型

类型名                     | 描述
-------------------------- | ----------------------
[fenv\_t](fenv_t.md)       | 浮点环境类型 (_类型_)
[fexcept\_t](fexcept_t.md) | 浮点异常类型 (_类型_)


## 宏常量

### 浮点异常

宏名                                | 描述
----------------------------------- | -----------------------
[FE\_DIVBYZERO](FE_DIVBYZERO.md)    | 极异常 (_宏_)
[FE\_INEXACT](FE_INEXACT.md)        | 不精确的结果异常 (_宏_)
[FE\_INVALID](FE_INVALID.md)        | 无效参数异常 (_宏_)
[FE\_OVERFLOW](FE_OVERFLOW.md)      | 向上溢出错误异常 (_宏_)
[FE\_UNDERFLOW](FE_UNDERFOW.md)     | 向下溢出错误异常 (_宏_)
[FE\_ALL\_EXCEPT](FE_ALL_EXCEPT.md) | 所有异常 (_宏_)


### 舍入方向

宏名                               | 描述
---------------------------------- | -------------------
[FE\_DOWNWARD](FE_DOWNWARD.md)     | 向下舍入模式 (_宏_)
[FE\_TONEAREST](FE_TONEAREST.md)   | 四舍五入模式 (_宏_)
[FE\_TOWARDZERO](FE_TOWARDZERO.md) | 朝零舍入模式 (_宏_)
[FE\_UPWARD](FE_UPWARD.md)         | 向上舍入模式 (_宏_)

### 整个环境

宏名                          | 描述
----------------------------- | ---------------
[FE\_DFL\_ENV](FE_DFL_ENV.md) | 默认环境 (_宏_)



## 编译指示

编译指示名                     | 描述
------------------------------ | ------------------------
[FENV\_ACCESS](FENV_ACCESS.md) | 访问浮点环境 (_编译指示_)
