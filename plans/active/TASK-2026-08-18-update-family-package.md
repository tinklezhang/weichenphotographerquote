# Update Family Photography Package

- State: review
- Scope: Replace the Family Photography hourly quote with the approved CAD $650 package for up to two hours, remove Filipino language support, and preserve every other service and current portrait package.

## Acceptance Criteria

- Family Photography displays and calculates CAD $650 for up to two hours.
- The package includes 30 client-selected professionally retouched images, high-resolution files, and an online gallery.
- Additional professionally retouched images are CAD $20 each.
- Only English and Chinese are offered.
- Other categories and the Back to the Moment package remain unchanged.
- Both HTML entry files remain synchronized.

## Eval / Test Commands

- Check inline JavaScript syntax in both HTML files.
- Run browser assertions for both languages, Family, hourly categories, and Back to the Moment.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Rebased the implementation onto the latest remote `main` after discovering newer portrait-package work.
- Applied the Family package and bilingual changes without overwriting the newer package feature.

## Results

- Inline JavaScript syntax passed for both HTML entry files.
- Browser checks confirmed only English and Chinese are available and Family totals CAD $650 in both languages.
- Browser checks confirmed Event remains CAD $600 for two hours and its duration control remains editable.
- Browser checks confirmed Back to the Moment remains CAD $288 with its package card and hidden hourly controls.
- Both HTML entry files are identical, and `git diff --check` passed.
