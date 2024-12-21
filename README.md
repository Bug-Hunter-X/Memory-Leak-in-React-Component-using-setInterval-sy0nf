# React setInterval Memory Leak

This repository demonstrates a common error in React applications involving the `setInterval` function within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Problem
The `bug.js` file contains a React component that uses `setInterval` to update a count every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.  The interval continues to run even after the component is no longer rendered, consuming resources unnecessarily.

## Solution
The `bugSolution.js` file shows the corrected implementation. The key change is adding a cleanup function within the `useEffect` hook to `clearInterval` when the component unmounts. This ensures that the interval is properly stopped, preventing memory leaks.

## How to reproduce
Clone this repo, and run `npm install` to install the project dependencies. Then, run `npm start` to run the application. Observe that the count continuously increments even after unmounting the component (for the buggy version).

## Contributing
Feel free to open issues or submit PRs.