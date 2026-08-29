# Draft 03 — Projects Section

Source: Task 4 of the master resume rebuild. Grounded exclusively in
`docs/plans/2026-08-29-evidence-ledger.md` (EL-15 through EL-28). Task 8
(LaTeX assembly) copies the text below verbatim into `.tex` commands.

---

## PROJECTS

### Trajectory — AI-Powered Career Counselling Platform
React, Redux Toolkit, Node.js, Express.js, Supabase, Python, FastAPI, LangChain, ChromaDB

- Engineered a Retrieval-Augmented Generation pipeline with FastAPI, LangChain, and ChromaDB, including document loading, chunking, and embedding generation via sentence-transformers. (EL-22, EL-23)
- Built an AI career assistant that combines psychometric assessment results with retrieved job/education data to generate personalized learning roadmaps. (EL-25)
- Designed a Node.js/Express/Supabase backend and a React frontend with Redux Toolkit, Chart.js, and react-d3-tree for interactive roadmap visualization. (EL-24)

### Ryder — Full-Stack Car Rental Platform
React, Node.js, Express.js, PostgreSQL, Supabase, Razorpay

- Designed a relational PostgreSQL schema (users, owners, cars, rentals, bookings) supporting real-time car search, filtering, and availability. (EL-16)
- Implemented JWT httpOnly-cookie authentication with role-based routing for separate user and owner flows. (EL-15)
- Integrated Razorpay payment order creation and signature validation, and automated booking-status updates via a daily cron job. (EL-17, EL-19)

### TurfOnTop — Turf Booking Platform
React, Node.js, Express.js, PostgreSQL, Razorpay, Weather API

- Built a RESTful Express.js API with JWT authentication supporting real-time turf slot booking and dynamic availability updates. (EL-20, EL-21)
- Integrated Razorpay payments, a Weather API for slot-time conditions, and Cloudinary for image/document storage. (EL-20)

---

## Decisions

### Final project count (Step 5)

**Decision:** The Projects section ships with **3 projects** — Trajectory,
Ryder, and TurfOnTop. LearnSphere and Suvidha are held in reserve, not
discarded: they remain drafted below and are candidates for a fourth/fifth
slot in a future Backend-Developer-tailored variant of this resume.

**Rationale:**

1. Per the master prompt's project-selection criteria (technical depth,
   backend complexity, AI engineering, relevance over CRUD simplicity),
   Trajectory, Ryder, and TurfOnTop score highest:
   - Trajectory carries the strongest AI-engineering evidence (RAG pipeline,
     LangChain/ChromaDB, embeddings) and is the clearest differentiator for
     an AI-facing Software Engineer identity — it leads the section.
   - Ryder has the greatest backend/schema complexity of the remaining
     candidates: a multi-entity relational schema, role-based auth, a
     third-party payment integration with signature validation, and a
     scheduled background job.
   - TurfOnTop adds a second full end-to-end booking platform with a
     distinct integration surface (Weather API, Cloudinary) without
     duplicating Ryder's domain, reinforcing breadth without redundancy.
2. LearnSphere (EL-26, EL-27) and Suvidha (EL-28) are technically strong
   (multi-identity RBAC, Sarvam AI/OCR/PDF processing) but overlap in theme
   with work already represented elsewhere in the resume — LearnSphere's
   RBAC/school-ERP domain echoes the Learner's Academy experience entry
   (EL-07, EL-08), and both are more naturally positioned as backend-only
   showcases. Including them as a 4th/5th project risks crowding a
   1-page-oriented resume and diluting the AI/full-stack positioning
   established by the three mandatory projects.
3. Holding LearnSphere and Suvidha in reserve (rather than discarding them)
   preserves optionality: a Backend-Developer-tailored variant of this
   resume can swap in LearnSphere and/or Suvidha in place of, or alongside,
   the more frontend-visible TurfOnTop/Ryder projects, since their backend
   depth (RBAC architecture, 3NF schema design, Sarvam AI integration, OCR/
   PDF parsing) is more relevant to that audience.

**Explicitly rejected:** Shipping all 5 projects was rejected as exceeding
reasonable space for a 1-page-oriented resume and diluting focus on the
strongest three. Dropping LearnSphere/Suvidha's evidence entirely from this
document was also rejected — both are kept fully drafted below so no
research is lost and they can be reused verbatim later.

---

## Reserve — optional projects (not included in this draft)

### LearnSphere — School Management ERP (optional 4th project)
React, Elysia, Bun, Supabase

- Designed a multi-identity RBAC architecture and academic-year-scoped relational schema (3NF) for a multi-role school ERP. (EL-26, EL-27)

### Suvidha — Healthcare Platform (optional 5th project)
Hono, Bun, Supabase, Sarvam AI

- Built a Hono/Bun backend integrating Sarvam AI, OCR (Tesseract.js), and PDF parsing for automated document processing. (EL-28)
