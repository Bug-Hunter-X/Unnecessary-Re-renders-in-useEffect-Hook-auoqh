# Unnecessary Re-renders in useEffect Hook

This example demonstrates a common performance issue in React applications involving the `useEffect` hook.  The `useEffect` hook, without a dependency array, runs after every render, leading to unnecessary re-renders and potential performance bottlenecks. The solution shows how to add a dependency array to fix this problem.

## Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the count after every render.  This is inefficient. 

## Solution
The `bugSolution.js` file provides a corrected version where the dependency array `[count]` ensures that the `useEffect` hook only runs when `count` changes.