# K. Рекурсивные числа Фибоначчи

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/68b90625-e20a-4164-b91b-c6b79770df9d" alt="Ближайший ноль" width="600">

## Решение
```python
def f(n):
    if n == 1 or n == 2:
        return 1
    return f(n - 1) + f(n - 2)

n = int(input())
a = f(n + 1)
print(a)
```
