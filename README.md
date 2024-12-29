# TypeScript Type Guard Issue with null and undefined

This repository demonstrates a subtle issue with TypeScript's type guards when dealing with `null` and `undefined`.  The `greet` function is designed to handle both string inputs and `null` gracefully, but it unexpectedly throws an error when provided with `undefined`.

The `bug.ts` file contains the problematic code. The solution, found in `bugSolution.ts`, showcases a more robust approach that addresses this issue.

## Bug Description
TypeScript's type guards do not implicitly check for undefined values. Even though the function specifies that the parameter can be either a string or null, an error occurs when the parameter is undefined. The error arises due to type narrowing not covering the undefined case.