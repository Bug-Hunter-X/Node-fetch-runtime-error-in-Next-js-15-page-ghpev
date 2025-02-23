# Next.js 15 node-fetch Runtime Error

This repository demonstrates a runtime error encountered when using `node-fetch` within a Next.js 15 page component.  The issue arises because `node-fetch` is designed for server-side environments, and Next.js's client-components render on the client-side using browser APIs.

## Problem

Attempting to use `node-fetch` directly in a page component leads to a `TypeError: fetch is not a function` error in the browser. This is because the browser's built-in `fetch` API is different from `node-fetch`.

## Solution

The solution involves using the browser's built-in `fetch` API or a suitable alternative like `cross-fetch` which handles client-side and server-side environments effectively. This corrected version replaces `node-fetch` and makes the necessary adjustments to use the client-side `fetch` API.