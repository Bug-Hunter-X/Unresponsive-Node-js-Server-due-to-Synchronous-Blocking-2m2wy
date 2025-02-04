# Unresponsive Node.js Server due to Synchronous Blocking

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, making the server unresponsive. The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The `bug.js` file creates an HTTP server.  A synchronous `while` loop simulates a long-running task that keeps the CPU busy for 5 seconds. During this time, the server cannot handle any other requests, leading to unresponsiveness.

## Solution

The `bugSolution.js` demonstrates how to solve this by using asynchronous operations (asynchronous functions) and callbacks or promises. This prevents the event loop from being blocked.