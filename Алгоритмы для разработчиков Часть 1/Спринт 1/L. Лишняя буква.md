# L. Лишняя буква

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/05e971a0-2ca1-4b99-93a7-25a7e00a3a31" alt="L. Лишняя буква" width="600">

## Решение
```python
s = [s for s in input()]
t = [t for t in input()]
for i in t:
    if i not in s or s.count(i) != t.count(i):
        print(i)
        break
```
