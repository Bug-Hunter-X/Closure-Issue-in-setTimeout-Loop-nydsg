# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop.  The expected behavior is to log the numbers 0 through 9 with a one-second delay between each.  However, due to the closure's behavior, the loop completes before the `setTimeout` callbacks execute, resulting in all callbacks logging the final value of `i` (which is 10).

## Bug Report
The `bug.js` file contains the problematic code.  Run this code to observe the unexpected output.

## Solution
The `bugSolution.js` file provides a corrected version using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, correctly capturing the value of `i`.