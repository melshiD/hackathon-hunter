# Hackathon Hunter

Research, track, and participate in relevant hackathons. Automated discovery + human decision-making.

## Purpose

Monitor hackathon opportunities across major platforms (Devpost, ETHGlobal, Encode Club, etc.). Research eligibility, prizes, and fit. Build submissions when opportunities align.

## Tech Stack

- **Static pages** - Research outputs, project trackers
- **Vue 3 CDN** - Interactive dashboards when needed
- **GitHub Pages** - Deployment
- **Claude Code** - Research automation

## Quick Start

```bash
# View current opportunities
open tracker/opportunities.html

# Read latest research
cat research/YYYY-MM-DD-[hackathon-name].md
```

## Current State

- ✅ Template structure ready
- ⏳ No hackathons tracked yet
- ⏳ No submissions built yet

## Delegation Guide

### Common Tasks

**Discover hackathons:**
```bash
claude-delegate.sh "Search for active and upcoming hackathons (next 60 days) on Devpost, ETHGlobal, Encode Club, Buildspace. Filter for: AI/agent tracks, crypto/Web3, or general software. Output: name, dates, prize pool, tracks, eligibility." research/hackathons-YYYY-MM-DD.md --cwd $(pwd)
```

**Deep research on specific hackathon:**
```bash
claude-delegate.sh "Research [hackathon name]. Analyze: (1) Judging criteria, (2) Past winners, (3) Sponsor prizes, (4) Technical requirements, (5) Our competitive advantage. Recommend: build vs skip with reasoning." research/[hackathon-name].md --cwd $(pwd)
```

**Build submission:**
```bash
claude-delegate.sh "Build hackathon submission for [hackathon name]: [project idea]. Requirements from research/[hackathon-name].md. Output working prototype following their technical specs." submissions/[hackathon-name]/ --cwd $(pwd)
```

See `DELEGATE.md` for full patterns.

## Structure

```
/hackathon-hunter/
├── README.md              # This file
├── DELEGATE.md           # Delegation patterns
├── /research/            # Hackathon research docs
├── /tracker/             # Opportunity tracking dashboard
├── /submissions/         # Built projects
└── /templates/           # Submission templates
```

## Deployment

Tracker dashboard deploys to:
`https://melshid.github.io/hackathon-hunter/tracker/`

---

**Built by Kishbrac** | For strategic hackathon participation
