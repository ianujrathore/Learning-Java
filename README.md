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

* How it Works :
A hash function converts a key into an array index.
The value is stored at that index in the hash table.
When searching, the same hash function is used to find the index again.

* Collisions :
A collision occurs when two different keys produce the same hash index. Common collision-handling techniques include:
Chaining (storing multiple values in a list at the same index)
Open Addressing (finding another empty slot using probing)

* Key Points :
Fast access compared to arrays and linked lists,
Performance depends on a good hash function,
Widely used in databases, caches, and dictionaries/maps.

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
* Linear Search :
  ```
  LinearSearch(A, n, key)
    for i ← 0 to n - 1 do
        if A[i] = key then
            return i      // element found at index i
        end if
    end for
    return -1             // element not found
  ```
* Binary Search : 
  ```
  BinarySearch(array, target):
    low ← 0
    high ← length(array) - 1

    while low ≤ high:
        mid ← low + (high - low) / 2

        if array[mid] == target:
            return mid

        else if array[mid] < target:
            low ← mid + 1

        else:
            high ← mid - 1

    return -1   // target not found
  ```
# Object Oriented Programming
Object-Oriented Programming is a way of writing code that works like real life. Instead of thinking only in steps or instructions, you think in terms of things (objects) that have properties and can do actions.

* Four pillars of Object Oriented Programming :
1. Encapsulation
Encapsulation is the concept of wrapping data and methods together into a single unit (class) and restricting direct access to the data to protect it from unintended modification.
```
class Student {

    // private variable (hidden from outside)
    private int age;

    // setter method
    public void setAge(int age) {
        if (age > 0) {        // validation
            this.age = age;
        }
    }

    // getter method
    public int getAge() {
        return age;
    }
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student();

        s.setAge(20);          // set value using method
        System.out.println(s.getAge());  // access using method
    }
}
```
2. Inheritance
Inheritance is the mechanism by which one class acquires the properties and behaviors of another class, allowing code reuse and hierarchical relationships.
```
// Parent class
class Animal {
    String name;

    void eat() {
        System.out.println(name + " is eating.");
    }
}

// Child class inherits from Animal
class Dog extends Animal {
    void bark() {
        System.out.println(name + " is barking.");
    }
}

// Main class to run program
public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.name = "Buddy";

        d.eat();   // inherited method
        d.bark();  // own method
    }
}
```
• Types of inheritance 
a) Single Inheritance

b) Multiple Inheritance

c) Multilevel Inheritance

d) Hierarchical Inheritance

e) Hybrid Inheritance

3. Polymorphism
Polymorphism means one interface or method can be used in different forms, allowing the same function name to perform different tasks depending on context.

Two Types Of Polymorphism

a) Run time Polymorphism  
b) Compile Time Polymorphism  

4. Abstraction
Abstraction is the process of hiding implementation details and showing only essential features, so the user interacts with simple interfaces instead of complex logic.
