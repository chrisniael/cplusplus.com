# 参考手册

标准 C++ 库参考手册

## [C 库](C library/README.md)

这些 C 语言库的头文件是 C++ 标准库的子集，涵盖了很多方面，包括通用工具库、输入/输出函数的宏和动态内存管理的函数。

头文件                                                      | 描述
----------------------------------------------------------- | ----------------------
[&lt;cassert&gt; (assert.h)](C library/cassert/README.md)       | C 诊断库 (_头文件_)
[&lt;cctype&gt; (ctype.h)](C library/cctype/README.md)          | 字符处理函数 (_头文件_)
[&lt;cerrno&gt; (errno.h)](C library/cerrno/README.md)          | C 错误 (_头文件_)
[&lt;cfenv&gt; (fenv.h)](C library/cfenv/README.md)             | 浮点环境 (_头文件_)
[&lt;cfloat&gt; (float.h)](C library/cfloat/README.md)          | 浮点类型特性 (_头文件_)
[&lt;cinttypes&gt; (inttypes.h)](C library/cinttypes/README.md) | C 整数类型 (_头文件_)
[&lt;ciso646&gt; (iso646.h)](C library/ciso646/README.md)       | ISO 646 可选操作符拼写 (_头文件_)
[&lt;climits&gt; (limits.h)](C library/climits/README.md)       | 整数类型的大小 (_头文件_)
[&lt;clocale&gt; (locale.h)](C library/clocale/README.md)       | C 本地化库 (_头文件_)
[&lt;cmath&gt; (math.h)](C library/cmath/README.md)             | C 数学库 (_头文件_)
[&lt;csetjmp&gt; (setjmp.h)](C library/csetjmp/README.md)       | 非局部跳转 (_头文件_)
[&lt;csignal&gt; (signal.h)](C library/csignal/README.md)       | 处理信号的 C 库 (_头文件_)
[&lt;cstdarg&gt; (stdarg.h)](C library/cstdarg/README.md)       | 可变数量参数处理 (_头文件_)
[&lt;cstdbool&gt; (stdbol.h)](C library/cstdbool/README.md)     | 布尔类型 (_头文件_)
[&lt;cstddef&gt; (stddef.h)](C library/cstddef/README.md)       | C 标准定义 (_头文件_)
[&lt;cstdint&gt; (stdint.h)](C library/cstdint/README.md)       | 整数类型 (_头文件_)
[&lt;cstdio&gt; (stdio.h)](C library/cstdio/README.md)          | 操作输入/输出的 C 库 (_头文件_)
[&lt;cstdlib&gt; (stdlib.h)](C library/cstdlib/README.md)       | C 标准通用工具库 (_头文件_)
[&lt;cstring&gt; (string.h)](C library/cstring/README.md)       | C 字符串 (_头文件_)
[&lt;ctgmath&gt; (tgmath.h)](C library/ctgmath/README.md)       | 类型泛化的数学 (_头文件_)
[&lt;ctime&gt; (time.h)](C library/ctime/README.md)             | C 时间库 (_头文件_)
[&lt;cuchar&gt; (uchar.h)](C library/cuchar/README.md)          | Unicode 字符 (_头文件_)
[&lt;cwchar&gt; (wchar.h)](C library/cwchar/README.md)          | 宽字符 (_头文件_)
[&lt;cwctype&gt; (wctype.h)](C library/cwctype/README.md)       | 宽字符类型 (_头文件_)


## [容器](Containers/README.md)

头文件                                                   | 描述
-------------------------------------------------------- | ---------------------
[&lt;array&gt;](Containers/array/README.md)                  | Array (_头文件_)
[&lt;bitset&gt;](Containers/bitset/README.md)                | Bitset (_头文件_)
[&lt;deque&gt;](Containers/deque/README.md)                  | Deque (_头文件_)
[&lt;forward\_list&gt;](Containers/forward_list/README.md)   | Forward list (_头文件_)
[&lt;list&gt;](Containers/list/README.md)                    | List (_头文件_)
[&lt;map&gt;](Containers/map/README.md)                      | Map (_头文件_)
[&lt;queue&gt;](Containers/queue/README.md)                  | Queue (_头文件_)
[&lt;set&gt;](Containers/set/README.md)                      | Set (_头文件_)
[&lt;stack&gt;](Containers/stack/README.md)                  | Stack (_头文件_)
[&lt;unordered\_map&gt;](Containers/unordered_map/README.md) | Unordered map (_头文件_)
[&lt;unordered\_set&gt;](Containers/unordered_set/README.md) | Unordered set (_头文件_)
[&lt;vector&gt;](Containers/vector/README.md)                | Vector (_头文件_)


## [输入/输出流库](Input && Output/README.md)

使用 _流_ 这种抽象概念，来执行像文件和字符串这样的序列字符的输入输出操作。

在下面的关系图上，展示了这个功能涉及的多个相关联的类以及对应的头文件名字。

![images](images/iostream.gif)


## [原子和线程库](Multi-threading/README.md)

头文件                                                                  | 描述
----------------------------------------------------------------------- | -------------------------
[&lt;atomic&gt;](Multi-threading/atomic/README.md)                          | Atomic (_头文件_)
[&lt;condition\_variable&gt;](Multi-threading/condition_variable/README.md) | Condition variable (_头文件_)
[&lt;future&gt;](Multi-threading/future/README.md)                          | Future (_头文件_)
[&lt;mutex&gt;](Multi-threading/mutex/README.md)                            | Mutex (_头文件_)
[&lt;thread&gt;](Multi-threading/thread/README.md)                          | Thread (_头文件_)


## [其他头文件](Other/README.md)

头文件                                                    | 描述
--------------------------------------------------------- | ----------------
[&lt;algorithm&gt;](Other/algorithm/README.md)                | 标准模板库 : 算法 (_库_)
[&lt;chrono&gt;](Other/chrono/README.md)                      | 时间库 (_头文件_)
[&lt;codecvt&gt;](Other/codecvt/README.md)                    | Unicode 转化方面 (_头文件_)
[&lt;complex&gt;](Other/complex/README.md)                    | 复数库 (_头文件_)
[&lt;exception&gt;](Other/exception/README.md)                | 标准异常 (_头文件_)
[&lt;functional&gt;](Other/functional/README.md)              | 函数对象 (_头文件_)
[&lt;initializer\_list&gt;](Other/initializer_list/README.md) | 初始化列表 (_头文件_)
[&lt;iterator&gt;](Other/iterator/README.md)                  | 迭代器定义 (_头文件_)
[&lt;limits&gt;](Other/limits/README.md)                      | 数值范围 (_头文件_)
[&lt;locale&gt;](Other/locale/README.md)                      | 本地化库 (_头文件_)
[&lt;memory&gt;](Other/memory/README.md)                      | 内存元件 (_头文件_)
[&lt;new&gt;](Other/new/README.md)                            | 动态内存 (_头文件_)
[&lt;numeric&gt;](Other/numeric/README.md)                    | 泛型的数值操作 (_头文件_)
[&lt;random&gt;](Other/random/README.md)                      | 随机 (_头文件_)
[&lt;ratio&gt;](Other/ratio/README.md)                        | 比例头文件 (_头文件_)
[&lt;regex&gt;](Other/regex/README.md)                        | 正则表达式 (_头文件_)
[&lt;stdexcept&gt;](Other/stdexcept/README.md)                | 异常类 (_头文件_)
[&lt;string&gt;](Other/string/README.md)                      | 字符串 (_头文件_)
[&lt;system\_error&gt;](Other/system_error/README.md)         | 系统错误  (_头文件_)
[&lt;tuple&gt;](Other/tuple/README.md)                        | Tuple 库  (_头文件_)
[&lt;typeindex&gt;](Other/typeindex/README.md)                | 类型索引 (_头文件_)
[&lt;typeinfo&gt;](Other/typeinfo/README.md)                  | 类型信息 (_头文件_)
[&lt;type\_traits&gt;](Other/type_traits/README.md)           | type\_traits (_头文件_)
[&lt;utility&gt;](Other/utility/README.md)                    | 工具组件 (_头文件_)
[&lt;valarray&gt;](Other/valarray/README.md)                  | 数值数组库 (_头文件_)
