# Changelog — CEO Sales 60-Second Quiz Outreach

All changes to this project are documented here in reverse chronological order.

---

## [1.7.0] — 2026-03-26 UTC

### Fixed
- **Lead Source field** — quiz submission email now correctly reads "CEO Sales 60-Second Quiz Outreach" (was "Babson College Executive Education Flyer" in the FormSubmit notification to Scott)
- **Residual Babson references purged** — updated insight copy in Critical Risk and Elevated Risk result tiers ("Babson's executive programs" → "Scott Magnacca's executive coaching"); fixed QR code alt text; updated page `<title>` tag; cleaned privacy note under email gate form; updated CTA mailto body copy

### Deployed
- Commit: `pending` — auto-deployed to Netlify via GitHub push

---

## [1.6.0] — 2026-03-26 UTC

### Fixed
- **Referral form — auto-notify Scott directly** — replaced dead FormSubmit hash (tied to old Babson email) with direct `scott.magnacca1@gmail.com` endpoint; Scott now receives referral name + friend's email automatically the moment the button is clicked — no email client required
- **Quiz URL in referral** — corrected from `babson-ai-risk-quiz.netlify.app` to `ceo-sales-60-second-quiz-outreach.netlify.app`
- **Added success/failure detection** — mailto fallback fires if FormSubmit is temporarily unavailable
- **Success message** — now confirms Scott was notified with referrer name and friend email

### Deployed
- Commit: `c9d3900` — auto-deployed to Netlify via GitHub push

---

## [1.5.0] — 2026-03-26 UTC

### Fixed
- **Suppressed iCloud / browser password AutoFill popup on refer section** — added `autocomplete="off"`, `data-lpignore="true"`, and `data-1p-ignore` to both refer inputs (Your name, Friend's work email); changed refer email input from `type="email"` to `type="text"` to eliminate browser credential-detection heuristics

### Changed
- **Pill animation redesign** — pills no longer fire on page load; sequence now triggered only after the hero subtitle typewriter completes
  - 4-second pause after typewriter finishes before first pill fires
  - Each pill now flashes **twice** (was once) before advancing
  - 5-second pause between each pill (was 3s)
  - Sequence plays through all 4 pills once and stops (no loop)

### Deployed
- Commit: `2f32158` — auto-deployed to Netlify via GitHub push

---

## [1.4.0] — 2026-03-26 UTC

### Fixed
- **Suppressed iCloud / browser password AutoFill popup on email gate form** — added `autocomplete="off"`, `data-lpignore="true"`, and `data-1p-ignore` to all three email gate inputs (Full Name, Work Email, Company); changed email input from `type="email"` to `type="text"`

### Deployed
- Commit: `f505cba` — auto-deployed to Netlify via GitHub push

---

## [1.3.0] — 2026-03-26 UTC

### Changed
- **Bio card — credential list** — replaced prose paragraph with 4-bullet list: "25+ Years in Financial Services", "Adjunct Lecturer, Babson College", "Master's (ALM) in Psychology, Harvard University", "Author, Storyselling in the Age of AI" (applied to both landing page and results page bio cards)
- **Bio card — title corrected** — "Adjunct Professor" → "Adjunct Lecturer" on both instances
- **Hero — new CTA headline** — added "Uncover the AI Blind Spots Costing You High-Ticket Sales." above the hero pills
- **Hero — new subtext** — added benchmark subtext below the headline: "In just 60 seconds, this assessment will benchmark your current strategy against top industry performers and reveal where your sales narrative is falling behind."
- **Attention ratio** — removed all external outbound links (babson.edu) from landing page and results page; 1:1 focus enforced
- **Button styling** — `btn-next` (Continue / See My Results) and `btn-submit` (Unlock My AI Risk Score) updated to high-contrast gold accent (`#C9A84C` on dark green)
- **Email gate copy** — removed residual "Babson College" reference from lock-sub copy
- **Results page — referral unlock block** — added "Forward this assessment to a colleague, and instantly unlock Chapter 1 of Storyselling in the Age of AI for free." block between follow-up and team-strip sections

### Deployed
- Commit: `1c673e7` — auto-deployed to Netlify via GitHub push

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
- [ ] **Formspree / webhook endpoint** — activate form submission to collect leads in real time
