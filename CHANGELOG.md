# Changelog — CEO Sales 60-Second Quiz Outreach

All changes to this project are documented here in reverse chronological order.

---

## [1.2.0] — 2026-03-25 UTC

### Changed
- **Replaced QR code** in the "Refer a Friend" section — old code pointed to the source Babson site; new code points to `https://ceo-sales-60-second-quiz-outreach.netlify.app`
- QR code uses rounded modules and high error-correction (level H) for clean scanning

### Deployed
- Commit: `66c852e` — auto-deployed to Netlify via GitHub push

---

## [1.1.0] — 2026-03-25 UTC

### Changed
- **Removed Peter Dennis photo and bio** from hero "Meet the Team" section and results team strip — site now shows Scott Magnacca only
- **Removed pdennis@babson.edu CC** from both quiz result and referral email notifications
- **Updated formsubmit endpoint** to `scott.magnacca1@gmail.com` — all lead and referral notifications now go to Scott only
- **Updated follow-up copy** — "Peter Dennis will follow up" → "Scott Magnacca will follow up"
- **Updated CTA block** — "Schedule with Peter Dennis at Babson College" → "Schedule with Scott Magnacca"; mailto updated to scott.magnacca1@gmail.com
- **Updated referral section** — removed "& Peter" from subtitle ("we'll also let Scott know") and success message
- **Fixed pre-filled email greeting** — "Hi Peter," → "Hi Scott,"

### Deployed
- Commit: `1f09046` — auto-deployed to Netlify via GitHub push
- Live at: https://ceo-sales-60-second-quiz-outreach.netlify.app

> ⚠️ **Action required:** FormSubmit will send a one-time verification email to scott.magnacca1@gmail.com — click the link to activate lead notifications.

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
