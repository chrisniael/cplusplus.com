宏

# FE_DFL_ENV (C++11)

`fenv_t *`

#### 默认环境

这个宏展开成一个指向 [fenv_t](fenv_t.md) 对象的指针，这个对象是用来为函数 [fesetenv](fesetenv.md) 和 [feupdateenv](feupdateenv.md) 选择 _默认环境_ 的。

_默认环境_ 是程序刚启动时的 _浮点环境_ 的状态。


## 另请参见

函数/类型                     | 描述
----------------------------- | ---------------------
[fesetenv](fesetenv.md)       | 设置浮点环境 (_函数_)
[feupdateenv](feupdateenv.md) | 更新浮点环境 (_函数_)
[fenv\_t](fenv_t.md)          | 浮点环境类型 (_类型_)
