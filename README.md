# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake in React: using `setInterval` within a `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## Solution
The `bugSolution.js` file provides a corrected version of the component. It uses the return value of `useEffect` to clear the interval when the component is unmounted, preventing memory leaks.