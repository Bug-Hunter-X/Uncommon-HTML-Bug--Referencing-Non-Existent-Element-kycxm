# Uncommon HTML Bug: Referencing Non-Existent Element

This repository demonstrates a subtle bug in HTML where JavaScript code attempts to modify a DOM element that does not exist in the HTML structure.  The issue is that the JavaScript code runs and throws a runtime error, but it can be tricky to diagnose if you are not closely inspecting the console or network logs. 

The `bug.html` file contains the erroneous code. The `bugSolution.html` file provides the corrected code.

## Bug Description

The bug is in the JavaScript code within the `bug.html` file. The script attempts to change the `innerHTML` of an element with the ID `nonExistentElement`.  However, no element with that ID exists in the HTML. This results in a JavaScript error, and the intended change is not made.

## Solution

The solution, in `bugSolution.html`, involves verifying that the element actually exists before attempting to modify it. This is accomplished by first retrieving the element using `getElementById`.  If the element doesn't exist, `getElementById` returns `null`.  A simple `if` check prevents an error from occurring.