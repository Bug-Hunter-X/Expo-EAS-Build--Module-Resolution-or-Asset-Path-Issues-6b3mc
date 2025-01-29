# Expo EAS Build: Resolving Module and Asset Path Errors

This repository demonstrates a common issue encountered when using Expo's EAS Build service: errors related to module resolution and asset path handling. These errors often stem from inconsistencies between the project's configuration (package.json, expo.json) and the way assets or modules are referenced in the application code.  The example highlights how incorrect paths or missing dependencies can disrupt the build process.

## Reproducing the Error

1. Clone this repository.
2. Navigate to the project directory.
3. Attempt to build the project using `eas build --profile development`.  You should observe build errors related to missing modules or incorrect asset paths.

## Solution

The `bugSolution.js` file demonstrates the corrected approach. The key is to ensure that:

*   All dependencies are correctly listed in `package.json` and installed.
*   Asset paths in `expo.json` and within the application code are accurate and consistent (relative to the project root).
*   Module imports are correctly resolved (relative paths, or absolute paths via node_modules if necessary).

This example underscores the importance of meticulously checking configurations and paths when using EAS Build to avoid frustrating build failures.