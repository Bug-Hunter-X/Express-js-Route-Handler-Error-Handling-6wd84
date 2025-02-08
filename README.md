# Express.js Route Handler Error Handling
This repository demonstrates a common error in Express.js route handlers and provides a solution.

## Bug
The `bug.js` file contains an Express.js route handler that fetches user data based on the user ID. If no user is found, it returns a 404 status code with a 'User not found' message. However, this approach has an issue: it doesn't handle potential errors during the database query itself.  If an error happens while attempting to fetch user data from the database (e.g., database connection issues, query errors), this code will crash the application.  This error is not gracefully handled.

## Solution
The `bugSolution.js` file demonstrates an improved approach using try-catch blocks and more robust error handling to prevent the application from crashing when there are errors fetching or finding a user.