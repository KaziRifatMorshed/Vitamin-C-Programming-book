# Primary Knowledge

***

***

qwertyuiop

***

# Helpful Tools

## CPH extension

link: <https://marketplace.visualstudio.com/items?itemName=DivyanshuAgrawal.competitive-programming-helper>

![cph-img](https://github.com/agrawal-d/competitive-programming-helper/raw/HEAD/screenshots/screenshot-main.png)

#### Pros:

## Online C visual debugger <https://pythontutor.com/c.html>

#### Pros:

* visualize variables and changes step by step

#### Cons/Limitations:

* Can not take input (You have to define values of variables within source code)
* Can not process long code (Suitable for অল্প পরিমাণ কোড and beginners)

***

## Special Characters

Special characters like form-feed (and others) are non-printing characters that perform certain control functions in text processing. Here's a brief explanation of some of them, including form-feed:

### 1. **Form-feed (`\f`)**

* The **form-feed** character (`\f`) is used to signal the end of a page in printed documents. In the past, it would move the printer to the top of the next page.
* It's rarely used today but might still appear in some contexts (e.g., older printers, plain text files designed for page breaks).

Example:

```python
text = "Page 1 content\fPage 2 content"
print(text)
```

In this case, `\f` represents a form-feed, which would traditionally move content to a new page.

### 2. **Newline (`\n`)**

* The **newline** character (`\n`) moves the cursor to the next line.
* It is widely used in modern text processing to mark line breaks.

Example:

```python
text = "First line\nSecond line"
print(text)
```

### 3. **Carriage Return (`\r`)**

* The **carriage return** character (`\r`) moves the cursor to the beginning of the same line.
* In older systems (e.g., typewriters and early computers), `\r` would reset the cursor position to the start of the line without moving down.

Example:

```python
text = "Hello\rWorld"
print(text)
```

This would print "World", as `\r` causes the cursor to return to the start of the line, overwriting "Hello".

### 4. **Tab (`\t`)**

* The **tab** character (`\t`) inserts horizontal spaces, usually equivalent to 4 or 8 spaces, depending on the environment.

Example:

```python
text = "Column 1\tColumn 2\tColumn 3"
print(text)
```

### 5. **Backspace (`\b`)**

* The **backspace** character (`\b`) moves the cursor one position backward, which can effectively delete the previous character when printed.

Example:

```python
text = "Hello\b World"
print(text)
```

This would print "Hell World" because the backspace removes the "o".

### 6. **Null Character(`\0`)**

***

### Summary of Common Special Characters:

* `\f` – Form feed (new page).
* `\n` – Newline (new line).
* `\r` – Carriage return (return to the beginning of the line).
* `\t` – Tab (horizontal space).
* `\b` – Backspace (deletes the previous character).

Each of these special characters can be used for controlling text formatting in various contexts. Today, most of them are used primarily in text processing and formatting, especially in file or console output.
