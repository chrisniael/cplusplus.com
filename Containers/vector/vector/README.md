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

与其他动态序列式容器([deques](../deque/deque/README.md)，[lists](../list/list/README.md) 和 [forward_lists](../forward_list/forward_list/README.md))相比，vector 访问它的元素还是很高效的，在尾部添加和移除元素相对也很高效。在除了尾部以外的位置插入或移除元素，vector 都没有其他容器高效，并且比 lists 和 forward_lists 拥有更少的稳定的迭代器（迭代器会失效）。


## 容器属性

#### 序列化
    序列式容器中的元素排列在一个严格线性的序列中。

#### 动态数组


#### 容器感知的

