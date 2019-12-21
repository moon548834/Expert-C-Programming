强制类型转换(cast)

```c
(float) 3
(float) 3.0
```

第一行是一个类型转换，并且实际的二进制位也发生了改变；而第二个只是消除类型歧义。

关于**void\***:
```c
void qsort(void base, size_t nel, size_t width,
    int (*compar)(const void *, const void *))
```

当调用qsort的时候，可以传递一个比较函数，它的比较函数将接受实际的数据类型而不是**void\***参数，就像下面这样：

```c
int intcompare(const int *i, const int *j) {
    return (*i - *j);
}
```
这个时候应该这样传递compar参数:

```c
(int (*)(const void *, const void *))intcompare
```

这样就没有警告了。

> 虽然直接写 `intcompare` 也可以得到正确结果