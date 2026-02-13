# 1. Programming Foundations for Quantum Computing

---

## 1.1 Python Virtual Environment (venv)

### Why do we need a virtual environment?

When we start working on different Python projects, we often run into dependency conflicts. Different projects may require **different versions of the same library**.

For example:

* A quantum simulation project may need **NumPy 1.19**
* A machine learning project may need **NumPy 1.21**

Without virtual environments, this becomes a serious problem because a system can usually have only one active version of a library at a time.

**Virtual environments solve this problem** by creating isolated Python environments for each project. Each environment has its own Python interpreter and its own set of installed libraries.

This allows you to:

* Avoid version conflicts
* Keep projects clean and independent
* Easily reproduce projects on another machine

---

### How to create a virtual environment

Suppose we want to create a project called `my_first_project`.

#### Step 1: Create the virtual environment

```bash
python -m venv my_first_project
```

#### Step 2: Activate the virtual environment

On **Windows**:

```bash
my_first_project\Scripts\activate
```

On **Linux / macOS**:

```bash
source my_first_project/bin/activate
```

Once activated, your terminal will show the environment name.

#### Step 3: Install required packages

```bash
pip install qiskit numpy matplotlib
```

These libraries will be installed **only inside this environment**.

---

### Saving dependencies (requirements.txt)

To keep track of all installed packages and their versions:

```bash
pip freeze > requirements.txt
```

This file allows anyone else (or you in the future) to recreate the same environment using:

```bash
pip install -r requirements.txt
```

---

## Object-Oriented Programming (OOPS) in Python

### What is Object-Oriented Programming?

Object-Oriented Programming (OOP) is a way of organizing code that makes it easier to manage **large and complex systems**.

Instead of writing many unrelated functions, we group related data and behavior together into **objects**.

This is especially useful in **quantum computing**, where concepts naturally form hierarchies:

* Qubits
* Quantum gates
* Circuits
* Algorithms

All of these can be cleanly represented as objects.

---

### Your first class: A Qubit

A **qubit** is the fundamental unit of quantum information. Let’s model it using a Python class.

```python
class Qubit:
    def __init__(self, label):
        self.label = label
        self.state = 0           # starts in |0⟩ state
        
    def flip(self):
        """Apply X gate - flips 0 to 1 or 1 to 0"""
        self.state = 1 - self.state
        
    def show_state(self):
        print(f"Qubit {self.label} is in state |{self.state}⟩")
```

#### Using the Qubit class

```python
q1 = Qubit("alice")
q1.show_state()       # Qubit alice is in state |0⟩

q1.flip()
q1.show_state()       # Qubit alice is in state |1⟩
```

---

### The `__init__` method

* `__init__` is a **constructor**
* It runs automatically when a new object is created
* It initializes the object’s attributes

---

### Inheritance and the `super()` function

Inheritance allows one class to **reuse and extend** another class.

Let’s define a general quantum gate, and then specialize it.

```python
class QuantumGate:
    def __init__(self, name):
        self.name = name
        
    def apply(self, qubit):
        print(f"Applying {self.name} gate to qubit {qubit.label}")
```

Now, we create a specific gate: **Pauli-X**.

```python
class PauliXGate(QuantumGate):
    def __init__(self):
        super().__init__("Pauli-X")
        
    def apply(self, qubit):
        super().apply(qubit)     # Call parent method
        qubit.flip()             # Gate operation
```

* `super()` allows us to call methods from the parent class
* This avoids code duplication and improves clarity

---

### Why OOPS matters for Quantum Computing

Object-Oriented Programming helps us:

* Model quantum systems naturally
* Build scalable simulators and frameworks
* Understand real quantum libraries like **Qiskit** and **PennyLane**

In fact, most quantum frameworks internally rely heavily on OOP concepts.

---

## 1.2 Difference Between Regular and Quantum Programming

| Classical Programming              | Quantum Programming                          |
| ---------------------------------- | -------------------------------------------- |
| Uses **bits** (0 or 1)             | Uses **qubits** (0 and 1 simultaneously)     |
| Executes instructions step by step | Explores many possibilities at once          |
| Uses logic gates (AND, OR, NOT)    | Uses quantum gates (Hadamard, Pauli-X, etc.) |
| Produces a definite output         | Produces probabilistic outcomes              |
| Already very fast for daily tasks  | Useful for extremely complex problems        |

**Analogy:**

* Classical programming → Driving on one road at a time
* Quantum programming → Looking at many roads simultaneously and choosing the best

Quantum advantage appears in problems like **cryptography, optimization, and molecular simulations**.

---

## 1.3 Writing Your First Program

Python is beginner-friendly and widely used in quantum computing.

### Step 1: Choose a Platform

* VS Code
* Jupyter Notebook
* Google Colab (cloud-based)

### Step 2: The Goal

Print the message:

```
Hello World!
```

### Step 3: The Code

```python
print("Hello World!")
```

### Step 4: Output

```
Hello World!
```

🎉 You’ve written your first Python program!

---

## 1.4 Variables

Think of variables as **labeled boxes** where you store values.

### Why Use Variables?

* Avoid repeating values
* Make code flexible
* Easily update information

### Example 1

```python
age = 18
print(age)
```

**Output:** `18`

### Example 2

```python
age = 18
print("Initial age:", age)

age = 19
print("Updated age:", age)
```

### Example 3: Area of Rectangle

```python
length = 5
width = 3
area = length * width
print("Area is:", area)
```

---

## 1.5 Functions and Parameters

Functions are reusable blocks of code designed to perform a task.

### Why Functions?

* Code reuse
* Better organization
* Abstraction

### Glossary

* **Function:** A block of code that performs a task
* **Parameter:** Input to a function
* **Return Value:** Output from a function
* **Scope:** Where a variable is accessible

---

## 1.6 Data Types and Structures

### Primitive Types

* `int`, `float`, `bool`, `string`

### Collections

* Lists
* Dictionaries
* Sets

### Concepts

* **Mutable:** Can be changed
* **Immutable:** Cannot be changed

---

## 1.7 Loops

Loops repeat actions automatically.

### Types

* `for` loop → iterate over items
* `while` loop → repeat while condition is true

### Keywords

* `break`, `continue`, `pass`

---

## 1.8 Lists

* Ordered collection of items
* Can be modified

```python
numbers = [1, 2, 3]
numbers.append(4)
```

### Glossary

* **Index:** Position (starts at 0)
* **Append():** Add item
* **Pop():** Remove last item

---

## 1.9 Tuples

* Like lists, but **immutable**
* Defined using `()`

```python
t = (1, 2, 3)
```

---

## 1.10 Dictionaries

* Store key-value pairs

```python
student = {"name": "Alice", "age": 20}
```

### Useful Methods

* `get()`
* `keys()`
* `values()`
* `items()`

---

## 1.11 Classes and Objects (OOP)

Object-Oriented Programming helps organize complex systems.

### Example: Qubit Class

```python
class Qubit:
    def __init__(self, label):
        self.label = label
        self.state = 0

    def flip(self):
        self.state = 1 - self.state

    def show_state(self):
        print(f"Qubit {self.label} is in state |{self.state}⟩")
```

---

## 1.12 Algorithms & Problem Solving

* Searching
* Sorting
* Greedy algorithms

### Key Concepts

* **Time Complexity (Big O)**
* **Space Complexity**

---

## 1.13 Modularity and Abstraction

* Break code into functions and files
* Hide complexity
* Use modules and packages

---

## 1.14 Debugging and Testing

### Types of Bugs

* Syntax
* Logic
* Runtime

### Tools

* Print statements
* Debuggers
* Assertions

---

## 1.15 Using Libraries and APIs

### Popular Quantum Libraries

* **Qiskit** (IBM)
* **PennyLane** (Xanadu)

```bash
pip install qiskit pennylane
```

---

## 1.16 Projects: Putting It All Together

### Beginner Projects

* Calculator
* To-do list
* Number guessing game

### Next Steps

* Data Structures & Algorithms
* Quantum Circuits
* Variational Algorithms

---

> **Quantum Computing Club – IIT Indore**
