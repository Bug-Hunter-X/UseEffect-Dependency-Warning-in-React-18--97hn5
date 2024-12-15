# React 18 useEffect Dependency Warning

This repository demonstrates a common warning encountered when upgrading to React 18 or later related to the `useEffect` hook's dependency array.

## The Problem

In React 17 and earlier, omitting dependencies from the useEffect array often worked without warnings.  However, React 18 and beyond have stricter rules.  If a value used within `useEffect` is not listed in the dependency array, you'll get a warning, and the effect may not run at the expected times.

The `bug.js` file shows an example of this.  The `count` variable is used inside the effect but isn't included in the dependency array `[count]`, leading to a warning.

## The Solution

The solution is simple: ensure that all values used within your `useEffect` callback are included in its dependency array. The `bugSolution.js` shows the corrected code.

## How to run

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.