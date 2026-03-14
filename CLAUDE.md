# CLAUDE.md — phllifesci Website Project
> Read this at the start of every session. This is the single source of truth for the site.

---

## 1. The Real Purpose of All of This

Before anything else, understand why this project exists.

**Dan Hall is a Business Development Manager at Zeta USA.** Everything on this site — both committees, the community work, the events, the network — is expressly in service of growing Dan's professional network and positioning him to sell more Zeta services. That is the primary business objective underlying all of this work.

This is not cynical. The community work is genuine. But the site, the analytics tool, the directory, the calendar — all of it should be built with the understanding that Dan is the face of this, his credibility and visibility are the product, and the people who interact with this site are ultimately part of a professional network that has real commercial value to him.

**When in doubt about what to build or how to position something, ask: does this make Dan look more credible, more connected, and more useful to the Philadelphia life sciences community?**

---

## 2. Who Dan Is

**Name:** Dan Hall
**Title:** Business Development Manager
**Company:** Zeta USA — King of Prussia, PA
**Email:** daniel.hall@zeta.com
**Location:** Philadelphia area (Conshohocken, PA)

**About Zeta USA:** Process-aware engineering and fabrication partner for liquid aseptic biopharma process systems. GMP-ready skids, digital traceability, simulation-driven engineering (INOSIM). Serves mAb, ADC, vaccine, plasma, cell & gene, and recombinant protein markets. Headquartered in King of Prussia with national coverage. Not a full EPCM firm — positioned as a process systems partner under EPC/owner umbrella.

**Community roles (both are professional strategy, not just volunteer work):**
- Co-Chair, ISPE Delaware Valley Chapter — Membership Committee
- Chair, Life Science Cares Philadelphia — Emerging Leaders Committee (founding)

---

## 3. What phllifesci.com Is

**URL:** phllifesci.com
**Hosting:** Netlify (free tier currently — may need to upgrade as site grows)
**Version control:** GitHub (under Dan's personal email)
**Stack:** Plain HTML/CSS/JS on the main site; React via CDN + Babel standalone on committee subpages (no build step)
**Fonts:** Google Fonts (Cormorant Garamond, Outfit on main site; DM Serif Display, DM Sans on subpages)

**Purpose:** A community hub for Philadelphia's life sciences professionals — primarily early-career individuals and those in career transition — to find connection, mentorship, and opportunity. Also serves experienced leaders and organizations looking to give back and invest in the region's talent pipeline.

**Tone:** Confident, civic, editorial. Like a well-written magazine about a city's professional community. Not corporate. Not casual. Authoritative but warm.

**Current vision:** A place Dan can send people so he doesn't have to re-explain himself. A clean, professional digital home for the work he's doing. Low effort to maintain, high credibility in appearance.

**One-year vision:** The go-to aggregator for the Philadelphia life sciences professional scene — a central place where people can follow what's happening across the community, find events, understand who's doing what, and plug in. Not a news site, not a nonprofit — a connective tissue platform built and maintained by one well-positioned person.

---

## 4. Current File Structure

```
phllifesci.com/
├── index.html                    ← Main landing page (LIVE)
├── ispe_dvc_membership.html      ← ISPE Membership Committee plan (LIVE)
└── lsc_el_masterplan_v5.html     ← LSC Emerging Leaders plan (LIVE)
```

**Do not rename or restructure existing files without explicit instruction from Dan — live links exist that would break.**

---

## 5. Target Site Architecture

Build toward this structure over time:

```
phllifesci.com/
├── index.html                  ← Landing page (add Calendar link to nav + CTA)
├── calendar.html               ← Aggregated events across both committees
├── ispe/
│   ├── index.html              ← ISPE committee hub (overview + links)
│   ├── roadmap.html            ← 90-day plan (migrated from ispe_dvc_membership)
│   ├── directory.html          ← Member directory (Google Sheets powered)
│   └── events.html             ← ISPE events (links out to Ticket Tailor)
└── lsc/
    ├── index.html              ← LSC committee hub (overview + links)
    ├── roadmap.html            ← 90-day plan (migrated from lsc_el_masterplan_v5)
    ├── directory.html          ← Member directory (Google Sheets powered)
    └── events.html             ← LSC events (links out to LSC site)
```

Events on the site link OUT to external registration — Ticket Tailor for ISPE, lifesciencecares.org for LSC. No on-site registration needed.

---

## 6. Design Reference — Spirit, Not Straitjacket

The existing site has a strong, distinctive aesthetic. Understand and respect it. Improve on it where you can. Do not abandon it without a reason and without flagging the change to Dan first.

### What exists and why it works
- **Cormorant Garamond** for display headlines — editorial, literary quality that sets it apart from typical professional org sites
- **Outfit** for body and UI — clean, modern, legible
- **Cream background (#F8F4EE)** with noise texture — warm, non-clinical, feels like high-quality print
- **Red (#C8202F)** used sparingly — italic headline emphasis, small accent dots and lines. Never large fills
- **Blue (#1B4DB8)** — ISPE identity color, links
- **Navy (#1B3A6B)** — dark surfaces, committee cards, footers
- **Scroll-reveal animations** on section elements — subtle, professional
- **Fixed nav** with blur backdrop
- **Independence Hall SVG watermark** — Philadelphia identity, hand-crafted feel
- **Max-width 1080px sections** — magazine column feel, not full-bleed
- **Section label system** — small caps label + red line accent before each section heading

### The aesthetic intent
Looks like a boutique consultancy or curated editorial platform. Not a nonprofit website. Not a corporate portal. Not a startup app. Restrained, high-contrast, typographically led.

### Where to improve
- Mobile responsiveness is underdeveloped — fix it
- Section transitions could be smoother
- New sections (directory, calendar, events) should feel native, not bolted on
- If you see a meaningfully better approach, propose it to Dan before implementing

### CSS Variables
```css
--cream:     #F8F4EE;
--parchment: #EDE8DF;
--stone:     #D8D2C8;
--ink:       #1A1714;
--mid:       #4A4440;
--muted:     #8C857C;
--red:       #C8202F;
--blue:      #1B4DB8;
--navy:      #1B3A6B;
```

---

## 7. The Two Committees

### ISPE Delaware Valley Chapter — Membership Committee

**Organization:** ISPE — global professional home for pharmaceutical engineers. Delaware Valley Chapter has 30+ year history.
**Dan's role:** Co-Chair
**Events platform:** Ticket Tailor — https://www.tickettailor.com/events/ispedvc

**Committee members:**
| Name | Title | Company | Role |
|------|-------|---------|------|
| Dan Hall | Business Development Manager | Zeta USA | Co-Chair |
| Anthony Cicamore | Business Development Manager | Burns & McDonnell | Corporate outreach |
| Emily Kate Simard | Mechanical Engineer | CRB | Corporate ask materials |
| Liah Osborne | Process Engineer | — | TBD |

**Mission:** Build engagement and early-career pipeline. Increase membership. Drive event attendance from end-user orgs and emerging leaders. Grow corporate relationships — this directly supports Dan's BD work at Zeta.

**90-day priorities:** First-timer tracking at events, 10+ corporate conversations, 3 board proposals (Ambassador Program, EL Dollar Match, Committee Prospectuses), shared workspace.

**The 90-day plan is a living document.** It should always reflect current active priorities, not become a static artifact.

---

### Life Science Cares Philadelphia — Emerging Leaders Committee

**Organization:** Life Science Cares — connects life sciences industry to underserved communities through volunteerism and philanthropy.
**Dan's role:** Chair (founding)
**Status:** NOT YET ESTABLISHED — founding phase, no Leads confirmed yet beyond Dan
**LSC staff contact:** Lexi Simchak (biweekly check-in)

**Mission:** Build early-career pipeline for LSC Philadelphia. Run the signature Fall event. Build corporate relationships. Establish the committee as a real contributor.

**2026 LSC Philadelphia events (all link out to lifesciencecares.org):**
- April 7 — Leadership Lunch + Underdog Series Session 2
- April 22 — Impact Reception (key anchor event for the committee)
- June 2 — Leadership Lunch + Underdog Series Session 3
- June 18 — Bases & Breakthroughs
- August 5 — Project Onramp Showcase & Reception
- September 22 — Leadership Lunch + Underdog Series Session 4
- Fall TBD — Emerging Leaders signature event (Dan's committee owns this)

**90-day priorities:** 3–5 Leads confirmed, show up at 2+ LSC events as a group, lock Fall event basics, 5+ corporate conversations, 10+ Members identified.

---

## 8. Content Management Philosophy

Dan does not write code. Dan prompts Claude Code in plain English. Build things so Dan never has to touch code to do routine updates.

- **Directory changes** → Dan edits a Google Sheet → site updates automatically
- **Event changes** → Dan updates Google Calendar → site reflects it
- **Everything else** → Dan describes it in plain English → Claude Code builds it

---

## 9. Directory Feature

**Goal:** Feature people prominently — a real showcase, not just a table.
**Required:** Name, title, company, contact info
**Nice to have:** Photo, LinkedIn, committee role
**Dan specifically** should be featured prominently as the person behind the site, with his Zeta affiliation visible. This is intentional and part of the commercial purpose.

---

## 10. How Dan Works — Rules for Claude Code

- Dan uses **voice dictation** — messages may be informal or loosely structured. Interpret charitably.
- Ask clarifying questions as a **simple bulleted list in plain text only** — no interactive widgets, no multi-select menus, no dropdown prompts.
- Always confirm before making irreversible changes to live files.
- Never rename existing files without explicit instruction.
- Flag breaking changes before making them.
- Build the simpler version first, show Dan, then expand.
- Prefer stability over cleverness — this needs to not break.
- Do not add dependencies requiring ongoing maintenance without flagging cost and complexity.

---

## 11. What This Is Not

Not a news site. Not a job board. Not a nonprofit website. Not a startup product. Not a platform requiring a team to maintain.

It is one person's professional digital infrastructure — built to serve his network, reflect his credibility, and advance his business development goals, while genuinely serving a community that benefits from having it exist.

---

*Last updated: March 2026 · Dan Hall · phllifesci.com*
