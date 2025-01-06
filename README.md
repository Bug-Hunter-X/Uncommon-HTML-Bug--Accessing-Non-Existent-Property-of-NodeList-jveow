# Uncommon HTML Bug: NodeList Property Access

This repository demonstrates a subtle bug related to accessing properties of a NodeList in JavaScript within an HTML context.  The issue arises from incorrectly assuming a NodeList has properties beyond standard array-like access.

## The Bug
The `document.querySelectorAll` method returns a NodeList, which is similar to an array but lacks certain array-like properties.  Attempting to directly access a non-existent property on this NodeList results in a runtime error.

## The Solution
The solution involves properly accessing NodeList elements using array-like indexing (`[index]`) and checking the length before accessing elements to avoid errors.  Iterating through the NodeList also ensures robustness.