# C. Нелюбимое дело

<img src="https://github.com/PavelKirushev/yandex/assets/137924137/1ecc1355-57fc-48fd-b0a5-994c96cf85f4" alt="Ближайший ноль" width="600">

## Решение
```python
class Node:
    def __init__(self, val: int, next=None):
        self.val = val
        self.next = next

class LinkedList:
    def __init__(self, head) -> None:
        self.head = head

    def insert(self, val: int) -> None:
        tmp = self.head
        while tmp.next:
            tmp = tmp.next
        tmp.next = Node(val=val)

    def delete(self, ind: int) -> None:
        tmp = self.head
        num = 1
        while num != ind:
            num += 1
            if num == ind:
                break
            tmp = tmp.next
        tmp.next = tmp.next.next

    def find(self, val):
        tmp = self.head
        ind = -1
        curind = 0
        while tmp.next:
            if tmp.val == val:
                ind = curind
                break
            curind += 1
            tmp = tmp.next
        print("\n" + str(ind))
    def output(self):
        tmp = self.head
        while tmp:
            print(tmp.val, end=" ")
            tmp = tmp.next

head = Node(10)
ll = LinkedList(head=head)
ll.insert(15)
ll.insert(30)
ll.delete(2)
ll.insert(20)
ll.output()
ll.find(13)
```
