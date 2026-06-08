# Search Queries for Job Scraper

## Search Sites

Primary (global / remote-friendly):
- **linkedin.com/jobs** - largest global job board, strong for remote roles
- **wellfound.com** - AngelList; strong for startups and fintech
- **otta.com** - tech-focused, good signal-to-noise for engineering roles
- **remoteok.com** - curated remote engineering roles
- **weworkremotely.com** - remote-only job board

Secondary (Nigeria / Africa-based roles):
- **jobberman.com** - largest Nigerian job board
- **myjobmag.com** - Nigerian tech and professional roles

Company career pages:
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. For remote roles, omit location or use "remote".

### Priority 1: Backend Engineering (Core Direction)

Strongest match — NestJS/Node.js/TypeScript backend roles.

```
site:linkedin.com/jobs "backend engineer" NestJS remote
site:linkedin.com/jobs "backend engineer" "Node.js" remote
site:linkedin.com/jobs "backend developer" TypeScript remote
site:wellfound.com "backend engineer" NestJS
site:otta.com "backend engineer" Node.js
site:remoteok.com backend NestJS
site:remoteok.com backend TypeScript
```

### Priority 2: Payments / Fintech Backend

High-value niche matching Haystack and Cliqpay project depth.

```
site:linkedin.com/jobs "backend engineer" payments remote
site:linkedin.com/jobs "backend engineer" fintech remote
site:linkedin.com/jobs "payments engineer" Node.js
site:wellfound.com "backend engineer" fintech payments
site:remoteok.com fintech backend engineer
```

### Priority 3: Platform Engineering / Developer Tooling

Adjacent to PNest CLI and developer-experience work.

```
site:linkedin.com/jobs "platform engineer" backend remote
site:linkedin.com/jobs "developer tools" backend engineer
site:linkedin.com/jobs "infrastructure engineer" Node.js remote
site:wellfound.com "platform engineer" backend
```

### Priority 4: Broader Software Engineering (Wider Net)

General engineering roles where backend TypeScript/Node.js is the core stack.

```
site:linkedin.com/jobs "software engineer" TypeScript Node.js remote
site:linkedin.com/jobs "software engineer" NestJS
site:jobberman.com "backend developer" Nigeria
site:myjobmag.com "software engineer" backend Nigeria
site:linkedin.com/jobs "senior software engineer" backend Nigeria
```

## Location Filter

Adebayo is based in Ibadan, Nigeria. Acceptable work arrangements:
- **Ideal:** Fully remote (worldwide)
- **Acceptable:** Remote with async collaboration across timezones
- **Borderline:** Remote with required overlap in WAT (UTC+1) business hours
- **Too far:** Mandatory on-site relocation outside Nigeria

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Suggested Role Types to Consider

Based on Adebayo's profile, also worth exploring:
- **API Platform Engineer** — companies building developer-facing APIs (Stripe, Paystack, Flutterwave, etc.)
- **Staff/Lead Backend Engineer** at Series A–C African startups — where sole ownership of backend systems is expected
- **Founding Engineer / Backend** at early-stage startups — matches the end-to-end ownership and builder profile

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and generate 2-3 custom queries for that focus. For example:
- "/scrape payments" → Priority 2 queries + custom fintech-specific searches
- "/scrape remote" → All Priority 1-2 queries filtered to remote-only
