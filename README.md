# React useEffect Closure Issue
This repository demonstrates a common issue related to closures within React's useEffect hook when using setInterval. The problem arises when trying to log or update state based on a value captured within the useEffect's callback, as the value may change before the setInterval function executes.

## Problem
The provided `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook to log the current count every second. However, due to closure, the logged value of `count` is always the most recent value at the time `setInterval` runs, not its value when the effect first started.

## Solution
The `bugSolution.js` file presents a solution using functional update with `setCount`. This ensures that the correct value of `count` is used within the `setInterval` callback, addressing the closure problem.
