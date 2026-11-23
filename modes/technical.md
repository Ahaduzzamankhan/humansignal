# Technical Mode

Version 2.1.0 · Human Signal

## Intended use

Technical documentation and engineering communication: READMEs, API references, installation and configuration guides, tutorials, architecture notes, changelogs, release notes, migration guides, error messages, code comments, and security documentation.

Use this mode when a reader must perform a task, integrate a system, or verify behavior. Do not use it for persuasive or reflective writing; the register will sound cold.

## Tone

Direct, neutral, and precise. The writer is a knowledgeable colleague explaining what the system does and how to use it. No enthusiasm, no apology, no marketing.

Confidence is appropriate when behavior is verified. When behavior depends on configuration, version, or environment, state the condition rather than hedging vaguely.

## Vocabulary

- Use the exact names from the implementation: identifiers, endpoints, flags, environment variables, status codes, file paths, package names.
- Use one term per concept. If the code says `workspace`, the documentation says `workspace`.
- Define abbreviations on first use, unless the audience universally knows them.
- Prefer concrete verbs: returns, rejects, writes, retries, expires, blocks.
- Avoid: "seamless," "powerful," "robust," "leverage," "simply," "just," "easy," "obviously."
- Include units in every quantity: milliseconds, MiB, requests per second.
- Distinguish must / should / may; do not use "should" for a hard requirement.

## Sentence characteristics

- Short to medium sentences. One instruction per sentence.
- Imperative mood for actions: "Run the migration." "Set `DATABASE_URL`."
- Present tense for behavior: "The endpoint returns 404 when the job does not exist."
- Past tense for changelogs: "Fixed a race condition in the scheduler."
- Active voice when the actor is the user or a named component; passive when the actor is irrelevant.
- Conditions before consequences: "If the token is expired, the request fails with 401."
- Avoid nested clauses in procedures. A step that needs a subordinate clause usually needs to be two steps.

## Paragraph structure

- Lead with the task or behavior, not with background.
- One topic per section; use headings that state the topic specifically.
- Put prerequisites before steps, verification after steps.
- Use numbered lists for sequences and bullets for parallel options.
- Tables for parameters, status codes, and configuration keys.
- Keep prose paragraphs short; most technical sections are lists, examples, or short explanations.

## Common mistakes

1. **Marketing language.** "A powerful, seamless API" tells the reader nothing.
2. **Feature without behavior.** "Supports retries" without saying how many, on what errors, with what backoff.
3. **Undocumented defaults.** Optional parameters with no stated default.
4. **Missing failure modes.** No documentation of errors, limits, or partial success.
5. **Unstated prerequisites.** A quick start that assumes a tool, version, or permission.
6. **Untested examples.** Commands or code that do not run as written.
7. **Inconsistent terminology.** "Job," "task," and "run" used for the same object.
8. **Restating the identifier.** "`timeout`: the timeout." Say the unit, default, and effect.
9. **Vague quantities.** "Large payloads" instead of "payloads over 1 MB."
10. **Documentation drift.** Describing a previous version's behavior.

## Editing rules

1. Verify every command, identifier, default, and status code against the implementation.
2. Never rename code identifiers, endpoints, or configuration keys for style.
3. Add the missing unit, default, or condition rather than smoothing the sentence.
4. Replace evaluative adjectives with observable behavior.
5. Cut "simply," "just," and "easy"; they blame the reader for difficulty.
6. Put the condition before the consequence.
7. Keep one instruction per step.
8. State what the document does not cover.
9. Test internal links and anchors.
10. If a fact cannot be verified, mark it as unverified or remove the claim.

## Examples

**Before:**
> Our powerful API makes it easy to seamlessly integrate with your workflow. Simply configure the timeout and you're good to go.

**After:**
> Set `timeout_ms` to the maximum time a request may run. The default is 5000; values above 30000 are rejected with `400 invalid_timeout`.

**Why:** It replaces promotion with a parameter, a default, a limit, and an error.

**Before:**
> ## Configuration
> This section explains the configuration options.

**After:**
> ## Configuration
> The service reads `config.toml` at startup. Environment variables override file values; command-line flags override both.

**Why:** The first sentence after the heading now carries information instead of restating the heading.

**Before:**
> The job retries failed uploads.

**After:**
> The job retries uploads that fail with a 5xx response or a network error, up to three times, with exponential backoff starting at 2 seconds. A 4xx response is not retried.

**Why:** It specifies which failures, how many attempts, the delay, and the exception.

**Before:**
> An error occurred while processing your request.

**After:**
> The uploaded file is 14 MB, above the 10 MB limit. Compress it or split it into smaller files.

**Why:** The error names the cause and the action.

## Checklist

- [ ] Commands are tested and complete.
- [ ] Identifiers match the implementation exactly.
- [ ] Defaults, units, and limits are stated.
- [ ] Error behavior is documented.
- [ ] Prerequisites and versions are stated.
- [ ] Examples are runnable.
- [ ] Terminology is consistent.
- [ ] No marketing language remains.
- [ ] No unimplemented feature is described.
- [ ] Links and anchors resolve.

See [../references/technical-documentation.md](../references/technical-documentation.md) and [../examples/technical-examples.md](../examples/technical-examples.md).

Back to [SKILL.md](../SKILL.md).
