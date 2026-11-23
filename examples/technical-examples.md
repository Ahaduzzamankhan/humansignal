# Technical Examples

Version 2.1.0 · Human Signal

Ten worked examples in technical documentation. Each follows the same seven-part structure. The commands and identifiers are illustrative; in real work, verify every one against the implementation.

Related: [../modes/technical.md](../modes/technical.md) · [../references/technical-documentation.md](../references/technical-documentation.md) · [english-examples.md](english-examples.md)

---

## TEC-01 — Marketing README opening

**Original:** "Welcome to Project Atlas, a revolutionary, next-generation platform that seamlessly empowers developers to unlock the full potential of their workflows."

**Issues:** Four promotional modifiers; "seamlessly" and "full potential" undefined; no statement of function.

**Analysis:** The sentence names the project and then describes it entirely in evaluative terms. A reader cannot tell whether it is a build tool, a database, or a dashboard.

**Explanation:** A README's first sentence must let a reader decide whether the project is relevant. Promotion delays that decision.

**Revised:** "Atlas is a command-line build cache for monorepos. It stores compiled artifacts locally and on a shared remote, so a CI job can reuse output from an earlier commit."

**Improvements:** Category, mechanism, and benefit are stated in two sentences.

**Meaning preserved:** No. The original made no falsifiable claim; the revision supplies one that must match the project's actual behavior.

---

## TEC-02 — Vague error message

**Original:** "Error: something went wrong. Please try again later."

**Issues:** No cause; no action; "later" unspecified; no identifier.

**Analysis:** The message reports failure without distinguishing user error, configuration error, or system failure. Retrying may repeat the failure indefinitely.

**Explanation:** An error message is a diagnostic interface. It should tell the user what failed, why (if known), and what to do next.

**Revised:** "Upload failed: the file is 14 MB, above the 10 MB limit for this plan. Compress the file or upgrade at Settings → Billing. Reference: `upl_8f21`."

**Improvements:** Cause, limit, two actions, and a support reference are present.

**Meaning preserved:** Yes, if the limit and plan structure match the product. The reference code is illustrative.

---

## TEC-03 — Missing default

**Original:** "`timeout`: The timeout for the request. Optional."

**Issues:** No unit, default, valid range, or effect; "timeout" restated.

**Analysis:** The entry tells the reader that a timeout exists but not what value to supply or what happens if they omit it. "Optional" without a default is incomplete.

**Explanation:** For configuration, the default is often the most important fact. Without it, the reader cannot predict behavior.

**Revised:** "`timeout_ms` (integer, optional) — Maximum time to wait for a response, in milliseconds. Default: `5000`. Values below `100` are rejected; values above `30000` are clamped to `30000`."

**Improvements:** Name, type, unit, default, and boundary behavior are explicit.

**Meaning preserved:** Yes, assuming these values are correct. The rename from `timeout` to `timeout_ms` must match the implementation.

---

## TEC-04 — Restating the identifier

**Original:** "`max_retries`: The maximum number of retries that can be retried."

**Issues:** Circular description; no default; no statement of which failures are retried or the backoff.

**Analysis:** The description repeats the field name in different words. It does not answer the questions a caller has: how many, for which errors, and with what delay.

**Explanation:** A parameter description should add information to the name, not translate it.

**Revised:** "`max_retries` (integer) — Number of additional attempts after a 5xx response or network error. Default: `2`. Delay doubles from 1 s after each attempt. 4xx responses are not retried."

**Improvements:** Semantics, default, backoff, and the exception are documented.

**Meaning preserved:** Yes, if the behavior is accurate. The original contained no behavior to preserve.

---

## TEC-05 — Inconsistent terminology

**Original:** "Create a job. The task will be queued. Each work item is assigned to a worker. You can monitor the run in the dashboard."

**Issues:** Four terms for one unit of work: job, task, work item, run.

**Analysis:** The paragraph implies four distinct objects. A reader familiar with the system may know they are the same, but a new reader will look for four concepts in the API.

**Explanation:** Terminology is a reference system. Rotation damages it. The fix is to choose the term the code uses and apply it consistently.

**Revised:** "Create a job. The job is queued and assigned to a worker. You can monitor the job in the dashboard."

**Improvements:** One term, one referent. The reader can now map the prose to the API.

**Meaning preserved:** Yes, if the four terms did refer to the same object. If they referred to different layers (job definition, task instance, work item, execution), the original distinction is real and the revision would erase it.

---

## TEC-06 — Documenting an unimplemented feature

**Original:** "The CLI supports incremental rebuilds, parallel execution, and remote caching."

**Issues:** Claims that may not match the implementation; no version or flag information.

**Analysis:** The sentence lists three capabilities as if they were available. If any is planned rather than shipped, the documentation is false.

**Explanation:** Documentation must describe behavior that exists. Aspirational documentation causes failed integrations and erodes trust.

**Revised:** "The CLI supports incremental rebuilds (`--incremental`) and parallel execution (`--jobs N`). Remote caching is planned for 2.2 and is not available in 2.1."

**Improvements:** Each available feature is tied to a flag, and the unavailable one is marked.

**Meaning preserved:** No, unless the implementation matches. The revision is a model for separating shipped from planned behavior.

---

## TEC-07 — "Various fixes" changelog

**Original:** "## 1.4.0\n- Various bug fixes and improvements.\n- Updated dependencies."

**Issues:** Unspecified changes; no user impact; no breaking-change notice.

**Analysis:** The entry tells the reader that something changed but not what. It cannot be used to decide whether to upgrade or to diagnose a regression.

**Explanation:** A changelog is a decision aid. Each entry should name the affected component and the user-visible effect.

**Revised:** "## 1.4.0 — 2026-03-14\n### Fixed\n- `POST /v1/jobs` no longer duplicates a job when the client retries after a timeout; the endpoint now honors `Idempotency-Key`.\n### Changed\n- Minimum Node version is now 20 (was 18). Node 18 is no longer supported."

**Improvements:** A specific fix, a behavior change, and a breaking requirement are documented.

**Meaning preserved:** No. The original contained no details; the revision is a template that must be filled from the actual release.

---

## TEC-08 — Overloaded installation step

**Original:** "Install the dependencies and configure the database and start the server, then check that everything works."

**Issues:** Five actions in one sentence; no commands; no verification criterion; "everything works" undefined.

**Analysis:** The reader must decompose the sentence into steps and infer the commands. The final instruction has no observable success condition.

**Explanation:** Installation steps should be one action each, with copyable commands and a check.

**Revised:**
> 1. Run `npm install`.
> 2. Copy `.env.example` to `.env` and set `DATABASE_URL`.
> 3. Run `npm run migrate`.
> 4. Run `npm start`. The server logs `listening on :3000`.
> 5. Run `curl localhost:3000/health`; it returns `{"status":"ok"}`.

**Improvements:** The sequence is explicit, each step is executable, and success is observable.

**Meaning preserved:** Yes, if these are the project's actual commands and ports.

---

## TEC-09 — Redundant code comment

**Original:**
```js
// Increment the counter by one
counter++;
```

**Issues:** Comment restates the code; no intent, constraint, or reason.

**Analysis:** The comment adds no information that the line does not already carry. It also risks becoming stale if the operation changes.

**Explanation:** Comments are valuable when they explain why, not what. The code already says what.

**Revised:**
```js
// Retries share one counter so the circuit breaker trips across all callers.
counter++;
```

**Improvements:** The comment explains a design decision that is not visible in the line.

**Meaning preserved:** Yes; the code is unchanged.

---

## TEC-10 — Step that hides a prerequisite

**Original:** "Run `docker compose up` to start the stack."

**Issues:** No statement of required Docker version, required environment file, port conflicts, or expected output.

**Analysis:** The command is correct in isolation but may fail for a reader without the Compose plugin, a `.env` file, or free ports. The guide does not say what success looks like.

**Explanation:** A command is only reproducible when its preconditions and result are documented.

**Revised:** "Requires Docker 24+ with the Compose plugin. Copy `.env.example` to `.env` first; the stack reads `POSTGRES_PASSWORD` from it. Run `docker compose up`. When the stack is ready, `docker compose ps` shows `api`, `db`, and `worker` as `running`; the API listens on port 8080."

**Improvements:** Version, prerequisite file, command, and verification are present.

**Meaning preserved:** Yes, if these are the actual requirements and service names.

---

## Cross-example observations

- **Technical editing is verification work.** Almost every revision above depends on facts that only the implementation can confirm.
- **Never rename identifiers for style.** TEC-03 changes `timeout` to `timeout_ms` only because the unit is otherwise ambiguous; in real work, the name must match the code.
- **Separate shipped from planned.** TEC-06 is the most consequential example: aspirational documentation is a factual error, not a stylistic one.
- **One action per step.** TEC-08 and TEC-10 show how much clarity comes from decomposition.

See [../references/technical-documentation.md](../references/technical-documentation.md) and [../modes/technical.md](../modes/technical.md).

Back to [SKILL.md](../SKILL.md).
