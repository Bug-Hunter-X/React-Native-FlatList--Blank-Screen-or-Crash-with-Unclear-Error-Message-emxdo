# React Native FlatList Bug: Data Structure and Key Extraction Issues

This repository demonstrates a common, yet subtle bug in React Native's FlatList component.  The bug manifests as a blank screen or unexpected crash when the `data` prop is improperly configured or when the `keyExtractor` function fails to provide unique keys for list items.

## The Problem
The primary issue is that the error message generated when encountering this problem is often unclear and doesn't pinpoint the exact source of the error.  This makes debugging challenging.

## Reproducing the Bug
Clone this repository and navigate to the `FlatListBug.js` file.  Run the application.  You'll observe the blank screen/crash.

## Solution
The `FlatListBugSolution.js` file provides a corrected implementation. The key changes include ensuring that:

1. The data prop is a properly formatted array of objects.
2. The `keyExtractor` function extracts a unique key for each item in the data array (e.g., a unique ID).