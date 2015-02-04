函数

# isupper

\<cctype\>

`int isupper ( int c );`

#### 检查字符是否是大写字母 (uppercase letter)

检查 _c_ 是否是一个大写字母。


注意，判别一个字符是否是大写字母取决于使用环境。在默认的 "C" 环境中，大写字母有：_A_ _B_ _C_ _D_ _E_ _F_ _G_ _H_ _I_ _J_ _K_ _L_ _M_ _N_ _O_ _P_ _Q_ _R_ _S_ _T_ _U_ _V_ _W_ _X_ _Y_ _Z_。

头文件 [\<cctype\>](README.md) 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [isupper](../../Other/locale/isupper.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个大写字母，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* isupper example */
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
		if(isupper(c))
			c = tolower(c);
		putchar(c);
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
--------------------- | ---------------
[islower](islower.md) | 检查字符是否是小写字母(islower) (_函数_)
[isalpha](isalpha.md) | 检查字符是否是字母(alphabetic) (_函数_)
[toupper](toupper.md) | 将小写字母转化为大写 (_函数_)
[tolower](tolower.md) | 将大写字母转化为小写 (_函数_)
