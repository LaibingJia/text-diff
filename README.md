# Text Diff

A lightweight, browser-based tool for comparing two pieces of text.
It highlights additions and deletions so you can quickly spot changes.

## Features
- Word-level diffing with whitespace awareness.
- Additions shown in green; deletions shown in red with strikethrough.
- Preserves line numbers and retains the last comparison using `localStorage`.
- Works offline – simply open the HTML file in your browser.

## Usage
1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. Paste the original text on the left and the modified text on the right.
4. Click **Compare** to view differences, or **Clear** to reset.

## Development
The application is a single HTML file and has no build step or external dependencies beyond the `diff` library served via CDN.

Contributions are welcome!
