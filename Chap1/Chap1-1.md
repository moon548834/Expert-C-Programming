> 在宏的拓展中，空格会对拓展的结果有很大的影响。

```c
#define a(y) a_expanded(y)
a(x);
```
会被拓展为 `a_expanded(x)`，而
```c
#define a (y) a_expanded(y)
a(x);
```
会被拓展为 `a_expaneded (y)(x)`
