# React UseEffect setInterval Cleanup Bug
This repository demonstrates a common bug in React applications involving the use of `setInterval` within the `useEffect` hook without proper cleanup.  The bug results in a memory leak and can lead to unexpected behavior, especially when the component unmounts.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts. This leads to the interval continuing to run in the background, even after the component is no longer rendered, eventually causing a memory leak.

## Solution
The solution involves using the return value of `useEffect` to clear the interval when the component unmounts. This ensures that the interval is properly stopped and prevents memory leaks.
