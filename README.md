# Uncommon HTML Bug: Handling Asynchronous Operations

This repository demonstrates a common JavaScript error encountered in HTML when dealing with asynchronous operations: attempting to access properties of an object that's `null` or `undefined` before it's been properly loaded.

The `bug.html` file showcases the erroneous code that triggers this error. The `bugSolution.html` file provides a corrected version with proper error handling using optional chaining and nullish coalescing.

## Bug Description
The error arises when the program tries to access a property (e.g., `user.name`) before the asynchronous operation (e.g., fetching user data from a server) completes.  This results in a `TypeError` because the object (`user` in this case) is not yet defined or is `null`.

## Solution
The solution uses optional chaining (`?.`) and nullish coalescing (`??`) operators to safely access the `name` property.  Optional chaining short-circuits if the object or any intermediate property is `null` or `undefined`, preventing the error. Nullish coalescing provides a default value if the expression is `null` or `undefined`.