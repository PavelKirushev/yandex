# I. Ограниченная очередь

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/4fc70d3c-4bd7-449b-a019-6e85340643a4" alt="Ближайший ноль" width="600">

## Решение
```python
class queue:
    def __init__(self, n):
        self.queue = [None] * n
        self.max_n = n
        self.head = 0
        self.tail = 0
        self.size = 0

    def push(self, x):
        if self.queue.count(None) == 0:
            print("error")
            return
        self.queue[self.tail] = x
        self.tail = (self.tail + 1) % self.max_n
        self.size += 1

    def pop(self):
        self.queue[self.head] = None
        self.head = (self.head + 1) % self.max_n
        self.size -= 1

    def output(self):
        print(self.queue)

    def peek(self):
        print(self.queue[0])

    def sizet(self):
        print(self.max_n)

print("Enter count of queue: ")
n = int(input())
q = queue(n)
while 1:
    print("Enter command")
    print("1.Push 2.Pop 3.Peek 4.Size 5.Print 6.end")
    m = int(input())
    if m == 1:
        print("Enter x: ")
        x = int(input())
        q.push(x)
    elif m == 2:
        q.pop()
    elif m == 3:
        q.peek()
    elif m == 4:
        q.sizet()
    elif m == 5:
        q.output()
    elif m == 6:
        break
    else:
        continue
```
