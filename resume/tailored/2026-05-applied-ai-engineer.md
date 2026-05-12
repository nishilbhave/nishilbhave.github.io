# NISHIL PRAVIN BHAVE

**Applied AI Engineer · Designed & shipped 29 production agents (Sivon HQ) · 11y backend foundation**

Mumbai, India · nishilbhave@gmail.com · +91 9821251354
[linkedin.com/in/nishil-bhave](https://linkedin.com/in/nishil-bhave) · [github.com/nishilbhave](https://github.com/nishilbhave) · [nishilbhave.github.io](https://nishilbhave.github.io)

---

## SUMMARY

Engineer building production multi-agent systems. Designed and shipped **29 agents across 7 engines** for Sivon HQ — two-phase agent architecture, explicit director-briefing handoff protocol with live SSE streaming, multi-workspace isolation, and a pluggable multi-destination publisher running on GCP. Backed by 11 years of production engineering, including 6 years scaling a subscription platform to 5,000+ users.

---

## EXPERIENCE

### Founder & Solo Developer — Sivon HQ
*Remote · Jan 2026 – Present · Live in production, building toward first paying customers*

- Designing and shipping production AI systems solo — Sivon HQ's **29-agent topology** covers research, strategy, copy, design, distribution, analytics, and ops; live at sivonhq.com.
- Designed a **two-phase agent architecture**: a Foundation pipeline (Research → Strategy) builds persistent brand context once, then on-demand agents reuse it across every channel — eliminating the "re-prompt ChatGPT every time" problem that kills generic AI tools.
- Engineered an explicit handoff protocol via lightweight director briefings between agents; **live SSE streaming** surfaces tool calls, briefings, and outputs to the UI in real time.
- Built **multi-workspace isolation** so agencies can run multiple client brands without cross-contamination — all data strictly scoped to `(user_id, workspace_id)` and enforced at every router and Firestore query.
- Shipped background intelligence (**Pulse**) — competitor tracking, AI citation monitoring, market moments — plus automated Weekly Briefs synthesizing workspace deltas.
- Built a pluggable multi-destination publisher (Ghost, WordPress, Framer, Webflow, Resend, custom webhooks) driven by a Cloud Scheduler calendar that dispatches scheduled content end-to-end.
- Stack: **Next.js 16**, **React 19**, **TypeScript**, **Python**, **FastAPI**, **Google Gemini**, **Firestore**, **Firebase Auth**, **GCS**, **Cloud Run**, **Cloud Build**, **Cloud Scheduler**, **Lemon Squeezy**, **Resend**, **Playwright**.

### Senior Backend Developer — Fooddarzee
*Remote · Jul 2019 – Jul 2025 · Meal-subscription platform · Led team of 4 (2 BE + 2 FE)*

- Architected and owned the backend of a meal-subscription platform that scaled to **5,000 active subscribers** processing **4,000+ meal orders daily**, with no rewrite.
- Designed the **subscription engine** with date-level customization (veg days, skips, address changes) and preference-driven order calculations for 4,000+ daily deliveries.
- Architected a **multi-role ERP system** (Super Admin, Admin, Nutritionist, Chef, Customer) — each role with bespoke workflows over a shared data layer.
- **Led a team of 4 engineers** (2 backend, 2 frontend); ran code reviews, enforced standards, mentored juniors, coordinated with Product, Ops, and Mobile.

### Co-Founder & Technical Lead — Frocery Innovative Retail Pvt. Ltd.
*Mumbai · Jan 2018 – May 2019*

- Co-founded and tech-led an end-to-end grocery e-commerce platform — backend, mobile apps, payments, and delivery operations.
- Built RESTful APIs and CMS using PHP (CodeIgniter); developed cross-platform mobile apps in Ionic + Angular.

### Assistant System Analyst — Gray Matrix Solutions
*Mumbai · Feb 2016 – Oct 2017*

- Built backend APIs and hybrid mobile applications (Ionic + AngularJS) supporting multiple concurrent client projects.

### Technical Trainer & Developer — Suven Consultants & Technology
*Mumbai · Dec 2014 – Oct 2015*

- Developed PHP web applications; **trained 15–20 interns** in PHP, MySQL, HTML/CSS, and MVC architecture.

---

## SELECTED PROJECTS

**[Sivon HQ](https://sivonhq.com)** — AI marketing team built around a 29-agent topology across 7 engines. Two-phase agent architecture (Foundation → on-demand reuse) · director-briefing handoff protocol with live SSE streaming · multi-workspace isolation scoped at `(user_id, workspace_id)` · Pulse background intelligence + Weekly Briefs · pluggable multi-destination publisher on Cloud Scheduler. *Next.js 16 · React 19 · TypeScript · Python · FastAPI · Google Gemini · Firestore · Cloud Run.*

**[codeprobe](https://github.com/nishilbhave/codeprobe)** — Open-source code analysis tool covering security, performance, error handling, SOLID, and design pattern audits. *Python.*

**[ats-resume-tailor](https://github.com/nishilbhave/ats-resume-tailor)** — JD-targeted resume generation powered by Claude. *TypeScript.*

---

## SKILLS

**AI / LLM / Agents:** **Google Gemini** (multi-agent orchestration, structured outputs, tool use), **Claude** (tool use, prompt caching, agent design), **multi-agent system design** (two-phase architecture, explicit director-briefing handoff protocols, live SSE streaming), **multi-tenant agent platforms** (strict workspace isolation, per-tenant data scoping, background intelligence pipelines), prompt engineering, RAG patterns, AI-assisted development workflows (Claude Code, Cursor)
**Frameworks & Runtime:** **Next.js** (App Router, SSR, API routes, RSC), **FastAPI**, React, Laravel, Vue.js, CodeIgniter
**Infrastructure & Cloud:** **Google Cloud** (Cloud Run, Cloud Build, Cloud Scheduler, Firestore, GCS, Firebase Auth — production at Sivon HQ in us-central1), **AWS** (Lambda, EC2, S3, CloudFront — serverless migration experience), Vercel, Linux server admin
**Languages:** **TypeScript / JavaScript** (ES6+, Node.js, 8+ yrs), **Python** (3+ yrs, AI/agent workloads), **PHP** (OOP, MVC, 10+ yrs), **SQL** (MySQL, PostgreSQL — schema design, indexing, query optimization)
**APIs & Integrations:** REST · OAuth2 / OIDC · Razorpay · Juspay · Stripe · Firebase Cloud Messaging · webhook design
**DevOps & Tooling:** Git/GitHub, GitHub Actions (CI/CD), Playwright (end-to-end), Composer, npm, Vite
**Architecture & Practice:** Multi-tenant SaaS architecture, subscription/billing systems, event-driven / async processing, technical documentation, code review, mentoring, remote/async collaboration

---

## EDUCATION

**Bachelor of Engineering (Computers)** — Mumbai University · 2015
