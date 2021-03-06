# ce04 From Exceptional to Enhanced Cat

This class exercise is designed to familiarize students with exceptions and file I/O in Java.

## Prerequisite Knowledge

* Basic knowledge of Java exceptions, including checked exceptions, unchecked exceptions, and
  the use of `try`-`catch`, `throw`, and `throws`.
* Familiarity with program command-line arguments in Java.

## Questions

In your notes, clearly answer the following questions. These instructions assume that you are 
logged into the Nike server. 

**NOTE:** If a step requires you to enter in a command, please provide in your notes the full 
command that you typed to make the related action happen. If context is necessary (e.g., the 
command depends on your present working directory), then please note that context as well.

### Getting Started

1. Use Git to clone the repository for this exercise onto Nike into a subdirectory called `cs1302-ce04`:

   ```
   $ git clone https://github.com/cs1302uga/cs1302-ce04.git
   ```

1. Change into the `cs1302-ce04` directory that was just created and look around. There should be
multiple Java files somewhere in the directory structure. 

   * What are the fully qualified names for the classes contained in those files?
   * What is the path to the default package for source code relative to the `cs1302-ce04`
     directory?

1. From the `cs1302-ce04` directory, try to compile each Java file separately. Note, there ares
   some dependencies between the Java files--therefore the order in which you compile them matters.
   **Note** The files likely contain some compile-time (syntax) errors.
   If the compiler displays multiple errors, then only look at the first one! That first
   error may have a domino / cascading effect on the rest of the file.
   For the the first compile-time error, do the following:

   * In what file is the error?
   * On what line in the source code is the error?
   * How does Java describe the error?
   * Fix that specific compile-time error. There may be logical errors with the code--do not fix them at this time.
   * Briefly describe your fix.
   * Try to recompile. Repeat these steps with the next compile-time error, as needed, until the code compiles.

**CHECKPOINT**
    
### Using Your Cat
   
1. From the `cs1302-ce04` directory, use the `MyCat` program to display the contents of `Printer.java`
   by passing the relative path to `Printer.java` as a command-line argument.
   **HINT:** When a program interacts with files, it is relative to the current working directory in
   which the program is being run. That is, the directory you are in when you type the `java` command.
   For a Java program, relative paths are relative to that directory. 

1. From the `cs1302-ce04` directory, use the `MyCat` program to display the contents of standard input.
   **HINT:** Read through the code to see what command-line argument you might use to read from standard 
   input.
   This may seem weird at first, but the program should allow you to type in lines of text to standard
   input. When you complete a line by hitting return, the program will print the line to standard input.
   The program will terminate once it reaches the end of the file. What does that mean for standard
   input? You can trigger the end of file (a.k.a. the `EOF`) by pressing `C-d`.

1. **[TRICKY]** From the `cs1302-ce04` directory, use the `MyCat` program to display the contents of 
   standard input. At the same time, use input redirection to make standard input for the program come 
   from `MyCat.java` instead of from the keyboard. You should be familiar with standard output redirection
   via `>` and `>>`. Redirecting input uses a similar syntax.

**CHECKPOINT**
    
### Enhancing Your Cat

1. From the `cs1302-ce04` directory, run the `MyCat` program with no command-line arguments. A run-time
   exception should occur. What is it, and why did it occur?

1. There are multiple ways to fix the run-time exception that you encountered in the last step.
   Fix the problem in such a way that the following criteria are met whenever the exception occurs:
   
   * The program does not crash.
   * The exception message is stil displayed to standard error. Check the Java API for methods if you're stuck.

   When displaying the exception message, something like the following will suffice 
   (replacing `<message>` with the actual exception message):

   ```
   MyCat: <message>
   ```

1. From the `cs1302-ce04` directory, run the `MyCat` program with no command-line arguments. What's the
   difference between this execution of the program and the one performed two steps earlier?

**CHECKPOINT**
    
### Further Enhancing Your Cat

1. Now, let's add some more functionality to the `MyCat` program. Change the code so that one of more
   command-line arguments are accepted. The expected behavor is that `MyCat` should print the files, in
   order, to standard output, effectively con<b>cat</b>enating the contents of the supplied files.

1. From the `cs1302-ce04` directory, use your enhanced `MyCat` program to display the contents of 
   `Printer.java`, standard input, and `MyCat.java` in that order! If your program does not currently
   allow "-" to be specified for arbitrary file names in the list of command-line arguments, then 
   modify it to accomodate that feature.

1. Run your enhanced `MyCat` program by passing in two filenames as command-line arguments. Make sure
   the first file does not exist in the file system. Your program should catch the `FileNotFoundException`,
   print the appropriate message, and still print the contents of the second file (assuming it exists).
   
1. Update the comments in the source code to reflect any functionality that has been added since
   the beginning of this exercise.

**CHECKPOINT** 
    
<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
