# J. Факторизация

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/bdd5e6b4-811b-4d14-926e-7fb7c7b78566" alt="Ближайший ноль" width="600">

## Решение
```python
def func(n):
    for i in range(2, n + 1):
        if n % i == 0:
            return False
    return True

n = int(input())
mas = []
j = 2
for i in range(2, n + 1, 1):
    if n % j == 0:
        mas.append(j)
        n //= j
    else:
        j += 1
    if func(n):
        break

print(" ".join(str(x) for x in mas))
```
