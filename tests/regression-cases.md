# Regression Cases

Version 2.1.0 · Human Signal

These cases test whether the skill's guidance produces the right behavior under pressure. Each case describes a text, the failure the skill is at risk of producing, the correct behavior, and the criteria for passing.

**Method note.** These are specification walkthroughs: each case was traced against the instructions in `SKILL.md`, the mode files, and the reference files. Where the instructions permitted a bad outcome, the guidance was tightened (see §3). This is not an empirical evaluation of a language model, and the results should not be reported as one.

Related: [quality-checklist.md](quality-checklist.md) · [meaning-preservation.md](meaning-preservation.md) · [../references/editing-guidelines.md](../references/editing-guidelines.md)

---

## REG-01 — Over-editing concise writing

**Input:**
> "The build failed. Exit code 1. See `build.log` line 42."

**Risk:** The skill treats short sentences as a rhythm problem and merges them, or expands them with explanation the reader does not need.

**Correct behavior:** Leave the text unchanged. This is a diagnostic message; brevity and scannability are the point. Three fragments are conventional in this genre.

**Failure signature:** "The build encountered a failure, returning exit code 1; for additional details, refer to line 42 of `build.log`." Longer, slower, no new information.

**Pass criteria:**
- No merge, no expansion.
- No added transitions.
- Genre recognized as diagnostic output.

**Result:** Pass. The guidance in [../modes/technical.md](../modes/technical.md) states that short sentences and fragments are appropriate for error output, and [../references/sentence-structure.md](../references/sentence-structure.md) §5 warns against splitting or merging for rhythm alone.

---

## REG-02 — Changing technical meaning

**Input:**
> "`max_retries` defaults to 2. A 4xx response is not retried."

**Risk:** The skill "improves" the prose by saying "failed requests are retried twice," which is false for 4xx responses, or changes `max_retries` to "retry limit."

**Correct behavior:** Preserve the identifier, the default, and the exception. If clarification is needed, add it without altering the rule.

**Failure signature:** "Failed requests are retried twice by default." The exception is gone and the identifier is renamed.

**Pass criteria:**
- `max_retries` unchanged.
- Default `2` unchanged.
- 4xx exception retained.
- Any added sentence is verifiable.

**Result:** Pass. [../references/technical-documentation.md](../references/technical-documentation.md) lists identifiers, defaults, and error behavior as protected, and [../tests/meaning-preservation.md](meaning-preservation.md) §2.3 requires a token-level diff.

---

## REG-03 — Removing necessary repetition

**Input:**
> "A tenant's data is isolated from other tenants. Tenant isolation is enforced at the storage layer. Each tenant has a separate encryption key."

**Risk:** The skill flags "tenant" as repeated and rotates synonyms: customer, account, organization.

**Correct behavior:** Keep "tenant" throughout. The repetition is the referent; rotation would imply multiple entities.

**Failure signature:** "A customer's data is isolated from other accounts. Organization isolation is enforced at the storage layer. Each client has a separate key."

**Pass criteria:**
- One term per referent.
- No synonym substitution for a technical entity.
- Repetition recognized as functional.

**Result:** Pass. [../references/vocabulary-analysis.md](../references/vocabulary-analysis.md) §5 and §8 state the rule explicitly, and [../references/ai-writing-patterns.md](../references/ai-writing-patterns.md) AWP-105 covers thesaurus swaps.

---

## REG-04 — Adding unnecessary transitions

**Input:**
> "Latency rose after the deploy. The connection pool was saturated."

**Risk:** The skill adds "Furthermore" or "Therefore" to "improve flow," or inserts a signpost sentence.

**Correct behavior:** Either leave the two sentences as they are, or make the causal relation explicit if the writer intended it: "Latency rose after the deploy because the connection pool was saturated." Do not add a connector that does not carry a relation.

**Failure signature:** "Furthermore, latency rose after the deploy. Additionally, the connection pool was saturated." The causal link is still missing, and two empty connectors were added.

**Pass criteria:**
- No connector without a named relation.
- No added signpost sentence.
- If a relation is added, it is one the writer's text supports.

**Result:** Pass, with a clarification added to [../references/editing-guidelines.md](../references/editing-guidelines.md): "Do not add transitions merely to smooth the surface."

---

## REG-05 — Making formal writing too casual

**Input:**
> "The committee has determined that the proposed amendment would not materially affect the existing contractual obligations of either party."

**Risk:** The skill replaces "determined" with "decided," "materially affect" with "change," and contracts "would not" to "wouldn't," producing a sentence that misstates the legal register.

**Correct behavior:** Preserve the register and the terms of art. "Materially affect" has a specific legal sense; "party" and "obligations" are defined terms.

**Failure signature:** "The committee decided the amendment wouldn't really change either side's existing contract obligations."

**Pass criteria:**
- Terms of art preserved.
- Register unchanged.
- Any simplification limited to syntax, not legal meaning.

**Result:** Pass. [../modes/academic.md](../modes/academic.md) and [../references/context-awareness.md](../references/context-awareness.md) §7–8 require register preservation in high-consequence text, and [../references/ai-writing-patterns.md](../references/ai-writing-patterns.md) AWP-080 covers the reverse error.

---

## REG-06 — Making conversational writing too formal

**Input:**
> "Can you send the link? I can't find it."

**Risk:** The skill treats the contraction and question as informal and rewrites: "Would you kindly provide the link? I am unable to locate it."

**Correct behavior:** Leave it. The register matches a peer chat; the request is clear and polite.

**Failure signature:** A two-line message becomes a formal request with "kindly" and no contraction.

**Pass criteria:**
- Register unchanged.
- No added ceremony.
- The ask and the reason remain.

**Result:** Pass. [../modes/conversational.md](../modes/conversational.md) states that warmth and directness are appropriate and that contractions are normal.

---

## REG-07 — Producing generic replacements

**Input:**
> "The migration moved 4.2 million rows in six hours, with two failed batches that were retried."

**Risk:** The skill removes the numbers as "detail" and replaces them with a general statement: "The migration completed successfully despite some issues."

**Correct behavior:** Keep the numbers. They are the content. The only possible edit is punctuation or ordering, not generalization.

**Failure signature:** A specific, verifiable sentence becomes a vague summary.

**Pass criteria:**
- Numbers retained.
- No evaluative substitution ("successfully," "some issues").
- Any rewrite preserves the measurable claim.

**Result:** Pass. [../references/natural-language-principles.md](../references/natural-language-principles.md) §7 and [../references/ai-writing-patterns.md](../references/ai-writing-patterns.md) AWP-024 both prohibit replacing numbers with vague quantifiers.

---

## REG-08 — Introducing unsupported claims

**Input:**
> "The new onboarding flow reduced support tickets."

**Risk:** The skill adds a figure ("by 40%") or a cause ("because it added a progress bar") to make the sentence more specific.

**Correct behavior:** Do not add facts. If specificity is needed, mark the gap: "The new onboarding flow reduced support tickets; the measured change is not stated here."

**Failure signature:** A plausible but invented number appears in the revision.

**Pass criteria:**
- No new numbers, causes, names, or examples.
- Any added specificity is a placeholder flagged for the writer.
- The revision is no more confident than the original.

**Result:** Pass. [../tests/meaning-preservation.md](meaning-preservation.md) §3 step 5 checks the reverse direction for added claims, and [../references/editing-guidelines.md](../references/editing-guidelines.md) forbids adding unsupported details.

---

## REG-09 — Voice flattening

**Input:**
> "Honestly, the whole thing was a mess — we shipped on Friday, broke the API, and spent the weekend undoing it. Lesson learned: never deploy before a holiday."

**Risk:** The skill removes the dash, the fragment, and the first-person stance, producing neutral prose: "The deployment occurred on Friday and caused API failures that required remediation over the weekend."

**Correct behavior:** Preserve the voice. The dash, the aside, and the direct judgment are the author's. A light edit may fix a comma or clarify "the whole thing," but the stance stays.

**Failure signature:** A personal, wry incident note becomes an impersonal report.

**Pass criteria:**
- First person and stance preserved.
- Deliberate dash and fragment retained.
- No added neutrality or formality.

**Result:** Pass. [../references/editing-guidelines.md](../references/editing-guidelines.md) Part V requires voice preservation, and [../modes/creative.md](../modes/creative.md) treats fragments and dashes as legitimate devices.

---

## REG-10 — Editing a sentence that is already good

**Input:**
> "Backups run nightly; restores are tested weekly."

**Risk:** The skill rewrites a balanced, precise sentence because it is short, uses a semicolon, and repeats a parallel structure.

**Correct behavior:** Leave it. The semicolon marks a real contrast, the parallelism is functional, and the length matches the content.

**Failure signature:** "Backups are performed on a nightly basis, and on a weekly basis the team conducts tests of the restoration process."

**Pass criteria:**
- No change without an identified problem.
- Semicolon and parallelism retained.
- No nominalization introduced.

**Result:** Pass. The minimum-effective-edit rule in [../references/editing-guidelines.md](../references/editing-guidelines.md) Part IV requires a named problem before any change.

---

## REG-11 — Normalizing a deliberate list

**Input:**
> "Three things broke: the scheduler, the queue, and my patience."

**Risk:** The skill flags the list as an unparallel triad (two components and an abstraction) and "fixes" it to "the scheduler, the queue, and the notification service."

**Correct behavior:** Leave it. The third item is a deliberate joke; the parallelism break is the point.

**Failure signature:** The joke is removed and replaced with a third component the writer did not mention.

**Pass criteria:**
- Deliberate rhetorical break recognized.
- No invented list item.
- Voice preserved.

**Result:** Pass, with a note added to [../references/sentence-structure.md](../references/sentence-structure.md) §11 that parallelism rules apply when items are meant to be compared, not when a deliberate break carries the effect.

---

## REG-12 — Adding a conclusion the writer did not make

**Input:**
> "The pilot ran for eight weeks in two stores. Sales rose 6% in one and fell 2% in the other."

**Risk:** The skill adds an evaluative conclusion: "Overall, the pilot was a success."

**Correct behavior:** Do not add a conclusion. The data are mixed, and the writer has not interpreted them. If a conclusion is required by the genre, mark it as needed rather than inventing one.

**Failure signature:** A summary judgment appears that the evidence does not support.

**Pass criteria:**
- No evaluative conclusion added.
- Both results preserved.
- No cherry-picking of the positive result.

**Result:** Pass. [../references/paragraph-analysis.md](../references/paragraph-analysis.md) §11 and [../tests/meaning-preservation.md](meaning-preservation.md) §5 prohibit conclusions that outrun the evidence.

---

## 1. Results summary

| Case | Risk tested | Result | Guidance relied on |
|---|---|---|---|
| REG-01 | Over-editing concise writing | Pass | Technical mode; sentence-structure §5 |
| REG-02 | Changing technical meaning | Pass | Technical documentation; preservation §2.3 |
| REG-03 | Removing necessary repetition | Pass | Vocabulary §5, §8; AWP-105 |
| REG-04 | Adding unnecessary transitions | Pass (clarified) | Editing guidelines Part II |
| REG-05 | Formal → casual | Pass | Context awareness §7–8; AWP-080 |
| REG-06 | Conversational → formal | Pass | Conversational mode |
| REG-07 | Generic replacement | Pass | Natural principles §7; AWP-024 |
| REG-08 | Unsupported claims | Pass | Preservation §3; editing guidelines Part II |
| REG-09 | Voice flattening | Pass | Editing guidelines Part V; creative mode |
| REG-10 | Editing good prose | Pass | Minimum effective edit |
| REG-11 | Normalizing deliberate list | Pass (clarified) | Sentence structure §11 |
| REG-12 | Adding a conclusion | Pass | Paragraph analysis §11; preservation §5 |

---

## 2. Failure patterns to watch

These are the ways a style-focused edit most often goes wrong. Each is paired with the instruction that prevents it.

| Failure pattern | Prevention |
|---|---|
| **Improvement without a problem** | Require a located, described, explained observation before editing |
| **Length as a proxy for quality** | Judge by information per unit of reader effort, not word count |
| **Variety as a goal** | Vary only when content's role changes |
| **Specificity invented** | Never add a fact; flag the gap |
| **Terminology cleaned up** | Treat identifiers as data |
| **Voice neutralized** | Record voice features before editing |
| **Register homogenized** | Apply the mode file for the genre |
| **Conclusion appended** | Require the writer's judgment or leave the data uninterpreted |
| **Transitions added** | Add only when a relation is unclear and supported |
| **Lists normalized** | Check whether the break is deliberate |

---

## 3. Guidance changes made after the walkthrough

The following changes were made to the skill during this release to close gaps the cases exposed. They are recorded here so future maintainers can see why the wording exists.

1. **Added an explicit minimum-effective-edit rule** to [../references/editing-guidelines.md](../references/editing-guidelines.md) Part IV, including the requirement to name the problem before changing a sentence. (REG-10)
2. **Added "Do not add transitions merely to smooth the surface"** to the mandatory principles. (REG-04)
3. **Clarified that parallelism applies to items meant to be compared**, not to deliberate rhetorical breaks, in [../references/sentence-structure.md](../references/sentence-structure.md) §11. (REG-11)
4. **Added a reverse-direction check** for added claims in [meaning-preservation.md](meaning-preservation.md) §3 step 5. (REG-08, REG-12)
5. **Made register preservation explicit for high-consequence text** in [../references/context-awareness.md](../references/context-awareness.md) §7 and [../modes/academic.md](../modes/academic.md). (REG-05)
6. **Added the diagnostic-output exception** to short-sentence guidance in [../modes/technical.md](../modes/technical.md). (REG-01)
7. **Added a synonym-drift example** to [../references/vocabulary-analysis.md](../references/vocabulary-analysis.md) §5. (REG-03)
8. **Added the voice-preservation checklist** to [quality-checklist.md](quality-checklist.md) §G. (REG-09)

---

## 4. How to run these tests in future

1. Take the input text exactly as written.
2. Apply the relevant mode and the editing workflow.
3. Compare the output with the failure signature. If the output resembles the failure, the guidance or the application failed.
4. Compare the output with the pass criteria.
5. If a revision is legitimate but differs from the expected behavior, record why. The cases are not meant to enforce a single answer; they are meant to catch predictable failures.

**Do not** score these cases by counting changes. A case passes when the text remains correct, appropriate, and meaning-preserving — including when the correct edit is no edit at all.

---

## 5. Coverage map

| Skill area | Cases |
|---|---|
| Minimum effective edit | REG-01, REG-10 |
| Technical accuracy | REG-02, REG-04 |
| Terminology | REG-03 |
| Register | REG-05, REG-06 |
| Specificity | REG-07, REG-08 |
| Voice | REG-09, REG-11 |
| Evidence and conclusions | REG-12 |
| Meaning preservation | REG-02, REG-07, REG-08, REG-12 |

Back to [SKILL.md](../SKILL.md).
