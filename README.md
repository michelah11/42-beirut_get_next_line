<h1 align="center">get_next_line</h1>

<p align="center">
  <strong>42 Beirut</strong><br>
  A function that reads from a file descriptor line by line using minimal memory and efficient buffer management.
</p>

---

## 📌 Project Description

**get_next_line** is a low-level C function that reads and returns one line at a time from a file descriptor. It handles dynamic memory allocation, buffer management, and persistent state tracking across multiple calls. This project emphasizes understanding how static variables work and how to manage data flow when reading streams incrementally.

---

## ✅ Function Prototype

```c
char *get_next_line(int fd);
```

---

## 📁 Project Structure

```
get_next_line/
├── get_next_line.c         # Core implementation of get_next_line
├── get_next_line_utils.c   # Helper functions (e.g., string and buffer operations)
├── get_next_line.h         # Header file containing prototypes and includes
├── Makefile                # Build rules (mandatory and bonus)
```

---

## 📜 Mandatory Requirements

- Read from any file descriptor using `read()`, one line at a time.
- The returned line **includes the `\n` character** if found before EOF.
- Must handle multiple calls and preserve buffer state across calls using a **static variable**.
- Must compile with a dynamic `BUFFER_SIZE`:
  ```bash
  cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 *.c
  ```
- Must not use:
  - `libft`
  - `lseek()`
  - global variables

---

## 🧪 Compilation

```bash
make          # Compile mandatory version
make bonus    # Compile bonus version (if implemented)
make clean    # Remove object files
make fclean   # Remove object files and executable
make re       # Clean and rebuild
```

---

## 🔧 Bonus Features

If the mandatory part is perfect, bonus features may include:

- Support for **multiple file descriptors** simultaneously.
- One single **static variable** used across function calls.
- Additional files for bonus:
  - `get_next_line_bonus.c`
  - `get_next_line_bonus.h`
  - `get_next_line_utils_bonus.c`

---

<p align="center"><i>A great exercise in stateful programming, memory management, and low-level stream handling in C.</i></p>
