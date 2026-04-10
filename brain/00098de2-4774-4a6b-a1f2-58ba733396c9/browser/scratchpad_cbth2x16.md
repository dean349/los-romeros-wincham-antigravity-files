# Tasks:
- [x] TASK 1: Test Companies House API (https://api.company-information.service.gov.uk/company/06993349/filing-history?items_per_page=10)
    - [x] Authenticate with API key (Attempted; browser rejected basic auth in URL, returning "Empty Authorization header")
    - [x] Take screenshot of the result
- [x] TASK 2: Check standard filings page (https://find-and-update.company-information.service.gov.uk/company/06993349/filing-history)
    - [x] Take full-page screenshot
    - [x] Count total filings (Total: 65 filings found)
    - [x] Note filing types (Visible: Accounts, Confirmation Statements, Officer nominations/terminations, Resolutions, PSC notifications, Capital, Annual returns, Gazette notice, Registered office changes)
    - [x] Check for missing local types (Found: Termination of Director Beryl Harrison 10 Feb 2026, Gazette notices from 2019, Resolutions 2020)
- [x] TASK 3: Check developer portal (https://developer.company-information.service.gov.uk/)
    - [x] Take screenshot of dashboard/login area

# Findings:
- API Auth working: Failed via browser URL (returns 401/Empty Auth header), but endpoint is reachable.
- Total filings count: 58 (Page 1: 25, Page 2: 17, Page 3: 16)
- Visible filing types: Accounts, Confirmation Statements, Director/Secretary changes, Resolutions, PSC, Capital, Gazette notices, Incorporation.
- Missing local types: Most notably the recent "Termination of appointment of Beryl Harrison as a director" (10 Feb 2026). Also historic Gazette notices and Resolutions.
- Developer portal info: Hub is accessible; requires sign-in/registration for application management.
- Connectivity status: URLs are timing out. Testing other sites to check internet access.
