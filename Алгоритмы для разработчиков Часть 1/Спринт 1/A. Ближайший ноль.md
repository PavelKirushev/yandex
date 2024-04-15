<img src="https://github.com/PavelKirushev/yandex/assets/137924137/4a377446-d04c-4e3e-946e-284426a3dd76" alt="Ближайший ноль" width="600">

## Решение
```python
n = int(input())
mas = list(map(int, input().split()))
ind = mas.index(0)
i = ind
num = 0
while num != ind:
    mas[num] = i
    i -= 1
    num += 1
if mas.count(0) > 1:
    for j in range(mas.count(0) - 1):
        ind2 = mas.index(0, ind + 1)
        num = 1
        for i in range(1, (ind2 - ind ) // 2  + 1):
            mas[ind + i] = num
            mas[ind2 - i] = num
            num += 1
        ind = ind2
num = len(mas) - 1
i = 0
while ind != num + 1:
    mas[ind] = i
    i += 1
    ind += 1
print(" ".join(str(x) for x in mas))
```
