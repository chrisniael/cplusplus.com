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

如果函数成功执行的话，包括设置 _浮点环境_ 为 _non-stop_ 模式，则返回 0， 否则返回非 0。


## 例子

```cpp
/* feholdexcept / feupdateenv example */
#include <stdio.h>	/* printf, puts */
#include <fenv.h>	/* feholdexcept, feclearexcept, fetestexcept, feupdateenv, FE_* */
#include <math.h>	/* log */
#pragma STDC FENV_ACCESS on

double log_zerook(double x)
{
	fenv_t fe;
	feholdexcept(&fe);
	x = log(x);
	feclearexcept(FE_OVERFLOW | FE_DIVBYZERO);
	feupdateenv(&fe);
	return x;
}

int main()
{
	feclearexcept(FE_ALL_EXCEPT);
	printf("log(0.0): %f\n", log_zerook(0.0));
	if(!fetestexcept(FE_ALL_EXCEPT));
		puts("no exceptions raised");
	
	return 0;
}
```

可能的输出：  
```
log(0.0): -inf
no exceptions raised
```


## 数据竞争

每个线程都保持着分离的、拥有自己状态的 _浮点环境_ 。产生一个新线程就复制当前状态。[ 这个适用于 C11 和 C++11 的实现 ]


## 异常

不抛出异常的保证：这个函数从不抛出异常。  
注意 C _浮点环境异常_ 不是 C++ 异常，因此不能被 _try/catch_ 块捕捉。


## 另请参见

函数                              | 描述
--------------------------------- | ---------------------
[fegetenv](fegetenv.md)           | 获取浮点环境 (_函数_)
[fesetenv](fesetenv.md)           | 设置浮点环境 (_函数_)
[feclearexcept](feclearexcept.md) | 清除浮点异常 (_函数_)
