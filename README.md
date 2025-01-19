# Expo AsyncStorage Data Race Condition

This repository demonstrates a common error when using AsyncStorage in Expo: accessing data before it's fully loaded. This can lead to unexpected behavior or crashes in your application.

## The Problem

The `bug.js` file shows the problematic code.  The component attempts to access AsyncStorage data immediately upon mounting, without waiting for the data to be fully loaded.

## The Solution

The `bugSolution.js` file demonstrates the correct approach using `async/await` to ensure the data is loaded before being accessed.  Alternatively, promises can also be used.  Proper error handling is also implemented.

## How to reproduce

1. Clone the repository.
2. Run `npm install`
3. Run `expo start`
4. Observe the console logs and application behavior in both `bug.js` and `bugSolution.js`.

This example highlights the importance of asynchronous programming in React Native and Expo applications.