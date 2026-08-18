# Improve Required Field Guidance

- State: merged
- Scope: Make incomplete quote submissions obvious and actionable without opening the review modal prematurely.

## Acceptance Criteria

- Clicking Review & Send with missing required details shows a concise English or Chinese summary listing every missing field.
- The page scrolls to and focuses the first invalid field.
- Each invalid field has a red border and a specific inline message.
- Name, email, preferred shoot date, and valid schedule data are required before review.
- Validation guidance clears as the user corrects a field.
- Existing pricing, language, review, and email behavior remains unchanged.

## Eval / Test Commands

- Check inline JavaScript syntax in both HTML files.
- Run browser assertions for empty submission, progressive correction, invalid email, date, and successful review opening.
- Test English and Chinese plus a mobile viewport.
- Recheck representative Family and Event totals.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Reviewed the current validation flow and confirmed it silently returns after marking fields, with no missing-field summary or first-field focus.
- Added a bilingual alert summary, field-specific red states, first-error scrolling/focus, and required preferred shoot date validation.
- Added accessible alert and invalid-field attributes while preserving the existing review modal.

## Results

- Inline JavaScript syntax passed for both HTML entry files.
- Mobile-width browser checks confirmed an empty submission lists name, email, and preferred shoot date and focuses the name field.
- Progressive correction checks confirmed the summary clears while editing and the next submission focuses the next invalid field.
- English and Chinese summary and inline messages passed.
- A complete form opens the review modal; an incomplete form does not.
- Family Portraits remains CAD $650 and Family Gatherings remains CAD $300 for one hour.
- Both HTML entry files are identical, and `git diff --check` passed.
- PR #8 was squash-merged to `main` as `3738d04`.
- GitHub Pages completed successfully, and the live mobile-width page confirmed the summary, inline messages, and first-field focus.
