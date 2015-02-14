函数

# fesetround (C++11)

`int fesetround(int rdir);`

#### 设置舍入方向模式

设置 _rdir_ 为 当前 _浮点环境_ 的 _舍入方向_。

这个函数的返回值不一定和 [cfloat](../cfloat/README.md) 中 _FLT_ROUNDS_ 的值相同。


## 参数

`rdir`

以下定义为 _舍入方向模式_ 的值之一：

宏值                               | 描述
---------------------------------- | -------------------
[FE\_DOWNWARD](FE_DOWNWARD.md)     | 向下舍入模式 (_宏_)
[FE\_TONEAREST](FE_TONEAREST.md)   | 四舍五入模式 (_宏_)
[FE\_TOWARDZERO](FE_TOWARDZERO.md) | 朝零舍入模式 (_宏_)
[FE\_UPWARD](FE_UPWARD.md)         | 向上舍入模式 (_宏_)

特定的库实现可能会支持附加的 _浮点舍入方向_ 值（它们对应的宏同样以 FE_ 开头的宏）。

#### C99

库可能定义在 [\<fenv.h\>](README.md)，仅仅支持上面这些宏值（其他可能没有被定义）。

#### C++11

至少上面所有的宏值都定义在 [\<fenv.h\>](README.md) 中（即使实现不支持）。


## 返回值

如果请求的浮点方向被成功设置的话，则返回 0 ，否则返回非 0 。


## 例子

```cpp
/* fesetround example */
#include <stdio.h>	/* printf */
#include <fenv.h>	/* fesetround, FE_* */
#include <math.h>	/* rint */
#pragma STDC FENV_ACCESS on

int main()
{
	printf("rounding -3.8:\n");

	fesetround(FE_DOWNWARD);
	printf("FE_DOWNWARD: %.1f\n", rint(-3.8));

	fesetround(FE_TONEAREST);
	printf("FE_TONEAREST: %.1f\n", rint(-3.8));

	fesetround("FE_TOWARDZERO: %.1f\n", rint(-3.8));
	printf("FE_TOWARDZERO: %.1f\n", rint(-3.8));

	fesetround(FE_UPWARD);
	printf("FE_UPWARD: %.1f\n", rint(-3.8));

	return 0;
}
```

可能的输出：  
```
rounding -3.8:
FE_DOWNWARD: -4.0
FE_TONEAREST: -4.0
FE_TOWARDZERO: -3.0
FE_UPWARD: -3.0
```


## 数据竞争

同时调用这个函数是安全的，不导致数据竞争。


## 异常

不抛出异常的保证：这个函数从不抛出异常。  


## 另请参见

函数                        | 描述
--------------------------- | -------------------------
[fegetround](fegetround.md) | 获取浮点方向模式 (_函数_)
[fesetenv](fesetenv.md)     | 设置浮点环境 (_函数_)
[rint](../cmath/rint.md)    | 舍入至整数值 (_函数_)
