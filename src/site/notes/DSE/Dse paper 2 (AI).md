---
{"updated":"2024-12-31T23:16:06.338+05:30","dg-publish":true,"dg-home":false,"tags":["semester-3","dse","python"],"permalink":"/dse/dse-paper-2-ai/","dgPassFrontmatter":true,"created":"2024-12-31T22:48:06.910+05:30"}
---


### Python Programming for Data Handling

---

#### Section A

1. **(a)** *Define a Python list and explain how it is different from a tuple. Provide an example for each.* **(3 marks)**
    - **Answer:**
        
        - A **list** in Python is a mutable, ordered collection of elements that can hold data of any type.  
            **Example:**
            
            ```python
            my_list = [1, 2, 3, "Python", True]
            ```
            
        - A **tuple** in Python is an immutable, ordered collection of elements that also supports heterogeneous data.  
            **Example:**
            
            ```python
            my_tuple = (1, 2, 3, "Python", True)
            ```
            
        
        **Difference:** Lists can be modified (add/remove items), whereas tuples cannot be changed after creation.

---

**(b)** *Write the output of the following code:* **(3 marks)**

```python
x = [2, 4, 6, 8]
y = [10, 20]
z = x + y
print(z)
print(len(z))
```

- **Answer:**  
    Output:
    
    ```plaintext
    [2, 4, 6, 8, 10, 20]
    6
    ```
    

---

**(c)** *Write a Python function that takes a string as input and returns the count of vowels in the string*. **(2 marks)**

- **Answer:**
    
    ```python
    def count_vowels(string):
        vowels = "aeiouAEIOU"
        return sum(1 for char in string if char in vowels)
    
    # Example
    result = count_vowels("Hello World")
    print(result)  # Output: 3
    ```
    

---

**(d)** *Explain the following methods for file operations in Python:* **(6 marks)**  
(i) `write()`

- Writes content to a file. If the file doesn’t exist, it creates one.

(ii) `readlines()`

- Reads all lines of a file and returns them as a list of strings.

(iii) `close()`

- Closes the file to free system resources.

---

**(e)** *Differentiate between the following*: **(6 marks)**  
(i) **while loop and for loop**

- **while loop:** Executes as long as a condition is true. Used when the number of iterations isn’t known.  
    Example:
    
    ```python
    x = 0
    while x < 5:
        print(x)
        x += 1
    ```
    
- **for loop:** Iterates over a sequence.  
    Example:
    
    ```python
    for x in range(5):
        print(x)
    ```
    

(ii) **pack() and grid() layout managers in Tkinter**

- **pack():** Automatically organizes widgets in a block.
- **grid():** Places widgets in a specified grid layout.

(iii) **and and or logical operators**

- **and:** Returns `True` if both conditions are true.
- **or:** Returns `True` if at least one condition is true.

---

**(f)** Evaluate the following expressions: **(4 marks)**  
(i) `pow(2, 3)`

- **Answer:** `8`  
    (ii) `len("Data Handling")`
- **Answer:** `13`  
    (iii) `5 ** 2 // 3`
- **Answer:** `8`  
    (iv) `25 % 7 + 3`
- **Answer:** `7`

---

**(g)** *Discuss the purpose of the `Button` widget in Tkinter. Briefly explain how to assign a callback function to it.* **(4 marks)**

- **Answer:**
    - A `Button` widget in Tkinter is used to perform actions when clicked.
    - To assign a callback:
        
        ```python
        from tkinter import Tk, Button
        
        def on_click():
            print("Button clicked!")
        
        root = Tk()
        btn = Button(root, text="Click Me", command=on_click)
        btn.pack()
        root.mainloop()
        ```
        

---

#### Section B

2. **(a)** *Identify all the widgets used in the code below. Modify the code to include a `Clear` button.* **(3 marks)**

- **Answer:**  
    Widgets: `Label`, `Entry`, and `Button`.  
    Code with `Clear` button:
    
    ```python
    from tkinter import Tk, Label, Entry, Button
    
    def clear_fields():
        username.delete(0, 'end')
        password.delete(0, 'end')
    
    root = Tk()
    Label(root, text="Username").grid(row=0)
    Label(root, text="Password").grid(row=1)
    username = Entry(root)
    password = Entry(root, show="*")
    username.grid(row=0, column=1)
    password.grid(row=1, column=1)
    Button(root, text="Submit").grid(row=2, column=0)
    Button(root, text="Clear", command=clear_fields).grid(row=2, column=1)
    root.mainloop()
    ```
    

---

**(b)** *Write a callback function `on_submit` for the `Submit` button to check for non-empty fields.* **(5 marks)**

- **Answer:**
    
    ```python
    def on_submit():
        if username.get() and password.get():
            print("Login Successful!")
        else:
            print("Error: All fields must be filled!")
    ```
    

---

**(c)** *Explain the difference between `Entry` and `Label` widgets in Tkinter.* **(2 marks)**

- **Answer:**
    - **Entry:** Used to accept user input.
    - **Label:** Used to display static text.
---

3. **(a)** *Explain the concept of "widget hierarchy" in Tkinter. Discuss how parent and child relationships work among widgets*. **(3 marks)**

- **Answer:**
    - **Widget hierarchy:** Refers to the organization of widgets in a parent-child relationship.
    - Widgets are placed inside containers (e.g., `Tk` or `Frame`), with the container being the parent and widgets within it being children.
    - For example:
        
        ```python
        import tkinter as tk
        root = tk.Tk()
        frame = tk.Frame(root)
        label = tk.Label(frame, text="Child Widget")
        frame.pack()
        label.pack()
        root.mainloop()
        ```
        
        Here, `label` is a child of `frame`, and `frame` is a child of `root`.

---

**(b)** *Given the following program, identify the error and suggest a correction*: **(5 marks)**

```python
import tkinter as tk  
window = tk.Tk()  
btn = tk.Button(window, text="Click Me!")  
btn.pack()  
btn.grid(row=0, column=0)  
window.mainloop()  
```

- **Answer:**
    
    - **Error:** You cannot use both `pack()` and `grid()` on the same widget.
    - **Correction:** Use only one geometry manager. Replace `btn.grid()` with `btn.pack()` or vice versa.  
        Corrected code:
    
    ```python
    import tkinter as tk
    window = tk.Tk()
    btn = tk.Button(window, text="Click Me!")
    btn.grid(row=0, column=0)
    window.mainloop()
    ```
    

---

**(c)** *Write Python code to create a form using Tkinter that takes the user’s name and age as input and displays it in a `Label` when a `Submit` button is clicked.* **(5 marks)**

- **Answer:**
    
    ```python
    import tkinter as tk
    
    def display_data():
        name = name_entry.get()
        age = age_entry.get()
        result_label.config(text=f"Name: {name}, Age: {age}")
    
    root = tk.Tk()
    tk.Label(root, text="Name").grid(row=0)
    tk.Label(root, text="Age").grid(row=1)
    
    name_entry = tk.Entry(root)
    age_entry = tk.Entry(root)
    name_entry.grid(row=0, column=1)
    age_entry.grid(row=1, column=1)
    
    submit_btn = tk.Button(root, text="Submit", command=display_data)
    submit_btn.grid(row=2, columnspan=2)
    
    result_label = tk.Label(root)
    result_label.grid(row=3, columnspan=2)
    
    root.mainloop()
    ```
    

---

4. **(a)** *Rewrite the following if-else block as a single conditional expression:* **(3 marks)**

```python
if x > 5:  
    result = "Greater"  
else:  
    result = "Smaller or Equal"  
```

- **Answer:**
    
    ```python
    result = "Greater" if x > 5 else "Smaller or Equal"
    ```
    

---

**(b)** *Write a Python program to read data from a file and count the number of lines, words, and characters in it*. **(5 marks)**

- **Answer:**
    
    ```python
    def file_stats(filename):
        with open(filename, "r") as file:
            content = file.read()
            lines = content.splitlines()
            words = content.split()
            characters = len(content)
            print(f"Lines: {len(lines)}")
            print(f"Words: {len(words)}")
            print(f"Characters: {characters}")
    
    # Example usage
    file_stats("example.txt")
    ```
    

---

**(c)** *What is the difference between mutable and immutable objects in Python? Provide an example for each*. **(2 marks)**

- **Answer:**
    - **Mutable objects:** Can be modified after creation.  
        Example:
        
        ```python
        my_list = [1, 2, 3]
        my_list.append(4)
        print(my_list)  # Output: [1, 2, 3, 4]
        ```
        
    - **Immutable objects:** Cannot be modified after creation.  
        Example:
        
        ```python
        my_tuple = (1, 2, 3)
        # my_tuple[0] = 4  # This will raise an error
        ```
        

---

5. **(a)** *Write a Python function that takes a number as input and prints its multiplication table up to 10.* **(5 marks)**

- **Answer:**
    
    ```python
    def multiplication_table(n):
        for i in range(1, 11):
            print(f"{n} x {i} = {n * i}")
    
    # Example
    multiplication_table(5)
    ```
    

---

**(b)** *Differentiate between `isupper()` and `upper()` methods of a string with examples.* **(3 marks)**

- **Answer:**
    - **`isupper()`:** Checks if all characters in the string are uppercase. Returns `True` or `False`.  
        Example:
        
        ```python
        print("HELLO".isupper())  # Output: True
        print("Hello".isupper())  # Output: False
        ```
        
    - **`upper()`:** Converts all characters in a string to uppercase.  
        Example:
        
        ```python
        print("hello".upper())  # Output: HELLO
        ```
        

---

**(c)** *Write Python code to create a file `example.txt`, write some text into it, and append additional content later.* **(5 marks)**

- **Answer:**
    
    ```python
    # Write initial content
    with open("example.txt", "w") as file:
        file.write("This is the initial content.\n")
    
    # Append more content
    with open("example.txt", "a") as file:
        file.write("This is appended content.\n")
    ```
    

---

6. **(a)** *Consider the following Python function:* **(3 marks)**

```python
def calculate(a, b=5, c=10):  
    return a + b * c
```

Predict the output for the following calls:  
(i) `calculate(1)`

- **Answer:** `1 + 5 * 10 = 51`

(ii) `calculate(2, 3)`

- **Answer:** `2 + 3 * 10 = 32`

(iii) `calculate(4, c=3)`

- **Answer:** `4 + 5 * 3 = 19`

---

**(b)** *What will the following code produce? Identify errors, if any.* **(5 marks)**

```python
lst = [1, 2, 3]  
print(lst[3])  
print(lst.pop(0))  
```

- **Answer:**
    - **Error:** `lst[3]` will raise an `IndexError` because the index is out of range.
    - Correct code:
        
        ```python
        lst = [1, 2, 3]
        print(lst.pop(0))  # Output: 1
        ```
        

---

6. **(c)** *Write short notes on the following:* **(5 marks)**  
    (i) **`zip()` function**

- **Answer:**
    - The `zip()` function combines two or more iterables (like lists or tuples) element-wise into a single iterable of tuples.
    - Example:
        
        ```python
        list1 = [1, 2, 3]
        list2 = ['a', 'b', 'c']
        zipped = zip(list1, list2)
        print(list(zipped))  # Output: [(1, 'a'), (2, 'b'), (3, 'c')]
        ```
        

(ii) **`enumerate()` function**

- **Answer:**
    - The `enumerate()` function adds a counter to an iterable, returning pairs of index and value.
    - Example:
        
        ```python
        items = ['apple', 'banana', 'cherry']
        for index, value in enumerate(items):
            print(index, value)
        # Output:
        # 0 apple
        # 1 banana
        # 2 cherry
        ```
        

(iii) **`os` module in Python**

- **Answer:**
    - The `os` module provides functions to interact with the operating system, such as file handling, directory management, and environment variables.
    - Example:
        
        ```python
        import os
        print(os.getcwd())  # Prints the current working directory
        os.mkdir("new_folder")  # Creates a new folder
        ```
        

---

7. **(a)** *Write a Python program to copy contents from one file to another, but only include lines that do not start with a hash* (`#`). **(5 marks)**

- **Answer:**
    
    ```python
    with open("input.txt", "r") as infile, open("output.txt", "w") as outfile:
        for line in infile:
            if not line.startswith("#"):
                outfile.write(line)
    ```
    
    Example:  
    If `input.txt` contains:
    
    ```
    # This is a comment
    Line 1
    # Another comment
    Line 2
    ```
    
    The resulting `output.txt` will contain:
    
    ```
    Line 1
    Line 2
    ```
    

---

**(b)** *What will the following code snippet output?* **(5 marks)**

```python
with open("test.txt", "w") as f:  
    f.write("Python\nProgramming\nLanguage")  
with open("test.txt", "r+") as f:  
    print(f.read(6))  
    f.seek(0)  
    f.write("Learn")  
    f.seek(0)  
    print(f.read())  
```

- **Answer:**
    
    - After `f.read(6)`: The first 6 characters, `Python`, are read and printed.
    - After `f.write("Learn")`: The first 5 characters of the file are replaced by `Learn`.
    - After the final `f.read()`, the file content is: `Learn\nProgramming\nLanguage`.  
        Output:
    
    ```
    Python
    Learn
    Programming
    Language
    ```
    

---

**(c)** *Explain the purpose of the following file handling modes*: **(3 marks)**  
(i) **`w`**

- Opens a file for writing. If the file exists, it truncates its content; if not, it creates a new file.

(ii) **`a`**

- Opens a file for appending. Writes are added to the end of the file without modifying existing content.

(iii) **`r+`**

- Opens a file for both reading and writing. The file pointer is positioned at the beginning.

---
