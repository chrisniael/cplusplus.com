函数

# isgraph

\<cctype\>

`int isgraph ( int c );`

#### 检查字符是否有图形表示(graphical representation)

检查 _c_ 是否是一个图形表示的字符

图形表示的字符是那些能被打印的字符 ([isprint](isprint.md) 决定)，除了空格字符 (' ')。
 
头文件 [\<cctype\>](README.md) 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [isgraph](../../Other/locale/isgraph.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为 _int_ 型或 _EOF_。


## 返回值

如果 _c_ 的确是一个有图形表示的字符，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* isgraph example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	FILE * pFile;
	int c;
	pFile = fopen("myfile.txt", "r")
	if(pFile)
	{
		do
		{
			c = fgetc(pFile);
			if(isgraph(c))
				putchar(c);
		}while(c != EOF);
		fclose(pFile);
	}
}
```
这个例子输出文件 "myfile.txt" 中除了空格字符和特殊字符外的内容，也就是说，只输出满足函数 [isgraph](isgraph.md) 的字符。


## 另请参阅

函数名                | 描述
--------------------- | -----------------------------------------------
[isprint](isprint.md) | 检查字符是否可打印 (_函数_)
[isspace](isspace.md) | 检查字符是否是空格符(white-space) (_函数_)
[isalnum](isalnum.md) | 检查字符是否是字母或数字(alphanumeric) (_函数_)
