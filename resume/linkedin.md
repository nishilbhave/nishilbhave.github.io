# LinkedIn Profile Update — Copy-Paste Reference

> Derives from `master.md`. Calibrated honesty applied throughout.
> Profile URL: https://linkedin.com/in/nishil-bhave
> Last updated: 2026-05-11

**Update order (35–45 min total):**
1. Banner image (5 min)
2. Headline (1 min — copy-paste)
3. About section (3 min — copy-paste)
4. Experience bullets, per role (10 min)
5. Featured section (5 min)
6. Services section (5 min)
7. Skills + Top 3 pinned (3 min)
8. Open to Work toggle — recruiters only (1 min)
9. Custom URL check (1 min)

---

## 1. Banner Image (1584 × 396 px)

Don't use a stock template. Design a banner in your portfolio aesthetic.

**Spec:**
- Background: `#09090b` (zinc-950) — matches portfolio
- One line of large Space Grotesk bold text:
  > **Senior Software Engineer. Building AI in production.**
- Subline in smaller monospace:
  > *Sivon HQ · 29 agents · 7 engines*
- Tiny lime accent dot bottom-right with mono text:
  > `Booking Q3 2026`

Tools that work in <10 min: Figma, Canva (use a blank canvas, ignore templates), or hand-code an SVG and screenshot. **Avoid:** AI-generated cyberpunk imagery, stock photos, gradient mush.

---

## 2. Headline (220 char limit)

Pick ONE. I recommend **H1** as the default — it's the strongest ATS-matchable + recruiter-readable hybrid.

### H1 — Recommended (default hybrid, 137 chars)
```
Senior Software Engineer · AI / Agent Systems · Built Sivon HQ (29 agents in prod) · Scaled subscription platform to 5K subs · 11y · Mumbai
```

### H2 — Backend-leaning alternative (133 chars)
```
Senior Backend Engineer · Laravel / Next.js · Scaled ERP to 5K subs · Building AI / multi-agent systems · 11y · Open to roles & client work
```

### H3 — Founding-Engineer-target alternative (124 chars)
```
Founding Engineer · 11y shipping production systems · Backend + AI / multi-agent systems · Sivon HQ creator · Booking Q3 2026
```

---

## 3. About Section (2,600 char limit · this draft ~1,950)

> Recruiter-inbound priority. Leads with FT availability; client work is demoted to a single line near the bottom. Copy-paste verbatim — the line breaks matter, LinkedIn preserves them and they make this scannable on mobile.

```
I'm a senior software engineer who went AI-native. 11 years shipping production systems end-to-end.

Open to senior full-time roles — Senior / Staff IC, Founding Engineer, Applied AI Engineer, Member of Technical Staff. Remote (worldwide), Mumbai or Bangalore (in-person).

Recently shipped:

→ Sivon HQ — a multi-agent AI marketing platform with 29 specialized agents across 7 engines (research, strategy, copy, design, distribution, analytics, ops). Built solo. Live in production. Multi-workspace, eval harness, observability, PII redaction at the agent boundary. SOC 2 + GDPR-aligned architecture.

→ Fooddarzee (Jul 2019 – Jul 2025) — backend lead for a meal-subscription platform that scaled to 5,000 active subscribers and 4,000+ daily orders. Led a team of 4 engineers. Cut AWS hosting costs ~40% via a serverless migration. Designed the subscription engine handling date-level customization for thousands of daily deliveries.

Before that: co-founder & technical lead at Frocery (grocery e-commerce), engineer at Gray Matrix, PHP trainer at Suven (15–20 interns).

What I'm strongest at:
• Multi-agent AI systems that survive production — topology, evals, observability, cost attribution, PII redaction
• Greenfield SaaS, end-to-end — Next.js + Supabase or Laravel + MySQL; Stripe billing; CI; deploy
• Senior IC at early-stage teams — architecture, code review, mentoring, on-call decisions

If you're hiring for a role where shipping AI in production matters more than the title, let's talk.

Also available for select client work (SaaS MVP build · multi-agent system build · fractional retainer) — booking Q3 2026. Details at nishilbhave.github.io.

Reach me: nishilbhave@gmail.com — 24h reply.

Portfolio: nishilbhave.github.io
Sivon HQ: sivonhq.com
GitHub: github.com/nishilbhave
```

---

## 4. Experience — Per-Role Copy

LinkedIn caps each role description at 2,000 characters. Plain bullets render best. Use `•` not `-` (LinkedIn renders bullets cleaner).

### 4.1 Founder & Solo Developer
**Company:** *Self-employed*
**Dates:** January 2026 – Present
**Location:** Remote
**Description (paste verbatim):**

```
Building production AI products solo.

Sivon HQ — sivonhq.com
A multi-agent AI marketing platform with 29 specialized agents across 7 engines (research, strategy, copy, design, distribution, analytics, ops). Live in production.

• Designed agent topology with explicit handoff protocols, eval harness with regression suite, and per-agent cost attribution
• Built observability layer covering tracing, token cost attribution per workspace, and PII redaction at the agent boundary
• Engineered multi-workspace isolation so agencies can run multiple client brands without cross-contamination
• SOC 2 + GDPR-aligned architecture
• Stack: Next.js, TypeScript, Python, Claude, Supabase, Firestore, Cloud Run, Vercel

MakeToCreate — maketocreate.com
Engineering publication on system design, AI tools, and SaaS. For developers who ship.

Operating production infrastructure solo: incident response, billing reconciliation, customer support, deployment automation.

Also maintaining open-source tools: codeprobe (code analysis), claude-skills (Claude skill collection), growth-engine (marketing automation primitives), ats-resume-tailor (JD-targeted resume generation).
```

### 4.2 Senior Backend Developer · Fooddarzee
**Company:** *Fooddarzee*
**Dates:** July 2019 – July 2025
**Location:** Remote
**Description (paste verbatim):**

```
Backend owner and technical lead for a meal-subscription platform. Led a team of 4 engineers (2 backend, 2 frontend).

• Architected and owned the backend of a meal-subscription platform that scaled to 5,000 active subscribers processing 4,000+ meal orders daily, with no rewrite
• Designed the subscription engine with date-level customization (veg days, skips, address changes) and preference-driven order calculations
• Architected a multi-role ERP system (Super Admin, Admin, Nutritionist, Chef, Customer) — each role with bespoke workflows over a shared data layer
• Led migration of the public website to AWS serverless (Lambda + CloudFront + S3), cutting hosting costs ~40%
• Led a team of 4 engineers; ran code reviews, enforced standards, mentored juniors
• Integrated Razorpay and Juspay for one-time and recurring payments processing thousands of transactions monthly; Zoho for invoicing via OAuth2
• Built CI/CD pipelines using GitHub Actions
• Automated manual order-processing workflows, saving the operations team 10+ hours/week
• Stack: PHP, Laravel, MySQL, AWS (EC2, Lambda, CloudFront, S3), Redis, GitHub Actions
```

### 4.3 Co-Founder & Technical Lead · Frocery Innovative Retail Pvt. Ltd.
**Dates:** January 2018 – May 2019
**Location:** Mumbai, India
**Description:**

```
Co-founded and tech-led an end-to-end grocery e-commerce platform — backend, mobile apps, payments, and delivery operations.

• Built RESTful APIs and CMS using PHP (CodeIgniter); developed cross-platform mobile apps in Ionic + Angular
• Integrated Razorpay payments and Firebase push notifications
• Designed a delivery countdown timer that improved on-time delivery SLA adherence
• Made all technical decisions across backend, mobile, and operations infrastructure as founding technical lead
```

### 4.4 Assistant System Analyst · Gray Matrix Solutions
**Dates:** February 2016 – October 2017
**Location:** Mumbai, India
**Description:**

```
• Developed hybrid mobile applications using Ionic and AngularJS with backend API integration
• Built backend APIs supporting multiple concurrent client projects in a collaborative team environment
• Worked closely with QA and product teams to deliver features on schedule
```

### 4.5 Technical Trainer & Developer · Suven Consultants & Technology
**Dates:** December 2014 – October 2015
**Location:** Mumbai, India
**Description:**

```
• Developed PHP web applications and internal tools; delivered freelance projects under tight timelines
• Trained 15–20 interns in PHP, MySQL, HTML, CSS, and MVC architecture
```

---

## 5. Featured Section (pin 4 items in this exact order)

Featured appears above Experience and gets 3–4× the click-through. Order matters.

1. **Link → Portfolio** (`https://nishilbhave.github.io/`)
   - Title: *Hire me — three productized offers*
   - Description: *AI-native senior builder. 11 years shipping production systems.*

2. **Link → Sivon HQ** (`https://sivonhq.com`)
   - Title: *Sivon HQ — 29 AI agents across 7 engines*
   - Description: *Multi-agent AI marketing platform. Live in production.*

3. **Link → codeprobe** (`https://github.com/nishilbhave/codeprobe`)
   - Title: *codeprobe — open-source code analysis*
   - Description: *Security, performance, SOLID, and design pattern audits. Python.*

4. **Reserve slot for first pinned LinkedIn post** — write this in Week 1 of posting. Best candidate: *"What 29 production agents taught me about handoff protocols"* (carousel format).

---

## 6. Services Section

Click your profile → Open to → Providing services. Fill in:

**Services:**
- Custom Software Development
- Artificial Intelligence
- Software Architecture
- Technical Consulting

**Service description (one box, all three offers):**

```
Three productized offers for founders and engineering leaders:

1. SaaS MVP build (4–12 wks) — Idea to shipped product. Architecture, full-stack build, billing, infra, deploy. You own the codebase from day one. Stack: Next.js + Supabase or Laravel + MySQL.

2. Multi-agent AI system (3–8 wks) — Production agent pipelines. Topology design, eval harness, observability, cost attribution, PII redaction. Not a demo, a system that ships.

3. Fractional senior engineer (monthly retainer) — Embed in your team. Architecture, code review, mentoring, and on-call decisions for early-stage teams.

Currently booking Q3 2026. Email nishilbhave@gmail.com with a one-line pitch — 24h reply.

Proof: Built Sivon HQ (29 agents in production) · Scaled Fooddarzee to 5K active subs · 11 years building production systems. Portfolio: nishilbhave.github.io
```

**Pricing:** Leave blank (matches portfolio's no-public-pricing decision).
**Project duration:** Tick all of: Less than a month, 1–3 months, 3–6 months (covers all three offers).

---

## 7. Skills (top 3 pinned, rest auto-ordered)

Click Skills section → pin these three to the top in this order:

1. **Software Architecture**
2. **Artificial Intelligence**
3. **Backend Development**

Add (LinkedIn auto-orders the rest):

```
Multi-Agent Systems · Large Language Models (LLM) · Software Architecture · System Design · Backend Development · Full-Stack Development · TypeScript · PHP · Laravel · Next.js · Python · MySQL · PostgreSQL · AWS · Google Cloud Platform · Supabase · REST APIs · OAuth2 · CI/CD · GitHub Actions · Code Review · Team Leadership · Mentoring · Technical Documentation · Multi-Tenant SaaS · Subscription Billing · Remote Work
```

---

## 8. Open to Work — Recruiters Only (PRIVATE)

Click profile → "Open to" → "Finding a new job":

- **Job titles:** Senior Software Engineer · Staff Software Engineer · Founding Engineer · Applied AI Engineer · AI Engineer · Member of Technical Staff · Senior Backend Engineer · Tech Lead
- **Locations:** Remote (worldwide), Mumbai (in-person), Bangalore (in-person)
- **Job types:** Full-time, Contract
- **Start date:** Immediately or within 1 month
- **Who can see this:** **Recruiters only** ← critical. Do NOT enable the public green #OpenToWork ring — it conflicts with "Booking Q3 2026" client positioning and reads as desperate to founders.

---

## 9. Custom URL

Already set to `linkedin.com/in/nishil-bhave` — keep it. Don't add numbers or change.

---

## 10. Profile Photo + Background Check

While you're in there:

- **Profile photo:** The GitHub avatar (the one already on your portfolio) is fine if it's a clear headshot. If it's a logo or distorted, replace with a clean headshot — neutral background, eye-level, professional but not stiff.
- **Cover photo / banner:** See §1.
- **Contact info:** Make sure email + portfolio URL are both filled in under Contact Info (LinkedIn hides email from public view unless you're connected).

---

## 11. First Week of Activity (after profile update)

LinkedIn algorithm rewards activity within 24–72h of profile changes. Use this window:

**Day 1 (today after update):**
- Send 8–12 reconnect DMs to past Fooddarzee colleagues / clients with this template:
  > "Hey [Name] — going through a positioning refresh. Wanted to say hi. I've gone solo and I'm building Sivon HQ (multi-agent AI marketing platform). If you're around anything AI/SaaS-build adjacent, happy to chat anytime."

**Day 2:**
- Write and pin the agent-handoff carousel: *"What 29 production agents taught me about handoff protocols"* — that becomes Featured slot #4.

**Day 3–7:**
- 30 min/day commenting substantively on 10–15 founder / agency-owner / AI-builder posts. This builds reach faster than posting.

---

## 12. What NOT to do

- **Don't post "I'm freelance now, taking on clients!" as your first post.** Signals desperation, devalues your offers, suppresses algorithmic reach. Make the first post a *demonstration* (the carousel), let work-with-me sit in About + Services + Featured.
- **Don't enable the green public Open-to-Work ring.** Conflicts with client positioning.
- **Don't add 50 skills.** Recruiters skim the top 5. Keep it tight.
- **Don't put portfolio URL in your headline.** Use the dedicated website slot in Contact Info instead — frees up headline characters.
- **Don't fill in pricing in Services.** Match portfolio decision.
```
