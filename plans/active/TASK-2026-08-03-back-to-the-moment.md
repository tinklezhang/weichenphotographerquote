# Add Back to the Moment Portrait Service

- State: merged
- Scope: Add the fixed-price `Back to the Moment｜回到那一刻` black-and-white portrait service to the existing portrait quote flow without changing the pricing behavior of other services.

## Acceptance Criteria

- The service appears under Portrait Photography in English, Chinese, and Filipino views.
- The service name is language-specific: `Back to the Moment` in English/Filipino and `回到那一刻` in Chinese, without mixed-language labels.
- The package is the first option when the Portrait Photography category is selected.
- Selecting it shows: 1–2 people, two finished black-and-white digital portraits, two matching professional 8×10 prints, Brandon, and the short campaign message.
- The package total is fixed at CAD $288 before tax.
- Hourly, evening-surcharge, and out-of-city travel calculations do not apply to this Brandon package.
- The package explicitly states that it is available only for local Brandon sessions, and selecting it clears and hides any out-of-city selection.
- Quote review, copied quote text, and email payload preserve the service name, inclusions, location, and fixed total.
- All other service calculations remain unchanged.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Extract the inline JavaScript and run `node --check`.
- Run focused automated DOM assertions for regular hourly services and the fixed portrait package.
- Exercise the category/service/language interactions in a browser at desktop and mobile widths.
- Run `git diff --check` and review the final diff.

## Progress

- Located the service taxonomy, localization strings, quote calculations, review modal, and email payload in the single-page app.
- Confirmed both HTML entry points were identical before implementation.
- Added the package to Portrait Photography and localized its presentation in English, Chinese, and Filipino.
- Added fixed-package rules to the page, quote text, review modal, and email payload.
- Made the local-only restriction explicit and reset any prior out-of-city selection when the package is chosen.
- Kept both HTML entry points synchronized.

## Results

- Inline JavaScript passed `node --check` with the bundled Node.js runtime.
- Browser checks confirmed the fixed $288 total, package inclusions, Brandon location, language switching, and suppression of hourly, evening, and travel charges.
- Regression check confirmed a regular 2-hour event at 19:00 with default out-of-city travel remains $1,020 ($600 shooting + $120 evening + $300 travel).
- A 390×844 responsive check had no horizontal overflow, and the page produced no console errors.
- `git diff --check` passed and the two HTML entry points are byte-for-byte identical.
- Merged to `main` through pull request #1 for GitHub Pages deployment.
