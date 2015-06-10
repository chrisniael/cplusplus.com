函数

# tolower

&lt;cctype&gt;

`int tolower ( int c );`

#### 将大写字母转化为小写

如果 _c_ 是一个大写字母并且存在对应的小写字母的话，则将 _c_ 转化为对应的小写字母，否则返回 _c_ 的原始值。

注意，判别一个字母是什么取决于使用环境。在默认的 "C" 环境中，大写字母有：_A_ _B_ _C_ _D_ _E_ _F_ _G_ _H_ _I_ _J_ _K_ _L_ _M_ _N_ _O_ _P_ _Q_ _R_ _S_ _T_ _U_ _V_ _W_ _X_ _Y_ _Z_，对应转化成的小写字母分别是：_a_ _b_ _c_ _d_ _e_ _f_ _g_ _h_ _i_ _j_ _k_ _l_ _m_ _n_ _o_ _p_ _q_ _r_ _s_ _t_ _u_ _v_ _w_ _x_ _y_ _z_。

在其他环境中，如果一个大写字母有多个对应的小写字母，那么对于同一个值 _c_，这个函数总是返回同样的字符。

在 C++ 中，这个函数的 locale-specific 模板版本 [tolower](../../Other/locale/tolower.md) 在头文件 [&lt;locale&gt;](../../Other/locale/README.md)中。


## 参数

`c`

被转化的字符，被转化为 _int_ 型或 _EOF_。


## 返回值

返回 _c_ 对应的小写字符，如果存在的话，否则返回 _C_ 本身（未改变）。返回值是能被隐式转化为 _char_ 的一个 _int_ 型值。

## 例子

```cpp
/* tolower example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	int i = 0;
	char str[] = "Test String.\n";
	char c;
	while(str[i])
	{
		c = str[i];
		putchar(tolower(c));
		i++;
	}
	return 0;
}
```

输出：  
```
test string.
```


## 另请参阅

函数名                | 描述
--------------------- | -------------------------------------------------
[toupper](toupper.md) | 将小写字母转化为大写 (_函数_)
[isupper](isupper.md) | 检查字符是否是大写字母(uppercase letter) (_函数_)
[islower](islower.md) | 检查字符是否是小写字母(lowercase letter) (_函数_)
[isalpha](isalpha.md) | 检查字符是否是字母(alphabetic) (_函数_)
