# React useEffect Hook with Incorrect Conditional Rendering

This repository demonstrates a common issue in React where incorrect conditional rendering logic is used within the `useEffect` hook, leading to unexpected behavior. The problem lies in how the conditional statement (`if (count > 0)`) is evaluated.

## Bug Description

The provided code intends to log a message whenever the `count` state variable becomes greater than 0. However, the `if` condition inside `useEffect` is only evaluated once per render cycle. If the count becomes greater than 0 during a render cycle, and then decreases to 0 after, the log statement will not be executed during that render cycle, which could lead to bugs and unexpected behavior. 

## Solution

The solution involves using the `count` state in the conditional render, and properly updating the UI to reflect the state changes.