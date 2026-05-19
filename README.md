# Libft

## 📖 About the Project
**Libft** is the foundational system administration and programming project of the 42 school core curriculum. The goal is to recreate a custom C library containing a set of standard C library functions (`libc`), as well as additional utility functions that will be used heavily throughout the rest of the curriculum. 

This project builds a solid foundation in C programming, low-level memory allocation, and data structures. This specific version of Libft has also been expanded to include Linked List management (Bonus) and a custom implementation of `ft_printf`.

## 🚀 Features

The library is divided into several categories of functions:

### 1. Standard C Library Functions (libc)
* **Character checks & manipulation:** `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower`
* **String manipulation:** `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`
* **Memory manipulation:** `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
* **Allocation & Conversion:** `ft_atoi`, `ft_calloc`, `ft_strdup`

### 2. Additional Utility Functions
* **String operations:** `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`, `ft_itoa`, `ft_strmapi`, `ft_striteri`
* **File Descriptor Output:** `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

### 3. Linked Lists (Bonus)
* `ft_lstnew`, `ft_lstadd_front`, `ft_lstsize`, `ft_lstlast`, `ft_lstadd_back`, `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`, `ft_lstmap`

### 4. Extended Capabilities (`ft_printf`)
* Includes a custom implementation of `printf` for formatted output (`ft_printf`, `ft_printhex`, etc.).

## 🛠️ Usage

### Compilation
The project includes a `Makefile` to easily compile the library into a static library file (`libft.a`).

Run the following commands in the terminal:

```bash
# Compile the library (standard functions + extensions)
make

# Remove object files (.o)
make clean

# Remove object files and the libft.a executable
make fclean

# Recompile everything from scratch
make re
```

### Implementing `libft` in your code
Include the header file in your C programs and compile your project with the generated `libft.a`.

**main.c:**
```c
#include "libft.h"
#include "ft_printf.h" // If using the ft_printf extension

int main(void)
{
    char *str;

    str = ft_strdup("Hello from Libft!");
    ft_putendl_fd(str, 1);
    
    ft_printf("Testing my custom printf: %s\n", "Works perfectly!");

    free(str);
    return (0);
}
```

**Compile your program:**
```bash
gcc -Wall -Wextra -Werror main.c -L. -lft -o my_program
./my_program
```

## 🧠 What I Learned
* A deep understanding of manual memory management in C (`malloc`, `free`, and preventing memory leaks).
* Re-implementing essential low-level algorithms for safe string manipulation and memory copying.
* Working with structural data types, specifically developing a robust toolkit for Singly Linked Lists.
* Automating simple build systems using `Makefiles`, compiling code into reusable `.a` static libraries.
