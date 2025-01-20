# CSS Calc() Unexpected Behavior

This repository demonstrates an uncommon issue with the CSS `calc()` function when combining percentages and fixed pixel values. The issue stems from the way `calc()` resolves percentages relative to the parent element's width, while fixed pixel values remain absolute.

## The Problem

When you use `calc()` to subtract pixels from a percentage width (e.g., `width: calc(50% - 10px)`), the result can be inconsistent if the parent element's width changes dynamically. The percentage is recalculated based on the new parent width, but the fixed pixel value remains constant. This mismatch leads to unpredictable layout shifts.

## Solution

The solution depends on the desired behavior and context.  If a consistent layout is required, consider using only percentages or only pixels.  If you need a mix, you might need to use JavaScript to dynamically recalculate the `width` based on the parent element's size and the current viewport.