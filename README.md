# Intermittent PurgeCSS Issue: Removing Whitelisted Responsive Tailwind Classes

This repository demonstrates an uncommon bug encountered with PurgeCSS and Tailwind CSS.  The issue involves PurgeCSS removing essential CSS classes that are explicitly whitelisted, particularly those related to responsive design. The problem occurs inconsistently, making it difficult to debug.

## Bug Description

Despite including specific Tailwind CSS classes in the PurgeCSS whitelist, these classes are occasionally removed during the build process. This leads to unexpected styling issues on certain screen sizes or devices.

## Reproduction Steps

1. Clone this repository.
2. Run the build process (details provided in the `build.sh` script). Note that you will likely need to install dependencies of the project.
3. Observe the generated CSS file and note the missing responsive classes.

## Potential Causes

- Potential conflicts between PurgeCSS configuration and the way Tailwind generates responsive classes.
- Unclear reasons for the inconsistent behavior of PurgeCSS (may relate to caching or other internal issues).

## Solution

The provided solution (bugSolution.js) addresses the issue using an alternative approach to whitelisting and potentially enhancing PurgeCSS's configuration to resolve conflicts.  See `bugSolution.js` for implementation details.