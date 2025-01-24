# React setInterval Memory Leak

This repository demonstrates a common mistake in React when using `setInterval` within a `useEffect` hook, leading to a memory leak. The problem is the lack of a cleanup function to stop the interval when the component unmounts.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it's missing the cleanup function in the `useEffect` hook, causing the interval to continue running even after the component is unmounted, leading to a memory leak.

## Solution

The `bugSolution.js` file provides a corrected version of the component. It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, effectively preventing the memory leak.