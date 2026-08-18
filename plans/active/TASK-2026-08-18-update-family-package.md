# Update Family Photography Package

- State: running
- Scope: Replace the Family Photography hourly quote with the approved CAD $650 package for up to two hours while preserving every other service category.

## Acceptance Criteria

- Family Photography displays CAD $650 for up to two hours.
- Family Photography includes 30 professionally retouched images of the client's choice, high-resolution digital files, and an online gallery.
- Additional professionally retouched images are displayed at CAD $20 each.
- Family quotes use a fixed CAD $650 base price and a two-hour maximum; other categories retain their current calculations.
- The app offers only English and Chinese, synchronized across both HTML entry files.

## Eval / Test Commands

- Extract the inline JavaScript and run `node --check` on it.
- Run browser-level assertions for Family and unchanged Event, Commercial, and Portrait calculations.
- Search both HTML files for obsolete Family hourly and photo-count wording.
- Run `git diff --check` and confirm both HTML entry files remain identical.

## Progress

- Located the existing GitHub Pages repository and reviewed the current Family display and calculation paths.
- Added the fixed Family package price and duration rules without changing the other service categories.
- Updated displayed, copied, review, and email-payload delivery details in English and Chinese.
- Removed the Filipino language option and restricted language switching to English and Chinese.
- Kept the existing evening and travel surcharges; for Family, the evening surcharge is prorated from the fixed two-hour package rate.

## Results

- Inline JavaScript syntax checks passed for both HTML entry files.
- Browser assertions confirmed only English and Chinese are available.
- Browser assertions confirmed Family is locked to two hours with a CAD $650 base total and includes all approved delivery copy in both languages.
- Browser assertions confirmed two-hour Event, Commercial, and Portrait quotes remain CAD $600 before surcharges.
- Both HTML entry files are identical, and `git diff --check` passed.
- GitHub CLI is available from the official release package and authenticated as `tinklezhang`; publishing is in progress.
