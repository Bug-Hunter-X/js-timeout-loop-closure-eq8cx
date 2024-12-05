# JavaScript Closure Issue in setTimeout Loop

This example demonstrates a common issue with closures in JavaScript when using `setTimeout` within a loop.  The expected output might be 0 to 9, each printed after a 1-second delay.  However, due to how closures work in JavaScript, you'll get a different result. This is because each setTimeout callback function does not create a copy of i, it captures i by reference, thus causing an issue. 

## Bug:
The `bug.js` file contains the buggy code.  Run it and observe the unexpected output.  The solution is provided in `bugSolution.js`

## Solution:
The solution addresses the closure problem by creating an immediately invoked function expression (IIFE) or using `let` within the loop. Each iteration of the loop will create a separate scope for the variable 'i'.