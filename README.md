# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug occurs when the dependency array is omitted or incorrectly specified, leading to an infinite render loop.

## Bug Description

The provided `MyComponent` uses `useEffect` to log the current count to the console. However, the dependency array is missing. This means the effect runs on every render, causing a new state update, triggering another render, and so on.

## Solution

The solution involves correctly specifying the dependency array in `useEffect`.  By including `[count]` the effect will only run when `count` changes, preventing the infinite loop.
