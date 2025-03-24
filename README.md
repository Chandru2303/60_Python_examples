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
