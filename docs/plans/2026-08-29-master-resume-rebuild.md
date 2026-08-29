# Master Resume Rebuild Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to
> implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rebuild `my-resume.tex` from scratch into an ATS-friendly, evidence-driven
Master Resume positioning Riyansh Verma as a Software Engineer / Full-Stack Developer
with AI Engineering as a credible secondary specialization — replacing the old
objective-driven, frontend-only framing.

**Architecture:** Single-column LaTeX resume (existing `resume.cls`), built section by
section. Every claim is sourced from one of: portfolio `experience-info.ts` /
`projects-info.ts`, individual project READMEs/package manifests, or the user-supplied
LinkedIn export (education, CGPA, IEEE publication). No section is written until its
source evidence is logged in this plan's task.

**Tech Stack:** LaTeX (existing `resume.cls` document class), verified against source
files in `my-portfolio/src/Data/`, `ryder/`, `turf-on-top/`, `career-counselling-system/`,
`learn-sphere/`, `suvidha/`.

**Spec:** The user's "MASTER RESUME REBUILD PROMPT" (chat message, 2026-08-29) — this
plan operationalizes it. Key deviations from the prompt's assumptions, corrected by
verified evidence, are listed in Global Constraints below.

## Global Constraints

- StoryWrite project: EXCLUDED — user confirmed it was a mock, never built.
- Aunwesha role title: "Data Visualization Intern" (verified in `experience-info.ts`),
  NOT "Data Analyst Intern" as the original prompt assumed.
- IEEE publication IS real: "Decentralized Carbon Markets: Blockchain-Enabled Carbon
  Credit Exchange," IEEE, published Apr 9 2026, co-authored (2 other authors), DOI at
  https://ieeexplore.ieee.org/document/11471701 — include in RESEARCH & PUBLICATIONS.
- CGPA IS real: 7.5/10 at JK Lakshmipat University — include in Education.
- Full education history (LinkedIn-verified): JKLU B.Tech CSE 2022–2026 (7.5 CGPA);
  DPS High School Diploma (Math & CS) Apr 2021–Apr 2022, 88%; DPS Middle School Diploma
  Apr 2019–Apr 2020, 91%. Middle school is likely cut for space per prompt's own rule
  ("don't let high-school info crowd out professional content") — decide in Task 7.
  Do not invent it.
- No performance metrics, user counts, or team sizes exist in any source — use scope
  (feature counts, module counts, architecture components) instead, per prompt rule.
- Source of truth priority when conflicts exist: portfolio `experience-info.ts` /
  `projects-info.ts` (most current, maintained data) > project README/package.json >
  old `.tex` resume (treated as historical only, per prompt rule).
- Never invent: metrics, percentages, team sizes, unverified technologies, unverified
  responsibilities.

---

### Task 1: Source Evidence Ledger

**Files:**
- Create: `my-resume/docs/plans/2026-08-29-evidence-ledger.md`

**Interfaces:**
- Produces: A claim-to-source mapping table that Tasks 2–8 cite by row ID (e.g. `EL-04`)
  instead of re-deriving evidence. This is the single source of truth for "is this
  claim verifiable."

- [ ] **Step 1: Build the ledger table**

  Create the file with this exact structure, filled in from the research already done
  in this session (portfolio data files, project READMEs/manifests, LinkedIn export):

  ```markdown
  # Evidence Ledger — Master Resume Rebuild

  | ID | Claim | Source | Verified? |
  |----|-------|--------|-----------|
  | EL-01 | Dynamicore Strategies, Full Stack Developer Intern, May 2026–Present | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-02 | Built multi-agent orchestration for financial chatbot: FastAPI, LangGraph, LangChain, Redis | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-03 | Implemented RAG and agentic memory for contextual conversations | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-04 | Built specialist agents + routing Supervisor for intent/compliance | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-05 | Used LLMs, fine-tuning, deterministic Python compliance gates | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-06 | The Learner's Academy, Full Stack Engineer Intern, Jan–May 2026 | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-07 | Built school management system, multi-identity RBAC architecture | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-08 | Academic year scoping, attendance monitoring, result publishing, parent dashboard | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-09 | Stack: React, Zustand, Tailwind, shadcn/ui, Framer Motion, Vite, Bun, Elysia, Supabase, Zod, Razorpay, ngrok | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-10 | Dynamicore Strategies, Front-End Developer Intern, May–Jun 2025 | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-11 | Built fintech platform: portfolio tracking, investment explorer, live market data, loan comparison, KYC, gamified learning | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-12 | Stack: React, TypeScript, Tailwind CSS, shadcn/ui, Radix UI, Chart.js, Vercel | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-13 | Aunwesha Knowledge Tech, Data Visualization Intern, May–Jun 2024, Kolkata | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-14 | Analyzed datasets, built dashboards with Tableau/Kaggle; Java+MySQL+JDBC CRUD; Vega-Lite/jQuery/AJAX visualizations | my-portfolio/src/Data/experience-info.ts | Yes |
  | EL-15 | Ryder: JWT httpOnly cookie auth, role-based `/user/*` `/owner/*` routing | ryder/README.md | Yes |
  | EL-16 | Ryder: PostgreSQL schema — users/owners/cars/car_rentals/car_bookings | ryder/README.md (db-schema.sql reference) | Yes |
  | EL-17 | Ryder: Razorpay order creation + signature validation payment flow | ryder/README.md | Yes |
  | EL-18 | Ryder: Supabase Storage for file uploads (id_proof, ownership_proof) | ryder/README.md | Yes |
  | EL-19 | Ryder: Nodemailer email (verification, reset, 2FA, cancellations) + daily cron job for booking status | ryder/README.md | Yes |
  | EL-20 | TurfOnTop: Express.js REST API, JWT auth, PostgreSQL, Razorpay, Weather API, Cloudinary | turf-on-top/README.md | Yes |
  | EL-21 | TurfOnTop: dynamic real-time slot availability tied to bookings/cancellations | turf-on-top/README.md | Yes |
  | EL-22 | Trajectory (career-counselling-system): FastAPI ModelServer with dedicated vectorstore.py, embeddings.py, knowledge_base.py, documents.py | career-counselling-system/Assessment/ModelServer/App/Services/ | Yes |
  | EL-23 | Trajectory: requirements.txt confirms fastapi, langchain-community, langchain-text-splitters, langchain-core, chromadb, sentence-transformers | career-counselling-system/Assessment/ModelServer/requirements.txt | Yes |
  | EL-24 | Trajectory: Node/Express + Supabase backend, React+Redux Toolkit+Chart.js+react-d3-tree frontend | career-counselling-system/Server/package.json, Client/package.json | Yes |
  | EL-25 | Trajectory: psychometric assessment (BigFive dir present), job/interest matching, roadmap tree visualization | career-counselling-system directory structure | Yes |
  | EL-26 | LearnSphere: Elysia + Bun backend, Supabase, JWT (@elysiajs/jwt) | learn-sphere/backend/package.json | Yes |
  | EL-27 | LearnSphere: multi-identity RBAC, academic year scoping (3NF schema) | learn-sphere/README.md | Yes |
  | EL-28 | Suvidha: Hono + Bun backend, Supabase, Sarvam AI SDK, Zod validation, OCR (tesseract.js), PDF parsing (unpdf) | suvidha/server/package.json | Yes |
  | EL-29 | IEEE publication: "Decentralized Carbon Markets: Blockchain-Enabled Carbon Credit Exchange," IEEE, Apr 9 2026, co-authored, DOI https://ieeexplore.ieee.org/document/11471701 | User-supplied LinkedIn export (this session) | Yes |
  | EL-30 | Education: JKLU B.Tech CSE, 2022–2026, CGPA 7.5/10 | User-supplied LinkedIn export (this session) | Yes |
  | EL-31 | Education: DPS High School Diploma (Math & CS), Apr 2021–Apr 2022, 88% | User-supplied LinkedIn export (this session) | Yes |
  | EL-32 | Education: DPS Middle School Diploma, Apr 2019–Apr 2020, 91% | User-supplied LinkedIn export (this session) | Yes |
  | EL-33 | StoryWrite project | User confirmed: mock, never built | EXCLUDED |
  | EL-34 | Performance metrics / user counts / team sizes for any project | Not found in any source | Not available — omit |
  ```

- [ ] **Step 2: Cross-check for contradictions**

  Compare EL-10/EL-11/EL-12 (portfolio version of the fintech internship) against the
  old `.tex` resume's description of the same role (line 69-75: "Built responsive
  dashboards, investment marketplace, loan management, virtual trading platform,
  gamified learning modules"). Note in the ledger file, under a `## Notes` heading,
  that the portfolio version is more detailed/current and is the one to use, but the
  old resume's "investment marketplace" and "virtual trading platform" phrasing is
  consistent with EL-11 and may be blended if it reads more naturally.

- [ ] **Step 3: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/2026-08-29-evidence-ledger.md
  git commit -m "docs: add evidence ledger for master resume rebuild"
  ```

---

### Task 2: Header, Summary, and Skills Draft

**Files:**
- Create: `my-resume/docs/plans/draft-01-header-summary-skills.md`

**Interfaces:**
- Consumes: Evidence ledger from Task 1 (EL-01 through EL-28 for skills coverage).
- Produces: Finalized text for the HEADER, PROFESSIONAL SUMMARY, and TECHNICAL SKILLS
  sections — Task 8 (LaTeX assembly) copies this text verbatim into `.tex` commands.

- [ ] **Step 1: Draft the header block**

  ```markdown
  ## HEADER

  Riyansh Verma
  Software Engineer | Full-Stack Developer

  +91-9509175031 | riyanshverma01.2004@gmail.com
  linkedin.com/in/riyansh-verma-71728b261 | github.com/Riyanshverma | riyansh-portfolio-five.vercel.app
  ```

  Use the portfolio's live URL (`riyansh-portfolio-five.vercel.app`) as the portfolio
  link — it is the actively deployed one per this session's SEO work, not a placeholder.

- [ ] **Step 2: Draft the professional summary (2–4 lines)**

  Write a draft grounded only in EL-01 through EL-28. It must name: full-stack
  identity, TypeScript/React/Node.js, FastAPI/Python, PostgreSQL, REST APIs, and
  AI/RAG/LangChain as a secondary specialization. Example shape (rewrite in your own
  final wording, this is a structural example not a copy-paste target):

  ```markdown
  ## PROFESSIONAL SUMMARY

  Software Engineer specializing in full-stack web development and AI-powered
  application engineering. Builds production-oriented systems with React,
  TypeScript, Node.js, and FastAPI, backed by PostgreSQL and Supabase. Delivers
  Retrieval-Augmented Generation pipelines and multi-agent LLM systems using
  LangChain and LangGraph, alongside REST API design, authentication, and
  relational database schema design across full-stack products.
  ```

  Verify every noun phrase against the ledger before finalizing:
  - "full-stack web development" → EL-01, EL-06, EL-10
  - "AI-powered application engineering" → EL-02, EL-03, EL-22, EL-23
  - "React, TypeScript, Node.js, FastAPI" → EL-02, EL-09, EL-12, EL-24
  - "PostgreSQL and Supabase" → EL-16, EL-24, EL-26, EL-28
  - "RAG pipelines and multi-agent LLM systems" → EL-02, EL-03, EL-04, EL-22, EL-23
  - "REST API design, authentication, relational database schema design" → EL-15, EL-16, EL-20

- [ ] **Step 3: Draft TECHNICAL SKILLS, categorized**

  Only include items with an EL- citation. Use this category structure:

  ```markdown
  ## TECHNICAL SKILLS

  **Languages:** TypeScript, JavaScript, Python, SQL, Java, C++
  **Frontend:** React.js, Redux Toolkit, Zustand, Tailwind CSS, shadcn/ui, Radix UI, Chart.js
  **Backend / Runtime:** Node.js, Bun, Uvicorn
  **Backend Frameworks:** Express.js, Elysia, Hono, FastAPI
  **Databases:** PostgreSQL, MySQL, Supabase, Redis, CockroachDB, ChromaDB
  **AI Engineering:** LangChain, LangGraph, Retrieval-Augmented Generation (RAG), LLM Applications, AI Agents, Embeddings, Vector Search, Prompt Engineering
  **Developer Tools:** Git, GitHub, Docker, Razorpay API, REST APIs, JWT Authentication, WebSockets
  **Engineering Concepts:** Data Structures & Algorithms, OOP, Database Design, API Design, System Design, Authentication & Authorization
  ```

  For each line, write the EL- citations as an inline comment for reviewer traceability,
  e.g. `Python, SQL, Java, C++  <!-- Python: EL-02,EL-05,EL-23; Java: EL-14; C++: old resume, DSA coursework -->`.
  Flag C++ explicitly: it has no project-implementation evidence, only DSA/OOP academic
  context from the old resume's Skills line — decide in Step 4 whether to keep it under
  Languages or move it to a coursework-only mention.

- [ ] **Step 4: Resolve the C++ question**

  Keep C++ in Languages (it is a real, commonly-expected CS fundamentals signal for
  entry-level SWE roles and was explicitly listed in the user's original resume), but
  do NOT invent any project bullet using it. Note this decision in the draft file under
  a `## Decisions` heading.

- [ ] **Step 5: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/draft-01-header-summary-skills.md
  git commit -m "docs: draft header, summary, and skills for master resume"
  ```

---

### Task 3: Experience Section Draft

**Files:**
- Create: `my-resume/docs/plans/draft-02-experience.md`

**Interfaces:**
- Consumes: EL-01 through EL-14.
- Produces: Finalized bullet text per role for Task 8.

- [ ] **Step 1: Draft Dynamicore Strategies (current role) bullets**

  4 roles total exist (EL-01, EL-06, EL-10, EL-13). Write 3–4 bullets for the current
  Dynamicore role using the ACTION+TECH+WORK+PURPOSE formula, each citing its EL- ID:

  ```markdown
  ### Dynamicore Strategies — Full Stack Developer Intern
  May 2026 – Present | Rajasthan (Hybrid)

  - Developed multi-agent orchestration for a financial chatbot using FastAPI, LangGraph, LangChain, and Redis. (EL-02)
  - Implemented Retrieval-Augmented Generation (RAG) and agentic memory for contextual, multi-turn conversations. (EL-03)
  - Built specialist agents and a routing Supervisor to handle user intent classification and compliance checks. (EL-04)
  - Integrated LLM-based reasoning with deterministic Python compliance gates and model fine-tuning. (EL-05)
  ```

- [ ] **Step 2: Draft The Learner's Academy bullets**

  ```markdown
  ### The Learner's Academy — Full Stack Engineer Intern
  Jan 2026 – May 2026 | Rajasthan (Remote)

  - Built a school management system with a multi-identity RBAC architecture using React, Elysia, Bun, and Supabase. (EL-07, EL-09)
  - Implemented academic year scoping and attendance monitoring across student and teacher modules. (EL-08)
  - Developed result publishing with historical term data and a parent dashboard for progress tracking. (EL-08)
  ```

- [ ] **Step 3: Draft Dynamicore Strategies (earlier frontend role) bullets**

  ```markdown
  ### Dynamicore Strategies — Front-End Developer Intern
  May 2025 – Jun 2025 | Rajasthan (Remote)

  - Built a fintech platform frontend with real-time portfolio tracking, an investment explorer, and live market data using React, TypeScript, and Chart.js. (EL-11, EL-12)
  - Developed loan comparison tools, KYC integration flows, and gamified financial-literacy learning modules. (EL-11)
  - Implemented a responsive, mobile-first UI using shadcn/ui, Radix UI, and Tailwind CSS. (EL-12)
  ```

- [ ] **Step 4: Draft Aunwesha Knowledge Tech bullets**

  Use the verified "Data Visualization Intern" title, not "Data Analyst."

  ```markdown
  ### Aunwesha Knowledge Tech — Data Visualization Intern
  May 2024 – Jun 2024 | Kolkata (On-site)

  - Analyzed Kaggle datasets and built interactive dashboards using Tableau. (EL-14)
  - Developed Java-based CRUD operations against MySQL via JDBC for dataset management. (EL-14)
  - Built data-visualization web tools using Vega-Lite and jQuery/AJAX for bar, line, pie, and time-series charts. (EL-14)
  ```

- [ ] **Step 5: Decide inclusion/compression for the 4-role set**

  Four internships is a lot for one resume section. Per the master prompt's "concise"
  requirement, decide whether all 4 stay at 3+ bullets each, or the two Dynamicore
  stints get slightly compressed (e.g., earlier frontend role reduced to 2 bullets) to
  keep total Experience section length proportional to a 1-page-oriented resume. Record
  the decision under a `## Decisions` heading in the draft file. Default: keep 3
  bullets for the two most recent/relevant roles (current Dynamicore, Learner's
  Academy), 2 bullets for the two older ones (earlier Dynamicore, Aunwesha).

- [ ] **Step 6: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/draft-02-experience.md
  git commit -m "docs: draft experience section for master resume"
  ```

---

### Task 4: Projects Section Draft

**Files:**
- Create: `my-resume/docs/plans/draft-03-projects.md`

**Interfaces:**
- Consumes: EL-15 through EL-28.
- Produces: Finalized project bullets for Task 8. Project selection: Trajectory, Ryder,
  TurfOnTop are mandatory (highest technical depth + AI differentiation). LearnSphere
  and Suvidha are optional fourth/fifth slots if space allows — decide in Step 5.

- [ ] **Step 1: Draft Trajectory (lead project — strongest AI evidence)**

  ```markdown
  ### Trajectory — AI-Powered Career Counselling Platform
  React, Redux Toolkit, Node.js, Express.js, Supabase, Python, FastAPI, LangChain, ChromaDB

  - Engineered a Retrieval-Augmented Generation pipeline with FastAPI, LangChain, and ChromaDB, including document loading, chunking, and embedding generation via sentence-transformers. (EL-22, EL-23)
  - Built an AI career assistant that combines psychometric assessment results with retrieved job/education data to generate personalized learning roadmaps. (EL-25)
  - Designed a Node.js/Express/Supabase backend and a React frontend with Redux Toolkit, Chart.js, and react-d3-tree for interactive roadmap visualization. (EL-24)
  ```

- [ ] **Step 2: Draft Ryder**

  ```markdown
  ### Ryder — Full-Stack Car Rental Platform
  React, Node.js, Express.js, PostgreSQL, Supabase, Razorpay

  - Designed a relational PostgreSQL schema (users, owners, cars, rentals, bookings) supporting real-time car search, filtering, and availability. (EL-16)
  - Implemented JWT httpOnly-cookie authentication with role-based routing for separate user and owner flows. (EL-15)
  - Integrated Razorpay payment order creation and signature validation, and automated booking-status updates via a daily cron job. (EL-17, EL-19)
  ```

- [ ] **Step 3: Draft TurfOnTop**

  ```markdown
  ### TurfOnTop — Turf Booking Platform
  React, Node.js, Express.js, PostgreSQL, Razorpay, Weather API

  - Built a RESTful Express.js API with JWT authentication supporting real-time turf slot booking and dynamic availability updates. (EL-20, EL-21)
  - Integrated Razorpay payments, a Weather API for slot-time conditions, and Cloudinary for image/document storage. (EL-20)
  ```

- [ ] **Step 4: Draft optional LearnSphere / Suvidha bullets (for space-permitting inclusion)**

  ```markdown
  ### LearnSphere — School Management ERP (optional 4th project)
  React, Elysia, Bun, Supabase

  - Designed a multi-identity RBAC architecture and academic-year-scoped relational schema (3NF) for a multi-role school ERP. (EL-26, EL-27)

  ### Suvidha — Healthcare Platform (optional 5th project)
  Hono, Bun, Supabase, Sarvam AI

  - Built a Hono/Bun backend integrating Sarvam AI, OCR (Tesseract.js), and PDF parsing for automated document processing. (EL-28)
  ```

- [ ] **Step 5: Decide final project count**

  Per the master prompt's project-selection criteria (technical depth, backend
  complexity, AI engineering, relevance over CRUD simplicity), default to 3 projects:
  Trajectory, Ryder, TurfOnTop. Record this decision and the reasoning under a
  `## Decisions` heading — note LearnSphere/Suvidha are held in reserve for a
  Backend-Developer-tailored variant of this resume later, not discarded.

- [ ] **Step 6: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/draft-03-projects.md
  git commit -m "docs: draft projects section for master resume"
  ```

---

### Task 5: Education Section Draft

**Files:**
- Create: `my-resume/docs/plans/draft-04-education.md`

**Interfaces:**
- Consumes: EL-30, EL-31, EL-32.
- Produces: Finalized education text for Task 8.

- [ ] **Step 1: Draft education entries**

  ```markdown
  ## EDUCATION

  Bachelor of Technology, Computer Science Engineering
  JK Lakshmipat University, Jaipur, Rajasthan | 2022 – 2026 | CGPA: 7.5/10

  High School Diploma, Mathematics and Computer Science
  Delhi Public School, Jaipur, Rajasthan | Apr 2021 – Apr 2022 | 88%
  ```

- [ ] **Step 2: Decide on Middle School entry**

  Per the master prompt's explicit rule ("Do not allow high-school information to
  occupy valuable space over professional experience, projects, technical skills, or
  research" and "School-level education should only remain if space permits"), exclude
  the Middle School Diploma (Apr 2019–Apr 2020, 91%) from the resume — it predates
  even high school and adds no signal beyond what the High School line already
  conveys for a candidate with 4 internships and a publication. Record this decision
  explicitly in the draft file so it's understood as a deliberate omission, not a
  missed fact — the fact itself stays verified in the evidence ledger (EL-32) in case
  a future version needs it.

- [ ] **Step 3: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/draft-04-education.md
  git commit -m "docs: draft education section for master resume"
  ```

---

### Task 6: Research & Publications Section Draft

**Files:**
- Create: `my-resume/docs/plans/draft-05-research.md`

**Interfaces:**
- Consumes: EL-29.
- Produces: Finalized publication text for Task 8.

- [ ] **Step 1: Draft the publication entry**

  ```markdown
  ## RESEARCH & PUBLICATIONS

  Decentralized Carbon Markets: Blockchain-Enabled Carbon Credit Exchange
  IEEE | Published April 2026 | https://ieeexplore.ieee.org/document/11471701

  Co-authored research addressing inefficiency, lack of transparency, and limited
  accessibility in offline carbon credit trading through a blockchain-based
  decentralized exchange design.
  ```

- [ ] **Step 2: Verify description matches source, not invention**

  Confirm the description sentence only restates the abstract snippet the user
  provided ("current offline carbon credit trading market suffers from
  inefficiencies, lack of transparency, and limited accessibility... blockchain
  technology...") — do not add unverified technical claims like "Proof-of-Stake" or
  "Layer-2 scaling" since those were only listed as *possible* concepts in the master
  prompt, not confirmed as part of this paper's actual content. Leave them out unless
  the user confirms the paper covers them.

- [ ] **Step 3: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/draft-05-research.md
  git commit -m "docs: draft research and publications section for master resume"
  ```

---

### Task 7: Section Ordering & Space Budget Decision

**Files:**
- Create: `my-resume/docs/plans/draft-06-layout-decisions.md`

**Interfaces:**
- Consumes: Drafts from Tasks 2–6.
- Produces: Final section order and inclusion/exclusion list for Task 8.

- [ ] **Step 1: Confirm section order**

  Per the master prompt Section 4: HEADER → PROFESSIONAL SUMMARY → TECHNICAL SKILLS →
  PROFESSIONAL EXPERIENCE → SELECTED PROJECTS → EDUCATION → RESEARCH & PUBLICATIONS →
  CERTIFICATIONS (only if evidence exists — none found, so this section is omitted
  entirely, not left as an empty heading).

- [ ] **Step 2: Estimate length and flag overflow risk**

  Count: 1 summary paragraph + 8 skill category lines + 4 experience roles
  (3+3+2+2 = 10 bullets) + 3 projects (3+3+2 = 8 bullets) + 2 education lines + 1
  publication entry. This is dense for a single page in the existing `resume.cls`
  margins (0.4in). Record in this file whether the LaTeX build (Task 8) fits one page;
  if not, the fallback order of trimming is: (1) drop earlier Dynamicore frontend role
  to 2 bullets if not already, (2) drop Aunwesha to 2 bullets, (3) drop LearnSphere/
  Suvidha mentions (already excluded per Task 4 Step 5), (4) as a last resort only,
  drop the oldest role (Aunwesha) entirely — but only if the user approves, since it
  is real, verified experience.

- [ ] **Step 3: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/draft-06-layout-decisions.md
  git commit -m "docs: finalize section order and space-budget plan for master resume"
  ```

---

### Task 8: Assemble Final `my-resume.tex`

**Files:**
- Modify: `my-resume/my-resume.tex` (full rewrite, same `resume.cls` document class)

**Interfaces:**
- Consumes: All finalized draft text from Tasks 2–7.
- Produces: The compilable `.tex` source. No new interfaces for later tasks — this is
  the terminal content task.

- [ ] **Step 1: Replace the OBJECTIVE section**

  Delete the `\begin{rSection}{OBJECTIVE}...\end{rSection}` block entirely (lines
  13-22 of the current file) and replace with a `SUMMARY` section using the Task 2
  Step 2 final text, in an `rSection` block:

  ```latex
  \begin{rSection}{SUMMARY}
  {<final summary text from draft-01>}
  \end{rSection}
  ```

- [ ] **Step 2: Rebuild the SKILLS section**

  Replace the existing `\begin{rSection}{SKILLS}...\end{rSection}` tabular block with
  the categorized version from Task 2 Step 3, using the same `tabular` pattern already
  in the file (one row per category, category name bold via `>{\bfseries}l`).

- [ ] **Step 3: Rebuild EXPERIENCE (renamed from INTERNSHIPS)**

  Replace the `INTERNSHIPS` section with an `EXPERIENCE` section containing all 4
  roles from Task 3, each as a `\textbf{Role} \hfill Dates \\ Company \hfill
  \textit{Location}` header followed by an `itemize` block, matching the existing
  LaTeX pattern used for the one internship already in the file (lines 59-77).

- [ ] **Step 4: Rebuild PROJECTS**

  Replace the existing PROJECTS section (Ryder/TurfOnTop/Trajectory/StoryWrite) with
  the Task 4 Step 5 final project list (Trajectory, Ryder, TurfOnTop), using the
  existing `\item \textbf{Name -}` pattern, followed by a `Technologies Used:` line
  per project.

- [ ] **Step 5: Update EDUCATION**

  Replace the existing Education section with Task 5's final text (JKLU with CGPA,
  DPS High School only — no Middle School entry).

- [ ] **Step 6: Add RESEARCH & PUBLICATIONS**

  Add a new `\begin{rSection}{RESEARCH \& PUBLICATIONS}...\end{rSection}` block after
  Education, using Task 6's final text, placed before the closing commented-out
  Extra-Curricular section.

- [ ] **Step 7: Compile and verify one-page fit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  pdflatex my-resume.tex
  ```

  Open the resulting PDF (or use a PDF page-count tool) and confirm page count. If it
  exceeds 1 page, apply the Task 7 Step 2 fallback trimming order and recompile.

- [ ] **Step 8: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add my-resume.tex my-resume.pdf
  git commit -m "feat: rebuild master resume with verified experience, projects, and publication"
  ```

---

### Task 9: Deliver Change Log, Keyword Map, and Optimization Audit

**Files:**
- Create: `my-resume/docs/plans/2026-08-29-final-deliverables.md`

**Interfaces:**
- Consumes: Final `my-resume.tex` from Task 8, evidence ledger from Task 1.
- Produces: The four deliverables the original master prompt requires beyond the
  resume itself (Section 31, parts B–E).

- [ ] **Step 1: Write the Change Log (old resume vs. new)**

  Compare against the original `.tex` (git history has it prior to Task 8's commit).
  Cover: removed (Objective, StoryWrite, Middle School — deliberate), added
  (Research & Publications, 3 additional experience roles, CGPA), rewritten
  (Skills categorization, all project bullets), promoted (Trajectory to lead
  project), deprioritized (earlier fintech internship bullets condensed).

- [ ] **Step 2: Write the Keyword Map**

  Table: `Keyword | Evidence in Resume | Source (EL- ID)`, covering every keyword
  from the master prompt's Section 21 that actually appears in the final resume
  (skip any not present — do not force-fit).

- [ ] **Step 3: Write the Resume Optimization Audit**

  Score 1–10 on: ATS readability, Full-Stack relevance, Software Engineer relevance,
  Backend relevance, Frontend relevance, AI Engineering relevance, Database relevance,
  System Design relevance, Keyword coverage, Evidence/achievement quality, Recruiter
  readability. Label explicitly as "Resume Optimization Audit," not a real ATS score,
  per the master prompt's Section 29 instruction. Follow with the Recruiter Test
  (Section 28's 10 questions, answered plainly).

- [ ] **Step 4: Write the Missing Information list**

  List what would strengthen the resume but isn't available: performance metrics,
  user counts, API/endpoint counts per project, team sizes, deployment/CI-CD
  evidence, testing coverage evidence — per master prompt Section 31E. Do not invent
  any of these; this section is a request list for the user.

- [ ] **Step 5: Present all deliverables to the user in-chat**

  Do not just leave this as a file — surface the Change Log, Keyword Map, Audit, and
  Missing Information directly in the conversation per the master prompt's Section 31
  output format, with a pointer to the full file.

- [ ] **Step 6: Commit**

  ```bash
  cd /Users/riyanshverma/Desktop/my-projects/my-resume
  git add docs/plans/2026-08-29-final-deliverables.md
  git commit -m "docs: add change log, keyword map, and optimization audit for master resume"
  ```

---

## Self-Review Notes

- **Spec coverage:** Every numbered section of the master prompt (1–31) maps to a task
  above except Sections 22–27 (ATS formatting rules, writing style, bullet length,
  master-vs-tailored distinction, JD alignment rules, anti-gaming rules) — these are
  *constraints applied throughout* Tasks 2–8 rather than standalone deliverables, so
  they are folded into the Global Constraints section and into each drafting task's
  instructions (e.g., Task 3's ACTION+TECH+WORK+PURPOSE formula, Task 8's LaTeX
  ATS-safe single-column requirement already satisfied by the existing `resume.cls`).
- **Placeholder scan:** No TBD/TODO markers used; every task step contains literal
  draft text or an exact file/command.
- **Certifications section:** Omitted as a task entirely — no certification evidence
  exists anywhere in the research, and the master prompt explicitly says to skip it
  when evidence is weak/absent rather than force an empty section.
