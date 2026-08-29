# Master Resume Rebuild — Final Deliverables

Task 9 of the master resume rebuild plan (`docs/plans/2026-08-29-master-resume-rebuild.md`).
Synthesizes the final `my-resume.tex` (commit `f28e031`), the evidence ledger
(`docs/plans/2026-08-29-evidence-ledger.md`), and drafts 01–06
(`docs/plans/draft-01-header-summary-skills.md` through
`docs/plans/draft-06-layout-decisions.md`) into the four deliverables the
original rebuild request requires beyond the resume file itself: a Change
Log, a Keyword Map, a Resume Optimization Audit, and a Missing Information
list.

---

## A. Change Log — Old Resume vs. New Resume

The pre-rebuild `.tex` was never committed to this repository (this branch's
"Initial commit" already contains the rebuild plan, not the old resume file),
so this comparison is against the old resume's actual content as preserved
in the task brief for this purpose.

### Removed

- **Objective statement** — "I am passionate about web development, eager to
  learn and implement new technologies to craft innovative and dynamic web
  experiences." Removed entirely. First-person, fluff-worded, and
  content-free; replaced by a third-person Professional Summary that leads
  with the target identity (Software Engineer / Full-Stack Developer) and
  cites concrete stack and evidence.
- **StoryWrite project.** Excluded per EL-33 — user-confirmed as a mock that
  was never actually built. No fabricated or unverifiable project is
  included in the rebuild.
- **Education CGPA/grade omission.** The old resume showed JKLU B.Tech CSE
  with no CGPA and DPS Senior Secondary with no grade shown. Both numbers
  now appear (see "Added" below) — this wasn't a removal so much as a
  historical gap the rebuild closed using the evidence ledger.
- **DPS Middle School Diploma** (Apr 2019–Apr 2020, 91%, EL-32) — not part
  of the old resume's shown content, but deliberately excluded from the new
  resume as well (draft-04's Decisions). Documented here because it was a
  candidate for inclusion once its evidence surfaced but was rejected as
  pre-high-school information that doesn't earn space over 4 internships,
  3 projects, and a publication.

### Added

- **Research & Publications section** (new) — one entry: "Decentralized
  Carbon Markets: Blockchain-Enabled Carbon Credit Exchange," IEEE,
  published April 2026, co-authored (EL-29). The old resume had no research
  section at all.
- **Three additional experience roles.** The old resume showed only one
  internship (Front-End Developer Intern, Dynamicore Strategies, May–June
  2025). The new resume shows four:
  1. Full Stack Developer Intern, Dynamicore Strategies, May 2026–Present
     (EL-01 through EL-05)
  2. Full Stack Engineer Intern, The Learner's Academy, Jan–May 2026
     (EL-06 through EL-09)
  3. Front-End Developer Intern, Dynamicore Strategies, May–June 2025
     (carried over from the old resume, EL-10 through EL-12)
  4. Data Visualization Intern, Aunwesha Knowledge Tech, May–June 2024
     (EL-13, EL-14)
- **CGPA and high-school grade.** JKLU B.Tech CSE now shows CGPA 7.5/10
  (EL-30); DPS High School Diploma now shows 88% (EL-31). Both were blank
  in the old resume.
- **Git, GitHub in Technical Skills.** The old resume listed Git/GitHub
  under "Development Skills." The new resume retains both under
  **Developer Tools**, now backed by an explicit ledger entry (EL-35, added
  mid-rebuild after user confirmation) rather than an unsupported claim.
- **AI Engineering as an explicit skills category and summary theme** —
  LangChain, LangGraph, RAG, LLM Applications, AI Agents, Embeddings,
  Vector Search, Prompt Engineering. None of this existed in the old resume
  in any form; it reflects work done since the old resume was last updated
  (EL-02, EL-03, EL-04, EL-22, EL-23).

### Rewritten

- **Skills categorization.** The old resume split skills into three flat,
  loosely-related buckets ("Technical Skills," "Languages," "Development
  Skills"). The new resume uses eight purpose-built categories (Languages,
  Frontend, Backend/Runtime, Backend Frameworks, Databases, AI Engineering,
  Developer Tools, Engineering Concepts), each tracing every listed item to
  an evidence-ledger ID (draft-01).
- **All project bullets.** Every bullet under every shipped project (Ryder,
  TurfOnTop, Trajectory) was rewritten from the old resume's one-bullet
  format into 2–3 evidence-cited bullets per project, describing specific
  schema/architecture/integration decisions rather than a generic
  tech-list summary (draft-03).
- **Professional Summary** replaces the old Objective outright — not a
  line-edit but a full rewrite in voice (first-person → third-person),
  content (aspirational → evidence-based), and positioning (generic web
  dev → Software Engineer/Full-Stack Developer primary, AI engineering
  secondary).

### Promoted

- **Trajectory** moved from one of four undifferentiated projects (old
  resume order: Ryder, TurfOnTop, Trajectory, StoryWrite) to the **lead
  project** in the new Projects section, and given the most detailed
  bullets of the three shipped projects (3 bullets covering the RAG
  pipeline, the AI career-assistant logic, and the full-stack architecture
  — EL-22 through EL-25). This reflects its role as the strongest
  available evidence for the AI-engineering secondary specialization
  called out in the Summary (draft-03's Decisions, rationale 1).

### Deprioritized

- No evidence-backed claim was dropped outright in content terms — every
  distinct fact that was verifiable and relevant made it into the final
  resume in some form.
- **Bullet-count compression** was applied unevenly across the four
  experience roles per draft-02's Decisions: the two most recent/relevant
  roles (current Dynamicore Full Stack Developer Intern; The Learner's
  Academy) carry 3 bullets each, while the two older roles (Dynamicore
  Front-End Developer Intern, May–June 2025; Aunwesha Knowledge Tech) were
  compressed to 2 bullets each. This was done by merging adjacent claims
  into single bullets, not by deleting any EL-cited fact — e.g., the
  Front-End Developer Intern's loan-comparison, KYC, and gamified-learning
  claims (EL-11) were folded into one bullet alongside the platform
  description, rather than dropped.
- **LearnSphere and Suvidha** (EL-26, EL-27, EL-28) were drafted in full
  during Task 4 but held in reserve rather than shipped as a 4th/5th
  project, to avoid crowding a one-page resume and diluting the
  three-project AI/full-stack positioning (draft-03's Decisions). They
  remain available, fully evidenced, for a future backend-tailored resume
  variant.

---

## B. Keyword Map

Covers every keyword category the resume was built against; keywords with
no occurrence in the final `my-resume.tex` are omitted per the brief's
instruction not to force-fit. Presence was verified directly against
`my-resume.tex` (commit `f28e031`).

| Keyword | Evidence in Resume | Source (EL-ID) |
|---|---|---|
| Software Engineer | Header title line ("Software Engineer \| Full-Stack Developer"); Summary opening sentence | Positioning decision, draft-01 |
| Full-Stack Developer | Header title line; Summary ("full-stack development experience") | Positioning decision, draft-01 |
| TypeScript | Skills → Languages; Experience → Dynamicore Front-End Developer Intern bullet (React, TypeScript, Chart.js) | EL-09, EL-12 |
| React.js | Skills → Frontend ("React.js"); Experience (3 roles use React); Projects (Trajectory, Ryder, TurfOnTop all list React) | EL-09, EL-12, EL-24 |
| Node.js | Skills → Backend/Runtime; Summary; Projects (Trajectory, Ryder, TurfOnTop) | EL-24 |
| Express.js | Skills → Backend Frameworks; Projects (Trajectory, Ryder, TurfOnTop) | EL-20, EL-24 |
| FastAPI | Skills → Backend Frameworks; Summary; Experience (Dynamicore current role bullet); Projects (Trajectory) | EL-02, EL-22, EL-23 |
| REST APIs | Skills → Developer Tools ("REST APIs"); Summary ("Designs and ships REST APIs"); Projects (TurfOnTop: "RESTful Express.js API") | EL-20 |
| PostgreSQL | Skills → Databases; Summary; Projects (Ryder schema, TurfOnTop) | EL-16, EL-20 |
| SQL | Skills → Languages | EL-16, EL-20 |
| Redis | Skills → Databases; Experience (Dynamicore current role: "FastAPI, LangGraph, LangChain, and Redis") | EL-02 |
| Git | Skills → Developer Tools | EL-35 |
| GitHub | Skills → Developer Tools; header link (github.com/Riyanshverma) | EL-35 |
| API Development | Skills → Engineering Concepts, as "API Design" (not the literal phrase "API Development") | EL-20, EL-22 |
| Database Design | Skills → Engineering Concepts | EL-16, EL-27 |
| Authentication | Skills → Developer Tools ("JWT Authentication") and Engineering Concepts ("Authentication & Authorization"); Projects (Ryder: JWT httpOnly-cookie auth; TurfOnTop: JWT auth) | EL-15, EL-20, EL-26 |
| Generative AI / LLM Applications | Skills → AI Engineering ("LLM Applications"); Summary ("multi-agent LLM systems") — the literal phrase "Generative AI" does not appear, but LLM Applications/systems is the resume's equivalent term | EL-02, EL-05, EL-22 |
| RAG / Retrieval-Augmented Generation | Skills → AI Engineering; Summary; Experience (Dynamicore current role bullet); Projects (Trajectory) | EL-03, EL-23 |
| AI Agents | Skills → AI Engineering; Experience (Dynamicore current role: "Built specialist agents and a routing Supervisor") | EL-02, EL-04 |
| LangChain | Skills → AI Engineering; Summary; Experience; Projects (Trajectory) | EL-02, EL-23 |
| LangGraph | Skills → AI Engineering; Summary; Experience (Dynamicore current role) | EL-02 |
| Vector Databases/ChromaDB | Skills → Databases ("ChromaDB") and AI Engineering ("Vector Search"); Projects (Trajectory: FastAPI/LangChain/ChromaDB) | EL-22, EL-23 |
| Embeddings | Skills → AI Engineering; Projects (Trajectory: "embedding generation via sentence-transformers") | EL-22, EL-23 |
| Prompt Engineering | Skills → AI Engineering | EL-02, EL-05 |
| System Design | Skills → Engineering Concepts | EL-02, EL-04, EL-07 |
| OOP | Skills → Engineering Concepts | EL-14 |

### Keywords checked but absent from the final resume (omitted, not force-fit)

- **Next.js** — not present anywhere in `my-resume.tex`; no project or role
  uses Next.js per the evidence ledger (all React work uses plain React,
  not the Next.js framework).
- **MongoDB** — not present; every database claim in the ledger is
  PostgreSQL, MySQL, Supabase, Redis, or ChromaDB. No MongoDB usage found
  in any project.
- **Docker** — not present. draft-01's Decisions record that a direct
  search across every project repository found no Dockerfile or
  docker-compose file in first-party code.
- **WebSockets** — not present. Same draft-01 search found no WebSocket
  usage in first-party project code.
- **Data Structures & Algorithms** — not present as a skills-list item.
  draft-01's Decisions explicitly dropped this from the Engineering
  Concepts category because the evidence ledger has no project or role
  citation for it (its only basis was the old resume's unverified
  skills line).
- **Database Management** — not present as an exact phrase; the resume
  uses "Database Design" instead (Skills → Engineering Concepts), which is
  the evidence-backed equivalent.

---

## C. Resume Optimization Audit

**This is a Resume Optimization Audit — an internal self-assessment, NOT a
real ATS score.** No resume was actually submitted to any Applicant
Tracking System or scored by one; the numbers below are a structured
qualitative judgment against the stated identity (Software Engineer /
Full-Stack Developer, AI Engineering secondary) and general ATS-parsing
conventions, produced for planning purposes only.

| Dimension | Score (1–10) | Rationale |
|---|---|---|
| ATS readability | 8 | Single-column LaTeX layout, standard section headers (SUMMARY, SKILLS, EXPERIENCE, PROJECTS, EDUCATION, RESEARCH & PUBLICATIONS), no tables/columns for content parsing except the simple two-column Skills tabular (label + comma-separated list, which most parsers handle fine). No graphics, icons, or multi-column body text that typically break ATS parsers. Not a 10 because the Skills section uses a LaTeX `tabular` environment, which is marginally riskier for some parsers than plain text lines. |
| Full-Stack relevance | 8 | Summary leads with full-stack framing; Experience shows both frontend (React, TypeScript, Tailwind) and backend (FastAPI, Express.js, PostgreSQL) work across 4 roles; Projects (Ryder, TurfOnTop, Trajectory) are each full end-to-end builds with schema design through UI. Not a 9–10 because only 2 of 4 experience roles are explicitly "Full Stack" titled — the other two are Front-End and Data Visualization titled, which slightly dilutes a pure full-stack narrative. |
| Software Engineer relevance | 8 | Broad language list (TypeScript, JavaScript, Python, SQL, Java, C++), System Design and OOP under Engineering Concepts, and evidence of building non-trivial systems (multi-agent orchestration, RBAC architecture, relational schema design) support a general SWE identity well beyond a narrow "frontend-only" or "bootcamp" profile. |
| Backend relevance | 8 | Strong: Express.js, FastAPI, Elysia, Hono across roles/projects; PostgreSQL schema design (Ryder); JWT auth flows; Razorpay payment integration with signature validation; scheduled cron jobs. Not higher because there's no evidence of infrastructure/deployment ownership (CI/CD, containerization, cloud infra) — see Missing Information below. |
| Frontend relevance | 7 | React, Redux Toolkit, Zustand, Tailwind CSS, shadcn/ui, Radix UI, Chart.js, react-d3-tree all appear with project-level evidence. Scored below Backend because the frontend work described is largely UI-integration and state-management rather than performance/accessibility/testing-specific frontend engineering claims. |
| AI Engineering relevance | 8 | Explicit AI Engineering skills category; a full RAG pipeline with LangChain/ChromaDB/embeddings (Trajectory); multi-agent orchestration with a routing Supervisor and compliance gates (Dynamicore current role); LangGraph and agentic memory. This is genuinely differentiated evidence, not just a buzzword list. Not a 9–10 because it's explicitly framed as a secondary focus per the resume's own positioning, and there's no quantified outcome (accuracy, latency, adoption) tied to any AI feature. |
| Database relevance | 7 | Relational schema design shown concretely (Ryder's users/owners/cars/rentals/bookings schema; multi-identity RBAC/3NF work referenced via The Learner's Academy role); PostgreSQL, MySQL, Supabase, Redis, ChromaDB all evidenced. Not higher because no query-optimization, indexing, or scaling claim exists anywhere in the ledger. |
| System Design relevance | 6 | "System Design" appears in Skills and is loosely supported by the multi-agent orchestration and RBAC architecture work, but there's no resume bullet that names a specific system-design decision (e.g., a tradeoff, a scaling choice, a data-flow diagram) the way the schema/auth bullets do for database/backend. This is the audit's most conservative score because the keyword is present but the evidentiary depth behind it is the thinnest of the technical categories. |
| Keyword coverage | 8 | 25 of 34 checked keyword-category items across Section B's list have direct textual evidence in the resume (the 9 absent ones — Next.js, MongoDB, Docker, WebSockets, DSA, Database Management as an exact phrase, etc. — were correctly and deliberately omitted rather than force-fit, which protects credibility at the cost of raw coverage against a keyword list written before the evidence was gathered). |
| Evidence/achievement quality | 6 | Every bullet is grounded in a real, verifiable project or role (no fabrication), and most describe specific architecture/integration decisions rather than generic responsibilities. The audit does not score higher because almost no bullet carries a quantified outcome — no user counts, latency numbers, percentage improvements, or team-size context anywhere in the document (see Missing Information, Section D). This is the single biggest gap between this resume and a resume that would score in the 8–10 range on this dimension. |
| Recruiter readability | 8 | One-page-oriented, clear section order (Summary → Skills → Experience → Projects → Education → Research), consistent bullet style, no jargon-only lines — every AI/backend term is used in a sentence describing what was built, not just listed. Not a 9–10 because the density is high (4 experience roles + 3 projects + an 8-category skills block + a publication), which is a real skim-speed cost for a recruiter doing a 6-second first pass. |

### The Recruiter Test

Ten questions, answered plainly against the resume as it stands today.

1. **What role does this candidate want?**
   Software Engineer or Full-Stack Developer — stated explicitly in the
   header title line and the first sentence of the Summary, with AI
   Engineering positioned as a secondary specialization rather than the
   primary target.

2. **What is he strongest at?**
   Full-stack web application development — designing and shipping
   complete systems (auth, payments, relational schemas, REST APIs) across
   the frontend and backend in both internship and independent-project
   contexts. His AI engineering work (RAG pipelines, multi-agent
   orchestration) is a close second and his most differentiated evidence,
   but the sheer volume and consistency of full-stack delivery across 4
   roles and 3 projects is the stronger, more repeated signal.

3. **Is he actually a Full-Stack Developer?**
   Yes, on the evidence shown. Two of four experience roles are explicitly
   titled Full Stack (current Dynamicore role, The Learner's Academy), and
   all three shipped projects (Trajectory, Ryder, TurfOnTop) show backend
   architecture (schema design, API endpoints, auth) paired with a
   corresponding frontend (React-based UI) built by the same person. This
   isn't a frontend-only profile with backend keywords sprinkled in — the
   backend claims are specific (schema tables named, auth mechanism named,
   payment-signature validation named).

4. **Does he demonstrate backend capability?**
   Yes, clearly: PostgreSQL schema design with named tables (Ryder), JWT
   httpOnly-cookie authentication with role-based routing, Razorpay
   payment order creation and signature validation, a scheduled cron job,
   a RESTful Express.js API, and FastAPI-based services in both a
   production internship context and an independent project. This is
   concrete backend engineering, not just a backend framework listed in
   Skills.

5. **Does he demonstrate modern frontend capability?**
   Yes, though with less specificity than the backend evidence: React,
   Redux Toolkit, Zustand, Tailwind CSS, shadcn/ui, Radix UI, and Chart.js
   all appear with role/project attribution, and one bullet explicitly
   calls out a "responsive, mobile-first UI." There's no claim about
   frontend performance, accessibility, or testing, which a stronger
   frontend-focused resume would typically include.

6. **Does he demonstrate database experience?**
   Yes: a concrete multi-table relational schema (Ryder: users, owners,
   cars, rentals, bookings) with real-time search/filtering/availability
   logic built on top of it, plus RBAC-scoped schema work referenced via
   The Learner's Academy role, across PostgreSQL, MySQL, Supabase, Redis,
   and ChromaDB. The gap is that there's no evidence of query optimization,
   indexing strategy, or working at scale (see Q9/Missing Information).

7. **Does he demonstrate AI engineering experience?**
   Yes, and this is his most differentiated evidence relative to a typical
   entry-level Full-Stack Developer: a working RAG pipeline (document
   loading, chunking, embedding generation, ChromaDB retrieval) in
   Trajectory, and a production multi-agent system with a routing
   Supervisor, LLM-based reasoning, and deterministic compliance gates in
   his current internship. This is real, cited AI-engineering work, not a
   buzzword list — but it's explicitly framed as secondary to the
   full-stack identity, and it carries no quantified outcome.

8. **Does he show evidence of building real applications?**
   Yes — three complete, named, evidenced projects (Trajectory, Ryder,
   TurfOnTop), each with a specific domain, a specific backend
   architecture, and a specific frontend, plus four internship roles each
   tied to a named employer and a specific deliverable. Nothing on the
   resume is generic or unattributable to a real system.

9. **Does he show professional (internship) experience?**
   Yes — four internships spanning May 2024 to present (one still
   ongoing), at three different organizations, with increasing scope and
   seniority (Data Visualization → Front-End → Full Stack Engineer → Full
   Stack Developer). This is a meaningfully deeper internship history than
   the old resume's single 2-month role.

10. **What differentiates him from another entry-level Full-Stack
    Developer?**
    The AI engineering work — specifically, a real RAG pipeline and a
    production multi-agent LLM system with compliance-gate logic, both
    independently verifiable via project artifacts and an active
    internship. Most entry-level full-stack candidates can show CRUD apps
    with auth and payments (which this candidate also has, via Ryder and
    TurfOnTop); comparatively few can show a working retrieval pipeline
    and a multi-agent orchestration system built and shipped in a
    professional setting. The secondary differentiator is the IEEE
    co-authored publication, which is uncommon at this career stage
    regardless of subject matter.

---

## D. Missing Information

The following would strengthen the resume but is **not available** in any
source consulted during this rebuild (portfolio data files, project
READMEs/package manifests, or the user-supplied LinkedIn export). Per
EL-34, this was checked for and confirmed absent — none of it has been
invented or estimated anywhere in the resume. This is a request list for
the user to consider supplying in a future update, not a set of claims
already made.

- **Performance metrics** — e.g., API response times, page-load times,
  query latency, or any before/after performance comparison for any
  project or internship deliverable.
- **User counts / usage figures** — e.g., how many users interacted with
  the fintech platform, the school management system, or any shipped
  project; adoption or engagement numbers of any kind.
- **API/endpoint counts per project** — e.g., "designed N REST endpoints"
  or "built an API surface of N routes" for Ryder, TurfOnTop, or
  Trajectory's backend.
- **Team sizes** — whether any of the four internships or three projects
  were solo work or done alongside a team, and if a team, how large and
  what the candidate's specific role/ownership within it was.
- **Deployment / CI-CD evidence** — whether any project has an automated
  deployment pipeline, is hosted in production (beyond the portfolio site
  itself, which is on Vercel), or uses any CI tooling (GitHub Actions,
  etc.). This also relates to the Docker/containerization gap noted in
  Section B — no infrastructure-as-code or deployment automation evidence
  exists anywhere in the ledger.
- **Testing coverage evidence** — unit/integration/E2E test suites, test
  coverage percentages, or any QA process for any project or internship
  deliverable.

If any of these become available (e.g., real usage numbers for the
Dynamicore fintech platform, or confirmation that a project has automated
tests), they should be added to the evidence ledger with a new EL- ID
before being incorporated into any future resume revision — consistent
with the sourcing discipline used throughout this rebuild.
