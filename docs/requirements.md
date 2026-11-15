# Requirements and acceptance scope

## Primary flows

- A visitor can start the complete edit without signing in.
- Search and mood selection narrow the same catalog, with a visible empty result state.
- Playback survives view changes.
- A visitor can pause, seek, skip, repeat and shuffle.
- A visitor can save tracks and return after reload.
- Queue order can be reviewed, edited and locked.
- Named sessions preserve original-track order after reload.
- Local audio plays without server upload and is clearly session-only.
- The interface adapts to phone, tablet and desktop sizes.
- Figma offers editable layouts, variables, reusable controls and connected mobile states.

## Non-goals

Commercial music licensing service, account authentication, social features, recommendation models, synchronized libraries, offline downloads, subscriptions and streaming infrastructure.

## Release checks

Run `npm test`, verify static asset references, check each bundled audio file decodes, exercise key flows in the live browser, inspect desktop and phone layouts, and record the actual scope of manual testing in validation.md. Do not infer usability or accessibility compliance from these checks.
