The assignment statement
The assignment statement assigns a new value to a variable or more generally to a storage location:

```
var x = "abc" # introduces a new variable `x` and assigns a value to it
x = "xyz"     # assigns a new value to `x`
```

= is the assignment operator. The assignment operator can be overloaded. You can declare multiple variables with a single assignment statement and all the variables will have the same value:

```
var x, y = 3  # assigns 3 to the variables `x` and `y`
echo "x ", x  # outputs "x 3"
echo "y ", y  # outputs "y 3"
x = 42        # changes `x` to 42 without changing `y`
echo "x ", x  # outputs "x 42"
echo "y ", y  # outputs "y 3"
```

Note that declaring multiple variables with a single assignment that calls a procedure can have unexpected results: the compiler will unroll the assignments and end up calling the procedure several times. If the result of the procedure depends on side effects, your variables may end up having different values! For safety use side-effect-free procedures if making multiple assignments.