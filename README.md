# Lua Table Iteration Bug
This repository demonstrates an uncommon bug in Lua related to the unpredictable iteration order of the `pairs()` function when used within a recursive function that modifies the table being iterated.

## Bug Description
Lua's `pairs()` iterator does not guarantee a specific order of traversal.  While generally consistent for a single pass, this becomes problematic in recursive functions where the table structure might change during iteration.

## How to Reproduce
1. Clone this repository.
2. Run `bug.lua`.
3. Observe that the output might not be as expected due to the inconsistent order of table traversal.

## Solution
The `bugSolution.lua` file provides a solution using a different approach to iterate and avoid unexpected behavior.