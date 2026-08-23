# Reprice Studio Portrait Package

- State: merged
- Scope: Change only the existing Indoor Studio Portrait package to CAD $200 for 20–30 minutes with two professionally retouched digital photos and no print, while preserving all unrelated services.

## Acceptance Criteria

- Indoor Studio Portrait displays and calculates CAD $200.
- The session duration displays as 20–30 minutes in English and Chinese.
- The package includes two professionally retouched digital photos and no physical print.
- Existing extra-image pricing, high-resolution files, online gallery, travel behavior, and email workflow remain unchanged.
- Back to the Moment, Family, Event, and Commercial prices and calculations remain unchanged.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check the English and Chinese Studio Portrait display and CAD $200 total.
- Verify the quote summary and outgoing payload show two included photos and no print.
- Regression-check representative Back to the Moment, Family, Event, and Commercial totals.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Changed the fixed Studio Portrait price from CAD $300 to CAD $200.
- Changed the session duration from 45 minutes to 20-30 minutes in English and Chinese.
- Reduced included delivery from five to two professionally retouched digital photos.
- Removed the complimentary 8x10 print from all Studio Portrait display and delivery copy.
- Preserved additional retouched photos at CAD $20 each, high-resolution files, the online gallery, travel behavior, and unrelated services.

## Results

- Both HTML entry files pass inline JavaScript parsing and remain byte-for-byte synchronized.
- Browser checks confirmed English and Chinese Studio Portrait displays, summaries, and totals show CAD $200, 20-30 minutes, two retouched digital photos, and no print.
- Browser console reported no errors.
- Regression totals passed: Back to the Moment CAD $288, Outdoor Family Session CAD $650, Family Gatherings CAD $300, two-hour Event CAD $600, and two-hour Commercial CAD $600.
- `git diff --check` passed.
- Released through PR #12 and squash-merged as `e8c2e67fa8ef0cc35967dc8553335202056409fc`.
- GitHub Pages deployment run `32645860870` completed successfully.
- Live English and Chinese checks confirmed CAD $200, 20–30 minutes, two retouched digital photos, no print, and no browser console errors.
