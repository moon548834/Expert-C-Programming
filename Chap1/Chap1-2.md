当试图把一个 **char\*\*** 的变量传递给 **const char\*\*** 时，编译器会给出类型不匹配的警告。

而 **char\*** 与 **const char\*** 确是可以相容的。

比如 *strcpy* 的操作，传递进来的 *src* 自然是 **char** 类型就可以了
```c
inline char *strcpy(char *dest, const char *src) {
    char *tmp = char *dest;
    while( (*dest++ = *src++) != '\0' ) {
        ;
    }
    return tmp;
}
```
