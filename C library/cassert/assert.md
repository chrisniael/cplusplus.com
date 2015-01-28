宏  

# assert 

\<cassert\>

`void assert(int expression)`


#### 评估断言

如果这个函数形式的宏的参数表达式等于 0（例如 expression 等于 false），那么编译器会调用 `abort` 函数来终止程序，并将消息写入标准错误设备。

虽然消息内容依赖于特定的库实现，但是它至少包括：断言失败的 _expression_ ，源文件的名字，和对应的行号。通常格式如下：

> Assertion failed: _expression_, file _filename_, line _line_ _number_


## 参数

`expression`

expression 会被评估。如果这个 expression 等于 0，则会导致断言失败，并终止程序。

如果在包含 `<assert.h>` 的时候，一个名为 `NDEBUG` 的宏已经被定义，那么 `assert` 宏将被关闭。这个功能使的开发人在调试程序的时候，能在源代码中包含很多 `assert` 调用，而发布版本的时候能关闭所有 `assert` 宏，只需要在代码开始部分，并在包含 `<assert.h>` 前写上这样一行代码：

```
#define NDEBUG
```

因此，`assert` 的设计是用来捕捉程序错误的，而不是用户或者运行时错误，在程序退出调试阶段后，通常都会使用 `NDEBUG` 来关闭这个宏。


## 返回值

无


## 例子

```cpp
/* assert example */
#include <stdio.h>	/* printf */
#include <assert.h> /* assert */

void print_number(int *myInt)
{
	assert(myInt != NULL);
	printf("%d\n", *myInt);
}

int main()
{
	int a = 0;
	int * b = NULL;
	int * c = NULL;

	b = &a;

	print_number(b);
	print_number(c);

	return 0;
}
```

在这个例子中，如果 `print_number` 使用一个空指针作为参数被调用，那么`assert` 会终止程序执行。这种情况发生在第二次调用 `print_number` 时，它触发了一个断言失败，提示了bug的存在。
