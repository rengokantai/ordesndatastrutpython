# ordesndatastrutpython
## Pointer Structures
### Linked Lists
```
class LinkedNode:
  def __init__(self,value,tail=None):
    self.value=value
    self.next=tail
class LinkedList:
  def __init__(self,*start):
    self.head = None
    for _ in start:
      self.prepend(_)
  def prepend(self,value):
    self.head = LinkedNode(value,self.head)
  def remove(self,value):
    pass
  def __iter__(self):
    n = self.head
    while n != None:
      yield n.value
      n=n.next
  
```
