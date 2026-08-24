# Remove Couples Portraits

- State: merged
- Scope: Remove Couples Portraits from the Portrait Photography choices while preserving the three approved portrait offerings and all pricing logic.

## Acceptance Criteria

- Portrait Photography shows only Back to the Moment, Studio Portraits, and Outdoor Portraits.
- The Chinese interface shows only 回到那一刻、影棚肖像、户外肖像.
- Studio remains CAD $200 for 20–30 minutes with two retouched photos.
- Outdoor remains CAD $300 per hour with five retouched photos per hour.
- Back to the Moment remains CAD $288.
- Both HTML entry files remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check the English and Chinese portrait option lists.
- Regression-check all three remaining portrait totals and deliveries.
- Run `git diff --check` and compare both HTML entry files.

## Progress

- Task created before implementation.
- Removed Couples Portraits and 情侣肖像 from the English and Chinese option lists.
- Removed the obsolete couples package value and Studio routing branch.
- Preserved the three approved portrait offerings and their pricing logic.

## Results

- Both HTML entry files pass inline JavaScript parsing and remain synchronized.
- English and Chinese browser checks confirmed only Back to the Moment, Studio Portraits, and Outdoor Portraits remain.
- Regression checks confirmed Back to the Moment CAD $288, Studio CAD $200 with two photos, and Outdoor CAD $300 per hour with five photos.
- Browser console reported no warnings or errors.
- `git diff --check` passed.
- Released through PR #17 and squash-merged as `2104d2c55a5f49445e55b44010ac96e27931809d`.
- GitHub Pages deployment run `32737966367` completed successfully.
- Cache-busted live-site checks confirmed the English and Chinese portrait menus contain only the three approved options, with no console warnings or errors.
