# Unhandled 404 Error in Express.js Route with req.params

This repository demonstrates a common but easily overlooked error in Express.js: failing to explicitly handle 404 (Not Found) errors when using parameters in routes.  Improper error handling can lead to unexpected behavior for the client and potential vulnerabilities.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides the solution.

## Bug
The bug lies in the lack of explicit 404 error handling when a user with the specified ID isn't found.  Express.js won't automatically return a 404; instead, it might return an empty response or an internal server error if other errors occur in the code. 

## Solution
The `bugSolution.js` file demonstrates the proper way to handle this scenario by explicitly checking if the user is found and sending a 404 response with a descriptive message if not.