函数

# feclearexcept (_C++11_)

\<cfenv\>

`int feclearexcept(int excepts);`

#### 清除浮点异常

试图清除 _excepts_ 指定的浮点异常。

调用这个函数的程序需要确保在本次函数调用中，编译指示 [FENV_ACCESS](FENV_ACCESS.md) 已经开启。


## 参数

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

特定的库实现可能会支持附加的 _浮点异常_ 值（和它们对应的同样以 FE_ 开头的宏）。

#### C99

库可能定义在 [\<fenv.h\>](README.md)，仅仅支持上面这些宏值（其他可能没有被定义）。

#### C++11

至少上面所有的宏值都定义在 [\<fenv.h\>](README.md) 中（即使实现不支持）。


## 返回值

如果所有在 _excepts_ 中的异常都被清除的话（或者 _excepts_ 为 0 ），则返回 0 ，其他返回非 0 。


## 例子

```cpp
/* feclearexcept, fetestexcept example */
#include <stdio.h> /* printf */
#include <math.h> /* sqrt */
#include <fenv.h> /* feclearexcept, fetestexcept, FE_ALL_EXCEPT, FE_INVALID */
#pragma STDC FENV_ACCESS on

int main()
{
	feclearexcept(FE_ALL_EXCEPT);
	sqrt(-1);
	if(fetestexcept(FE_INVALID))
		printf("sqrt(-1) raises FE_INVALID\n");
	return 0;
}
```

可能的输出：   
```
sqrt(-1) raises FE_INVALID
```


## 数据竞争

每个线程都保持着分离的、拥有自己状态的 _浮点环境_ 。产生一个新线程就复制当前状态。[ 这个适用于 C11 和 C++11 的实现 ]


## 异常

不抛出异常的保证：这个函数从不抛出异常。  
注意 C _浮点环境异常_ 不是 C++ 异常，因此不能被 _try/catch_ 块捕捉。  
调用这个函数的时候，如果编译指示 [FENV_ACCESS](FENV_ACCESS.md) 关闭的话，则会导致未定义行为。


## 另请参见

函数                              | 描述
--------------------------------- | ---------------------
[feraiseexcept](feraiseexcept.md) | 触发浮点异常 (_函数_)
[fetestexcept](fetestexcept.md)   | 测试浮点异常 (_函数_)
