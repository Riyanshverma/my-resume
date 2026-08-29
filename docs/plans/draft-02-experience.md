# Draft 02 — Experience Section

Source: Task 3 of the master resume rebuild. Grounded exclusively in
`docs/plans/2026-08-29-evidence-ledger.md` (EL-01 through EL-14). Task 8
(LaTeX assembly) copies the text below verbatim into `.tex` commands.

---

## EXPERIENCE

### Dynamicore Strategies — Full Stack Developer Intern
May 2026 – Present | Rajasthan (Hybrid)

- Developed multi-agent orchestration for a financial chatbot using FastAPI, LangGraph, LangChain, and Redis. (EL-02)
- Implemented Retrieval-Augmented Generation (RAG) and agentic memory for contextual, multi-turn conversations. (EL-03)
- Built specialist agents and a routing Supervisor with LLM-based reasoning, deterministic Python compliance gates, and model fine-tuning to handle user intent classification and compliance checks. (EL-04, EL-05)

### The Learner's Academy — Full Stack Engineer Intern
Jan 2026 – May 2026 | Rajasthan (Remote)

- Built a school management system with a multi-identity RBAC architecture using React, Elysia, Bun, and Supabase. (EL-07, EL-09)
- Implemented academic year scoping and attendance monitoring across student and teacher modules. (EL-08)
- Developed result publishing with historical term data and a parent dashboard for progress tracking. (EL-08)

### Dynamicore Strategies — Front-End Developer Intern
May 2025 – Jun 2025 | Rajasthan (Remote)

- Built a fintech platform frontend with real-time portfolio tracking, an investment explorer, live market data, loan comparison tools, KYC integration flows, and gamified financial-literacy learning modules using React, TypeScript, and Chart.js. (EL-11, EL-12)
- Implemented a responsive, mobile-first UI using shadcn/ui, Radix UI, and Tailwind CSS. (EL-12)

### Aunwesha Knowledge Tech — Data Visualization Intern
May 2024 – Jun 2024 | Kolkata (On-site)

- Analyzed Kaggle datasets and built interactive dashboards using Tableau, alongside Java-based CRUD operations against MySQL via JDBC for dataset management. (EL-14)
- Built data-visualization web tools using Vega-Lite and jQuery/AJAX for bar, line, pie, and time-series charts. (EL-14)

---

## Decisions

### Bullet-count compression (Step 5)

**Decision:** The four internships are compressed unevenly rather than kept
uniform at 3+ bullets each: **3 bullets** for the two most recent/relevant
roles (Dynamicore Strategies — Full Stack Developer Intern, current; The
Learner's Academy — Full Stack Engineer Intern), and **2 bullets** for the
two older roles (Dynamicore Strategies — Front-End Developer Intern;
Aunwesha Knowledge Tech — Data Visualization Intern). This matches the
brief's stated default.

**Rationale:**

1. Four internship entries is already a lot of vertical space for a
   1-page-oriented resume. Compressing the two oldest/least-recent roles to
   2 bullets each keeps total Experience section length proportional
   without dropping any distinct EL-backed claim.
2. Recency and relevance to the target identity (Software Engineer /
   Full-Stack Developer, per draft-01's Professional Summary) favor giving
   the most space to the current full-stack/AI-engineering role and the
   most recent full-stack role (The Learner's Academy), both of which
   carry the resume's primary positioning.
3. No content was deleted to hit the 2-bullet counts for the older roles —
   the brief's example bullets for Step 3 (Dynamicore frontend) and Step 4
   (Aunwesha) were merged/combined rather than cut, so every EL-ID citation
   from the brief's examples (EL-05, EL-11, EL-12, EL-14) is still present
   in the compressed version:
   - Dynamicore Front-End: the brief's 3-bullet example (fintech
     frontend+stack / loan+KYC+gamified modules / responsive UI) was
     merged into 2 bullets by folding the loan comparison, KYC, and
     gamified-learning-module claims (EL-11) into the first bullet
     alongside the platform description, leaving the second bullet for
     the responsive/mobile-first UI stack (EL-12).
   - Aunwesha: the brief's 3-bullet example (Tableau dashboards / Java+MySQL
     CRUD / Vega-Lite+jQuery tools) was merged into 2 bullets by combining
     the Tableau-dashboard claim and the Java/MySQL/JDBC CRUD claim into one
     bullet (both are EL-14), leaving the second bullet for the Vega-Lite/
     jQuery/AJAX visualization tools (also EL-14).
   - The current Dynamicore role's brief example (4 bullets: EL-02, EL-03,
     EL-04, EL-05) was compressed to 3 bullets by merging EL-04 and EL-05
     into one bullet (specialist agents + routing Supervisor, combined with
     the LLM-reasoning/compliance-gates/fine-tuning claim), since both
     describe the same agent-routing/compliance-check subsystem.
   - The Learner's Academy bullets were kept at the brief's original 3,
     unmodified, since it is already at the 3-bullet target.

**Explicitly rejected:** Dropping any EL-backed claim entirely to shorten
bullets (e.g., omitting KYC integration or the Vega-Lite tools) was
rejected — compression was achieved only by merging existing claims into
fewer bullets, not by deleting evidence-backed content.
