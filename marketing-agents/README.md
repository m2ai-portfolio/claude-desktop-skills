# M2AI Marketing Agents -- CoWork Plugin

**Version:** 0.1.0
**Author:** M2AI / Matthew Snow

Tier 1 marketing agent pack for trades and local service businesses -- kitchen fitters, bathroom specialists, contractors, and similar. Three agents, 14 skills, zero external API integrations required.

Built for [Claude CoWork](https://cowork.anthropic.com/) (CW).

---

## What's Included

### Creator -- Content Creation (5 skills)

| Skill | What it does |
|-------|-------------|
| `creator-social-post` | Platform-specific posts for Facebook, Instagram, LinkedIn |
| `creator-blog-seo` | 800-1200 word locally-targeted SEO blog posts |
| `creator-case-study` | Project case studies with scope, process, result, testimonial |
| `creator-content-calendar` | Weekly/monthly content calendar using the 40/25/20/15 mix |
| `creator-repurpose` | One asset repurposed into multiple formats across platforms |

### Scout -- Competitive Intelligence (4 skills)

| Skill | What it does |
|-------|-------------|
| `scout-competitor-scan` | Deep-scan a specific competitor across all channels |
| `scout-market-snapshot` | Weekly competitive landscape summary for tracked competitors |
| `scout-directory-audit` | Audit directory listings for presence and NAP consistency |
| `scout-pricing-intel` | Research competitor pricing signals and market positioning |

### RepMan -- Reputation Management (5 skills)

| Skill | What it does |
|-------|-------------|
| `repman-review-monitor` | Check for new reviews and flag anything urgent |
| `repman-review-respond` | Draft on-brand responses (positive/negative/mixed) -- always DRAFT, never auto-posted |
| `repman-review-request` | Personalised review request messages (SMS + email) |
| `repman-directory-manage` | Audit directory listings for NAP consistency and completeness |
| `repman-gbp-manage` | Monitor GBP Q&A, draft posts, optimise profile |

---

## Getting Started

### Prerequisites

- A [Claude CoWork](https://cowork.anthropic.com/) account (desktop app)
- A CoWork project set up for the client business

### Step 1: Download the plugin

Clone this repo or download the `.plugin` file directly:

```bash
git clone https://github.com/m2ai-portfolio/marketing-agents-cw.git
```

The installable file is `m2ai-marketing-agents.plugin`.

### Step 2: Install in CoWork

1. Open your CoWork project
2. Drag `m2ai-marketing-agents.plugin` into the CoWork chat window, or copy it into your CoWork workspace folder and present it for installation
3. CoWork will prompt you to install -- click Install
4. Restart the CoWork session (close and reopen the project)
5. The 14 skills will appear in the skills panel

### Step 3: Configure for your client

Each agent needs client-specific details set in the project's `CLAUDE.md`. Add these variables:

```markdown
## Business Details

- Business name: Premier Kitchens Ltd
- Business type: kitchen fitter
- City: Coventry
- Region: West Midlands
- CTA: Call us on 01234 567890
- Brand voice: Professional but approachable
- Contact method: info@premierkitchens.co.uk
```

For **Scout**, also add 3-5 competitor names and URLs.
For **RepMan**, also add review platform URLs (Google Business Profile, Checkatrade, etc.).

### Step 4: Use the skills

Invoke skills naturally in conversation:

- "Write a Facebook post about the kitchen we just finished"
- "Scan what ABC Kitchens is doing online this week"
- "Draft a response to this 1-star Google review: [paste review]"
- "Build a content calendar for May"
- "Turn this case study into social posts"

Each skill is triggered by natural language -- see the skill descriptions for full trigger phrases.

---

## Automated Workflows (Optional)

The file `m2ai-scheduled-workflows-onboarding.md` contains a ready-to-paste prompt that sets up 4 automated marketing pipelines as CoWork scheduled tasks:

| Workflow | Schedule | What it does |
|----------|----------|-------------|
| Monday Reputation Triage | Mon 8 AM | Scans reviews, drafts responses, checks GBP Q&A |
| Weekly Competitive Intel | Fri 5 PM | Market snapshot + conditional pricing deep-dive |
| Monthly Content Engine | 1st of month 8 AM | Calendar + SEO blog + repurposed content pack |
| Friday Post-Job Loop | Fri 12 PM | Review requests + case study + social posts |

Open `m2ai-scheduled-workflows-onboarding.md` for the full setup prompt and instructions.

---

## Tier 2 Agents (Not Yet Built)

LeadGen, Analytics, and AdOps require external API integrations (CRM, Google Ads, Meta Ads, GA4) and are not included in this Tier 1 pack.

---

## Important Notes

- **RepMan never auto-posts.** All responses are clearly marked DRAFT and require human review before posting.
- **Scout cites everything.** All competitive intel includes source URLs and access dates. No fabricated claims.
- **Creator targets local keywords only.** National generic keywords are excluded by design -- these skills are built for local service businesses.

---

## Repository Contents

| File | Purpose |
|------|---------|
| `m2ai-marketing-agents.plugin` | Installable CoWork plugin (zip containing all 14 skills) |
| `m2ai-scheduled-workflows-onboarding.md` | Setup prompt for 4 automated marketing pipelines |
| `README.md` | This file |

---

## License

Proprietary -- M2AI / Matthew Snow. Not licensed for redistribution.
