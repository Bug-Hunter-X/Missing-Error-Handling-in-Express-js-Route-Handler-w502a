# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The provided code attempts to fetch a user based on their ID, but lacks proper error handling if the ID is not a number or if the user is not found.  This can lead to application crashes or unexpected behavior.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides a corrected version with appropriate error handling.

## Bug Description

The primary issue is the lack of error handling when parsing the user ID from the request parameters. If the ID is not a valid integer, `parseInt(userId)` will return `NaN`, leading to potential issues when searching for the user.  The code also does not handle the case where no user matches the given ID.