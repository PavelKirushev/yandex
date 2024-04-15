# G. Работа из дома

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/6179131e-c1a8-429a-9742-ff9170ab342e" alt="Ближайший ноль" width="600">

## Решение
```python
n = int(input())
dv = ""
while n != 0:
    dv += str(n % 2)
    n //= 2
dv = dv[::-1]
print(dv)
```
