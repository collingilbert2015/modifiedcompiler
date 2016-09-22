# modifiedcompiler

##Description

This a book project from "Compiler Construction Using Java, JavaCC, and Yacc" by Anthony Dos Reis. It is very complicated if you're not familiar with the custom Operating System designed just for the book.
However, if you're interested in actually understanding what a compiler does and how assembly instructions are actually created from the parsing of your code, this is a project you might be interested in. Much of it has been heavily modified by me to allow special instructions and I'll probably continue to do so. 


## Usage 

The software package for the J1 system must be downloaded and install, but other than that simple programs can be passed through the compiler. For example, if you wanted to pass in the following: 

//This is a comment

x = 5;

y = x + 5;

print(y);

println(x+y);

If you were to just create a file in a test editor and pass it into the compiler what happens and why?


Simply put, a line of tokens is passed into a struct where each char can be analyzed, categorized, and passed into functions that know how to do with them. For example, let's look at the x = 5 statement. 
First, X would be recognized as not a number, but a variable. So the "image" of that variable is saved, we'll need to output it later. Moreover, the '=' will be flagged as an assign statement character and '5' is simply an integer. 


The assign character would make the compiler pass into the "assign" function. It emits instructions to take the integer and store it as the address of variable X. 
Output of x = 5 would be: 

pc x <---- address of x

p 5  <---- push the value of 5 on the stack 

stav <---- put the last value in the last address on the stack. 


If this all seems boring. Go check out the code to the Java Virtual Machine. It is isn't all that different. Knowing what is going on inside your programs is powerful. This compiler is simple. However, many compilers use similar recursive descent parsing and can be easily understood. 
