函数

# isblank (_C++11_)

\<cctype\>

`int isblank ( int c );`

#### 检查字符是否是空白符(blank)

检查 _c_ 是否是一个空白字符(blank character)。

标准 "C" 环境把水平制表符 ('\t') 和空格符 (' ') 认为是空白字符。

其他环境认定的空白符可能会不一样，但是它们必须是在函数 [isspace](isspace.md) 中返回 _true_ 的空格字符。

头文件 [\<cctype\>](README.md) 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [isblank](../../Other/locale/isblank.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为 _int_ 型或 _EOF_。


## 返回值

如果 _c_ 的确是一个空白字符，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 false)。

## 例子

```cpp
/* isblank example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	char c;
	int i = 0;
	char str[] = "Example sentence to test is blank\n";
	while(str[i])
	{
		c = str[i];
		if(isblank(c))
			c = '\n';
		putchar(c);
		i++;
	}
	return 0;
}
```
这段代码把 C 字符串中所有的空白字符替换为换行字符，并追个字符的输出。

输出：  
```
Example
sentence
to
test
isblank
```


## 另请参阅

函数名                | 描述
--------------------- | ----------------------------------------------------------------------------
[isspace](isspace.md) | 检查字符是否是空格符(white-space) (_函数_)
[isgraph](isgraph.md) | 检查字符是否可打印(graphical representation) (_函数_)
[ispunct](ispunct.md) | 检查字符是否是标点字符(punctuation) (_函数_)
[isalnum](isalnum.md) | 检查字符是否是字母或数字(alphanumeric) (_函数_)
[isblank (locale)](../../Other/locale/isblank.md) | 使用环境检查字符是否是空白符(blank) (_函数模板_)
