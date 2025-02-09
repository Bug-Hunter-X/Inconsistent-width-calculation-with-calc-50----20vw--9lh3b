# Inconsistent Width Calculation with calc(50% - 20vw)

This repository demonstrates a subtle bug related to the use of CSS's `calc()` function with a mix of percentage and viewport-width units.  The issue arises from inconsistencies in how different browsers interpret and evaluate the expression `calc(50% - 20vw)`.  The expected behavior is a consistent width calculation across various viewport sizes, but this is not always the case.

## Bug Description

The `calc(50% - 20vw)` expression aims to calculate a width that's 50% of the container's width minus 20% of the viewport's width.  However, inconsistencies may occur in the order of operations, resulting in different calculated widths depending on the browser and the viewport size.

## Reproduction

The `bug.css` file contains the problematic CSS.  You can reproduce the issue by creating an HTML file that includes this CSS and observing the width of the element with the `.container` class across different viewport sizes in various browsers.

## Solution

The `bugSolution.css` file provides a potential workaround to address the inconsistency, ensuring a more reliable width calculation.