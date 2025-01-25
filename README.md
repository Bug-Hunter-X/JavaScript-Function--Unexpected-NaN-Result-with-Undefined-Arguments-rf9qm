# JavaScript Function Bug: Unexpected NaN Result with Undefined Arguments

This repository demonstrates a common subtle bug in JavaScript functions related to handling undefined values. The `foo` function intends to return 0 if either `a` or `b` is null; however, it fails to correctly handle undefined values, leading to unexpected NaN results.

## Bug Description

The original `foo` function only explicitly checks for null values. When either `a` or `b` is undefined, the addition operation (`a + b`) results in NaN (Not a Number). This is a common error when working with potentially undefined values in JavaScript.

## Solution

The solution involves explicitly checking for both null and undefined values using loose equality (`==`) or the strict equality operator (`===`).  The solution provided uses loose equality for conciseness, allowing the function to consistently return 0 for null or undefined inputs.