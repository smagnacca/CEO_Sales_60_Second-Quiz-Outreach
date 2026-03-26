# Changelog — CEO Sales 60-Second Quiz Outreach

All changes to this project are documented here in reverse chronological order.

---

## [1.0.0] — 2026-03-25 UTC

### Added
- **New GitHub repository** — `smagnacca/CEO_Sales_60_Second-Quiz-Outreach` created as a clean fork of `smagnacca/babson-ai-risk-quiz`
- **Netlify site created** — `ceo-sales-60-second-quiz-outreach.netlify.app` live and deployed
- **GitHub ↔ Netlify auto-deploy linked** — every push to `main` triggers an automatic Netlify production deploy (installation ID: 113957747)
- **Initial production deploy** — site live and returning HTTP 200

### Changed
- Stripped all Babson College and Peter Dennis references from the codebase — site is now branded for general CEO sales outreach use
- Retained all quiz logic, email capture gate, scoring tiers, and animations from v1.14.0 of the source project

### Inherited from source (babson-ai-risk-quiz v1.14.0)
- 4-question AI readiness quiz with scored answer options
- Progress bar with percentage display and back/forward navigation
- Email capture gate (Name, Work Email, Company) before results reveal
- 4 personalized result tiers: Critical / Elevated / Moderate / Low Risk
- Score circle with color-coded risk level badge and 3 tailored insight bullets per tier
- Hero subtitle typewriter animation (~42ms/char) with gold pulse on completion
- Sequential pill glow animation ("4 Questions", "Under 60 Seconds", "Personalized Results", "No Cost")
- Responsive mobile layout
- `netlify.toml` deploy config and `_headers` security headers

### Deployed
- GitHub: https://github.com/smagnacca/CEO_Sales_60_Second-Quiz-Outreach (main)
- Netlify site ID: `20e7d9ad-c961-4d75-a120-e342f2ed5a74`
- Live at: https://ceo-sales-60-second-quiz-outreach.netlify.app

---

## Pending / Planned
- [ ] **Lead capture → Google Sheets** — wire email gate submissions to master lead template via smagnacca/email-outreach-machine
- [ ] **Email outreach integration** — connect with email-outreach-machine repo to send quiz invitations and capture responses
- [ ] **Branding pass** — update copy, colors, and CTAs to match CEO sales outreach context
- [ ] **Formspree / webhook endpoint** — activate form submission to collect leads in real time
