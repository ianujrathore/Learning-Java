# Learning-Java

* Java programming practice and projects! 

* Basic Java Code Template: 
```
  class Main {
       public static void main (String [] args){
         System.out.print("Hello World");
       }
  }
```
## Hashing & Hash Tables

* Hashing is a technique used to map data (keys) to a fixed-size value using a hash function. This value is typically used as an index in an array for fast data access.
A hash table is a data structure that stores key–value pairs and uses hashing to achieve average-case O(1) time complexity for insertion, deletion, and lookup.
* How it Works
A hash function converts a key into an array index.
The value is stored at that index in the hash table.
When searching, the same hash function is used to find the index again.
* Collisions
A collision occurs when two different keys produce the same hash index. Common collision-handling techniques include:
Chaining (storing multiple values in a list at the same index)
Open Addressing (finding another empty slot using probing)
* Key Points
Fast access compared to arrays and linked lists
Performance depends on a good hash function
Widely used in databases, caches, and dictionaries/maps

## Sorting Algorithms

* This repository provides implementations of Selection Sort, Bubble Sort, and Insertion Sort, focusing on clarity and fundamental algorithmic concepts.

## Time & Space Complexity

Selection Sort

* Best Case: O(n²)

* Average Case: O(n²)

* Worst Case: O(n²)

* Space Complexity: O(1)

Bubble Sort

* Best Case: O(n)

* Average Case: O(n²)

* Worst Case: O(n²)

* Space Complexity: O(1)

Insertion Sort

* Best Case: O(n)

* Average Case: O(n²)

* Worst Case: O(n²)

* Space Complexity: O(1)

Merge Sort

* Best Case: O(n log n)

* Average Case: O(n log n)

* Worst Case: O(n log n)

* Space Complexity: O(n)

Quick Sort

* Best Case: O(n log n)

* Average Case: O(n log n)

* Worst Case: O(n²)

* Space Complexity: O(log n)

Searching Algorithm
* Linear Search
  ```
  LinearSearch(A, n, key)
    for i ← 0 to n - 1 do
        if A[i] = key then
            return i      // element found at index i
        end if
    end for
    return -1             // element not found
  ```
* Binary Search
