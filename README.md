# Unhandled Exceptions in Asynchronous Dart Operations

This repository demonstrates a common error in Dart: neglecting to handle exceptions that can occur during asynchronous operations, particularly network requests and JSON parsing.  The `bug.dart` file shows the problematic code.  The `bugSolution.dart` file provides a corrected version with improved error handling.

## Problem

The original code attempts to fetch data from a remote API.  However, it lacks robust error handling. If the network request fails (due to network issues, server errors, etc.) or if the JSON response is malformed, the application might crash silently or behave unexpectedly.

## Solution

The solution involves implementing comprehensive `try-catch` blocks to handle potential exceptions.  The improved code checks the HTTP status code to ensure the request succeeded before parsing the JSON. It also includes a catch block to handle exceptions during both network operations and JSON decoding.  The solution also demonstrates how to optionally rethrow exceptions to handle them at a higher level if needed.