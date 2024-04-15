# E. Самое длинное слово

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/4598d232-7071-4052-b30b-f04548efac21" alt="E. Самое длинное слово" width="600">

## Решение
```python
n = int(input())
s = input()
cnt = 0
cntmax = 0
slovo = ""
slovomax = ""
for i in range(n):
    if s[i] != " ":
        cnt += 1
        slovo += s[i]
    else:
        if cnt > cntmax:
            cntmax = cnt
            slovomax = slovo
        slovo = ""
        cnt = 0
print(slovomax)
print(cntmax)
```
