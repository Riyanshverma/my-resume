# Draft 01 — Header, Professional Summary, Technical Skills

Source: Task 2 of the master resume rebuild. Grounded exclusively in
`docs/plans/2026-08-29-evidence-ledger.md` (EL-01 through EL-28). Task 8
(LaTeX assembly) copies the text below verbatim into `.tex` commands.

---

## HEADER

Riyansh Verma
Software Engineer | Full-Stack Developer

+91-9509175031 | riyanshverma01.2004@gmail.com
linkedin.com/in/riyansh-verma-71728b261 | github.com/Riyanshverma | riyansh-portfolio-five.vercel.app

---

## PROFESSIONAL SUMMARY

Software Engineer with full-stack development experience across React,
TypeScript, Node.js, and FastAPI, backed by PostgreSQL and Supabase, gained
through internships and independent projects. Designs and ships REST APIs,
authentication systems, and relational database schemas end-to-end. Works as
an AI engineering specialist as a secondary focus, building
Retrieval-Augmented Generation pipelines and multi-agent LLM systems with
LangChain and LangGraph for production chatbot and assessment platforms.

**Noun-phrase verification against the ledger:**

- "full-stack development experience ... internships and independent projects" → EL-01, EL-06, EL-10
- "React, TypeScript, Node.js, and FastAPI" → EL-02 (FastAPI), EL-09 (React), EL-12 (React, TypeScript), EL-24 (Node/Express)
- "PostgreSQL and Supabase" → EL-16 (PostgreSQL schema), EL-24 (Supabase backend), EL-26 (Supabase), EL-28 (Supabase)
- "REST APIs, authentication systems, and relational database schemas" → EL-15 (JWT auth), EL-16 (PostgreSQL schema), EL-20 (Express REST API, JWT auth, PostgreSQL)
- "AI engineering specialist as a secondary focus" → positioning constraint (SWE/full-stack primary, AI secondary), supported by EL-02, EL-03, EL-22, EL-23
- "Retrieval-Augmented Generation pipelines and multi-agent LLM systems" → EL-02 (multi-agent orchestration), EL-03 (RAG + agentic memory), EL-04 (specialist agents + routing Supervisor)
- "LangChain and LangGraph" → EL-02, EL-23 (langchain-community, langchain-text-splitters, langchain-core)
- "production chatbot and assessment platforms" → EL-02/EL-03/EL-04/EL-05 (financial chatbot, Dynamicore), EL-22/EL-23/EL-25 (Trajectory career-counselling assessment system)

No first-person pronouns used. No fluff words ("passionate," "eager," "hardworking") used. Identity ordering: Software Engineer / Full-Stack Developer stated first and given the most detail; AI engineering introduced explicitly as "a secondary focus."

---

## TECHNICAL SKILLS

**Languages:** TypeScript, JavaScript, Python, SQL, Java, C++ <!-- TypeScript: EL-09,EL-12; JavaScript: EL-09,EL-12,EL-24; Python: EL-02,EL-05,EL-22,EL-23; SQL: EL-16,EL-20; Java: EL-14; C++: old resume, DSA/OOP coursework only — see Decisions -->
**Frontend:** React.js, Redux Toolkit, Zustand, Tailwind CSS, shadcn/ui, Radix UI, Chart.js <!-- React.js: EL-09,EL-12,EL-24; Redux Toolkit: EL-24; Zustand: EL-09; Tailwind CSS: EL-09,EL-12; shadcn/ui: EL-09,EL-12; Radix UI: EL-12; Chart.js: EL-12,EL-24 -->
**Backend / Runtime:** Node.js, Bun <!-- Node.js: EL-24; Bun: EL-09,EL-26,EL-28 -->
**Backend Frameworks:** Express.js, Elysia, Hono, FastAPI <!-- Express.js: EL-20,EL-24; Elysia: EL-09,EL-26; Hono: EL-28; FastAPI: EL-02,EL-22,EL-23 -->
**Databases:** PostgreSQL, MySQL, Supabase, Redis, ChromaDB <!-- PostgreSQL: EL-16,EL-20; MySQL: EL-14; Supabase: EL-09,EL-24,EL-26,EL-28; Redis: EL-02; ChromaDB: EL-23 -->
**AI Engineering:** LangChain, LangGraph, Retrieval-Augmented Generation (RAG), LLM Applications, AI Agents, Embeddings, Vector Search, Prompt Engineering <!-- LangChain: EL-02,EL-23; LangGraph: EL-02; RAG: EL-03,EL-23; LLM Applications: EL-02,EL-05,EL-22; AI Agents: EL-02,EL-04; Embeddings: EL-22,EL-23; Vector Search: EL-22,EL-23 (vectorstore.py, chromadb); Prompt Engineering: EL-02,EL-05 -->
**Developer Tools:** Razorpay API, REST APIs, JWT Authentication <!-- Razorpay API: EL-09,EL-17; REST APIs: EL-20; JWT Authentication: EL-15,EL-20,EL-26 -->
**Engineering Concepts:** OOP, Database Design, API Design, System Design, Authentication & Authorization <!-- OOP: EL-14 (Java CRUD); Database Design: EL-16,EL-27 (3NF schema); API Design: EL-20,EL-22; System Design: EL-02,EL-04,EL-07 (multi-agent orchestration, RBAC architecture); Authentication & Authorization: EL-15,EL-20,EL-26 -->

---

## Decisions

### C++ (Step 4)

**Decision:** C++ is kept under **Languages**. No project bullet, achievement,
or metric mentioning C++ is added anywhere in the resume.

**Rationale:** The evidence ledger contains no project-implementation
evidence for C++ — no repository, README, or experience entry cites it. Its
only basis is the user's prior/old resume, where it appeared as part of a
Skills line alongside Data Structures & Algorithms and OOP coursework
context. It is retained as a bare language-list entry because:

1. It is a real, previously-claimed skill (not fabricated for this rebuild).
2. C++ is a standard, commonly-expected CS-fundamentals signal for
   entry-level Software Engineer / Full-Stack Developer roles (the primary
   identity this resume targets), and is conventionally listed even without
   a shipped C++ project, since it typically reflects DSA/OOP coursework
   rather than production work.
3. Listing it in a bare Languages line makes no claim beyond "familiar with
   this language" — unlike a bullet, which would assert a specific
   accomplishment. No such accomplishment claim is made.

**Explicitly rejected:** Any resume bullet, project line, or achievement
statement using C++ (e.g., "built X in C++," "optimized Y using C++") is
excluded, since no such work is present in the evidence ledger.

### Deviation from the brief's Step 3 example skills block

The brief's Step 3 gives an example Technical Skills block as a *category
structure* to follow, but that example also lists several items with no
supporting EL- entry: **Uvicorn**, **CockroachDB**, **Git**, **GitHub**,
**Docker**, **WebSockets**, and **Data Structures & Algorithms**. The
brief's own governing sentence for this step is "Only include items with an
EL- citation," and the project's global constraint states every technology
in the skills list must trace to an EL-ID.

Where the illustrative example and the governing rule conflict, this draft
follows the rule: these seven items are **dropped** from the Technical
Skills section rather than included with a flag, since no EL entry
(EL-01–EL-28) references Uvicorn, CockroachDB, Docker, WebSockets, Git,
GitHub, or Data Structures & Algorithms by name or clear implication. The
`Backend / Runtime` category is retained (Node.js, Bun are EL-backed) with
Uvicorn removed; `Databases` retains PostgreSQL/MySQL/Supabase/Redis/ChromaDB
with CockroachDB removed; `Developer Tools` retains only Razorpay
API/REST APIs/JWT Authentication, with Git, GitHub, Docker, and WebSockets
removed; `Engineering Concepts` drops Data Structures & Algorithms for the
same reason, retaining OOP, Database Design, API Design, System Design, and
Authentication & Authorization, all of which have direct EL- support.

If a reviewer later finds ledger-worthy evidence for any of these seven
items (e.g., a repository README mentioning Docker or a CI file), they can
be reinstated with a proper EL- citation in a future ledger update — this
draft does not fabricate that evidence to preserve the brief's example
list.
