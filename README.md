# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook:  an infinite loop caused by a missing dependency in the dependency array.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

## Problem
The original code attempts to log the count on every render.  However, omitting `count` from the dependency array causes the effect to run continuously, leading to an infinite loop of console logs and potential performance issues.

## Solution
The solution includes `count` in the dependency array. Now, the effect only runs when the `count` value changes, resolving the infinite loop.