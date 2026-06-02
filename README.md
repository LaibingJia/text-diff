# Text Diff

A browser-based WinDiff-style text comparison tool with optional AI-assisted review planned for future releases.

Text Diff helps people compare two versions of text quickly without installing a desktop application. It runs as a static web page, highlights word-level changes, preserves line numbers in the result, and keeps the deterministic diff local in the browser.

Live demo: <https://laibingjia.github.io/text-diff/>

## Why this project exists

Most diff tools show what changed, but ordinary users can still struggle to understand what the change means. Text Diff starts with a simple visual comparison interface and is designed to grow toward optional AI explanations that summarize edits, group related changes, and flag review risks.

## Use cases

Text Diff is useful when comparing:

- Contract or policy drafts.
- Paper, thesis, or report revisions.
- Code snippets and configuration files.
- Email drafts or meeting notes.
- Translation revisions.
- Any two text versions where a lightweight browser tool is enough.

## Features

- Word-level diffing with whitespace awareness.
- Additions shown in green; deletions shown in red with strikethrough.
- Line-numbered diff output.
- `localStorage` restore for the last comparison on the same device.
- Vendored `diff` library so the app can run after download without a CDN request.
- Static HTML deployment with no build step.

## Privacy model

The current app compares text locally in the browser and does not send pasted text to a server or API. The most recent comparison is stored in `localStorage` for convenience and can be removed with **Clear**.

Future AI-assisted review features will be optional and must require explicit user action before any text is sent to an API. See [`PRIVACY.md`](PRIVACY.md) for details.

## Usage

1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. Paste the original text on the left and the modified text on the right.
4. Click **Compare** to view differences, or **Clear** to reset stored text and output.

## Development

The application is a static HTML page. The browser diff dependency is vendored at `vendor/diff.min.js` so the app does not depend on a CDN at runtime. A GitHub Actions smoke test verifies that the vendored renderer can produce line-numbered additions and deletions.

To test changes manually:

1. Open `index.html`.
2. Compare sample text with multiple lines, additions, and deletions.
3. Refresh the page to confirm the previous comparison is restored.
4. Click **Clear** to confirm text and saved output are removed.

## Roadmap

The roadmap focuses on making Text Diff reliable, maintainable, accessible, and eventually AI-assisted while keeping local deterministic diffing available for everyone. See [`ROADMAP.md`](ROADMAP.md).

## Contributing

Contributions are welcome. Please read [`CONTRIBUTING.md`](CONTRIBUTING.md) before opening issues or pull requests. Issue templates are available for bug reports, feature requests, and optional AI review ideas.

## Security

Please report security or privacy concerns using the guidance in [`SECURITY.md`](SECURITY.md).

## License

Text Diff is released under the MIT License. See [`LICENSE`](LICENSE).
