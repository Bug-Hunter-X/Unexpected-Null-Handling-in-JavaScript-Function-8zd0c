# Unexpected Null Handling in JavaScript Function

This repository demonstrates a subtle bug in a JavaScript function related to null handling. The function `foo` aims to add two numbers, but its behavior when null values are passed as arguments is unexpected and may lead to errors in applications that use this function.

## Bug Description

The `foo` function doesn't explicitly handle null values and uses loose comparison (`==`) for its null checks. This can lead to incorrect results when one or both arguments are null. The intended behavior is to return null if either argument is null. However, the current implementation only handles this correctly in the case of two null values.

## Solution

The solution involves using strict equality (`===`) to check for null values, ensuring a more robust and predictable outcome.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` to see the buggy code.
3. Run `bug.js` using a Node.js environment (or any JavaScript runtime) to observe the incorrect results.
4. Open `bugSolution.js` to see the fixed code.
5. Run `bugSolution.js` to observe the corrected results.