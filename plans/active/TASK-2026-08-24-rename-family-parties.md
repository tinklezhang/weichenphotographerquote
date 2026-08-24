# Rename Family Gatherings to Parties

- State: review
- Scope: Rename the Family Photography hourly service from `Family Gatherings` to `Parties`, with the Chinese label `派对摄影`, without changing pricing, delivery quantities, or calculations.

## Acceptance Criteria

- The English photography type displays `Parties`.
- The Chinese photography type displays `派对摄影`.
- The selected service name in the quote summary uses the updated label.
- The CAD $300 hourly rate, 20–30 edited photos per hour, evening surcharge, travel behavior, and all calculations remain unchanged.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check the English and Chinese Family Photography selection and quote summary.
- Confirm the one-hour total remains CAD $300.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Task created before implementation.
- Renamed the English hourly Family Photography option from `Family Gatherings` to `Parties`.
- Renamed the corresponding Chinese option from `家庭聚会` to `派对摄影`.
- Preserved all pricing, delivery, travel, and surcharge logic.

## Results

- Both HTML entry files pass inline JavaScript parsing and remain synchronized.
- English browser check confirmed `Family Photography — Parties`, CAD $300 for one hour, and 20+ photos.
- Chinese browser check confirmed `家庭摄影 — 派对摄影`, CAD $300 for one hour, and 20+ photos.
- Browser console reported no warnings or errors.
- `git diff --check` passed.
