# H. Двоичная система
<img src="https://github.com/PavelKirushev/yandex/assets/137924137/d92c6d4c-38e8-4cb5-aa5e-9b3f3dcb012a" alt="H. Двоичная система" width="600">

## Решение
```python
a = input()
b = input()
a1 = 0
b1 = 0
for i in range(len(a)):
    a1 += int(a[i]) * (2 ** (len(a) - 1 - i))
for i in range(len(b)):
    b1 += int(b[i]) * (2 ** (len(b) - 1 - i))
n = a1 + b1
s = ""
while n != 0:
    s += str(n % 2)
    n //= 2
print(s[::-1])

```
