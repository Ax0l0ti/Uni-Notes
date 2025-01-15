# Library Design
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  15-01-2025
> > *Module :* [[]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]
> [[#]]
> [[#]]
> [[#]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  header + source, object
> $b)$ - 
> $c)$ - 

---

#TODO 

## **Creating Libraries**

### 1. **Write Your Own**

- Libraries in C are collections of related functions and definitions that can be reused in multiple programs.
- To create a library:
    1. Write your C code (`.c` files) containing the functions you want to include in the library.
    2. Define function prototypes and constants in a header file (`.h`) for easier integration.

#### Example:

**Header File (`mylib.h`):**


```c
#ifndef MYLIB_H
#define MYLIB_H

int add(int a, int b);
int subtract(int a, int b);

#endif
```

**Source File (`mylib.c`):**

```c
#include "mylib.h"

int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}```

---

### 2. **Use of Header Files and C Pre-processor**

- The **header file** provides function declarations and macros to be included in multiple programs.
- Include the header file using the `#include` directive, ensuring the preprocessor replaces `#include "mylib.h"` with the actual content of the file during compilation.

#### Usage in Another Program:

**Main Program (`main.c`):**

```c
#include <stdio.h>
#include "mylib.h"

int main() {
    printf("Sum: %d\n", add(5, 3));
    printf("Difference: %d\n", subtract(5, 3));
    return 0;
}```

---

### 3. **Use of Object Files**

- Compile the source files (`mylib.c`) into an **object file** (`mylib.o`):

```bash
gcc -c mylib.c -o mylib.o
```
    
- Use the object file during the final linking stage of the program:
```bash	       
gcc main.c mylib.o -o main
  ```


---

### 4. **Use of Makefiles** NOT EXAMINED

- Automate compilation using a **Makefile**: **Makefile Example:**

```Makefile
CC = gcc
CFLAGS = -Wall -c
LFLAGS = -Wall

all: main

main: main.o mylib.o
	$(CC) $(LFLAGS) main.o mylib.o -o main

main.o: main.c mylib.h
	$(CC) $(CFLAGS) main.c

mylib.o: mylib.c mylib.h
	$(CC) $(CFLAGS) mylib.c

clean:
	rm -f *.o main

```

Run `make` to build the program, and `make clean` to remove compiled files.

---

## **Implementing Your Own Garbage Collection**

- In C, memory is managed manually using `malloc`, `calloc`, `realloc`, and `free`. Custom garbage collection requires tracking memory allocations and ensuring unused memory is freed.
### Steps:
1. **Track Allocations**:
    - Maintain a data structure (e.g., a linked list or hash table) to store pointers to all allocated memory blocks.
2. **Free Unused Memory**:
    - Periodically check the data structure for memory that is no longer referenced and free it.
    - Use reference counting or a mark-and-sweep algorithm.