# Update Studio Portrait Package

- State: merged
- Scope: Update only the Studio Portrait offering in the existing quote system to the approved CAD $450 / 45–60 minute package, eligible portrait types, and included deliverables. Preserve every other package and calculation.

## Acceptance Criteria

- Studio Portrait displays CAD $450 / 45–60 min.
- Eligible types are Professional Headshots, Business Portraits, LinkedIn / Professional Profile Photos, Personal Portraits, and Couples Portraits, with the approved bilingual labels.
- Includes are a 45–60 minute studio session, 5 professionally retouched digital photos, optional extra retouched photos at $20 each, one complimentary 8×10 professional print, high-resolution digital files, and an online gallery.
- Studio Portrait totals CAD $450 before any selected travel fee and does not use hourly or evening-surcharge calculations.
- All other service categories retain their existing types, rates, delivery rules, travel calculations, and email workflow.
- `index.html` and `photography-quote-en.html` remain synchronized.

## Eval / Test Commands

- Extract the inline JavaScript and run `node --check`.
- Assert Studio Portrait labels, fixed pricing, includes, and quote payload/output.
- Assert unchanged Event, Commercial, and Family hourly calculations, evening surcharge, and travel fee.
- Run `git diff --check` and verify both HTML files are identical.

## Progress

- Located the existing GitHub Pages quote project and confirmed the current Studio Portrait entry still uses the generic hourly calculation.
- Replaced the Studio Portrait types with the five approved bilingual options.
- Added the approved 45–60 minute session and all six included-deliverable lines in English and Chinese modes, with equivalent English copy in Filipino mode.
- Changed only Studio Portrait to a fixed CAD $450 calculation and suppressed the hourly control and evening-surcharge notice for that package.
- Kept travel fees available and unchanged; all other categories remain on the existing CAD $300/hour calculation.
- Rebasing onto the latest deployed project preserved the separate Back to the Moment portrait package and the newer Family Photography pricing rules.

## Results

- Inline JavaScript parses successfully in both HTML entry files.
- Headless browser assertions confirmed Studio Portrait shows five approved types, CAD $450, 45–60 min, all approved inclusions, no hourly selector, and no evening surcharge.
- Regression assertion confirmed a two-hour Event Photography booking starting at 19:00 remains $600 shooting + $120 evening surcharge = $720 before travel.
- Regression assertions also confirmed Back to the Moment remains CAD $288 and the Family Portrait package remains CAD $650.
- `index.html` and `photography-quote-en.html` are byte-for-byte synchronized.
- `git diff --check` passes.
