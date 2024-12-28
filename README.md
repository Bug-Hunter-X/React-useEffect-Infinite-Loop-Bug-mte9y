# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by omitting dependencies from the dependency array.

## Bug Description
The `MyComponent` component uses `useState` to track a count. The `useEffect` hook logs the count to the console. However, because `count` is not included in the dependency array, the effect runs after every render, leading to an infinite loop and causing the browser to freeze.

## Bug Solution
The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the value of `count` changes.