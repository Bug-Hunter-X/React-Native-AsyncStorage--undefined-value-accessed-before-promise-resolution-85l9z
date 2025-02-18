# React Native AsyncStorage: undefined value accessed before promise resolution

This repository demonstrates a common error when working with AsyncStorage in React Native: accessing the retrieved data before the asynchronous operation completes.  The example shows how this leads to an `undefined` value and how to correctly handle the asynchronous nature of AsyncStorage's `getItem` method.

## Problem

The `AsyncStorage.getItem` method is asynchronous.  Attempting to access the value before the promise resolves results in an `undefined` value.

## Solution

The solution involves correctly handling the promise returned by `AsyncStorage.getItem`.  The value should only be accessed within the `.then` block or using `async/await`.

## Setup

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run the app on your emulator or device.