# 📘 Learning Java

A collection of Java practice programs, algorithms, and core concept implementations for mastering fundamentals step-by-step.

---

## 📑 Table of Contents
- [Basic Java Template](#-basic-java-template)
- [Hashing & Hash Tables](#-hashing--hash-tables)
- [Sorting Algorithms](#-sorting-algorithms)
- [Time & Space Complexity](#-time--space-complexity)
- [Searching Algorithms](#-searching-algorithms)
- [Object-Oriented Programming](#-object-oriented-programming)

---

## 💻 Basic Java Template
```java
class Main {
    public static void main(String[] args) {
        System.out.print("Hello World");
    }
}
```

---

## 🔑 Hashing & Hash Tables

**Hashing** maps data (keys) to a fixed-size value using a hash function.  
This value is used as an index for fast data access.

### 📦 Hash Table
Stores **key–value pairs** and provides average **O(1)** time for:
- Insertion
- Deletion
- Lookup

### ⚙️ How It Works
1. Hash function converts key → array index  
2. Value stored at that index  
3. Same hash function used to retrieve it  

### ⚠️ Collisions
Occurs when two keys map to the same index.

**Handling Methods**
- **Chaining** → Store multiple values at same index (list)
- **Open Addressing** → Find another empty slot

### ⭐ Advantages
- Faster access than arrays & linked lists  
- Efficiency depends on hash function quality  

**Used in:**
- Databases
- Caches
- Dictionaries / Maps

---

## 🔄 Sorting Algorithms

Implemented with focus on clarity + fundamentals:

- Selection Sort
- Bubble Sort
- Insertion Sort
- Merge Sort
- Quick Sort

---

## ⏱ Time & Space Complexity

| Algorithm | Best | Average | Worst | Space |
|--------|------|---------|-------|------|
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) |
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) |

---

## 🔎 Searching Algorithms

### Linear Search
```
LinearSearch(A, n, key)
  for i ← 0 to n - 1 do
      if A[i] = key then
          return i
  return -1
```

### Binary Search
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

  return -1
```

---

## 🧠 Object-Oriented Programming

OOP models real-world entities as **objects** containing:

- Properties (data)
- Behaviors (methods)

---

### 🧱 Four Pillars of OOP

#### 1️⃣ Encapsulation
Wraps data + methods into a class and restricts direct access.

```java
class Student {
    private int age;

    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }

    public int getAge() {
        return age;
    }
}
```

---

#### 2️⃣ Inheritance
Allows a class to inherit properties and behaviors from another.

```java
class Animal {
    String name;
    void eat() {
        System.out.println(name + " is eating.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println(name + " is barking.");
    }
}
```

**Types of Inheritance**
- Single  
- Multiple  
- Multilevel  
- Hierarchical  
- Hybrid  

---

#### 3️⃣ Polymorphism
Same method name → different behavior.

```java
// Parent class
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

// Child class 1
class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

// Child class 2
class Cat extends Animal {
    void sound() {
        System.out.println("Cat meows");
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Animal a;

        a = new Dog();  // reference is Animal, object is Dog
        a.sound();

        a = new Cat();  // reference is Animal, object is Cat
        a.sound();
    }
}
```

**Types**
- Compile-time → Method Overloading  
- Runtime → Method Overriding  

---

#### 4️⃣ Abstraction
Shows only essential features and hides internal implementation details.

```java
abstract class Animal {
    // Abstract method (no body)
    abstract void makeSound();
    
    // Regular method
    void sleep() {
        System.out.println("Sleeping...");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.makeSound(); // Output: Woof Woof!
        myDog.sleep();     // Output: Sleeping...
    }
}
```

##  📌 Types of Loops in Java

Java mainly provides three types of loops:
- for loop 
- while loop 
- do-while loop 

#### 1 For Loop Syntax in Java
```java
for (initialization; condition; update) {
    // code to run each loop
}
```

#### 2 While Loop Syntax in Java
```java
while (condition) {
    // code to execute repeatedly
}
```

#### 3 Do While Loop Syntax in Java
```java
do {
    // code to be executed
} while (condition);
```

## For - Each Loop 
the for-each loop (also called the enhanced for loop) is used to iterate through arrays or collections easily without using an index.

```java
for (datatype variable : arrayOrCollection) {
    // code to execute
}
```

## Java Collection Frame Works
The Java Collections Framework (JCF) is a set of classes and interfaces in Java that help you store, manage, and manipulate groups of objects efficiently. It is part of the Java standard library (java.util package).

Instead of writing your own data structures, Java provides ready-made structures like lists, sets, queues, and maps.

#### The main interfaces in the Collection Framework are:

#### Collection

- List : List is an interface in the Java Collection Framework that represents an ordered collection of elements where duplicates are allowed and elements can be accessed using an index.

- Set : A Set is a collection that does not allow duplicate elements and typically does not guarantee insertion order (depending on the implementation).

- Queue : A Queue in the Java Collections Framework is an interface that represents a collection of elements designed to be processed in a First-In-First-Out (FIFO) order, where elements are inserted at the rear and removed from the front.

- Map (separate interface for key-value storage) : There are map used to store data in Java! A map is an object that stores elements in key-value pairs, where each key is unique and is used to access its corresponding value.
* HashMap
```java
import java.util.HashMap;

public class Example {
    public static void main(String[] args) {
        HashMap<String, String> map = new HashMap<>();

        map.put("1", "Apple");
        map.put("2", "Banana");
        map.put("3", "Mango");

        System.out.println(map.get("2"));  // Banana

        for (String key : map.keySet()) {
            System.out.println(key + " -> " + map.get(key));
        }
    }
}
```
* LinkedHashMap
* TreeMap
* HashTable
* ConcurrentHashMap

