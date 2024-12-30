# React Event Listener Leak

This repository demonstrates a common React bug: event listener leaks caused by missing cleanup functions in `useEffect` hooks.

The `bug.js` file contains a component that adds an event listener but fails to remove it when the component unmounts, leading to memory leaks and potential unexpected behavior.

The `bugSolution.js` file provides the corrected code with proper cleanup using a return statement within the `useEffect` hook.

## How to reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and interact with the component to see the count increase. Note that even after unmounting and remounting the component, the event listener may still be active.
