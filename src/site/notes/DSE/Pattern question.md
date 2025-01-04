---
{"updated":"2025-01-01T20:28:01.825+05:30","dg-publish":true,"dg-home":false,"tags":["semester-3","dse","python"],"permalink":"/dse/pattern-question/","dgPassFrontmatter":true,"created":"2025-01-01T20:23:00.529+05:30"}
---


# Python Pattern Questions and Answers

## 1. Right-Angled Triangle Pattern

### Question:
Print the following pattern for `n = 5`:
```

*
**
***
****
*****

````

### Answer:
```python
n = 5
for i in range(1, n + 1):
    print("*" * i)
````

---

## 2. Inverted Right-Angled Triangle Pattern

### Question:

Print the following pattern for `n = 5`:

```
*****
****
***
**
*
```

### Answer:

```python
n = 5
for i in range(n, 0, -1):
    print("*" * i)
```

---

## 3. Pyramid Pattern

### Question:

Print the following pattern for `n = 5`:

```
    *
   ***
  *****
 *******
*********
```

### Answer:

```python
n = 5
for i in range(1, n + 1):
    print(" " * (n - i) + "*" * (2 * i - 1))
```

---

## 4. Diamond Pattern

### Question:

Print the following pattern for `n = 5`:

```
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
```

### Answer:

```python
n = 5
for i in range(1, n + 1):
    print(" " * (n - i) + "*" * (2 * i - 1))
for i in range(n - 1, 0, -1):
    print(" " * (n - i) + "*" * (2 * i - 1))
```

---

## 5. Number Triangle Pattern

### Question:

Print the following pattern for `n = 5`:

```
1
12
123
1234
12345
```

### Answer:

```python
n = 5
for i in range(1, n + 1):
    for j in range(1, i + 1):
        print(j, end="")
    print()
```

---

## 6. Pascal's Triangle Pattern

### Question:

Print Pascal's Triangle for `n = 5`:

```
    1
   1 1
  1 2 1
 1 3 3 1
1 4 6 4 1
```

### Answer:

```python
from math import comb

n = 5
for i in range(n):
    print(" " * (n - i), end="")
    for j in range(i + 1):
        print(comb(i, j), end=" ")
    print()
```

---

## 7. Alphabet Pattern

### Question:

Print the following pattern for `n = 5`:

```
A
AB
ABC
ABCD
ABCDE
```

### Answer:

```python
n = 5
for i in range(1, n + 1):
    for j in range(65, 65 + i):
        print(chr(j), end="")
    print()
```

---

## 8. Hollow Square Pattern

### Question:

Print the following pattern for `n = 5`:

```
*****
*   *
*   *
*   *
*****
```

### Answer:

```python
n = 5
for i in range(n):
    if i == 0 or i == n - 1:
        print("*" * n)
    else:
        print("*" + " " * (n - 2) + "*")
```

---

## 9. Floyd's Triangle Pattern

### Question:

Print the following pattern for `n = 5`:

```
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

### Answer:

```python
n = 5
num = 1
for i in range(1, n + 1):
    for j in range(1, i + 1):
        print(num, end=" ")
        num += 1
    print()
```

---

## 10. Checkerboard Pattern

### Question:

Print the following pattern for `n = 5`:

```
* * * * *
 * * * * *
* * * * *
 * * * * *
* * * * *
```

### Answer:

```python
n = 5
for i in range(n):
    if i % 2 == 0:
        print("* " * n)
    else:
        print(" *" * n)
```

---
