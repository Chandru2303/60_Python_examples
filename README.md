# Here are 60 Python examples to help you master the Python language:
Ranging from basics to advanced concepts. These examples cover a variety of topics like syntax, data structures, algorithms, libraries, and more:

### 1. **Hello World**
```python
print("Hello, World!")
```

### 2. **Basic Arithmetic Operations**
```python
a = 5
b = 3
print(a + b, a - b, a * b, a / b)
```

### 3. **Variables and Data Types**
```python
name = "Alice"
age = 25
height = 5.7
is_student = True
print(name, age, height, is_student)
```

### 4. **Lists**
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits)
```

### 5. **Tuples**
```python
coordinates = (4, 5)
print(coordinates[0], coordinates[1])
```

### 6. **Dictionaries**
```python
person = {"name": "Bob", "age": 30, "city": "New York"}
print(person["name"])
```

### 7. **Sets**
```python
numbers = {1, 2, 3, 3, 4}
numbers.add(5)
print(numbers)
```

### 8. **If-Else Statements**
```python
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is less than or equal to 5")
```

### 9. **For Loop**
```python
for i in range(5):
    print(i)
```

### 10. **While Loop**
```python
i = 0
while i < 5:
    print(i)
    i += 1
```

### 11. **Functions**
```python
def greet(name):
    return f"Hello, {name}!"
print(greet("Alice"))
```

### 12. **Lambda Functions**
```python
square = lambda x: x ** 2
print(square(5))
```

### 13. **List Comprehensions**
```python
squares = [x**2 for x in range(5)]
print(squares)
```

### 14. **String Manipulation**
```python
text = "hello"
print(text.upper(), text.lower(), text.replace("e", "a"))
```

### 15. **Handling Exceptions**
```python
try:
    x = 5 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### 16. **Reading from Files**
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

### 17. **Writing to Files**
```python
with open("example.txt", "w") as file:
    file.write("Hello, world!")
```

### 18. **Class and Objects**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 30)
print(person1.name, person1.age)
```

### 19. **Inheritance**
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):
        print("Woof!")

dog = Dog()
dog.speak()
```

### 20. **Polymorphism**
```python
class Cat:
    def speak(self):
        print("Meow")

animals = [Dog(), Cat()]
for animal in animals:
    animal.speak()
```

### 21. **Encapsulation**
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())
```

### 22. **Abstract Base Class**
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius ** 2

circle = Circle(5)
print(circle.area())
```

### 23. **Generators**
```python
def countdown(n):
    while n > 0:
        yield n
        n -= 1

for number in countdown(5):
    print(number)
```

### 24. **Iterators**
```python
class Reverse:
    def __init__(self, data):
        self.data = data
        self.index = len(data)

    def __iter__(self):
        return self

    def __next__(self):
        if self.index == 0:
            raise StopIteration
        self.index = self.index - 1
        return self.data[self.index]

rev = Reverse("giraffe")
for char in rev:
    print(char)
```

### 25. **Sorting Lists**
```python
numbers = [5, 3, 8, 6]
numbers.sort()
print(numbers)
```

### 26. **Lambda with Sorting**
```python
pairs = [(1, 2), (3, 1), (5, 4)]
pairs.sort(key=lambda x: x[1])
print(pairs)
```

### 27. **Decorators**
```python
def decorator(func):
    def wrapper():
        print("Before the function call")
        func()
        print("After the function call")
    return wrapper

@decorator
def say_hello():
    print("Hello")

say_hello()
```

### 28. **Counter from Collections**
```python
from collections import Counter
text = "hello world"
counter = Counter(text)
print(counter)
```

### 29. **DefaultDict from Collections**
```python
from collections import defaultdict
d = defaultdict(int)
d["apple"] += 1
print(d)
```

### 30. **NamedTuples**
```python
from collections import namedtuple
Point = namedtuple("Point", ["x", "y"])
p = Point(3, 4)
print(p.x, p.y)
```

### 31. **Deque**
```python
from collections import deque
d = deque([1, 2, 3])
d.append(4)
print(d)
```

### 32. **Queue**
```python
from queue import Queue
q = Queue()
q.put(1)
q.put(2)
print(q.get())
```

### 33. **Priority Queue**
```python
import heapq
pq = []
heapq.heappush(pq, (2, "task2"))
heapq.heappush(pq, (1, "task1"))
print(heapq.heappop(pq))
```

### 34. **Shuffling a List**
```python
import random
cards = [1, 2, 3, 4, 5]
random.shuffle(cards)
print(cards)
```

### 35. **Random Choice**
```python
import random
fruits = ["apple", "banana", "cherry"]
print(random.choice(fruits))
```

### 36. **Random Range**
```python
import random
print(random.randint(1, 100))
```

### 37. **Regular Expressions**
```python
import re
pattern = r"\d+"
text = "There are 100 apples."
result = re.findall(pattern, text)
print(result)
```

### 38. **JSON Parsing**
```python
import json
data = '{"name": "Alice", "age": 25}'
parsed_data = json.loads(data)
print(parsed_data)
```

### 39. **Sending an HTTP Request**
```python
import requests
response = requests.get("https://api.github.com")
print(response.json())
```

### 40. **Using Python Debugger**
```python
import pdb
x = 10
pdb.set_trace()
y = 5
z = x + y
print(z)
```

### 41. **Zip Function**
```python
names = ["Alice", "Bob"]
ages = [25, 30]
zipped = zip(names, ages)
for name, age in zipped:
    print(name, age)
```

### 42. **Enumerate**
```python
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(index, fruit)
```

### 43. **Map**
```python
def square(x):
    return x * x

numbers = [1, 2, 3, 4]
squared_numbers = map(square, numbers)
print(list(squared_numbers))
```

### 44. **Filter**
```python
def is_even(x):
    return x % 2 == 0

numbers = [1, 2, 3, 4]
even_numbers = filter(is_even, numbers)
print(list(even_numbers))
```

### 45. **Reduce**
```python
from functools import reduce

def multiply(x, y):
    return x * y

numbers = [1, 2, 3, 4]
result = reduce(multiply, numbers)
print(result)
```

### 46. **Set Operations**
```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a.union(b))
print(a.intersection(b))
print(a.difference(b))
```

### 47. **Matrix Operations with Numpy**
```python
import numpy as np
matrix = np.array([[1, 2], [3, 4]])
print(np.transpose(matrix))
```

### 48. **Pandas DataFrame**
```python
import pandas as pd
data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
df = pd.DataFrame(data)
print(df)
```

### 49. **Plotting with Matplotlib**
```python
import matplotlib.pyplot as plt
x = [1, 2, 3, 4]
y = [1, 4, 9, 16]
plt.plot(x, y)
plt.show()
```

### 50. **Date and Time**
```python
import datetime
now = datetime.datetime.now()
print(now)
```

### 51. **Time Measurement**
```python
import time
start = time.time()
time.sleep(2)
end = time.time()
print(f"Elapsed time: {end - start} seconds")
```

### 52. **Reading CSV File**
```python
import csv
with open('file.csv', mode='r') as file:
    csv_reader = csv.reader(file)
    for row in csv_reader:
        print(row)
```

### 53. **Writing to CSV File**
```python
import csv
data = [["Name", "Age"], ["Alice", 25], ["Bob", 30]]
with open('file.csv', mode='w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

### 54. **Context Managers**
```python
with open('file.txt', 'w') as file:
    file.write("Hello, world!")
```

### 55. **Multithreading**
```python
import threading
def print_numbers():
    for i in range(5):
        print(i)
        
thread = threading.Thread(target=print_numbers)
thread.start()
thread.join()
```

### 56. **Multiprocessing**
```python
import multiprocessing
def print_numbers():
    for i in range(5):
        print(i)

process = multiprocessing.Process(target=print_numbers)
process.start()
process.join()
```

### 57. **Web Scraping with BeautifulSoup**
```python
from bs4 import BeautifulSoup
import requests

url = "https://example.com"
response = requests.get(url)
soup = BeautifulSoup(response.content, "html.parser")
print(soup.prettify())
```

### 58. **Sending an Email with SMTP**
```python
import smtplib
from email.mime.text import MIMEText

msg = MIMEText("Hello, this is a test email.")
msg['Subject'] = 'Test Email'
msg['From'] = 'youremail@example.com'
msg['To'] = 'recipient@example.com'

with smtplib.SMTP('smtp.gmail.com', 587) as server:
    server.starttls()
    server.login("youremail@example.com", "yourpassword")
    server.sendmail(msg['From'], msg['To'], msg.as_string())
```

### 59. **Testing with Unittest**
```python
import unittest

def add(a, b):
    return a + b

class TestMathOperations(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)

if __name__ == "__main__":
    unittest.main()
```

### 60. **Mocking with Unittest**
```python
from unittest.mock import MagicMock
mock = MagicMock(return_value=5)
print(mock())
```

#

# Python If ... Else

## Python Conditions and If Statements

Python supports the usual logical conditions from mathematics:

- Equals: `a == b`
- Not Equals: `a != b`
- Less than: `a < b`
- Less than or equal to: `a <= b`
- Greater than: `a > b`
- Greater than or equal to: `a >= b`

These conditions can be used in several ways, most commonly in "if statements" and loops.

### An "if statement" is written by using the `if` keyword.

### Example 1: If Statement
```python
a = 33
b = 200
if b > a:
  print("b is greater than a")
```
In this example, we use two variables, `a` and `b`, which are used as part of the if statement to test whether `b` is greater than `a`. As `a` is 33, and `b` is 200, we know that 200 is greater than 33, and so we print to screen that "b is greater than a".

## Indentation
Python relies on **indentation** (whitespace at the beginning of a line) to define scope in the code. Other programming languages often use curly-brackets for this purpose.

### Example 2: If Statement Without Indentation (Will Raise an Error)
```python
a = 33
b = 200
if b > a:
print("b is greater than a")  # you will get an error
```

## Elif
The `elif` keyword is Python's way of saying **"if the previous conditions were not true, then try this condition."**

### Example 3: Elif Statement
```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```
In this example, `a` is equal to `b`, so the first condition is not true, but the `elif` condition is true, so we print to screen that "a and b are equal".

## Else
The `else` keyword catches anything which isn't caught by the preceding conditions.

### Example 4: Else Statement
```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```
In this example, `a` is greater than `b`, so the first condition is not true, and also the `elif` condition is not true, so we go to the `else` condition and print to screen that "a is greater than b".

You can also have an `else` without the `elif`:

### Example 5: Else Without Elif
```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

## Short Hand If
If you have only one statement to execute, you can put it on the same line as the `if` statement.

### Example 6: One Line If Statement
```python
if a > b: print("a is greater than b")
```

## Short Hand If ... Else
If you have only one statement to execute, one for `if`, and one for `else`, you can put it all on the same line:

### Example 7: One Line If Else Statement
```python
a = 2
b = 330
print("A") if a > b else print("B")
```
This technique is known as **Ternary Operators**, or **Conditional Expressions**.

You can also have multiple else statements on the same line:

### Example 8: One Line If Else Statement with 3 Conditions
```python
a = 330
b = 330
print("A") if a > b else print("=") if a == b else print("B")
```

## And
The `and` keyword is a logical operator, and is used to combine conditional statements.

### Example 9: And Operator
```python
a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")
```

## Or
The `or` keyword is a logical operator, and is used to combine conditional statements.

### Example 10: Or Operator
```python
a = 200
b = 33
c = 500
if a > b or a > c:
  print("At least one of the conditions is True")
```

## Not
The `not` keyword is a logical operator, and is used to reverse the result of the conditional statement.

### Example 11: Not Operator
```python
a = 33
b = 200
if not a > b:
  print("a is NOT greater than b")
```

## Nested If
You can have `if` statements inside `if` statements, this is called **nested if statements**.

### Example 12: Nested If Statement
```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

## The pass Statement
`if` statements cannot be empty, but if you for some reason have an `if` statement with no content, put in the `pass` statement to avoid getting an error.

### Example 13: Using `pass` Statement
```python
a = 33
b = 200

if b > a:
  pass
```
