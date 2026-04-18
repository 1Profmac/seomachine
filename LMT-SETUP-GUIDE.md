# SEO Machine Setup Guide — Learn More Technologies

## Status: In Progress
**Date:** April 17, 2026
**Goal:** Configure SEO Machine to produce SEO-optimized content for learnmoretechnologies.com

---

## Step 1: Install (DONE)

- [x] Clone repo to `C:\Users\USER\seomachine\`
- [x] Install Node.js v24.15.0
- [x] Install Python 3.14.4
- [x] Run `pip install -r data_sources/requirements.txt`

---

## Step 2: Fill Out Context Files

These files live in `seomachine/context/`. They teach SEO Machine your brand voice so every article sounds like you, not generic AI slop.

### 2a. `context/brand-voice.md` — YOUR VOICE

Open this file and fill in:

- **Voice Pillars** — LMT has these:
  1. **Authoritative but Warm** — You have the data (347 completions, 3X rate) but you lead with compassion. "It is never too late to learn."
  2. **Direct / No-BS** — You don't sugarcoat ageism. "90% feel invisible in advertising." Say it plain.
  3. **Mission-Driven** — Every piece ties back to bridging ageism and opportunity. Not selling software — selling dignity.
  4. **Proof-First** — Stats before claims. 347 Pioneers, 23 orgs, 74% confidence rate.
- **Tone:** Confident, inclusive, urgent. Never condescending. Never preachy.
- **Audience:** Workforce board directors, HR/L&D leaders, AARP program managers, employers with aging workforce
- **Avoid:** Jargon-heavy tech talk, "senior citizen," anything patronizing, hype without data

### 2b. `context/features.md` — WHAT YOU SELL

Fill in with your 3 offerings:

1. **AI/Digital Skills Workshops** — 90-minute on-site or virtual sessions for employees 50+. $5K per engagement. 347 completions, 3X industry rate. You bring everything.
2. **WIOA Subcontractor Training** — Deliver workforce-funded training through boards (ETPL/ITA). $2K-$5K per student. MBE-certified.
3. **Keynote Speaking** — "The $76 Trillion Blind Spot" — ageism + AI + workforce. $2.5K-$7.5K per engagement.

Key differentiators:
- MBE-certified (procurement preference)
- 347 completions with verified outcomes
- 3X industry completion rate (audit-proof)
- Curriculum already built — turnkey delivery
- Only provider focused exclusively on adults 50+

### 2c. `context/writing-examples.md` — YOUR BEST WORK

Paste 3-5 of your best LinkedIn articles in full. You have 10 written and unposted — pick the strongest ones. Candidates from your content calendar:

1. "Why Your 50+ Workforce Is Your Biggest Untapped Asset"
2. "The $850 Billion Cost" (workforce director version)
3. "23 Organizations Reached Out — Here's What They Asked"
4. "Deploy This Quarter — A Workforce Leader's Action Plan"

Copy the full text of each article into this file.

### 2d. (Optional) `context/internal-links-map.md`

Add your key pages:

```
- Homepage: https://learnmoretechnologies.com/
- Workforce/B2B: https://learnmoretechnologies.com/workforce/
- Join (Individual): https://learnmoretechnologies.com/join-now/
- Speaking: https://learnmoretechnologies.com/speak/
```

### 2e. (Optional) `context/target-keywords.md`

Add keywords you want to rank for:

```
- AI training for adults 50+
- workforce development aging workforce
- WIOA digital skills training
- ageism in the workplace
- 50+ workforce training program
- MBE certified workforce training Texas
- AI workshops for older employees
```

---

## Step 3: Configure .env (Optional — Skip for Now)

Only needed if you want analytics-driven features (performance reviews, SERP analysis). Requires:

- [ ] Google Analytics 4 property ID + service account JSON
- [ ] Google Search Console access
- [ ] DataForSEO account ($50/mo for keyword data)

**Skip this for now.** You can write and research articles without it. Come back when you have a signed contract and need to optimize.

To set up later:
```bash
cp .env.example data_sources/config/.env
# Edit data_sources/config/.env with your credentials
```

---

## Step 4: WordPress Publishing (Optional — Skip for Now)

If you want to publish directly from SEO Machine to learnmoretechnologies.com:

- [ ] Upload `wordpress/seo-machine-yoast-rest.php` as MU-plugin on your WordPress site
- [ ] Create WordPress Application Password (Users > Your Profile > Application Passwords)
- [ ] Add WordPress credentials to `.env`

---

## Step 5: Test It

Once context files are filled out:

```bash
cd C:\Users\USER\seomachine

# Open in Claude Code
claude .

# Research a topic
/research AI training for adults 50+

# Check the research brief
# Look in research/ folder

# Write an article
/write Why Workforce Boards Should Fund AI Training for Adults 50+

# Check drafts/ folder for output
```

---

## Available Commands (Quick Reference)

| Command | What It Does |
|---------|-------------|
| `/research [topic]` | Keyword + competitor research, saves brief to `research/` |
| `/write [topic]` | Full SEO article (2000+ words) to `drafts/` |
| `/rewrite [topic]` | Update existing content |
| `/optimize [file]` | Final SEO polish pass |
| `/scrub [file]` | Remove AI-sounding patterns |
| `/publish-draft [file]` | Push to WordPress |
| `/repurpose [file]` | Adapt for LinkedIn, Medium, Reddit |
| `/research-serp [keyword]` | SERP analysis |
| `/research-gaps` | Competitor content gaps |
| `/research-trending` | Trending topics in your space |
| `/priorities` | Content prioritization matrix |
| `/cluster [topic]` | Full topic cluster strategy |

---

## Suggested First Articles (Revenue-Aligned)

These target the people who can write you a check:

1. **"How WIOA Funds Can Pay for AI Training for Adults 50+"** — targets workforce board directors searching for WIOA-eligible programs
2. **"The ROI of Training Your 50+ Workforce in AI"** — targets HR/L&D leaders at companies with 200+ employees
3. **"Why MBE-Certified Training Partners Outperform"** — targets procurement officers searching for diverse vendors
4. **"The $850 Billion Workforce Crisis No One Is Talking About"** — thought leadership that drives inbound

---

## File Structure

```
seomachine/
  context/         ← YOUR BRAND INFO (fill these out)
  research/        ← Research briefs (auto-generated)
  drafts/          ← Written articles (auto-generated)
  published/       ← Final versions
  rewrites/        ← Updated old content
  .claude/commands/ ← Slash commands
  .claude/agents/   ← Specialized AI agents
  data_sources/    ← Python analytics modules
```

---

## Next Action

- [ ] Fill out `context/brand-voice.md`
- [ ] Fill out `context/features.md`
- [ ] Paste writing examples into `context/writing-examples.md`
- [ ] Run `/research` on your first target topic
- [ ] Run `/write` to generate your first article
