函数

# islower

\<cctype\>

`int islower ( int c );`

#### 检查字符是否是小写字母 (lowercase letter)

检查字符 _c_ 是否是一个小写字母。


注意，判别一个字符是否是小写字母取决于使用环境。在默认的 "C" 环境中，小写字母有：_a_ _b_ _c_ _d_ _e_ _f_ _g_ _h_ _i_ _j_ _k_ _l_ _m_ _n_ _o_ _p_ _q_ _r_ _s_ _t_ _u_ _v_ _w_ _x_ _y_ _z_。

头文件 (\<cctype\>)[README.md] 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [islower](../../Other/locale/islower.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个小写字母，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* islower example */
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
		if(islower(c))
			c = toupper(c);
		putchar(c);
		i++;
	}
}
```

输出：  
```
TEST STRING
```


## 另请参阅

函数名                | 描述
--------------------- | ---------------
[isupper](isupper.md) | 检查字符是否是大写字母(isupper) (_函数_)
[isalpha](isalpha.md) | 检查字符是否是字母(alphabetic) (_函数_)
[toupper](toupper.md) | 将小写字母转化为大写 (_函数_)
[tolower](tolower.md) | 将大写字母转化为小写 (_函数_)
