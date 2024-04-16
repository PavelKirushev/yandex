# F. Стек - Max

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/7b502869-11c5-4714-a5da-e6cc7f6be0c0" alt="Ближайший ноль" width="600">

## Решение
```python
class StackMax:
    def __init__(self) -> None:
        self.items = []

    def push(self, x):
        self.items.append(x)

    def pop(self):
        if len(self.items) == 0:
            print("error")
            return
        self.items.pop()

    def get_max(self):
        if len(self.items) == 0:
            print("None")
            return
        print(max(self.items))


ll = StackMax()
ll.push(8)
ll.push(5)
ll.push(11)
ll.push(9)
ll.pop()
ll.get_max()
print(ll.items)
```
