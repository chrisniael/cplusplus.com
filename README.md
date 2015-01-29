# 参考手册

标准 C++ 库参考手册

## C 库

这些 C 语言库的头文件是 C++ 标准库的子集，涵盖了很多方面，包括通用工具库、输入/输出函数的宏和动态内存管理的函数。

头文件                                                      | 描述
----------------------------------------------------------- | ----------------------
[\<cassert\> (assert.h)](C library/cassert/README.md)       | C 诊断库
[\<cctype\> (ctype.h)](C library/cctype/README.md)          | 字符处理函数
[\<cerrno\> (errno.h)](C library/cerrno/README.md)          | C 错误
[\<cfenv\> (fenv.h)](C library/cfenv/README.md)             | 浮点环境
[\<cfloat\> (float.h)](C library/cfloat/README.md)          | 浮点类型特性
[\<cinttypes\> (inttypes.h)](C library/cinttypes/README.md) | C 整数类型
[\<ciso646\> (iso646.h)](C library/ciso646/README.md)       | ISO 646 可选操作符拼写
[\<climits\> (limits.h)](C library/climits/README.md)       | 整数类型的大小
[\<clocale\> (locale.h)](C library/clocale/README.md)       | C 本地化库
[\<cmath\> (math.h)](C library/cmath/README.md)             | C 数学库
[\<csetjmp\> (setjmp.h)](C library/csetjmp/README.md)       | 非局部跳转
[\<csignal\> (signal.h)](C library/csignal/README.md)       | 处理信号的 C 库
[\<cstdarg\> (stdarg.h)](C library/cstdarg/README.md)       | 可变数量参数处理
[\<cstdbool\> (stdbol.h)](C library/cstdbool/README.md)     | 布尔类型
[\<cstddef\> (stddef.h)](C library/cstddef/README.md)       | C 标准定义
[\<cstdint\> (stdint.h)](C library/cstdint/README.md)       | 整数类型
[\<cstdio\> (stdio.h)](C library/cstdio/README.md)          | 操作输入/输出的 C 库
[\<cstdlib\> (stdlib.h)](C library/cstdlib/README.md)       | C 标准通用工具库
[\<cstring\> (string.h)](C library/cstring/README.md)       | C 字符串
[\<ctgmath\> (tgmath.h)](C library/ctgmath/README.md)       | 类型泛化的数学
[\<ctime\> (time.h)](C library/ctime/README.md)             | C 时间库
[\<cuchar\> (uchar.h)](C library/cuchar/README.md)          | Unicode 字符
[\<cwchar\> (wchar.h)](C library/cwchar/README.md)          | 宽字符
[\<cwctype\> (wctype.h)](C library/cwctype/README.md)       | 宽字符类型


## 容器

头文件                                                   | 描述
-------------------------------------------------------- | ---------------------
[\<array\>](Containers/array/README.md)                  | Array 头文件
[\<bitset\>](Containers/bitset/README.md)                | Bitset 头文件
[\<deque\>](Containers/deque/README.md)                  | Deque 头文件
[\<forward\_list\>](Containers/forward_list/README.md)   | Forward list 头文件
[\<list\>](Containers/list/README.md)                    | List 头文件
[\<map\>](Containers/map/README.md)                      | Map 头文件
[\<queue\>](Containers/queue/README.md)                  | Queue 头文件
[\<set\>](Containers/set/README.md)                      | Set 头文件
[\<stack\>](Containers/stack/README.md)                  | Stack 头文件
[\<unordered\_map\>](Containers/unordered_map/README.md) | Unordered map 头文件
[\<unordered\_set\>](Containers/unordered_set/README.md) | Unordered set 头文件
[\<vector\>](Containers/vector/README.md)                | Vector 头文件


## 输入/输出流库

使用_流_这种抽象概念，来执行像文件和字符串这样的序列字符的输入输出操作。

在下面的关系图上，展示了这个功能涉及的多个相关联的类以及对应的头文件名字。

![images](images/iostream.gif)


## 原子和线程库




## 其他头文件
