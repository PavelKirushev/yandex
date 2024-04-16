# A. Дек
<img src="https://github.com/PavelKirushev/yandex/assets/137924137/e1b27463-c641-4b39-bdb6-6e1e1af34b51" alt="A. Дек" width="600">

## Решение
### Первая реализция
```python
def dekReal(m):
    dek = [None] * m
    return dek

def push_back(dek, x, t):
    if dek.count(None) == 0:
        print("error")
        return t
    dek[t] = x
    t = (t + 1) % len(dek)
    return t

def push_front(dek, x, h):
    if dek.count(None) == 0:
        print("error")
        return h
    h = (h - 1) % len(dek)
    dek[h] = x
    return h

def pop_front(dek, h):
    if dek.count(None) == len(dek) or dek[h] == None:
        print("error")
        return h
    dek[h] = None
    h = (h + 1) % len(dek)
    return h

def pop_back(dek, t):
    if dek.count(None) == len(dek) or dek[(t - 1) % len(dek)] == None:
        print("error")
        return t
    t = (t - 1) % len(dek)
    dek[t] = None
    return t

h = 0
t = 0
n = int(input())#операций
m = int(input())#size
dek = dekReal(m)
for i in range(n):
    st = input().split()
    if st[0] == "push_front":
        x = int(st[1])
        h = push_front(dek, x, h)
        print(dek)
    if st[0] == "push_back":
        x = int(st[1])
        t = push_back(dek, x, t)
        print(dek)
    if st[0] == "pop_back":
        t = pop_back(dek, t)
        print(dek)
    if st[0] == "pop_front":
        h = pop_front(dek, h)
        print(dek)
```

### Вторая реализация
```python
class deque:
    def __init__(self, n):
        self.deque = [None] * n
        self.head = 0
        self.tail = 0
        self.len = n

    def push_back(self, val):
        if self.deque.count(None) == 0:
            print("error")
            return
        if self.head == self.tail:
            self.deque[self.tail] = val
            self.tail = (self.tail + 1) % self.len
            return
        self.deque[self.tail] = val
        self.tail = (self.tail + 1) % self.len
        return

    def push_front(self, val):
        if self.deque.count(None) == 0:
            print("error")
            return
        if self.head == self.tail:
            self.deque[self.tail] = val
            self.tail = (self.tail + 1) % self.len
            return
        self.head = (self.head - 1) % self.len
        self.deque[self.head] = val
        return

    def pop_back(self):
        if self.deque.count(None) == self.len:
            print("error")
            return
        self.tail = (self.tail - 1) % self.len
        self.deque[self.tail] = None
        return

    def pop_front(self):
        if self.deque.count(None) == self.len:
            print("error")
            return
        self.deque[self.head] = None
        self.head = (self.head + 1) % self.len
        return

    def output(self):
        print(self.deque)

print("Enter count of elements: ")
n = int(input())
d = deque(n)
while 1:
    print("Enter command:")
    print("1.push_back 2.push_front 3.pop_back 4.pop_front 5.print 6.exit")
    m = int(input())
    if m == 1:
        print("Enter x:")
        x = int(input())
        d.push_back(x)
    elif m == 2:
        print("Enter x:")
        x = int(input())
        d.push_front(x)
    elif m == 3:
        d.pop_back()
    elif m == 4:
        d.pop_front()
    elif m == 5:
        d.output()
    elif m == 6:
        break
    else:
        continue
```
