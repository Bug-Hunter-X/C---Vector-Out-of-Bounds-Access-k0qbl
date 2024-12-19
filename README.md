# C++ Vector Out-of-Bounds Access Bug

This repository demonstrates a common C++ bug: accessing an element beyond the bounds of a `std::vector`.  The provided code attempts to iterate through the vector, but the loop condition is incorrect, leading to undefined behavior (likely a crash or unpredictable output).

The solution provides the corrected code with the appropriate loop condition to avoid the out-of-bounds access.

## Bug

The bug lies in the loop condition of the `for` loop.  `i <= vec.size()` allows `i` to become equal to `vec.size()`, which is an invalid index for a zero-based vector.

## Solution

The solution simply corrects the loop condition to `i < vec.size()`, ensuring that the loop iterates only up to, but not including, the last valid index.