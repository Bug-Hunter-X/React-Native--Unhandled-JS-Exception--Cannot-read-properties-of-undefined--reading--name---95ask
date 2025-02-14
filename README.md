# React Native: Unhandled JS Exception: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common error in React Native applications: attempting to access a state variable before it has been initialized. This typically happens when dealing with asynchronous operations like API calls or database interactions.

## The Problem

The `bug.js` file shows incorrect code where the component renders before the `data` state variable is populated from an API call.  Accessing `data.name` before the API call completes results in an `undefined` value, causing the error.

## The Solution

The `bugSolution.js` file provides a corrected version.  It uses optional chaining (`?.`) and nullish coalescing (`??`) operators to gracefully handle the case where `data` is undefined before the API call is complete.  This prevents the runtime error.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app.
4. Observe the error with `bug.js` and the corrected behavior with `bugSolution.js`.