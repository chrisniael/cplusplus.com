函数

# isalpha

\<cctype\>

`int isalpha ( int c );`

#### 检查字符是否是字母(alphabetic)

检查 _c_ 是否是一个字母。

注意，判别一个字符是否是字母取决于使用环境。在默认的 "C" 环境中，只有当 [isupper](isupper.md) 和 [islower](islower.md) 返回 _true_ 的时候才是字母。


使用其他的环境，只有当 [isupper](isupper.md) 或 [islower](islower.md) 返回 _true_ 时才是字母，其他还有一些被环境特定认为是字母的一些字符（在中情况下，这个字母字符不可能在函数 [iscntrl](iscntrl.md)，[isdigit](isdigit.md)，[ispunct](ispunct.md) 或 [isspace](isspace.md) 中返回 _true_ 。


头文件 (\<cctype\>)[README.md] 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 [isalpha](../../Other/locale/isalpha.md) 在头文件 [\<locale\>](../../Other/locale/README.md)中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个字母，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false_)。

## 例子

```cpp
/* isalpha example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	int i = 0;
	char str[] = "C++";
	while(str[i])
	{
		if(isalpha(str[i]))
			printf("character %c is alphabetic\n", str[i]);
		else
			printf("character %c is not alphabetic\n", str[i]);
		i++;
	}
	return 0;
}
```

输出：  
```
character C is alphabetic
character + is not alphabetic
character + is not alphabetic
```


## 另请参阅

函数名                | 描述
--------------------- | ------------------------------------------------
[isalnum](isalnum.md) | 检查字符是否是字母或数字(alphanumeric) (_函数_)
[isdigit](isdigit.md) | 检查字符是否是十进制数字(dicimal digit) (_函数_)
