---
{"updated":"2025-01-01T22:57:29.017+05:30","dg-publish":true,"dg-home":false,"tags":["semester-3","dse","python"],"permalink":"/dse/dse-paper-1/","dgPassFrontmatter":true,"created":"2024-12-30T19:31:06.109+05:30"}
---




---

# Python Programming for Data Handling Questions and Answers


---

# Section A

#### Question 1

##### (a) What is a dictionary in Python? Explain using an example. (3 marks)

A dictionary in Python is an unordered collection of items. Each item in a dictionary is a key-value pair, where keys are unique and immutable, and values can be of any type.

Example:

##### Creating a dictionary
```python
student = {'name': 'John', 'age': 21, 'grade': 'A'}
print(student['name']) 
# Output: John
```
---

##### (b) Analyze the output of the following code:

1. 
```python

n = [1,2,3,4,5,6,7,8,9,10]
r = 0
for i in range(0, 10):
    if (n[i] % 2 == 0):
        r += n[i]
print(r)
```

Answer:
The code calculates the sum of all even numbers in the list `n`.
Output: 30
This is because the even numbers in `n` are 2, 4, 6, 8, 10, and their sum is 30.

---
2. 
```python
gv = 10

def func():

    lv = 20
    gv = 30
    print(gv)
    print(lv)
func()
print(gv)
```

Answer:
Code Behavior
- Global variable gv is initialized with 10.
- Inside the function func():

    - A local variable lv is assigned 20.
    - A new local variable gv (not the global gv) is assigned 30.
    - print(gv) refers to the local gv, so it prints 30.
    print(lv) prints 20 (local variable lv).

- After calling func(), the global gv is printed again, which remains 10 because the gv inside func() does not affect the global gv.

Expected Output
```
30
20
10
```

---

##### (c) Write a function in Python to find the sum and maximum of three integers. (2 marks)

Answer:
```python

def sum_and_max(a, b, c):
    total = a + b + c
    maximum = max(a, b, c)
    return total, maximum
```


#### Example usage:
print(sum_and_max(10, 20, 30))  # Output: (60, 30)


---

#### (d) Explain the following functions of files in Python: (6 marks)

**f.seek()**: Moves the file cursor to a specified position.

**f.tell()**: Returns the current position of the file cursor.

**f.readline()**: Reads a single line from the file.


Example Usage:
```python
file = open('example.txt', 'r+')
file.seek(5)
print(file.tell()) 
# Output: 5
print(file.readline())  
# Reads the next line
file.close()
```

---

#### (e) Differentiate between the following: (6 marks)

###### 1. startswith() and endswith():

**startswith()**: Checks if a string starts with a specified prefix.

**endswith()**: Checks if a string ends with a specified suffix.



###### 2. break and continue:

**break**: Exits the nearest enclosing loop entirely.

**continue**: Skips the current iteration and moves to the next iteration of the loop.



###### 3. Radiobutton and Checkbutton in Tkinter:

**Radiobutton**: Allows the user to select one option from a group.

**Checkbutton**: Allows the user to select multiple options independently.





---
##### (f) Evaluate the following expressions: (4 marks)

 1. abs(-5.4): 5.4


2. math.floor(25.7): 25


3. x = 2 + 9 * ((3 * 12) - 8) / 10: 32.6


4. 5 % 10 + 10 - 25 * 8 // 5: -30




---

##### (g) What is the use of a layout manager in Tkinter? Briefly discuss the ‘grid’ layout manager and the purpose of ‘row’ and ‘column’ parameters. (4 marks)

Answer:
A layout manager in Tkinter is used to organize widgets within a window. The grid layout manager arranges widgets in a table-like structure using row and column parameters.

row: Specifies the row number.

column: Specifies the column number.


Example:
```Python
import tkinter as tk
root = tk.Tk()
tk.Label(root, text="Name").grid(row=0, column=0)
tk.Entry(root).grid(row=0, column=1)
root.mainloop()
```



---

# Section B

#### Question 2

##### (a) Identify all the Tkinter Control Variables in the code below. Write Python code for adding a ‘Save’ button. (3 marks)

Answer:
The Tkinter Control Variables in the code are:

name_var (instance of tk.StringVar)

rollno_var (instance of tk.IntVar)

```python
import tkinter as tk
root = tk.Tk()

# Name of the Student

name_var = tk.StringVar(root)
name_inp = tk.Entry(root, textvariable=name_var)
name_inp.pack()

# Roll Number of the Student

rollno_var = tk.IntVar(root)
rollno_inp = tk.Entry(root, textvariable=rollno_var)
rollno_inp.pack()
```

Python code for adding a Save button:

##### Save Button
```python 
save_button = tk.Button(root, text="Save")
save_button.pack()

root.mainloop()
```



---

#### (b) Write a callback function on_save for the ‘Save’ button that performs the following tasks:

 - (i) Collect name and rollno from the form using get and store them in a Python dictionary object. (5 marks)

Answer:
```python

def on_save():
    student_data = {
        "Name":
        name_var.get(),
        "Roll No":
        rollno_var.get()
    }
    print(student_data)  
    # Example output
```

- (ii) Using the CSV DictWriter class, write the student’s record (Name, Roll No) collected in a dictionary object to a file students.csv. Create a new file if it doesn’t exist. Also, write a header in the students.csv file using the dictionary keys. (5 marks)

Answer:

import csv

``` python

def on_save():
    student_data = {
        "Name": 
        name_var.get(),
        "Roll No": 
        rollno_var.get()
    }
    with open('students.csv',
    mode='a',newline='') as 
    file:
        writer = 
        csv.DictWriter(file, 
        fieldnames=["Name", 
        "Roll No"])
        if file.tell() == 0:         # Check if the file is empty     
    writer.writeheader()
    writer.writerow
    (student_data)
    
    
    print("Data saved to   
    students.csv")
```


---

#### Question 3

##### (a) What is the widget hierarchy? Identify the different widgets and their child widgets in the code above. (5 marks)

Answer:
Widget hierarchy represents the parent-child relationship between widgets in a Tkinter GUI. In the provided code:

window: Root widget (parent of all widgets).

myform: Child of window.

Label and Entry: Children of myform.


Example Code:
```python

import tkinter as tk
window = tk.Tk()
myform = tk.Frame(window)
myform.grid()
tk.Label(myform, text="Welcome").pack()
tk.Entry(myform, text="Enter some Text").pack()
window.mainloop()
```

---

##### (b) Draw the graphical user interface created by the program. (5 marks)

Answer:
Below is a graphical representation of the layout:
```text
+------------------+
|  Welcome         |
| [Enter some Text]|
+------------------+

```



---

#### Question 3 (Continued)

##### (b) Choose the best option: (5 marks)

(i)
```python

def fl():
    x = 15
    print(x)
x = 12
fl()
```

Answer: The output is 15 because x inside the function is a local variable.
Correct option: (c) 15


---

(ii)
```python

x = [i for i in range(3)]
for i in x:
    print(i)

```
Answer: The output is 0 1 2. The list comprehension creates [0, 1, 2], and the loop iterates over it.
Correct option: (a) 012


---

(iii)

`math.ceil(54.6)`

Answer: The output is 55 because ceil rounds up the number to the nearest integer.
Correct option: (c) 55


---

(iv)

``5 % 10 + 10 < 50 and 29 >= 29``

Answer: The output is True. The expression evaluates step-by-step, and both conditions hold.
Correct option: (a) True


---

(v)

```python
T = 0
count = 20
while count > 5:
    print(T)
    T += count
    count -= 1
```
Answer: The output is 190. The loop sums values from 20 to 6.
Correct option: (b) 190



---

#### Question 4

##### (a) Write an assignment statement using a single conditional expression for the following if-else code: (5 marks)

Given Code:
```python
if marks >= 70:
    remarks = 'good'
else:
    remarks = 'average'
```
Answer:

`remarks = 'good' if marks >= 70 else 'average'`


---

##### (b) What is the difference between a mutable data type and an immutable data type? Explain with examples. (5 marks)

Answer:

Mutable Data Types: Can be modified after creation.

```python

Example: Lists
lst = [1, 2, 3]
lst.append(4)  # Modifies the list
print(lst)  # Output: [1, 2, 3, 4]

Immutable Data Types: Cannot be modified after creation.
Example: Strings

text = "hello"
text[0] = "H"  # Raises an error
```

---

##### (c) Write a Python program to print the following pattern: (5 marks)

Pattern:
```
1
12
123
1234
12345
```
Answer:
```python
for i in range(1, 6):
    print("".join(str(x) for x in range(1, i+1)))

```
Output:
```
1
12
123
1234
12345
```


Continuing with Question 5:


---

#### Question 5

##### (a) Determine the output or indicate an error for the following code: (5 marks)
```
Msg = "Happy New Year 2024 !!"
```

Answer 
```python
Q1.print(Msg.lower())       # Output: happy new year 2024 !!
Q2.print(Msg[ : :2])          # Output: HpyNwYr22 !
Q3.print(Msg[-4:-11])       # Output: (empty string, incorrect slicing)
Q4.print(Msg.index('n'))    # Output: 8 (position of 'n')
Q5.print(Msg.partition('/'))
# Output: ('Happy New Year 2024 !!', '', '')
```


##### (b) Differentiate between the following: (5 marks)

(i) append() and extend():

**append()**: Adds a single element to the end of a list.
```python
lst = [1, 2]
lst.append(3)
print(lst)  
# Output: [1, 2, 3]
```
**extend()**: Adds elements from another iterable to the list.

```python
lst = [1, 2]
lst.extend([3, 4])
print(lst)  # Output: [1, 2, 3, 4]
```


---

(ii) x = 10 and x == 10:

**x=10**: An assignment statement, assigning the value 10 to the variable x.

**x==10**: A comparison statement, checking if the value of x is equal to 10.



---

##### (c) Write a Python function to return the sum of the digits of a number passed as an argument. (5 marks)

Answer:
```python

def sum_of_digits(number):
    return sum(int(digit) for digit in str(abs(number)))
```

##### Example usage
`print(sum_of_digits(1234))`
`# Output: 10` 


Explanation: The function converts the number to a string, iterates through its digits, and calculates the sum. It handles negative numbers using abs().


Continuing with Question 6:


---

#### Question 6

##### (a) Consider the following function:
```python

def nfunc(a=0, num=1):
    return a * num
```
Give the output produced for each of the following function calls: (5 marks)

(i) **nfunc(5)**
Answer:
5 * 1 = 5
Output: 5


---

(ii) **nfunc(5, 6)**
Answer:
5 * 6 = 30
Output: 30


---

(iii) **nfunc(num=7)**
Answer:
0 * 7 = 0
Output: 0


---

(iv) **nfunc(num=6, a=5)**
Answer:
5 * 6 = 30
Output: 30


---

(v) **nfunc(5, num=6)**
Answer:
5 * 6 = 30
Output: 30


---

##### (b) Identify the error, if any, in the following code segments: (5 marks)

(i)

**SET**
```python
grade = ("A+", "A", "A-")
gradel = grade + {1}
print(gradel)
print(grade[2:])
```
Answer:
The code raises a TypeError because sets ({}) cannot be concatenated with tuples.
Error: TypeError: can only concatenate tuple (not "set") to tuple


---

(ii)

**FUNCTION**
```python
def example(a):
    a = a + '2'
    a = a * 2
    return a
example("hello")
```

Answer:
No error. The function returns the string 'hello2hello2'.


---

(iii)

**TUPLE**
```python
t = ([40, 50], "Ram", [40, 30])
t[0][1] = "Ram"
print(t)
```
Answer:
No error. Tuples are immutable, but their mutable elements (like lists) can be modified. The output is:

``([40, "Ram"], "Ram", [40, 30])``


---

(iv)
```python
for a in range(7, 20):
    if (a = 6):
        print("EXITING")
        continue
    print(a)
```
Answer:
The code contains a syntax error because = is an assignment operator, not a comparison operator.
Error: SyntaxError: invalid syntax


---

(v)
```python
print(*%5d', % 12345)
```


Answer:
The code contains a syntax error because of improper string formatting.
Error: SyntaxError: invalid syntax


---

##### (c) Write a short note on: (5 marks)

- (i) map and reduce operations:

**map**: Applies a function to all elements in an iterable.
Example:
```python
nums = [1, 2, 3]
squared = list(map(lambda x: x ** 2, nums))
print(squared)  
# Output: [1, 4, 9]
```
**reduce**: Reduces an iterable to a single value using a function.
Example:
```python
from functools import reduce
nums = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, nums)
print(product)  
# Output: 24
```


---

- (ii) islower, lower, and istitle functions of strings:

**islower**: Returns True if all characters in the string are lowercase.

**lower**: Converts all characters in the string to lowercase.

**istitle**: Returns True if the string follows title case (each word starts with an uppercase letter).


Example:

```python
text = "Hello World"
print(text.islower())  
# Output: False
print(text.lower())    
# Output: "hello world"
print(text.istitle())  
# Output: True

```

Continuing with Question 7:


---

#### Question 7

##### (a) Write a Python program to perform the following operations: (5 marks)

1. Create a file file1.txt and write the following text in it:
   "Python is a popular language"

2.  Read file1.txt and copy its contents to another file file2.txt.

Answer:

##### Part (i): Writing to file1.txt
```python
with open('file1.txt', 'w') as file1:
    file1.write("Python is a popular language")
```

##### Part (ii): Reading from file1.txt and writing to file2.txt
```python
with open('file1.txt', 'r') as file1:
    content = file1.read()

with open('file2.txt', 'w') as file2:
    file2.write(content)

```

---

##### (b) Consider the file vowels.txt containing the line:

**`aeiouAEIOU`**

The file is opened in r+ mode, and the following operations are performed sequentially. What will be the output after each operation? (3 marks)

- (i) **f.write('12345')**
Answer: Appends 12345 at the current cursor position. And it is zero The file contents will be:
12345AEIOU


---

- (ii) **f.read()**
Answer: Reads the remaining contents of the file starting from the current cursor position. If the cursor is at the end after the write, no output is returned.


---

- (iii) **f.seek(0)**
Answer: Moves the cursor to the beginning of the file.


---

- (iv) **f.read(5)**
Answer: Reads the first 5 characters from the file. Output: aeiou


---

- (v) **f.read()**
Answer: Reads the remaining contents of the file from the current cursor position. Output: 12345AEIOU


---

##### (c) What are the following functions used for? (5 marks)

- (i) **eval function**
Evaluates a string as a Python expression.
Example:
```python
x = eval('3 + 5')
print(x)  # Output: 8
```



---

- (ii) **append in lists**
Adds a single element to the end of a list.
Example:
```python
lst = [1, 2]
lst.append(3)
print(lst)  
# Output: [1, 2, 3]
```



---

- (iii) **reverse in lists**
Reverses the elements of a list in place.
Example:
```python
lst = [1, 2, 3]
lst.reverse()
print(lst)  
# Output: [3, 2, 1]

```

---

- (iv) **isalpha in strings**
Returns True if all characters in the string are alphabetic.
Example:
```python
text = "hello"
print(text.isalpha()) 
# Output: True

```

---

- (v) **encode in strings**
Encodes the string into a specified encoding format.
Example:
```python
text = "hello"
encoded = text.encode('utf-8')
print(encoded)
# Output: b'hello'
```

---








