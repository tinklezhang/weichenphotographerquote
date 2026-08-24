# Restructure Portrait Packages

- State: review
- Scope: Consolidate Professional Headshots and Personal Portraits into Studio Portraits, add an Outdoor Portraits hourly service, and preserve the approved Back to the Moment and Couples Portraits options.

## Acceptance Criteria

- Portrait Photography options are `Back to the Moment`, `Studio Portraits`, `Outdoor Portraits`, and `Couples Portraits` in English, with corresponding Chinese labels.
- Studio Portraits is CAD $200 for 20–30 minutes and includes two professionally retouched digital photos.
- Outdoor Portraits is CAD $300 per hour with a one-hour minimum and includes five professionally retouched digital photos per hour.
- Additional Studio retouches remain CAD $20 each; no physical print is included with Studio Portraits.
- Back to the Moment and Couples Portraits retain their current rules unless required for label routing.
- Quote summaries and calculations use the correct package-specific prices and delivery quantities.
- Both HTML entry files remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check English and Chinese Studio Portraits and Outdoor Portraits displays and summaries.
- Confirm Studio totals CAD $200 and Outdoor Portraits totals CAD $300 for one hour and CAD $600 for two hours.
- Regression-check Back to the Moment and Couples Portraits.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Task created before implementation.
- Replaced Professional Headshots and Personal Portraits with one Studio Portraits option.
- Added Outdoor Portraits as a CAD $300 hourly service with five professionally retouched digital photos per hour.
- Added stable package values so Studio, Outdoor, Couples, and Back to the Moment use separate calculation paths.
- Preserved Couples Portraits as a Studio-priced option and preserved Back to the Moment unchanged.

## Results

- Both HTML entry files pass inline JavaScript parsing and remain synchronized.
- English and Chinese Studio Portraits checks confirmed CAD $200, 20–30 minutes, and two retouched digital photos.
- English and Chinese Outdoor Portraits checks confirmed CAD $300 for one hour with five photos and CAD $600 for two hours with ten photos.
- Regression checks confirmed Couples Portraits remains CAD $200 and Back to the Moment remains CAD $288.
- Browser console reported no warnings or errors.
- `git diff --check` passed.
