```c
int apricot[2][3][5];
int (*r)[5] = apricot[0];
int *t = apricot[0][0];
```

r的步进是 20 t的步进是 4

> 如果把一个C语言的矩阵传递给一个fortran程序，矩阵就会自动转置