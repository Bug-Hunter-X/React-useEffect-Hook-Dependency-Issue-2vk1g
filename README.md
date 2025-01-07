# React useEffect Hook Dependency Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can lead to unexpected behavior, often an infinite loop.

## The Problem

The `bug.js` file contains a component with a `useEffect` hook. This hook attempts to log the current count, but omits `count` from the dependency array.  This means the effect runs after every render, regardless of whether `count` has actually changed.

## The Solution

The `bugSolution.js` file corrects this by adding `count` to the dependency array. Now the effect only runs when `count` changes.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output in the browser and how it differs between bug.js and bugSolution.js.
