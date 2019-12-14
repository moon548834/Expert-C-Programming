file1.c:
```c
int mango[100];
```

file2.c:
```c
extern int *mango;
```

事实上，这样操作，会在file2中引起错误(在我这里是 segmentation fault)。

改成 `extern int mango[]` 则不会有错误了。