# Express.js 404 Error Handling in Route Parameters

This repository demonstrates a common issue in Express.js applications: improper handling of 404 errors when accessing route parameters. Specifically, the example shows how failing to check for the existence of a user before sending a response can lead to unexpected behavior or crashes.

## Bug

The `bug.js` file contains an Express.js route handler that fetches user data based on an ID passed as a route parameter.  If the user ID is not found, the code doesn't explicitly handle this scenario, which can lead to errors or inconsistent responses.

## Solution

The `bugSolution.js` demonstrates the correct way to handle this scenario.  It explicitly checks if `userData` exists before sending the response. If the user is not found, it sends a proper 404 Not Found response.