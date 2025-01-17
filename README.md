# Uncommon HTML Bug: Modifying innerHTML of a Non-Existent Element

This repository demonstrates a subtle bug in HTML/JavaScript that can be difficult to track down.  The issue arises from attempting to modify the `innerHTML` property of a DOM element that doesn't exist yet. This often results in a silent failure, leading to unexpected behavior.

The `bug.html` file contains the erroneous code. The `bugSolution.html` file provides a corrected version.

## Bug Description
The bug involves using `document.getElementById('nonExistentElement').innerHTML = "..."` to change the content of an element with the ID 'nonExistentElement'.  If this element is not present in the HTML document, the script throws no error, but fails silently; the intended change will not occur, potentially leading to confusion and unexpected program state.