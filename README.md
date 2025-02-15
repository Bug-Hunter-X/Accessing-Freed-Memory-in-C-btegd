# Accessing Freed Memory in C

This repository demonstrates a common error in C programming: accessing memory after it has been freed.  The `bug.c` file contains the erroneous code. The `bugSolution.c` file provides a corrected version. 

**Problem:**

The code allocates memory using `malloc`, copies data into it, and then frees the memory using `free`.  After freeing, it attempts to access the memory again which results in undefined behavior. This can lead to crashes or unpredictable results.

**Solution:**

The solution avoids accessing the memory after it has been freed.  After calling `free`, the pointer `ptr` should no longer be used to access the memory.

**Lesson:**
Always be careful when working with dynamically allocated memory. After freeing memory with `free`, do not use the pointer to access the memory again.  This is a common source of segmentation faults and other memory-related errors.