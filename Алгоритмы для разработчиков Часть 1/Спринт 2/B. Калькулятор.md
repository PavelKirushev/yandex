# B. Калькулятор

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/444dd017-f251-4842-a528-113b03b9f104" alt="B. Калькулятор" width="600">

## Решение
```python
s = list(map(str, input().split()))
stack = []
res = 0
for i in range(len(s)):
    if s[i].isdigit():
        stack.append(s[i])
    else:
        if s[i] == "+":
            summa = int(stack[-2]) + int(stack[-1])
            stack.pop()
            stack.pop()
            stack.append(summa)
        elif s[i] == "-":
            raz = int(stack[-2]) - int(stack[-1])
            stack.pop()
            stack.pop()
            stack.append(raz)
        elif s[i] == "*":
            pr = int(stack[-2]) * int(stack[-1])
            stack.pop()
            stack.pop()
            stack.append(pr)
        elif s[i] == "/":
            ch = int(stack[-2]) // int(stack[-1])
            stack.pop()
            stack.pop()
            stack.append(ch)
res = stack[0]
print(res)
```
