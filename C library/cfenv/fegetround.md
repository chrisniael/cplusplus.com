函数

# fegetround (C++11)

`int fegetround(void);`

#### 获取舍入方向模式

返回当前 _浮点环境_ 中表明舍入方向模式的值。

这个函数的返回值不一定和 [cfloat](../cfloat/README.md) 中 _FLT_ROUNDS_ 的值相同。

## 参数

无


## 返回值

如果这个函数能决定当前舍入模式，并且被当前实现支持，那么函数返回值对应的宏定义如下：

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


## 例子

```cpp
/* fegetround / rint example */
#include <stdio.h>	/* printf */
#include <fenv.h>	/* fegetround FE_* */
#include <math.h>	/* rint */

int main()
{
	printf("Rounding using ");
	switch(fegetround())
	{
		case FE_DOWNWARD:
			printf("downward");
			break;
		case FE_TONEAREST:
			printf("to-nearset");
			break;
		case FE_TOWARDZERO:
			printf("toward-zero");
			break;
		case FE_UPWARD:
			printf("upward");
			break;
		default:
			printf("unknown");
	}
	printf(" rounding:\n");

	printf("rint (2.3) = %.1f\n", rint(2.3));
	printf("rint (3.8) = %.1f\n", rint(3.8));
	printf("rint (-2.3) = %.1f\n", rint(-2.3));
	printf("rint (-3.8) = %.1f\n", rint(-3.8));

	return 0;
}
```

可能的输出：  
```
Rounding using to-nearset rounding:
rint (2.3) = 2.0
rint (3.8) = 4.0
rint (-2.3) = -2.0
rint (-3.8) = -4.0
```

## 数据竞争

每个线程都保持着分离的、拥有自己状态的 _浮点环境_ 。产生一个新线程就复制当前状态。[ 这个适用于 C11 和 C++11 的实现 ]


## 异常

不抛出异常的保证：这个函数从不抛出异常。  


## 另请参见

函数                        | 描述
--------------------------- | -------------------------
[fesetround](fesetround.md) | 设置舍入方向模式 (_函数_)
[fegetenv](fegetenv.md)     | 获取浮点环境 (_函数_)
[rint](../cmath/rint.md)    | 舍入至整数值 (_函数_)
