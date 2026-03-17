# faniefikri.com — Build Tickets

> **Reference:** Use alongside `faniefikri-website-prd.md`
> **How to use:** Hand each coding ticket to your AI agent (Copilot/Codex) one at a time. Complete the manual tasks yourself. Go in order — each ticket builds on the previous one.
> **Rule:** After each coding ticket, spend 10-15 min reading the generated code before moving to the next ticket. This is how you learn.

---

## MANUAL TASK 1: Create GitHub Repo

**Do this first, before any coding.**

1. Go to github.com/new
2. Repo name: `faniefikri.com` (or `personal-site` — your call)
3. Set to **Public** (this repo IS a portfolio piece)
4. Check "Add a README"
5. Add `.gitignore` → select `Node` (covers common junk files)
6. Clone to your local machine: `git clone https://github.com/faniefikri/faniefikri.com.git`
7. Open the project folder in your editor (VS Code recommended — Copilot lives here)

**Done when:** You have an empty repo locally with just README.md and .gitignore.

---

## CODING TICKET 1: Scaffolding

**Hand this entire block to your AI agent:**

```
Create the file structure for a static personal website. No frameworks, no build tools, plain HTML + CSS.

Create these files:
- index.html
- style.css

In index.html:
- DOCTYPE, html lang="en", head, body
- In <head>: charset utf-8, viewport meta tag, title "Fanie Fikri — Builder"
- Link to style.css
- Link to Google Fonts: pick ONE distinctive display font (NOT Inter, NOT Roboto, NOT Arial — something with character like "Sora", "General Sans", "Outfit", "Satoshi", or "Cabinet Grotesk" — use whatever is available on Google Fonts) and one clean body font (like "DM Sans" or "Plus Jakarta Sans")
- Body should have 5 empty sections with ids: hero, about, projects, now, contact
- Each section should have a comment placeholder like <!-- Hero section -->

In style.css:
- CSS reset (box-sizing border-box, margin 0, padding 0)
- CSS variables at :root for:
  - --color-bg: #FAFAFA
  - --color-bg-card: #FFFFFF
  - --color-text: #1A1A1A
  - --color-text-muted: #6B7280
  - --color-text-light: #9CA3AF
  - --color-accent-purple: #7F77DD
  - --color-accent-teal: #1D9E75
  - --color-accent-gradient: linear-gradient(135deg, #AFA9EC, #5DCAA5)
  - --color-tag-fintech-bg: #EEEDFE
  - --color-tag-fintech-text: #534AB7
  - --color-tag-ai-bg: #E1F5EE
  - --color-tag-ai-text: #0F6E56
  - --color-tag-vibe-bg: #FAEEDA
  - --color-tag-vibe-text: #854F0B
  - --color-badge-live-bg: #E1F5EE
  - --color-badge-live-text: #0F6E56
  - --color-badge-building-bg: #FAEEDA
  - --color-badge-building-text: #854F0B
  - --color-badge-soon-bg: #F1EFE8
  - --color-badge-soon-text: #5F5E5A
  - --font-display: (the display font you chose)
  - --font-body: (the body font you chose)
  - --font-mono: "JetBrains Mono", "Fira Code", monospace
  - --max-width: 640px
  - --spacing-section: 4rem
- Body: background var(--color-bg), font-family var(--font-body), color var(--color-text), line-height 1.7, font-size 16px
- A .container class: max-width var(--max-width), margin 0 auto, padding 0 1.5rem
- Section spacing: each section gets padding var(--spacing-section) 0

Do NOT add any content yet. Just the skeleton and styles.
```

**Acceptance criteria:**
- [ ] index.html opens in browser with blank white page, no errors in console
- [ ] Google Fonts load (check Network tab)
- [ ] All 5 sections exist as empty divs with correct IDs
- [ ] CSS variables are defined and the body has correct background/font

---

## CODING TICKET 2: Hero Section

**Hand this to your AI agent:**

```
Build the Hero section inside the #hero div in index.html. Reference style.css for all styling.

Layout (centered, stacked vertically):
1. Initials avatar circle:
   - 72px circle
   - Background: var(--color-accent-gradient)
   - White text "FF" centered, font-weight 600, font-size 24px
   - margin-bottom: 1.5rem

2. Name:
   - <h1> "Fanie Fikri"
   - Font: var(--font-display), font-size 2rem, font-weight 700
   - margin-bottom: 0.5rem

3. One-liner:
   - <p> "Fintech strategist turned AI builder. Shipping from Jakarta."
   - Color: var(--color-text-muted), font-size 1.1rem
   - margin-bottom: 1.5rem

4. Tag pills row (horizontal, centered, wrapping):
   - Four pills: "fintech", "AI tools", "vibe coding", "Jakarta"
   - Each pill: font-size 0.8rem, padding 0.35rem 0.85rem, border-radius 100px, font-family var(--font-mono)
   - "fintech" uses tag-fintech-bg and tag-fintech-text colors
   - "AI tools" uses tag-ai-bg and tag-ai-text colors
   - "vibe coding" uses tag-vibe-bg and tag-vibe-text colors
   - "Jakarta" uses tag-soon-bg and tag-soon-text colors (gray)
   - Gap between pills: 0.5rem
   - margin-bottom: 1.5rem

5. Social links row (horizontal, centered):
   - Four links: GitHub, LinkedIn, X (Twitter), Email
   - Use inline SVG icons (from Lucide or Feather icon set), 20px size
   - Icon color: var(--color-text-light), hover: var(--color-text)
   - Gap: 1rem
   - GitHub → https://github.com/faniefikri
   - LinkedIn → https://linkedin.com/in/faniefikri
   - X → https://x.com/faniefikri (placeholder, update later)
   - Email → mailto:fanie@faniefikri.com (placeholder)
   - All links open in new tab (target="_blank" rel="noopener")

The entire hero section should be centered (text-align center) and wrapped in a .container div.
```

**Acceptance criteria:**
- [ ] FF gradient circle renders correctly
- [ ] Name is large and uses display font
- [ ] One-liner is muted color, readable
- [ ] All 4 tag pills show with correct colors
- [ ] All 4 social icons render and are clickable
- [ ] Everything is centered on desktop and mobile

---

## CODING TICKET 3: About Section

**Hand this to your AI agent:**

```
Build the About section inside the #about div in index.html.

Layout:
1. Section heading (optional — can skip if it flows naturally from hero):
   - If using a heading: <h2> "About" — font-size 1.3rem, font-weight 600, margin-bottom 1rem
   - Or skip the heading and just flow the text naturally

2. Two paragraphs of body text:

   Paragraph 1:
   "By day, I work in fintech strategy at one of Indonesia's largest tech companies — partnerships, product, venture building. By night, I'm teaching myself to code with AI and shipping tools that solve problems I actually have."

   Paragraph 2:
   "I'm not a developer by training. I'm a business person who got tired of having ideas and no way to build them. So I started."

3. Styling:
   - font-size: 1rem (body default)
   - color: var(--color-text)
   - line-height: 1.7
   - Paragraph spacing: margin-bottom 1rem
   - Wrap in .container

Keep it simple. No cards, no special styling. Just clean readable text.
```

**Acceptance criteria:**
- [ ] Two paragraphs render cleanly
- [ ] Text is readable, proper line-height
- [ ] No company name mentioned (just "one of Indonesia's largest tech companies")
- [ ] Wraps properly on mobile

---

## CODING TICKET 4: Projects Section

**Hand this to your AI agent:**

```
Build the Projects section inside the #projects div in index.html.

Layout:
1. Section heading:
   - <h2> "Projects"
   - font-size: 1.3rem, font-weight: 600, margin-bottom: 1.5rem

2. Project cards grid:
   - CSS Grid: 1 column on mobile (<640px), 2 columns on desktop
   - Gap: 1rem

3. Project card component (create as a reusable structure):
   - Background: var(--color-bg-card)
   - Border: 1px solid #E5E7EB
   - Border-radius: 12px
   - Padding: 1.25rem
   - On hover: subtle border color change to #D1D5DB (optional, not critical for v1)

   Inside each card:
   a. Top row: project name + status badge
      - Project name: <h3>, font-size 1rem, font-weight 600
      - Status badge: font-size 0.7rem, padding 0.2rem 0.6rem, border-radius 100px
      - Badge colors from CSS variables: live = badge-live colors, building = badge-building, soon = badge-soon

   b. Description:
      - <p>, font-size 0.9rem, color var(--color-text-muted), margin 0.75rem 0

   c. Tech tags row:
      - Font-family: var(--font-mono), font-size 0.75rem, color var(--color-text-light)
      - Tags separated by " · " (middot)

   d. Link:
      - <a> wrapping the entire card (or a small "View →" link at bottom)
      - Opens in new tab

4. Card data for v1 (only 1 real card + 1 placeholder):

   Card 1 (real):
   - Name: "X-Bookmark Digest Bot"
   - Status: "live"
   - Description: "Scans X bookmarks and sends a daily Telegram digest of what to build next."
   - Tech: "Python · Telegram Bot API · X API"
   - Link: https://github.com/faniefikri (update to actual repo later)

   Card 2 (placeholder):
   - Name: "Project #2"
   - Status: "soon"
   - Description: "Coming soon. Currently in the idea phase."
   - Tech: "TBD"
   - Link: none (no link, slightly lower opacity: 0.6)

Wrap everything in .container.
```

**Acceptance criteria:**
- [ ] Two cards render in a grid (2 columns desktop, 1 column mobile)
- [ ] Card 1 has green "live" badge
- [ ] Card 2 has gray "soon" badge and is slightly faded
- [ ] Tech tags use monospace font
- [ ] Cards have proper borders and border-radius
- [ ] Card 1 links to GitHub (new tab)

---

## CODING TICKET 5: Now Section

**Hand this to your AI agent:**

```
Build the Now section inside the #now div in index.html.

This is inspired by Derek Sivers' /now page concept — a short "what I'm up to right now" list.

Layout:
1. Section heading:
   - <h2> "Now"
   - font-size: 1.3rem, font-weight: 600, margin-bottom: 0.25rem

2. Subheading:
   - <p> "What I'm focused on right now."
   - font-size: 0.9rem, color: var(--color-text-light), margin-bottom: 1rem

3. List of 3 items (use a simple unordered list or just paragraphs with bullet-style):
   - "Building this website (you're looking at it)"
   - "Learning HTML, CSS, and JavaScript fundamentals"
   - "Ramadan mode — shipping when energy allows"

4. Styling:
   - List items: font-size 0.95rem, color var(--color-text-muted), line-height 1.7
   - Spacing between items: 0.5rem
   - Use a subtle left border accent (3px solid with var(--color-accent-teal)) on the entire list container as a visual anchor
   - padding-left on the list container: 1rem

5. Small note at bottom:
   - <p> "Last updated: March 2026"
   - font-size: 0.75rem, color: var(--color-text-light), margin-top: 1rem

Wrap in .container.
```

**Acceptance criteria:**
- [ ] Three bullet points render cleanly
- [ ] Subtle left border accent visible
- [ ] "Last updated" date is visible
- [ ] Section feels light and scannable (not heavy)
- [ ] Works on mobile

---

## CODING TICKET 6: Contact + Footer

**Hand this to your AI agent:**

```
Build the Contact section inside the #contact div in index.html, plus a simple footer.

Contact section layout:
1. Section heading:
   - <h2> "Say hi"
   - font-size: 1.3rem, font-weight: 600, margin-bottom: 1rem

2. Contact text:
   - <p> "Want to build something together, talk fintech, or just say hi?"
   - font-size: 1rem, color: var(--color-text-muted), margin-bottom: 1rem

3. Email link:
   - <a href="mailto:fanie@faniefikri.com"> styled as a simple text link
   - Color: var(--color-accent-purple), no underline, underline on hover
   - Display the email address as text

4. Social links row (repeat from hero — same icons, same links):
   - GitHub, LinkedIn, X, Email
   - Same SVG icons, same styling as hero section
   - Centered, margin-top: 1.5rem

Footer:
- Simple <footer> after the contact section
- Text: "© 2026 Fanie Fikri. Built with HTML, CSS, and AI."
- font-size: 0.8rem, color: var(--color-text-light), text-align: center
- Padding: 2rem 0
- Border-top: 1px solid #E5E7EB

Wrap contact content in .container. Footer can be full-width with its own container.
```

**Acceptance criteria:**
- [ ] "Say hi" heading renders
- [ ] Email is clickable (opens mail client)
- [ ] Social icons are present and match hero section
- [ ] Footer shows at bottom with copyright
- [ ] "Built with HTML, CSS, and AI" — honest and on-brand

---

## CODING TICKET 7: Responsive Pass

**Hand this to your AI agent:**

```
Review the entire index.html and style.css and make the site fully responsive.

Requirements:

1. Mobile (< 640px):
   - Container padding: 0 1.25rem
   - Hero heading: font-size 1.6rem
   - Project cards: single column (1fr)
   - Tag pills: allow wrapping to 2 lines if needed
   - Social icons: keep in one row, reduce gap if needed
   - All text should be readable without horizontal scrolling

2. Tablet (640px - 1024px):
   - Project cards: 2 columns
   - Everything else stays the same

3. Desktop (> 1024px):
   - Max-width container keeps content centered and readable
   - No changes needed beyond what .container already does

4. General:
   - No horizontal scroll at any viewport width
   - All touch targets (links, icons) are at least 44px tap area
   - Images (if any) are max-width: 100%
   - Test: resize browser from 320px to 1440px — nothing should break

Use @media queries in style.css. Keep them at the bottom of the file, organized by breakpoint.

Do NOT add any new content. Only adjust existing layout and sizing.
```

**Acceptance criteria:**
- [ ] Site looks good at 375px wide (iPhone SE)
- [ ] Site looks good at 768px wide (iPad)
- [ ] Site looks good at 1440px wide (desktop)
- [ ] No horizontal scrolling at any width
- [ ] Project cards stack on mobile, grid on desktop
- [ ] All links/icons are easy to tap on mobile

---

## CODING TICKET 8: Meta Tags + OG Image

**Hand this to your AI agent:**

```
Add meta tags and Open Graph tags to the <head> of index.html for proper link previews when shared on social media.

Add these meta tags:
1. <meta name="description" content="Fanie Fikri — Fintech strategist turned AI builder. Shipping tools from Jakarta.">
2. <meta name="author" content="Fanie Fikri">

3. Open Graph tags:
   - og:title = "Fanie Fikri — Builder"
   - og:description = "Fintech strategist turned AI builder. Shipping from Jakarta."
   - og:type = "website"
   - og:url = "https://faniefikri.com"
   - og:image = "https://faniefikri.com/assets/og-image.png"

4. Twitter Card tags:
   - twitter:card = "summary_large_image"
   - twitter:title = "Fanie Fikri — Builder"
   - twitter:description = "Fintech strategist turned AI builder. Shipping from Jakarta."
   - twitter:image = "https://faniefikri.com/assets/og-image.png"

5. Favicon:
   - Add a simple SVG favicon with the letters "FF" in white on the accent gradient background
   - Use inline data URI: <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,...">

6. Also create a simple og-image-template.html that I can screenshot to use as my og:image:
   - Dimensions: 1200x630px (set as a fixed-size div)
   - Background: white
   - Centered content: "FF" gradient circle (same as hero) + "Fanie Fikri" in display font + one-liner below
   - Include the same Google Fonts as the main site
   - This is just a template I'll screenshot — not automated

Do NOT change any existing content or layout.
```

**Acceptance criteria:**
- [ ] View page source shows all meta tags in head
- [ ] Favicon shows in browser tab
- [ ] og-image-template.html exists and looks good when opened in browser
- [ ] Test URL in https://www.opengraph.xyz/ after deploy

---

## CODING TICKET 9: README

**Hand this to your AI agent:**

```
Create a README.md for this project repository. This README is a portfolio piece — it should be clean, informative, and show that the author thinks carefully about documentation.

Structure:

# faniefikri.com

One-liner description: "Personal website and project hub. Built with plain HTML, CSS, and a lot of AI assistance."

## About

2-3 sentences: This is my personal home on the internet. It lists my projects, background, and ways to connect. Built as a learning project while teaching myself web development with AI.

## Tech Stack

- HTML5 + CSS3 (no frameworks)
- Google Fonts
- Hosted on Cloudflare Pages
- Domain: faniefikri.com

## Project Structure

Show the file tree:
faniefikri.com/
├── index.html
├── style.css
├── assets/
│   ├── og-image.png
│   └── (other assets)
├── README.md
└── .gitignore

## Development

"Clone the repo and open index.html in your browser. That's it. No build step, no dependencies, no package manager."

## Author

Fanie Fikri
GitHub: https://github.com/faniefikri
LinkedIn: https://linkedin.com/in/faniefikri
Website: https://faniefikri.com

Keep it concise. No emoji overload. No badges unless they add real info. No license section needed.
```

**Acceptance criteria:**
- [ ] README.md is well-structured and readable
- [ ] File tree matches actual project structure
- [ ] Links to social profiles are correct
- [ ] Someone landing on the GitHub repo understands what this is in 10 seconds

---

## MANUAL TASK 2: Commit and Push

After all 9 coding tickets are done:

1. Open terminal in your project folder
2. Run:
   ```
   git add .
   git commit -m "feat: initial personal website v1"
   git push origin main
   ```
3. Go to github.com/faniefikri/faniefikri.com and verify everything is there

**Better approach — commit after each ticket:**
```
git add . && git commit -m "feat: scaffolding and CSS variables"
git add . && git commit -m "feat: hero section"
git add . && git commit -m "feat: about section"
git add . && git commit -m "feat: projects section with cards"
git add . && git commit -m "feat: now section"
git add . && git commit -m "feat: contact and footer"
git add . && git commit -m "fix: responsive pass"
git add . && git commit -m "feat: meta tags, og image, favicon"
git add . && git commit -m "docs: README"
git push origin main
```

Cleaner commit history = better portfolio piece.

---

## MANUAL TASK 3: Deploy to Cloudflare Pages

1. Go to [pages.cloudflare.com](https://pages.cloudflare.com) and sign up (free)
2. Click "Create a project" → "Connect to Git"
3. Authorize GitHub and select your `faniefikri.com` repo
4. Build settings:
   - **Framework preset:** None
   - **Build command:** (leave empty)
   - **Build output directory:** `/` (root — your index.html is at the root)
5. Click "Save and Deploy"
6. Wait ~1 minute. You'll get a URL like `faniefikri-com.pages.dev`
7. Open that URL and verify the site works

**Done when:** Your site is live at `*.pages.dev` and all sections render correctly.

---

## MANUAL TASK 4: Connect Your Domain

1. In Cloudflare Pages dashboard, go to your project → "Custom domains"
2. Click "Set up a custom domain"
3. Enter: `faniefikri.com`
4. Cloudflare will show you DNS records to add
5. If your domain is already on Cloudflare DNS: it'll auto-configure
6. If your domain is on another registrar (Namecheap, GoDaddy, etc.):
   - Option A: Transfer nameservers to Cloudflare (recommended — free, gives you Cloudflare DNS)
   - Option B: Add a CNAME record pointing to your `*.pages.dev` URL
7. Wait for DNS propagation (usually 5-30 minutes, can take up to 24 hours)
8. SSL certificate is automatic — no action needed

**Done when:** `https://faniefikri.com` loads your site with a valid SSL certificate.

---

## MANUAL TASK 5: Create OG Image

1. Open the `og-image-template.html` file (from Ticket 8) in your browser
2. Set browser window to roughly 1200x630px
3. Take a screenshot (or use a browser extension like "GoFullPage")
4. Crop to exactly the template area
5. Save as `assets/og-image.png`
6. Commit and push:
   ```
   git add assets/og-image.png
   git commit -m "feat: add og image for social previews"
   git push
   ```
7. Cloudflare Pages will auto-redeploy (~1 min)
8. Test your link preview at https://www.opengraph.xyz/

---

## MANUAL TASK 6: Final Checklist

Open your site on your phone and go through this:

- [ ] Site loads at faniefikri.com (not just pages.dev)
- [ ] FF avatar circle looks correct
- [ ] Name and one-liner are readable
- [ ] All 4 tag pills show with correct colors
- [ ] GitHub link → opens your GitHub profile
- [ ] LinkedIn link → opens your LinkedIn
- [ ] X link → opens your X profile
- [ ] Email link → opens mail client
- [ ] About text reads well, no company name visible
- [ ] Project card shows "X-Bookmark Digest Bot" with green "live" badge
- [ ] Project card link goes to correct repo
- [ ] "Now" section has 3 items with left border accent
- [ ] Contact email is clickable
- [ ] Footer shows at bottom
- [ ] No horizontal scrolling on mobile
- [ ] Share the URL in WhatsApp/Telegram and check link preview shows og:image

**If something is broken:** Don't fix it yourself in raw code. Open your AI agent and describe what's wrong — let it fix it. That's the workflow.

---

## MANUAL TASK 7: Update Your Profiles

Immediately after shipping:

1. **GitHub profile** → add `faniefikri.com` to your bio
2. **LinkedIn** → add website URL to contact info
3. **X bio** → add `faniefikri.com`
4. **vibe-coding-journey.md** → move "Personal branding website" to "Shipped Projects" section
5. **Email signature** (optional) → add the URL

**You now have 2 shipped projects. Next one starts when energy allows.**

---

*Total estimated time: 4-6 hours in one burst. If it takes longer, that's fine. If any single ticket takes more than 1 hour, skip the polish and move to the next one. Ship at 80%.*
