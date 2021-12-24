库

# C 库

C 语言库

C++ 库被组织在 C 语言库相同结构的头文件中，并包括了相同的定义，但有以下的不同之处 :

- 每个头文件的名字和 C 语言版本一样，但是多了 "_c_" 前缀。例如，C++ 头文件 _&lt;cstdlib&gt;_ 等价于 C 语言头文件 _&lt;stdlib.h&gt;_。
- 库中所有元素都被定义在了 _std_ 命名空间中了。

虽然这样，但为了兼容 C，传统头文件 _name.h_ (比如 _stdlib.h_ ) 在全局作用域中同样提供了定义。这个手册中所有的例子就是使用这个版本，所以这些例子是完全与 C 兼容的，即使它在 C++ 中被废弃了。

在 C++ 的实现中当然也有某些特定的改变：

- _wchar\_t_，_char16\_t_，_char32\_t_ 和 _bool_ 是 C++ 中的基本类型，因此，它们没有被定义在 C 语言中应该出现的头文件中。[&lt;iso646.h&gt;](ciso646/README.md) 中的宏也一样，成了 C++ 中的关键字。
- 下面这些函数的参数常量性定义有所改变：_strchr_，_strpbrk_，_strrchr_，_strstr_，_memchr_。
- 头文件 &lt;cstdlib&gt; 中的函数 _atexit_，_exit_ 和 _abort_，在 C++ 中增加了行为。
- 提供了一些重载版本的函数，使用额外的类型作为参数，但有相同的语义，例如，在头文件 &lt;cmath&gt; 中的的 _flot_ 和 _long_ _double_ 版本的函数，_long_ 版本的 _abs_ 和 _div_。


## 注解版本

C++ 98 包括了 1990 ISO C 标准和它的修正案 #1 (ISO/IEC 9899:1990 和 ISO/IEC 9899:1990/DAM 1) 描述的 C 库。

C++ 11 包括了 1990 ISO C 标准和它的 Technical Corrigenda 1，2，3 (ISO/IEC 9899:1999 和 ISO/IEC 9899:1999/Cor.1,2,3) 描述的 C 库，加上 [&lt;cuchar&gt;](cuchar/README.md) (ISO/IEC 19769:2004)。


## 头文件 C90 (C++98)

头文件                                            | 描述
------------------------------------------------- | ---------------------------------
[&lt;cassert&gt; (assert.h)](cassert/README.md)       | C 诊断库
[&lt;cctype&gt; (ctype.h)](cctype/README.md)          | 字符处理函数 (_头文件_)
[&lt;cerrno&gt; (errno.h)](cerrno/README.md)          | C 错误 (_头文件_)
[&lt;cfenv&gt; (fenv.h)](cfenv/README.md)             | 浮点环境 (_头文件_)
[&lt;cfloat&gt; (float.h)](cfloat/README.md)          | 浮点类型特性 (_头文件_)
[&lt;cinttypes&gt; (inttypes.h)](cinttypes/README.md) | C 整数类型 (_头文件_)
[&lt;ciso646&gt; (iso646.h)](ciso646/README.md)       | ISO 646 可选操作符拼写 (_头文件_)
[&lt;climits&gt; (limits.h)](climits/README.md)       | 整数类型的大小 (_头文件_)
[&lt;clocale&gt; (locale.h)](clocale/README.md)       | C 本地化库 (_头文件_)
[&lt;cmath&gt; (math.h)](cmath/README.md)             | C 数学库 (_头文件_)
[&lt;csetjmp&gt; (setjmp.h)](csetjmp/README.md)       | 非局部跳转 (_头文件_)
[&lt;csignal&gt; (signal.h)](csignal/README.md)       | 处理信号的 C 库 (_头文件_)
[&lt;cstdarg&gt; (stdarg.h)](cstdarg/README.md)       | 可变数量参数处理 (_头文件_)
[&lt;cstddef&gt; (stddef.h)](cstddef/README.md)       | C 标准定义 (_头文件_)
[&lt;cstdio&gt; (stdio.h)](cstdio/README.md)          | 操作输入/输出的 C 库 (_头文件_)
[&lt;cstdlib&gt; (stdlib.h)](cstdlib/README.md)       | C 标准通用工具库 (_头文件_)
[&lt;cstring&gt; (string.h)](cstring/README.md)       | C 字符串 (_头文件_)
[&lt;ctime&gt; (time.h)](ctime/README.md)             | C 时间库 (_头文件_)

ISO-C 90 修正案 1 添加了两个额外的头文件：[&lt;cwchar&gt;](cwchar/README.md) 和 [&lt;cwctype&gt;](cwctype/README.md)。


## 头文件 C99 (C++11)

头文件                                            | 描述
------------------------------------------------- | -------------------------
[&lt;cstdbool&gt; (stdbol.h)](cstdbool/README.md)     | 布尔类型 (_头文件_)
[&lt;cstdint&gt; (stdint.h)](cstdint/README.md)       | 整数类型 (_头文件_)
[&lt;ctgmath&gt; (tgmath.h)](ctgmath/README.md)       | 类型泛化的数学 (_头文件_)
[&lt;cuchar&gt; (uchar.h)](cuchar/README.md)          | Unicode 字符 (_头文件_)
[&lt;cwchar&gt; (wchar.h)](cwchar/README.md)          | 宽字符 (_头文件_)
[&lt;cwctype&gt; (wctype.h)](cwctype/README.md)       | 宽字符类型 (_头文件_)
