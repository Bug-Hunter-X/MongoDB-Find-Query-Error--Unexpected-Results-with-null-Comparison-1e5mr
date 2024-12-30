# MongoDB Find Query Bug: Unexpected Results with Null Comparison

This repository demonstrates a common error when using MongoDB's find query with null values. The incorrect use of `$eq: null` can lead to unexpected results when searching for fields that are missing or undefined. The correct method uses `$exists: false`.

## Bug Description
The provided code attempts to find documents where a specific field is null. However, it incorrectly uses `$eq: null`, which doesn't accurately identify missing fields. This results in incorrect query results. The solution demonstrates the correct way to find documents where a field does not exist.

## How to reproduce
1.  Clone this repository
2.  Replace `YOUR_MONGODB_URI` in `bug.js` with your MongoDB connection string
3.  Run `bug.js` to observe the incorrect results.
4.  Run `bugSolution.js` to see how to correctly identify documents where a field is missing.

## Solution
The solution replaces `$eq: null` with `$exists: false` within the MongoDB find query to correctly identify documents where the field is not present.