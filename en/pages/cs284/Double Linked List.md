## Doubly linked list
- contains two references, one to the next node and one to the previous node
	- therefore, contains three fields total
		- the data
		- the reference to the next
		- the reference to the previous
- see also [Linked list](Linked%20Links.md)
### Uses
- can traverse both forward and backward
- delete more efficient (given the node pointer)
- quickly insert a new node before a given node
- get the previous node using previous pointer
### Disadvantages
 - extra space needed for previous pointers
 - all operations need to maintain previous pointers
## Operations

### Insert from beginning

``` java


Node newnode = new Node();

newnode.item = "ITEM";

---

newnode.next = head;
newnode.prev = Null;

----

if (head!=Null) head.prev = newnode; // works since head references the previous first

head = newnode; // changes head

```

### Insert at the end
``` java
Node newnode = new Node(data)

Node last = head;


---
newnode.next = NULL;


---

last.next = newnode;

---

newnode.prev

if (head == Null){

	newnode.prev = null;
	head = newnode;
	return;
}

while (last.next != null){
	last = last.next;
}

last.next = newnode;

newnode.prev = last;

```
