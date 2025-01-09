# Unhandled routes in React Router v6

This repo demonstrates a common issue in React Router v6 where unexpected behavior occurs when a route does not match any defined routes.  The application lacks a catch-all route to handle these cases, resulting in unexpected rendering or errors.

## Problem

The `App.js` file shows a basic React Router setup with routes for `/` and `/about`.  However, navigating to any other path (e.g., `/invalid`) will not produce a 404 or any other defined fallback.  This could leave the user with a blank screen or a routing error in the console depending on your React Router configuration.

## Solution

`AppSolution.js` provides the solution.  By adding a `Route` with a wildcard path (`/*`), we can create a catch-all route to handle any unhandled path.  This ensures a better user experience by providing a 404 page or another suitable fallback.
