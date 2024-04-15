# D. Хаотичность погоды

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/ace0ed48-a960-44b3-b876-4ff5cf21e0b3" alt="D. Хаотичность погоды" width="600">


## Решение
```python
n = int(input())
mas = list(map(int, input().split()))
cnt = 0
if mas[0] > mas[1]:
    cnt += 1
if mas[-1] > mas[-2]:
    cnt += 1
for i in range(1, n - 2):
    if mas[i] > mas[i - 1] and mas[i] > mas[i + 1]:
        cnt += 1
print(cnt)
```
