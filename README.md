# 参考手册

标准 C++ 库参考手册

## [C 库](clibrary/README)

这些 C 语言库的头文件是 C++ 标准库的子集，涵盖了很多方面，包括通用工具库、输入/输出函数的宏和动态内存管理的函数。

| 头文件                                                       | 描述                              |
| ------------------------------------------------------------ | --------------------------------- |
| [&lt;cassert&gt; \(assert.h)](clibrary/cassert/README)       | C 诊断库 (_头文件_)               |
| [&lt;cctype&gt; \(ctype.h)](clibrary/cctype/README)          | 字符处理函数 (_头文件_)           |
| [&lt;cerrno&gt; \(errno.h)](clibrary/cerrno/README)          | C 错误 (_头文件_)                 |
| [&lt;cfenv&gt; \(fenv.h)](clibrary/cfenv/README)             | 浮点环境 (_头文件_)               |
| [&lt;cfloat&gt; \(float.h)](clibrary/cfloat/README)          | 浮点类型特性 (_头文件_)           |
| [&lt;cinttypes&gt; \(inttypes.h)](clibrary/cinttypes/README) | C 整数类型 (_头文件_)             |
| [&lt;ciso646&gt; \(iso646.h)](clibrary/ciso646/README)       | ISO 646 可选操作符拼写 (_头文件_) |
| [&lt;climits&gt; \(limits.h)](clibrary/climits/README)       | 整数类型的大小 (_头文件_)         |
| [&lt;clocale&gt; \(locale.h)](clibrary/clocale/README)       | C 本地化库 (_头文件_)             |
| [&lt;cmath&gt; \(math.h)](clibrary/cmath/README)             | C 数学库 (_头文件_)               |
| [&lt;csetjmp&gt; \(setjmp.h)](clibrary/csetjmp/README)       | 非局部跳转 (_头文件_)             |
| [&lt;csignal&gt; \(signal.h)](clibrary/csignal/README)       | 处理信号的 C 库 (_头文件_)        |
| [&lt;cstdarg&gt; \(stdarg.h)](clibrary/cstdarg/README)       | 可变数量参数处理 (_头文件_)       |
| [&lt;cstdbool&gt; \(stdbol.h)](clibrary/cstdbool/README)     | 布尔类型 (_头文件_)               |
| [&lt;cstddef&gt; \(stddef.h)](clibrary/cstddef/README)       | C 标准定义 (_头文件_)             |
| [&lt;cstdint&gt; \(stdint.h)](clibrary/cstdint/README)       | 整数类型 (_头文件_)               |
| [&lt;cstdio&gt; \(stdio.h)](clibrary/cstdio/README)          | 操作输入/输出的 C 库 (_头文件_)   |
| [&lt;cstdlib&gt; \(stdlib.h)](clibrary/cstdlib/README)       | C 标准通用工具库 (_头文件_)       |
| [&lt;cstring&gt; \(string.h)](clibrary/cstring/README)       | C 字符串 (_头文件_)               |
| [&lt;ctgmath&gt; \(tgmath.h)](clibrary/ctgmath/README)       | 类型泛化的数学 (_头文件_)         |
| [&lt;ctime&gt; \(time.h)](clibrary/ctime/README)             | C 时间库 (_头文件_)               |
| [&lt;cuchar&gt; \(uchar.h)](clibrary/cuchar/README)          | Unicode 字符 (_头文件_)           |
| [&lt;cwchar&gt; \(wchar.h)](clibrary/cwchar/README)          | 宽字符 (_头文件_)                 |
| [&lt;cwctype&gt; \(wctype.h)](clibrary/cwctype/README)       | 宽字符类型 (_头文件_)             |

## [容器](containers/README)

| 头文件                                                   | 描述                     |
| -------------------------------------------------------- | ------------------------ |
| [&lt;array&gt;](containers/array/README)                 | Array (_头文件_)         |
| [&lt;bitset&gt;](containers/bitset/README)               | Bitset (_头文件_)        |
| [&lt;deque&gt;](containers/deque/README)                 | Deque (_头文件_)         |
| [&lt;forward_list&gt;](containers/forward_list/README)   | Forward list (_头文件_)  |
| [&lt;list&gt;](containers/list/README)                   | List (_头文件_)          |
| [&lt;map&gt;](containers/map/README)                     | Map (_头文件_)           |
| [&lt;queue&gt;](containers/queue/README)                 | Queue (_头文件_)         |
| [&lt;set&gt;](containers/set/README)                     | Set (_头文件_)           |
| [&lt;stack&gt;](containers/stack/README)                 | Stack (_头文件_)         |
| [&lt;unordered_map&gt;](containers/unordered_map/README) | Unordered map (_头文件_) |
| [&lt;unordered_set&gt;](containers/unordered_set/README) | Unordered set (_头文件_) |
| [&lt;vector&gt;](containers/vector/README)               | Vector (_头文件_)        |

## [输入/输出流库](Input && Output/README)

使用 _流_ 这种抽象概念，来执行像文件和字符串这样的序列字符的输入输出操作。

在下面的关系图上，展示了这个功能涉及的多个相关联的类以及对应的头文件名字。

![images](_assets/iostream.gif)

## [原子和线程库](Multi-threading/README)

| 头文件                                                                  | 描述                          |
| ----------------------------------------------------------------------- | ----------------------------- |
| [&lt;atomic&gt;](Multi-threading/atomic/README)                         | Atomic (_头文件_)             |
| [&lt;condition_variable&gt;](Multi-threading/condition_variable/README) | Condition variable (_头文件_) |
| [&lt;future&gt;](Multi-threading/future/README)                         | Future (_头文件_)             |
| [&lt;mutex&gt;](Multi-threading/mutex/README)                           | Mutex (_头文件_)              |
| [&lt;thread&gt;](Multi-threading/thread/README)                         | Thread (_头文件_)             |

## [其他头文件](Other/README)

| 头文件                                                    | 描述                        |
| --------------------------------------------------------- | --------------------------- |
| [&lt;algorithm&gt;](Other/algorithm/README)               | 标准模板库 : 算法 (_库_)    |
| [&lt;chrono&gt;](Other/chrono/README)                     | 时间库 (_头文件_)           |
| [&lt;codecvt&gt;](Other/codecvt/README)                   | Unicode 转化方面 (_头文件_) |
| [&lt;complex&gt;](Other/complex/README)                   | 复数库 (_头文件_)           |
| [&lt;exception&gt;](Other/exception/README)               | 标准异常 (_头文件_)         |
| [&lt;functional&gt;](Other/functional/README)             | 函数对象 (_头文件_)         |
| [&lt;initializer_list&gt;](Other/initializer_list/README) | 初始化列表 (_头文件_)       |
| [&lt;iterator&gt;](Other/iterator/README)                 | 迭代器定义 (_头文件_)       |
| [&lt;limits&gt;](Other/limits/README)                     | 数值范围 (_头文件_)         |
| [&lt;locale&gt;](Other/locale/README)                     | 本地化库 (_头文件_)         |
| [&lt;memory&gt;](Other/memory/README)                     | 内存元件 (_头文件_)         |
| [&lt;new&gt;](Other/new/README)                           | 动态内存 (_头文件_)         |
| [&lt;numeric&gt;](Other/numeric/README)                   | 泛型的数值操作 (_头文件_)   |
| [&lt;random&gt;](Other/random/README)                     | 随机 (_头文件_)             |
| [&lt;ratio&gt;](Other/ratio/README)                       | 比例头文件 (_头文件_)       |
| [&lt;regex&gt;](Other/regex/README)                       | 正则表达式 (_头文件_)       |
| [&lt;stdexcept&gt;](Other/stdexcept/README)               | 异常类 (_头文件_)           |
| [&lt;string&gt;](Other/string/README)                     | 字符串 (_头文件_)           |
| [&lt;system_error&gt;](Other/system_error/README)         | 系统错误 (_头文件_)         |
| [&lt;tuple&gt;](Other/tuple/README)                       | Tuple 库 (_头文件_)         |
| [&lt;typeindex&gt;](Other/typeindex/README)               | 类型索引 (_头文件_)         |
| [&lt;typeinfo&gt;](Other/typeinfo/README)                 | 类型信息 (_头文件_)         |
| [&lt;type_traits&gt;](Other/type_traits/README)           | type*traits (*头文件\_)     |
| [&lt;cassert&gt; \(assert.h)](clibrary/cassert/README)    | C 诊断库 (_头文件_)         |
| [&lt;utility&gt;](Other/utility/README)                   | 工具组件 (_头文件_)         |
| [&lt;valarray&gt;](Other/valarray/README)                 | 数值数组库 (_头文件_)       |
