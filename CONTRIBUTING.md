# Contributing

Thanks for your interest in improving Text Diff.

## Project goals

Text Diff aims to be a simple, browser-based WinDiff-style text comparison tool. The deterministic diff should remain local, lightweight, and easy to run. Optional AI features should help users understand changes without making local comparison dependent on external services.

## Development setup

No build step is required.

1. Clone the repository.
2. Open `index.html` in a modern browser.
3. Make changes to `index.html`, documentation, or vendored assets.
4. Test by comparing sample text, refreshing the page, and using **Clear**.

## Contribution ideas

Good first contributions include:

- Accessibility improvements.
- Keyboard shortcuts.
- Exporting diff output as HTML or plain text.
- Ignore-whitespace options.
- Browser smoke tests.
- Documentation examples.
- Privacy controls for future AI-assisted review.

## Pull request expectations

- Keep the app usable as a static page.
- Do not add network calls for normal local comparison.
- Document any behavior that stores or sends user-provided text.
- Keep UI changes clear and accessible.
