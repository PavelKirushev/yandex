# I. Степень четырёх

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/48c56e6e-5fbc-4589-a4f5-18a15c6d3970" alt="Ближайший ноль" width="600">

## Решение
```python
n = int(input())
a = False
for i in range(7):
    if n == 4 ** i:
        a = True
print(a)

```
