# Split Family Portrait and Gathering Pricing

- State: review
- Scope: Apply the CAD $650 fixed package only to Family Portraits while keeping Family birthday parties, anniversaries, and gatherings at CAD $300 per hour.

## Acceptance Criteria

- Family Portraits / 家庭合照 uses CAD $650 for up to two hours and the approved 30-image package.
- Birthday Parties, Anniversary Celebrations, and Family Gatherings use CAD $300 per hour with editable duration and 20+ standard edited photos per hour.
- English and Chinese labels, totals, review text, copied quote text, and payload metadata agree with the selected subtype.
- Event, Commercial, Portrait, and Back to the Moment behavior remains unchanged.
- Both HTML entry files remain identical.

## Eval / Test Commands

- Check inline JavaScript syntax in both HTML files.
- Run browser assertions for every Family subtype in English and Chinese.
- Recheck Event and Back to the Moment calculations.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Confirmed the current bug: fixed Family pricing is keyed to the whole category rather than the selected subtype.
- Added a subtype-specific Family Portrait package rule and restored hourly behavior for the other three Family types.
- Updated delivery wording and outgoing payload package metadata to match the selected subtype.

## Results

- Inline JavaScript syntax passed for both HTML entry files.
- Browser checks confirmed Family Portraits / 家庭合照 is fixed at two hours and CAD $650 in English and Chinese.
- Browser checks confirmed Birthday Parties, Anniversary Celebrations, and Family Gatherings are editable and total CAD $300 for one hour with 20+ photos per hour.
- Browser checks confirmed Event remains CAD $600 for two hours and Back to the Moment remains CAD $288.
- Payload checks distinguish fixed Family Portraits from hourly Family events.
- Both HTML entry files are identical, and `git diff --check` passed.
