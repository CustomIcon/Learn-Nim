The let statement
The let statement works like the var statement but the declared symbols are single assignment variables: After the initialization their value cannot change:

```
let x = "abc" # introduces a new variable `x` and binds a value to it
x = "xyz"     # Illegal: assignment to `x`
```

The difference between let and const is: let introduces a variable that can not be re-assigned, const means "enforce compile time evaluation and put it into a data section":

const input = readLine(stdin) # Error: constant expression expectedlet input = readLine(stdin)   # works