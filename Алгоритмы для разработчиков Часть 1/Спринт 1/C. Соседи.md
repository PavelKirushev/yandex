# C. Соседи

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/b37164c9-d825-4398-89be-2e88370ad636" alt="Ближайший ноль" width="600">

## Решение
```python
def func(mat, x, y):
    l = len(mat)
    w = len(mat[0])
    if y == 0 or y == l - 1:
        if y == 0:
            if x == 0:
                print(mat[0][1], mat[1][0])
            elif x == w - 1:
                print(mat[0][x - 1], mat[1][x])
            else:
                print(mat[0][x - 1], mat[0][x + 1], mat[1][x])
        else:
            if x == 0:
                print(mat[y - 1][0], mat[y][1])
            elif x == w - 1:
                print(mat[y][x - 1], mat[y - 1][x])
            else:
                print(mat[y][x - 1], mat[y - 1][x], mat[y][x + 1])
    elif x == 0 or x == w - 1:
        if x == 0:
            print(mat[y - 1][0], mat[y][1], mat[y + 1][0])
        else:
            print(mat[y][x - 1], mat[y - 1][x], mat[y + 1][x])
    else:
        print(mat[y][x - 1], mat[y - 1][x], mat[y][x + 1], mat[y + 1][x])


n = int(input())
m = int(input())
mat = []
for i in range(n):
    mat.append(list(map(int, input().split())))
y = int(input())
x = int(input())
func(mat, x, y)
```
