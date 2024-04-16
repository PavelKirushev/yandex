# L. Фибоначчи по модулю

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/23c42589-933a-4e3f-9ef3-81895c905a9f" alt="Ближайший ноль" width="600">

## Решение
```python
def f(n, k):
    if n == 1 or n == 2:
        return 1
    return (f(n - 1, k) + f(n - 2, k)) % (10 ** k)

n, k = map(int, input().split())
a = f(n + 1, k)
print(a)
```
