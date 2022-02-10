## What
- destroys objects to free up memory
## Types it destroys
### Unreachable objects
	- an object with no reference
#### Example of unreachable
```java
int i = 4;
i = null;
```


### Phantom
```java 
Date a = new Date(12,31,1999);
Date b = new Date(1,1,2011);

a = b

```
- since they are now refencing the same object, the object that was *12,31,1999* can no longer be reachable. 
	-therefore, that area of memory can be deleted since it is now unreachable