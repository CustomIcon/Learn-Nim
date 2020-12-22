Constants
Constants are symbols which are bound to a value. The constant's value cannot change. The compiler must be able to evaluate the expression in a constant declaration at compile time:

`const x = "abc" # the constant x contains the string "abc"`
Indentation can be used after the const keyword to list a whole section of constants:

```
const
  x = 1
  # a comment can occur here too
  y = 2
  z = y + 5 # computations are possible
```