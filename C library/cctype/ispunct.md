函数

# ispunct

\<cctype\>

`int ispunct ( int c );`

#### 检查字符是否是标点字符(punctuation)

检查 _c_ 是否是一个标点字符。

标准 "C" 环境把所有是图形字符 (as in [isgraph](isgraph.md)) 但不是字母或数字 (as in [isalnum](isalnum.md)) 的字符认为是标点字符。

其他环境可能会把不同的字符当作标点字符，但无论哪种情况，它们肯定是 [isgraph](isgraph.md) 但不是 [isalnum](isalnum.md)。

头文件 [\<cctype\>](README.md) 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [ispunct](../../Other/locale/ispunct.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为 _int_ 型或 _EOF_。


## 返回值

如果 _c_ 的确是一个数字或字母，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* ispunct example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	int i = 0;
	int cx = 0;
	char str[] = "Hello, welcome!";
	while(str[i])
	{
		if(ispunct(str[i]))
			cx++;
		i++;
	}
	printf("Sentence contains %d punctuation characters.\n", cx);
}
```

输出：  
```
Sentence contains 2 punctuation characters.
```


## 另请参阅

函数名                | 描述
--------------------- | ---------------
[isgraph](isgraph.md) | 检查字符是否有图形表示(graphical representation) (_函数_)
[iscntrl](iscntrl.md) | 检查字符是否是控制字符(control character) (_函数_)
