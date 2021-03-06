---
annotatedpdfurl: /lectures/CS16_Lecture5_ann.pdf
annotatedready: true
num: Lecture 5
desc: "Makefiles, File IO"
ready: true
slides: /lectures/CS16_Lecture5.pdf
lecture_date: 2020-01-21
---

# Topics


## Automate the compilation of code using makefiles

* [read about Makefile](https://foo.cs.ucsb.edu/16wiki/index.php/C%2B%2B:_Separate_Compilation_and_Makefiles)
* Compile-time errors
* Linker errors
* Header guards
* Refer to Professor Wang's detailed notes on makefiles: [https://ucsb-cs32.github.io/f19/lectures/lect01/](https://ucsb-cs32.github.io/f19/lectures/lect01/)


## Test driven development

* Write test code and actual code side by side- so your implementation is always tested
* Start with function stubs
* Write the simplest test case and make your code pass that case
* Write another test case, expect your code to fail, see it fail, then add code to pass that test case (and the previous one).
* With every new test case, we have to make sure that all our previous tests still pass - this is a great way to make sure that things that were working before are not broken by new code!


## Lesson plan

* We will start with the code that we wrote earlier for drawing shapes and testing the functions we wrote with our home grown test framework
* Our first goal is to split our original implementation into multiple files in a way that maximizes reuse. For example we can reuse our drawTriangle and drawSquare functions to draw a house. However, this is not possible with the file structure in lecture 5. We'll discuss why that is.

* Once we have broken down our single cpp file into logical separate files, its time to compile the code. Our goal will be to select and combine the pieces that make a complete program

* If we tried to compile any one file (independent of the others), we are likely to get compiler errors and linker errors. You should be able to distinguish between these two types of errors and why they occur. To understand this distinction we need to peek under the hood of the compilation process and the intermediate steps that g++ takes to create an executable (see slides for more information). You will be introduced to object files - a very important concept for later lessons.

* We will first try to compile each file separately on the command line using the g++ option -c. For example

```
g++ -c shapes.cpp
```
The above command creates the object file shapes.o

We will then look at how to link all the object files into an executable using the -o option as shown below

```
g++ file1.o file2.o file3.o -o finalexecuatble
```





## File I/O basics
* Intro to lab03
* Examining text files using 1) an editor 2) cat command
* Opening a file: open()
* Reading a line from a file: getline()
* Reading until the end of file is reached
* Detecting failures
* Printing error messages to standard error with cerr
* When do we use exit() and why?


