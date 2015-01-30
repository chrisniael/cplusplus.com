库

# C 库

C 语言库

C++ 库被组织在 C 语言库相同结构的头文件中，并包括了相同的定义，但有以下的不同之处 :

- 每个头文件的名字和 C 语言版本一样，但是多了 "_c_" 前缀。例如，C++ 头文件 _\<cstdlib\>_ 等价于 C 语言头文件 _\<stdlib.h\>_。
- 库中所有元素都被定义在了 _std_ 命名空间中了。

## 版本注释

虽然这样，但为了兼容 C，传统头文件 _name.h_ (比如 _stdlib.h_ ) 在全局作用域中同样提供了定义。这个手册中所有的例子就是使用这个版本，所以这些例子是完全与 C 兼容的，即使它在 C++ 中被废弃了。

在 C++ 的实现中当然也有某些特定的改变：

- _wchar\_t_，_char16\_t_，_char32\_t_ 和 _bool_ 是 C++ 中的基本类型，因此，它们没有被定义在 C 语言中应该出现的头文件中。[\<iso646.h\>](ciso646/README.md) 中的宏也一样，成了 C++ 中的关键字。


## 头文件 (C++98)

头文件                                                      | 描述
----------------------------------------------------------- | ---------------------------------
[\<cassert\> (assert.h)](cassert/README.md)                 | C 诊断库
[\<cctype\> (ctype.h)](cctype/README.md)          | 字符处理函数 (_头文件_)
[\<cerrno\> (errno.h)](cerrno/README.md)          | C 错误 (_头文件_)
[\<cfenv\> (fenv.h)](cfenv/README.md)             | 浮点环境 (_头文件_)
[\<cfloat\> (float.h)](cfloat/README.md)          | 浮点类型特性 (_头文件_)
[\<cinttypes\> (inttypes.h)](cinttypes/README.md) | C 整数类型 (_头文件_)
[\<ciso646\> (iso646.h)](ciso646/README.md)       | ISO 646 可选操作符拼写 (_头文件_)
[\<climits\> (limits.h)](climits/README.md)       | 整数类型的大小 (_头文件_)
[\<clocale\> (locale.h)](clocale/README.md)       | C 本地化库 (_头文件_)
[\<cmath\> (math.h)](cmath/README.md)             | C 数学库 (_头文件_)
[\<csetjmp\> (setjmp.h)](csetjmp/README.md)       | 非局部跳转 (_头文件_)
[\<csignal\> (signal.h)](csignal/README.md)       | 处理信号的 C 库 (_头文件_)
[\<cstdarg\> (stdarg.h)](cstdarg/README.md)       | 可变数量参数处理 (_头文件_)
[\<cstddef\> (stddef.h)](cstddef/README.md)       | C 标准定义 (_头文件_)
[\<cstdio\> (stdio.h)](cstdio/README.md)          | 操作输入/输出的 C 库 (_头文件_)
[\<cstdlib\> (stdlib.h)](cstdlib/README.md)       | C 标准通用工具库 (_头文件_)
[\<cstring\> (string.h)](cstring/README.md)       | C 字符串 (_头文件_)
[\<ctime\> (time.h)](ctime/README.md)             | C 时间库 (_头文件_)

ISO-C 90 修正案 1 添加了两个额外的头文件：[\<cwchar\>](cwchar/README.md) 和 [\<cwctype\>](cwctype/README.md)。


## 头文件 (C++11)
头文件                                                      | 描述
----------------------------------------------------------- | -------------------------
[\<cstdbool\> (stdbol.h)](cstdbool/README.md)     | 布尔类型 (_头文件_)
[\<cstdint\> (stdint.h)](cstdint/README.md)       | 整数类型 (_头文件_)
[\<ctgmath\> (tgmath.h)](ctgmath/README.md)       | 类型泛化的数学 (_头文件_)
[\<cuchar\> (uchar.h)](cuchar/README.md)          | Unicode 字符 (_头文件_)
[\<cwchar\> (wchar.h)](cwchar/README.md)          | 宽字符 (_头文件_)
[\<cwctype\> (wctype.h)](cwctype/README.md)       | 宽字符类型 (_头文件_)
