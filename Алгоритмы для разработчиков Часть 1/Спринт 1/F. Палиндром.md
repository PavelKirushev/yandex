# F. Палиндром

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/13c8072b-3a6d-4788-affa-ddb8c0618989" alt="Ближайший ноль" width="600">

## Решение
```python
s = input()
st = ""
for i in range(len(s)):
    if s[i].isalpha():
        st += s[i].lower()
if st == st[::-1]:
    print("True")
else:
    print("False")
```
