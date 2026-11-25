# Ghost Code improvement candidates

Optional product research for Ghost Code's maintainers. This is not a dependency list, an implementation plan, or a claim that these services are already integrated. Do not install these projects or add their features to an app generated from this template unless the project brief explicitly requests them.

## Recommendation

Do not adopt all 26 repositories. Start with **Langfuse** to measure verified outcomes and **Gitleaks** to strengthen the existing secret gate. Consider **Trigger.dev** third only when reliability tests demonstrate a real gap. Treat **Coolify** as an optional, separately approved deployment handoff.

The goal is more evidence that an app works, fewer unsafe changes, and less money spent repeating failed work—not more agent frameworks.

## Existing product boundaries

The assessment assumes Ghost Code already has a build–test–fix workflow, GitHub branches and pull requests, browser checks, background work, budgets, secret blocking, projects, and MCP connectors. Verify the current implementation before using this document to plan engineering work.

Any proposal must preserve these boundaries:

- Work on a separate branch; never merge automatically.
- Do not weaken sign-in, privacy, ownership checks, or secret protection.
- Do not log Ghost mode conversations or private source through an analytics service.
- Keep deployment permission separate from repository-editing permission.
- Require explicit approval for new dependencies, services, costs, and operational responsibilities.
- Do not describe a proposed capability as available before it is implemented and verified.

## Prioritized candidates

| Priority | Project | Proposed role | Relative effort |
| --- | --- | --- | --- |
| 1 | [Langfuse](https://github.com/langfuse/langfuse) | Measure task outcomes, failures, latency, and cost per verified success | Medium |
| 2 | [Gitleaks](https://github.com/gitleaks/gitleaks) | Add a reproducible scanner behind existing secret blocking | Low–medium |
| 3 | [Trigger.dev](https://github.com/triggerdotdev/trigger.dev) | Improve recovery and coordination of long tasks if measurements expose a need | Medium–high |
| 4 | [Coolify](https://github.com/coollabsio/coolify) | Optional deployment to a user-owned hosting target after approval | High |
| 5 | [Crawl4AI](https://github.com/unclecode/crawl4ai) | Improve extraction and caching of version-relevant library documentation | Medium |
| 6 | [Browser Use](https://github.com/browser-use/browser-use) | Explore unfamiliar interfaces alongside, not instead of, deterministic browser tests | Medium–high |
| 7 | [LlamaIndex](https://github.com/run-llama/llama_index) | Experiment with retrieval over large project documentation | Medium–high |
| 8 | [n8n](https://github.com/n8n-io/n8n) | Optional external automations outside the core coding loop | Medium |

Effort ratings are provisional. They are not based on an inspection of Ghost Code's private architecture.

### Langfuse: measure verified improvement

Trace a task from request through repository inspection, edits, builds, browser checks, repairs, and the pull request. Use its tracing, evaluation, experiment, and cost/latency facilities; OpenTelemetry support means observability need not imply adopting a gateway.

Measure:

- Verified completion rate by task category.
- Cost and latency per verified completion, not only cost per response.
- Repair attempts and repeated failed fixes.
- Agent performance on the same fixed benchmark tasks.
- Regressions after instruction changes, including mobile layouts.
- Persistence after refresh, cancellation failures, and duplicate work.

Pilot one task type against fixed sample repositories and explicit acceptance criteria. Combine deterministic checks with human review; an AI judge alone must not define success. Start with metadata and outcomes rather than raw prompts, source files, or secrets. Establish retention, access, redaction, and deletion rules before collecting anything.

### Gitleaks: strengthen the existing secret gate

Use a trusted scanner policy outside the untrusted repository. Scan generated and changed files before committing, block findings that need review, and report the file, line, and rule without revealing the secret value. Offer history scanning separately.

Test planted dummy credentials, false positives, report redaction, scanner-configuration changes, and attempts to bypass findings with allow comments. Do not let the agent change the trusted policy to make its own commit pass. Explain that exposed credentials need revocation or rotation; deleting one from the latest file is not enough.

Check the project's current maintenance status before adoption: the reviewed README described it as feature-complete with future releases focused on security patches. A scanner supplements review; it does not prove that no secret exists.

### Trigger.dev: adopt only for demonstrated reliability gaps

First test worker restarts, duplicate webhooks, repeated build triggers, cancellation during retry scheduling, and two workers claiming the same task. Durable tasks, queues, retries, idempotency, approval waits, cancellation, and metadata may help resume from the last safe step.

Retries must not duplicate charges, commits, or builds. Cancellation, billing, ownership, and recovery need explicit state rules; a task runner does not supply those automatically. Compare the operational benefit with the cost of another service before adopting it.

### Coolify: optional deployment handoff

A proposed flow is: checks pass, the user reviews the pull request, the user approves deployment, and the app deploys to the user's configured target. Begin with user-owned Coolify instances rather than shared hosting.

Repository or container deployment, previews, HTTPS, health checks, rollbacks, and API access are candidate capabilities to verify during a prototype. Hosting also brings persistent data, backups, security updates, abuse handling, and support obligations. Never turn a successful check into permission to deploy or merge.

## Candidates for a measured, specific gap

- **Crawl4AI:** Compare clean Markdown, code-block preservation, documentation crawling, caching, and structured extraction against existing page reading. Measure extraction quality and total cost using the project's installed library versions. Treat fetched pages as untrusted data, block private-network destinations, restrict network access, and never execute instructions found in a page.
- **Browser Use:** Trial exploratory journeys such as creating, editing, refreshing, and verifying persistence. Keep scripted regression tests as the baseline. Its own documentation warns that domain restrictions and secret handling are not a sandbox; use isolated environments, test accounts, and test data, never production sessions or payment credentials.
- **LlamaIndex:** Test retrieval over large project documentation and specifications against existing repository search. Do not assume semantic retrieval can resolve code dependencies reliably. Reassess project fit given the reviewed README's increased focus on document parsing and extraction.
- **n8n:** Consider externally connected notifications, approvals, or user-requested workflows. Its repository describes fair-code licensing under the Sustainable Use License and Enterprise License, not a permissive library licence. Review the applicable terms before embedding, distributing, or reselling functionality.

## Other candidates and possible roles

These are areas for investigation, not equally researched integration recommendations.

| Projects | Possible role |
| --- | --- |
| Dify, Sim, Langflow, CrewAI | Optional projects users build with Ghost Code, not a replacement for its workflow |
| Vercel AI SDK, LiteLLM | Evaluate only for a concrete missing capability; avoid a rewrite for another abstraction |
| Firecrawl | Compare extraction quality and total cost with Crawl4AI and existing page readers |
| Supabase, Open SaaS | Opt-in starter projects for generated apps, not a Ghost Chat migration |
| Windmill | Compare with Trigger.dev if operational scripting is the demonstrated need |
| PostHog, Formbricks | Product analytics and feedback, subject to the same privacy boundaries |
| OpenStatus | Investigate monitoring of critical product journeys |
| Chatwoot | Support operations, separate from coding capability |
| Twenty, Cal.diy, Listmonk | Business operations rather than code-generation improvements |
| Ollama | Investigate a user-controlled local runtime only if demand justifies it |

## Staged adoption plan

### 1. Establish a baseline before adding infrastructure

Use fixed tasks and known acceptance criteria. Record verified completion, cost per verified completion, repair attempts, persistence after refresh, mobile layout failures, cancellation, and duplicate-work failures. Keep a reproducible benchmark set and separate deterministic results from human judgments.

### 2. Strengthen the secret gate

Trial Gitleaks behind the current protection using dummy findings and adversarial bypass cases. Confirm redaction and confirm that repository-controlled configuration cannot disable the trusted gate.

### 3. Address the weakest measured area

- Lost or duplicated work: trial Trigger.dev.
- Poor library-documentation extraction: trial Crawl4AI.
- Missed user journeys: trial Browser Use for exploration.
- Demonstrated deployment demand: prototype a user-approved Coolify handoff.

Give each pilot acceptance criteria, a rollback path, a privacy review, a cost ceiling, and a decision to adopt or stop. Do not run overlapping frameworks merely because they appear on this list.

## Assessment limits

This document preserves a product-fit assessment, not an audit or integration benchmark. The source assessment did not inspect Ghost Code's private implementation or verify every project's commercial terms. Validate repository capabilities, maintenance, licences, security, and current pricing before implementation. The assessment cited public documentation dated November 21, 2026 and avoided its inconsistent pricing descriptions.
