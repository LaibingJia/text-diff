# Privacy

Text Diff is designed to run locally in the browser.

## Current behavior

- Text comparison happens in the user's browser.
- The app stores the most recent comparison in `localStorage` so the page can restore it after refresh.
- The vendored diff library is loaded from this repository, not from a CDN.
- The current app does not send pasted text to a server or API.

## Local storage

The browser may retain the old text, new text, and rendered diff result on the same device. Use **Clear** to remove the saved comparison from `localStorage`.

## Planned AI features

Future AI-assisted review features will be optional. If a feature needs to send text to an API, it should:

1. Explain what data will be sent.
2. Require the user to explicitly start the AI review.
3. Keep the deterministic local diff available without AI.
4. Provide guidance for users comparing sensitive or confidential text.
