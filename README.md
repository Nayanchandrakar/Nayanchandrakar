# Hi, I'm Nayan chandrakar 👋

**Software Engineer building developer tools, AI systems, and production software around hard engineering problems.**

I like building systems where the interesting work is underneath the interface: agent orchestration, code intelligence, asynchronous workflows, distributed boundaries, data modeling, cloud infrastructure, and the failure modes that appear when software has to behave reliably.

<a href="https://nayan.ink"><picture><source media="(prefers-color-scheme: dark)" srcset="https://shieldcn.dev/badge/Website-nayan.ink.svg?variant=outline&amp;font=geist-mono&amp;logo=lu%3ALink&amp;brand=drizzle&amp;statusDot=true&amp;mode=dark"><img alt="badge" src="https://shieldcn.dev/badge/Website-nayan.ink.svg?variant=outline&amp;font=geist-mono&amp;logo=lu%3ALink&amp;brand=drizzle&amp;statusDot=true&amp;mode=light"></picture></a> <a href="https://x.nayan.ink"><picture><source media="(prefers-color-scheme: dark)" srcset="https://shieldcn.dev/badge/X.com-@nayanexe.svg?variant=outline&amp;font=geist-mono&amp;logo=ri%3ABsTwitterX&amp;brand=drizzle&amp;statusDot=true&amp;mode=dark"><img alt="badge" src="https://shieldcn.dev/badge/X.com-@nayanexe.svg?variant=outline&amp;font=geist-mono&amp;logo=ri%3ABsTwitterX&amp;brand=drizzle&amp;statusDot=true&amp;mode=light"></picture></a> <a href="https://substack.nayan.ink"><picture><source media="(prefers-color-scheme: dark)" srcset="https://shieldcn.dev/badge/Substack-@nayanchandrakar.svg?variant=outline&amp;font=geist-mono&amp;logo=ri%3ABsSubstack&amp;brand=drizzle&amp;statusDot=true&amp;mode=dark"><img alt="badge" src="https://shieldcn.dev/badge/Substack-@nayanchandrakar.svg?variant=outline&amp;font=geist-mono&amp;logo=ri%3ABsSubstack&amp;brand=drizzle&amp;statusDot=true&amp;mode=light"></picture></a> <a href="https://linkedin.nayan.ink"><picture><source media="(prefers-color-scheme: dark)" srcset="https://shieldcn.dev/badge/Linkedin-nayan--chandrakar.svg?variant=outline&amp;font=geist-mono&amp;logo=lu%3ALinkedin&amp;brand=drizzle&amp;statusDot=true&amp;mode=dark"><img alt="badge" src="https://shieldcn.dev/badge/Linkedin-nayan--chandrakar.svg?variant=outline&amp;font=geist-mono&amp;logo=lu%3ALinkedin&amp;brand=drizzle&amp;statusDot=true&amp;mode=light"></picture></a>

## Skills & Languages

**Languages:** typescript, python, sql, bash

**Backend & systems:** bun, node.js, express.js, hono.js, context engineering, ast, lsp, tree-sitter, bloom-filters

**Frontend:** react.js, next.js, tailwindcss, shadcn, zustand, jotai, tanstack query

**Data and orms:** postgresql, mysql, sqlite, mongodb, pgvector, pinecone, drizzle, prisma, zod

**Cloud and infrastructure:** aws, cloudflare, docker, vercel, turborepo, event driven architectures, firebase, convex

**Services:** stripe, resend, redis, auth.js, clerk


## Selected Engineering Work

### [Supermaven](https://github.com/Nayanchandrakar/supermaven)

**LLM-powered VS Code inline completion built around precise code replacement.**

Instead of treating autocomplete as “append text”, it models completion as a **replace-region** problem: keep, insert, replace, or delete.

Tree-sitter provides syntax-aware boundaries; LSP-derived symbols provide cross-file grounding; context is assembled under a hard token budget; completions stream with cancellation; stale requests are aborted; duplicate output is rejected; and accepted responses become minimal undoable edits.

The goal is making raw model output behave like a **precise editor operation**.

### [LeaperOne](https://github.com/Nayanchandrakar/leaperone)

**Digital business cards built as durable, measurable web objects.**

Each card has a stable identifier resolved through an edge service, allowing the destination to remain editable while clicks remain measurable.

The system spans Next.js, Hono, Cloudflare Workers, Neon/Postgres, Redis, S3, CloudFront, Lambda, Stripe, and Resend.

Notable engineering: Redis short-link caching, asynchronous click attribution, opaque Redis sessions, composable authorization middleware, direct-to-S3 presigned uploads, event-driven storage accounting, and device-aware click deduplication.

### [QR Leaper](https://github.com/Nayanchandrakar/qrleaper)

**Dynamic QR infrastructure where the printed code can outlive its destination.**

QR codes encode a stable application URL while the runtime resolves the current destination at scan time. That enables post-print editing, expiration, subscription enforcement, and centralized analytics.

The system covers authentication, Stripe subscriptions, plan quotas, transactional writes, presigned S3 uploads, streamed file delivery with HTTP range support, scan analytics, geo/device metadata, and deduplication.

Core request path: **resolve → validate → enforce limits → record analytics → redirect**.

### [Alpha](https://github.com/Nayanchandrakar/alpha)

**An autonomous prompt-to-app coding system running generated code inside isolated sandboxes.**

A coding agent can inspect files, write files, install packages, and run terminal commands inside an isolated E2B environment.

Long-running generations are orchestrated through Inngest with memoized steps, allowing retries to preserve progress and reconnect to an existing sandbox. The product also handles multi-turn iteration, live previews, code inspection, usage limits, authentication, billing, and persistence.

The engineering question: **how do you make an LLM reliably execute multi-step work against a real filesystem and runtime?**

### [Git Index](https://github.com/Nayanchandrakar/git-doc)

**Repository analysis for understanding codebases before working on them.**

Git Index clones repositories, excludes irrelevant files, estimates token usage, and produces directory-level reports. It combines shallow Git operations, bounded concurrency, Hono APIs, S3 storage, Redis rate limiting, Docker, and TypeScript.

It reflects a recurring interest: **understanding software as files, dependencies, constraints, and context — not isolated source code.**

## Open Source

I contributed **drizzle orm support** to [`rate-limiter-flexible`](https://github.com/animir/node-rate-limiter-flexible/pull/318), including implementation and database-backed tests. The change was merged upstream and published in `v7.2.0`.

Open source forces decisions to survive **existing contracts, review feedback, compatibility, and users outside the codebase**.

## Currently Exploring

I'm particularly interested in the layer where **LLMs meet traditional software engineering**: coding agents that reason over large codebases, use tools safely, preserve context across long sessions, recover from failure, and produce maintainable changes.

Current areas of exploration include **agent runtimes, code intelligence, ASTs/LSPs, vector databases, rag pipelines, context management, model evaluation, distributed execution and developer tooling**.
