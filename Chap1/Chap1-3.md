警惕 **unsigned** 类型，下面的代码不会运行至 *printf* 函数，因为 *TOTAL_ELEMENT* 是一个 **unsigned** 类型，而-1(在 **unsigned** 下)是一个很大的数。

```c
int array[] = {23, 34, 12, 17};
#define TOTAL_ELEMENTS (sizeof(array)/sizeof(array[0]))

int main() {
    int d = -1, x;
    if(d <= TOTAL_ELEMENTS - 2)
        printf("%s\n", "running here!\n");
    return 0;
}
```
> 注意这个宏使用的是 *array[0]* 这样无需修改宏就可以把它适配到其他类型了。