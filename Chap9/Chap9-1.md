之所以把传递给函数的数组参数转换给指针是出于效率的考虑(但其实其实写成 `void test(int array[10]);` 调用 `test` 的时候也不会拷贝)

对于实参要进行一份拷贝并传递给调用的函数，函数不修改实参实际变量的值，而只修改传递给它的那份拷贝。但如果要拷贝整个数组，开销会很大。