# PRD: faniefikri.com — Personal Website

> **Author:** Fanie Fikri
> **Date:** 2026-03-18
> **Status:** Draft
> **Target ship date:** One burst session (6-10 hrs)

---

## 1. Purpose

A single home base on the internet that answers three questions for anyone who lands on it:

1. **Who is this person?** → Fintech strategist in Jakarta who builds AI-powered tools on the side.
2. **What has he shipped?** → A growing list of real projects with live links.
3. **How do I connect?** → GitHub, LinkedIn, X, email — all one click away.

This is NOT a blog. NOT a portfolio agency site. NOT a startup landing page. It's a personal hub that grows with every project shipped — the single URL you put in every bio, every email signature, every GitHub README.

---

## 2. Target Visitors

| Who | Why they're here | What they need to see |
|-----|-----------------|----------------------|
| **Fellow builders / indie hackers** | Found you on X or GitHub | Projects list, tech stack, links to repos |
| **Professional network** | LinkedIn click-through, conference follow-up | Credibility — role, background, what you're building |
| **Potential collaborators** | Interested in working together | Contact method, proof you ship things |
| **Future you** | Portfolio review, motivation | A growing record of everything you've built |

---

## 3. Design Direction

**Style:** Modern indie builder — warm, approachable, credible. Not corporate, not hacker-dark, not bare-bones.

**Visual identity:**
- Light background, clean typography
- Accent color: purple-teal gradient (represents the intersection of business/strategy and tech/building)
- Avatar or initials circle as visual anchor
- Tag pills for domains (fintech, AI tools, vibe coding)
- Project cards with status badges (live, building, soon)
- Generous whitespace — let it breathe

**Tone of copy:** First person, direct, slightly informal. "I work in fintech by day and ship AI-powered tools by night." Not "Fanie is a results-driven professional with a passion for..." — no third-person LinkedIn speak.

**Typography:**
- One distinctive display/heading font (not Inter, not Roboto — something with character)
- One clean body font
- Monospace for tech tags and project metadata

**References to study:**
- The warmth of a good indie hacker "about" page
- The clarity of a Linktree (every link visible, nothing buried)
- The credibility of a minimal startup founder page

---

## 4. Site Structure

Single page, 5 sections, scroll-based. No routing, no navigation menu needed for v1.

### Section 1: Hero
- Initials avatar (FF) or photo (decide later)
- Name: **Fanie Fikri**
- One-liner: "Fintech strategist turned AI builder. Shipping from Jakarta."
- Tag pills: `fintech` · `AI tools` · `vibe coding` · `Jakarta`
- Social links row: GitHub · LinkedIn · X · Email (icons, not text)

### Section 2: About (2-3 sentences max)
- What you do by day (fintech strategy at a major Indonesian tech company — NO company name)
- What you do by night (building AI-powered tools, learning to code)
- The angle: "Business person who knows what to build, now learning how to build it"

### Section 3: Projects
- Card grid (1-2 columns on mobile, 2 columns on desktop)
- Each card shows:
  - Project name
  - One-line description
  - Tech tags (Python, Telegram API, etc.)
  - Status badge: `live` (green) / `building` (amber) / `soon` (gray)
  - Link to repo or live project
- Start with 1 card (X-Bookmark Digest Bot). The grid grows as you ship.
- Empty state for "coming soon" slots is fine — shows momentum

**Project card for v1:**

| Field | Value |
|-------|-------|
| Name | X-Bookmark Digest Bot |
| Description | Scans X bookmarks and sends a daily Telegram digest of what to build next |
| Stack | Python · Telegram Bot API · X API |
| Status | Live |
| Link | GitHub repo |

### Section 4: Now (optional but recommended)
- A "what I'm currently working on" section — 2-3 bullet points max
- Updated manually whenever priorities change
- Inspired by Derek Sivers' /now page concept
- Example: "Building my personal site (you're looking at it)" / "Learning FastAPI" / "Ramadan mode — lower output"

### Section 5: Contact
- Simple line: "Want to build something together? Say hi."
- Email link (mailto:) — no contact form for v1, that's overengineering
- Repeat social links (GitHub, LinkedIn, X)

---

## 5. What's NOT in v1

These are explicitly out of scope. Don't build them. Don't plan for them. Ship without them.

- ❌ Blog / writing section (add in v2 if content strategy materializes)
- ❌ Dark mode toggle (nice-to-have, not v1)
- ❌ Contact form (mailto is fine)
- ❌ Analytics dashboard (add Plausible or SimpleAnalytics later)
- ❌ CMS or admin panel (edit HTML directly — you have 5 sections)
- ❌ Animations or transitions (ship plain, polish later)
- ❌ Multi-page routing (single page, scroll)
- ❌ SEO optimization beyond basics (meta tags, og:image — that's it)
- ❌ Indonesian language version (English only for v1 — broader reach)

---

## 6. Tech Stack

| Layer | Choice | Why |
|-------|--------|-----|
| **Language** | HTML + CSS + minimal JS | You're learning these — this IS the learning project |
| **Framework** | None | A personal site doesn't need React. Plain HTML is faster to ship and easier to understand. |
| **Styling** | Single CSS file | No Tailwind, no preprocessors. Write real CSS, learn real CSS. |
| **Fonts** | Google Fonts (2 fonts max) | Free, fast CDN, huge selection |
| **Icons** | Lucide or Feather icons (SVG) | Clean, consistent, lightweight |
| **Hosting** | **Cloudflare Pages** (recommended) | Free. Fast global CDN. Dead-simple deploy from GitHub. Custom domain support. Zero config. |
| **Domain** | faniefikri.com (already owned) | Connect to Cloudflare Pages via DNS |
| **Version control** | GitHub public repo | This repo IS a portfolio piece — clean commits, good README |

### Why Cloudflare Pages over alternatives:
- **vs Oracle VM:** Your VM is for backend projects (bots, APIs). A static site doesn't need a VM. Cloudflare Pages is faster, free, and zero maintenance.
- **vs Vercel:** Both excellent. Cloudflare is slightly better for pure static sites — no cold starts, no edge function complexity. Also easier DNS if you move your domain to Cloudflare.
- **vs Netlify:** Also fine. Cloudflare wins on speed in Southeast Asia (closer edge nodes to Jakarta).

---

## 7. File Structure

```
faniefikri.com/
├── index.html          ← the entire site
├── style.css           ← all styles
├── assets/
│   ├── avatar.jpg      ← photo (optional, can use initials)
│   └── og-image.png    ← social sharing preview image
├── README.md           ← project documentation (this IS a portfolio piece)
└── .gitignore
```

That's it. Four files that matter. This ships in one burst.

---

## 8. Content Draft

### Hero one-liner options (pick one):
1. "Fintech strategist turned AI builder. Shipping from Jakarta."
2. "I build AI-powered tools from Jakarta. Fintech by day, side projects by night."
3. "Business person learning to build. One shipped project at a time."

### About section draft:
> By day, I work in fintech strategy at one of Indonesia's largest tech companies — partnerships, product, venture building. By night, I'm teaching myself to code with AI and shipping tools that solve problems I actually have.
>
> I'm not a developer by training. I'm a business person who got tired of having ideas and no way to build them. So I started.

### Contact section draft:
> Want to build something together, talk fintech, or just say hi?
> Reach me at [email] or find me on [GitHub] · [LinkedIn] · [X].

---

## 9. Hosting Setup Steps (When Ready to Deploy)

1. Push code to GitHub repo (`faniefikri/faniefikri.com` or similar)
2. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
3. Connect GitHub account → select repo
4. Build settings: none needed (it's static HTML)
5. Deploy → get a `.pages.dev` URL instantly
6. Add custom domain: `faniefikri.com` → follow Cloudflare DNS instructions
7. SSL is automatic. You're live.

Total deploy time: ~15 minutes.

---

## 10. Success Criteria

**Ship criteria (v1 is done when):**
- [ ] Site loads at faniefikri.com
- [ ] All 5 sections present and readable
- [ ] All social links work (GitHub, LinkedIn, X, email)
- [ ] X-Bookmark Digest Bot project card links to live repo
- [ ] Looks good on mobile (test on your phone)
- [ ] og:image and meta tags set (so link previews look good when shared)
- [ ] GitHub repo is public with a clean README

**NOT success criteria for v1:**
- Pixel-perfect design (good enough is good enough)
- Perfect copy (you'll iterate)
- Google ranking (not the goal right now)

---

## 11. What You'll Learn Building This

This project is a learning investment, not a revenue play. Be explicit about that.

| Skill | How this project teaches it |
|-------|-----------------------------|
| HTML structure | Building semantic sections, links, images |
| CSS layout | Flexbox, grid, responsive design, typography |
| Git workflow | Commits, push, public repo, README writing |
| Deployment | Cloudflare Pages, DNS, custom domains |
| Spec-driven dev | You're using THIS document to guide the build |
| Reading AI code | After AI generates each section, spend 15 min understanding it |

---

## 12. Build Plan (One Burst Session)

Estimated total: 4-6 hours in one sitting.

| Step | Task | Time est. |
|------|------|-----------|
| 1 | Set up repo, file structure, blank index.html | 15 min |
| 2 | Build Hero section (HTML + CSS) | 45 min |
| 3 | Build About section | 20 min |
| 4 | Build Projects section with 1 card | 45 min |
| 5 | Build Now section | 15 min |
| 6 | Build Contact section | 15 min |
| 7 | Responsive CSS (test on mobile) | 30 min |
| 8 | Meta tags, og:image, favicon | 20 min |
| 9 | Deploy to Cloudflare Pages | 15 min |
| 10 | Connect custom domain | 15 min |
| 11 | Write README for the repo | 15 min |
| 12 | Final check on phone + share link | 10 min |
| | **Total** | **~4-5 hours** |

**Rule:** If any step takes more than 2x the estimate, skip it and come back. Ship the site with 80% done rather than not shipping at 100%.

---

## 13. After v1 Ships

Park these for later. Don't touch them until v1 is live.

| Enhancement | When |
|-------------|------|
| Add project #2 card | When project #2 ships |
| Dark mode | When bored on a low-energy day |
| Simple analytics (Plausible) | When you care about traffic |
| Blog/writing section | When content strategy is clear |
| Indonesian language toggle | When Bahasa content exists |
| Subtle animations/transitions | When the base design feels stale |
| Contact form (if email gets spam) | When it's actually a problem |

---

*"Ship the site. Add to it every time you ship something new. The site grows as you grow."*
