# TP-01: Python Foundations and Clean Coding

## Objective

Review core Python concepts and learn to write clear, organized, maintainable code.

---

## Part 1: Basic Concepts

| Concept  | Meaning                             | Example                                  |
|----------|-------------------------------------|------------------------------------------|
| Variable | Stores a value                      | `score = 85`                             |
| Function | Reusable code that performs a task  | `def calculate_sum(a, b): return a + b`  |
| Class    | Blueprint for creating objects      | `class Student: pass`                    |
| Object   | Instance created from a class       | `student1 = Student()`                   |
| Method   | Function defined inside a class     | `def study(self): ...`                   |
| Constant | Value intended not to change        | `MAX_SCORE = 100`                        |
| Module   | One Python file with reusable code  | `calculator.py`                          |
| Package  | Folder of related modules           | `data_tools/` with `__init__.py`         |

```python
class Student:
    def study(self):
        print("The student is studying.")


student1 = Student()
student1.study()
```

Structure: Package → Module → Class → Method. Python does not enforce constants, so uppercase names signal "do not modify".

---

## Part 2: Clean Code Principles

| Principle       | Meaning                     | Example                          |
|-----------------|-----------------------------|----------------------------------|
| Readability     | Easy to understand          | Meaningful variable names        |
| Maintainability | Easy to update              | Put repeated logic in functions  |
| Efficiency      | Simple, appropriate solution| Use `sum(numbers)` over a loop   |
| Error handling  | Manage problems safely      | Use `try` / `except`             |

```python
# Readable
price = 10
quantity = 3
total_price = price * quantity

# Error handling
try:
    age = int(input("Enter your age: "))
except ValueError:
    print("Please enter a number.")
```

---

## Part 3: PEP 8 Quick Reference

| Item        | Style                                |
|-------------|--------------------------------------|
| Variables   | `snake_case`                         |
| Functions   | `snake_case`                         |
| Classes     | `PascalCase`                         |
| Constants   | `UPPERCASE`                          |
| Indentation | 4 spaces                             |
| Operators   | Spaces around them (`a = b * c`)     |
| Commas      | Space after each (`[1, 2, 3]`)       |
| Imports     | Near the top of the file             |
| Long lines  | Break into readable lines            |
| Blank lines | Separate functions                   |
| Comments    | Explain why, not what                |

Before and after:

```python
# Before
def Calc(a,b):
 return a+b


# After
def calculate_sum(a, b):
    return a + b
```

---

## Debugging Process

1. Run the program and read the error.
2. Find the line causing the problem.
3. Check the values involved.
4. Fix one problem at a time, then run again.

```python
student_age = "20"
print(int(student_age) + 5)  # 25; without int() this raises a TypeError
```

---
