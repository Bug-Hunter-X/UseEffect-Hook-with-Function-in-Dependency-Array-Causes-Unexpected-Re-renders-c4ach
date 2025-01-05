# useEffect Hook with Function in Dependency Array - React Native Bug

This repository demonstrates a common bug in React Native applications involving the `useEffect` hook and functions within its dependency array.  The issue stems from React's shallow comparison of dependencies; if a function is redefined on every render (even if its logic remains the same), it's treated as a new object, triggering unnecessary re-renders or, in some cases, infinite loops.

## Reproduction

1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to start the application. 
4. Observe the console logs and the counter. The counter will increment indefinitely in the `useEffectBug.js` example due to the function being recreated each render.  The `useEffectSolution.js` demonstrates how to fix this.