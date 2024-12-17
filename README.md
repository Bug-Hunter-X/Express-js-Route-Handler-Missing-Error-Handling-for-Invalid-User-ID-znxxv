# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for errors. If the `id` parameter is not a valid integer, the code will throw an error or return unexpected results.

## Bug

The `bug.js` file contains the erroneous code. The issue lies in the lack of input validation and error handling for the `userId` parameter.  If a non-numeric value is provided, `parseInt(userId)` will return `NaN`, and the `find()` method may behave unpredictably.  A more robust solution is needed to handle potential errors and provide informative error messages.

## Solution

The `bugSolution.js` file provides a corrected version of the code that includes comprehensive error handling.  This improved version checks if `userId` is a valid integer and handles the case where a user with the provided ID is not found.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Install the required packages using `npm install express`.
4. Run `node bug.js` (or `node bugSolution.js`) to see the output.