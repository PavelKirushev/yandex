# G. Стек - MaxEffective

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/eb1aac52-e906-4422-8464-0d742de4b644" alt="Ближайший ноль" width="600">

## Решение
```python
class StackMax:
    def __init__(self) -> None:
        self.items = []
        self.max = []

    def push(self, x):
        self.items.append(x)
        if not self.max or x > self.max[-1]:
            self.max.append(x)

    def pop(self):
        if len(self.items) == 0:
            print("error")
            return
        self.items.pop()

    def get_max(self):
        if len(self.items) == 0:
            print("None")
            return
        print(self.max[-1])


ll = StackMax()
ll.push(8)
ll.push(5)
ll.push(11)
ll.push(9)
ll.pop()
ll.get_max()
print(ll.items)
```
