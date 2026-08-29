# Draft 06 — Section Ordering & Space Budget Decision

Source: Task 7 of the master resume rebuild. Synthesizes drafts 01–05
(Tasks 2–6) into the final section order and inclusion/exclusion list that
Task 8 (LaTeX assembly) will consume directly. No LaTeX is written or
compiled in this task.

---

## Step 1: Section order (confirmed)

Per the master prompt Section 4, the final section order is:

1. HEADER
2. PROFESSIONAL SUMMARY
3. TECHNICAL SKILLS
4. PROFESSIONAL EXPERIENCE
5. SELECTED PROJECTS
6. EDUCATION
7. RESEARCH & PUBLICATIONS

**CERTIFICATIONS is omitted entirely** — not left as an empty heading. No
certification evidence exists in the evidence ledger, so per the master
prompt's rule (only include a section if evidence exists), this section is
dropped from the document rather than rendered empty.

This order is confirmed as final for Task 8.

---

## Step 2: Length estimate and overflow risk (qualitative)

No `.tex` file exists yet — Task 8 has not run — so this is a qualitative
estimate based on the content counts fixed by drafts 01–05, not a compiled
page count. Actual page-fit to be confirmed when Task 8 compiles the .tex
file.

**Content inventory going into Task 8:**

- 1 Professional Summary paragraph (draft-01)
- 8 Technical Skills category lines (draft-01: Languages, Frontend,
  Backend/Runtime, Backend Frameworks, Databases, AI Engineering, Developer
  Tools, Engineering Concepts)
- 4 Experience roles, 10 bullets total (draft-02: 3 + 3 + 2 + 2 — Dynamicore
  Full Stack Developer Intern (3), The Learner's Academy Full Stack Engineer
  Intern (3), Dynamicore Front-End Developer Intern (2), Aunwesha Knowledge
  Tech Data Visualization Intern (2))
- 3 Projects, 8 bullets total (draft-03: 3 + 3 + 2 — Trajectory (3), Ryder
  (3), TurfOnTop (2))
- 2 Education lines (draft-04: B.Tech CSE, High School Diploma)
- 1 Publication entry (draft-05: IEEE carbon-credit paper)

**Density assessment:** This is dense for a single page under
`resume.cls`'s 0.4in margins. Seven populated sections (Header through
Research & Publications), 18 total bullets across Experience and Projects,
an 8-category skills block, and a full paragraph summary is a substantial
amount of content to fit on one page even with tight margins. This is
flagged as a real overflow risk, not a marginal one — the fallback trimming
order below should be treated as likely-needed rather than a purely
contingency-only measure.

Note: draft-01's Developer Tools category now includes Git and GitHub
(added via ledger amendment EL-35, after the brief was written). This does
not change the "8 skill category lines" count used above — the category
count is unaffected, since Git/GitHub were added as additional items within
the existing Developer Tools line, not as a new category. It does mean the
Developer Tools line itself is slightly longer, which marginally adds to
the density concern noted above but does not change the section or line
count going into the estimate.

**Fallback trimming order, if Task 8's compiled `.tex` does not fit one
page**, in the exact priority order specified by the brief:

1. Drop the earlier Dynamicore Front-End Developer Intern role to 2 bullets,
   if not already at 2 (per draft-02, it is already compressed to 2
   bullets, so this step is already satisfied going into Task 8).
2. Drop the Aunwesha Knowledge Tech role to 2 bullets, if not already at 2
   (per draft-02, it is already compressed to 2 bullets, so this step is
   also already satisfied going into Task 8).
3. Drop LearnSphere / Suvidha mentions — already excluded per Task 4 Step 5
   (draft-03 confirms these two projects are held in reserve, not included
   in the shipped 3-project Projects section, so this step is also already
   satisfied going into Task 8).
4. As a last resort only, drop the oldest role (Aunwesha Knowledge Tech)
   entirely — but only if the user approves, since it is real, verified
   experience. This step must not be applied unilaterally; it requires
   explicit user sign-off before removal.

Because steps 1–3 are already satisfied by the content as drafted in
02/03, if Task 8's compiled document still overflows one page, the next
available lever is step 4 (subject to user approval) or further bullet-level
compression not enumerated here.

---

## Step 3: Commit

This file is committed with the message specified by the brief's Step 3.
