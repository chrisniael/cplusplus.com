头文件

# \<cctype\> (ctype.h)

#### 字符处理函数

这个头文件定义了分类和转化字符的函数集


## 函数

这些函数把等价于一个字符的 _int_ 型变量作为参数，并且返回一个 _int_ 型值，这个返回值即可以作为一个字符，又可以代表一个布尔值：一个值为 _0_ 的 _int_ 型变量意味着 _false_，而非 _0_ 的 _int_ 型变量代表 _true_ 。

这里有两个函数集：

#### 字符分类函数

这些函数会检查作为参数传递进来的字符是否属于某一特定类别：

函数名                          | 描述
------------------------------- | ---------------------------------------------------------
[isalnum](isalnum.md)           | 检查字符是否是字母数字的(alphanumberic) (_函数_)
[isalpha](isalpha.md)           | 检查字符是否是字母的(alphabetic) (_函数_)
[isblank (_c++11_)](isblank.md) | 检查字符是否是空白符(blank) (_函数_)
[iscntrl](iscntrl.md)           | 检查字符是否是控制字符(control character) (_函数_)
[isdigit](isdigit.md)           | 检查字符是否是十进制数字(dicimal digit) (_函数_)
[isgraph](isgraph.md)           | 检查字符是否有图形表示(graphical representation) (_函数_)
[islower](islower.md)           | 检查字符是否是小写字母(lowercase letter) (_函数_)
[isprint](isprint.md)           | 检查字符是否可打印(printable) (_函数_)
[ispunct](ispunct.md)           | 检查字符是否是标点符号(punctuation) (_函数_)
[isspace](isspace.md)           | 检查字符是否是空格符(white-space) (_函数_)
[isupper](isupper.md)           | 检查字符是否是大写字母(uppercase letter) (_函数_)
[isxdigit](isxdigit.md)         | 检查字符是否是十六进制数字(hexadecimal) (_函数_)


#### 字符转化函数

这是两个转化字母大小写的函数

函数名                | 描述
--------------------- | --------------------
[tolower](tolower.md) | 将大写字母转化为小写
[toupper](toupper.md) | 将小写字母转化为大写


对于第一个函数集，这里有一张各个函数将原始的127个ASCII字符集作为参数的返回值表 (表格中的 x 表明这个函数将相应字符作为参数时返回 _true_ )

ASCII值       | 字符                               | iscntrl | isblank | isspace | isupper | islower | isalpha | isdigit | isxdigit | isalnum | ispunct | isgraph | isprint
------------- | ---------------------------------- | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :------: | :-----: | :-----: | :-----: | :-----:
0x00 .. 0x008 | NUL,(其他控制码)                   |    x    |         |         |         |         |         |         |          |         |         |         | 
0x09          | tab('\t')                          |    x    |    x    |    x    |         |         |         |         |          |         |         |         | 
0x0A .. 0x0D  | (空格控制码 : '\f','\v','\n','\r') |    x    |         |    x    |         |         |         |         |          |         |         |         | 
0x0E .. 0x1F  | (其他控制码)                       |    x    |         |         |         |         |         |         |          |         |         |         | 
0x20          | 空格(' ')                          |         |    x    |    x    |         |         |         |         |          |         |         |         |    x
0x21 .. 0x2F  | !"#$%&'()\*+,-./                   |         |         |         |         |         |         |         |          |         |    x    |    x    |    x
0x30 .. 0x39  | 0123456789                         |         |         |         |         |         |         |    x    |    x     |    x    |         |    x    |    x
0x3a .. 0x40  | :;\<=\>?@                          |         |         |         |         |         |         |         |          |         |    x    |    x    |    x
0x41 .. 0x46  | ABCDEF                             |         |         |         |    x    |         |    x    |         |    x     |    x    |         |    x    |    x
0x47 .. 0x5A  | GHIJKLMNOPQRSTUVWXYZ               |         |         |         |    x    |         |    x    |         |          |    x    |         |    x    |    x
0x5B .. 0x60  | [\\]^\_`                           |         |         |         |         |         |         |         |          |         |    x    |    x    |    x
0x61 .. 0x66  | abcdef                             |         |         |         |         |    x    |    x    |         |    x     |    x    |         |    x    |    x
0x67 .. 0x7A  | ghijklmnopqrstuvwxyz               |         |         |         |         |    x    |    x    |         |          |    x    |         |    x    |    x
0x7B .. 0x7E  | {\|}                               |         |         |         |         |         |         |         |          |         |    x    |    x    |    x
0x7F          | (DEL)                              |         |         |         |         |         |         |         |          |         |         |         | 

扩展字符集 (大于 0x7F) 可能会因为环境和平台的缘故而属于不同的种类。通常规则是，在大多数支持扩展字符集的平台下，标准 C 环境的 _isgraph_ 和 _isprint_ 函数返回 _true_ 。
