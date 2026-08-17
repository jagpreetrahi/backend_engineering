### Arrays

An array is a data struture that holds a similar data type items in a single contiguous memory space.

##### Types 
    - 1-D array : A single line block of contiguous memory.

    - 2-D array : Array of arrays that stores elements in rows and columns format.

    - 3-D array : It contain the volumentric structue like cube to store the items.

#### Why need Array
    - Group data: Hold multiple values into a single variable instead of making a separate variable for each items.

    - Save memory : It stores the data in a continuous memory cells and has no extra pointer and no memory addresss like linked list.

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
  - End : O(1) - If there is an empty space available next to it, otherwise it doubling the size, copying the old array values and put them with the new value into an new one.
  ```
  This is also called as amortized O(1) means average cost of opertion over a long sequence of operations, in which some operation can take expensive cost. while doubling the size, the cost reduces significantly and becomes a constant time
  ```

  - Middle - O(n) 
  ```
   It requires to shift the elements firstly from right to left to prevent the overwrite and copying it. 
  
