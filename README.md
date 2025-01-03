# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common but easily overlooked error in React: forgetting the return statement in a `useEffect` hook.  This can lead to memory leaks and unexpected behavior if the component unmounts before the effect's cleanup has finished.

## Bug Description

The `bug.js` file contains a `MyComponent` that uses `useEffect` to log a message when the component mounts. However, it's missing a return statement containing a cleanup function. This means that any asynchronous operations or subscriptions within the effect will not be cleaned up when the component unmounts.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  A cleanup function is returned, ensuring that any necessary cleanup operations are performed when the component unmounts.