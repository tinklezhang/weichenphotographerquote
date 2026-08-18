# Simplify Family Gathering Types

- State: merged
- Scope: Consolidate the overlapping Family Photography hourly options into one Family Gatherings option while preserving the separate Family Portrait package and every other service.

## Acceptance Criteria

- Family Photography offers only Family Portraits and Family Gatherings.
- Family Gatherings remains CAD $300/hour with a one-hour minimum.
- Family Portraits retains its existing fixed CAD $650 package.
- Other services and calculations remain unchanged.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check the Family Photography option list, Family Gatherings one-hour minimum, and Family Portrait fixed price.
- Regression-check Studio Portrait and Event Photography pricing.
- Run `git diff --check` and verify both HTML files are identical.

## Progress

- Confirmed Birthday Parties, Anniversary Celebrations, and Family Gatherings currently share the same hourly behavior.
- Consolidated the three overlapping hourly choices into Family Gatherings / 家庭聚会.
- Added an explicit one-hour-minimum note and reset the duration to one hour when the user switches from Family Portraits to Family Gatherings.

## Results

- Both HTML entry files pass JavaScript parsing and remain byte-for-byte synchronized.
- Browser assertions confirmed the Family Photography list contains only Family Portraits and Family Gatherings in English and Chinese.
- Family Gatherings starts at one hour and CAD $300; Family Portraits remains CAD $650.
- Studio Portrait remains CAD $450.
- `git diff --check` passes.
