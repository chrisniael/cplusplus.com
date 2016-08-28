类模板

# std::vector

<vector>

`templete < class T, class Alloc = allocator<T> > class vector;	//generic template`

#### vector

Vector 是序列式容器，表示大小可变的数组。

和数组一样的地方是，vector 使用连续的空间位置存储元素，这就意味着可以使用带偏移量的普通指针来访问其中的元素，就和像在数组中一样高效。但是和数组不一样的是，vector 的大小可以动态改变，容器会自动处理它们的存储。

vectors 内部使用一个动态分配的数组来存储它们的元素。当新元素被插入时，这个数组为了增加大小可能需要被重新分配，这意味着分配一个新数组，并将所有元素移动到这个新数组中。在处理时间方面这是一个相对昂贵的开销，因此，当元素被添加到容器时，vectors 不会每次都重新分配空间。

vector 容器可能会分配一些额外的存储空间来适应可能的增长，因此容器真实的 [capacity](capacity.md) 可能会大于它当前包含的所有元素的大小(也就是它的 [size](size.md))。不同库可以使用不同的增长策略来平衡内存使用和重新分配，但无论如何，重新分配的区间大小应该呈对数级增长，这样单个元素插入 vector 的尾部才能分摊成常数时间复杂度(请查看 [push_back](push_back.md))。

因此，和数组相比，vector 会消耗更多的内存来换取管理存储以及动态增长的高效性。

与其他动态序列式容器([deques](../../deque/deque/README.md)，[lists](../list/list/README.md) 和 [forward_lists](../forward_list/forward_list/README.md))相比，vector 访问它的元素还是很高效的，在尾部添加和移除元素相对也很高效。在除了尾部以外的位置插入或移除元素，vector 都没有其他容器高效，并且比 [lists](../../list/list/README.md) 和 [forward_lists](../../forward_list/forward_list/README.md) 拥有更少的稳定的迭代器（迭代器会失效）。


## 容器属性

#### 序列化

序列式容器中的元素排列在一个严格线性的序列中。元素可以通过它们在序列中的位置来访问。

#### 动态数组

允许直接访问序列中的任何元素，即使通过指针算数，并且能相对快速地从序列尾部添加/删除元素

#### 内存分配器感知的

容器使用一个内存分配器对象来动态处理它的存储需求。


## 模板参数

`T`

元素的类型。  
仅仅当 T [保证移动的时候不抛出异常](../../../Other/type_traits/is_nothrow_move_constructible.md)，实现才能在重新分配内存的时候进行优化，用移动元素的方式代替拷贝。  
别名是成员类型 vector::value_type

`Alloc`

内存分配器对象的类型，用来定义存储分配器模型。默认使用 [allocator](../../../Other/memory/allocator/README.md) 类模板，它定义了最简单的内存分配模型并且是与值无关的。  
别名是成员类型 vector::allocator_type


## 成员类型

#### C++98

类型名          | 定义                   | 注释
--------------- | -----------------------|----------------------------------
value_type      | 第一个模板参数 (T)     | 
allocator_type  | 第二个模板参数 (Alloc) | 默认值为：[allocator](../../../Other/memory/allocator/README.md)<value_type>
reference       | allocator_type::reference | 对于默认的 [allocator](../../../Other/memory/allocator/README.md) ：value_type&
const_reference | allocator_type::const_reference | 对于默认的 [allocator](../../../Other/memory/allocator/README.md) ：const value_type&
pointer         | allocator_type::pointer | 对于默认的 [allocator](../../../Other/memory/allocator/README.md) ：value_type*
const_pointer   | allocator_type::const_pointer | 对于默认的 [allocator](../../../Other/memory/allocator/README.md) ：const value_type*
iterator        | 一个指向 value_type 的[随机访问迭代器](../../../Other/iterator/random_access_iterator.md) | 可以转化为 const_iterator
const_iterator  | 一个指向 const value_type 的[随机访问迭代器](../../../Other/iterator/random_access_iterator.md) |
reverse_iterator | [reverse_iterator](../../../Other/iterator/reverse_iterator/README.md)<iterator> |
const_reverse_iterator | [reverse_iterator](../../../Other/iterator/reverse_iterator/README.md)<const_iterator> |


#### C++11


## 成员函数


## 非成员函数重载


## 模板特殊化
