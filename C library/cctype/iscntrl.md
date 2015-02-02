函数

# iscntrl

\<cctype\>

`int iscntrl ( int c );`

#### 检查字符是否是控制字符(control character)

在显示中，控制字符并不占据打印位置（这和在函数 [isprint](isprint.md) 中返回 _true_ 的可打印字符相反）。

对于标准 ASCII 字符集（在 "C" 环境中），控制字符是 ASCII 值在 0x00 (NUL) 到 0x1f (US) 之间的，加上 0x7f (DEL) 的字符。

头文件 (\<cctype\>)[README.md] 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [iscntrl](../../Other/locale/iscntrl.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个控制字符，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* iscntrl example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	int i;
	char str[] = "first line \n second line \n";
	while(!iscntrl(str[i]))
	{
		putchar(str[i]);
		i++;
	}
	return 0;
}
```

这段代码追个字符输出一个字符串，直到遇到一个控制字符才跳出 while 循环。在这个例子中，只有第一行被输出，因为第一行以控制字符 '\n' (ASCII 值是 0x0a) 结尾。


## 另请参阅

函数名                | 描述
--------------------- | ---------------
[isgraph](isgraph.md) | 检查字符是否有图形表示(graphical representation) (_函数_)
[ispunct](ispunct.md) | 检查字符是否是标点符号(punctuation) (_函数_)
