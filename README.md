# Unexpected Behavior of Loose Comparison with NaN and -0 in JavaScript

This repository demonstrates an uncommon bug in JavaScript related to the loose comparison operator (==) when used with NaN (Not a Number) and -0 (negative zero).

## Bug Description

The loose comparison operator (==) in JavaScript does not correctly handle comparisons involving NaN and -0.  Specifically:

* `NaN == NaN` evaluates to `false`, even though NaN represents an undefined numerical value.
* `0 == -0` evaluates to `true`, despite being distinct numerical values.

This behavior can lead to unexpected and incorrect results in conditional statements.

## Bug Solution

To avoid this issue, use the strict equality operator (===) instead of the loose equality operator (==). The strict equality operator performs type checking before comparison, providing more predictable and reliable results.

## How to Reproduce

1. Clone this repository.
2. Run the `bug.js` file using a JavaScript runtime environment (e.g., Node.js).
3. Observe the unexpected output, specifically that `NaN == NaN` evaluates to `false`, which is counterintuitive.
4. Examine the corrected code in `bugSolution.js` which demonstrates the proper usage of the strict equality operator (===).