# Update Quote Title, Delivery, and Brandon Travel Wording

- State: merged
- Scope: Update `index.html` copy and photo-delivery calculations without changing pricing, surcharges, travel prices, email delivery, or other behavior.

## Acceptance Criteria

- Browser, English, Chinese, and Filipino titles use the requested quote-calculator wording.
- English and Chinese quote headers use the requested wording.
- Every photography type includes 50–60 standard edited photos per hour in all languages.
- Included-photo calculations use 50 photos minimum and 60 photos maximum per hour for every photography type.
- Out-of-city wording identifies Brandon as the city baseline in all languages.
- Initial static HTML matches the localized strings before and after language switching.

## Eval / Test Commands

- Extract the inline JavaScript and run `node --check` on it.
- Search `index.html` for obsolete static and localized wording.
- Review the final diff to confirm prices, fees, travel pricing, and email behavior are unchanged.

## Progress

- Located all requested static strings, localized strings, and included-photo calculations.
- Updated the initial HTML and English, Chinese, and Filipino localized strings.
- Unified included-photo calculations at 50–60 photos per hour for every photography type.

## Results

- Inline JavaScript passed `node --check` using the bundled Node.js runtime.
- Obsolete wording search returned no matches.
- `git diff --check` passed.
- Final diff confirms no pricing, surcharge, travel-price, or email-interface changes.
