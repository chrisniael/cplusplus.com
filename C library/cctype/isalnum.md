函数

# isalnum

\<cctype\>

`int isalnum ( int c );`

#### 检查字符是否是字母数字(alphanumeric)

检查字符 _c_ 是否是一个十进制数字或者是大写或小写字母。

函数返回值是 _true_，那么 [isalpha](isalpha.md) 和 [isdigit](isdigit.md) 也返回 _true_。

注意，判别一个字符是否是字母取决于使用环境。在默认的 "C" 环境中，只有当 [isupper](isupper.md) 和 [islower](islower.md) 返回 _true_ 的时候才是字母。

头文件 (\<cctype\>)[README.md] 的参考中，有标准 ASCII 字符集的各个字符在不同 _ctype_ 函数的返回值的详细图表。

在 C++ 中，这个函数的 locale-specific 模板版本 (isalnum)[../../Other/locale/isalnum.md] 在头文件 (\<locale\>)[../../Other/locale/README.md]中。


## 参数

`c`

被检查的字符，被转化为_int_ 型或 _EOF_。


## 返回值
如果 _c_ 的确是一个数字或字母，则返回一个非0值 (也就是 _true_ )，否则返回0 (也就是 _false)。

## 例子

```cpp
/* isalnum example */
#include <stdio.h>
#include <ctype.h>

int main()
{
	int i;
	char str[] = "c3po...";
	i = 0;
	while(isalnum(str[i])) i++;
	printf("The first %d characters are alphanumeric.\n", i);
	return 0;
}
```

输出：  
```
The first 4 characters are alphanumeric.
```


## 另请参阅

函数名                | 描述
--------------------- | ---------------
[isalpha](isalpha.md) | 检查字符是否是字母(alphabetic) (_函数_)
[isdigit](isdigit.md) | 检查字符是否是十进制数字(dicimal digit) (_函数_)
