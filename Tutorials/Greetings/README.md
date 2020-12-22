We start the tour with a modified "hello world" program:

# This is a comment
```
echo "What's your name? "
var name: string = readLine(stdin)
echo "Hi, ", name, "!"
```
Save this code to the file "greetings.nim". Now compile and run it:

`nim compile --run greetings.nim`
With the `--run` switch Nim executes the file automatically after compilation. You can give your program command-line arguments by appending them after the filename:

`nim compile --run greetings.nim arg1 arg2`
Commonly used commands and switches have abbreviations, so you can also use:

nim c -r greetings.nim
To compile a release version use:

nim c -d:release greetings.nim
By default, the Nim compiler generates a large number of runtime checks aiming for your debugging pleasure. With -d:release some checks are turned off and optimizations are turned on.

Though it should be pretty obvious what the program does, I will explain the syntax: statements which are not indented are executed when the program starts. Indentation is Nim's way of grouping statements. Indentation is done with spaces only, tabulators are not allowed.

String literals are enclosed in double-quotes. The var statement declares a new variable named name of type string with the value that is returned by the readLine procedure. Since the compiler knows that readLine returns a string, you can leave out the type in the declaration (this is called local type inference). So this will work too:

var name = readLine(stdin)
Note that this is basically the only form of type inference that exists in Nim: it is a good compromise between brevity and readability.

The "hello world" program contains several identifiers that are already known to the compiler: echo, readLine, etc. These built-ins are declared in the system module which is implicitly imported by any other module.

