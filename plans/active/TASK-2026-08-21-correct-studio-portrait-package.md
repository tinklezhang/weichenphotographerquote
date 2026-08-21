# Correct Studio Portrait Package

- State: merged
- Scope: Correct only the existing Indoor Studio Portrait package to CAD $300 for 45 minutes while preserving its five portrait photos, one complimentary 8×10 print, and all unrelated services.

## Acceptance Criteria

- Indoor Studio Portrait displays and calculates CAD $300.
- The session duration displays as 45 minutes in English and Chinese.
- The package continues to include five professionally retouched digital portrait photos and one complimentary professional 8×10 print.
- Existing extra-image, high-resolution-file, gallery, travel, and email behavior remains unchanged.
- Back to the Moment, Family, Event, and Commercial prices and calculations remain unchanged.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check the English and Chinese Studio Portrait display and CAD $300 total.
- Regression-check Back to the Moment, Outdoor Family Session, Family Gatherings, Event, and Commercial totals.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Rebased the correction onto the latest remote `main` so newer service categories, validation, and summary-layout work are preserved.
- Changed the fixed Studio Portrait rate from CAD $450 to CAD $300.
- Changed all English and Chinese Studio Portrait duration and quote-summary copy from 45–60 minutes to 45 minutes.
- Preserved the existing five retouched digital portraits, one complimentary 8×10 print, optional extra-image pricing, high-resolution files, online gallery, and travel behavior.

## Results

- Both inline scripts parse successfully and the two HTML entry files remain byte-for-byte synchronized.
- Browser checks confirmed English and Chinese Studio Portrait displays show 45 minutes, CAD $300, five professionally retouched digital photos, and one complimentary professional 8×10 print.
- Studio Portrait hides the hourly duration control and totals CAD $300 before any selected travel fee.
- Regression checks passed: Back to the Moment CAD $288, Outdoor Family Session CAD $650, Family Gatherings CAD $300, two-hour Event CAD $600, and two-hour Commercial CAD $600.
- Browser console reported no errors and `git diff --check` passed.
- PR #10 was squash-merged to `main` as `76cfa6f`.
- GitHub Pages deployment `32529493475` completed successfully.
- The live English and Chinese quote page was verified at CAD $300 / 45 minutes with the approved five-photo and 8×10-print inclusions.
