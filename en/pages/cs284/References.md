## What
- **reference** is an address that indicates where an **object's** variables and methods are stored
- only stores the address, not object
	- remember [Primitive Types#Storing in Memory](Primitive%20Types#Storing%20in%20Memory.md)
- 

## Referencing an object
- Java is Call-by-value
- when you assign an object to a variable, you are assigning its address

### Examples
1.
```java

int [] data1 = {somearray};
int [] data2 = data1;

data2[0] = 8;

```
- since it copies that **address**, then data 2 will also change data1
#### To avoid this
	- using the *clone* method 
```java

int [] data1 = {somearray};
int [] data2 = data1.clone();

data2[0] = 8
```

## Types of References
- strong
- weak
	- Weak reference will be marked for garbage collection
	- [Garbage Collection](Garbage%20Collection.md)
- soft
- phantom
	- eligible for [Garbage Collection](Garbage%20Collection.md), but gets put into a queue
	- 

