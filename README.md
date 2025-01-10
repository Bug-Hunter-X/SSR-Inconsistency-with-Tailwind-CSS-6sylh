# SSR Inconsistency with Tailwind CSS in Next.js
This repository demonstrates a bug where Tailwind CSS styles are not applied correctly to server-side rendered (SSR) components in Next.js. The issue is specific to components that are dynamically or conditionally rendered.

## Problem
When a component is rendered on the server, the Tailwind directives are not processed, leading to unstyled components on the initial render. Once the client-side hydration occurs, the styles are correctly applied.

## Solution
The solution involves ensuring that Tailwind directives are correctly evaluated during the server-side rendering process. This can be achieved through various techniques, such as using `@apply` directives for direct CSS application or by ensuring that the conditional rendering logic doesn't interfere with Tailwind's processing.