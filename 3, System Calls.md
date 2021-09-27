
# System calls
## Intro
So this is where the book's handholding stops. And fair warning, plenty of the stuff from here on is stuff I came up without referring anywhere. It was faster and more fun this way. Sure it works, but I am not sure this is the best way. Getting that out of the way, let's talk about system calls. 
## About System calls
For this assignment, we are expected to implement system calls as an array of functions basically. The user library, supplied with the assignment - `stdlib.c`, will call the appropriate function for each system call based on constants defined in `stdlib.h`. The constants mainly define two things: where in memory the array of functions should start from and what the index of each function should be. It also defines some types for our convenience.

## Idea behind implementing system calls
So for this assignment, we have the constants we need defined in stdlib.h. The ones useful for us now are the start address of the array (SYSCALL_VECTOR) and the index of each system call. All we have to do for this part now is take the print and print_int functions we have from the screen driver (if you haven't implemented print_int, implement it) then place them at the appropriate index.

## Pitfalls
- Don't forget to cast the functions and system call array to the types defined in the stdlib.h
