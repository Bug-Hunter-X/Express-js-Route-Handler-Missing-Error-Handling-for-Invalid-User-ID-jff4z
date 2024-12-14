# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  The example shows a route that fetches a user by ID.  The code attempts to parse the ID as an integer but fails to handle potential errors such as non-numeric IDs, leading to crashes or unexpected behavior.  The solution shows how to add robust error handling to prevent these issues.

## Bug
The `bug.js` file contains the erroneous code.  The `parseInt()` function may throw an error or return `NaN` if the `userId` is not a valid number, causing the route to fail without proper error handling.

## Solution
The `bugSolution.js` file demonstrates the corrected code.  It uses `isNaN()` to check if the parsed `userId` is a number. If not, it gracefully returns an error response, preventing unexpected crashes and providing informative feedback to the client.  This addition provides improved stability and user experience.
