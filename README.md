# Julia Bug: Improper Exception Handling

This repository demonstrates an example of improper exception handling in Julia. The `bug.jl` file contains code that abruptly halts execution using `error()` when it encounters a negative input, which may not always be desired. The `bugSolution.jl` file provides a more robust solution.

## Bug Description
The `myfunction` function in `bug.jl` throws an error if the input is negative.  This is generally undesirable unless the negative input represents an unrecoverable condition.  A more graceful approach would be to either return a default value (like NaN or -1) or log a warning message.

## Solution
The `bugSolution.jl` demonstrates how to handle this scenario more gracefully.  It returns `NaN` for negative inputs. A better option might be to handle this in a way appropriate to the specific application.