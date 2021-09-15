# CEG3136 C cheatsheet
- [CEG3136 C cheatsheet](#ceg3136-c-cheatsheet)
- [Getting Setup](#getting-setup)
  - [Installing a c compiler](#installing-a-c-compiler)
    - [Installing C compiler on MacOS](#installing-c-compiler-on-macos)
    - [Installing C compiler on Windows](#installing-c-compiler-on-windows)
    - [Installing C compiler on Linux](#installing-c-compiler-on-linux)
  - [Hello World Script](#hello-world-script)
    - [Sample Code:](#sample-code)
    - [Running Hello world](#running-hello-world)
- [Appendix](#appendix)
  - [Code focused text editors](#code-focused-text-editors)
    - [Visual Studio Code](#visual-studio-code)
    - [Atom](#atom)
    - [Sublime Text](#sublime-text)
    - [Notepad++](#notepad)

# Getting Setup
## Installing a c compiler 
### Installing C compiler on MacOS
* Using brew run the following command `brew install gcc`
	* If you do not have brew setup follow instructions here: [The Missing Package Manager for macOS (or Linux) — Homebrew](https://brew.sh/)
### Installing C compiler on Windows 
* Pending
### Installing C compiler on Linux
* Pending

## Hello World Script
### Sample Code:
```
/* Hello World program */
#include <stdio.h>

void main(void){
printf("Hello World.\n");
}
```
### Running Hello world
1. Copy and paste the above sample code into a text editor of your choice. (If you don't have one visit the [Code focused text editors](#some-code-focused-text-editors) for examples) 
2. Save the file as `HelloWorld.c`
3. Open your preferred command line program and navigate to the directory in which you stored the above file.
4. Run the following command `gcc -o HelloWorld.out HelloWorld.c`
5. There should now be a file in that directory called `HelloWorld.out`
6. Depending on system you will have to run `./HelloWorld.out` or `HelloWorld.out`
7. If you have run these commands successfully you should see an output in your terminal that looks like `Hello World.`





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
