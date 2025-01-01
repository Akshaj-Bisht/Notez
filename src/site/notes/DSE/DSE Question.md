---
{"updated":"2025-01-01T18:50:33.781+05:30","dg-publish":true,"dg-home":false,"tags":["semester-3","dse","python"],"permalink":"/dse/dse-question/","dgPassFrontmatter":true,"created":"2025-01-01T18:45:50.357+05:30"}
---


---

# Python Programming Tasks

### 1. Write a Python program to calculate the factorial of a number.

**Answer:**

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)

# Example usage
number = 5
print(f"The factorial of {number} is {factorial(number)}")
```

This program uses recursion to calculate the factorial of a number. It multiplies the number by the factorial of the number decremented by one until it reaches one.

---

### 2. Write a Python program to generate prime numbers between 1 to n, where n is provided as input by the user.

**Answer:**

```python
def generate_primes(n):
    primes = []
    for num in range(2, n + 1):
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                break
        else:
            primes.append(num)
    return primes

# Example usage
n = 20
print(f"Prime numbers between 1 and {n}: {generate_primes(n)}")
```

This program checks each number between 2 and n for divisors and adds it to the list if no divisors are found.


---

### 3. Write a Python program to find the sum and average of numbers in a given list.

**Answer:**

```python
def sum_and_average(numbers):
    total_sum = sum(numbers)
    average = total_sum / len(numbers) if numbers else 0
    return total_sum, average

# Example usage
numbers = [10, 20, 30, 40]
total, avg = sum_and_average(numbers)
print(f"Sum: {total}, Average: {avg}")
```

This program uses Python's built-in `sum()` function and calculates the average by dividing the sum by the length of the list.

---

### 4. Given two sets, set1 and set2, write a Python program to find their union, intersection, and difference.

**Answer:**

```python
def set_operations(set1, set2):
    union = set1 | set2
    intersection = set1 & set2
    difference = set1 - set2
    return union, intersection, difference

# Example usage
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union, intersection, difference = set_operations(set1, set2)
print(f"Union: {union}, Intersection: {intersection}, Difference: {difference}")
```

This program demonstrates set operations using Python's built-in set methods.

---

### 5. Given a list of numbers, write a Python program to count the number of times an element occurs in a list and create a dictionary with `element: count` as key-value pairs.

**Answer:**

```python
from collections import Counter

def count_elements(numbers):
    return dict(Counter(numbers))

# Example usage
numbers = [1, 2, 2, 3, 3, 3]
element_counts = count_elements(numbers)
print(element_counts)
```

This program uses the `Counter` class from the `collections` module to count occurrences efficiently.

---

### 6. Write a Python program to swap the first two and last two characters in a given string.

**Answer:**

```python
def swap_characters(s):
    if len(s) < 4:
        return "String too short!"
    return s[-2:] + s[2:-2] + s[:2]

# Example usage
string = "abcdef"
print(swap_characters(string))
```

This program handles string manipulation by slicing and swapping the respective segments.

---

### 7. Write a Python program to create a text file having names of ten Indian cities.

**Answer:**

```python
cities = ["Delhi", "Mumbai", "Chennai", "Kolkata", "Bengaluru", 
          "Hyderabad", "Ahmedabad", "Pune", "Jaipur", "Lucknow"]

with open("indian_cities.txt", "w") as file:
    for city in cities:
        file.write(city + "\\n")
```

This program writes the names of Indian cities to a text file named `indian_cities.txt`.

---
### 8. Write a Python program to create a text file having at least five lines about your college using `writelines()` function.

**Answer:**

```python
college_info = [
    "My college is renowned for its academic excellence.\n",
    "It has a beautiful campus with state-of-the-art facilities.\n",
    "The faculty members are highly qualified and supportive.\n",
    "There are various extracurricular activities for students.\n",
    "The placement record of my college is outstanding.\n"
]

with open("college_info.txt", "w") as file:
    file.writelines(college_info)
```

This program uses the `writelines()` method to write multiple lines into a text file named `college_info.txt`.

---

### 9. Write a Python program which reads the data from two input files having Employee Names and merges them into one output file.

**Answer:**

```python
# File names
file1 = "employee_names_1.txt"
file2 = "employee_names_2.txt"
output_file = "merged_employees.txt"

# Reading and merging
with open(file1, "r") as f1, open(file2, "r") as f2, open(output_file, "w") as output:
    output.writelines(f1.readlines())
    output.writelines(f2.readlines())

print(f"Data merged into {output_file}")
```

This program reads the contents of two input files and combines them into a single output file.

---

### 10. Write a Python program to count the number of vowels in a file and write the `vowel: count` in a dictionary.

**Answer:**

```python
def count_vowels(file_path):
    vowels = "aeiouAEIOU"
    counts = {v: 0 for v in vowels}

    with open(file_path, "r") as file:
        text = file.read()
        for char in text:
            if char in vowels:
                counts[char] += 1

    return {v: c for v, c in counts.items() if c > 0}

# Example usage
file_path = "sample_text.txt"
vowel_counts = count_vowels(file_path)
print(vowel_counts)
```

This program reads a file, counts the occurrences of vowels, and stores them in a dictionary.

---

### 11. Write a Python program to create a CSV file having student data: RollNo, Enrollment_No, Name, Course, Semester.

**Answer:**

```python
import csv

# Student data
students = [
    {"RollNo": 1, "Enrollment_No": "A001", "Name": "John Doe", "Course": "B.Tech", "Semester": 5},
    {"RollNo": 2, "Enrollment_No": "A002", "Name": "Jane Smith", "Course": "B.Sc", "Semester": 3},
    {"RollNo": 3, "Enrollment_No": "A003", "Name": "Sam Wilson", "Course": "B.Com", "Semester": 1}
]

# Writing to CSV
with open("students.csv", "w", newline="") as file:
    writer = csv.DictWriter(file, fieldnames=students[0].keys())
    writer.writeheader()
    writer.writerows(students)

print("CSV file 'students.csv' created successfully.")
```

This program writes student data to a CSV file using Python's `csv` module.

---

### 12. Write a Python program to read the CSV file created in the above program and filter out records of II semester students.

**Answer:**

```python
import csv

# Reading and filtering
with open("students.csv", "r") as file:
    reader = csv.DictReader(file)
    filtered_students = [row for row in reader if int(row["Semester"]) == 2]

print("Filtered students:", filtered_students)
```

This program reads the `students.csv` file and filters out students in the second semester.

---

### 13. Write a Python program using tkinter library to create a GUI to enter registration details for an event.

**Answer:**

```python
import tkinter as tk

def submit_details():
    print(f"Name: {name_entry.get()}, Age: {age_entry.get()}, Event: {event_entry.get()}")

# GUI setup
root = tk.Tk()
root.title("Event Registration")

tk.Label(root, text="Name:").grid(row=0)
tk.Label(root, text="Age:").grid(row=1)
tk.Label(root, text="Event:").grid(row=2)

name_entry = tk.Entry(root)
age_entry = tk.Entry(root)
event_entry = tk.Entry(root)

name_entry.grid(row=0, column=1)
age_entry.grid(row=1, column=1)
event_entry.grid(row=2, column=1)

tk.Button(root, text="Submit", command=submit_details).grid(row=3, columnspan=2)

root.mainloop()
```

This program creates a simple GUI for event registration using the `tkinter` library.

---

### 14. Write a Python program using tkinter library to create a calculator to perform addition, subtraction, multiplication, and division of two numbers entered by the user.

**Answer:**

```python
import tkinter as tk

def calculate():
    num1 = float(entry1.get())
    num2 = float(entry2.get())
    operation = operation_entry.get()
    if operation == "+":
        result = num1 + num2
    elif operation == "-":
        result = num1 - num2
    elif operation == "*":
        result = num1 * num2
    elif operation == "/":
        result = num1 / num2
    else:
        result = "Invalid Operation"
    result_label.config(text=f"Result: {result}")

# GUI setup
root = tk.Tk()
root.title("Calculator")

tk.Label(root, text="Enter number 1:").grid(row=0)
entry1 = tk.Entry(root)
entry1.grid(row=0, column=1)

tk.Label(root, text="Enter number 2:").grid(row=1)
entry2 = tk.Entry(root)
entry2.grid(row=1, column=1)

tk.Label(root, text="Enter operation (+, -, *, /):").grid(row=2)
operation_entry = tk.Entry(root)
operation_entry.grid(row=2, column=1)

tk.Button(root, text="Calculate", command=calculate).grid(row=3, columnspan=2)

result_label = tk.Label(root, text="Result: ")
result_label.grid(row=4, columnspan=2)

root.mainloop()
```

This program creates a basic calculator GUI for arithmetic operations.

---
