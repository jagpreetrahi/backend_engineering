### Arrays

An array is a data structure that stores elements in an ordered sequence, typically using the contiguous memory in convetional array implementations, allowing efficient indexed access.

##### Types 
    - 1-D array : A single line block of contiguous memory.

    - 2-D array : Array of arrays that stores elements in rows and columns format.

    - 3-D array : It's about multiple 2D layers 

#### Why need Array
    - Group data: Hold multiple values into a single variable instead of making a separate variable for each items.

    - Contiguous storage : excellent locality

    - Fast Access : Instanly looks up for an elements by using a direct math 
       
    - Easy loops : It helps to iterate step by step for an items.

#### How they work
    - Memory Layout : Saves an array in a straight line of memory boxes back to back.

    - Every box has a number called index number that helps to find out an elements.

    - Direct Math : Find any items instantly by 
    Formula - Starting memory address + (index * size of the data type)
    

#### What actually do
    - Stores items 
    - Sort and searches 
    - Build structures further for another data 


#### Time Complexity  
For retrieving an element anywhere - O(1) fast access, constant time 
````
 Example : arr[] = [5,3,6,8,3]
    arr[2] = 6 : O(1)
````

For storing i.e. inserting an elements 
  - Start : O(n)
    ```
    Example : arr[] = [2,3,4,5]

    I want to store value 1 at the starting index, so for that i need to shift the element from left to right to require space at that place, takes O(n) while shifiting.
    ```
  - End : O(1) - If there is an empty space available next to it, and when the capacity is exhausted, a dynamic array may allocate a larger memory region and copy its elements. The occasional expensive resize is why append can still have amortized O(1) complexity.
  ```
  This is also called as amortized O(1) means average cost of opertion over a long sequence of operations, in which some operation can take expensive cost. while doubling the size, the cost reduces significantly and becomes a constant time
  ```

  - Middle - O(n) 
  ```
   It requires to shift the elements firstly from right to left to prevent the overwrite and copying it. 


#### Why does contiguous memory matter ?

Because modern CPUs use caches.

```
Arrays are highly efficient for sequential processing due to the CPU cache locality.

Contiguous memory layout - 
1. Sequential management : Unbroken block of physical memory
2. Predictable Addressing 


CPU cache utilization 
1. Cache lines : fetch data in blocks 
2. Prefetching : Automatically loads the next several elements.
3. Cache Hits : Sequential loops read directly from the cache instead of the main memory.


```

### Static vs Dynamic arrays

Static array : Fixed capacity

Dynamic array : 
    1. grow when the capacity is exhausted.
    2. usually allocates a larger block i.e. double size.
    3. Copy/move elements
    4. Expensive resize occasionally
    5. Amortized O(1) append


## Backend Revelance 

Array/dynamic array appear in :

1. request results
2. Batches of databases record
3. API response collections
4. queues/buffers

```
Main point is to ask as 

What operation will I perform frequently, and which data structure makes that operation cheap.

```

  
