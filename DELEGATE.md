# Claude Code Delegation Patterns - Hackathon Hunter

## Discovery Tasks

### Weekly Hackathon Scan
```bash
claude-delegate.sh "Search major hackathon platforms (Devpost, ETHGlobal, Encode Club, Buildspace, DoraHacks, Gitcoin) for active + upcoming hackathons in next 60 days. Filter: (1) AI/ML/agent tracks, (2) Crypto/Web3, (3) General software with >$10k prizes. For each: name, dates, prize breakdown, judging criteria, registration deadline, technical requirements. Output structured markdown table + detailed notes." research/scan-YYYY-MM-DD.md --cwd $(pwd)
```

### Competitive Intelligence
```bash
claude-delegate.sh "Research past winners of [hackathon series]. Analyze last 3 editions: (1) Winning project types, (2) Common patterns in submissions, (3) Judge preferences, (4) Technical sophistication level, (5) Presentation style. Identify success formula." research/[series]-winners-analysis.md --cwd $(pwd)
```

## Evaluation Tasks

### Deep Dive Assessment
```bash
claude-delegate.sh "Full analysis of [hackathon name]: (1) Judging rubric breakdown, (2) Sponsor prize opportunities, (3) Technical stack requirements, (4) Submission format, (5) Our competitive advantages, (6) Resource requirements (time, skills), (7) Expected competition level. Conclude with: RECOMMEND BUILD / SKIP with confidence level and reasoning." research/[hackathon-name]-assessment.md --cwd $(pwd)
```

### Idea Fit Check
```bash
claude-delegate.sh "Evaluate project idea '[idea]' for [hackathon name]. Check alignment with: (1) Hackathon themes/tracks, (2) Judging criteria, (3) Sponsor interests, (4) Technical feasibility in timeframe, (5) Differentiation from likely competitors. Score fit 0-100 with breakdown." research/[hackathon]-idea-fit.md --cwd $(pwd)
```

## Build Tasks

### Rapid Prototype
```bash
claude-delegate.sh "Build minimum viable submission for [hackathon name] implementing [idea]. Follow requirements in research/[hackathon]-assessment.md. Prioritize: (1) Core demo functionality, (2) Clear value prop, (3) Sponsor tech integration if applicable, (4) Clean UI. Output to submissions/[hackathon]/. Include README with setup instructions." build-log.md --cwd $(pwd)
```

### Sponsor Integration
```bash
claude-delegate.sh "Integrate [sponsor tech/API] into submissions/[hackathon]/. Follow their docs and prize requirements. Ensure: (1) Meaningful usage (not superficial), (2) Highlights their tech capabilities, (3) Documents integration clearly. Update README with sponsor prize targeting." integration-log.md --cwd $(pwd)
```

## Documentation Tasks

### Submission Package
```bash
claude-delegate.sh "Create complete hackathon submission package for [project]. Include: (1) README with problem/solution/tech stack, (2) Video script (2 min), (3) Devpost description (compelling copy), (4) Screenshots/demo GIFs, (5) Technical architecture diagram, (6) Pitch deck (if required). Follow best practices from research/past-winners." submissions/[hackathon]/SUBMISSION.md --cwd $(pwd)
```

### Video Script
```bash
claude-delegate.sh "Write 2-minute video script for [project] at [hackathon]. Structure: (1) Hook (problem), (2) Solution demo (60-90s), (3) Tech highlights, (4) Impact/vision. Make it: compelling, clear, judge-friendly. Include timestamps and shot suggestions." submissions/[hackathon]/script.md --cwd $(pwd)
```

## Tracker Updates

### Update Dashboard
```bash
claude-delegate.sh "Update tracker/opportunities.html with latest hackathons from research/scan-YYYY-MM-DD.md. Add: status badges (Open/Upcoming/Closed), countdown timers, prize amounts, quick links. Sort by registration deadline. Maintain existing entries." tracker-update-log.md --cwd $(pwd)
```

---

## Workflow Example

```bash
# 1. Weekly scan
claude-delegate.sh "Scan hackathon platforms for next 60 days. Filter AI/crypto/>$10k." research/scan-2026-02-10.md --cwd $(pwd)

# 2. Deep dive on promising one
claude-delegate.sh "Full analysis of ETHGlobal London. Past winners, judging criteria, our advantages." research/ethglobal-london-assessment.md --cwd $(pwd)

# 3. Evaluate fit
claude-delegate.sh "Check if 'AI agent coordination protocol' fits ETHGlobal London themes and prizes." research/ethglobal-london-idea-fit.md --cwd $(pwd)

# 4. Build if green-lit
claude-delegate.sh "Build coordination protocol prototype for ETHGlobal London per assessment requirements." submissions/ethglobal-london/ --cwd $(pwd)

# 5. Package submission
claude-delegate.sh "Create full submission package: README, video script, Devpost copy, screenshots." submissions/ethglobal-london/SUBMISSION.md --cwd $(pwd)
```

---

**Remember:** We're optimizing for learning + visibility, not just prizes. Strategic participation builds reputation and network.
