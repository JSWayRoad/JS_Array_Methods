const arr = [] - dynamic array

RAM - consists from cells where we save bits(биты).  
Every bit is unit of information which can me 0 or 1.
We can work with 8 bits(2 bytes) for one time

When we create an array in JS then  interpreter initializes about 16kBytes of memories(it depends from creaters of interpreter).  

system checks current memory by cycle

When the memory for current array is fool then  system allocates(аллоцирует или выделяет)  
new array which memory = current * 2(about) and an old array will be free for another info.

```
const newArr = [...arr, arr1]
```
