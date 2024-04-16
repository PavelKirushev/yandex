# A. Мониторинг

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/4ccca2fb-2f37-47fe-b414-699e604ccef1" alt="A. Мониторинг" width="600">

## Решение
```python
n = int(input())
m = int(input())
mat1 = []
mat2 = []
for i in range(n):
    mat1.append(list(map(int, input().split())))
for i in range(m):
    l = []
    for j in range(n):
        l.append(mat1[j][i])
    mat2.append(l)
print(mat2)
```
