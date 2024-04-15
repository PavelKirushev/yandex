# B. Чётные и нечётные числа
<img src="https://github.com/PavelKirushev/yandex/assets/137924137/c747e125-d253-4ad8-a32f-816d216e162e" alt="Ближайший ноль" width="600">

## Решение
```python
a, b, c = map(int, input().split())
if a % 2 == b % 2 and a % 2 == c % 2:
    print('WIN')
else:
    print("FAIL")
```
