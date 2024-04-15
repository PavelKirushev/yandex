# B. Ловкость рук

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/0eab7947-ef06-4516-9485-5751ec316d16" alt="Ближайший ноль" width="600">

## Решение
```python
k = int(input())
mas = []
for i in range(4):
    arr = [arr for arr in input()]
    mas += arr
cnt = 0
for i in range(1, 10):
    if k * 2 >= mas.count(str(i)) and str(i) in mas:
        cnt += 1
print(cnt)
```
