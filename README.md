# exercise-8

## Overview

The point of this assignment is to get hands-on with the stack. You will allocate a stack frame, save register values onto the stack, perform some register operations, restore selected values, and deallocate the stack frame.

This exercise focuses only on stack mechanics. No subroutines are required.

Complete the provided `main.s` file using the Venus simulator extension in VS Code.

## Required Work

As always, the specifics can be found in comments in the source code, but the general idea is:

You will be given initialized values in registers `t0`, `t1`, `t2`, and `t3`.

You will allocate a 16-byte stack frame and save those initial values onto the stack in register order, using word-aligned slots starting at `0(sp)`.

Then you will perform the calculations described in the source code.

After that, restore the values of `t0`, `t1`, `t2`, and `t3` and put them in `a2`, `a3`, `a4`, and `a5` respectively.

Finally, you will deallocate the stack frame so that `sp` is back where it started.

The starter code sets `sp` to a known address for grading. You do not need to change that setup, but your final value of `sp` should match the starting value.

Freeing a stack frame does not erase the memory that was used. The saved values should still be present in the stack region when the program finishes.

## Grading

- `t0-3` contain the correct values: 12 total points, 3 points per register
- `a2-5` contain the correct values: 16 total points, 4 points per register
- The memory from the deallocated stack frame contains the original saved values: 16 total points, 4 points per value
- `sp` is restored to the original starting address: 4 points
- Output contains the correct string message: 2 points

# Submitting Work

When you are done working, or just want to save your progress, you need to **commit AND push** your work to your repository. This can be done in any number of ways, but as I have suggested and will continue to suggest, GitHub Desktop makes this very easy. If you need more information on exactly how to do this, I suggest watching the tutorial video posted on canvas. When you are all done, submit the link to your GitHub repo to canvas. Submitting the link is just so canvas doesn't think you skipped the assignment, it has no bearing on your actual grade.

Here is some more information about submission:

1. Committing alone is not enough to submit your work. You must also push. The push step immediately follows the commit step. Without pushing, your work has not actually been submitted. 
2. If you want to check that your work has truly been submitted, you can always go to your repository online and view your most recent changes. 
3. You can commit and push as many times as you want. There is no limit, and it does not trigger any grading. It does however enable me to see your work/changes. So if you ever need my help with a programming issue, you must commit and push first.