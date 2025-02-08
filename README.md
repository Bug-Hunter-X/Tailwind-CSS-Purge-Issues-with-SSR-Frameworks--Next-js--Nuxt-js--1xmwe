# Tailwind CSS Purge Issues with SSR Frameworks

This repository demonstrates a common issue encountered when using Tailwind CSS with server-side rendering (SSR) frameworks like Next.js or Nuxt.js.  The problem arises from Tailwind's purge functionality failing to remove all unused styles, leading to significantly larger CSS bundles than expected.  This is particularly noticeable with dynamically generated classNames.

## Bug Description:

The bug results in bloated CSS output because Tailwind CSS cannot accurately identify all the classes that are actually used during SSR. This is mainly because of dynamic class names which make static analysis complicated.   The `bug.js` file demonstrates this problem. 

## Solution:

The `bugSolution.js` file presents a solution utilizing different approaches to address this problem: more explicit class names, proper usage of purge options, and potentially adopting an alternative strategy like `@apply` for specific cases.

## How to Reproduce:

1. Clone the repository.
2. Install dependencies: `npm install`.
3. Run the application (instructions may vary based on the framework used).
4. Observe the size of the generated CSS file.  It will be larger than it should be, demonstrating the issue.