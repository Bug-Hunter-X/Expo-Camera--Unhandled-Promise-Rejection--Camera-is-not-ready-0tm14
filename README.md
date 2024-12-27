# Expo Camera Initialization Error

This repository demonstrates a common error encountered when using the Expo Camera API: attempting to access camera features before the camera has properly initialized. The `bug.js` file reproduces the issue, while `bugSolution.js` provides a solution.

## Problem

The `bug.js` file attempts to access the camera's state and take a picture immediately after mounting the Camera component.  Before the camera is fully initialized, accessing properties like `isTakingPhoto` results in an error because the camera object is not yet ready.

## Solution

The `bugSolution.js` file corrects this by using the `Camera.State` to ensure the camera is ready before accessing its functionalities.  It utilizes the `onCameraReady` callback to execute the picture-taking action only after the camera initialization is completed.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `expo start` for the bug example.
5. Run `expo start` again for the corrected solution.