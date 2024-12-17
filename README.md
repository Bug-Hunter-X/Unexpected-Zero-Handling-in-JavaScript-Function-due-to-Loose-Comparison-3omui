# Unexpected Zero Handling in JavaScript Function

This repository demonstrates a subtle bug in JavaScript related to loose comparison (==) and its interaction with zero values. The bug causes a function to prematurely return zero even when it should be performing a calculation.

## Bug Description

The `foo` function is intended to add two numbers together. However, the `if` statement uses loose comparison (`===`) to check if either input is zero. This leads to unexpected behavior when inputs that are type-coerced to zero are encountered.  The function will incorrectly return 0 for these cases. 

## Solution

The solution replaces the loose comparison (`==`) with strict comparison (`===`). This ensures that the function correctly handles all input types.