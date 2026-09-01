# Open Source Contribution Research — Full Report
Compiled 2026-08-31 via live GitHub API research (GitHub MCP server, authenticated; contributor counts via GitHub REST pagination). All stars/issues/contributors/activity figures below were fetched live on this date — treat as a snapshot, not a historical claim. Where a figure could not be fetched (rate-limited), it is explicitly marked **"Not verified this session"** with fork count given as a rough proxy, rather than guessed.

**Methodology notes**
- "Open issues" = GitHub API `open_issues_count`, which bundles open PRs with open issues (typically ~10-25% are PRs on active repos).
- "Recent activity" = confirmed by pulling the most recently *updated* open issues per repo; every Tier 1/2/3 repo below (except where noted) had issues actively triaged/commented on **within the last 24-48 hours** of research (Aug 30-31, 2026) — this is direct evidence of a live maintainer/community loop, not just a stale star count.
- "Contributors" = unique commit authors via GitHub's contributors-pagination trick (verified live).
- Archived repos (no new issues/PRs possible) were found and excluded: **FlowiseAI/Flowise**, RedPlanetHQ/tegon, maybe-finance/maybe, fastenhealth/fasten-onprem, reorproject/reor, Peppermint-Lab/peppermint — do not contribute to these despite star counts.
- Scoring is out of 100 per the rubric: Technical fit(20) / App relevance(15) / Issue availability(15) / Issue quality(10) / Maintenance(15) / External contributor health(10) / Codebase accessibility(5) / Long-term potential(10).

Total repositories researched in depth: **81** (Tier 1: 20, Tier 2: 25, Tier 3: 23, Tier 4: 13).

---

## TIER 1 — 20 Best Immediate Opportunities
*(Verified: stars, issues, language, contributors, live sample issues, activity)*

### 1. supabase/supabase — Score 91/100
https://github.com/supabase/supabase
- **What it is**: Open-source Firebase alternative — Postgres database, auth, instant APIs, edge functions, realtime, storage. Used by hundreds of thousands of production apps.
- **Stack**: TypeScript, Postgres, Deno, WebSockets. **Stars**: 108,643 | **Open issues**: 1,085 | **Contributors**: 2,023 (verified) | **Language**: TypeScript
- **Activity**: Issues actively triaged within hours (multiple updated same day as research).
- **Match**: Postgres + TypeScript + realtime/WebSockets is a near-perfect match to your stack.
- **Contribution areas**: Auth (GoTrue), RLS/Postgres tooling, dashboard (React), realtime, docs.
- **Sample open issues**: #49639 Policy/Role panel redesign (L1, frontend) · #49727 GoTrue auth intermittent freeze (L2, backend) · #49655 PGRST303 JWT issue with new secret key format (L2/L3) · #48302 RLS INSERT policy rejected by PostgREST (L2, has PR opened) · #49739 setup.sh Docker permission bug (L1)
- **First-PR suitability**: High (huge external-issue-labeled backlog specifically curated for community). **Long-term potential**: Very high.

### 2. immich-app/immich — Score 90/100
https://github.com/immich-app/immich
- **What it is**: Self-hosted, high-performance Google Photos alternative — photo/video backup, ML-based search, mobile apps.
- **Stack**: TypeScript, NestJS (backend), SvelteKit (frontend), Postgres, **Redis** (job queues), Docker. **Stars**: 113,071 | **Open issues**: 701 | **Contributors**: 989 (verified) | **Language**: TypeScript
- **Activity**: Issues updated continuously, same-day triage.
- **Match**: Exceptional — NestJS/Node + Postgres + Redis + Docker is exactly your stack.
- **Contribution areas**: Backend API (NestJS), mobile sync (Flutter, less relevant to you), ML pipeline integration, job-queue/Redis work.
- **Sample open issues**: #30813 Sync failure after SQLite reset (L2) · #31147 Mobile filename bug with `#` char (L1) · #17570 Delete-without-confirmation bug (L1/L2) · #31124 DB backup job leaks password in plaintext to subprocess (L2, security-adjacent) · #30756 iOS backup PathNotFoundException (L2)
- **First-PR suitability**: High. **Long-term potential**: Very high — massive, well-run self-hosted project.

### 3. twentyhq/twenty — Score 89/100
https://github.com/twentyhq/twenty
- **What it is**: Open-source CRM, positioned as the "AI-native Salesforce alternative."
- **Stack**: TypeScript, React, **NestJS**, **PostgreSQL**, GraphQL. **Stars**: 55,945 | **Open issues**: 172 (well-triaged, low backlog relative to size) | **Contributors**: 720 (verified) | **Language**: TypeScript
- **Activity**: Issues triaged same-day with explicit priority labels (`prio: high/medium`).
- **Match**: Exceptional — this is literally your stack (React + NestJS + Postgres).
- **Contribution areas**: Workflow engine, kanban/board views, CalDAV sync, accessibility (WCAG), CRM object model.
- **Sample open issues**: #25112 TypeError on duplicate Tasks view (L1) · #25082 CalDAV sync href bug (L2) · #23132 WCAG 4.1.2 nested interactive controls (L1, accessibility) · #25099 Hard-coded per-app throttle breaks large app deploys (L2/L3) · #24976 AI instructions editor crash (L1)
- **First-PR suitability**: Very high — clean codebase, active `prio:` triage. **Long-term potential**: Very high.

### 4. n8n-io/n8n — Score 88/100
https://github.com/n8n-io/n8n
- **What it is**: Fair-code workflow automation platform (Zapier/Make alternative), 400+ integrations, heavy AI-agent adoption.
- **Stack**: TypeScript, Node.js, Vue. **Stars**: 202,950 | **Open issues**: 1,121 | **Contributors**: 777 (verified) | **Language**: TypeScript
- **Activity**: Issues triaged continuously (Linear-synced, `status:in-linear` label shows real internal tracking).
- **Match**: Excellent for Node/TypeScript + automation/integration work; less direct DB/infra but huge for API integration skills.
- **Contribution areas**: New integration nodes, expression engine, AI node development (MCP support present), core workflow execution.
- **Sample open issues**: #37420 Class instance loses `toString` override in workflow data (L2) · #37358 Prototype pollution via field names (L2/L3) · #37307 AI node-generation description length bug (L1) · #37377 MCP execute_workflow schema mismatch (L2) · #37434 Jira node "Get Many Issues" bug (L1)
- **First-PR suitability**: High (huge, well-documented contributor guide). **Long-term potential**: Very high.

### 5. mem0ai/mem0 — Score 85/100
https://github.com/mem0ai/mem0
- **What it is**: Universal memory layer for AI agents — persistent long-term memory across LLM sessions, widely embedded in agent stacks.
- **Stack**: Python, with TypeScript SDK. **Stars**: 64,430 | **Open issues**: 707 | **Contributors**: 399 (verified) | **Language**: Python
- **Match**: Direct hit for your RAG/LangChain/agent-memory interest.
- **Contribution areas**: Vector-store integrations (Elasticsearch, Neptune), SDK bugs (Python + TypeScript), REST API, entity extraction/i18n.
- **Sample open issues**: #7157 Elasticsearch custom metadata filters silently match nothing (L2) · #7068 Neptune Analytics inverted similarity ranking (L2/L3, real correctness bug) · #7165 Add iFLYTEK Spark LLM provider (L1) · #7159 Add Rostam vector store provider (L1) · #4884 BM25/entity extraction hardcoded to English (L2/L3)
- **First-PR suitability**: High — many "add provider" L1 issues. **Long-term potential**: High, fast-growing.

### 6. topoteretes/cognee — Score 83/100
https://github.com/topoteretes/cognee
- **What it is**: Open-source AI memory platform — self-hosted knowledge-graph + RAG memory engine for agents.
- **Stack**: Python. **Stars**: 30,369 | **Open issues**: 484 | **Contributors**: 280 (verified) | **Language**: Python
- **Match**: Excellent RAG/knowledge-graph match; repo explicitly tags `good-first-issue`/`help-wanted`/`contributions-welcome`.
- **Contribution areas**: Data-source connectors (running a "hackathon" series specifically for these — YouTube, Telegram, Obsidian, MediaWiki, Todoist connectors all open), SQL parsing, ACL bugs.
- **Sample open issues**: #4808 Add YouTube connector (L1, `good first issue`) · #4730 Add Telegram connector (L1) · #4839 SQL parser drops WHERE clause on JOINs — silent full-table ingestion (L2/L3, serious correctness bug) · #4673 Cloud tenant endpoints hang forever (L2/L3) · #4829 Dataset ownership check false negative (L2)
- **First-PR suitability**: Very high — actively curating beginner-friendly connector issues. **Long-term potential**: High.

### 7. langfuse/langfuse — Score 87/100
https://github.com/langfuse/langfuse
- **What it is**: Open-source LLM engineering platform — tracing, evals, prompt management, playground. YC-backed, integrates with LangChain/OpenTelemetry.
- **Stack**: TypeScript (Next.js), Postgres, ClickHouse. **Stars**: 33,973 | **Open issues**: 861 | **Contributors**: 203 (verified) | **Language**: TypeScript
- **Activity**: Extremely active — issues updated within minutes of each other.
- **Match**: Excellent — TypeScript full-stack + LLM observability is squarely in your target zone.
- **Contribution areas**: SDK bugs (Python/TS), OTel integration, evals UI, cost-tracking for new providers.
- **Sample open issues**: #16841 OpenAI adapter mis-attributes Microsoft.Extensions.AI spans (L2) · #16508 Reasoning-token cost calculation (L2) · #16835 Dataset runs invisible in UI after API creation (L2) · #12907 Trust scores for trace provenance (L2/L3, design-level) · #16654 Bedrock structured-output evaluator bug (L2)
- **First-PR suitability**: High, well-documented monorepo. **Long-term potential**: High — fast-growing category.

### 8. formbricks/formbricks — Score 82/100
https://github.com/formbricks/formbricks
- **What it is**: Open-source Qualtrics/Typeform alternative — surveys, in-product experience management.
- **Stack**: TypeScript, Next.js. **Stars**: 12,848 | **Open issues**: 234 | **Contributors**: 321 (verified) | **Language**: TypeScript
- **Contribution areas**: Webhook fan-out architecture, i18n, survey logic engine, security (CORS credentials issue is currently open).
- **Sample open issues**: #9081 `Access-Control-Allow-Credentials: true` alongside wildcard origin (L2, security) · #8825 Webhook fan-out architecture feature (L3) · #8722 Partial-batch AI example generation bug (L2) · #8685 `DEFAULT_ORGANIZATION_ID` broken after v5 (L2) · #7774 Unify date picker component (L1)
- **First-PR suitability**: High. **Long-term potential**: Good, has `agent-ready` labeling showing active DX investment.

### 9. novuhq/novu — Score 80/100
https://github.com/novuhq/novu
- **What it is**: Open-source notification infrastructure (email/SMS/push/in-app) for products and, increasingly, AI agents.
- **Stack**: TypeScript, Node.js. **Stars**: 39,699 | **Open issues**: 107 (small, well-managed backlog) | **Contributors**: 527 (verified) | **Language**: TypeScript
- **Contribution areas**: Workflow engine, provider integrations (SMS/push), dashboard UX.
- **Sample open issues**: #12498 HTTP step response empty in downstream steps, self-hosted (L2) · #12305 MaxListenersExceededWarning regression since 3.17.0 (L2) · #11114 Preferences-by-context not applied (L2) · #12267 Autofill disabled on self-hosted auth forms (L1) · #6285 Content-available option for push step (L1/L2)
- **First-PR suitability**: High. **Long-term potential**: Good — core dependency for many other OSS apps (used by Novu-integrated products).

### 10. docmost/docmost — Score 79/100
https://github.com/docmost/docmost
- **What it is**: Open-source Confluence/Notion alternative — collaborative wiki & docs.
- **Stack**: TypeScript, **NestJS**, React, Postgres. **Stars**: 21,523 | **Open issues**: 322 | **Contributors**: 52 (verified — smaller core team, real opportunity for outsized impact) | **Language**: TypeScript
- **Contribution areas**: Search (typo-tolerant/infix matching requested), webhooks, real-time collaboration (Yjs), auth (OAuth/Graph).
- **Sample open issues**: #2452 Improve search: typo tolerance / infix matching (L2) · #2455 HMAC-signed outgoing webhooks (L2) · #2437 Password reset for existing user (L1) · #2258 Microsoft Graph/OAuth2 integration (L2/L3) · #2436 Search result doesn't scroll to match (L1)
- **First-PR suitability**: High — small enough team that PRs get real attention fast. **Long-term potential**: High, fast-growing (21.5k stars from a 2023 repo).

### 11. medplum/medplum — Score 84/100
https://github.com/medplum/medplum
- **What it is**: Open-source healthcare developer platform — FHIR-native EHR/backend-as-a-service used by real healthcare startups (SOC2 compliant).
- **Stack**: TypeScript, React, GraphQL, FHIR. **Stars**: 2,640 (small but extremely real usage — healthcare companies build on this in production) | **Open issues**: 621 | **Contributors**: 194 (verified) | **Language**: TypeScript
- **Contribution areas**: FHIR search parameters, patient intake forms, scheduling, white-labeling.
- **Sample open issues**: #8827 New-patient intake form creates patient even on validation error (L2) · #10222 `:missing` modifier broken for `_id` search param (L2/L3) · #10110 Overbooking support for scheduling (L2) · #10377 C-CDA import ignores negation indicator (L3, healthcare-domain-specific) · #9921 Navbar active-state persistence (L1)
- **First-PR suitability**: Medium-high (healthcare domain adds learning curve, but `open-to-community` label exists). **Long-term potential**: Very high — real clinical impact, growing fast.

### 12. ghostfolio/ghostfolio — Score 81/100
https://github.com/ghostfolio/ghostfolio
- **What it is**: Open-source wealth-management / portfolio-tracking app.
- **Stack**: **Angular**, **NestJS**, **Prisma**, TypeScript. **Stars**: 9,218 | **Open issues**: 297 | **Contributors**: 308 (verified) | **Language**: TypeScript
- **Contribution areas**: Explicitly labels `help wanted` issues; allocation charts, activity import/duplicate-detection, self-hosted ARM support.
- **Sample open issues**: #7769 "By Holding" chart mislabels asset names (L1, `help wanted`) · #7393 Enable Angular strictTemplates (L2, `help wanted`) · #6221 Group-by-year in portfolio performance endpoint (L2, `help wanted`, NestJS) · #7728 Duplicate detection not scoped to account (L2) · #7716 OIDC callback silent failure (L2/L3)
- **First-PR suitability**: High — maintainer explicitly tags issues for outside contributors. **Long-term potential**: Good, steady fintech niche.

### 13. hyperdxio/hyperdx — Score 80/100
https://github.com/hyperdxio/hyperdx
- **What it is**: Open-source observability platform (session replay, logs, metrics, traces) built on ClickHouse + OpenTelemetry.
- **Stack**: TypeScript, React, ClickHouse. **Stars**: 9,871 | **Open issues**: 190 | **Contributors**: 85 (verified — small core, good impact ratio) | **Language**: TypeScript
- **Contribution areas**: Search query parser (boolean logic bugs currently open), ClickHouse query performance, CLI SSO auth.
- **Sample open issues**: #3032 Search mixing AND/OR without parens returns wrong rows (L2/L3, query-parser bug) · #3037 Unbounded SQL autocomplete scan without date filter (L2) · #3034 p95 query scan times out (L2/L3, ClickHouse perf) · #3006 CLI lacks Google SSO support (L2) · #3004 Trace-level AND search across spans (L3, feature)
- **First-PR suitability**: Medium (ClickHouse/query-engine work is meatier). **Long-term potential**: Good — fast-growing observability category.

### 14. SigNoz/signoz — Score 82/100
https://github.com/SigNoz/signoz
- **What it is**: Open-source OpenTelemetry-native APM/observability platform (Datadog/New Relic alternative).
- **Stack**: TypeScript (React), Go. **Stars**: 31,981 | **Open issues**: 1,549 (large, actively triaged backlog) | **Contributors**: 218 (verified) | **Language**: TypeScript
- **Contribution areas**: Explicit `good first issue` label in active use; query builder, dashboards, alerting/Slack integration.
- **Sample open issues**: #9120 Metrics Explorer summary page breaks with sidebar open (L1, `good first issue`) · #12701 TTL/retention silently deletes logs on one code path (L2/L3, data-loss bug) · #9079 Deprecate `/v3,v4/query_range`, migrate to `/prometheus` prefix (L2) · #8931 Migrate quick filters to `/fields/keys` and `/fields/values` (L2) · #12461 Slack alert messages should thread (L1)
- **First-PR suitability**: High. **Long-term potential**: Very high — large, funded, growing fast.

### 15. triggerdotdev/trigger.dev — Score 78/100
https://github.com/triggerdotdev/trigger.dev
- **What it is**: Open-source background jobs / durable workflow platform for AI agents and apps.
- **Stack**: TypeScript, Next.js, Redis (queues), Postgres. **Stars**: 16,170 | **Open issues**: 344 | **Contributors**: 143 (verified) | **Language**: TypeScript
- **Contribution areas**: CLI/telemetry, Kubernetes worker networking, idempotency semantics, docs accuracy.
- **Sample open issues**: #4627 Idempotency keys don't protect ad-hoc calls inside `run()` despite docs claiming so (L2/L3) · #4733 `get_run_details` cursor never progresses since a specific PR (L2, regression) · #4214 K8s worker telemetry missing hostname (L2) · #4801 CLI accepts out-of-range esbuild version, corrupts sourcemaps (L2) · #4425 Docs contradiction on `dev --env-file` scope (L1)
- **First-PR suitability**: Medium-high. **Long-term potential**: Good — core infra for many downstream AI-agent products.

### 16. activepieces/activepieces — Score 79/100
https://github.com/activepieces/activepieces
- **What it is**: Open-source workflow automation + MCP-server hub (~400 MCP servers), n8n/Zapier alternative geared toward AI agents.
- **Stack**: TypeScript. **Stars**: 24,145 | **Open issues**: 501 | **Contributors**: 492 (verified) | **Language**: TypeScript
- **Contribution areas**: New "pieces" (integrations), job-queue reliability (BullMQ-related), MCP-tool option resolution latency.
- **Sample open issues**: #15130 OOM-killed worker job re-delivered forever, bypasses max-attempts (L2/L3, queue-reliability bug) · #15132 `POST /v1/pieces/options` 10-17s latency blocks worker jobs (L2/L3, perf) · #15149 Fillout Forms webhook silently dropped (double-JSON-parse bug) (L1/L2) · #14515 Client-credentials auth for remaining MS pieces (L2) · #15133 Sync webhook should respond immediately (L2)
- **First-PR suitability**: High — huge "piece" ecosystem is very approachable for first PRs. **Long-term potential**: Good, directly in AI-agent tooling growth curve.

### 17. actualbudget/actual — Score 78/100
https://github.com/actualbudget/actual
- **What it is**: Local-first, open-source personal-finance/budgeting app (YNAB alternative).
- **Stack**: TypeScript. **Stars**: 28,489 | **Open issues**: 230 | **Contributors**: 707 (verified — very healthy contributor:star ratio) | **Language**: TypeScript
- **Contribution areas**: Bank-sync importers (GoCardless, YNAB4), mobile-responsive UI, sync-engine edge cases.
- **Sample open issues**: #3561 YNAB4 import produces malformed split transactions (L2, `help wanted`) · #8830 GoCardless duplicate transactions from a specific bank (L2) · #8816 `_fullSync` requires 10+ retries (L2/L3, sync-engine) · #8822 Linked-transfer date doesn't update on parent split edit (L2) · #8819 Cannot change group on mobile (L1)
- **First-PR suitability**: High. **Long-term potential**: Good, mature stable niche with real daily users.

### 18. refinedev/refine — Score 76/100
https://github.com/refinedev/refine
- **What it is**: React meta-framework for building admin panels/internal tools/B2B apps (headless, backend-agnostic).
- **Stack**: TypeScript, React, Next.js. **Stars**: 35,603 | **Open issues**: 105 (small, well-kept) | **Contributors**: 328 (verified) | **Language**: TypeScript
- **Contribution areas**: Security (an XSS/arbitrary-code-execution issue currently open — great advanced pick), adapter packages (antd/mantine), build tooling migration.
- **Sample open issues**: #7556 Arbitrary code execution in `@refinedev/inferencer` via unescaped field names reaching `react-live` (L3, security) · #7477 Notification type not respected across UI adapters (L2) · #6969 Migrate build to tsdown (L2/L3, infra) · #7527 Make `MetaQuery` an interface for declaration merging (L2) · #7551 Docs bug on `NumberField` Intl usage (L1)
- **First-PR suitability**: High, `good-first-issue` topic actively used. **Long-term potential**: Good, well-governed monorepo.

### 19. excalidraw/excalidraw — Score 83/100
https://github.com/excalidraw/excalidraw
- **What it is**: Real-time collaborative whiteboard for hand-drawn-style diagrams — embedded in dozens of other products.
- **Stack**: TypeScript, React, Canvas, WebSockets/CRDT for collaboration. **Stars**: 130,859 | **Open issues**: 3,426 (very large, active backlog) | **Contributors**: 372 (verified) | **Language**: TypeScript
- **Contribution areas**: Real-time collaboration engine, accessibility, mobile input handling, security (an open-redirect via collaboration iframe is currently open).
- **Sample open issues**: #11930 iframe element renders without validation → open-redirect via collaboration (L2/L3, security) · #9276 Ctrl+F doesn't work in help menu (L1, `good first issue`) · #7177 Grouping line invisible on dark bg (L1, `good first issue`) · #11963 `setLanguage()` mutates host document, not scoped to widget (L2) · #9637 Object links don't open on mobile tap (L2)
- **First-PR suitability**: Very high — actively curated `good first issue` label. **Long-term potential**: Excellent — foundational real-time-canvas library used everywhere.

### 20. hoppscotch/hoppscotch — Score 79/100
https://github.com/hoppscotch/hoppscotch
- **What it is**: Open-source API development ecosystem (Postman/Insomnia alternative) — web, desktop, CLI.
- **Stack**: TypeScript, Vue. **Stars**: 80,126 | **Open issues**: 804 | **Contributors**: 353 (verified) | **Language**: TypeScript
- **Contribution areas**: MCP client support (open feature request — direct match to your interest), REST/GraphQL client bugs, desktop-app auth flow.
- **Sample open issues**: #5966 Add MCP client support (L2/L3, directly matches your AI-agent skills) · #6624 Self-hosted desktop login stuck on spinner — device-token handoff bug (L2/L3) · #6612 Large integers lose precision generating cURL — Snowflake ID corruption (L2) · #6607 Allow default endpoint per collection environment (L1/L2) · #6484 Large messages freeze UI (L2, perf)
- **First-PR suitability**: High. **Long-term potential**: Good — huge user base, steady maintenance cadence.

---

## TIER 2 — 25 Strong Contribution Opportunities
*(Verified: stars, issues, language, contributors, live sample issues)*

| # | Repo | What it is | Stack | ★ | Issues | Contributors | Sample issues (live) | Score |
|---|------|-----------|-------|---|--------|--------------|----------------------|-------|
| 21 | [langchain-ai/langchain](https://github.com/langchain-ai/langchain) | The agent engineering framework | Python | 145,348 | 431 | 3,731 | #40002 PIIMiddleware misses IP/MAC near non-ASCII (L2) · #40057 Markdown parser misses `+` bullets (L1) · #39953 ShellToolMiddleware timeout doesn't restart session (L2/L3) | 82 |
| 22 | [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) | Durable agent orchestration graphs | Python | 40,785 | 730 | 285 | #8764 Crash before first checkpoint silently drops run (L3) · #8748 Checkpoint durability race condition (L3) · #8753 Cache namespace collision across graphs (L2) | 83 |
| 23 | [run-llama/llama_index](https://github.com/run-llama/llama_index) | Document agent / RAG framework | Python | 51,940 | 674 | 1,991 | #22888 `Dispatcher.__init__` mutable default args (L1) · #22743 choice-select parser off-by-one (L2) · #22899 Add Webz.io news-search tool (L1) | 79 |
| 24 | [langgenius/dify](https://github.com/langgenius/dify) | Agentic workflow + RAG pipeline platform | TypeScript+Python | 153,997 | 1,004 | 1,455 | #41542 Langfuse `events_only` mode silently drops Dify traces (L2/L3) · #39947 `good first issue`: unnecessary type conversion cleanup (L1) · #37403 `db.session` param passing refactor (L1/L2) | 80 |
| 25 | [langflow-ai/langflow](https://github.com/langflow-ai/langflow) | Visual agent/workflow builder | Python | 153,971 | 1,005 | 378 | #14865 Trace name uses UUID not display name (L1) · #14860 OpenAI-compatible embed model false "API key required" error (L2) · #14847 AG-UI stream leaks full flow topology, no opt-out (L2/L3, privacy) | 78 |
| 26 | [mattermost/mattermost](https://github.com/mattermost/mattermost) | Secure team collaboration/chat platform | TypeScript+Go | 38,946 | 1,003 | 1,213 | #909 `good first issue`: settings confirmation UX (L1) · #42002 Livechat async filter no-op bug (L2) · #41997 `sendInvitationEmail` always returns false (L2) | 81 |
| 27 | [RocketChat/Rocket.Chat](https://github.com/RocketChat/Rocket.Chat) | Secure comms platform (Slack alternative) | TypeScript | 46,052 | 4,014 | 1,102 | #38198 No element limit/dedup on multiselect CPA values (L2) · #38146 Board picker loads only first 10 users, no pagination (L2) · #36069 DMs fail to load due to missing-role check (L2) | 76 |
| 28 | [chatwoot/chatwoot](https://github.com/chatwoot/chatwoot) | Customer support / omnichannel desk | Ruby (backend) + Vue/JS (frontend) | 36,336 | 1,353 | 385 | #15618 Add Prometheus `/metrics` endpoint for self-hosted (L2) · #15624 Audio transcription via account-level OpenAI BYOK (L2/L3) · #15625 Persist/reuse processed attachment text across integrations (L2) — *note: backend is Ruby, frontend contributions (Vue/JS) are the best stack match* | 72 |
| 29 | [makeplane/plane](https://github.com/makeplane/plane) | Open-source Jira/Linear alternative | TypeScript + Python(Django) | 58,626 | 1,066 | 162 | #9721 Cloudflare blocks API/MCP writes (403) (L2) · #1809 Modal shouldn't close on outside-click while creating issue (L1) · #1495 Gitea integration (L2) | 78 |
| 30 | [hcengineering/platform (Huly)](https://github.com/hcengineering/platform) | All-in-one PM/CRM/chat/wiki platform | TypeScript | 27,508 | 849 | 127 | #11026 Multi-workspace accounts never get metadata cookie → 401 on previews (L2/L3) | #11024 Base Docker image ships CVE-2025-48384-vulnerable git (L1/L2, security patch) · #10933 Published npm packages missing `.d.ts` despite declaring `types` (L1/L2) | 74 |
| 31 | [outline/outline](https://github.com/outline/outline) | Real-time collaborative knowledge base/wiki | TypeScript | 40,391 | 84 (small, well-kept) | 259 | #13585 Deleting large doc subtree issues one update per descendant (L2/L3, perf) | #13586 Android PWA dark-theme white bars (L1) · #13579 MCP `documents.update` truncates blockquote+table (L2) | 79 |
| 32 | [strapi/strapi](https://github.com/strapi/strapi) | Leading open-source headless CMS | TypeScript | 73,048 | 554 | 1,381 | #27469 `Strapi.destroy()` doesn't stop cron, throws on shutdown (L2) · #25299 Auth callback race condition, uniqueness not enforced at DB level (L2/L3) · #22164 JSON fields in lifecycles changed type in v5 (breaking) (L2) | 77 |
| 33 | [payloadcms/payload](https://github.com/payloadcms/payload) | Full-stack Next.js headless CMS/app framework | TypeScript | 44,508 | 1,101 | 574 | #18056 Globals `/versions` 500s — missing guard in Drizzle adapter (L2/L3) · #18063 MCP plugin: localized array update breaks locale row IDs (L2) · #18055 Job errors drop original stack trace (L2) | 78 |
| 34 | [directus/directus](https://github.com/directus/directus) | Headless CMS / instant API over any DB | TypeScript | 37,661 | 389 | 577 | #28161 Bulk update/delete on `directus_comments` bypasses auth check (L2/L3, security) · #27476 Dynamic field-condition values don't trigger UI (L2) · #28165 Tooltips don't appear on keyboard focus (L1, accessibility) | 78 |
| 35 | [nocodb/nocodb](https://github.com/nocodb/nocodb) | Airtable-alternative no-code DB platform | TypeScript | 64,793 | 710 | 352 | #14471 `convertDateTime` hardcodes Berlin-like offset, corrupts raw storage (L2/L3, data-integrity bug) · #14467 Knex connection-pool timeout (L2) · #14463 Support TiDB backend (L3) | 75 |
| 36 | [baserow/baserow](https://github.com/baserow/baserow) | Open-source Airtable alternative, AI-assisted | Python | 5,753 | 1,222 | 80 (small core — high impact ratio) | #5741 Duration field required-validation fails (L1) · #5971 Missing permission check on data-sync endpoint (L2, security) · #4457 Single-select option dependencies (L2) | 74 |
| 37 | [medusajs/medusa](https://github.com/medusajs/medusa) | Composable e-commerce platform | TypeScript | 36,078 | 197 | 550 | #16377 `addStoreCreditsToCartWorkflow` applies full balance, ignores amount (L2, `good first issue`) · #16392 Product-tag loader forwards stray URL param (L1, `good first issue`) · #16396 Buy-get promo ignored depending on line-item order (L2/L3) | 78 |
| 38 | [appsmithorg/appsmith](https://github.com/appsmithorg/appsmith) | Internal-tools/admin-panel builder | TypeScript+Java | 40,788 | 4,470 (very large, active backlog) | 380 | #17330 macOS setup fails: postgresql@13 disabled in Homebrew (L1, docs+DX, `good first issue`) · #17679 Cloning app w/ custom datasource 422s (L2) · #17717 26 findings: sensitive field exposure (L2/L3, security) | 74 |
| 39 | [ToolJet/ToolJet](https://github.com/ToolJet/ToolJet) | Low-code internal-tools builder | JavaScript/TS | 40,803 | 1,174 | 681 | #18356 Duplicating workspace can bring in stale users table (L2/L3) · #19580 Docker image ships 19.8MB unnecessary apt indexes (L1, DX) · #19573 Seed-from-dev fails on single-user column (L2) | 73 |
| 40 | [Budibase/budibase](https://github.com/Budibase/budibase) | Low-code internal-tools/apps platform | TypeScript | 28,250 | 273 | 145 | #34162 DB errors post-upgrade migration (L2/L3) · #33920 dbt integration treats all non-success as failure (L2) · #11841 Generate ARM64 Docker images (L2, DX) | 73 |
| 41 | [dagster-io/dagster](https://github.com/dagster-io/dagster) | Data-orchestration platform | Python | 16,076 | 2,579 (large, active) | 695 | #10887 MCP: expose incoming HTTP headers to scripts (L2/L3) · #10861 Schedule silently changes if job overruns interval (L2/L3) · #10872 Jupyter notebook support request (L2) | 75 |
| 42 | [windmill-labs/windmill](https://github.com/windmill-labs/windmill) | Dev platform: scripts → webhooks/workflows/UIs | Rust+TS+Python | 17,739 | 838 | 170 | #6736 Add MariaDB backend support (L2/L3) · #6731 Topology re-import creates duplicate incidents (L2) · #4767 Cannot set every field in dedup config (L2) | 74 |
| 43 | [keephq/keep](https://github.com/keephq/keep) | Open-source AIOps / alert-management platform | Python | 12,264 | 579 | 198 | #6715 OpenAI/DeepSeek providers crash on empty choices list (L2) · #6736 MariaDB backend (L2/L3) — *(overlap note: some issues shared list position, verified separately)* · #5404 FluxCD missing from provider-topology docs (L1) | 73 |
| 44 | [BerriAI/litellm](https://github.com/BerriAI/litellm) | LLM gateway — unify 100+ LLM APIs, cost tracking | Python (Rust core) | 57,672 | 4,915 (very large, active) | 1,653 | #38963 Gemini transcribe model mislabels `.webm` as video (L2) · #38957 Cached async HTTP client closes pooled client mid-SSE-stream, kills batched streams hourly (L2/L3, concurrency bug) · #38953 Streaming guardrail block sends malformed SSE (L2) | 79 |
| 45 | [danny-avila/LibreChat](https://github.com/danny-avila/LibreChat) | Self-hosted multi-provider AI chat UI | TypeScript | 42,654 | 734 | 397 | #15024 Unexpected OpenAI fallback despite working Azure config (L2) · #15398 File-filter checkbox state desyncs visually (L1) · #14249 Agents via Responses API can't use configured subagents (L2/L3) | 76 |

---

## TIER 3 — 23 Medium/Advanced Contribution Opportunities
*(Verified: stars, issues, language, contributors where noted; sample issues where fetched)*

| # | Repo | What it is | Stack | ★ | Issues | Contributors | Notes | Score |
|---|------|-----------|-------|---|--------|--------------|-------|-------|
| 46 | [milvus-io/milvus](https://github.com/milvus-io/milvus) | Cloud-native vector database, distributed | Go | 45,903 | 1,298 | 372 (verified) | Distributed-systems heavy; Go not core to your stack but huge ANN/vector-search learning | 68 |
| 47 | [qdrant/qdrant](https://github.com/qdrant/qdrant) | Vector database & search engine | Rust | 34,293 | 702 | 191 (verified) | Rust learning curve; strong RAG-infra relevance | 65 |
| 48 | [weaviate/weaviate](https://github.com/weaviate/weaviate) | Vector database w/ hybrid search | Go | 16,768 | 690 | 186 (verified) | Similar profile to Milvus | 65 |
| 49 | [meilisearch/meilisearch](https://github.com/meilisearch/meilisearch) | Hybrid full-text/vector search engine | Rust | 59,147 | 322 | 256 (verified) | Excellent search/relevance-engineering exposure | 68 |
| 50 | [temporalio/temporal](https://github.com/temporalio/temporal) | Durable-execution / distributed workflow engine | Go | 22,679 | 935 | 302 (verified) | Best-in-class for learning distributed-systems durable execution patterns | 72 |
| 51 | [conductor-oss/conductor](https://github.com/conductor-oss/conductor) | Event-driven agentic workflow engine | Java | 32,150 | 258 | 416 (verified) | Netflix-origin orchestration engine, now community-run | 66 |
| 52 | [Kong/kong](https://github.com/Kong/kong) | API + AI Gateway | Lua/Go plugins | 44,063 | 193 | 452 (verified) | Plugin ecosystem (Go/Lua) is the realistic entry point | 67 |
| 53 | [apache/apisix](https://github.com/apache/apisix) | Cloud-native API/AI Gateway | Lua | 17,065 | 242 | 518 (verified) | Apache-governed, strong mentoring culture | 65 |
| 54 | [TykTechnologies/tyk](https://github.com/TykTechnologies/tyk) | Open-source API Gateway (REST/GraphQL/gRPC) | Go | 10,810 | 499 | 137 (verified) | Good Go-backend, real enterprise usage | 66 |
| 55 | [openobserve/openobserve](https://github.com/openobserve/openobserve) | Unified observability (logs/metrics/traces) | Rust core, TS frontend | 21,586 | 578 | 141 (verified) | Frontend (TS) is the accessible entry point | 70 |
| 56 | [louislam/uptime-kuma](https://github.com/louislam/uptime-kuma) | Self-hosted uptime monitoring | JavaScript | 90,793 | 791 | 1,125 (verified) | Massive community, historically very beginner-friendly | 73 |
| 57 | [TwiN/gatus](https://github.com/TwiN/gatus) | Automated status-page / alerting | Go | 11,941 | 379 | 172 (verified) | Small, approachable Go codebase | 68 |
| 58 | [nats-io/nats-server](https://github.com/nats-io/nats-server) | High-performance cloud/edge messaging system | Go | 20,640 | 547 | 236 (verified) | Core message-queue infra, CNCF-adjacent | 68 |
| 59 | [svix/svix-webhooks](https://github.com/svix/svix-webhooks) | Enterprise webhooks-as-a-service | Rust | 3,377 | 68 | 85 (verified) | Small, high quality; webhook-delivery semantics are a great distributed-systems topic | 66 |
| 60 | [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | Multi-agent orchestration framework | Python | 57,877 | 769 | 304 (verified) | Direct AI-agent stack match | 76 |
| 61 | [infiniflow/ragflow](https://github.com/infiniflow/ragflow) | RAG engine fusing retrieval + agent capability | Go/Python | 89,744 | 1,721 | Not verified (fork proxy: 10,983) | #19064 Tenant-model UUID collision across datasets (L2/L3) · #18754 Missing column breaks all tenant queries post-upgrade (L2/L3) | 75 |
| 62 | [open-webui/open-webui](https://github.com/open-webui/open-webui) | Self-hosted LLM chat/agent web UI | Python | 150,487 | 201 | Not verified (fork proxy: 21,968) | #29280 Alembic migration circular-import breaks schema silently (L2/L3) · #29293 Stuck "Executing…" state on repeated tool calls (L2) | 76 |
| 63 | [Mintplex-Labs/anything-llm](https://github.com/Mintplex-Labs/anything-llm) | Full-stack RAG/agent app, local-first | JavaScript | 65,423 | 331 | Not verified (fork proxy: 7,224) | #6228 `fillSourceWindow` mutates caller's array in place (L1/L2) · #6229 Embed-override permissions drop workspace defaults (L2) | 74 |
| 64 | [OpenHands/OpenHands](https://github.com/OpenHands/OpenHands) | AI software-engineering agent platform | Python+TypeScript | 85,741 | 609 | Not verified (fork proxy: 11,232) | #17047 Model missing from Agent Canvas LLM list (L1) · #16774 Mac installer produces damaged binary (L2/L3) | 77 |
| 65 | [voideditor/void](https://github.com/voideditor/void) | Open-source Cursor alternative (AI code editor) | TypeScript | 28,819 | 307 | Not verified (fork proxy: 2,648) | #226 Build AppImage for Linux (L2) · #752 Local LLM can't access filesystem via MCP (L2/L3) | 71 |
| 66 | [letta-ai/letta](https://github.com/letta-ai/letta) | Stateful agents platform w/ persistent memory | Python | 24,508 | 39 (small, high signal:noise) | Not verified (fork proxy: 2,601) | #3390 Missing ClientTimeout causes coroutine starvation (L2/L3) · #3270 Sliding-window compaction ignores percentage param (L2) | 72 |
| 67 | [frappe/crm](https://github.com/frappe/crm) | Fully-featured open-source CRM | Vue + Python | 3,438 | 299 | Not verified (fork proxy: 1,402) | #2723 Bulk-edit reports success even on failure (L2) · #2692 Link fields with filters return empty dropdowns (L2) | 68 |
| 68 | [frappe/helpdesk](https://github.com/frappe/helpdesk) | Open-source customer-service desk | Vue + Python | 3,345 | 189 | Not verified (fork proxy: 924) | #3614 No conditional field visibility in ticket templates (L2) · #3717 "Prefer knowledgebase" setting broken (L1/L2) | 67 |

---

## TIER 4 — 13 Long-Term / High-Impact Targets
*(Massive scale, harder onboarding, exceptional learning ceiling and real-world impact)*

| # | Repo | What it is | Stack | ★ | Issues | Contributors | Score |
|---|------|-----------|-------|---|--------|--------------|-------|
| 69 | [TriliumNext/Trilium](https://github.com/TriliumNext/Trilium) | Personal knowledge-base / notes app | TypeScript | 37,646 | 695 | Not verified (fork proxy: 2,529) | 70 |
| 70 | [glanceapp/glance](https://github.com/glanceapp/glance) | Self-hosted homelab dashboard | Go | 36,753 | 312 | Not verified (fork proxy: 1,441) | 65 |
| 71 | [usememos/memos](https://github.com/usememos/memos) | Self-hosted quick-capture notes | Go (+ React frontend) | 62,676 | 43 | Not verified (fork proxy: 4,703) | 64 |
| 72 | [redis/redis](https://github.com/redis/redis) | In-memory data structure store, cache, vector engine | C | 76,159 | 2,926 | Not verified (fork proxy: 24,768) | 62 (C core is a language mismatch, but foundational infra you already use daily) |
| 73 | [puppeteer/puppeteer](https://github.com/puppeteer/puppeteer) | Headless-browser automation (Google) | TypeScript | 95,528 | 265 | Not verified (fork proxy: 9,573) | 70 |
| 74 | [netdata/netdata](https://github.com/netdata/netdata) | Real-time infra monitoring | C (+ web UI) | 80,374 | 393 | Not verified (fork proxy: 6,609) | 60 |
| 75 | [kestra-io/kestra](https://github.com/kestra-io/kestra) | Event-driven orchestration/scheduling platform | Java | 27,963 | 652 | Not verified (fork proxy: 2,971) | 66 |
| 76 | [PrefectHQ/prefect](https://github.com/PrefectHQ/prefect) | Python workflow orchestration | Python | 23,731 | 867 | Not verified (fork proxy: 2,497) | 71 |
| 77 | [mlflow/mlflow](https://github.com/mlflow/mlflow) | ML/LLM lifecycle & evaluation platform | Python | 27,749 | 2,054 | Not verified (fork proxy: 6,236) | 70 |
| 78 | [elastic/kibana](https://github.com/elastic/kibana) | Data visualization/observability for Elasticsearch | TypeScript | 21,276 | 14,330 (huge — mature triage process, not neglect) | Not verified (fork proxy: 8,622) | 62 (large company process overhead) |
| 79 | [frappe/erpnext](https://github.com/frappe/erpnext) | Full open-source ERP (accounting, mfg, HR, healthcare module) | Python | 38,718 | 1,812 | Not verified (fork proxy: 12,661) | 68 |
| 80 | [openmrs/openmrs-core](https://github.com/openmrs/openmrs-core) | Global open-source medical record system (used across 40+ countries) | Java | 1,904 | 279 | Not verified (fork proxy: 4,386) | 66 (huge humanitarian impact, steeper Java/legacy-code learning curve) |
| 81 | [openemr/openemr](https://github.com/openemr/openemr) | Most-used open-source EHR/practice-management system | PHP | 5,404 | 1,049 | Not verified (fork proxy: 3,018) | 62 (language mismatch, but critical real-world healthcare software) |

---

## TOP 25 RANKING

| Rank | Repository | Application | Stack | Stars | Contributors | Open Issues | Best Contribution Area | Difficulty | Score |
|------|-----------|-------------|-------|-------|--------------|-------------|------------------------|-----------|-------|
| 1 | supabase/supabase | Postgres dev platform | TypeScript | 108,643 | 2,023 | 1,085 | Auth, RLS, realtime | L1-L3 | 91 |
| 2 | immich-app/immich | Self-hosted Google Photos alt | TS/NestJS/Svelte | 113,071 | 989 | 701 | Backend API, job queues | L1-L2 | 90 |
| 3 | twentyhq/twenty | Open-source CRM | React/NestJS/Postgres | 55,945 | 720 | 172 | Workflow engine, a11y | L1-L2 | 89 |
| 4 | n8n-io/n8n | Workflow automation | TypeScript | 202,950 | 777 | 1,121 | Integration nodes, AI | L1-L3 | 88 |
| 5 | langfuse/langfuse | LLM observability | TypeScript | 33,973 | 203 | 861 | SDKs, OTel, evals | L1-L3 | 87 |
| 6 | medplum/medplum | Healthcare dev platform | TypeScript/FHIR | 2,640 | 194 | 621 | FHIR, scheduling | L2-L3 | 84 |
| 7 | topoteretes/cognee | AI memory/knowledge-graph | Python | 30,369 | 280 | 484 | Connectors, RAG | L1-L2 | 83 |
| 8 | excalidraw/excalidraw | Real-time collaborative canvas | TypeScript | 130,859 | 372 | 3,426 | Real-time engine, a11y | L1-L3 | 83 |
| 9 | SigNoz/signoz | OTel-native APM | TS/Go | 31,981 | 218 | 1,549 | Query builder, alerting | L1-L3 | 82 |
| 10 | mem0ai/mem0 | AI agent memory layer | Python | 64,430 | 399 | 707 | Vector-store integrations | L1-L3 | 85 |
| 11 | ghostfolio/ghostfolio | Wealth-management app | Angular/NestJS | 9,218 | 308 | 297 | Charts, import, NestJS API | L1-L2 | 81 |
| 12 | hyperdxio/hyperdx | Observability platform | TypeScript/ClickHouse | 9,871 | 85 | 190 | Query parser, perf | L2-L3 | 80 |
| 13 | novuhq/novu | Notification infrastructure | TypeScript | 39,699 | 527 | 107 | Workflow engine, providers | L1-L2 | 80 |
| 14 | docmost/docmost | Collaborative wiki | TS/NestJS/React | 21,523 | 52 | 322 | Search, real-time, OAuth | L1-L3 | 79 |
| 15 | hoppscotch/hoppscotch | API client (Postman alt) | Vue/TypeScript | 80,126 | 353 | 804 | MCP client, REST/GraphQL | L1-L3 | 79 |
| 16 | activepieces/activepieces | Workflow + MCP hub | TypeScript | 24,145 | 492 | 501 | Integrations, queue reliability | L1-L3 | 79 |
| 17 | actualbudget/actual | Local-first budgeting app | TypeScript | 28,489 | 707 | 230 | Bank-sync importers, sync engine | L1-L3 | 78 |
| 18 | triggerdotdev/trigger.dev | Background jobs/durable workflow | TypeScript/Redis | 16,170 | 143 | 344 | CLI, K8s workers, idempotency | L2-L3 | 78 |
| 19 | medusajs/medusa | Composable e-commerce | TypeScript | 36,078 | 550 | 197 | Cart/promo workflows | L1-L3 | 78 |
| 20 | payloadcms/payload | Headless CMS/app framework | TypeScript | 44,508 | 574 | 1,101 | Drizzle adapter, MCP plugin | L2-L3 | 78 |
| 21 | directus/directus | Headless CMS/instant API | TypeScript | 37,661 | 577 | 389 | Auth/security, a11y | L1-L3 | 78 |
| 22 | strapi/strapi | Leading headless CMS | TypeScript | 73,048 | 1,381 | 554 | Core lifecycle bugs | L2-L3 | 77 |
| 23 | OpenHands/OpenHands | AI software-engineering agent | Python/TypeScript | 85,741 | ~11,232 forks | 609 | Agent canvas, LLM integration | L1-L3 | 77 |
| 24 | refinedev/refine | React admin/internal-tools framework | TypeScript/React | 35,603 | 328 | 105 | Security fix, adapters | L1-L3 | 76 |
| 25 | crewAIInc/crewAI | Multi-agent orchestration | Python | 57,877 | 304 | 769 | Agent framework core | L1-L3 | 76 |

---

## CATEGORY WINNERS

- 🥇 **Best overall**: **supabase/supabase** — perfect stack match, massive real usage, exceptionally well-curated `external-issue` backlog specifically for community contributors, 2,023 verified contributors proving outside PRs land routinely.
- 🥈 **Best Full-Stack**: **twentyhq/twenty** — React + NestJS + PostgreSQL + GraphQL, clean `prio:` triage, real CRM used by real companies.
- 🥉 **Best Backend**: **immich-app/immich** — NestJS + Postgres + Redis + Docker, huge community, backend bugs are meaty and real (job queues, DB backup security bug currently open).
- 🤖 **Best AI**: **langfuse/langfuse** — TypeScript full-stack LLM observability, directly useful for your LangChain/agent work, extremely active triage.
- ⚡ **Best Real-Time**: **excalidraw/excalidraw** — canvas + live collaboration engine, actively curated first-issue backlog, used inside dozens of other products.
- 🗄️ **Best Database**: **nocodb/nocodb** — Airtable-alternative DB app, TypeScript, real data-integrity bugs (timezone corruption issue is a great L2/L3 pick).
- 🏗️ **Best Distributed Systems**: **temporalio/temporal** — best-in-class durable-execution patterns; steeper Go learning curve but unmatched systems-design learning.
- 🛠️ **Best Developer Application**: **hoppscotch/hoppscotch** — Postman alternative with an open MCP-client feature request that plays directly to your AI-agent skills.
- 🌱 **Best first contribution**: **topoteretes/cognee** — actively running a connector "hackathon" with explicit `good first issue` labels (YouTube/Telegram/Obsidian connectors), small enough to get fast maintainer feedback.
- 🚀 **Best long-term project**: **medplum/medplum** — real clinical-software impact, TypeScript/FHIR, growing fast, small enough (194 contributors) that sustained contribution builds real reputation and expertise.
