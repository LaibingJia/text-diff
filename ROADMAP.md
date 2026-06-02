# Roadmap

Text Diff is an early-stage, browser-based text comparison tool inspired by WinDiff. The near-term goal is to keep deterministic comparison local and easy to use while building a path toward optional AI-assisted review.

## v0.1: Reliable local diff foundation

- Keep the app usable as a static HTML page with no build step.
- Vendor the browser diff dependency so the tool works after download without a CDN request.
- Preserve line numbers in rendered results.
- Improve accessibility for keyboard users and screen readers.
- Add smoke tests for loading the page, entering text, comparing, clearing, and restoring from `localStorage`.

## v0.2: Maintainer quality and contribution workflow

- Add issue templates for bugs, accessibility problems, and feature proposals.
- Add a lightweight CI workflow for static checks and browser smoke tests.
- Publish tagged releases with release notes.
- Document supported browsers and privacy expectations.
- Add examples for common use cases: contracts, papers, email drafts, code snippets, configuration files, and translations.

## v0.3: Optional AI-assisted review

AI features must be opt-in. The local diff should remain free, deterministic, and usable without sending text anywhere.

Planned AI features:

- Plain-language summaries of what changed.
- Semantic grouping of related edits.
- Risk flags for potentially important changes in legal, configuration, or policy text.
- Reviewer checklists tailored to the detected change type.
- Explanations of meaningful differences when visual red/green highlighting is not enough.

## Privacy principles for AI work

- Do not send text to an API by default.
- Clearly label any feature that sends user-provided text to a third-party service.
- Require an explicit user action before AI review starts.
- Provide guidance for sensitive text and local-only workflows.
