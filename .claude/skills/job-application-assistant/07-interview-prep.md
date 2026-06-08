# Interview Preparation Guide

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

### Postpaddy Monolith Rewrite
**Source:** Resume — Backend Developer, Postpaddy (02/2025–present)
**Why it matters:** Answers questions about technical decision-making, migration strategy, handling scope and risk alone, and owning a system end-to-end.

**S:** PostPaddy's social media management product was running on a Laravel 9 monolith with 200+ controllers and 74 jobs. The codebase had grown unmaintainable and couldn't support the product's next phase.
**T:** Rewrite the entire backend to NestJS as the sole backend engineer, maintaining full API compatibility so the frontend wouldn't break during migration.
**A:** Designed the full system architecture from scratch — modular monolith structure, unified BullMQ queue processing replacing multiple Laravel queue commands, WorkOS central auth, multi-tenant org structure, and platform service abstractions for 6 social networks. Built three production systems in parallel: the social platform rewrite, campaign automation, and Listings.
**R:** Three live NestJS backends replacing the Laravel system, with 100% API compatibility maintained throughout and a significantly more maintainable, observable codebase.
**Use for:** "Tell me about a time you owned a large technical migration", "Describe a system you designed from scratch", "How do you handle high-stakes solo ownership"

### Tros IoT System — Team Lead
**Source:** Resume — Backend Engineer, Tros (02/2024–07/2024)
**Why it matters:** Answers questions about team leadership, technical delivery under constraints, security, and quantified impact.

**S:** Tros needed a backend system to manage authentication and real-time data for an IoT deployment going into a live pilot.
**T:** Lead backend development — design secure device auth, QR-based payment flows, and keep infrastructure lean.
**A:** Built authentication system for 100+ devices, designed QR-based identification and payment flows with security as a primary constraint, and made architectural decisions that cut infrastructure costs by 40%.
**R:** Successfully processed 200+ QR transactions across a 4-week pilot with zero security incidents.
**Use for:** "Tell me about a time you led a team", "Describe a project where you had to balance security and speed", "Give an example of reducing costs through architecture"

### Ckrowd Africa BaaS Migration
**Source:** Resume — Backend Developer, Ckrowd Africa (07/2024–03/2025)
**Why it matters:** Answers questions about architectural trade-offs, vendor risk, migration planning, and technical judgement.

**S:** Ckrowd's backend was built on a BaaS platform that limited control over performance, data models, and costs.
**T:** Migrate the entire backend to NestJS and PostgreSQL without disrupting the product.
**A:** Rebuilt the backend from scratch on NestJS/PostgreSQL, set up AWS infrastructure (EC2, S3), restructured API contracts, and worked with the frontend team to align on the new API layer.
**R:** Eliminated vendor dependency and associated costs, reduced API latency, and gave the team full control over performance tuning and scalability.
**Use for:** "Tell me about a time you made a build-vs-buy decision", "Describe a migration you led", "How do you manage technical risk"

### Cliqpay Double-Entry Ledger
**Source:** Independent project — Cliqpay (05/2026–present)
**Why it matters:** Answers questions about complex data modelling, financial correctness, concurrency, and independent technical depth.

**S:** Building a P2P payment platform where multiple users could trigger concurrent wallet operations — creating real risk of race conditions and incorrect balances.
**T:** Design a financial data model that guaranteed correctness under concurrency with no stuck states or double-executions.
**A:** Implemented a double-entry ledger where every money movement records across two accounts, used pessimistic locking on all multi-account balance updates wrapped in database transactions, built idempotent webhook processing deduplicating by reference key, and added a reversal engine that atomically restores balances on failed payouts.
**R:** A payment system where the total user wallet balances always reconcile against the platform float, with no race conditions, no double charges, and no stuck pending states by design.
**Use for:** "How do you ensure data consistency at scale", "Describe a hard technical problem you solved independently", "Tell me about your experience with financial systems"

## Common Tough Questions

### "Why did you leave [previous company]?"
> [Prepare your answer — be honest, forward-looking, no negativity about former employer]

### "You don't have [specific skill/experience]."
> [Prepare your answer — acknowledge the gap, bridge to adjacent experience, show willingness to learn]

### "Where do you see yourself in 5 years?"
> [Prepare your answer — show ambition aligned with the role's growth path]

### "What's your biggest weakness?"
> [Prepare your answer — genuine weakness with concrete mitigation strategy]

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission — this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
