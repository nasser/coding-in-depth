# History

Unity's semantics are not arbitrary, but a fairly well reasoned approach to video game programming that makes sense given their historical context. This is non-critical information, but might help answer questions that come up.

In many respects, video game development is a lot like other kinds of programming. It is unique in one important way, however: **the goal is an aesthetic, human experience**. This means “success” is highly subjective, and as a result **iteration and playtesting are indispensable**. The effect that has on the kind of programming you end up doing in games is that the flexibility of your code is important to ensure that you remain able to adapt to new creative ideas. This is radically different from, say, programming a server, where there will be a specification and a narrow definition of what is *correct*. Here, iteration is less important, and the kind of code you write changes accordingly.

```
_start:
        # write(1, message, 13)
        mov     $1, %rax
        mov     $1, %rdi
        mov     $message, %rsi
        mov     $13, %rdx
        syscall
        mov     $60, %rax
        xor     %rdi, %rdi
        syscall
message:
        .ascii  "Hello, world\n"
```

> *From http://cs.lmu.edu/~ray/notes/x86assembly/*

The original programming paradigm of the 1950s was imperative, where programs were nothing more than a sequence of machine level commands. There were no named variables, limited support for named blocks of code, mostly memory addresses that could be read and written to, no loops or conditionals, just “branch statements” to jump to different instructions, and no named functions, just blocks of code. Assembly languages for different computers fall into this category, and this kind of programming is still done on some low level systems.

```
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
}
```

> *From https://en.wikipedia.org/wiki/C_(programming_language)#.22Hello.2C_world.22_example*

Shortly following that was the structured programming of the late 1950s and 1960s. Most of the progress was being made in America, and these languages allowed programmers to assign English names to their variables and functions which made it easier for them to read and manage.