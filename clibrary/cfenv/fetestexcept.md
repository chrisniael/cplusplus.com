函数

# fetestexcept (C++11)

`int fetestexcept(int excepts);`

#### 测试浮点异常

返回在 _excepts_ 中当前设置的异常。

返回值是用按位或表示的 _excepts_ 中被当前 _浮点环境_ 设置的异常的集合。如果 _excepts_ 中的异常一个没有被设置，则返回 0。

调用这个函数的程序需要确保在本次函数调用时，编译指示 [FENV_ACCESS](FENV_ACCESS.md) 已经开启。


## 参数

`excepts`

位掩码值：支持的任何浮点异常数字的组合（按位 OR）：

| 宏值                              | 描述                                                       |
| --------------------------------- | ---------------------------------------------------------- |
| [FE_DIVBYZERO](FE_DIVBYZERO.md)   | 极错误：被 0 除，或一些其他渐进无限的结果（从有限的参数）。|
| [FE_INEXACT](FE_INEXACT.md)       | 不精确：结果不准确。                                       |
| [FE_INVALID](FE_INVALID.md)       | 作用域错误：至少一个参数是函数没有定义的值。               |
| [FE_OVERFLOW](FE_OVERFLOW.md)     | 上溢错误：结果太大了，超出了返回值类型能表示的数量级。     |
| [FE_UNDERFLOW](FE_UNDERFLOW.md)   | 下一错误：结果太小了，超出了返回值类型能表示的数量级。     |
| [FE_ALL_EXCEPT](FE_ALL_EXCEPT.md) | 所有异常（选择实现支持的所有异常）                         |

特定的库实现可能会支持附加的 _浮点异常_ 值（它们对应的宏同样以 FE_ 开头的宏）。

#### C99

库可能定义在 [&lt;fenv.h&gt;](README.md)，仅仅支持上面这些宏值（其他可能没有被定义）。

#### C++11

至少上面所有的宏值都定义在 [&lt;fenv.h&gt;](README.md) 中（即使实现不支持）。


## 返回值

如果 _excepts_ 中的异常没有一个被设置的话，则返回 0，否则返回当前设置的异常（在 _excepts_ 中的）。


## 例子

```cpp
/* fetestexcept example */
#include <stdio.h>	/* puts */
#include <fenv.h>	/* feraiseexcept, fetestexcept, FE_* */
#pragma STDC FENV_ACCESS on

double fn(double x)
{
	/* some function for which zero is a domain and range error */
	if(x == 0.0)
		feraiseexcept(FE_INVALID | FE_OVERFLOW);
	return x;
}

int main()
{
	int fe;

	feclearexcept(FE_ALL_EXCEPT);
	fn(0.0);

	/* testing for single exception: */
	if(fetestexcept(FE_OVERFLOW))
		puts("FE_OVERFLOW is set");

	/* testing multiple exceptions: */
	fe = fetestexcept(FE_ALL_EXCEPT);

	puts("The following exceptions are set:");
	if(fe & FE_DIVBYZERO)
		puts("FE_DIVBYZERO");
	if(fe & FE_INEXACT)
		puts("FE_INEXACT");
	if(fe &FE_INVALID)
		puts("FE_INVALID");
	if(fe & FE_OVERFLOW)
		puts("FE_OVERFLOW");
	if(fe & FE_UNDERFLOW)
		puts("FE_UNDERFLOW");

	return 0;
}
```

可能的输出：  
```
FE_OVERFLOW is set
The following exceptions are set:
FE_INVALID
FE_OVERFLOW
```

## 数据竞争

每个线程都保持着分离的、拥有自己状态的 _浮点环境_ 。产生一个新线程就复制当前状态。[ 这个适用于 C11 和 C++11 的实现 ]


## 异常

不抛出异常的保证：这个函数从不抛出异常。  
注意 C _浮点环境异常_ 不是 C++ 异常，因此不能被 _try/catch_ 块捕捉。  
调用这个函数的时候，如果编译指示 [FENV_ACCESS](FENV_ACCESS.md) 关闭的话，则会导致未定义行为。


## 另请参见

| 函数                              | 描述                  |
| --------------------------------- | --------------------- |
| [feraiseexcept](feraiseexcept.md) | 触发浮点异常 (_函数_) |
| [feclearexcept](feclearexcept.md) | 清楚浮点异常 (_函数_) |
| [feholdexcept](feholdexcept.md)   | 保留浮点异常 (_函数_) |
