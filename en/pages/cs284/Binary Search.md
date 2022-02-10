## What
- an <mark style="background: #BBFABBA6;">efficient</mark> algorithm for finding an item from a sorted list of items
- it searches a sorted array by repeatedly <mark style="background: #FFB8EBA6;">dividing the search interval in half</mark> 
## How
### Goal
- given a sorted array and a key, find the index of the key in the array
### Process
- too small; go left
- too big; go right
- equal to the key; found
	- <mark style="background: #FFB86CA6;">Each time, find the new mid and restart process</mark> 