# Babson AI Risk Quiz — Project Brief

## Project Overview
A lead generation website for Babson College Professional & Executive Education. Visitors take a 4-question AI readiness assessment, enter their contact details, and receive a personalized AI Risk Score. Every submission notifies the Babson team by email.

## Live URL
**https://babson-ai-risk-quiz.netlify.app**

## Netlify Site ID
`c316d57c-5c06-433e-873a-5252b2a85840`

## Key Contacts
| Role | Name | Email |
|------|------|-------|
| Project Owner | Scott Magnacca | smagnacca@babson.edu |
| Sales Contact | Peter Dennis | pdennis@babson.edu |

## Lead Source
All leads originating from this site are tagged as: **Babson College Professional & Executive Education Flyer**

---

## Tech Stack
- **Frontend:** Single-file HTML/CSS/JS — no framework, no build step
- **Hosting:** Netlify (account: scott-magnacca1)
- **Form Handling:** Formspree (pending setup — endpoint TBD)
- **Fonts:** Google Fonts — Merriweather + Inter

---

## Brand Guidelines
| Token | Value | Usage |
|-------|-------|-------|
| `--green` | `#1B4332` | Primary — nav, hero, buttons, card borders |
| `--green-mid` | `#2D6A4F` | Stats bar, hover states |
| `--gold` | `#C9A84C` | Accents — labels, progress bar, logo mark |
| `--gold-light` | `#E8C96A` | Hero text accents, CTA button |
| `--cream` | `#FAFAF7` | Page background |
| `--border` | `#E4E0D8` | Card borders, dividers |
| Font (display) | Merriweather | All headings |
| Font (body) | Inter | All body text, UI |

---

## Quiz Logic

### Questions
1. Current AI Usage (A=1, B=2, C=3, D=4)
2. Team AI Confidence (A=1, B=2, C=3, D=4)
3. Competitive Concern (A=1, B=2, C=3, D=4)
4. AI Strategy Maturity (A=1, B=2, C=3, D=4)

### Scoring Formula
`score = round(((sum - 4) / 12) * 100)`
- Range: 0–100
- Min raw: 4 → Score 0
- Max raw: 16 → Score 100

### Score Tiers
| Range | Level | Color |
|-------|-------|-------|
| 0–25 | Critical Risk | Red `#B84040` |
| 26–50 | Elevated Risk | Orange `#B87030` |
| 51–75 | Moderate Risk | Blue `#2C72A8` |
| 76–100 | Low Risk | Green `#1B7A4A` |

---

## Email Notifications (Formspree — Pending)
- **Recipient 1:** smagnacca@babson.edu
- **Recipient 2:** pdennis@babson.edu
- **Fields captured:** Full Name, Work Email, Company, AI Score, Risk Level
- **Lead source tag:** "Babson College Flyer"

### To complete setup:
1. Create free account at formspree.io
2. Create new form → copy endpoint URL
3. Provide endpoint to Claude → auto-deployed

---

## Deployment
Claude deploys directly via Netlify API using a zip upload. No Git required.

```bash
# Deployment command (Claude handles this automatically)
curl -X POST \
  -H "Authorization: Bearer [TOKEN]" \
  -H "Content-Type: application/zip" \
  --data-binary @deploy.zip \
  "https://api.netlify.com/api/v1/sites/c316d57c-5c06-433e-873a-5252b2a85840/deploys"
```

---

## Future Enhancements (Backlog)
- [ ] Connect Formspree endpoint for email notifications
- [ ] Add Google Analytics or Netlify Analytics
- [ ] A/B test hero headline copy
- [ ] Add a "Share your score" social share button on results page
- [ ] CRM integration (HubSpot / Salesforce)
