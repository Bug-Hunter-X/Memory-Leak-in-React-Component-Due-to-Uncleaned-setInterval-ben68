# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug Description

The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in the interval continuing to run, consuming resources even after the component is no longer visible.

## Solution

The solution involves clearing the interval in the cleanup function of the `useEffect` hook, ensuring that it stops when the component unmounts.