# CEG3136 C cheatsheet
- [CEG3136 C cheatsheet](#ceg3136-c-cheatsheet)
- [Getting Setup](#getting-setup)
  - [Installing a C compiler](#installing-a-c-compiler)
    - [Installing C compiler on MacOS](#installing-c-compiler-on-macos)
    - [Installing C compiler on Windows](#installing-c-compiler-on-windows)
    - [Installing C compiler on Linux](#installing-c-compiler-on-linux)
  - [Hello World Script](#hello-world-script)
    - [Sample Code:](#sample-code)
    - [Running Hello World](#running-hello-world)
- [Variables in C](#variables-in-c)
  - [Primitive Types](#primitive-types)
  - [Strings](#strings)
  - [Arrays](#arrays)
- [Printing to the console (printf)](#printing-to-the-console-printf)
- [Appendix](#appendix)
  - [Code focused text editors](#code-focused-text-editors)
    - [Visual Studio Code](#visual-studio-code)
    - [Atom](#atom)
    - [Sublime Text](#sublime-text)
    - [Notepad++](#notepad)

# Getting Setup
## Installing a C compiler 
### Installing C compiler on MacOS
* Using brew run the following command `brew install gcc`
	* If you do not have brew setup follow instructions here: [The Missing Package Manager for macOS (or Linux) — Homebrew](https://brew.sh/)
### Installing C compiler on Windows 
Pending
### Installing C compiler on Linux
Pending

## Hello World Script
### Sample Code:
```
/* Hello World program */
#include <stdio.h>

void main(void){
printf("Hello World.\n");
}
```
### Running Hello World
1. Copy and paste the above sample code into a text editor of your choice. (If you don't have one visit the [Code focused text editors](#some-code-focused-text-editors) for examples) 
2. Save the file as `HelloWorld.c`
3. Open your preferred command line program and navigate to the directory in which you stored the above file.
4. Run the following command `gcc -o HelloWorld.out HelloWorld.c`
5. There should now be a file in that directory called `HelloWorld.out`
6. Depending on system you will have to run `./HelloWorld.out` or `HelloWorld.out`
7. If you have run these commands successfully you should see an output in your terminal that looks like `Hello World.`

# Variables in C
Pending
## Primitive Types
Pending
## Strings
Pending
## Arrays
Pending

# Printing to the console (printf)
Printing a predeterminded string to the console:
`printf("string goes here")`
You can also format a string to insert variables, this relies on the following markers that will be inserted in the base string
|  Variable Type  |  Marker  |
|---|---|
| `%d`  |  int |
| `%c`  | char  |
| `%f`  |  float |
| `%lf`  |  double |
| `%s`  |  string |

Multiple variables of the same type can be inserted into a `printf()` command. While the order that these variables are passed into the function are important, you should place them in the order that they are printed.
In the following example you can see 3 variables being passed in, 2 strings, and 1 integer. As you can see the variables being passed in are in the order that they will be displayed in. 
```
/* prinf example */
#include <stdio.h>

void main(void){
    char* name="John Smith";
    char* school="uOttawa";
    int age=19;
    printf("Hello my name is %s, I go to the %s and I am %d years old", name, school,age);
}
``` 
Output:
```Hello my name is John Smith, I go to the uOttawa and I am 19 years old```

For reference here is an example where the order of the variables being passed in are changed. 
`printf("Hello my name is %s, I go to the %s and I am %d years old", school, name, age);`
Output:
`Hello my name is uOttawa, I go to the John Smith and I am 19 years old`

Making an attempt to pass variables in an order that are not expected will cause an issue.

For example, if you state there will be 2 strings and then 1 int. They must be passed in this order.
Otherwise you will not be able to compile. 
`printf("Hello my name is %s, I go to the %s and I am %d years old", school, age, name);`

Results in the following error:
```
test.c:8:77: warning: format specifies type 'char *' but the argument has type 'int' [-Wformat]
printf("Hello my name is %s, I go to the %s and I am %d years old", school, age, name);
                                         ~~                                 ^~~
                                         %d
test.c:8:82: warning: format specifies type 'int' but the argument has type 'char *' [-Wformat]
printf("Hello my name is %s, I go to the %s and I am %d years old", school, age, name);
                                                     ~~                          ^~~~
                                                     %s
```


# Appendix 
## Code focused text editors 
### Visual Studio Code
>Visual Studio Code is an integrated development environment made by Microsoft for Windows, Linux and macOS. Features include support for debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git.

[Visual Studio Code Site](https://code.visualstudio.com/)
### Atom
>Atom is a free and open-source text and source code editor for macOS, Linux, and Microsoft Windows with support for plug-ins written in JavaScript, and embedded Git Control. Developed by GitHub, Atom is a desktop application built using web technologies.

[Atom Site](https://atom.io/)
### Sublime Text
>Sublime Text is a commercial source code editor. It natively supports many programming languages and markup languages. Users can expand its functionality with plugins, typically community-built and maintained under free-software licenses. To facilitate plugins, Sublime Text features a Python API.

[Sublime Text Site](https://www.sublimetext.com/)
### Notepad++
>Notepad++ is a text and source code editor for use with Microsoft Windows. It supports tabbed editing, which allows working with multiple open files in a single window. The project's name comes from the C increment operator. Notepad++ is distributed as free software.

[Notepad++ Site](https://notepad-plus-plus.org/)
