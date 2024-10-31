# Expo Router Entry.js Issue Reproduction

This repository demonstrates the `_lruCache is not a constructor` error occurring in the metro bundle phase of development build.

## Environment

- Expo SDK: 52.0.0-preview.18
- expo-router: 4.0.0-preview.11
- expo-dev-client: 5.0.0-preview.5
- React Native: 0.76.1

## Steps to Reproduce

1. Install dependencies

```bash
npm install
```

2. Build development client

3. Start the development server

4. Open the app on your device

## Expected Behavior

The app should bundle without issues

## Actual Behavior

Metro bundling fails with the following error:

```
iOS Bundling failed 7ms
node_modules\expo-router\entry.js: [BABEL] node_modules\expo-router\entry.js: *lruCache is not a constructor
```

## Additional Information

- This issue occurs during the Metro bundling phase
- The development build itself completes successfully
- This seems to be a babel configuration issue specific to expo-router's entry point
