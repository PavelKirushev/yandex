# H. Скобочная последовательность

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/ebb9ba9f-a13a-4671-96cb-691e649cee35" alt="Ближайший ноль" width="600">

## Решение
```python
s = input()
stack = []
for i in range(len(s)):
    if s[i] == "{" or s[i] == "(" or s[i] == "[":
        stack.append(s[i])
    else:
        l = stack[len(stack) - 1]
        if l == "(" and s[i] == ")" or l == "[" and s[i] == "]" or l == "{" and s[i] == "}":
            stack.pop()
        else:
            break

if not stack:
    print("True")
else:
    print("False")
```
