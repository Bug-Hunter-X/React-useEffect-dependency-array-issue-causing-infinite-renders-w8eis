# React useEffect Dependency Array Issue

This repository demonstrates a common mistake when using the `useEffect` hook in React: forgetting to include all variables used inside the effect in its dependency array.  This leads to infinite rerenders.

## Bug
The `bug.js` file contains a `MyComponent` that uses `useState` and `useEffect`.  The `useEffect` hook attempts to log the current count to the console after every render. However, the `count` variable is not included in the dependency array which causes the component to render repeatedly.

## Solution
The `bugSolution.js` file fixes the issue by adding `count` to the dependency array of `useEffect`.  Now, the effect only runs when the `count` value changes.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the button.