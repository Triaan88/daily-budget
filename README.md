# Daily Budget — deployable static web application

The Expense Ledger is the source of truth for actual expenses. This standalone application runs fully in the browser, with no external server or third-party libraries.

## Deployment
- GitHub Pages: create a dedicated public repository, upload `index.html` to its root, then enable Pages using `main` / root in repository Settings > Pages.
- Netlify Drop: upload the folder containing `index.html` to Netlify Drop.

## Privacy and persistence
Financial data is stored only in the browser using localStorage. Hosting the HTML DOES NOT create an account, cross-device sync, or a cloud backup. Data added on one device will not appear on another. Use Settings > Export JSON backup regularly; Import JSON backup restores the data.

## Important accounting conventions
- Only ledger entries classified `Discretionary` reduce discretionary spending allowance.
- `Transfer` should be used for card-bill settlements if underlying transactions were already recorded.
- Rollover starts at the configured start month; only *completed* months generate rollover.
- The month-specific rollover override is entered in Settings while the relevant source month is selected.
- Default budget amounts are EXAMPLES, not your actual financial data. Set them before use.

This is a local-first personal tool, not a cloud-synced application. For account-based synchronization a backend, authentication, encryption and a hosted database would need to be added separately.