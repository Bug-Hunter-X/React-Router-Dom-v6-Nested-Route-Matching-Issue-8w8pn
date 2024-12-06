# React Router Dom v6 Nested Route Matching Issue

This repository demonstrates a bug in React Router Dom v6 related to unexpected route matching when using nested routes and a wildcard route ('*').  The wildcard route is incorrectly matching before more specific nested routes.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to a path that should match a nested route (e.g., '/users/1').
5. Observe that the wildcard route ('*') is matched instead of the nested route.

## Expected Behavior

Nested routes should have precedence over the wildcard route when their path matches the URL.

## Actual Behavior

The wildcard route is matching regardless of more specific nested routes.

## Solution

The solution involves re-ordering the routes, ensuring that specific routes are matched before the wildcard route.  This ensures correct route matching.  Please refer to `AppSolution.js` for a corrected implementation.