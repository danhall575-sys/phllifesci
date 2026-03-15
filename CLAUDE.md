# CLAUDE.md — phllifesci Website Project
> Read this at the start of every session. This is the single source of truth for the site.

---

## 1. The Real Purpose of All of This

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

**About Zeta USA:** Process-aware engineering and fabrication partner for liquid aseptic biopharma process systems. GMP-ready skids, digital traceability, simulation-driven engineering (INOSIM). Serves mAb, ADC, vaccine, plasma, cell & gene, and recombinant protein markets. Headquartered in King of Prussia. Not a full EPCM firm — positioned as a process systems partner under EPC/owner umbrella.

**Community roles (both are professional strategy, not just volunteer work):**
- Co-Chair, ISPE Delaware Valley Chapter — Membership Committee
- Chair, Life Science Cares Philadelphia — Emerging Leaders Committee (founding)

---

## 3. What phllifesci.com Is

**URL:** phllifesci.com
**Hosting:** Netlify (free tier)
**Version control:** GitHub (under Dan's personal email — danhall575)
**Stack:** Plain HTML/CSS/JS on main site; React via CDN + Babel standalone on committee subpages (no build step)
**Fonts:** Google Fonts

**Purpose:** A community hub for Philadelphia's life sciences professionals — primarily early-career individuals and those in career transition — to find connection, mentorship, and opportunity.

**Tone:** Confident, civic, editorial. Like a well-written magazine about a city's professional community. Not corporate. Not casual. Authoritative but warm.

**Current vision:** A place Dan can send people so he doesn't have to re-explain himself. Low effort to maintain, high credibility in appearance.

**One-year vision:** The go-to aggregator for the Philadelphia life sciences professional scene.

---

## 4. Current File Structure (DO NOT RENAME — live links exist)

```
phllifesci.com/
├── index.html                    ← Main landing page (LIVE)
├── ispe_dvc_membership.html      ← ISPE 90-day plan (LIVE)
├── lsc_el_masterplan_v5.html     ← LSC 90-day plan (LIVE)
└── ispe/
    └── index.html                ← ISPE committee hub (LIVE — built today)
```

---

## 5. Target Site Architecture

```
phllifesci.com/
├── index.html                  ← Landing page
├── ispe/
│   ├── index.html              ← ISPE hub (chapter health dashboard, mission, events carousel, committee members, links)
│   ├── roadmap.html            ← 90-day plan (visual refresh of ispe_dvc_membership.html)
│   ├── directory.html          ← Member directory (placeholder for now)
│   └── dashboard.html          ← Live chapter tracker (outward-facing, no personal data)
└── lsc/
    ├── index.html              ← LSC hub (mission, goals, events, directory, links)
    ├── roadmap.html            ← 90-day plan (visual refresh of lsc_el_masterplan_v5.html)
    ├── directory.html          ← Committee member directory (critical for LSC)
    └── events.html             ← LSC events (links out to lifesciencecares.org)
```

**Priority build order:**
1. Full visual redesign of index.html
2. Redesign ISPE hub (ispe/index.html)
3. Build ISPE dashboard (ispe/dashboard.html)
4. Visual refresh of both 90-day plan pages
5. Build LSC hub (lsc/index.html)
6. LSC directory and events pages
7. Calendar page (aggregated)

---

## 6. Design Direction — The Redesign Brief

### The problem with the current site
The site is too flat. While the cream palette gives a reserved, upscale feel, there is no dynamic range, no eye-catching elements, no moments that stop the eye. It needs more contrast, more tension, more visual hierarchy. It reads as a first draft of something good rather than the finished thing.

### The standard to hit
When someone lands on this site they should think a real firm built it. Not a side project. Not AI. References for the "this is a real website" quality level: zeta.com, jacobs.com, crbgroup.com. Not necessarily their aesthetic — their level of execution and polish.

### What works and must be preserved
- Cormorant Garamond for display headlines — keep it, it's distinctive
- The cream/navy/red color system — refine it, don't replace it
- The hero text and committee cards — structure is right, execution needs elevation
- The Independence Hall SVG watermark — Philadelphia identity, keep it
- The section label system — small caps + red line accent
- The editorial, restrained tone — add energy without losing intelligence
- Scroll-reveal animations — keep them, make them smoother

### What needs to change
- **Dynamic range** — the site needs moments of high contrast and visual tension
- **Typography scale** — headlines need to be bigger, bolder, more dramatic
- **Spacing** — more deliberate, more generous, more intentional
- **Mobile** — fully responsive on every single page, no exceptions
- **The 90-day plan pages** — strong content, weak visual execution, need a full refresh that brings them into the same design system as the rest of the site
- **The ISPE hub** — currently feels like a clone of the main page, needs its own identity

### Distinct committee identities within one system
- **ISPE** — established, institutional, precise, navy-led. Feels like it has 30 years of credibility behind it.
- **LSC** — energetic, civic, warmer, more movement. Feels like something being built right now.
- Both should be unmistakably part of the same site family

### Illustration + typography direction
No photography for now. Pure typography with illustration elements. Photography of people gets added later as the community grows. SVG illustrations, geometric elements, and typographic treatments are the visual language.

### Light theme with dark accent moments
Cream background stays primary. Navy dark sections used deliberately and sparingly for drama — not everywhere, but where they add weight and contrast.

### CSS Variables — do not change without flagging
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

### Before any redesign work
1. Read ALL existing HTML files in full
2. Write a complete design brief — what is changing, why, and what the new system looks like across every page
3. Wait for Dan's explicit approval before writing a single line of code

---

## 7. Page-by-Page Specifications

### index.html — Main Landing Page
- Keep overall structure: hero, city section, committee cards, who this is for, get involved
- Elevate the hero — it should stop people
- Committee cards need more visual weight and drama
- "Get Involved" links to dan.hall@zeta.com
- Dan's name appears in the footer — prominence level is fine there, don't over-feature

### ispe/index.html — ISPE Committee Hub
**First thing visible on page:** Chapter health dashboard — membership trend, key metrics, upcoming events. Outward-facing, no personal data, designed to motivate people and show chapter momentum.

**Page sections in order:**
1. Chapter health dashboard (membership number, trend visual, a key metric or two)
2. Upcoming events — carousel or card strip linking out to Ticket Tailor
3. Chapter and committee overview — mission, what we're building
4. Committee members — callout section (not the focus, but present)
5. Links to: 90-day roadmap, directory (placeholder), dashboard (full version)

**Note:** This page will be shared selectively at first, not fully public. Design for credibility, not mass audience.

### ispe/dashboard.html — Live Chapter Tracker
- Outward-facing version of the analytics data
- Shows membership health, trends, org engagement
- NO personal data, NO BD intelligence layer — that stays in the private analytics tool
- Should feel like a live dashboard — something the chapter can be proud of
- Data loaded manually by Dan via file upload (same Excel files)

### ispe_dvc_membership.html → ispe/roadmap.html (eventually)
- Keep the tabbed structure and all content exactly
- Visual refresh only — bring into the unified design system
- Do not break the existing URL until Dan explicitly says to migrate

### lsc/index.html — LSC Committee Hub
**Page sections:**
1. Mission and overall goals (pulled from the LSC 90-day plan HTML)
2. Events — cards or strip linking out to lifesciencecares.org events
3. Directory — committee members (critical for LSC, more so than ISPE)
4. Links to: 90-day roadmap, get involved

### lsc_el_masterplan_v5.html → lsc/roadmap.html (eventually)
- Keep the tabbed structure and all content
- Visual refresh to match unified design system
- Do not break existing URL until Dan says to migrate

---

## 8. ISPE Events — Ticket Tailor Carousel
The ISPE hub page should feature upcoming events from Ticket Tailor (https://www.tickettailor.com/events/ispedvc) as a carousel or horizontal card strip. Each card shows event name, date, and a link out to register. This should feel dynamic and alive — not a static list.

---

## 9. The Two Committees

### ISPE Delaware Valley Chapter — Membership Committee
**Dan's role:** Co-Chair
**Events:** Ticket Tailor — https://www.tickettailor.com/events/ispedvc

| Name | Title | Company | Role |
|------|-------|---------|------|
| Dan Hall | Business Development Manager | Zeta USA | Co-Chair |
| Anthony Cicamore | Business Development Manager | Burns & McDonnell | Corporate outreach |
| Emily Kate Simard | Mechanical Engineer | CRB | Corporate ask materials |
| Liah Osborne | Process Engineer | — | Committee member |

**Mission:** Build engagement and early-career pipeline. Increase membership. Drive event attendance from end-user orgs and emerging leaders.

**The 90-day plan is a living document** — always reflects current priorities, never becomes static.

### Life Science Cares Philadelphia — Emerging Leaders Committee
**Dan's role:** Chair (founding)
**Status:** Founding phase — no Leads confirmed yet beyond Dan
**LSC contact:** Lexi Simchak

**2026 LSC Philadelphia events (link out to lifesciencecares.org):**
- April 7 — Leadership Lunch + Underdog Series Session 2
- April 22 — Impact Reception
- June 2 — Leadership Lunch + Underdog Series Session 3
- June 18 — Bases & Breakthroughs
- August 5 — Project Onramp Showcase & Reception
- September 22 — Leadership Lunch + Underdog Series Session 4
- Fall TBD — Emerging Leaders signature event (Dan's committee owns this)

---

## 10. Content Management Philosophy

Dan does not write code. Dan prompts Claude Code in plain English.

- **Directory updates** → Google Sheet → auto-renders on site
- **Event updates** → Google Calendar or manual update → site reflects it
- **Everything else** → plain English prompt to Claude Code

---

## 11. How Dan Works — Rules for Claude Code

- Dan uses **voice dictation** — interpret loosely structured messages charitably
- Ask clarifying questions as a **simple bulleted list in plain text** — never interactive widgets or multi-select menus
- Always confirm before irreversible changes to live files
- Never rename existing files without explicit instruction
- Flag breaking changes before making them
- Build simpler version first, show Dan, then expand
- Prefer stability over cleverness
- No new dependencies without flagging cost and complexity
- **Always write a plan and get approval before building**
- **Always read CLAUDE.md at the start of every session**

---

## 12. What This Is Not

Not a news site. Not a job board. Not a nonprofit. Not a startup product. Not a platform requiring a team to maintain.

One person's professional digital infrastructure — built to serve his network, reflect his credibility, and advance his business development goals, while genuinely serving a community that benefits from having it exist.

---

*Last updated: March 2026 · Dan Hall · phllifesci.com*
