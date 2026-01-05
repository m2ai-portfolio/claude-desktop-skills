# Claude Desktop Skills Portfolio

> 21 production-ready Claude skills capturing 153,200+ monthly searches across Career, Creator, Growth, and Developer domains.

[![Skills](https://img.shields.io/badge/Skills-21-blue)]()
[![Monthly Searches](https://img.shields.io/badge/Monthly%20Searches-153.2K%2B-green)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)]()

Built by [Me, Myself Plus AI LLC](https://memyselfplusai.com) | Specialized in Claude ecosystem, n8n workflows, and AI automation

---

## 📋 Table of Contents

- [Overview](#overview)
- [Skill Suites](#skill-suites)
  - [Career Suite](#-career-suite-57900-searchesmonth)
  - [Creator Suite](#-creator-suite-52600-searchesmonth)
  - [Growth Suite](#-growth-suite-39300-searchesmonth)
  - [Specialized Tools](#-specialized-tools-14200-searchesmonth)
  - [Developer Tools](#-developer-tools)
- [Quick Start](#quick-start)
- [Skill Catalog](#skill-catalog)
- [Examples](#examples)
- [Development](#development)
- [Use Cases](#use-cases)
- [Contributing](#contributing)

---

## Overview

This repository contains 21 validated, production-ready Claude Desktop skills built using the Model Context Protocol (MCP). Each skill addresses a specific, high-demand use case validated by search volume data.

### What Makes These Skills Unique

- **✅ Validated Demand**: Every skill targets 3K-14K monthly searches
- **✅ Production-Ready**: Complete with examples, edge cases, and quality checks
- **✅ Suite-Based**: Organized into cohesive product lines (Career, Creator, Growth, Developer)
- **✅ Integration-Ready**: Designed to work with n8n workflows and automation
- **✅ Lightweight**: Total portfolio size ~86KB

### Total Market Reach
**153,200+ monthly searches** across all 21 skills

---

## Skill Suites

### 📊 Career Suite (57,900 searches/month)
**Target Audience**: Job seekers, career coaches, HR managers, recruiters

| Skill | Monthly Searches | Purpose |
|-------|-----------------|---------|
| Resume Bullet Generator | 12,100 | ATS-optimized achievement bullets |
| Cover Letter Personalizer | 11,200 | Targeted application letters |
| Social Media Bio Writer | 9,400 | Platform-specific bios |
| Email Tone Converter | 8,400 | Adjust tone for any audience |
| Job Description Generator | 8,300 | Unbiased, effective job postings |
| LinkedIn Post Formatter | 7,200 | Engagement-optimized posts |

### 🎨 Creator Suite (52,600 searches/month)
**Target Audience**: Content creators, social media managers, agencies

| Skill | Monthly Searches | Purpose |
|-------|-----------------|---------|
| Instagram Caption Generator | 14,200 | Hooks, CTAs, hashtags |
| YouTube Script Outliner | 7,800 | Retention-optimized structures |
| Tweet Thread Generator | 6,400 | Narrative-driven threads |
| Blog Post Outline Creator | 5,600 | SEO-optimized structures |
| Meta Description Generator | 4,800 | Click-worthy search snippets |
| Podcast Show Notes Generator | 3,200 | Episode summaries with timestamps |

### 📈 Growth Suite (39,300 searches/month)
**Target Audience**: Sales teams, marketers, agencies

| Skill | Monthly Searches | Purpose |
|-------|-----------------|---------|
| Product Description Writer | 9,600 | E-commerce copy that converts |
| Meeting Summary Generator | 9,100 | Action items from transcripts |
| Google Ads Copy Generator | 8,700 | Compliant, character-limited ads |
| Cold Email Personalizer | 6,800 | Outreach that gets replies |
| Email Subject Line Generator | 6,200 | High-open-rate headlines |

### 🔧 Specialized Tools (14,200 searches/month)
**Target Audience**: Business owners, technical teams, sellers

| Skill | Monthly Searches | Purpose |
|-------|-----------------|---------|
| Amazon Product Review Generator | 5,900 | Compliant review guidance |
| Legal Document Simplifier | 4,900 | Plain-language contract summaries |
| Technical Document Simplifier | 3,400 | API docs for non-technical users |

### 🔨 Developer Tools
**Target Audience**: MCP developers, AI engineers, system architects

| Skill | Purpose |
|-------|---------|
| MCP Forge | Guide users through designing production-ready MCP server PRDs with tool specifications, architecture decisions, and implementation guidance |

---

## Quick Start

### Upload to Claude Desktop

1. **Clone this repository**
```bash
   git clone https://github.com/YOUR-ORG/claude-skills.git
```

2. **Navigate to claude.ai and create a project**
   - Option A: Create suite-specific projects (Career Tools, Creator Tools, etc.)
   - Option B: Create one master project with all skills

3. **Upload skills**
   - Click "Skills" → "Upload skill"
   - Select `.skill` files from skill folders
   - Skills are ready to use immediately

### Using Skills

Skills trigger automatically based on your request. No need to reference skill names:
```
❌ "Use the resume-bullet-generator to help me"
✅ "Help me write resume bullets for my data analyst role"
```

Claude automatically matches your intent to the appropriate skill.

### Examples

**Resume Bullet Generator**
```
Input: "I managed a team of 5 developers working on a web application"

Output: 
- Led cross-functional development team of 5 engineers, delivering 
  customer-facing web application 2 weeks ahead of schedule
- Established agile workflows and daily standups, improving sprint 
  completion rate from 67% to 94%
```

**Cold Email Personalizer**
```
Input: 
Prospect: Sarah Chen, VP Product at TechCorp
Recent: Just announced Series B funding
Offer: AI workflow automation consulting

Output:
Subject: Congrats on TechCorp's Series B - Scaling Product Operations

Hi Sarah,

Saw TechCorp's Series B announcement - congrats! Growing from 50 
to 150 people is exciting, but I know product ops complexity grows 
exponentially...

[personalized 3-paragraph email with specific value prop]
```

**Instagram Caption Generator**
```
Input:
Post type: Carousel
Topic: Morning productivity routine
Audience: Entrepreneurs, 25-35
Tone: Motivational, practical

Output:
Your morning sets the tone for your entire day. Here's the 5-step 
routine that transformed mine 👇

(Swipe to see each step with actionable tips)

[Full caption with hooks, value, and CTA]

#ProductivityHacks #MorningRoutine #EntrepreneurLife
```

**MCP Forge**
```
Input: "I want to build an MCP server that connects to Notion"

Output:
[Guides through comprehensive PRD including:]
- Server overview and scope
- Tool specifications with parameters
- Error handling strategies
- Authentication patterns
- Rate limiting considerations
- Testing approach
- Deployment guidelines
```

See [docs/SKILL_CATALOG.md](docs/SKILL_CATALOG.md) for complete trigger patterns and examples.

---

## Skill Catalog

### Complete Skill List

<details>
<summary><b>Career Suite (6 skills)</b></summary>

1. **resume-bullet-generator** - Transform duties into ATS-optimized achievements
2. **cover-letter-personalizer** - Targeted letters matching job postings
3. **job-description-generator** - Clear, unbiased job postings
4. **email-tone-converter** - Adjust email tone for any context
5. **linkedin-post-formatter** - Engagement-optimized LinkedIn posts
6. **social-media-bio-writer** - Platform-specific bios (LinkedIn, X, Instagram, TikTok)

</details>

<details>
<summary><b>Creator Suite (6 skills)</b></summary>

7. **instagram-caption-generator** - Hooks, CTAs, and hashtag strategies
8. **youtube-script-outliner** - Retention-optimized video structures
9. **tweet-thread-generator** - Narrative-driven Twitter/X threads
10. **blog-post-outline-creator** - SEO-optimized content structures
11. **podcast-show-notes-generator** - Episode summaries with timestamps
12. **meta-description-generator** - Click-worthy search snippets

</details>

<details>
<summary><b>Growth Suite (5 skills)</b></summary>

13. **meeting-summary-generator** - Action items from transcripts
14. **cold-email-personalizer** - Personalized outreach that converts
15. **google-ads-copy-generator** - Compliant ad copy with character limits
16. **email-subject-line-generator** - High-open-rate subject lines
17. **product-description-writer** - E-commerce copy (short/medium/long)

</details>

<details>
<summary><b>Specialized Tools (3 skills)</b></summary>

18. **legal-document-simplifier** - Plain-language contract summaries
19. **technical-document-simplifier** - API docs for non-technical users
20. **amazon-product-review-generator** - Compliant review templates

</details>

<details>
<summary><b>Developer Tools (1 skill)</b></summary>

21. **mcp-forge** - Production-ready MCP server PRD generation with architecture guidance, tool specifications, and implementation best practices

</details>

---

## Development

### Built With
- **Model Context Protocol (MCP)** - Claude's skill framework
- **Search Volume Validation** - Each skill targets proven demand
- **Production Testing** - Real-world use case validation

### Architecture Principles
1. **Single Responsibility** - Each skill solves ONE problem exceptionally
2. **Composability** - Skills work standalone or in sequences
3. **Context-Aware** - Industry/role-specific adaptations
4. **Quality-First** - Built-in checklists and validation

### File Structure
```
skill-name/
├── SKILL.md          # Complete skill documentation
├── examples/         # Before/after examples
└── tests/           # Edge case validation
```

---

## Use Cases

### Individual Professionals
- Job seekers crafting applications
- Content creators producing social media
- Sales reps personalizing outreach
- AI engineers building MCP servers

### Teams & Agencies
- HR departments writing job descriptions
- Marketing teams creating ad copy
- Customer success simplifying technical docs
- Development teams designing tool integrations

### Automation Workflows (n8n Integration)
- Auto-summarize Zoom meetings → Slack
- Generate job descriptions from templates → ATS
- Personalize cold emails from LinkedIn scrapes → CRM
- Design MCP servers from requirements → PRD documentation

### Example n8n Workflow
```
Trigger: New meeting recording in Zoom
↓
Extract transcript via Zoom API
↓
Call Claude with meeting-summary-generator skill
↓
Post summary to Slack channel
↓
Create tasks in Asana with owners/deadlines
```

---

## Contributing

### Found an Issue?
Open an issue with:
- Skill name
- Input provided
- Expected vs actual output
- Context (industry, role, etc.)

### Want to Improve a Skill?
1. Fork the repo
2. Edit the `SKILL.md` in the skill folder
3. Test with real use cases
4. Submit PR with before/after examples

### Building Custom Skills?
See [docs/DEVELOPMENT.md](docs/DEVELOPMENT.md) for skill creation guidelines.

---

## License

MIT License - see [LICENSE](LICENSE) for details

---

## About Me, Myself Plus AI LLC

Specialized in:
- Claude ecosystem integration
- n8n workflow automation
- AI-powered healthcare applications
- Production MCP server development

**Portfolio**: [memyselfplusai.com](https://memyselfplusai.com)  
**Contact**: matthew@memyselfplusai.com  
**GitHub**: [@m2ai-portfolio](https://github.com/m2ai-portfolio)

---

## Acknowledgments

Built using Anthropic's Claude Desktop and Model Context Protocol (MCP) framework.

Search volume data validates market demand for each skill.

---

**Ready to use these skills?** See [docs/QUICK_START.md](docs/QUICK_START.md) for upload instructions.

**Want to see more examples?** Browse [docs/SKILL_CATALOG.md](docs/SKILL_CATALOG.md) for comprehensive trigger patterns.