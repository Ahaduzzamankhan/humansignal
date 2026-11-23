# Technical Documentation

Version 2.1.0 · Human Signal

In technical documentation, precision is the style. A sentence that reads beautifully but misstates a default value, a status code, or a scope is a defect. This file covers the document types Human Signal supports and the rules that govern editing them.

Related: [context-awareness.md](context-awareness.md) · [../modes/technical.md](../modes/technical.md) · [../examples/technical-examples.md](../examples/technical-examples.md) · [vocabulary-analysis.md](vocabulary-analysis.md)

---

## Overriding rule

**Technical accuracy outranks stylistic preference.** If a choice is between a more natural sentence and a correct one, choose correct. If a rewrite would change a command, identifier, type, default, or error code, do not make it.

Never rewrite, for style:

- code identifiers, function names, class names, module names;
- API endpoints, parameter names, header names, status codes;
- command-line flags, environment variables, configuration keys;
- file paths, package names, version numbers;
- error messages and log output;
- protocol names, standards, and units.

If one of these looks wrong, verify it against the implementation and report the discrepancy. Do not silently "fix" it.

---

## 1. README files

**Purpose.** Help a reader decide whether to use the project, and get it running if they do.

**Structure that works.**
1. One-sentence description of what the project does and for whom.
2. Status (stable, beta, unmaintained) if relevant.
3. A minimal working example or quick start.
4. Installation with prerequisites and supported versions.
5. Core usage, with the two or three tasks most users need.
6. Configuration summary, linking to full reference.
7. Troubleshooting for common failures.
8. Contributing, license, and support links.

**Common weaknesses.**
- Opening with a mission statement instead of a description.
- Badges with no explanation.
- A quick start that omits a prerequisite.
- Examples that do not run.
- Feature lists that describe intentions rather than behavior.

**Editing guidance.**
- Test every command in a clean environment.
- State versions and platforms.
- Put the fastest path to "it works" near the top.
- Link to depth rather than including all of it.

---

## 2. API documentation

**Purpose.** Let a developer call the interface correctly without reading the source.

**Required elements per operation.**
- Method and path.
- Purpose in one sentence.
- Authentication and required scopes.
- Parameters: name, type, required/optional, default, constraints, example.
- Request body schema, with required and optional fields.
- Response schema, with status codes and error shapes.
- Rate limits and idempotency behavior.
- One complete request and response example.

**Style rules.**
- Use the second person for instructions ("Send…", "Include…").
- Use the present tense for behavior ("Returns 404 when…").
- Name fields exactly as they appear on the wire.
- Distinguish null, absent, empty string, and zero.
- Document ordering, pagination, and filtering semantics.

**Common weaknesses.**
- Types given loosely ("string or number").
- Optional fields with undocumented defaults.
- Error responses omitted.
- Examples that omit required headers.
- Descriptions that restate the field name ("`name`: the name").

**Editing guidance.** For each field, ask what a caller must know to send a valid value and interpret the response. Document that, and nothing decorative.

---

## 3. Installation guides

**Purpose.** Move a reader from a supported starting state to a working installation.

**Requirements.**
- State prerequisites with versions.
- Give commands that can be copied verbatim.
- Explain what each step does only when it is non-obvious.
- Include a verification step.
- Cover the common failure modes: permissions, proxies, missing compilers, conflicting versions.
- State platform differences explicitly.

**Common weaknesses.**
- "Simply install…" without saying how.
- Assuming a package manager or shell.
- Mixing instructions for different operating systems.
- No verification, so the reader does not know whether it worked.
- Hidden steps (creating a directory, setting an environment variable).

**Editing guidance.** Follow the guide on a clean machine or container. Every place you improvise is a missing step.

---

## 4. Architecture documentation

**Purpose.** Explain how a system is structured, why it is structured that way, and what constraints shaped it.

**What to include.**
- Context: what the system does and where its boundary is.
- Components and their responsibilities.
- Data flow and control flow.
- Storage, consistency, and failure behavior.
- Deployment topology.
- Key trade-offs and rejected alternatives.
- Known limits and planned changes.

**What to avoid.**
- Diagrams without a legend or explanation.
- Describing every class instead of the important boundaries.
- Presenting decisions as inevitable.
- Aspirational architecture that does not match the code.

**Editing guidance.** Every architectural claim should be traceable to the repository or to a decision record. Mark proposals as proposals.

---

## 5. Tutorials

**Purpose.** Teach a reader to complete a task by doing it.

**Structure.**
1. What the reader will build and why it is useful.
2. Prerequisites and estimated time.
3. Numbered steps, each with a verifiable result.
4. A checkpoint where the reader can confirm progress.
5. Next steps and where to go deeper.

**Style rules.**
- One action per step.
- Imperative mood.
- Show expected output after commands that produce it.
- Explain errors the reader is likely to hit.
- Keep the tutorial on one path; move alternatives to notes.

**Common weaknesses.**
- Conceptual lectures between steps.
- Steps that skip intermediate state.
- "Now do the same for the other files" without listing them.
- No working final state.
- Examples that depend on the author's private data.

---

## 6. Changelogs

**Purpose.** Tell users what changed between versions and what they must do about it.

**Format.** Group by release, newest first. Within a release, group by type: Added, Changed, Deprecated, Removed, Fixed, Security.

**Rules.**
- Write for users, not for the commit log.
- Name the affected component.
- Mark breaking changes prominently and explain the migration.
- Link to issues or pull requests where useful.
- Keep entries in past or present tense consistently.
- Include the version number and date.

**Common weaknesses.**
- "Various bug fixes and improvements."
- Internal refactors listed as user-facing changes.
- Breaking changes buried in a list.
- No migration note.
- Versions out of order.

**Example.**
- Weak: "Improved the API."
- Better: "`POST /v2/jobs` now rejects payloads over 1 MB with `413 payload_too_large`; the previous limit was 10 MB."

---

## 7. Release notes

**Purpose.** Communicate a release to users, with emphasis on impact and action.

**Difference from a changelog.** A changelog is exhaustive and structured; release notes are selective and narrative. They highlight the changes that matter and explain why.

**What to include.**
- The headline change and its benefit, stated concretely.
- Breaking changes and required actions.
- Known issues.
- Upgrade instructions.
- Links to full documentation.

**What to avoid.**
- Marketing superlatives.
- Long feature lists with no priority.
- Repeating the changelog verbatim.
- Omitting the upgrade path.

---

## 8. Error messages

**Purpose.** Tell the user what went wrong, why, and what to do next.

**Anatomy of a good message.**
1. What failed, in plain terms.
2. The specific cause, if known.
3. The action to take, if one exists.
4. An identifier for support, if useful.

**Example.**
- Weak: "Error: invalid input."
- Better: "`timeout_ms` must be a positive integer; received `-1`. Set it to at least 1, or omit it to use the default of 5000."

**Rules.**
- Do not blame the user.
- Do not expose secrets or internal paths.
- Keep the message stable enough to search for.
- Log detail; display guidance.
- Distinguish user error, configuration error, and system failure.

---

## 9. Code comments

**Purpose.** Explain intent, constraints, and non-obvious decisions.

**Comment what the code cannot say.**
- Why this approach rather than the obvious one.
- What invariant the code depends on.
- What external system behavior is being worked around.
- What the units are, when they are not in the type.
- What would break if the code changed.

**Do not comment what the code already says.** `// increment i` above `i++` is noise.

**Style.**
- Keep comments close to the code they describe.
- Update comments when the code changes; a stale comment is worse than none.
- Use the project's doc-comment convention for public interfaces.
- Mark uncertainty explicitly (`// TODO: assumes single-writer`).

---

## 10. Configuration guides

**Purpose.** Let an operator set up and tune the system safely.

**Requirements.**
- List every option with type, default, valid range, and effect.
- State which options require a restart.
- Explain interactions between options.
- Provide a minimal working configuration and a production example.
- Document precedence (file, environment, CLI flag).
- Warn about options that affect security or data loss.

**Common weaknesses.**
- Defaults omitted.
- "See the source" instead of documentation.
- Units unspecified (seconds? milliseconds?).
- No example of a valid file.
- Security-relevant options described neutrally.

---

## 11. Developer guides

**Purpose.** Help a contributor work effectively inside the codebase.

**What to include.**
- Local setup and test commands.
- Repository layout and where things live.
- Coding conventions and linting.
- Branch, commit, and review workflow.
- How to add a feature end to end (a "golden path").
- Where to ask questions.

**Rules.**
- Prefer commands over descriptions.
- Keep the guide current with the build system.
- Link to deeper references rather than duplicating them.

---

## 12. Troubleshooting documentation

**Purpose.** Help a reader diagnose and fix a problem without contacting support.

**Structure.** Symptom → likely causes (ordered by frequency) → diagnostic steps → fix → prevention.

**Rules.**
- Organize by symptom, in the user's words.
- Give commands that produce diagnostic information.
- State what a normal result looks like.
- Distinguish "fix" from "workaround."
- Link to related errors.

**Example.**
- Symptom: "The service exits immediately after start."
- Causes: missing `DATABASE_URL`; port already in use; incompatible Node version.
- Diagnostic: `journalctl -u api --no-pager | tail -40`.
- Fix: set the variable, free the port, or use the supported version.

---

## 13. Migration guides

**Purpose.** Move users from one version or system to another without data loss or surprise.

**Structure.**
1. Who needs to migrate and who does not.
2. Breaking changes, with before/after examples.
3. Step-by-step migration, with rollback at each stage.
4. Verification.
5. Known issues and support.

**Rules.**
- State the supported source and target versions.
- Show the exact diff for configuration and API changes.
- Explain data migrations, including downtime and reversibility.
- Warn about irreversible steps before they occur.
- Provide a rollback path or say explicitly that none exists.

---

## 14. Security documentation

**Purpose.** Help users deploy and operate the system without introducing vulnerabilities.

**What to include.**
- Threat model and trust boundaries.
- Authentication and authorization model.
- Secret handling and rotation.
- Network exposure and recommended defaults.
- Known vulnerabilities and disclosure policy.
- Secure configuration examples.
- Audit logging and monitoring.

**Rules.**
- Never include real credentials or tokens in examples.
- State the security impact of each option.
- Distinguish "not recommended" from "unsafe."
- Keep advisories dated and versioned.
- Do not soften a vulnerability's severity for tone.

---

## Cross-cutting documentation rules

### Audience
Name the intended reader at the top when a document serves more than one. Separate the quick start from the reference.

### Terminology
Use one term per concept. If the code calls it `workspace`, do not call it "project" in one section and "tenant" in another. Maintain a glossary for overloaded terms.

### Tense and mood
- Instructions: imperative ("Run…").
- Behavior: present tense ("Returns…").
- History and changelogs: past tense ("Fixed…").
- Requirements: "must" for hard requirements, "should" for recommendations, "may" for permission.

### Numbers and units
Always include units. State whether timeouts are seconds or milliseconds. Give byte limits in the unit the API uses. Use consistent decimal precision.

### Examples
Every example must be runnable or clearly labeled as illustrative. Use realistic values. Never invent output that the command would not produce.

### Linking
Link to the canonical page rather than repeating content. Check that anchors and paths resolve before publishing.

### Deprecation
Mark deprecated features with the version of deprecation and the removal target. Offer the replacement.

### Accessibility
Use descriptive link text, alt text for diagrams, and heading levels that reflect structure rather than appearance.

---

## Editing checklist for technical documents

- [ ] Every command was tested or verified against the source.
- [ ] Every identifier matches the implementation.
- [ ] Every default value is stated and correct.
- [ ] Every error path is documented or intentionally omitted.
- [ ] Units are explicit.
- [ ] Prerequisites and supported versions are stated.
- [ ] Examples are complete and runnable.
- [ ] Terminology is consistent.
- [ ] No marketing language remains.
- [ ] No feature is described that does not exist.
- [ ] Internal links resolve.
- [ ] The document states what it does not cover.

Back to [SKILL.md](../SKILL.md).
