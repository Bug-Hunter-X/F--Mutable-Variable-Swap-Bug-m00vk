# F# Mutable Variable Swap Bug

This repository demonstrates a common error when working with mutable variables in F#.  The `swap` function attempts to swap the values of two mutable variables, but it fails to do so correctly.

The bug arises because F# variables are passed by value by default, meaning the function receives copies of the values, not references.  Therefore, modifying the copies within the function doesn't affect the original variables. 

The solution demonstrates the correct approach, using references or tuples to effectively swap the variable values.

## How to Reproduce

1. Clone the repository.
2. Open `bug.fs` to see the buggy code.
3. Compile and run the code.  Notice the values of `x` and `y` are unchanged after calling `swap`.
4. Then, look at `bugSolution.fs` to see how to correctly swap mutable variables.