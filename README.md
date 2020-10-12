# C
The C Programming Language

# Compile and Run HelloWorld
![Compiling](https://www3.ntu.edu.sg/home/ehchua/programming/cpp/images/GCC_CompilationProcess.png)

## HelloWorld.c
```
#include <stdio.h>

int main()
{
        printf("Hello World!\n");

        return 0;
}
```

### step by step

1. Preprocessing: express directives(#include, #define, #if/#ifdef/#ifndef/...) and delete comments

    `$ gcc -E HelloWorld.c -o HelloWorld.i`

1. Compilation: compile the pre-processed source code into assembly code

    `$ gcc -S HelloWorld.i -o HelloWorld.s`

1. Assemble: converts the assembly code into machine code in the object file

    `$ gcc -c HelloWorld.s -o HelloWorld.o`

1. Linking: links the object code with the library code to produce an executable file

    `$ gcc HelloWorld.o -o HellWorld`

### all in one
* `-v` in verbose mode

    `$ gcc -v HelloWorld.c -o HelloWorld`

# Reference && Resource
1. [GCC Compilation Process](https://www3.ntu.edu.sg/home/ehchua/programming/cpp/gcc_make.html#zz-1.7)
