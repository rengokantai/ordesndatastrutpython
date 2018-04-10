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
    n = self.head
    last = None
    while n!=None:
      if n.value==value:
        if last is None:
          self.head = self.head.next
        else:
          last.next = n.next
        return True
    last = n
    return False
      
  def pop(self):
    if self.head is None:
      raise Exception("empty list")
    val = self.head.value
    self.head = self.head.next
    return val
  def __iter__(self):
    n = self.head
    while n != None:
      yield n.value
      n=n.next
  
```

### Queues
```
def append(self, value):
  newNode = LinkedNode(value, None)
  if self.head is None:
    self.head = self.tail = newNode
  else:
    self.tail.next=newNode
    self.tail=newNode

def isEmpty(self):
  return self.head = None
def pop(self):
  if self.head is None:
    raise Exception("Queue is Empty")
  val = self.head.value
  self.head = self.head.next
  if self.head is None:
    self.tail = None
  return val
````

#### Pointer-Based Queues Summary
Dont need to implement Queue
- Use collections.deque instead
- 5x faster on sample












