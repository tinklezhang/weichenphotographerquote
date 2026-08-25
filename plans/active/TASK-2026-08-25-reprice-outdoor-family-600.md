# Reprice Outdoor Family Session to CAD $600

- State: review
- Scope: Change the existing Outdoor Family Session fixed package from CAD $650 to CAD $600 while retaining its maximum two-hour duration and current deliverables.

## Acceptance Criteria

- English rate and summary display CAD $600 and `Up to 2 hours`.
- Chinese rate and summary display CAD $600 and `最多 2 小时`.
- The Outdoor Family Session quote total and payload use CAD $600.
- The two-hour maximum, 30 retouched photos, additional image pricing, travel rules, and all unrelated services remain unchanged.
- Both HTML entry files remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check English and Chinese Outdoor Family Session displays and totals.
- Verify the two-hour duration is fixed and the total is CAD $600.
- Regression-check Studio Portraits, Outdoor Portraits, Parties, and Back to the Moment.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Task created before implementation.
- Changed the Outdoor Family Session fixed rate from CAD $650 to CAD $600.
- Updated the English and Chinese rate labels while retaining `Up to 2 hours` and `最多 2 小时`.
- Preserved 30 retouched photos, additional image pricing, fixed duration, travel rules, and all unrelated packages.

## Results

- Both HTML entry files pass inline JavaScript parsing and remain synchronized.
- English browser check confirmed `CAD $600 · Up to 2 hours`, the disabled two-hour duration, 30 included retouched photos, and a CAD $600 total.
- Chinese browser check confirmed `CAD $600 · 最多 2 小时`, the disabled two-hour duration, 30 included retouched photos, and a CAD $600 total.
- Regression checks confirmed Parties CAD $300, Studio Portraits CAD $200, Outdoor Portraits CAD $300 per hour, and Back to the Moment CAD $288.
- Browser console reported no warnings or errors.
- `git diff --check` passed.
