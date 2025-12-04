---
sidebar_position: 5
---

# Refactor

The `refactor` tag categorizes a change as one that does not make any objective change in the code but improves internal structuring of the code without changing its external behavior.

Some examples of changes that would count as refactors are as follows:

- Moving a section of code reused in multiple places to its own function
- Setting a defined constant in the code to be a variable

Basically if a change is made to improve the readability or reusability of the code with our altering how the code actually functions then it should be given the `refactor` tag.

Examples:

- `refactor(user-controller): move creating error response to function`
- `refactor: replace repeated use of constant with immutable variable`