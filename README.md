# React Router Catch-All Route Conflict

This repository demonstrates a common issue with React Router's catch-all route (`/*`). When placed before other routes, it intercepts all navigation attempts, preventing access to other routes in the application. The solution involves placing the catch-all route as the last route definition within the `Routes` component.

## Steps to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/about`. It should lead to the '404 Not Found' page due to the incorrect route order.

## Solution

The solution involves moving the catch-all route (`/*`) to be the last route defined in the `Routes` component. This ensures that it only matches paths not matched by other routes.

## Additional Notes

- Ensure that you are using the latest version of `react-router-dom`.
- Carefully consider the order of your routes to avoid unintended conflicts.