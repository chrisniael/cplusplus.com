函数

# isspace

\<cctype\>

`int isspace ( int c );`

#### 检查字符是否是一个空格

检查 _c_ 是否是一个空格字符。

标准 "C" 环境中，空白字符有：

字符 | ASCII值 | 描述
---- | ------- | ----
' '  | (0x20)  | 空格(SPC)
'\t' | (0x09)  | 水平制表符(TAB)
'\n' | (0x0a)  | 换行符(LF)
'\v' | (0x0b)  | 垂直制表符(VT)
'\f' | (0x0c)  | 换页(FF)
'\r' | (0x0d)  | 回车(CR)

在其他的环境中，可能会有不同的字符被认为是空格，但是它们不可能让函数 [isalnum](isalnum.md) 返回 _true_。

头文件 (\<cctype\>)[README.md] 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [isspace](../../Other/locale/isspace.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个空格字符，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* isspace example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	char c;
	int i = 0;
	char str[] = "Example sentence to test isspace\n";
	while(str[i])
	{
		c=str[i];
		if(isspace(c))
			c = '\n';
		putchar(c);
		i++;
	}
}
```

这段代码替换了 C 字符串中的空白字符为换行符，并追个字符的将其输出。

输出：  
```
Example
sentence
to
test
isspace
```


## 另请参阅

函数名                | 描述
--------------------- | ---------------
[isgraph](isgraph.md) | 检查字符是否有图形表示(graphical representation) (_函数_)
[ispunct](ispunct.md) | 检查字符是否是标点字符(punctuation) (_函数_)
[isalnum](isalnum.md) | 检查字符是否是字母或数字(alphanumeric) (_函数_)
[isspace](isspace.md) | 检查字符是否是空格符(white-space) (_函数_)
