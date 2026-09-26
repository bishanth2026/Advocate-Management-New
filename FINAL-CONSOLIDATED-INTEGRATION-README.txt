AdvocateDesk — Final Consolidated Integration Check

This package combines the module consolidations completed so far into one
integration-ready index.html.

CONSOLIDATED FILES:
- app-core-fixes.js
- cases.js
- calendar.js
- finance.js
- task.js
- client-management.js
- user-menu.js
- dashboard.js
- mobile-keyboard.js
- mobile-consolidated.css

INTENTIONALLY KEPT SEPARATE:
- app.js (main application)
- auth.js (authentication)
- case-number-rules-v2.js (not merged because it is a distinct rule layer)

INTENTIONALLY REMOVED FROM FINAL INDEX:
- case-details-new-button-placement.js — confirmed no-op
- hearings-case-typeahead.js — compatibility shim; actual hearing selector is
  implemented in app.js, so the shim is unnecessary in the consolidated index

The integration index keeps the existing inline dashboard-calendar and mobile
menu handlers. No GitHub files are modified by this package.

IMPORTANT:
Do NOT delete the original fix files yet. Keep them as backups until this
integration package is fully tested.

TEST MATRIX:
Desktop:
- Login/authentication
- Dashboard
- Case & Client / All Cases
- Case 360
- Client Management
- Hearings
- Calendar
- Documents
- Tasks
- Finance
- Reports
- Settings
- Super Admin / Central Control where applicable

Mobile:
- Sidebar opening/closing
- Top-right account menu
- All forms and keyboard scrolling
- Case & Client cards
- Client cards
- Tasks
- Finance
- Calendar
- Hearings
- Case 360
- Dashboard
- Modal scrolling

Regression:
- Add/edit/delete records
- Search/typeahead fields
- Case/client relationships
- Finance case -> client autofill
- Task case/client selection
- Calendar and dashboard calendar
- Logout only through explicit account-menu action
- No horizontal page overflow
- Desktop layout unchanged
