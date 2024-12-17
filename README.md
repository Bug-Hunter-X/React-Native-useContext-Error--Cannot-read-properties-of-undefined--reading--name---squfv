# React Native useContext Error: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common error encountered when using React Native's `useContext` hook. The error, "Cannot read properties of undefined (reading 'name')", arises when a component attempts to access context outside of a provider.

## Problem

The `MyComponent` attempts to read the context value within its render method but fails when no context provider is available in the render tree above it.  This is usually observed in test environments or if the component's rendering is not managed correctly within the context provider.

## Solution

The solution involves wrapping `MyComponent` within a `MyContextProvider` which provides the context value that the component consumes.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Try to run the test file or render the component without proper context wrapping.  You should see the described error.
4. Uncomment the lines that correctly wrap the component with `MyContextProvider` in either the test file or render to view the correct solution.

## Technologies Used

* React Native
* Jest (for testing)