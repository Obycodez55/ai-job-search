# Job Application Assistant for Adebayo Obikoya

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Adebayo Obikoya, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Adebayo Obikoya
- **Location:** Ibadan, Oyo State, Nigeria
- **Languages:** English (native)
- **Status:** Backend Developer at Postpaddy (employed); BSc student, University of Ibadan (2023–2028)
- **LinkedIn headline:** "Back End Developer @ PostPaddy | System Architecture, Collaborative Leadership"

### Education
- **BSc in Computer Science** (2023–2028) - University of Ibadan, Ibadan, Nigeria
  - First Class – 3.72/4.0
  - Research: developed gesture recognition system with associate professor (Google AI model, Raspberry Pi, Python)

### Professional Experience
- **Backend Developer** (02/2025–present) - **Postpaddy** (Ibadan, Nigeria)
  - Led full backend rewrite of PostPaddy's Laravel monolith to NestJS modular monolith, maintaining 100% API compatibility across 6 social platforms as sole backend engineer
  - Built campaign automation backend (email/SMS campaigns, multi-step workflows, CRM) and Listings platform (storefronts, ad promotions, lead capture, conversion tracking)
  - Designed multi-tenant architecture, WorkOS auth, BullMQ queue processing

- **Backend Developer** (07/2024–03/2025) - **Ckrowd Africa** (Ibadan, Nigeria)
  - Migrated backend from BaaS to NestJS/PostgreSQL, eliminating vendor dependency and reducing API latency

- **Backend Engineer** (02/2024–07/2024) - **Tros** (Nigeria)
  - Led IoT backend for 100+ devices; 200+ QR-based transactions with zero security incidents; 40% infrastructure cost reduction

### Technical Skills
- **Primary:** TypeScript, JavaScript, Node.js, NestJS, REST APIs, PostgreSQL
- **Secondary:** Python, MySQL, Redis, Docker, GitHub Actions, WebSockets, Jest
- **Domain:** Payment systems, multi-tenant SaaS architecture, IoT backend, developer tooling
- **Software:** BullMQ, WorkOS, Git, GitHub Actions, Docker, Jest

### Certifications
- The Compete 2024 Web Development Bootcamp – Certificate of Completion
- JavaScript (Intermediate) Certificate
- Master The Coding Interview: Data Structures + Algorithms – Certificate of Completion
- JavaScript (Basic) Certificate
- Node (Basic) Certificate

### Publications
- Obikoya, A. "Why Validation Matters: Ensuring Data Integrity and Security in Backend Development."
- Obikoya, A. "10 Tips for Effectively Learning Any Programming Technology."

### Awards
- None on record yet.

### Behavioral Profile
- **Builder orientation** - Spots inefficiencies and turns them into tools; energized by developer experience and hard technical challenges
- **Teacher/mentor** - Shares LeetCode thought process publicly; tutors and mentors other developers
- **Strengths:** End-to-end ownership, system design, independent project delivery
- **Growth areas:** Building seniority; balancing concurrent study with professional work
- **Thrives in:** Ownership-oriented teams; collaborative environments; roles requiring technical depth and initiative

### What Excites You
- Building systems that require technical correctness at scale: payment systems, state machines, reconciliation
- Developer tooling and developer experience: reducing friction for other engineers

### Target Sectors
- Fintech / Payments: [example companies TBD — run /setup --section search to update]
- SaaS / Product engineering: [example companies TBD]
- Developer tools / Platform engineering: [example companies TBD]

### Deal-breakers
- [To be confirmed — run /setup --section search to update]

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`
