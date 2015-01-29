# 参考手册

标准 C++ 库参考手册

## C 库

这些 C 语言库的头文件是 C++ 标准库的子集，涵盖了很多方面，包括通用工具库、输入/输出函数的宏和动态内存管理的函数。

头文件                                                      | 描述
----------------------------------------------------------- | ----------------------
[\<cassert\> (assert.h)](C library/cassert/README.md)       | C 诊断库 (_头文件_)
[\<cctype\> (ctype.h)](C library/cctype/README.md)          | 字符处理函数 (_头文件_)
[\<cerrno\> (errno.h)](C library/cerrno/README.md)          | C 错误 (_头文件_)
[\<cfenv\> (fenv.h)](C library/cfenv/README.md)             | 浮点环境 (_头文件_)
[\<cfloat\> (float.h)](C library/cfloat/README.md)          | 浮点类型特性 (_头文件_)
[\<cinttypes\> (inttypes.h)](C library/cinttypes/README.md) | C 整数类型 (_头文件_)
[\<ciso646\> (iso646.h)](C library/ciso646/README.md)       | ISO 646 可选操作符拼写 (_头文件_)
[\<climits\> (limits.h)](C library/climits/README.md)       | 整数类型的大小 (_头文件_)
[\<clocale\> (locale.h)](C library/clocale/README.md)       | C 本地化库 (_头文件_)
[\<cmath\> (math.h)](C library/cmath/README.md)             | C 数学库 (_头文件_)
[\<csetjmp\> (setjmp.h)](C library/csetjmp/README.md)       | 非局部跳转 (_头文件_)
[\<csignal\> (signal.h)](C library/csignal/README.md)       | 处理信号的 C 库 (_头文件_)
[\<cstdarg\> (stdarg.h)](C library/cstdarg/README.md)       | 可变数量参数处理 (_头文件_)
[\<cstdbool\> (stdbol.h)](C library/cstdbool/README.md)     | 布尔类型 (_头文件_)
[\<cstddef\> (stddef.h)](C library/cstddef/README.md)       | C 标准定义 (_头文件_)
[\<cstdint\> (stdint.h)](C library/cstdint/README.md)       | 整数类型 (_头文件_)
[\<cstdio\> (stdio.h)](C library/cstdio/README.md)          | 操作输入/输出的 C 库 (_头文件_)
[\<cstdlib\> (stdlib.h)](C library/cstdlib/README.md)       | C 标准通用工具库 (_头文件_)
[\<cstring\> (string.h)](C library/cstring/README.md)       | C 字符串 (_头文件_)
[\<ctgmath\> (tgmath.h)](C library/ctgmath/README.md)       | 类型泛化的数学 (_头文件_)
[\<ctime\> (time.h)](C library/ctime/README.md)             | C 时间库 (_头文件_)
[\<cuchar\> (uchar.h)](C library/cuchar/README.md)          | Unicode 字符 (_头文件_)
[\<cwchar\> (wchar.h)](C library/cwchar/README.md)          | 宽字符 (_头文件_)
[\<cwctype\> (wctype.h)](C library/cwctype/README.md)       | 宽字符类型 (_头文件_)


## 容器

头文件                                                   | 描述
-------------------------------------------------------- | ---------------------
[\<array\>](Containers/array/README.md)                  | Array (_头文件_)
[\<bitset\>](Containers/bitset/README.md)                | Bitset (_头文件_)
[\<deque\>](Containers/deque/README.md)                  | Deque (_头文件_)
[\<forward\_list\>](Containers/forward_list/README.md)   | Forward list (_头文件_)
[\<list\>](Containers/list/README.md)                    | List (_头文件_)
[\<map\>](Containers/map/README.md)                      | Map (_头文件_)
[\<queue\>](Containers/queue/README.md)                  | Queue (_头文件_)
[\<set\>](Containers/set/README.md)                      | Set (_头文件_)
[\<stack\>](Containers/stack/README.md)                  | Stack (_头文件_)
[\<unordered\_map\>](Containers/unordered_map/README.md) | Unordered map (_头文件_)
[\<unordered\_set\>](Containers/unordered_set/README.md) | Unordered set (_头文件_)
[\<vector\>](Containers/vector/README.md)                | Vector (_头文件_)


## 输入/输出流库

使用 _流_ 这种抽象概念，来执行像文件和字符串这样的序列字符的输入输出操作。

在下面的关系图上，展示了这个功能涉及的多个相关联的类以及对应的头文件名字。

![images](images/iostream.gif)


## 原子和线程库

头文件                                                                  | 描述
----------------------------------------------------------------------- | -------------------------
[\<atomic\>](Multi-threading/atomic/README.md)                          | Atomic (_头文件_)
[\<condition\_variable\>](Multi-threading/condition_variable/README.md) | Condition variable (_头文件_)
[\<future\>](Multi-threading/future/README.md)                          | Future (_头文件_)
[\<mutex\>](Multi-threading/mutex/README.md)                            | Mutex (_头文件_)
[\<thread\>](Multi-threading/thread/README.md)                          | Thread (_头文件_)


## 其他头文件
