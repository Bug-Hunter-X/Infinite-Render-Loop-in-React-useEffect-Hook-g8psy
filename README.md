# React useEffect Hook Dependency Array Issue

This repository demonstrates a common error when using the `useEffect` hook in React: an infinite render loop caused by incorrectly specifying the dependency array.

## Bug
The `bug.js` file contains a component that uses the `useEffect` hook to log the current count.  However, the dependency array is missing the `count` state variable. This causes the effect to run after every render, triggering a continuous loop.

## Solution
The `bugSolution.js` file provides a corrected version of the component. Adding `count` to the dependency array ensures that the effect only runs when the value of `count` changes.