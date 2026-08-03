# Add Back to the Moment Deep Link

- State: review
- Scope: Add a URL suffix that opens the existing quote page directly on Portrait Photography and the Back to the Moment package without changing the default main-page selection.

## Acceptance Criteria

- The main URL continues to open with Event Photography selected.
- The `#back-to-the-moment` suffix opens Portrait Photography with Back to the Moment selected.
- The fixed CAD $288 package rules and local-only restriction remain active through the deep link.
- English, Chinese, and Filipino language switching preserves the selected package.
- Both HTML entry points remain synchronized.

## Eval / Test Commands

- Run `node --check` on the inline JavaScript.
- Verify default and suffixed URLs in a browser.
- Run `git diff --check` and compare both HTML entry points.

## Progress

- Identified hash-based routing as the smallest backward-compatible option for the static GitHub Pages site.
- Added `#back-to-the-moment` handling to both HTML entry points.

## Results

- The default URL opens Event Photography at the unchanged $300 one-hour total.
- The suffixed URL opens Portrait Photography with Back to the Moment selected at the fixed $288 total.
- The deep-linked package hides out-of-city controls and retains the Brandon local-only restriction.
- Switching the deep-linked page to Chinese preserves the package and displays `回到那一刻`.
- Browser console checks reported no errors.
