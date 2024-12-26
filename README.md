# Express.js Route Handler Error
This repository demonstrates a common error in Express.js route handlers: lack of error handling for invalid input.  Specifically, the `/users/:id` route does not handle cases where `:id` is not a valid integer.

## Bug
The `bug.js` file contains the erroneous code.  It attempts to parse the `userId` as an integer directly without any validation or error handling. If a non-numeric `userId` is provided, this leads to an error or unexpected behavior.

## Solution
The `bugSolution.js` file provides a corrected version. This solution includes comprehensive error handling to validate the `userId` before attempting to access the user data, gracefully handling the case where the user is not found or the ID is invalid.

## How to Reproduce
1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `node bug.js` and then access the route with a non-numeric id in the URL to see the error. 
4. Run `node bugSolution.js` and test to see how the error is correctly handled.