
## Definition
- a recursive data structure that is either empty null or a reference to a [Nodes](Nodes.md) having generic item and a reference to a linked list
## Linked List 
- linear data structure, but not contiguous
- starts with a head and ends with a null
	- null makes sure the end node does not point to unexpected data
- non-contiguous memory locations
- uses [Nodes](Nodes.md)
- linked using pointers
	- address of the next element in the structure
	- acts like [References](References.md)

## Traverse
- assuming you have a node class with <mark style="background: #D2B3FFA6;">Node.item</mark> and the <mark style="background: #D2B3FFA6;">Node.next</mark> 

``` java

for (Node x = first; x ! = null; x = x.next){
	// process x.item

}

```


## Remove Element from a linked list
### From Beginning
- point the head to the second element in the linked list, skipping the first
```java

first = first.next;

```
### From the end
- point the second to last element to Null, skipping the last element
```java
secondToLast = null;
```

## adding elements
### From Beginning
```java 
Node oldFirst = first
first = new Node();
first.item = "item";
first.next = oldFirst; // oldFirst is the original first element
```
- renaming elements might be necessary for cleaner code
### From End
```java

Node oldLast = last
last = new Node();
last.item = "item";
last.next = null;

```
### From the Middle

```java

newnode.next = previousnode.next;

```

## Drawbacks
- random access not allowed
- extra memory space to link to another element
- expensive to insert a node since you must go through each one
	- solution is [Double Linked List](Double%20Linked%20List.md)