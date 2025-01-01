# React Router v6 Catch-All Route Issue

This repository demonstrates a common issue with React Router v6's catch-all route (`path="/*"`).  The problem arises when the catch-all route is placed after more specific routes, causing it to intercept all navigation attempts regardless of the defined path. 

## Issue Description

The `App.js` file contains a simple React Router setup with three routes: home, about, and a catch-all not found route.  Expected behavior is that navigating to `/` or `/about` shows the respective components, and any other path shows the 404 component. However, the catch-all route intercepts all navigation, and only the 404 page is shown.

## Solution

The solution (`AppSolution.js`) moves the catch-all route to be the last route defined within the `Routes` component. By placing the catch-all at the end, React Router correctly handles routes before it first.  This ensures that specific routes are matched before falling back to the catch-all route.