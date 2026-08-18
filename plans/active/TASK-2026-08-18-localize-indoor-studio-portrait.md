# Localize Indoor Studio Portrait

- State: merged
- Scope: Rename the CAD $450 studio portrait package to Indoor Studio Portrait and ensure portrait type labels use only the active language.

## Acceptance Criteria

- English displays `Indoor Studio Portrait` and English-only portrait type names.
- Chinese displays `室内影棚肖像摄影` and Chinese-only portrait type names.
- Pricing, inclusions, Back to the Moment, and all non-portrait services remain unchanged.
- Both HTML entry files remain synchronized.

## Eval / Test Commands

- Parse inline JavaScript in both HTML files.
- Browser-check English and Chinese labels and the CAD $450 package calculation.
- Regression-check Back to the Moment, Family Gatherings, and Family Portraits.
- Run `git diff --check` and compare both HTML files.

## Progress

- Identified bilingual labels in the portrait type options and quote summary.
- Renamed the CAD $450 package to Indoor Studio Portrait / 室内影棚肖像摄影.
- Separated all five studio portrait type labels by active language.

## Results

- Both HTML entry files pass JavaScript parsing and remain byte-for-byte synchronized.
- Browser assertions confirmed English contains only English portrait labels and Chinese contains only Chinese portrait labels.
- Indoor Studio Portrait remains CAD $450 / 45–60 min.
- Regression assertions confirmed Back to the Moment remains CAD $288 and Family Gatherings remains CAD $300 starting at one hour.
- `git diff --check` passes.
