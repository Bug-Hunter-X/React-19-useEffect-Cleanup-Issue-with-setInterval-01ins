# React 19 useEffect Cleanup Issue with setInterval

This repository demonstrates a common error in React 19's `useEffect` hook when using `setInterval` without proper cleanup.  Forgetting to return a cleanup function from `useEffect` can lead to memory leaks and unexpected behavior.  The example uses `setInterval` to update a counter every second.  Without the cleanup function, multiple intervals continue to run, resulting in performance issues and the component not unmounting properly.

## Bug

The `bug.js` file contains the buggy code.  The `setInterval` function is used without a cleanup function, leading to memory leaks.

## Solution

The `bugSolution.js` file demonstrates the correct approach. The returned cleanup function from the `useEffect` hook ensures that the `setInterval` is cleared when the component unmounts or when the dependencies change.