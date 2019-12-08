**typedef** 类似于宏文本替换，他并没有引入新类型，而是为现有类型取个新名字。

例子：`void (*signal(int sig, void(*func)(int)))(int)`

使用刚才的技巧：signal是一个函数指针，signal本身具有一些可怕的参数，这个指针指向的函数具有一个int型的参数，返回值是void。

在不理会参数的情况下，我们把它改写成如下的形式：
`void(*signal())(int)` => `void(*func)(int)`

`typedef void(*ptr_to_func)(int)`

`ptr_to_func signal(int, ptr_to_func) //这条语句与最开始的那条等价`

**注意：** **typedef** 声名的变量均是同一种类型，然而 **#define** 定义的类型无法保证

```c
#define int_ptr int *
int_ptr chalk, cheese;
typedef char * char_ptr;
char_ptr Bentley, Rolls_Royce; 
```

在上面的例子中， chalk 是一个指针，而 cheese 只是一个 **int** 型变量；相反，使用 **typedef** 则全部都是指针，这也是期望的结果。
