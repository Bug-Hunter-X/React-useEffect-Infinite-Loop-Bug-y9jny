# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrectly updating state within a useEffect hook that has an empty dependency array.  The provided code implements a simple counter, but because the state update within the useEffect immediately causes a re-render, and because the useEffect has an empty dependency array and will run infinitely.

## Bug Description
The bug lies in the `useEffect` hook's callback function. Updating the `count` state within this function, when the dependency array is empty, creates an infinite loop. Each state update triggers a re-render, and the `useEffect` is executed repeatedly.

## Solution
The solution involves correctly managing dependencies within the useEffect hook.