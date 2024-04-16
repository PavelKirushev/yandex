# J. Списочная очередь

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/7c55afa6-c06e-4e13-9ba5-bf51decbb8c1" alt="Ближайший ноль" width="600">

## Решение
```python
class node:
    def __init__(self, val=None, next=None):
        self.val = val
        self.next = next

class queue:
    def __init__(self, head = None, tail = None):
        self.head = head
        self.tail = tail
        self.size = 0

    def get(self):
        if self.head == None:
            print("error")
            return
        print(self.head.val)
        self.head = self.head.next
        self.size -= 1

    def put(self, x):
        if self.head == None:
            self.head = node(val=x, next=None)
            self.tail = self.head
            self.size += 1
            return
        self.tail.next = node(val=x, next=None)
        self.tail = self.tail.next
        self.size += 1


    def output(self):
        tmp = self.head
        while tmp:
            print(tmp.val)
            tmp = tmp.next

    def sizet(self):
        print(self.size)


q = queue()
while 1:
    print("Enter command")
    print("1.get 2.put 3.size 4.print 5.end")
    m = int(input())
    if m == 1:
        q.get()
    elif m == 2:
        print("Enter x: ")
        x = int(input())
        q.put(x)
    elif m == 3:
        q.sizet()
    elif m == 4:
        q.output()
    elif m == 5:
        break
    else:
        continue
```
