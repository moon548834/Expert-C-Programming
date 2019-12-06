```c
generate_initializer(char *string) {
    static char separator = ' ';
    printf(" %c %s\n", separator, string);
    separator = ',';
}
```
在第一次执行时，函数会首先打印一个空格，然后打印字符串。这样做的目的在于“第一次执行的前面加个空格”相比“最后一次执行，省略逗号前缀”要简单一些。
