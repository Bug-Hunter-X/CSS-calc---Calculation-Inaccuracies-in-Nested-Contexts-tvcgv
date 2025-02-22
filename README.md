# CSS calc() Calculation Issues

This repository demonstrates a subtle bug related to the `calc()` function in CSS when combining percentages and fixed units (like pixels) within nested elements. The bug arises when the calculation's base (percentage) is dependent on an ancestor's size, and that ancestor's size is affected by other CSS rules.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to observe the incorrect implementation.
3. Open `bugSolution.css` to see how to mitigate the issue.

## Solution

The solution involves ensuring the calculation base is reliable and consistent. Using viewport units such as `vw` or `vh` may provide more consistent results, as they're based on the viewport's size, rather than the parent's size, which might be affected by unexpected factors.