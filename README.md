# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite loop caused by an incorrectly used `useEffect` hook. The `useEffect` hook, without dependencies, rerenders infinitely, leading to performance issues and potential crashes.

## Bug Description

The `MyComponent` function uses `useState` to track a count. The `useEffect` hook logs the count to the console after every render.  Because the `useEffect` hook lacks a dependency array, it runs after every render, creating an infinite loop.

## Solution

The solution involves adding a dependency array to the `useEffect` hook.  The dependency array specifies that the effect should only run when the `count` variable changes.