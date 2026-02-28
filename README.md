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

**Types**
- Compile-time → Method Overloading  
- Runtime → Method Overriding  

---

#### 4️⃣ Abstraction
Shows only essential features and hides internal implementation details.
