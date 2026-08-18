# Simplify Portrait and Family Labels

- State: merged
- Scope: Apply the approved non-overlapping portrait choices and rename the outdoor family package while preserving pricing and package behavior.

## Acceptance Criteria

- English Portrait Photography offers Back to the Moment, Professional Headshots, Personal Portraits, and Couples Portraits.
- Chinese Portrait Photography offers 回到那一刻、职业形象照、个人肖像、情侣肖像.
- Family Portraits / 家庭合照 is renamed Outdoor Family Session / 户外家庭拍摄.
- English and Chinese labels remain separated by active language.
- All prices and package calculations remain unchanged.

## Eval / Test Commands

- Parse inline JavaScript and compare both HTML entry files.
- Browser-check English and Chinese option lists.
- Regression-check Outdoor Family Session, Family Gatherings, Indoor Studio Portrait, and Back to the Moment pricing.
- Run `git diff --check`.

## Progress

- Confirmed the approved text and current option arrays.
- Removed the overlapping Business Portraits and LinkedIn / Professional Profile Photos choices.
- Renamed the fixed outdoor family package in English and Chinese.

## Results

- English and Chinese option lists match the approved copy and remain language-separated.
- Browser assertions confirmed Indoor Studio Portrait CAD $450, Back to the Moment CAD $288, Outdoor Family Session CAD $650, and Family Gatherings CAD $300 starting at one hour.
- Both HTML entry files parse successfully and are byte-for-byte synchronized.
- `git diff --check` passes.
