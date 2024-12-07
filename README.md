# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common issue with the React `useEffect` hook: unnecessary re-renders caused by an incorrectly specified dependency array.  The `useEffect` hook should only re-run when its dependencies change, and failing to specify these correctly can lead to performance issues and unexpected behavior.

The `bug.js` file shows the incorrect implementation, where the `useEffect` hook re-renders even when the `count` state variable hasn't actually changed.  This can happen if additional variables are referenced within the `useEffect` callback. The `bugSolution.js` file provides a corrected implementation.