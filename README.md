# React Router Dom Unexpected Routing Behavior
This repository demonstrates a common issue encountered when using React Router Dom v6 and above. The problem arises from unexpected routing behavior when navigating to a path that is a substring of another defined path.  This can lead to unexpected component rendering.

## Issue Description
The example showcases how a path like `/contact` is not matched correctly if a path like `/contact-us` is also defined earlier in the `Routes` component. The application may render the `/contact-us` component instead of `/contact` when `/contact` is entered in the browser.

## Solution
The solution demonstrates how to avoid this issue using the `useLocation` hook to check the current location and redirect accordingly. Alternatively, using exact matching within the route definitions is more straightforward.  However, if you have many routes, the `useLocation` method offers more flexibility.