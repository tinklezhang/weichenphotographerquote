# Align Quote Page With Studio Services

- State: blocked
- Blocker: missing_capability — the local environment has no GitHub CLI, the HTTPS remote has no usable credentials, and the connected GitHub App can read the repository but is not permitted to update its contents.
- Scope: Reorganize the quote page around the four bookable Weichen Studio service categories while preserving existing pricing, surcharge, travel, validation, email-delivery, and language-switching behavior.

## Acceptance Criteria

- Browser and visible page titles read `Weichen Studio Quote` in every language mode.
- The quote form offers Event Photography, Commercial Photography, Family Photography, and Portrait Photography. Documentary Photography is not offered in the quote form.
- Each category exposes only the subtypes documented for the current Studio service structure.
- Included-photo wording and quote output match the selected category: 40–50/hour for Event and Commercial, 20+/hour for Family, and package-based for Portrait.
- Existing CAD $300/hour pricing, evening surcharge, transportation pricing, validation, review, and email submission behavior remain intact.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Extract the inline JavaScript and run `node --check` on it.
- Run browser-level assertions for language switching, category/subtype changes, delivery wording, totals, evening surcharge, and transportation pricing.
- Search both HTML files for obsolete title and category wording.
- Run `git diff --check` and review the final diff for unintended pricing or submission changes.

## Progress

- Cloned the GitHub Pages repository and reviewed the current implementation and prior task record.
- Confirmed both HTML entry files are currently identical.
- Mapped the current Studio service categories and delivery rules from the approved website copy.
- Replaced the flat legacy type list with four bookable service categories and category-specific photography types in English, Chinese, and Filipino modes.
- Removed Documentary Photography from the quote form at the user's request while leaving all other services unchanged.
- Updated page, quote, and email-copy titles to `Weichen Studio Quote`.
- Added category-aware photo-delivery wording without changing pricing or surcharge calculations.

## Results

- Inline JavaScript passed `node --check` using the bundled Node.js runtime.
- Browser checks confirmed all four bookable category/type lists, category-specific delivery copy, English/Chinese switching, and a $1,020 calculation for 2 hours at 19:00 with the default $300 out-of-city travel fee ($600 shooting + $120 evening surcharge + $300 travel).
- Browser console reported no warnings or errors.
- `index.html` and `photography-quote-en.html` are synchronized, and `git diff --check` passed.
- Local commit `a9f0759` contains the completed change. Publishing is pending GitHub CLI installation and authentication (`gh auth login`) or equivalent repository write credentials.
