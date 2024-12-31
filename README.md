# Expo Linking.getInitialURL() returns null inconsistently on Android

This repository demonstrates a bug in Expo's `Linking` API where `getInitialURL()` returns `null` on Android devices even when a deep link is successfully opened. This behavior is inconsistent and makes it difficult to reliably handle the initial application launch with a deep link.

The `bug.js` file showcases the problem, while `bugSolution.js` offers a potential workaround involving checking for the URL multiple times, leveraging `addListener` for more robust handling of deep link resolution.

## Steps to Reproduce

1. Clone this repository.
2. Run the app on an Android emulator or device.
3. Open a deep link intended for the app (as defined in the `bug.js` file).
4. Observe that `getInitialURL()` might return `null` even after a successful link launch.

## Workaround

The `bugSolution.js` provides a more reliable method to handle deep links by using `addListener` which provides a more robust way to handle the event.