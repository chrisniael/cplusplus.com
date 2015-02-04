函数

# isxdigit

\<cctype\>

`int isxdigit ( int c );`

#### 检查字符是否是十六进制数字(decimal digit)

检查 _c_ 是否是一个十六进制数字字符。

十进制数字有：_0_ _1_ _2_ _3_ _4_ _5_ _6_ _7_ _8_ _9_ _a_ _b_ _c_ _d_ _e_ _f_ _A_ _B_ _C_ _D_ _E_ _F_

头文件 [\<cctype\>](README.md) 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [isxdigit](../../Other/locale/isxdigit.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个十六进制数字，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。


## 例子

```cpp
/* isxdigit example */
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

int main()
{
	char str[] = "ffff";
	long int number;
	if(isxdigit(str[0]))
	{
		number = strtol(str, NULL, 16);
		printf("The hexadecimal number %lx is %ld.\n", number, number);
	}
	return 0;
}
```

输出：  
```
The hexadecimal number ffff is 65535.
```

[isxdigit](isxdigit.md) 被用来检查 _str_ 的第一个字符是否是一个十六进制数字，来成为一个有效的候选者被 [strtol](../cstdlib/strtol.md) 转化为一个整型的值。


## 另请参阅

函数名                | 描述
--------------------- | ------------------------------------------------
[isdigit](isdigit.md) | 检查字符是否是十进制数字(decimal digit) (_函数_)
[isalnum](isalnum.md) | 检查字符是否是字母或数字(alphanumeric) (_函数_)
[isalpha](isalpha.md) | 检查字符是否是字母(alphabetic) (_函数_)
