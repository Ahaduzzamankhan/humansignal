# English Examples

Version 2.1.0 · Human Signal

Forty worked examples of general English editing. Each entry follows the same seven-part structure: original, identified issues, linguistic analysis, explanation, revised version, improvements, and a meaning-preservation assessment.

The revisions are not the only correct answers. They demonstrate a method: locate the problem, explain its effect, make the smallest change that fixes it, and verify that meaning survived.

**All texts are constructed for illustration.** Names, numbers, versions, and commands are hypothetical. Before publishing a revision, replace every illustrative figure with verified data from the writer's source.

Related: [../references/ai-writing-patterns.md](../references/ai-writing-patterns.md) · [../references/editing-guidelines.md](../references/editing-guidelines.md) · [../tests/meaning-preservation.md](../tests/meaning-preservation.md)

---

## GEN-01 — Landscape opening

**Original:** "In today's rapidly evolving digital landscape, businesses must adapt or risk falling behind."

**Issues:** Formulaic era framing; false dilemma; no subject-specific content.

**Analysis:** The sentence has an abstract temporal frame ("today's rapidly evolving digital landscape") and a binary threat ("adapt or risk falling behind"). Neither term is defined, and the claim would fit any business document.

**Explanation:** The opening delays the actual subject and asserts a trend the text has not established. The either/or framing also removes middle options, such as adapting slowly or not at all.

**Revised:** "Three of our four payment providers will retire their legacy APIs this year, so checkout needs a migration plan."

**Improvements:** A dated, specific condition replaces the trend claim. The stakes are concrete, and the sentence creates a real reason to keep reading.

**Meaning preserved:** Yes, at a narrower scope. The original claimed a general need to adapt; the revision makes that need specific. If the writer intended the general claim, it would require evidence and a defined audience.

---

## GEN-02 — Adjective stacking

**Original:** "Our platform is a powerful, flexible, scalable, and secure solution for modern teams."

**Issues:** Four evaluative adjectives; "solution" as an empty category noun; "modern" as a mood word.

**Analysis:** Each adjective asserts a quality without naming the property that produces it. "Secure" against what threat? "Scalable" in which dimension? The sentence is grammatically sound and informationally empty.

**Explanation:** The reader cannot compare the platform with alternatives, because none of the claims can be checked. Stacking also dilutes each adjective: four claims receive the emphasis of none.

**Revised:** "The platform runs each tenant's workloads in a separate namespace, encrypts stored objects with per-tenant keys, and adds capacity by starting another worker."

**Improvements:** Isolation, encryption, and scaling become observable behaviors. The reader can now judge fit.

**Meaning preserved:** Partly. The original's four qualities are represented by three mechanisms; "flexible" has no direct equivalent because it was never defined. The writer should confirm which behavior "flexible" referred to.

---

## GEN-03 — Contrastive negation

**Original:** "This isn't just a text editor. It's a complete writing environment."

**Issues:** "Not X but Y" construction; undefined category ("complete writing environment"); implied superiority.

**Analysis:** The first sentence denies a modest category, and the second substitutes a grander but vaguer one. The rhetorical move creates emphasis by reclassification rather than by describing capability.

**Explanation:** The reader learns that the product is more than an editor, but not what it does. The contrast is doing the work that a feature description should do.

**Revised:** "The editor tracks changes across files, runs a spell check on save, and exports to DOCX without a plugin."

**Improvements:** Three concrete capabilities replace the category shift. The reader can decide whether these matter.

**Meaning preserved:** Yes, if the product does these things. The original's implication of breadth is replaced by specifics; if the writer meant a broader claim, it needs support.

---

## GEN-04 — Rule of three everywhere

**Original:** "The update improves speed, reliability, and usability, and it makes the product better, faster, and easier to use."

**Issues:** Two three-item lists; the second restates the first; "better" and "easier" are undefined.

**Analysis:** The sentence contains six evaluative claims arranged in parallel triads. Only three concepts are named, and each is repeated in different words.

**Explanation:** The triadic rhythm creates an impression of completeness, but the second list adds no information. The reader still does not know what changed.

**Revised:** "The update cuts cold-start time from 4.1 s to 1.8 s and removes the dialog that blocked first-run setup."

**Improvements:** Two measurable changes replace six adjectives. The list length now follows the content.

**Meaning preserved:** Partly. Speed and usability are represented; "reliability" is not addressed. The writer should add the reliability change or drop the claim.

---

## GEN-05 — The summary echo

**Original:** "In conclusion, we have discussed the causes of the outage, the effects on customers, and the steps taken to prevent recurrence."

**Issues:** Pure recap; no consequence, decision, or remaining risk.

**Analysis:** The sentence lists the document's sections in order and adds nothing. Every noun phrase refers to content already presented.

**Explanation:** A reader who has finished the report learns nothing. The conclusion occupies the position of greatest emphasis with the least information.

**Revised:** "The outage came from a certificate that expired during a holiday freeze. Certificates now renew 30 days before expiry, and the on-call runbook includes a manual renewal step."

**Improvements:** The conclusion states cause, fix, and residual procedure, so it functions as a closing argument rather than a table of contents.

**Meaning preserved:** Yes, and it adds specificity that the summary omitted. If the report did not contain these facts, the revision would be invalid.

---

## GEN-06 — Additive transition chain

**Original:** "Furthermore, the service supports retries. Moreover, it supports timeouts. Additionally, it supports circuit breaking."

**Issues:** Three additive connectors in three sentences; three short parallel clauses; no relationship beyond listing.

**Analysis:** Each sentence has the same shape and adds one capability. The connectors all mean "also," so they carry no distinct logical information.

**Explanation:** The reader receives a list disguised as an argument. The transitions suggest development where there is only enumeration.

**Revised:** "The service retries failed calls, enforces per-request timeouts, and opens a circuit after five consecutive failures."

**Improvements:** One sentence, parallel verbs, and a specific threshold. The list is now visibly a list.

**Meaning preserved:** Yes. The revision adds the threshold "five," which must be verified; if unknown, "after repeated failures" would preserve the original's vagueness.

---

## GEN-07 — Unquantified improvement

**Original:** "The new onboarding flow significantly improves the user experience."

**Issues:** "Significantly" with no measure; "user experience" as an undefined construct; no baseline.

**Analysis:** The sentence asserts a change in a broad quality without a metric, a comparison, or a timeframe. "Significantly" may imply statistical significance without saying so.

**Explanation:** The reader cannot tell whether the change is large, small, or measured at all. The claim is unfalsifiable as written.

**Revised:** "The new onboarding flow cuts setup from nine screens to four; completion within one session rose from 61% to 78% in the first month."

**Improvements:** Baseline, mechanism, and outcome are all present. "Significantly" is replaced by numbers that speak for themselves.

**Meaning preserved:** Yes, if the figures are the writer's. If no measurement exists, the honest revision is: "The flow now uses four screens instead of nine; completion data is not yet available."

---

## GEN-08 — Both-sides reflex

**Original:** "Some people believe remote work is more productive, while others believe offices are better. Both sides make valid points."

**Issues:** False balance; unnamed groups; "valid points" without content.

**Analysis:** Two positions are set against each other with no evidence, criteria, or consequence. The closing sentence affirms both without saying what either claims.

**Explanation:** The reader finishes the paragraph without knowing what the evidence shows or how to decide. Balance has replaced analysis.

**Revised:** "Remote work raises individual output for focused tasks but weakens spontaneous coordination; the teams that struggled most were those shipping interdependent work across time zones."

**Improvements:** The trade-off is specific and conditional. The reader learns where each mode helps.

**Meaning preserved:** Yes in substance, but the revision takes a position the original avoided. If neutrality was required, the writer should present the evidence for each side and the criteria for choosing.

---

## GEN-09 — Rhetorical question stack

**Original:** "What if you could ship faster? What if your team never missed a deadline? What if deployment felt effortless?"

**Issues:** Three hypothetical questions; no answers; "effortless" as an absolute.

**Analysis:** The questions share a frame ("What if…") and promise benefits without mechanism. Each implies a product claim that is never stated.

**Explanation:** The pattern withholds information to create desire, which is appropriate in advertising and out of place in explanatory prose. The reader cannot evaluate a promise that has no content.

**Revised:** "Deployments currently take 40 minutes and fail 12% of the time, mostly at the database migration step."

**Improvements:** A measured problem replaces three hypothetical benefits, and it points to a cause the reader can act on.

**Meaning preserved:** No direct equivalence. The original made promises; the revision describes a problem. This is a deliberate change of function and must be confirmed with the writer.

---

## GEN-10 — Causal prose converted to bullets

**Original:**
> - The cache expired.
> - Requests hit the database.
> - The pool saturated.
> - Latency rose.

**Issues:** A causal chain presented as independent items; fragments; no connectors.

**Analysis:** Each bullet is a clause, and the sequence is chronological, but the list format implies four separate facts. The causal relation exists only in the reader's inference.

**Explanation:** Lists are for parallel items. When items depend on each other, the format hides the logic and invites misreading.

**Revised:** "When the cache expired, requests reached the database, saturated the connection pool, and pushed latency up."

**Improvements:** One sentence makes the chain explicit. The reader no longer has to reconstruct causality.

**Meaning preserved:** Yes. No fact is added or removed.

---

## GEN-11 — Bureaucratic phrasing

**Original:** "Please be advised that, in the event that the requested documentation is not received by the stipulated deadline, the application shall be subject to closure."

**Issues:** Nominalization ("closure"), passive construction, triple conditional frame, legalistic register in a routine notice.

**Analysis:** The sentence contains one instruction: send the document by the deadline or the application closes. Most of its length comes from formulaic frames.

**Explanation:** The register creates distance and slows comprehension without adding legal precision. A plain sentence would be equally binding in most contexts.

**Revised:** "Send the requested documents by 30 June. If they arrive later, we will close the application."

**Improvements:** The action, deadline, and consequence are explicit. The register matches a routine administrative notice.

**Meaning preserved:** Yes, except "subject to closure" allowed discretion; the revision states closure as certain. If discretion is intended, write "we may close the application."

---

## GEN-12 — Nominalization chain

**Original:** "The implementation of the optimization of the allocation process resulted in an improvement in performance."

**Issues:** Three nominalizations; "improvement in performance" undefined; no actor.

**Analysis:** The actions are buried in nouns: implement, optimize, allocate, improve. The only finite verb is "resulted," which carries no content.

**Explanation:** The sentence hides who did what and turns a process into an abstraction. The reader must unpack three layers to find the event.

**Revised:** "We changed how the scheduler allocates memory, and the service now handles 20% more requests per second."

**Improvements:** Actors and actions are visible, and the result is measurable.

**Meaning preserved:** Partly. "Optimization" is now a specific change (scheduler allocation); the writer must confirm that this was the optimization. The performance figure is illustrative and must be supplied.

---

## GEN-13 — Hedge stacking

**Original:** "It could possibly be argued that the proposed approach may potentially offer some benefits in certain situations."

**Issues:** Four hedges; passive frame; "some benefits" undefined; "certain situations" unspecified.

**Analysis:** The sentence contains five uncertainty markers and no content. The one proposition — the approach may help — is buried under qualifications that do not identify what is uncertain.

**Explanation:** Stacked hedges make the writer sound unsure of everything, including the existence of the claim. The reader cannot tell what is believed or what would count as evidence.

**Revised:** "The approach reduced error rates in the two small datasets tested. It has not been evaluated at production scale."

**Improvements:** The finding and its limit are both explicit. Uncertainty is located rather than spread across the sentence.

**Meaning preserved:** Yes, if the finding is accurate. The original's caution is retained as a specific scope statement.

---

## GEN-14 — Synonym drift

**Original:** "Each tenant's data is isolated. The customer's records are stored separately. The account's information is partitioned by organization."

**Issues:** Four terms for one entity (tenant, customer, account, organization); three verbs for one operation (isolated, stored separately, partitioned).

**Analysis:** The paragraph varies vocabulary to avoid repetition, but the variation implies distinctions that do not exist. The reader must decide whether these are four entities or one.

**Explanation:** In technical and business writing, a stable term is a feature. Synonym rotation damages reference tracking and can create legal or architectural ambiguity.

**Revised:** "Each tenant's data is stored in a separate partition, keyed by `tenant_id`."

**Improvements:** One term, one mechanism, one key. The reader can now look up the implementation.

**Meaning preserved:** Yes, assuming the three original sentences described the same mechanism. If they described different layers (logical isolation, physical storage, partitioning), the revision would collapse a real distinction and should not be made.

---

## GEN-15 — Obvious consequence

**Original:** "The migration removes the old table, which means the old table will no longer exist."

**Issues:** Tautology; relative clause restating the main clause.

**Analysis:** "Removes" already entails "will no longer exist." The second clause adds no information and no condition.

**Explanation:** The sentence treats the reader as unable to infer the consequence of deletion. It also misses the consequence that actually matters: queries or jobs that still reference the table will fail.

**Revised:** "The migration drops the `legacy_events` table; any job still querying it will fail until it is updated."

**Improvements:** The real operational consequence replaces the tautology.

**Meaning preserved:** Yes, and it adds a consequence the original omitted. If that consequence is not true for this system, the revision must be adjusted.

---

## GEN-16 — Process narration

**Original:** "I will now walk you through the three main factors that influence the outcome. First, I will explain the first factor."

**Issues:** Meta-commentary; announcement of an announcement; "first factor" with no content.

**Analysis:** Two sentences describe the text's plan without executing it. The reader learns the number of factors but not what they are.

**Explanation:** Narration adds a layer between the reader and the content. It is appropriate in a live walkthrough, where the audience watches the process, and unnecessary in written prose.

**Revised:** "Three factors drive the outcome: queue depth, retry policy, and database contention."

**Improvements:** The content arrives immediately, and the list is specific.

**Meaning preserved:** Yes. The structure is preserved without the announcement.

---

## GEN-17 — Em dash overload

**Original:** "The service — which handles payments — retries failed calls — up to three times — before alerting the team — usually within a minute."

**Issues:** Four em dashes; nested asides; a sentence that cannot be read linearly.

**Analysis:** Each dash pair introduces a different kind of material: a relative clause, a quantity, a temporal qualifier. The reader must track which aside is open and which has closed.

**Explanation:** Dashes are strong marks; using them repeatedly turns emphasis into noise. Parentheses or commas would distinguish the levels.

**Revised:** "The service retries failed payment calls up to three times, then alerts the team, usually within a minute."

**Improvements:** The asides are integrated or removed. The sentence reads in one pass.

**Meaning preserved:** Yes. The parenthetical "which handles payments" is folded into "payment calls."

---

## GEN-18 — Passive voice hiding responsibility

**Original:** "The configuration was changed, and as a result, the outage occurred."

**Issues:** Two passives; no actor; causal link asserted without mechanism.

**Analysis:** Nobody changed the configuration, and nothing caused the outage; both events appear without agents. The causal claim is grammatical but unattributed.

**Explanation:** In an incident report, the actor and the mechanism are the information the reader needs. Passive voice here protects nobody and informs nobody.

**Revised:** "An engineer changed the replica count from 3 to 1 during the maintenance window. With one replica, the remaining node could not absorb the traffic, and the service returned 503s for four minutes."

**Improvements:** Actor, change, mechanism, and duration are all explicit.

**Meaning preserved:** Yes, if these are the facts. The revision is more specific; the writer must confirm the values.

---

## GEN-19 — Generic example

**Original:** "For example, a company might want to improve its processes to become more efficient."

**Issues:** Placeholder company; "processes" and "efficient" undefined; no mechanism.

**Analysis:** The example instantiates nothing. It restates the general goal in slightly more concrete words but supplies no case the reader can map onto their situation.

**Explanation:** An example earns its place by showing a specific instance where a general rule applies, including the conditions and the result.

**Revised:** "A four-person billing team that reconciles invoices by hand each month can import the bank feed instead, which removes about 20 hours of manual matching."

**Improvements:** Team size, task, alternative, and effect are present.

**Meaning preserved:** Yes, at the cost of specificity the original lacked. If the writer's example was about a different process, the revision should use that process.

---

## GEN-20 — Definition spiral

**Original:** "Idempotency means the property of being idempotent, which is to say that an operation that is idempotent produces the same result when repeated."

**Issues:** Circular definition; nested gloss; no example or consequence.

**Analysis:** "Idempotent" is defined by "idempotency," which is defined by "idempotent." The only new information is "produces the same result when repeated," which is then not illustrated.

**Explanation:** The reader who does not know the term still does not know it. The definition substitutes morphological variation for explanation.

**Revised:** "An idempotent request can be retried safely: sending the same payment twice returns the first charge instead of creating a second one."

**Improvements:** A consequence and an example replace the circle.

**Meaning preserved:** Yes. The definition is narrower than the mathematical one (which concerns function composition), so the revision should note that it describes the API sense.

---

## GEN-21 — Section recap

**Original:** "In this section, we have seen how the scheduler assigns jobs to workers and how it handles retries."

**Issues:** Recap that restates the heading and the section; no consequence.

**Analysis:** The sentence names the section's two topics without adding a finding. It is the textual equivalent of a page number.

**Explanation:** Recaps are useful when a reader may have skipped or when the section is long enough to need consolidation. Here the heading already performed the navigation.

**Revised:** (Delete the sentence and end the section on the last substantive finding.)

**Improvements:** Removing the recap shortens the document and lets the final finding carry the emphasis.

**Meaning preserved:** Yes; no information is removed.

---

## GEN-22 — Bold inflation

**Original:** "**Important:** You **must** **always** **verify** that the **configuration** is **correct** before **deploying**."

**Issues:** Seven bold spans in one sentence; emphasis distributed across function words and content words alike.

**Analysis:** Bold is applied to the modal, the adverb, the verb, the noun, and the adjective. When every word is emphasized, the formatting carries no hierarchy.

**Explanation:** Emphasis should mark the one thing the reader must not miss. Multiple marks compete, and the reader's eye has no path.

**Revised:** "Verify the configuration before deploying. A mismatched `region` value causes every request to fail with 403."

**Improvements:** The instruction is plain, and the consequence explains why it matters. No bold is needed.

**Meaning preserved:** Yes. The obligation ("must") remains as an imperative.

---

## GEN-23 — Subject-first monotone

**Original:** "The parser reads the file. The parser builds an abstract syntax tree. The parser reports errors. The parser writes the output."

**Issues:** Four sentences with identical subject and frame; four separate events in one process.

**Analysis:** The repeated subject creates a chant and makes each step feel independent. In fact, the steps form a pipeline with a shared actor.

**Explanation:** When several sentences share a subject and describe one process, a single clause chain is usually clearer. The repetition is not wrong grammar; it is a structure that obscures the flow.

**Revised:** "The parser reads the file, builds an abstract syntax tree, reports any errors, and writes the output."

**Improvements:** The pipeline is visible, and the shared subject appears once.

**Meaning preserved:** Yes. The order of operations is unchanged.

---

## GEN-24 — Artificial paragraph symmetry

**Original:** Three paragraphs of exactly five sentences each: a definition of caching, a list of three benefits, and a closing sentence beginning "Ultimately."

**Issues:** Identical paragraph length and internal shape; a conclusion that repeats the benefits.

**Analysis:** The layout assigns equal space to a definition, an argument, and a summary. The symmetry is visual rather than logical.

**Explanation:** Paragraph length signals importance. When every paragraph is the same size, the reader cannot tell which idea carries the argument.

**Revised:** A two-sentence definition, a longer paragraph with the mechanism and its cost, and a single-sentence caveat about invalidation.

**Improvements:** Space now tracks weight, and the caveat has its own emphasis.

**Meaning preserved:** Yes, if the same content is retained. The revision changes distribution, not claims.

---

## GEN-25 — Redundant doublet

**Original:** "The final end result was a complete and total success."

**Issues:** "Final end," "complete and total," "success" undefined.

**Analysis:** Two pairs of synonyms and one evaluative noun. The sentence contains no verifiable claim.

**Explanation:** Redundant doublets suggest the writer is reaching for emphasis because the content is thin. The revision must supply the missing criterion for success.

**Revised:** "The release shipped on 14 March with no rollbacks in the first week."

**Improvements:** A date and an operational criterion replace three abstractions.

**Meaning preserved:** Partly. The original claimed success without defining it; the revision defines it. If the writer's criterion was different, the revision should use theirs.

---

## GEN-26 — Moral-of-the-story conclusion

**Original:** "This shows that teamwork is always the key to success."

**Issues:** Universal claim from a single case; "always"; "key" and "success" undefined.

**Analysis:** The sentence generalizes from an unspecified case to all cases. No mechanism, condition, or counterexample is offered.

**Explanation:** The moral overreaches the evidence and repeats a lesson the reader already knows. It closes the text without advancing it.

**Revised:** "Pairing a new engineer with a reviewer for the first two pull requests cut rework in this team; whether the practice helps larger teams is untested."

**Improvements:** The finding is bounded by setting and mechanism, and the limit is explicit.

**Meaning preserved:** Partly. The original's universal claim is deliberately narrowed; that change must be disclosed.

---

## GEN-27 — Unnamed authority

**Original:** "Studies show that most teams waste a significant amount of time in meetings."

**Issues:** "Studies show" with no citation; "most teams" undefined; "significant" unquantified.

**Analysis:** The sentence cites an unnamed body of research and a universal population. Neither can be checked, and "significant" may or may not be statistical.

**Explanation:** Appeal to authority without a source is not evidence. It also makes the claim sound stronger than the writer may be able to support.

**Revised:** "In the 2023 survey of 1,200 knowledge workers, respondents reported spending 6.5 hours a week in status meetings and rated half of that time as duplicative. The sample was self-selected."

**Improvements:** Source, sample, measure, and limitation are present.

**Meaning preserved:** No, unless these are the studies the writer meant. If the source is unknown, the honest revision is: "Many teams report meeting overload; no reliable estimate is cited here."

---

## GEN-28 — Scope-free universal

**Original:** "Microservices always improve scalability."

**Issues:** "Always"; "improve" without a measure; "scalability" undefined.

**Analysis:** The claim covers every system, every workload, and every implementation. It would be refuted by one counterexample.

**Explanation:** Universals are rarely true in engineering, where outcomes depend on workload, team size, and operational maturity. The sentence also omits the costs of distribution.

**Revised:** "Splitting the image service from the API let each scale independently; the gain appeared only after image traffic exceeded API traffic."

**Improvements:** The condition that produced the benefit is named, and the claim is bounded.

**Meaning preserved:** Partly. The original claimed a universal; the revision reports a case. The change in scope must be intentional.

---

## GEN-29 — Prestige comparison

**Original:** "We're building the Stripe of internal tooling."

**Issues:** Analogy as description; borrowed credibility; no mechanism.

**Analysis:** The comparison names a company and a market position, not a product property. The reader must already know Stripe's model to decode the sentence.

**Explanation:** Prestige analogies orient investors quickly but tell users nothing about what the product does. They also invite unflattering comparisons.

**Revised:** "We provide one API for internal teams to charge other departments, with usage metering, monthly invoicing, and a reconciliation report."

**Improvements:** The function and the three core capabilities replace the analogy.

**Meaning preserved:** Yes, if the product does these things. The analogy may still be useful in a pitch deck, where shorthand has a purpose; it should not stand alone.

---

## GEN-30 — Overloaded sentence

**Original:** "Although the service, which was deployed on Tuesday after a delay caused by a failed security review that had already been rescheduled twice, performed well under load, it failed the next morning when the certificate expired, which the team had not anticipated."

**Issues:** Three nested relative clauses; two main events; unclear emphasis.

**Analysis:** The sentence contains a deployment, a review history, a load result, a certificate failure, and an expectation. The main clause ("it failed") is buried after 40 words of background.

**Explanation:** The reader must hold the deployment history in memory to reach the failure. The sentence is grammatical but poorly prioritized.

**Revised:** "The service was deployed on Tuesday after a security review that had been rescheduled twice. It handled the load test, then failed the next morning when its certificate expired."

**Improvements:** Two sentences separate background from event, and the failure is no longer subordinate.

**Meaning preserved:** Yes. The details are retained; only the packaging changes.

---

## GEN-31 — Fragments for drama

**Original:** "The migration took six months. Six months of planning. Six months of testing. Six months of waiting. Then it failed."

**Issues:** Four fragments; repetitive anaphora; "failed" without a cause.

**Analysis:** The repetition builds a rhythm, but the fragments carry no new information after the first. The final sentence delivers a result with no mechanism.

**Explanation:** Deliberate fragments can create emphasis, but here the device substitutes for detail. The reader learns that the migration was long and failed, not why.

**Revised:** "The migration took six months, mostly because two services shared a database. The team split them first, then moved the remaining tables. The cutover failed when the replication lag exceeded the maintenance window."

**Improvements:** Duration, cause, sequence, and failure mechanism are present.

**Meaning preserved:** Yes, assuming the causes are accurate. The revision removes the rhetorical repetition deliberately.

---

## GEN-32 — Label-description repetition

**Original:** "**Performance:** The system's performance is fast. **Reliability:** The system is reliable. **Security:** The system is secure."

**Issues:** Each label is restated as an adjective; no evidence; "fast," "reliable," "secure" undefined.

**Analysis:** The pattern "Label: category adjective" produces three tautologies. The labels promise information that the descriptions do not deliver.

**Explanation:** The format implies a structured comparison, but each line is empty. The reader cannot evaluate any claim.

**Revised:** "**Performance:** p95 response time is 180 ms at 500 requests per second. **Reliability:** 99.95% availability over the last 12 months, with two incidents. **Security:** AES-256 at rest, TLS 1.3 in transit, and per-tenant keys."

**Improvements:** Each label receives a measurable property.

**Meaning preserved:** Yes, if the figures are real. The structure is retained because it aids scanning.

---

## GEN-33 — Unnecessary disclaimer

**Original:** "This is not professional advice, and results may vary. Please consult a professional before making any decisions."

**Issues:** Generic disclaimer; no identified risk; no scope; "professional" undefined.

**Analysis:** The disclaimer could accompany any advice on any subject. It does not tell the reader which decisions are risky or which professional to consult.

**Explanation:** Blanket disclaimers transfer responsibility without informing. Readers learn to skip them, which weakens the disclaimers that matter.

**Revised:** "These thresholds assume a single-server deployment. Above roughly 10,000 writes per second, the locking scheme needs a different design; benchmark before committing."

**Improvements:** The limitation is specific and tied to the advice.

**Meaning preserved:** Yes, and it is more useful. A formal disclaimer may still be required by the publisher; place it once, separately.

---

## GEN-34 — Forced engagement close

**Original:** "So, what are you waiting for? Start optimizing your workflow today!"

**Issues:** Rhetorical question; imperative with no action; "optimizing" undefined.

**Analysis:** The closing creates urgency without saying what to do first. "Optimize your workflow" is a goal, not an action.

**Explanation:** The question and exclamation simulate a sales close. In instructional writing, the reader needs a first step, not encouragement.

**Revised:** "Start by timing one recurring task for a week; the longest task is usually the best candidate for automation."

**Improvements:** A concrete first step replaces the call to action.

**Meaning preserved:** Partly. The promotional function is removed; the instructional function is added.

---

## GEN-35 — Mixed register

**Original:** "The present study examines the aforementioned phenomena. We'll dig into the data and see what pops out."

**Issues:** Formal academic frame followed by chatty idiom; inconsistent person and contraction.

**Analysis:** The first sentence uses nominalization and "aforementioned"; the second uses a contraction and two idioms. The register shifts within two sentences.

**Explanation:** The reader cannot tell what kind of text this is. The shift may be an attempt at accessibility, but it is unmarked and abrupt.

**Revised:** "This study examines the three phenomena described above. The analysis focuses on the two datasets with complete records."

**Improvements:** One register, explicit reference, and a specific scope.

**Meaning preserved:** Yes. The informal sentence's actual content ("look at the data") is replaced by a precise description of the analysis.

---

## GEN-36 — Dangling modifier

**Original:** "After reviewing the logs, the error was caused by a timeout."

**Issues:** Dangling participle; the error did not review the logs; causal claim without agent.

**Analysis:** The introductory phrase modifies the subject of the main clause, which is "the error." The sentence therefore says the error reviewed the logs.

**Explanation:** The grammatical error obscures who performed the action. It also leaves the cause unattributed.

**Revised:** "After reviewing the logs, we found that a timeout caused the error."

**Improvements:** The actor is restored, and the causal finding is attributed.

**Meaning preserved:** Yes. The revision makes explicit who reviewed the logs.

---

## GEN-37 — Faulty parallelism

**Original:** "The role requires writing documentation, to review pull requests, and good communication."

**Issues:** Gerund, infinitive, and noun phrase in one list; the third item is not an action.

**Analysis:** The three items are grammatically different, so the list cannot be read as a set. "Good communication" is a quality, not a task.

**Explanation:** The reader cannot tell whether the role requires three activities or two activities and a personal attribute. Parallel form would make the list a set of comparable requirements.

**Revised:** "The role requires writing documentation, reviewing pull requests, and communicating decisions to the team."

**Improvements:** Three gerunds; each item is an activity.

**Meaning preserved:** Yes. "Good communication" becomes a specific communicative act; the writer may prefer "communicating clearly with stakeholders."

---

## GEN-38 — Ambiguous pronoun

**Original:** "The service calls the API, then it retries if it fails."

**Issues:** Two "it" pronouns with three possible referents (service, API, call); "fails" unclear.

**Analysis:** The reader cannot tell what is retried or what condition triggers the retry. The sentence is short and still ambiguous.

**Explanation:** Pronoun ambiguity is common in technical prose because several nouns share the same gender and number. Repetition is the fix, not variation.

**Revised:** "The service calls the API. If the call returns a 5xx response, the service retries it twice."

**Improvements:** Each referent is named, and the failure condition is specified.

**Meaning preserved:** Yes, if the retry condition was a 5xx. If it was a timeout, substitute that condition.

---

## GEN-39 — Nested list cascade

**Original:**
> - Configuration
>   - Database
>     - Host
>       - The hostname of the database server

**Issues:** Four levels for one value; each level has one child; indentation carries no information.

**Analysis:** The hierarchy implies a taxonomy, but each parent has a single child, so the levels are decorative.

**Explanation:** Deep nesting is hard to read and suggests structure that does not exist. A table or a single line would be clearer.

**Revised:** "`database.host` — hostname of the database server (default: `localhost`)."

**Improvements:** One line carries the path, the meaning, and the default.

**Meaning preserved:** Yes, and it adds the default if one exists.

---

## GEN-40 — Polished but empty

**Original:** "By harnessing the power of cutting-edge technology, organizations can unlock unprecedented opportunities and drive meaningful transformation across every dimension of their operations."

**Issues:** Three metaphors ("harnessing," "unlock," "drive"); "unprecedented," "meaningful," "every dimension" undefined; no agent, mechanism, or example.

**Analysis:** Every content word is abstract. The sentence could describe any technology applied to any organization.

**Explanation:** The polish is the problem: the sentence sounds authoritative while saying nothing. A reader cannot act on it or disagree with it.

**Revised:** "Automating invoice matching cut the accounting team's month-end close from nine days to four."

**Improvements:** A specific technology, a specific task, and a measured result.

**Meaning preserved:** No. The original made a general promise; the revision reports a case. The writer must decide which claim they can support.

---

## Cross-example observations

1. **Vagueness cannot be edited into specificity without information.** Several revisions above narrow the original claim. That is a meaning change and must be disclosed, not smuggled in.
2. **The smallest fix is often deletion.** Recaps, restatements, and tautologies usually need no replacement.
3. **Terminology is not repetition.** The examples that fixed synonym drift restored a single term rather than inventing variety.
4. **Numbers do the work that adjectives pretend to do.** Where a figure was available, it replaced evaluation.
5. **Meaning preservation is a separate check.** A revision can read better and still fail the preservation test.

See [academic-examples.md](academic-examples.md), [technical-examples.md](technical-examples.md), and [conversational-examples.md](conversational-examples.md).

Back to [SKILL.md](../SKILL.md).
