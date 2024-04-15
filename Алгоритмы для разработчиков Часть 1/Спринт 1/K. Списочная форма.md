# K. Списочная форма

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/f5fb3165-0592-42aa-bd92-fcc14eb3ed03" alt="K. Списочная форма" width="600">

## Решение
```python
n = int(input())
print(" ".join(s for s in str(int("".join(list(map(str, input().split())))) + int(input()))))
```
