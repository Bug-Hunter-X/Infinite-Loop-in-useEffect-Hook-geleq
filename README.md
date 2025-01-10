# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React applications: an infinite loop caused by the `useEffect` hook.

The `bug.js` file contains a component with a `useEffect` hook that incorrectly depends on the state variable `count`.  This creates a loop where the state is updated constantly, leading to performance issues and potentially crashing the application.

The `bugSolution.js` file provides a corrected version of the component.  This version demonstrates the correct usage of the `useEffect` hook, preventing the infinite loop.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the console and the constantly updating count.
5. Observe the corrected behavior in `bugSolution.js`

## Solution
The solution involves understanding the correct usage of the `useEffect` hook and its dependencies. The `count` variable in the original code should not be a dependency when the count is only updating.  The `useEffect` hook should only run when it is needed to avoid unintended side effects.