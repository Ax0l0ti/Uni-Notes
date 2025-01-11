# Dynamic Memory Allocation
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  11-01-2025
> > *Module :* [[Advanced Programming]]
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
> > $a)$ -  
> $b)$ - 
> $c)$ - 

---

### 1. **Dynamic memory allocation in C**

- Use of `malloc`, `calloc`, `realloc`, and `free` to manage memory during runtime. Allows flexible memory use for unknown sizes.

### 2. **Pointers and their dangers**

- **Definition**: Address-holding variables, indirect memory access.
- **Dangers**: Dangling pointers, memory leaks, segmentation faults, invalid pointer dereferencing.

### 3. **Static vs. dynamic arrays**

- **Static**: Fixed size, compile-time allocation (`int arr[10]`).
- **Dynamic**: Flexible size, runtime allocation (`int* arr = malloc(n * sizeof(int))`).

### 4. **Using `malloc` for memory allocation**

- Allocates memory in bytes, requires manual size calculation and type casting (`void*` return type).

### 5. **Typecasting malloc return types**

- Cast the `void*` return to target type (`int* p = (int*)malloc(n * sizeof(int))`). Optional in C but required in C++.

### 6. **Freeing memory with `free`**

- Prevents **memory leaks**. Match each `malloc` with `free`. Double freeing leads to undefined behavior.

### 7. **Importance of garbage collection**

- Automatic memory management (not in C). Prevents leaks/dangling pointers but increases overhead.

### 8. **Dynamic arrays vs. static arrays**

- **Dynamic**: Flexible size, fragmented memory.
- **Static**: Contiguous, predictable access time, faster.

### 9. **1D vs. 2D dynamic arrays**

- **1D**: Single `malloc` call.
- **2D**: Array of pointers with nested `malloc`. Slower access than static 2D arrays.

### 10. **Static and dynamic 2D arrays**

- **Static**: `int arr[10][10]`. Fixed, stack memory.
- **Dynamic**: Use `int**` with multiple `malloc` calls for rows/columns.

### 11. **Pointer to pointer for 2D arrays**

- **Definition**: `int** p;`. Pointer to row pointers, indirect access to elements.

### 12. **Allocating and freeing memory for arrays**

- **Allocation**: `malloc` for rows, nested `malloc` for columns.
- **Freeing**: Free columns first, then rows to prevent dangling rows.

### 13. **Contiguous vs. non-contiguous memory allocation**

- **Contiguous**: Single block, efficient caching (`int* p = malloc(n*m*sizeof(int))`).
- **Non-contiguous**: Separate blocks (pointer arrays), slower access.

### 14. **Memory models for static and dynamic arrays**

- **Static**: Stack memory, fixed size, faster access.
- **Dynamic**: Heap memory, flexible, more overhead.

### 15. **Error handling in dynamic memory allocation**

- Check `malloc` return (`if (ptr == NULL)`), log errors, clean up partially allocated memory.

### 16. **Importance of checking for null pointers**

- Prevents segmentation faults. Essential in low-memory scenarios or faulty allocation.

### 17. **Ragged arrays and uses**

- **Definition**: 2D array with varying column sizes.
- **Uses**: Sparse matrices, space optimization.

### 18. **Pass by value vs. pass by reference**

- **Value**: Copies data, safer, more memory.
- **Reference**: Efficient, modifies original data, risk of unintended changes.

### 19. **Drawing lines in a framebuffer**

- **Framebuffer**: Contiguous memory for pixel storage. Algorithms like Bresenham’s for line rendering.

### 20. **Managing framebuffers**

- Allocate memory, initialize, update pixels, free memory. Functions abstract the logic for easy reuse.

### 21. **Testing dynamic memory management in C**

- Use tools like **Valgrind**. Test boundary cases, null pointers, and memory leaks rigorously.

### 22. **Next steps: Libraries and transforms in programming**

- **Libraries**: GLib for dynamic data structures, OpenGL for framebuffers.
- **Transforms**: Fourier Transform for signal/image processing, linear transforms for rendering.