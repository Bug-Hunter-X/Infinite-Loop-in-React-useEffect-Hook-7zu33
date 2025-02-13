# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook.  The bug occurs because the state is updated within the `useEffect` function, causing the effect to run repeatedly in an endless cycle.

## Bug Description

The `MyComponent` component uses `useState` to manage a count. The `useEffect` hook attempts to set the count to 10 immediately upon mounting. Because this update triggers another render cycle, the `useEffect` is called again, leading to an infinite loop. 

## Solution

The solution involves correcting the logic within `useEffect` to avoid directly setting the state in a way that leads to infinite loop. Instead, we should use functional updates or conditional logic based on values to prevent this issue.