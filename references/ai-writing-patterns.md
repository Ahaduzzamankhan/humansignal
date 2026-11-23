# AI Writing Patterns: A Working Encyclopedia

Version 2.1.0 · Human Signal

## How to use this file

This file documents 120 recurring writing-pattern observations, grouped into 30 categories of four entries each. Every entry has the same structure so that a reviewer can compare one observation with another and apply the same standard.

A pattern in this encyclopedia is a **signal to inspect**, not a verdict. None of these features proves that a text was written by a machine. Most of them occur in human writing, and several are correct in the right context. The question is always whether the feature serves the text's purpose, audience, and meaning.

Read the entry's *Recognition criteria* line before acting. If the condition does not hold, the pattern is not present. Read the *Appropriate exceptions* line before editing. If the exception applies, leave the text alone.

See also: [natural-language-principles.md](natural-language-principles.md), [editing-guidelines.md](editing-guidelines.md), [detector-reliability.md](detector-reliability.md).

---

## 1. Formulaic introductions

### AWP-001 — The landscape opening
**Category:** Formulaic introductions
**Description:** The text opens with a broad statement about an era, trend, or "landscape" before reaching its actual subject.
**Linguistic characteristics:** Present-tense generalization ("In today's…"), abstract nouns such as *world*, *age*, *landscape*; no concrete referent; often a colon that finally introduces the topic.
**Why it can weaken writing:** It delays the point, asserts a trend the writer has not established, and would fit almost any document on the same subject.
**Recognition criteria:** Delete the first sentence. If no information is lost, it was framing rather than content.
**Original example:** "In today's fast-paced digital landscape, developers face more choices than ever before."
**Improved example:** "A new project usually has three viable build tools, and each one changes the deployment story."
**Explanation of improvement:** The revision names the subject and a concrete condition, so the first line carries information.
**Appropriate exceptions:** A trend claim is appropriate when the trend is the topic and the next paragraph supports it with evidence.

### AWP-002 — The importance announcement
**Category:** Formulaic introductions
**Description:** The opening asserts that the topic is important, critical, or increasingly relevant instead of showing why.
**Linguistic characteristics:** Phrases such as "plays a crucial role," "has become increasingly important," "is essential to understand"; no actor, no mechanism, no consequence.
**Why it can weaken writing:** Importance is a conclusion. Asserting it up front asks the reader to accept the thesis before seeing the argument.
**Recognition criteria:** Ask what would change if the claim were false. If the answer is "nothing in the text," the sentence is decoration.
**Original example:** "Data security plays a crucial role in modern software development."
**Improved example:** "A single leaked API key can expose every customer record the service stores, which is why key rotation belongs in the deployment checklist."
**Explanation of improvement:** It replaces a ranking adjective with a mechanism and a consequence.
**Appropriate exceptions:** A brief importance statement is conventional in grant proposals and funding requests, where the audience expects a framing paragraph.

### AWP-003 — The dictionary definition opening
**Category:** Formulaic introductions
**Description:** The text begins by defining a common term in general terms before addressing the specific question.
**Linguistic characteristics:** "X is defined as…", "By definition, X refers to…", often followed by a restatement of everyday knowledge.
**Why it can weaken writing:** It spends the reader's attention on shared knowledge and postpones the part that is specific to this document.
**Recognition criteria:** Would the intended reader already know the definition? If yes, it is filler.
**Original example:** "Artificial intelligence, broadly defined, refers to the simulation of human intelligence by machines."
**Improved example:** "The classifier assigns each support ticket one of nine categories, and it mislabels billing questions most often."
**Explanation of improvement:** It starts at the level of detail the audience needs rather than at the level of a glossary.
**Appropriate exceptions:** Defining a term is necessary when the document uses it in a nonstandard or disputed way.

### AWP-004 — The rhetorical scene-setting question
**Category:** Formulaic introductions
**Description:** The text opens with a question the reader did not ask, used to create momentum.
**Linguistic characteristics:** "Have you ever wondered…?", "What if…?", "Why does this matter?"; the answer arrives several sentences later.
**Why it can weaken writing:** It simulates engagement instead of providing it, and it delays the answer the reader came for.
**Recognition criteria:** Check whether the question is the document's actual research question. If not, it is staging.
**Original example:** "Have you ever stopped to think about how much time you waste in meetings?"
**Improved example:** "The team spends 6.5 hours a week in status meetings, and half of that time repeats information already in the tracker."
**Explanation of improvement:** The revision answers the implied question immediately with a measurable fact.
**Appropriate exceptions:** Questions work in reflective essays and opinion columns, where the reader has chosen a discursive form.

---

## 2. Formulaic conclusions

### AWP-005 — The summary echo
**Category:** Formulaic conclusions
**Description:** The final paragraph restates the introduction and body in the same order without adding a consequence, decision, or next step.
**Linguistic characteristics:** "In summary," "To sum up," followed by compressed repetition; no new information; similar length to the introduction.
**Why it can weaken writing:** A reader who has read the document learns nothing. The ending occupies space that could hold implications or action.
**Recognition criteria:** Cover the conclusion and ask what decision the reader can now make. If the answer was already available before the conclusion, the paragraph is redundant.
**Original example:** "In conclusion, we discussed the causes, effects, and possible solutions to the problem."
**Improved example:** "Because most delays trace back to the approval step, the team should move sign-off before staging rather than after."
**Explanation of improvement:** It converts summary into a recommendation grounded in the analysis.
**Appropriate exceptions:** Long reports and theses often require a formal summary chapter for readers who skim; keep it, but add the implication.

### AWP-006 — The uplift ending
**Category:** Formulaic conclusions
**Description:** The text closes on a general expression of optimism or possibility rather than a specific finding.
**Linguistic characteristics:** "The possibilities are endless," "the future looks bright," "only time will tell," "this is just the beginning."
**Why it can weaken writing:** It replaces the document's actual conclusion with mood, and it can imply outcomes the evidence does not support.
**Recognition criteria:** Does the sentence make a checkable claim? If not, ask whether the genre expects an emotional close.
**Original example:** "Ultimately, the future of renewable energy is full of exciting possibilities."
**Improved example:** "Storage costs fell 34% over four years, so the open question is no longer generation but overnight supply."
**Explanation of improvement:** It ends on the live uncertainty the analysis identified.
**Appropriate exceptions:** Commencement speeches, campaign material, and personal essays may legitimately end on aspiration.

### AWP-007 — The moral of the story
**Category:** Formulaic conclusions
**Description:** The ending extracts a universal lesson from a specific case, usually with "this shows that" or "the key takeaway is."
**Linguistic characteristics:** A leap from one case to a general principle; modal verbs of obligation; no boundary conditions.
**Why it can weaken writing:** It overgeneralizes and often repeats a lesson the reader already inferred.
**Recognition criteria:** Identify the population the lesson covers. If it is broader than the evidence, the sentence overreaches.
**Original example:** "This shows that teamwork is always the key to success."
**Improved example:** "Pairing a new engineer with a reviewer for the first two pull requests cut rework in this team; whether it transfers to larger teams is untested."
**Explanation of improvement:** It states the finding, its setting, and its limit.
**Appropriate exceptions:** Parables and opinion pieces use explicit morals by design; the audience expects the compression.

### AWP-008 — The truncated recommendation
**Category:** Formulaic conclusions
**Description:** The text ends by recommending "further research" or "more work" without naming the question, method, or owner.
**Linguistic characteristics:** "Further research is needed," "more studies should explore this area," no verb specific to the case.
**Why it can weaken writing:** It reads as an obligation to close rather than a direction, and it gives the next reader nothing to act on.
**Recognition criteria:** Ask what exactly should be studied and by whom. If the text cannot answer, the sentence is empty.
**Original example:** "Further research is needed to fully understand this complex topic."
**Improved example:** "A follow-up study should test whether the effect persists when reviewers see author names, which this design deliberately hid."
**Explanation of improvement:** It names the variable, the design change, and the reason.
**Appropriate exceptions:** A funding proposal may end with an agenda; even then, each item should be specific.

---

## 3. Repetitive transitions

### AWP-009 — The additive chain
**Category:** Repetitive transitions
**Description:** Paragraphs are linked by a rotating set of additive connectors that all mean "also."
**Linguistic characteristics:** *Furthermore*, *Moreover*, *Additionally*, *In addition*, *Besides* in close succession; sentence subjects unchanged.
**Why it can weaken writing:** Additive connectors imply a list, so the reader stops looking for relationships such as cause, contrast, or consequence.
**Recognition criteria:** Replace each connector with "and." If the sentence still reads correctly, the connector carried no logical weight.
**Original example:** "Furthermore, the API supports pagination. Moreover, it supports filtering. Additionally, it supports sorting."
**Improved example:** "The API paginates, filters, and sorts results; filtering happens before pagination, so page sizes stay stable."
**Explanation of improvement:** It merges a list, then adds the ordering fact that matters to callers.
**Appropriate exceptions:** In long procedural documents, explicit enumerative connectors help readers resume after interruption; keep them if they mark real steps.

### AWP-010 — The contrastive hinge overuse
**Category:** Repetitive transitions
**Description:** Nearly every paragraph turns on a contrast marker, producing a seesaw rhythm.
**Linguistic characteristics:** *However*, *Nevertheless*, *That said*, *On the other hand* opening successive paragraphs; each paragraph first concedes, then corrects.
**Why it can weaken writing:** Constant reversal makes the argument feel defensive and obscures which position the writer holds.
**Recognition criteria:** Count contrast markers per thousand words. If the rate is high, check whether the text actually contains that many reversals.
**Original example:** "However, the first approach is slow. That said, the second is complex. Nevertheless, the third is expensive."
**Improved example:** "All three approaches trade speed for complexity: the first is fastest to build, the third is fastest at runtime, and the second sits between them."
**Explanation of improvement:** A single comparative frame replaces three staged reversals.
**Appropriate exceptions:** A genuine literature review often contains many contrasts; the marker should still point to a real disagreement.

### AWP-011 — The signpost without a road
**Category:** Repetitive transitions
**Description:** The text announces what it will do before doing it, repeatedly.
**Linguistic characteristics:** "Let us now turn to…", "Having established X, we can examine Y", "This brings us to…"; the announcement adds a sentence without adding content.
**Why it can weaken writing:** It doubles the length of every structural move and treats navigation as substance.
**Recognition criteria:** Delete the sentence. If the following paragraph still makes sense in place, the signpost was unnecessary.
**Original example:** "Now that we have explored the background, let us move on to the methodology."
**Improved example:** "The study compared two review queues over eight weeks."
**Explanation of improvement:** The heading and the content perform the transition.
**Appropriate exceptions:** Spoken lectures and long technical reports benefit from occasional orientation, especially when readers jump between sections.

### AWP-012 — The mechanical sequencing
**Category:** Repetitive transitions
**Description:** Steps, causes, or points are numbered with ordinal transitions even when the relationship is not sequential.
**Linguistic characteristics:** *First*, *Second*, *Third* applied to unordered reasons; *Firstly*, *Secondly* in short prose; numbering that implies priority the text never justifies.
**Why it can weaken writing:** Ordinals assert order. When the items are parallel, the numbering misrepresents the structure.
**Recognition criteria:** Ask whether item three depends on item one. If not, the sequence is imposed.
**Original example:** "Firstly, the library is fast. Secondly, it is well documented. Thirdly, it is maintained."
**Improved example:** "The library is fast, well documented, and actively maintained."
**Explanation of improvement:** The items are parallel properties, so a list is more accurate than a sequence.
**Appropriate exceptions:** Genuine procedures, ranked findings, and legal clauses need explicit numbering.

---

## 4. Overused vocabulary

### AWP-013 — The "delve" register
**Category:** Overused vocabulary
**Description:** The text reaches for elevated verbs where plain ones would be more precise.
**Linguistic characteristics:** *Delve into*, *dive deep*, *explore*, *navigate*, *unpack*, *illuminate* used for ordinary acts of reading, explaining, or examining.
**Why it can weaken writing:** The metaphor is vague and often inflates a simple action such as "read the logs."
**Recognition criteria:** Substitute "look at," "read," or "explain." If meaning is unchanged and the sentence improves, the elevated verb was decoration.
**Original example:** "This section delves into the intricacies of cache invalidation."
**Improved example:** "This section explains when the cache is cleared and what happens to in-flight requests."
**Explanation of improvement:** It states the two facts the reader needs.
**Appropriate exceptions:** "Explore" is standard in data analysis ("we explored three hypotheses") and in user-interface language ("explore the dataset").

### AWP-014 — The significance adjective
**Category:** Overused vocabulary
**Description:** Nouns are repeatedly promoted with adjectives that rank their importance rather than describe them.
**Linguistic characteristics:** *Robust*, *comprehensive*, *powerful*, *seamless*, *cutting-edge*, *state-of-the-art*, *world-class*.
**Why it can weaken writing:** The adjective asserts a quality without supplying the property that produces it, so the reader cannot verify the claim.
**Recognition criteria:** Ask "what makes it X?" If the text never answers, the adjective is a placeholder.
**Original example:** "The platform offers a robust, scalable, and comprehensive solution."
**Improved example:** "The platform retries failed jobs three times and keeps a queue per tenant, so one tenant's backlog does not delay another's."
**Explanation of improvement:** Specific behaviors replace quality labels.
**Appropriate exceptions:** Marketing copy may use evaluative adjectives, but a factual claim should still follow within the same paragraph.

### AWP-015 — The nominalization habit
**Category:** Overused vocabulary
**Description:** Actions are turned into abstract nouns, which then need weak verbs to carry them.
**Linguistic characteristics:** *Utilization*, *implementation*, *optimization*, *facilitation*, *consideration*, *the provision of*; verb + noun where a single verb would do.
**Why it can weaken writing:** It hides the actor and the action, lengthens sentences, and makes text harder to skim.
**Recognition criteria:** Look for "the X of Y" and "-tion" clusters. Rewrite with the underlying verb.
**Original example:** "The implementation of the migration requires the consideration of downtime."
**Improved example:** "Before migrating, decide how much downtime is acceptable."
**Explanation of improvement:** Two hidden verbs ("implement," "consider") become one direct instruction.
**Appropriate exceptions:** Nominalizations are normal in scientific writing ("measurement," "expression") and often name an established concept.

### AWP-016 — The filler intensifier
**Category:** Overused vocabulary
**Description:** Degree adverbs modify words that already carry the degree, or modify claims that need evidence instead.
**Linguistic characteristics:** *Very*, *extremely*, *highly*, *incredibly*, *truly*, *remarkably*, *significantly* (non-statistical), often stacked.
**Why it can weaken writing:** Intensifiers scale a claim without supporting it, and repeated use flattens emphasis.
**Recognition criteria:** Remove the adverb. If the sentence loses no information, keep it removed.
**Original example:** "The new compiler is significantly faster and extremely reliable."
**Improved example:** "The new compiler builds the sample project in 12 seconds instead of 41, and it produced identical binaries across 200 test runs."
**Explanation of improvement:** Measurements do the intensifying.
**Appropriate exceptions:** "Significantly" is precise in statistics and should be kept when a test result is being reported.

---

## 5. Generic descriptions

### AWP-017 — The category description
**Category:** Generic descriptions
**Description:** A thing is described by naming its category and one obvious property instead of its distinguishing behavior.
**Linguistic characteristics:** "X is a tool that helps users do Y," where Y is what every tool in the category does.
**Why it can weaken writing:** The description does not help a reader decide whether X is the right choice.
**Recognition criteria:** Compare the description with a competitor's. If it would still be accurate, it is too general.
**Original example:** "This library helps developers build web applications."
**Improved example:** "This library renders server-side HTML with no client JavaScript and reloads only the changed fragment."
**Explanation of improvement:** It states the two design choices that determine fit.
**Appropriate exceptions:** A one-line index entry may need category-level description; the detail can follow.

### AWP-018 — The adjective inventory
**Category:** Generic descriptions
**Description:** A product, place, or person is described through a list of evaluative adjectives with no observable details.
**Linguistic characteristics:** *Beautiful*, *intuitive*, *user-friendly*, *modern*, *elegant*, *simple*; adjectives that require a standard the text never states.
**Why it can weaken writing:** The reader cannot picture the object or check the judgment.
**Recognition criteria:** Ask what a reader would see, hear, or measure. If the text cannot answer, the adjectives are doing no work.
**Original example:** "The dashboard has a clean, modern, and intuitive interface."
**Improved example:** "The dashboard puts the four error rates above the fold and links each one to its alert rule."
**Explanation of improvement:** Layout and function replace taste.
**Appropriate exceptions:** Design criticism legitimately evaluates appearance, but it should name the features that produce the impression.

### AWP-019 — The universal user
**Category:** Generic descriptions
**Description:** The text describes behavior in terms of "users" or "people" without specifying who they are or what they are trying to do.
**Linguistic characteristics:** "Users want…", "people expect…", "developers need…", with no segment, task, or evidence.
**Why it can weaken writing:** It converts a design assumption into a supposed fact.
**Recognition criteria:** Ask which users, in which situation, and on what evidence. If the text cannot say, the claim is an assumption.
**Original example:** "Users want a simpler onboarding experience."
**Improved example:** "First-time administrators abandoned setup at the permissions step in 38% of trials, mostly because the required role was not explained."
**Explanation of improvement:** A defined group, a defined task, and a measured failure replace a wish.
**Appropriate exceptions:** Early product documents may state hypotheses explicitly ("we assume…"); mark them as assumptions.

### AWP-020 — The feature without a consequence
**Category:** Generic descriptions
**Description:** A capability is listed without saying what it changes for the reader.
**Linguistic characteristics:** "Supports X," "includes Y," "offers Z," with no condition, limit, or outcome.
**Why it can weaken writing:** Features are only meaningful in relation to a task; a bare list makes the reader do the translation.
**Recognition criteria:** For each feature, ask "so what changes?" If the document never says, add the consequence or cut the item.
**Original example:** "The service supports custom domains and SSL."
**Improved example:** "Custom domains with automatic certificates let a customer serve the app from their own hostname without a proxy."
**Explanation of improvement:** The feature is tied to the task it unblocks.
**Appropriate exceptions:** API reference tables list capabilities compactly; the surrounding prose should still explain consequences.

---

## 6. Excessive adjectives

### AWP-021 — The evaluative pile-up
**Category:** Excessive adjectives
**Description:** Three or more evaluative adjectives modify one noun.
**Linguistic characteristics:** "A powerful, flexible, and reliable system"; commas and "and" building a rhythm rather than a description.
**Why it can weaken writing:** The modifiers compete, none is verifiable, and the noun loses precision.
**Recognition criteria:** Keep the one adjective that changes the reader's decision. Delete the rest or convert them to properties.
**Original example:** "a fast, secure, and scalable database"
**Improved example:** "a database that commits in 4 ms and encrypts replicas at rest"
**Explanation of improvement:** Each property becomes measurable.
**Appropriate exceptions:** Literary description can accumulate adjectives deliberately; the effect should be intentional and controlled.

### AWP-022 — The mood adjective
**Category:** Excessive adjectives
**Description:** Adjectives describe the writer's attitude toward the subject rather than the subject itself.
**Linguistic characteristics:** *Exciting*, *fascinating*, *remarkable*, *impressive*, *amazing*, *incredible*.
**Why it can weaken writing:** It tells the reader how to feel and often substitutes for the detail that would produce the feeling.
**Recognition criteria:** Remove the adjective. If the sentence still conveys the fact, the adjective was commentary.
**Original example:** "The team achieved impressive results with an innovative approach."
**Improved example:** "The team cut review time from nine days to two by reviewing one small change per day."
**Explanation of improvement:** The result produces the impression without instruction.
**Appropriate exceptions:** Reviews and personal essays may express enthusiasm; specific reasons should accompany it.

### AWP-023 — The redundant pair
**Category:** Excessive adjectives
**Description:** Two adjectives repeat the same semantic content.
**Linguistic characteristics:** "Basic fundamentals," "future plans," "unexpected surprise," "collaborative teamwork," "end result."
**Why it can weaken writing:** It suggests the writer is not attending to meaning, and it weakens both words.
**Recognition criteria:** Check whether one word entails the other. If so, delete one.
**Original example:** "The final end result was a complete success."
**Improved example:** "The release shipped on schedule with no rollbacks."
**Explanation of improvement:** The claim becomes checkable and the redundancy disappears.
**Appropriate exceptions:** Some fixed phrases ("null and void") are legal terms of art; keep them in legal text.

### AWP-024 — The adjective instead of a number
**Category:** Excessive adjectives
**Description:** A quantity is described with a vague adjective where a figure is available.
**Linguistic characteristics:** *Many*, *numerous*, *significant* (as "large"), *substantial*, *a variety of*, *several* used for counts the writer knows.
**Why it can weaken writing:** It withholds the precision the reader needs and can hide a small effect.
**Recognition criteria:** Ask whether the writer has the count. If yes, give it.
**Original example:** "Numerous customers reported substantial improvements."
**Improved example:** "Of 240 surveyed customers, 168 reported faster checkout."
**Explanation of improvement:** Counts and denominators let the reader judge the claim.
**Appropriate exceptions:** When the figure is unknown or confidential, say so ("the exact count is under NDA") rather than implying precision.

---

## 7. Unnecessary adverbs

### AWP-025 — The manner adverb default
**Category:** Unnecessary adverbs
**Description:** Verbs are paired with manner adverbs that restate the verb.
**Linguistic characteristics:** "Quickly rushed," "quietly whispered," "completely eliminated," "actively pursuing," "successfully completed."
**Why it can weaken writing:** The adverb adds syllables, not meaning, and can imply that the plain verb was insufficient.
**Recognition criteria:** Remove the adverb. If the action is unchanged, leave it out.
**Original example:** "The team successfully completed the migration."
**Improved example:** "The team finished the migration on 14 March."
**Explanation of improvement:** It replaces a redundant modifier with a fact.
**Appropriate exceptions:** Adverbs distinguish real alternatives: "she spoke quietly" contrasts with loudly, and the contrast may matter.

### AWP-026 — The hedging adverb
**Category:** Unnecessary adverbs
**Description:** Adverbs soften claims that the text could state directly or qualify precisely.
**Linguistic characteristics:** *Potentially*, *arguably*, *seemingly*, *relatively*, *fairly*, *somewhat*, *perhaps*; often several in one sentence.
**Why it can weaken writing:** Vague hedging makes the writer sound unsure without telling the reader what is uncertain.
**Recognition criteria:** Ask which specific condition is uncertain. State it, or drop the hedge.
**Original example:** "This approach is potentially somewhat more effective in certain situations."
**Improved example:** "This approach reduced error rates in the two small datasets tested; the effect on larger datasets is unknown."
**Explanation of improvement:** The uncertainty is located and bounded.
**Appropriate exceptions:** Genuine uncertainty deserves language: "the estimate is rough because the sample was not random."

### AWP-027 — The emphasis adverb
**Category:** Unnecessary adverbs
**Description:** Adverbs attempt to strengthen a statement whose strength should come from evidence.
**Linguistic characteristics:** *Really*, *very*, *definitely*, *absolutely*, *highly*, *particularly*, *especially* before adjectives.
**Why it can weaken writing:** Emphasis by adverb is a claim about importance that the sentence does not support.
**Recognition criteria:** Delete the adverb and read the sentence. If it sounds weaker but is equally true, the evidence is missing, not the adverb.
**Original example:** "This is a particularly important consideration."
**Improved example:** "Ignoring this step drops the session cookie, so every request fails after login."
**Explanation of improvement:** The consequence explains the importance.
**Appropriate exceptions:** Conversational writing uses "really" and "very" as normal rhythm; the pattern matters when it clusters in formal prose.

### AWP-028 — The process adverb
**Category:** Unnecessary adverbs
**Description:** Stage directions describe how the writer is proceeding instead of advancing the content.
**Linguistic characteristics:** "Interestingly," "importantly," "notably," "crucially," "surprisingly," "essentially," "basically."
**Why it can weaken writing:** The writer grades their own material, which is weaker than letting the material speak.
**Recognition criteria:** Remove the adverb. If the sentence still shows why the point matters, the label was unnecessary.
**Original example:** "Interestingly, the second run produced a different result."
**Improved example:** "The second run produced a different result because the seed was not fixed."
**Explanation of improvement:** The interesting fact and its cause are both present.
**Appropriate exceptions:** In a research narrative, "surprisingly" can signal a genuine deviation from expectation that the text then analyzes.

---

## 8. Repetitive sentence structures

### AWP-029 — The subject-first monotone
**Category:** Repetitive sentence structures
**Description:** Consecutive sentences begin with the same subject and verb pattern.
**Linguistic characteristics:** "The system does X. The system does Y. The system does Z."; or "It is… It is… It is…"
**Why it can weaken writing:** The repetition creates a chant, and each new sentence feels like a reset rather than a development.
**Recognition criteria:** Read the first words of ten consecutive sentences. If the same noun or pronoun recurs, restructure some sentences around their actual topic.
**Original example:** "The parser reads the file. The parser builds a tree. The parser reports errors."
**Improved example:** "The parser reads the file, builds a tree, and reports errors with line numbers."
**Explanation of improvement:** Shared subject and shared tense become one clause chain.
**Appropriate exceptions:** Deliberate anaphora is a rhetorical device; in instructions, repeated subjects can reduce ambiguity.

### AWP-030 — The triplet cadence
**Category:** Repetitive sentence structures
**Description:** Ideas are habitually grouped into three, regardless of how many the content contains.
**Linguistic characteristics:** Three adjectives, three examples, three clauses; "X, Y, and Z" as a reflex.
**Why it can weaken writing:** The third item is often padding, and a real fourth item gets cut to preserve the rhythm.
**Recognition criteria:** Count the items the content actually has. If the text forces three, the structure is driving the content.
**Original example:** "The update improves speed, reliability, and usability."
**Improved example:** "The update halves cold-start time and retries failed uploads twice."
**Explanation of improvement:** Two real changes replace three vague ones.
**Appropriate exceptions:** Three-part lists are natural when exactly three items exist, and they are a legitimate rhetorical pattern in speeches.

### AWP-031 — The short-short-long seesaw
**Category:** Repetitive sentence structures
**Description:** Sentence lengths alternate in a mechanical pattern intended to sound dynamic.
**Linguistic characteristics:** A very short sentence after every long one; fragments used as punctuation; a "punchy" line at the end of each paragraph.
**Why it can weaken writing:** Rhythm that follows a template draws attention to itself and can make simple ideas sound portentous.
**Recognition criteria:** Mark sentence lengths across a paragraph. If the pattern repeats identically in every paragraph, it is a formula.
**Original example:** "The migration took six months. It was hard. The team learned a lot. But they shipped."
**Improved example:** "The migration took six months, mostly because two services shared a database. The team split them first, then moved the rest."
**Explanation of improvement:** Length follows content: the cause needs a clause, the outcome is short.
**Appropriate exceptions:** Marketing and speechwriting use controlled rhythm intentionally; even there, variation should track emphasis.

### AWP-032 — The identical clause frame
**Category:** Repetitive sentence structures
**Description:** Several sentences use the same syntactic frame with different words.
**Linguistic characteristics:** "X is not Y, it is Z" repeated; "By doing A, we can B" repeated; "Not only X but also Y" repeated.
**Why it can weaken writing:** The frame becomes more noticeable than the content, and the text sounds generated from a template.
**Recognition criteria:** Compare sentence skeletons rather than words. If three or more share a skeleton, vary the syntax where meaning allows.
**Original example:** "It is not a database, it is a cache. It is not a queue, it is a log. It is not a framework, it is a library."
**Improved example:** "The tool is a cache with a log underneath, not a database or a queue, and it ships as a library rather than a framework."
**Explanation of improvement:** The distinctions are preserved in one sentence with a different shape.
**Appropriate exceptions:** Parallel definitions in a glossary or comparison table should keep a shared frame for scanability.

---

## 9. Artificial paragraph symmetry

### AWP-033 — The equal-length paragraph
**Category:** Artificial paragraph symmetry
**Description:** Every paragraph is about the same length, regardless of the complexity of its idea.
**Linguistic characteristics:** Four to six sentences per paragraph throughout; section boundaries that fall at regular intervals.
**Why it can weaken writing:** Importance and complexity stop being visible in the layout; a minor point gets the same space as the main argument.
**Recognition criteria:** Compare paragraph lengths with the weight of their claims. If the correlation is weak or absent, the symmetry is imposed.
**Original example:** Three paragraphs of five sentences each covering setup, a central proof, and a minor caveat.
**Improved example:** A short setup paragraph, a longer proof with its evidence, and a one-sentence caveat.
**Explanation of improvement:** Space now signals importance.
**Appropriate exceptions:** Style guides for web content sometimes cap paragraph length for readability; that is a deliberate constraint, not symmetry.

### AWP-034 — The mirrored section
**Category:** Artificial paragraph symmetry
**Description:** Sections repeat the same internal shape: claim, three supports, mini-summary.
**Linguistic characteristics:** Predictable sequence in every section; each ends with a summary sentence; each begins with a definition.
**Why it can weaken writing:** Readers can predict the structure instead of following the argument, and sections that need a different shape are forced into the mold.
**Recognition criteria:** Outline the internal structure of each section. If they are identical, check whether the content really has the same shape.
**Original example:** Every one of six sections defines a term, lists three benefits, and concludes with a sentence beginning "Ultimately."
**Improved example:** The problem section states symptoms and causes; the options section compares trade-offs; the decision section states the choice and its cost.
**Explanation of improvement:** Each section's shape follows its job.
**Appropriate exceptions:** Reference documentation benefits from consistent section templates ("Parameters," "Returns," "Errors") because readers look for those fields.

### AWP-035 — The symmetric comparison
**Category:** Artificial paragraph symmetry
**Description:** Two options are given exactly equal space and structure even though the evidence or the writer's conclusion favors one.
**Linguistic characteristics:** "On the one hand… on the other hand…"; equal bullet counts; a neutral closing that refuses to choose.
**Why it can weaken writing:** It can manufacture balance where none exists and leave the reader without a decision.
**Recognition criteria:** Ask whether the options are genuinely comparable in evidence and consequence. If not, the symmetry is misleading.
**Original example:** "Some say the rewrite is worth it; others disagree. Both views have merit."
**Improved example:** "The rewrite would take eleven weeks and remove the two failure modes that caused most incidents; the main cost is a feature freeze."
**Explanation of improvement:** It compares specific costs and benefits instead of moods.
**Appropriate exceptions:** A literature review may present competing positions at equal length when the disagreement itself is the subject.

### AWP-036 — The balanced list of three pros and three cons
**Category:** Artificial paragraph symmetry
**Description:** Advantages and disadvantages are forced into matching counts.
**Linguistic characteristics:** Three pros, three cons, regardless of how many exist; the third item on each side is often weak.
**Why it can weaken writing:** Matching the counts distorts the evidence and implies an equivalence the analysis does not support.
**Recognition criteria:** Count the real items on each side. If the list was padded to match, cut the padding.
**Original example:** "Pros: faster, cheaper, simpler. Cons: newer, riskier, less familiar."
**Improved example:** "It is faster and cheaper to run. The risk is maturity: two of the four required features are still beta."
**Explanation of improvement:** Real asymmetry is allowed to show.
**Appropriate exceptions:** A decision matrix with fixed criteria may produce equal counts; the criteria, not the count, should drive it.

---

## 10. Redundant explanations

### AWP-037 — The definition restatement
**Category:** Redundant explanations
**Description:** A term is defined, then re-explained in the next sentence with different words.
**Linguistic characteristics:** "X is A. In other words, X is A."
**Why it can weaken writing:** The second sentence adds length but not understanding, and it can suggest the first was inadequate.
**Recognition criteria:** Compare the two sentences for new information. If none, delete one.
**Original example:** "The cache stores copies of data. In other words, it keeps data copies for faster access."
**Improved example:** "The cache stores copies of hot rows in memory, so repeated reads skip the database."
**Explanation of improvement:** The second sentence adds mechanism and consequence instead of repeating the definition.
**Appropriate exceptions:** Rephrasing is useful when the first statement was technical and the audience needs a plain version; then the plain version should be genuinely different in register.

### AWP-038 — The obvious consequence
**Category:** Redundant explanations
**Description:** The text spells out a consequence the reader can infer immediately.
**Linguistic characteristics:** "Because it is faster, it takes less time." "Since the file is deleted, it is no longer there."
**Why it can weaken writing:** It insults the reader's inference and slows the argument.
**Recognition criteria:** Ask whether a competent reader would need the sentence. If not, cut it.
**Original example:** "The new index makes queries faster, which means they take less time to run."
**Improved example:** "The new index cuts the report query from 3.1 s to 180 ms."
**Explanation of improvement:** A measurement replaces a tautology.
**Appropriate exceptions:** Safety, legal, and onboarding texts sometimes state consequences explicitly to prevent misreading; that is a deliberate choice.

### AWP-039 — The pre-emptive justification
**Category:** Redundant explanations
**Description:** The text defends a choice before the reader has questioned it.
**Linguistic characteristics:** "This may seem unusual, but…", "Some might argue…", "It is worth noting that we chose…"
**Why it can weaken writing:** It invents an objection, gives it space, and makes the writer sound anxious.
**Recognition criteria:** Ask whether the objection appears anywhere in the audience's likely response. If not, cut the defense.
**Original example:** "Some might wonder why we used a queue here, but it is actually a reasonable choice."
**Improved example:** "A queue decouples ingestion from processing, so a slow consumer does not block uploads."
**Explanation of improvement:** The rationale replaces the imagined critic.
**Appropriate exceptions:** In peer review responses, addressing likely objections is the genre's purpose.

### AWP-040 — The explanatory echo in headings
**Category:** Redundant explanations
**Description:** A heading is immediately followed by a sentence that restates it.
**Linguistic characteristics:** "## Performance. This section discusses performance."
**Why it can weaken writing:** It wastes the most-read line of the section and delays the first fact.
**Recognition criteria:** Read the heading and the first sentence together. If the sentence only repeats the heading, delete it.
**Original example:** "## Installation. This section explains how to install the package."
**Improved example:** "## Installation. Run `npm install @scope/pkg`, then add the middleware to your server entry point."
**Explanation of improvement:** The first sentence starts the task.
**Appropriate exceptions:** A long reference chapter may need a scope sentence listing what the section covers, especially if readers arrive by search.

---

## 11. Excessive summarization

### AWP-041 — The section recap
**Category:** Excessive summarization
**Description:** Every section ends with a sentence or paragraph summarizing what it just said.
**Linguistic characteristics:** "In this section, we saw that…"; repeated at each heading.
**Why it can weaken writing:** It doubles the number of summary sentences and trains readers to skip endings, where qualifications often sit.
**Recognition criteria:** Count recaps. If more than one appears in a short document, most are removable.
**Original example:** "In this section, we looked at the three configuration options."
**Improved example:** (Delete the sentence; the section already showed the options.)
**Explanation of improvement:** The heading and content carry the structure.
**Appropriate exceptions:** Long chapters benefit from a short recap before a major transition, especially in textbooks.

### AWP-042 — The abstract that repeats the title
**Category:** Excessive summarization
**Description:** A summary opens by restating the title or the obvious subject instead of stating the finding.
**Linguistic characteristics:** "This paper is about X. X is important. We study X."
**Why it can weaken writing:** It spends the most valuable lines on orientation rather than results.
**Recognition criteria:** Ask what the reader learns from the summary that the title did not already say.
**Original example:** "This report examines employee retention. Employee retention is a key issue for organizations."
**Improved example:** "Voluntary turnover fell from 22% to 14% after the team moved to fixed on-call rotations, with no change in pay."
**Explanation of improvement:** A finding and its condition replace a topic announcement.
**Appropriate exceptions:** Structured abstracts in medicine often include a Background sentence by convention; keep it brief.

### AWP-043 — The layered summary
**Category:** Excessive summarization
**Description:** The same content is summarized at several levels: introduction, section recap, chapter summary, executive summary.
**Linguistic characteristics:** Near-identical sentences at three removes from the source material.
**Why it can weaken writing:** Repetition consumes space and can introduce drift, where the summary and the body disagree.
**Recognition criteria:** Compare summaries across levels. If they repeat rather than escalate in abstraction, cut the middle layer.
**Original example:** An executive summary, an introduction, and a conclusion all stating the same three recommendations.
**Improved example:** The executive summary states the decision; the introduction states the problem; the conclusion states the remaining risk.
**Explanation of improvement:** Each layer has a different job.
**Appropriate exceptions:** Regulatory and grant documents may mandate multiple summary layers; follow the template while keeping each layer's distinct function.

### AWP-044 — The summary instead of an answer
**Category:** Excessive summarization
**Description:** A question receives a recap of the topic rather than a direct answer.
**Linguistic characteristics:** The first paragraph describes the field; the answer appears at the end or not at all.
**Why it can weaken writing:** The reader has to extract the answer from context, and the writer avoids committing to one.
**Recognition criteria:** Look for the sentence that answers the question. If it is missing, the text summarized instead of answering.
**Original example:** "There are many factors to consider when choosing a database. Each has strengths and weaknesses."
**Improved example:** "Use PostgreSQL here: the workload is transactional, the team already operates it, and the data fits on one machine."
**Explanation of improvement:** A recommendation with reasons replaces a survey.
**Appropriate exceptions:** Exploratory questions ("what are the options?") legitimately call for a survey; even then, state the criterion for choosing.

---

## 12. Generic examples

### AWP-045 — The placeholder persona
**Category:** Generic examples
**Description:** Examples use unnamed users or companies doing unspecified things.
**Linguistic characteristics:** "A user wants to…", "A company needs to…", "Imagine a developer who…"
**Why it can weaken writing:** The reader cannot map the example onto a real situation, so the lesson stays abstract.
**Recognition criteria:** Ask whether the example would change if the domain changed. If not, it is a placeholder.
**Original example:** "For example, a company might want to improve its processes."
**Improved example:** "A three-person support team that answers 400 tickets a week can route billing questions to a shared queue and cut first-response time."
**Explanation of improvement:** Scale, task, and outcome make the example testable.
**Appropriate exceptions:** Hypotheticals are appropriate for logic and ethics, where the point is the structure of the case.

### AWP-046 — The foo-bar example
**Category:** Generic examples
**Description:** Code or data examples use meaningless identifiers that hide the real shape of the problem.
**Linguistic characteristics:** `foo`, `bar`, `baz`, `data`, `item`, `value` standing in for domain objects.
**Why it can weaken writing:** The reader must translate the example before applying it, and edge cases specific to real data disappear.
**Recognition criteria:** Ask whether the identifier tells the reader what the object is. If not, rename it.
**Original example:** `function process(data) { return data.map(x => x.value) }`
**Improved example:** `function invoiceAmountsCents(lineItems) { return lineItems.map(item => item.amountCents) }`
**Explanation of improvement:** Names carry the domain and the unit.
**Appropriate exceptions:** Purely syntactic demonstrations (a regex, a language feature) sometimes need neutral names; keep them minimal.

### AWP-047 — The example that restates the rule
**Category:** Generic examples
**Description:** The example illustrates a rule by repeating the rule's wording with no new case.
**Linguistic characteristics:** Rule: "Use active voice." Example: "The team used active voice."
**Why it can weaken writing:** The reader learns nothing about application, especially at the boundaries where rules are hard.
**Recognition criteria:** Ask what the example shows that the rule did not. If nothing, replace it with a realistic case.
**Original example:** "Avoid vague language. For example, do not be vague."
**Improved example:** "Replace 'improve performance' with the metric and target: 'cut p95 latency from 800 ms to 200 ms.'"
**Explanation of improvement:** The example shows the transformation, not the label.
**Appropriate exceptions:** Definitions may need a simple canonical instance before a complex one.

### AWP-048 — The borrowed case study
**Category:** Generic examples
**Description:** A famous company is cited as an example without specifics that transfer.
**Linguistic characteristics:** "Companies like Google and Amazon…"; the example is used to justify a practice.
**Why it can weaken writing:** Scale, resources, and context differ, and the claim about the company is often unverifiable.
**Recognition criteria:** Ask what the cited company actually did, at what scale, and whether the reader's situation resembles it.
**Original example:** "Successful companies like Google use this approach."
**Improved example:** "Google's published SRE practice of limiting change velocity applies here only if the team has comparable monitoring; without it, the limit hides failures."
**Explanation of improvement:** The example is bounded and its transfer conditions are stated.
**Appropriate exceptions:** Historical and business case studies can use well-known firms when sources are cited and differences are acknowledged.

---

## 13. Empty motivational statements

### AWP-049 — The encouragement filler
**Category:** Empty motivational statements
**Description:** The text inserts encouragement that does not help the reader act.
**Linguistic characteristics:** "You've got this!", "Keep pushing forward," "Every expert was once a beginner."
**Why it can weaken writing:** It can read as condescension, and it occupies space where a concrete next step would be more useful.
**Recognition criteria:** Ask what the reader can do differently after the sentence. If nothing, it is filler.
**Original example:** "Learning to code takes time, but don't give up!"
**Improved example:** "Start with one small script that renames files in a folder; it exercises input, loops, and error handling in about 20 lines."
**Explanation of improvement:** A first task replaces a slogan.
**Appropriate exceptions:** Personal essays and coaching material may use encouragement as part of the relationship; it should be specific to the reader's situation.

### AWP-050 — The greatness invitation
**Category:** Empty motivational statements
**Description:** The text invites the reader to imagine their potential in grand terms.
**Linguistic characteristics:** "Unlock your potential," "take your skills to the next level," "transform your workflow."
**Why it can weaken writing:** The promise is unmeasurable and often unrelated to what the document actually delivers.
**Recognition criteria:** Ask what changes concretely after reading. If the answer is a feeling, the claim is promotional.
**Original example:** "Unlock your full potential with this productivity system."
**Improved example:** "The system asks for three priorities each morning and hides the rest of the backlog until they are done."
**Explanation of improvement:** A behavior replaces an aspiration.
**Appropriate exceptions:** Advertising may promise transformation, but product documentation should describe behavior.

### AWP-051 — The journey metaphor
**Category:** Empty motivational statements
**Description:** Progress is described as a journey with no route, distance, or destination.
**Linguistic characteristics:** "Your journey starts here," "on this journey," "the path ahead."
**Why it can weaken writing:** The metaphor substitutes for a plan and can make a routine task sound momentous.
**Recognition criteria:** Ask where the reader is now and what the next milestone is. If the text cannot say, the metaphor is empty.
**Original example:** "Your journey to better writing begins today."
**Improved example:** "Rewrite one paragraph a day for a week, focusing only on sentence openings; compare the before and after on Friday."
**Explanation of improvement:** It gives a scope, a duration, and a check.
**Appropriate exceptions:** Autobiographical and reflective writing may use journey language when the narrative actually follows a course.

### AWP-052 — The stakes inflation
**Category:** Empty motivational statements
**Description:** Ordinary tasks are framed as high-stakes turning points.
**Linguistic characteristics:** "This changes everything," "the future depends on," "a pivotal moment."
**Why it can weaken writing:** It exhausts the reader's sense of scale and makes genuine stakes harder to signal.
**Recognition criteria:** Ask what concretely changes if the reader acts or does not. If the answer is small, lower the language.
**Original example:** "This decision will shape the future of your entire career."
**Improved example:** "This decision affects which team you join for the next year and whether you keep your current on-call rotation."
**Explanation of improvement:** The scope is stated and bounded.
**Appropriate exceptions:** Crisis communication and fundraising may legitimately emphasize stakes; the claim should be supported in the same document.

---

## 14. Unnecessary disclaimers

### AWP-053 — The blanket limitation
**Category:** Unnecessary disclaimers
**Description:** A general disclaimer is attached to specific advice without identifying what it limits.
**Linguistic characteristics:** "This is not financial advice," "results may vary," "consult a professional," attached to an answer with no risk-specific content.
**Why it can weaken writing:** It shifts responsibility without informing the reader, and repeated boilerplate trains them to ignore it.
**Recognition criteria:** Ask what specific action could cause harm and what condition would change the advice. If the text cannot answer, the disclaimer is decorative.
**Original example:** "This is not professional advice; consult an expert."
**Improved example:** "These thresholds assume a single-server deployment; above roughly 10,000 writes per second, the locking scheme needs a different design."
**Explanation of improvement:** The limitation names the condition where the advice stops applying.
**Appropriate exceptions:** Regulated domains require formal disclaimers; place them once and keep them accurate.

### AWP-054 — The capability disclaimer
**Category:** Unnecessary disclaimers
**Description:** The writer disclaims knowledge they demonstrably have, or lack they could resolve.
**Linguistic characteristics:** "I'm not an expert, but…", "I may be wrong, but…", followed by a confident claim.
**Why it can weaken writing:** It undermines the claim while pretending to be modest, and it makes the reader arbitrate without evidence.
**Recognition criteria:** Ask whether the claim is supported. If yes, cut the preface. If no, state the uncertainty precisely.
**Original example:** "I'm not a lawyer, but this contract clause is definitely unenforceable."
**Improved example:** "This clause may be unenforceable in England and Wales because it excludes liability for negligence causing death; a solicitor should confirm."
**Explanation of improvement:** The uncertainty is specific and located.
**Appropriate exceptions:** When the writer genuinely lacks expertise and the reader might overtrust them, a brief scope note is honest.

### AWP-055 — The repetition of an earlier caveat
**Category:** Unnecessary disclaimers
**Description:** The same limitation is stated several times in slightly different words.
**Linguistic characteristics:** The caveat appears in the introduction, again after each claim, and again in the conclusion.
**Why it can weaken writing:** It crowds out content and makes the writer sound unsure of their own scope.
**Recognition criteria:** Search for the key noun of the caveat. If it appears in more than two places, consolidate.
**Original example:** "'Results may vary' appears after every recommendation."
**Improved example:** "One scope note before the recommendations covers sample size and geography."
**Explanation of improvement:** The limitation is stated once, where it applies.
**Appropriate exceptions:** Safety-critical instructions may repeat a warning at each point of use; that repetition prevents injury.

### AWP-056 — The pre-emptive apology
**Category:** Unnecessary disclaimers
**Description:** The text apologizes for length, complexity, or the reader's confusion before any problem occurs.
**Linguistic characteristics:** "Sorry for the long email," "I know this is confusing," "Forgive the detail."
**Why it can weaken writing:** It draws attention to the writer's discomfort and can make the reader expect difficulty.
**Recognition criteria:** Remove the apology. If the text still works, it was unnecessary.
**Original example:** "Sorry for the long explanation, but here's how the build works."
**Improved example:** "The build has four stages; the third is the one that fails when the cache is cold."
**Explanation of improvement:** A map replaces an apology.
**Appropriate exceptions:** A genuine delay or error warrants an apology; that is accountability, not boilerplate.

---

## 15. Repetitive headings

### AWP-057 — The generic heading
**Category:** Repetitive headings
**Description:** Headings name a category ("Overview," "Details," "Considerations") without saying what the section contains.
**Linguistic characteristics:** Nouns that could head any document; no verb, number, or subject-specific term.
**Why it can weaken writing:** Headings are the main navigation aid; a generic one forces the reader to read the section to know what it is.
**Recognition criteria:** Read the heading alone. Could it belong to a different document? If yes, make it specific.
**Original example:** "## Overview"
**Improved example:** "## How the retry queue behaves when Redis is unavailable"
**Explanation of improvement:** The heading states the question the section answers.
**Appropriate exceptions:** A document's first section may legitimately be titled "Overview" when the document is short and the title supplies context.

### AWP-058 — The question heading treadmill
**Category:** Repetitive headings
**Description:** Every heading is a question, including ones with obvious answers.
**Linguistic characteristics:** "What is X?", "Why does X matter?", "How does X work?" repeated at every level.
**Why it can weaken writing:** The pattern becomes predictable and can make declarative content feel like a FAQ.
**Recognition criteria:** Check whether the question form adds anything. If the answer is a single known fact, a statement is cleaner.
**Original example:** "## What is caching? ## Why use caching? ## How does caching work?"
**Improved example:** "## Cache behavior ## When a cache helps ## Invalidation rules"
**Explanation of improvement:** Declarative headings organize by topic and read faster in a table of contents.
**Appropriate exceptions:** FAQ pages and troubleshooting guides use question headings because readers search in question form.

### AWP-059 — The heading that repeats the title
**Category:** Repetitive headings
**Description:** The first heading restates the document title.
**Linguistic characteristics:** Title "Deployment Guide," first heading "## Deployment."
**Why it can weaken writing:** It spends the top-level hierarchy on information the reader already has.
**Recognition criteria:** Compare the title with the first heading. If one contains the other, remove the redundancy.
**Original example:** "# Backup Strategy\n## Backup Strategy Overview"
**Improved example:** "# Backup Strategy\n## What is backed up, and when"
**Explanation of improvement:** The hierarchy advances instead of restarting.
**Appropriate exceptions:** Formal reports sometimes require a title page and a repeated section heading; follow the template.

### AWP-060 — The parallel heading template
**Category:** Repetitive headings
**Description:** All headings share an identical grammatical template, even when sections do different things.
**Linguistic characteristics:** Every heading is a gerund ("Installing," "Configuring," "Troubleshooting") or every heading is a noun phrase, regardless of content.
**Why it can weaken writing:** Forced parallelism can mislabel a section; a conceptual explanation becomes "Understanding X."
**Recognition criteria:** Ask what each section does: instruct, explain, compare, warn. Let the heading's form reflect the job.
**Original example:** "## Understanding Configuration ## Understanding Deployment ## Understanding Errors"
**Improved example:** "## Configuration options ## Deploying to production ## Common errors"
**Explanation of improvement:** Each heading uses the form that matches its function.
**Appropriate exceptions:** Task-based documentation benefits from consistent imperative headings ("Install," "Configure," "Deploy") because readers scan for actions.

## 16. Excessive bullet-list usage

### AWP-061 — The prose-to-list conversion
**Category:** Excessive bullet-list usage
**Description:** Connected reasoning is broken into bullets that depend on each other for meaning.
**Linguistic characteristics:** Bullets containing full arguments, pronouns that refer to earlier bullets, or causal links between items.
**Why it can weaken writing:** Lists imply independent, parallel items. When the items depend on each other, the format hides the logic.
**Recognition criteria:** Read each bullet alone. If it needs the previous one to make sense, the content is prose.
**Original example:** "- Latency rose. - Because the cache expired. - So requests hit the database. - Which then saturated the pool."
**Improved example:** "Latency rose because the cache expired: requests reached the database and saturated the connection pool."
**Explanation of improvement:** The causal chain is visible in one sentence.
**Appropriate exceptions:** Numbered steps are legitimate when each step is an action the reader performs in order.

### AWP-062 — The one-line bullet
**Category:** Excessive bullet-list usage
**Description:** A list contains a single item, or items so short they carry no more information than a phrase.
**Linguistic characteristics:** "Key benefits:" followed by one bullet; bullets of three or four words.
**Why it can weaken writing:** The list machinery (indentation, marker, spacing) outweighs the content and signals structure that is not there.
**Recognition criteria:** Count the items. One item is a sentence. Three-word items usually belong in a sentence too.
**Original example:** "- Faster"
**Improved example:** "Queries return in about 40 ms instead of 300 ms."
**Explanation of improvement:** A sentence carries the comparison and the number.
**Appropriate exceptions:** Checklists and inventories may have short items because the value is in scanning and ticking.

### AWP-063 — The bullet as paragraph
**Category:** Excessive bullet-list usage
**Description:** Bullets are used for long explanatory blocks with multiple sentences each.
**Linguistic characteristics:** Bullets of five or more lines, containing qualifications, examples, and caveats.
**Why it can weaken writing:** Long bullets are hard to scan, and they lose the visual benefit that justified the list.
**Recognition criteria:** If a bullet exceeds roughly three lines, consider a subheading or a paragraph.
**Original example:** A bullet containing a full method description, limitations, and a result.
**Improved example:** A short bullet stating the result, with the method and limitations in the paragraph beneath.
**Explanation of improvement:** Scanning stays easy and detail stays available.
**Appropriate exceptions:** Legal and compliance lists sometimes require self-contained clauses; the format is dictated, not chosen.

### AWP-064 — The nested-list cascade
**Category:** Excessive bullet-list usage
**Description:** Lists nest several levels deep, with sparse content at each level.
**Linguistic characteristics:** Third- and fourth-level bullets; one child per parent; indentation wider than the text.
**Why it can weaken writing:** The hierarchy implies a taxonomy the content does not have, and deep indentation is hard to read on narrow screens.
**Recognition criteria:** Count levels. If a level has only one item, flatten it.
**Original example:** A three-level list where the third level contains one word.
**Improved example:** A two-level list, or a short table when items have parallel attributes.
**Explanation of improvement:** Structure matches content depth.
**Appropriate exceptions:** Outlines and legal hierarchies may need depth; those genres have their own reading conventions.

---

## 17. Artificially balanced arguments

### AWP-065 — The both-sides reflex
**Category:** Artificially balanced arguments
**Description:** Every issue is presented as having two equally valid sides, even when the evidence is one-sided.
**Linguistic characteristics:** "While some argue X, others argue Y"; no criterion for adjudicating; a concluding call for "balance."
**Why it can weaken writing:** It can present a consensus and a fringe view as peers, which misinforms the reader about the state of the evidence.
**Recognition criteria:** Ask what the evidence supports and whether the text says so. If not, the balance is procedural rather than evidential.
**Original example:** "While climate scientists agree on warming, some commentators disagree, so the debate continues."
**Improved example:** "Measurements from independent networks agree on the warming trend; the remaining scientific disputes concern regional magnitude, not the direction."
**Explanation of improvement:** It locates the real disagreement instead of inventing symmetry.
**Appropriate exceptions:** Policy questions involve value trade-offs where reasonable people differ; present the values explicitly.

### AWP-066 — The false dichotomy
**Category:** Artificially balanced arguments
**Description:** The text reduces a range of options to two extremes.
**Linguistic characteristics:** "Either we adopt X or we fail"; "It is a choice between speed and quality."
**Why it can weaken writing:** It hides intermediate designs and makes the conclusion follow from the framing rather than the evidence.
**Recognition criteria:** Name a third option the text ignores. If a plausible one exists, the dichotomy is false.
**Original example:** "Either we rewrite the system or accept technical debt forever."
**Improved example:** "We can isolate the two unstable modules first, which removes most incidents without a full rewrite."
**Explanation of improvement:** A middle path with a mechanism replaces the forced choice.
**Appropriate exceptions:** Genuine binary constraints (a boolean flag, a legal deadline) are real dichotomies and should be stated plainly.

### AWP-067 — The strawman concession
**Category:** Artificially balanced arguments
**Description:** The opposing view is stated in its weakest form so it can be dismissed.
**Linguistic characteristics:** "Critics say X is bad, but…" where X is a caricature; no citation of the strongest version.
**Why it can weaken writing:** It wins an argument nobody made and signals that the writer has not engaged with the real position.
**Recognition criteria:** Find the strongest published version of the opposing view. If the text does not address it, the concession is a strawman.
**Original example:** "Some claim we should abandon all testing because it is slow."
**Improved example:** "The strongest objection is that integration tests duplicate coverage already provided by contract tests; that holds only when the contracts are generated from the same schema."
**Explanation of improvement:** The objection is stated at its best and then bounded.
**Appropriate exceptions:** Informal debate may summarize an opposing view briefly; attribute it and avoid overstating it.

### AWP-068 — The mandatory counterpoint
**Category:** Artificially balanced arguments
**Description:** A counterpoint is inserted because the genre expects one, not because it affects the conclusion.
**Linguistic characteristics:** "Of course, no approach is perfect"; a final paragraph that lists minor drawbacks and then restates the recommendation unchanged.
**Why it can weaken writing:** It adds words without changing the analysis, and it can suggest the drawbacks were considered when they were only named.
**Recognition criteria:** Ask whether any drawback would change the recommendation. If not, explain why not, or cut the paragraph.
**Original example:** "Of course, this approach has some limitations, but overall it is the best choice."
**Improved example:** "The approach fails if writes exceed one region; because this workload is single-region, that limit does not affect the decision."
**Explanation of improvement:** The limitation is tested against the case.
**Appropriate exceptions:** Formal risk sections must list low-probability issues even when they do not change the recommendation.

---

## 18. Unnecessary rhetorical questions

### AWP-069 — The answered-by-the-next-sentence question
**Category:** Unnecessary rhetorical questions
**Description:** A question is posed and answered immediately, adding a beat of suspense with no content.
**Linguistic characteristics:** "What does this mean? It means…"; "Why does this happen? Because…"
**Why it can weaken writing:** It splits one sentence into two and simulates dialogue with a reader who is not present.
**Recognition criteria:** Join the question and answer with "because" or a colon. If the result is clearer, use it.
**Original example:** "So what is the result? The result is a 20% reduction in cost."
**Improved example:** "The change reduced cost by 20%."
**Explanation of improvement:** The finding leads.
**Appropriate exceptions:** Teaching material may use the question-answer pattern to model a reasoning sequence; do it sparingly and only when the question is real.

### AWP-070 — The stacked rhetorical questions
**Category:** Unnecessary rhetorical questions
**Description:** Several questions appear in a row to build momentum.
**Linguistic characteristics:** Three or more questions before any answer; often in introductions and conclusions.
**Why it can weaken writing:** It withholds information and can feel like a sales pitch.
**Recognition criteria:** Count consecutive questions. If more than one appears without an answer between them, consolidate.
**Original example:** "What if you could ship faster? What if bugs disappeared? What if your team loved deployments?"
**Improved example:** "Deployments take 40 minutes and fail 12% of the time; both numbers come from the same manual step."
**Explanation of improvement:** Concrete problems replace hypothetical benefits.
**Appropriate exceptions:** Persuasive speeches use series of questions deliberately; the audience has accepted a rhetorical frame.

### AWP-071 — The question as a heading substitute
**Category:** Unnecessary rhetorical questions
**Description:** A question introduces a paragraph where a topic sentence would be more informative.
**Linguistic characteristics:** "But why does this matter?" at the start of a paragraph that explains relevance.
**Why it can weaken writing:** It makes the reader do the work of inferring the topic and delays the claim.
**Recognition criteria:** Replace the question with the answer's main clause. If the paragraph reads better, the question was scaffolding.
**Original example:** "Why is this important? Because errors compound."
**Improved example:** "Errors compound: a 1% daily failure rate leaves a third of jobs unfinished after a month."
**Explanation of improvement:** The claim and its quantification lead.
**Appropriate exceptions:** In a dialogue or interview format, questions are the structure, not a device.

### AWP-072 — The rhetorical question with an obvious answer
**Category:** Unnecessary rhetorical questions
**Description:** The question's answer is so evident that asking it condescends.
**Linguistic characteristics:** "Who doesn't want faster software?" "Is downtime bad?"
**Why it can weaken writing:** It substitutes agreement for argument and can alienate a knowledgeable reader.
**Recognition criteria:** If the answer is "everyone" or "obviously," the question adds nothing.
**Original example:** "After all, who wants to waste time?"
**Improved example:** "The manual step costs each engineer about 25 minutes a day."
**Explanation of improvement:** A cost replaces a truism.
**Appropriate exceptions:** Light conversational writing may use obvious questions for humor; the tone must support it.

---

## 19. Vague claims

### AWP-073 — The unquantified improvement
**Category:** Vague claims
**Description:** An improvement is claimed without a baseline, a measure, or a magnitude.
**Linguistic characteristics:** "Improves performance," "reduces costs," "enhances usability," "boosts productivity."
**Why it can weaken writing:** The reader cannot tell whether the change matters or how it was measured.
**Recognition criteria:** Ask: compared with what, measured how, by how much? If the text cannot answer, the claim is incomplete.
**Original example:** "The new workflow improves team productivity."
**Improved example:** "The new workflow removed two approval steps, shortening the median release from nine days to four."
**Explanation of improvement:** Baseline, mechanism, and result are present.
**Appropriate exceptions:** Early-stage claims may be directional; label them ("we expect…") and state the planned measure.

### AWP-074 — The authority without a source
**Category:** Vague claims
**Description:** A claim is supported by an unnamed authority.
**Linguistic characteristics:** "Studies show," "experts agree," "research suggests," "industry best practice."
**Why it can weaken writing:** The reader cannot check the claim, and the phrase can launder a guess as a finding.
**Recognition criteria:** Ask which study, which experts, and where. If the text cannot name them, attribute honestly or soften the claim.
**Original example:** "Studies show that remote work increases productivity."
**Improved example:** "A 2023 study of 1,600 call-center workers found a 13% productivity gain for those working from home four days a week; the effect may differ for collaborative work."
**Explanation of improvement:** Source, sample, effect, and scope are stated.
**Appropriate exceptions:** When a source cannot be disclosed, say why and describe its type ("internal telemetry, not published").

### AWP-075 — The scope-free universal
**Category:** Vague claims
**Description:** A claim is stated for all cases when it was observed in one.
**Linguistic characteristics:** "This always works," "X causes Y," with no population, condition, or timeframe.
**Why it can weaken writing:** It overstates the evidence and fails as soon as a reader meets a counterexample.
**Recognition criteria:** Add "in this sample" or "for this configuration." If the claim then becomes true, the universal was unsupported.
**Original example:** "Microservices always improve scalability."
**Improved example:** "Splitting the image service from the API let each scale independently; the gain appeared only when image traffic exceeded API traffic."
**Explanation of improvement:** The condition that produced the benefit is named.
**Appropriate exceptions:** Mathematical and logical claims can be universal when proved; the proof must be present or cited.

### AWP-076 — The undefined success
**Category:** Vague claims
**Description:** Success, quality, or effectiveness is asserted without criteria.
**Linguistic characteristics:** "The project was a success," "the system works well," "the results were positive."
**Why it can weaken writing:** Without criteria, the statement cannot be evaluated or repeated.
**Recognition criteria:** Ask what threshold would have counted as failure. If the text never defines one, success is undefined.
**Original example:** "The pilot was a success."
**Improved example:** "The pilot met its target: 92% of orders shipped within two days, against a goal of 90%."
**Explanation of improvement:** The criterion and the result are explicit.
**Appropriate exceptions:** Narrative and opinion writing may use evaluative language; factual reporting should define its terms.

---

## 20. Contextually inappropriate formality

### AWP-077 — The bureaucratic email
**Category:** Contextually inappropriate formality
**Description:** A routine message is written in officialese.
**Linguistic characteristics:** "Please be advised," "kindly note," "at your earliest convenience," "pursuant to," "herewith."
**Why it can weaken writing:** It creates distance, slows reading, and can make a simple request feel like a legal notice.
**Recognition criteria:** Ask whether the reader would speak this way to a colleague. If not, simplify.
**Original example:** "Please be advised that the report has been finalized and is attached hereto for your review."
**Improved example:** "The report is attached; I need your comments by Thursday."
**Explanation of improvement:** The action and deadline are clear.
**Appropriate exceptions:** Formal correspondence with regulators, courts, or external counsel may require terms of art.

### AWP-078 — The elevated casual message
**Category:** Contextually inappropriate formality
**Description:** A casual channel receives writing that belongs in a formal report.
**Linguistic characteristics:** Full introductions, headings, and conclusions in a two-line chat reply; "Furthermore" in a message to a teammate.
**Why it can weaken writing:** It mismatches the channel's rhythm and can read as cold or performative.
**Recognition criteria:** Compare with the surrounding messages. If the register is far from the room's, adjust.
**Original example:** "Furthermore, I would like to formally acknowledge your assistance with the deployment."
**Improved example:** "Thanks, that deploy fix saved me an hour."
**Explanation of improvement:** It matches the channel and states the specific help.
**Appropriate exceptions:** Sensitive news should not be delivered in a clipped chat style; choose the channel for the content.

### AWP-079 — The ceremonial opener
**Category:** Contextually inappropriate formality
**Description:** A message begins with several lines of greeting and context before its purpose.
**Linguistic characteristics:** "I hope this message finds you well. I am writing to you today regarding…"
**Why it can weaken writing:** It delays the request, and in high-volume inboxes it signals low priority.
**Recognition criteria:** Cover the first two sentences. If the reader still knows why you wrote, they were optional.
**Original example:** "I hope you are doing well. I am reaching out to inquire about the status of the invoice."
**Improved example:** "Is invoice 2041 approved? It is due Friday."
**Explanation of improvement:** It asks the question and gives the reason.
**Appropriate exceptions:** First contact with a stranger or in a high-context culture may warrant a brief greeting; keep it to one line.

### AWP-080 — The casual register in formal evidence
**Category:** Contextually inappropriate formality
**Description:** A formal document uses slang, contractions, or chat conventions where precision and distance are expected.
**Linguistic characteristics:** "Basically," "a ton of," "super," "won't," emoji, sentence fragments in a research report.
**Why it can weaken writing:** It can undermine credibility and, in some genres, create ambiguity about whether a claim is empirical or offhand.
**Recognition criteria:** Check the genre's published conventions. If the document's peers avoid the expression, revise.
**Original example:** "The results were super promising and basically proved the hypothesis."
**Improved example:** "The results were consistent with the hypothesis: the treated group's mean score was 0.6 standard deviations higher (95% CI 0.2–1.0)."
**Explanation of improvement:** The claim is stated at the genre's evidential level.
**Appropriate exceptions:** Opinion columns and personal blogs may use informal register deliberately; that is the voice, not an error.

---

## 21. Overexplaining obvious concepts

### AWP-081 — The beginner tangent
**Category:** Overexplaining obvious concepts
**Description:** The text pauses to explain a basic concept the target audience already knows.
**Linguistic characteristics:** A paragraph on what a database, a function, or a browser is, inside an advanced document.
**Why it can weaken writing:** It wastes expert readers' time and can make the document feel padded or unsure of its audience.
**Recognition criteria:** State the assumed knowledge. If the passage teaches something below that level, cut it or link to a primer.
**Original example:** "A database stores data in tables. Each table has rows and columns."
**Improved example:** "The migration adds a partial index on `orders (tenant_id) WHERE status = 'open'`."
**Explanation of improvement:** It begins at the document's actual technical level.
**Appropriate exceptions:** Tutorials and onboarding guides are supposed to explain basics; match the explanation to the stated prerequisites.

### AWP-082 — The definition spiral
**Category:** Overexplaining obvious concepts
**Description:** Each new term is defined by another term, which is then defined, and so on.
**Linguistic characteristics:** Nested definitions; a parenthetical definition inside a definition.
**Why it can weaken writing:** The reader loses the thread and the main claim disappears under terminology.
**Recognition criteria:** Trace the chain. If defining A requires B and C, use one plain gloss and move on.
**Original example:** "An idempotent operation (an operation that, when applied multiple times, produces the same result as a single application) is…"
**Improved example:** "Retrying an idempotent request is safe: charging the same order twice returns the first charge instead of creating a second."
**Explanation of improvement:** A concrete consequence replaces a nested definition.
**Appropriate exceptions:** Legal and standards documents require precise definitions; put them in a glossary and reference them.

### AWP-083 — The obvious prerequisite
**Category:** Overexplaining obvious concepts
**Description:** The text lists a step or requirement that any reader of the document already meets.
**Linguistic characteristics:** "You will need a computer," "make sure you have internet access," in a guide for developers.
**Why it can weaken writing:** It adds noise to the setup path and can bury a real prerequisite.
**Recognition criteria:** Ask who reads the document and what they must already have. Cut anything below that floor.
**Original example:** "Before you begin, ensure that you have a text editor installed."
**Improved example:** "You need Node 20 or later and a PostgreSQL 15 instance."
**Explanation of improvement:** It lists only the constraints that actually block the task.
**Appropriate exceptions:** Consumer-facing guides may need to state basics; the prerequisite list should still be short and specific.

### AWP-084 — The explain-again footnote
**Category:** Overexplaining obvious concepts
**Description:** A term is explained in the body and then explained again in a note.
**Linguistic characteristics:** A parenthetical gloss followed by a footnote with the same gloss.
**Why it can weaken writing:** It duplicates content across layers and suggests the writer did not trust the first explanation.
**Recognition criteria:** Compare the body and note. If the note adds no example or source, remove it.
**Original example:** Body: "latency (delay before a response)"; note: "Latency refers to the delay before a response."
**Improved example:** Body: "latency (time to first byte)"; note: "Measured at the 95th percentile over one-minute windows."
**Explanation of improvement:** The note adds measurement detail rather than repeating the gloss.
**Appropriate exceptions:** Annotated editions and teaching texts may repeat deliberately for readers who skip around.

---

## 22. Repetitive opening phrases

### AWP-085 — The "When it comes to" opener
**Category:** Repetitive opening phrases
**Description:** Sentences begin with a long prepositional frame instead of the subject.
**Linguistic characteristics:** "When it comes to X," "In terms of X," "With regard to X," "In the context of X."
**Why it can weaken writing:** It postpones the subject and often adds a frame the sentence does not need.
**Recognition criteria:** Delete the frame and start with the subject. If the sentence still means the same, keep the shorter version.
**Original example:** "When it comes to performance, the second version is faster."
**Improved example:** "The second version is faster."
**Explanation of improvement:** The comparison is the sentence.
**Appropriate exceptions:** The frame can narrow a broad subject legitimately: "In terms of memory, the two versions are identical" signals a change of dimension.

### AWP-086 — The "There is/are" opener
**Category:** Repetitive opening phrases
**Description:** Sentences begin with an existential construction that hides the real subject.
**Linguistic characteristics:** "There are several reasons why…", "There is a need for…", "There are many ways to…"
**Why it can weaken writing:** The grammatical subject is empty, and the reader waits for the content.
**Recognition criteria:** Move the real noun to the subject position.
**Original example:** "There are several reasons why the build fails."
**Improved example:** "The build fails for three reasons: a stale lockfile, a missing environment variable, and a flaky network test."
**Explanation of improvement:** The subject and the list arrive together.
**Appropriate exceptions:** Existential constructions are natural when introducing new information: "There is a second path through the forest" is fine in narrative.

### AWP-087 — The "It is important to note" opener
**Category:** Repetitive opening phrases
**Description:** Sentences begin with a phrase that grades the importance of what follows.
**Linguistic characteristics:** "It is important to note that," "It should be mentioned that," "It is worth remembering that."
**Why it can weaken writing:** The phrase claims importance instead of demonstrating it, and it appears often enough to lose force.
**Recognition criteria:** Delete the frame. If the sentence still shows why it matters, the frame was unnecessary.
**Original example:** "It is important to note that the API rate limit is 100 requests per minute."
**Improved example:** "The API allows 100 requests per minute; batch requests above that return 429 until the window resets."
**Explanation of improvement:** The limit and its consequence are stated directly.
**Appropriate exceptions:** In safety instructions, an explicit "Note:" can help readers scan for warnings.

### AWP-088 — The "In order to" opener
**Category:** Repetitive opening phrases
**Description:** Sentences use a wordy purpose frame where "to" would do.
**Linguistic characteristics:** "In order to achieve X, we must…"; "for the purpose of"; "with the aim of."
**Why it can weaken writing:** It adds syllables without adding meaning and can make instructions feel heavier.
**Recognition criteria:** Replace with "to." If the sentence is grammatical and clear, keep the shorter form.
**Original example:** "In order to reduce latency, we added an index."
**Improved example:** "We added an index to reduce latency."
**Explanation of improvement:** The action leads and the purpose follows.
**Appropriate exceptions:** "In order to" can help rhythm in a long sentence with several infinitives; the gain is small.

---

## 23. Predictable paragraph endings

### AWP-089 — The significance closer
**Category:** Predictable paragraph endings
**Description:** Paragraphs end by asserting that the preceding point matters.
**Linguistic characteristics:** "…which is why this matters." "…making it an important consideration." "…and that is significant."
**Why it can weaken writing:** The assertion repeats the paragraph's job instead of advancing it, and it becomes predictable across many paragraphs.
**Recognition criteria:** Read the last sentence alone. If it only evaluates the paragraph, cut it or replace it with a consequence.
**Original example:** "The cache expires every five minutes, which is an important detail."
**Improved example:** "The cache expires every five minutes, so a write is visible to other readers within five minutes."
**Explanation of improvement:** The consequence replaces the evaluation.
**Appropriate exceptions:** A paragraph ending on a judgment can be appropriate in criticism, where evaluation is the content.

### AWP-090 — The forward-reference closer
**Category:** Predictable paragraph endings
**Description:** Paragraphs end by announcing the next paragraph.
**Linguistic characteristics:** "We will explore this next." "The following section addresses…"
**Why it can weaken writing:** It uses the strongest position in the paragraph for navigation rather than content.
**Recognition criteria:** Delete the sentence. If the next paragraph follows naturally, the signpost was unnecessary.
**Original example:** "These constraints shape the design. We will discuss the design next."
**Improved example:** "These constraints shape the design: one queue per tenant, no shared connection pool."
**Explanation of improvement:** The paragraph ends on the conclusion the constraints produce.
**Appropriate exceptions:** Long reports may use explicit roadmap sentences at chapter boundaries, where readers need orientation.

### AWP-091 — The hedge closer
**Category:** Predictable paragraph endings
**Description:** Paragraphs end with a vague qualification that weakens the claim without specifying risk.
**Linguistic characteristics:** "…though results may vary." "…depending on the circumstances." "…in most cases."
**Why it can weaken writing:** It retroactively dilutes the paragraph and leaves the reader unsure what was actually claimed.
**Recognition criteria:** Ask which circumstance changes the result. Name it, or remove the hedge.
**Original example:** "The method works well, though results may vary."
**Improved example:** "The method works when the input is under 10 MB; above that, memory use grows quadratically."
**Explanation of improvement:** The boundary is stated.
**Appropriate exceptions:** Genuine variability deserves acknowledgment; specify the source of variation (sample, region, version).

### AWP-092 — The quotable kicker
**Category:** Predictable paragraph endings
**Description:** Paragraphs end with a short, aphoristic line written to be remembered.
**Linguistic characteristics:** Fragments, parallel structures, or metaphors placed at the end of every section.
**Why it can weaken writing:** Constant aphorism makes the prose sound like a keynote and can substitute for specifics.
**Recognition criteria:** Ask whether the line adds a claim the paragraph did not make. If it only restates, cut it.
**Original example:** "In the end, simplicity is the ultimate sophistication."
**Improved example:** "Removing the plugin layer cut the configuration file from 300 lines to 40."
**Explanation of improvement:** The concrete change makes the point without a slogan.
**Appropriate exceptions:** Essays and speeches use closers for rhetorical effect; the device should be rare enough to land.

---

## 24. Unnecessary restatements

### AWP-093 — The immediate paraphrase
**Category:** Unnecessary restatements
**Description:** A sentence is followed by a paraphrase of itself with no added detail.
**Linguistic characteristics:** "In other words," "that is to say," "put differently," followed by the same proposition.
**Why it can weaken writing:** It doubles length and implies the first sentence failed, which is usually not true.
**Recognition criteria:** Compare the two propositions. If they are identical, delete the second.
**Original example:** "The service is stateless. In other words, it does not store session data."
**Improved example:** "The service is stateless: session data lives in the client's signed token."
**Explanation of improvement:** The colon introduces a consequence, not a repeat.
**Appropriate exceptions:** Rephrasing helps when moving between technical and plain registers for a mixed audience; the second version should genuinely simplify.

### AWP-094 — The closing restatement of the opening
**Category:** Unnecessary restatements
**Description:** The final sentence repeats the first sentence almost exactly.
**Linguistic characteristics:** A circular structure where the conclusion is the introduction.
**Why it can weaken writing:** It gives the impression of an ending without providing one.
**Recognition criteria:** Place the first and last sentences side by side. If they assert the same thing, change the last one to a consequence or a limit.
**Original example:** First: "Caching improves performance." Last: "Thus, caching improves performance."
**Improved example:** Last: "For this workload, the cache cut database reads by 70%, at the cost of five seconds of staleness."
**Explanation of improvement:** The ending adds the trade-off.
**Appropriate exceptions:** Deliberate circular structure is a literary device; the echo should be marked and meaningful.

### AWP-095 — The restatement before the point
**Category:** Unnecessary restatements
**Description:** The writer restates the question or the previous point immediately before answering.
**Linguistic characteristics:** "So, to answer your question about X, X is…"
**Why it can weaken writing:** It delays the answer and can read as stalling.
**Recognition criteria:** Delete everything before the answer. If the answer is still clear, keep it deleted.
**Original example:** "To answer your question about whether the migration is safe, the migration is safe if backups are current."
**Improved example:** "The migration is safe if backups are current."
**Explanation of improvement:** The answer is the sentence.
**Appropriate exceptions:** In a long thread with several questions, naming the one being answered prevents confusion.

### AWP-096 — The duplicated caption
**Category:** Unnecessary restatements
**Description:** A figure, table, or code block is captioned with a sentence that repeats its title or content.
**Linguistic characteristics:** Title "Request flow," caption "This diagram shows the request flow."
**Why it can weaken writing:** Captions are prime space for interpretation; repeating the title wastes it.
**Recognition criteria:** Ask what the reader should notice in the figure. Put that in the caption.
**Original example:** "Figure 2: A diagram of the request flow."
**Improved example:** "Figure 2: Requests pass through the rate limiter before authentication, so unauthenticated floods are rejected earlier."
**Explanation of improvement:** The caption directs attention to the meaningful detail.
**Appropriate exceptions:** Accessibility text may need a plain description of the image; keep it separate from the analytical caption.

---

## 25. Artificially polished phrasing

### AWP-097 — The seamless sentence
**Category:** Artificially polished phrasing
**Description:** Every sentence is smoothed to the same degree, with no rough edges, hesitations, or specificity.
**Linguistic characteristics:** Balanced clauses, no contractions, no concrete nouns, no attributed opinions.
**Why it can weaken writing:** Uniform polish removes the texture that signals a person choosing words for a situation.
**Recognition criteria:** Look for a sentence that could only have been written by someone who did the work. If none exists, the text is too smooth.
**Original example:** "By leveraging cutting-edge methodologies, organizations can optimize outcomes across all dimensions."
**Improved example:** "We tested the method on two years of support tickets; it shortened triage by 11 minutes per case."
**Explanation of improvement:** A specific method and result replace polish.
**Appropriate exceptions:** Ceremonial and promotional writing aim for polish; even there, concrete claims improve it.

### AWP-098 — The balanced clause habit
**Category:** Artificially polished phrasing
**Description:** Sentences are built as neat pairs of balanced clauses.
**Linguistic characteristics:** "Not only X but also Y"; "X not because A, but because B"; every sentence with a symmetrical "and."
**Why it can weaken writing:** The symmetry draws attention to the sentence's shape and can force content into pairs.
**Recognition criteria:** Count balanced constructions per page. If the rhythm repeats, break some sentences where the content is asymmetric.
**Original example:** "It is not merely a tool for writing but a framework for thinking, not just for individuals but for teams."
**Improved example:** "The tool structures revision; teams use it to agree on what counts as a clear paragraph."
**Explanation of improvement:** One claim, stated once.
**Appropriate exceptions:** Antithesis is a legitimate rhetorical figure; use it where the contrast is the point.

### AWP-099 — The ornamented verb
**Category:** Artificially polished phrasing
**Description:** A plain verb is replaced with a decorative phrase.
**Linguistic characteristics:** "Shines a light on," "paves the way for," "serves as a testament to," "plays a pivotal role in."
**Why it can weaken writing:** The ornament obscures the action and often implies more than the evidence shows.
**Recognition criteria:** Name the action in one verb. If the sentence still works, the ornament was decoration.
**Original example:** "The discovery paves the way for a new era of personalized medicine."
**Improved example:** "The discovery identifies a protein marker that predicted response in 60% of the trial group."
**Explanation of improvement:** The finding replaces the prophecy.
**Appropriate exceptions:** Feature writing and speeches use figurative verbs for effect; the figure should fit the subject.

### AWP-100 — The perfect transition
**Category:** Artificially polished phrasing
**Description:** Every idea is connected by a fluent transition, leaving no gaps for the reader to fill.
**Linguistic characteristics:** A connector at the start of nearly every sentence; conclusions anticipated before they are earned.
**Why it can weaken writing:** Over-connection hides weak links and makes the argument feel smoother than it is.
**Recognition criteria:** Remove the connectors and read the paragraph. If the logic collapses, the links were doing the work the evidence should do.
**Original example:** "Therefore, it follows that, consequently, the approach is superior."
**Improved example:** "The approach handled 3× the load at the same latency, so it is the better fit for this traffic profile."
**Explanation of improvement:** One causal link, supported by a measurement.
**Appropriate exceptions:** Philosophical and mathematical prose often need explicit logical connectives; there, they mark inference steps.

---

## 26. Excessive hedging

### AWP-101 — The triple hedge
**Category:** Excessive hedging
**Description:** Several epistemic markers stack in one claim.
**Linguistic characteristics:** "It could possibly be argued that…", "may potentially suggest," "might perhaps."
**Why it can weaken writing:** The claim becomes unfalsifiable and the reader cannot tell what the writer believes.
**Recognition criteria:** Count hedges in the sentence. Keep at most one, and make it specific.
**Original example:** "This may possibly indicate that the treatment could potentially help."
**Improved example:** "The treatment reduced symptoms in the pilot group; the sample was too small to rule out chance."
**Explanation of improvement:** The result and its limitation are both explicit.
**Appropriate exceptions:** In legal and regulatory writing, layered qualification can be required; that is precision, not vagueness.

### AWP-102 — The hedge without a referent
**Category:** Excessive hedging
**Description:** Uncertainty is expressed without saying what is uncertain.
**Linguistic characteristics:** "It depends," "context matters," "there are many factors," with no further specification.
**Why it can weaken writing:** The reader learns that the answer is conditional but not what the conditions are.
**Recognition criteria:** Ask "depends on what?" If the text cannot list the variables, the hedge is incomplete.
**Original example:** "The best choice depends on your needs."
**Improved example:** "Choose the managed service if you need compliance paperwork handled; choose self-hosting if data must stay in your network."
**Explanation of improvement:** The conditions and their consequences are named.
**Appropriate exceptions:** An initial scoping answer may say "it depends" before asking a clarifying question; that is conversation, not a finished claim.

### AWP-103 — The defensive qualifier
**Category:** Excessive hedging
**Description:** The writer adds qualifications to avoid any possible objection rather than to inform.
**Linguistic characteristics:** "In most cases, generally speaking, under certain conditions, for some users."
**Why it can weaken writing:** It weakens every claim equally and makes the text sound afraid of its own conclusions.
**Recognition criteria:** Ask which reader would object and on what grounds. Address that objection once, precisely.
**Original example:** "This generally tends to work in most situations for many teams."
**Improved example:** "This works for teams under 50 engineers; beyond that, the single review queue becomes the bottleneck."
**Explanation of improvement:** The scope is quantified.
**Appropriate exceptions:** Medical and safety guidance must qualify broad recommendations; the qualifiers should be clinically meaningful.

### AWP-104 — The disclaimer hedge
**Category:** Excessive hedging
**Description:** A claim is followed by a disclaimer that removes its force.
**Linguistic characteristics:** "But of course, this is just my opinion." "That said, I could be wrong."
**Why it can weaken writing:** It transfers the burden of judgment to the reader after offering no reasons.
**Recognition criteria:** If the claim has reasons, state them and drop the disclaimer. If it has none, mark it as a hypothesis.
**Original example:** "This is the best approach, but of course that's just my opinion."
**Improved example:** "This approach fits best here because it needs no new infrastructure; the trade-off is a single point of failure."
**Explanation of improvement:** Reasons and costs replace the retreat.
**Appropriate exceptions:** Informal conversation uses softeners to maintain rapport; the pattern matters when it undermines a professional recommendation.

---

## 27. Unnatural word substitutions

### AWP-105 — The thesaurus swap
**Category:** Unnatural word substitutions
**Description:** A common word is replaced with a near-synonym that does not fit the context.
**Linguistic characteristics:** "Utilize" for "use," "commence" for "start," "endeavor" for "try," "reside" for "live."
**Why it can weaken writing:** Near-synonyms differ in connotation, transitivity, and register; the swap can be wrong as well as stiff.
**Recognition criteria:** Substitute the plain word. If the meaning and tone improve, the swap was unnecessary.
**Original example:** "We utilized a script to commence the deployment."
**Improved example:** "We used a script to start the deployment."
**Explanation of improvement:** Plain verbs match the technical setting.
**Appropriate exceptions:** "Utilize" is appropriate when distinguishing productive use from mere possession; that distinction is rare.

### AWP-106 — The euphemism ladder
**Category:** Unnatural word substitutions
**Description:** Direct language is replaced with softer or more abstract terms.
**Linguistic characteristics:** "Let go" for "fired," "negative outcome" for "death," "rightsizing" for "layoffs."
**Why it can weaken writing:** It obscures responsibility and can be read as evasive or manipulative.
**Recognition criteria:** Ask who is protected by the softer term. If the answer is the writer, use the direct term.
**Original example:** "The company right-sized its workforce to optimize operational efficiency."
**Improved example:** "The company cut 400 jobs, about 12% of its staff."
**Explanation of improvement:** The action and scale are explicit.
**Appropriate exceptions:** Clinical and legal contexts sometimes use technical terms to avoid ambiguity; the term should be defined.

### AWP-107 — The invented compound
**Category:** Unnatural word substitutions
**Description:** New compounds or jargon are coined where established terms exist.
**Linguistic characteristics:** "Solution-oriented," "future-proofed," "next-level," "hyper-personalized," "learnings."
**Why it can weaken writing:** The reader must decode an unfamiliar word that carries less precision than the standard one.
**Recognition criteria:** Ask whether a standard term names the same idea. If yes, use it.
**Original example:** "We need a future-proof, solution-oriented architecture."
**Improved example:** "We need an architecture that can add a second payment provider without changing the checkout code."
**Explanation of improvement:** The requirement is stated as a testable property.
**Appropriate exceptions:** A new concept may need a new term; define it once and use it consistently.

### AWP-108 — The misapplied metaphor
**Category:** Unnatural word substitutions
**Description:** A metaphor is used outside the domain where it makes sense.
**Linguistic characteristics:** "The API is the nervous system of the application"; "the database is the brain"; mixed metaphors in one sentence.
**Why it can weaken writing:** The figure implies a structural analogy that does not hold, which can mislead.
**Recognition criteria:** Ask what property the metaphor is supposed to transfer. If the text cannot name it, the metaphor is decorative.
**Original example:** "The message queue is the beating heart of the system."
**Improved example:** "The message queue absorbs bursts: producers write at up to 5,000 events per second, while consumers process 800."
**Explanation of improvement:** The mechanism replaces the body metaphor.
**Appropriate exceptions:** Explanatory metaphors are useful when they map precisely and the text marks where the mapping stops.

---

## 28. Repetitive explanatory structures

### AWP-109 — The claim-evidence-repeat loop
**Category:** Repetitive explanatory structures
**Description:** Every point follows the same three-beat pattern: claim, evidence, restatement.
**Linguistic characteristics:** Each paragraph ends by repeating its claim in slightly different words.
**Why it can weaken writing:** The loop makes the text predictable and inflates length by roughly a third.
**Recognition criteria:** Outline paragraphs by role. If every one ends with a restatement, cut the third beat.
**Original example:** "Latency improved. The p95 fell from 800 ms to 200 ms. So latency is better now."
**Improved example:** "The p95 fell from 800 ms to 200 ms after the index change."
**Explanation of improvement:** The evidence carries the claim.
**Appropriate exceptions:** Teaching materials may restate to reinforce; the restatement should add a new angle or example.

### AWP-110 — The definition-example-application triple
**Category:** Repetitive explanatory structures
**Description:** Concepts are always introduced with the same three-part template, even when a different treatment fits.
**Linguistic characteristics:** Definition, then example, then "this applies when…" in every subsection.
**Why it can weaken writing:** Some concepts need comparison, history, or a counterexample; the template flattens them.
**Recognition criteria:** Ask what the concept most needs: a definition, a demonstration, a boundary case, or a contrast. Choose accordingly.
**Original example:** Every subsection: "X is… For example… This is useful when…"
**Improved example:** The core concept gets a definition and example; the edge case gets a counterexample; the alternative gets a comparison.
**Explanation of improvement:** Form follows the explanatory need.
**Appropriate exceptions:** Glossaries and encyclopedias use consistent entry templates so readers can compare entries.

### AWP-111 — The problem-solution loop
**Category:** Repetitive explanatory structures
**Description:** The text repeatedly poses a small problem and immediately resolves it.
**Linguistic characteristics:** "But there is a problem… The solution is…" repeated in each section.
**Why it can weaken writing:** It manufactures tension and resolution, which can make a straightforward explanation feel like a sales pitch.
**Recognition criteria:** Count the loops. If a resolution does not change the analysis, it is a device.
**Original example:** "But what about errors? We handle them with retries. But what about timeouts? We handle them with retries."
**Improved example:** "Retries cover both transient errors and timeouts; the backoff schedule is the same for each."
**Explanation of improvement:** One mechanism covers both cases.
**Appropriate exceptions:** Troubleshooting guides legitimately use problem-solution pairs; each pair should describe a distinct failure.

### AWP-112 — The mirrored exception
**Category:** Repetitive explanatory structures
**Description:** Every rule is immediately followed by a symmetrical exception.
**Linguistic characteristics:** "However, there are exceptions…" after each principle; the exception often restates a previous one.
**Why it can weaken writing:** Constant exception-making dilutes the rule and gives the reader no hierarchy of importance.
**Recognition criteria:** Ask which exception actually changes behavior. Keep those; group the rest in a limitations section.
**Original example:** "Use active voice. However, passive voice is sometimes appropriate. However, active voice usually works."
**Improved example:** "Use active voice except when the actor is unknown or irrelevant, as in 'the backup was deleted.'"
**Explanation of improvement:** One bounded exception replaces a loop.
**Appropriate exceptions:** Legal rules require exhaustive exceptions; organize them by condition rather than repeating them.

---

## 29. Unnecessary meta-commentary

### AWP-113 — The process narration
**Category:** Unnecessary meta-commentary
**Description:** The text narrates the writer's process instead of presenting the result.
**Linguistic characteristics:** "I will now…", "Let me walk you through…", "First, I will analyze…"
**Why it can weaken writing:** The reader cares about the result, and the narration adds a layer between them and it.
**Recognition criteria:** Delete the sentence describing what the text will do. If the text still does it, the narration was unnecessary.
**Original example:** "I will now break down the three main factors that influence the outcome."
**Improved example:** "Three factors drive the outcome: queue depth, retry policy, and database contention."
**Explanation of improvement:** The content arrives without an announcement.
**Appropriate exceptions:** Live demonstrations and screen recordings benefit from narration because the audience is following in real time.

### AWP-114 — The self-assessment
**Category:** Unnecessary meta-commentary
**Description:** The text evaluates its own quality or difficulty.
**Linguistic characteristics:** "This is a complex topic," "This explanation is comprehensive," "I have carefully considered…"
**Why it can weaken writing:** Self-assessment is not evidence, and it invites the reader to test the claim against a text that may not support it.
**Recognition criteria:** Remove the evaluation. If the text is comprehensive, the reader will notice.
**Original example:** "This is a comprehensive and nuanced analysis of the factors involved."
**Improved example:** "The analysis compares four studies and finds that only two control for baseline traffic."
**Explanation of improvement:** The description of the work replaces the self-praise.
**Appropriate exceptions:** Abstracts sometimes state scope ("this review covers 2015–2024") because the boundary is information.

### AWP-115 — The reader instruction
**Category:** Unnecessary meta-commentary
**Description:** The text tells the reader how to read it.
**Linguistic characteristics:** "Note that," "Keep in mind that," "It is worth emphasizing," "As you can see."
**Why it can weaken writing:** It directs attention instead of earning it, and "as you can see" often points to something the reader cannot see.
**Recognition criteria:** Delete the instruction. If the sentence still makes the point, the instruction was scaffolding.
**Original example:** "As you can see, the second graph shows a clear upward trend."
**Improved example:** "Downloads rose from 2,000 to 11,000 between January and June."
**Explanation of improvement:** The observation is stated rather than assigned.
**Appropriate exceptions:** Guides for complex interfaces may need explicit attention cues ("check the box labeled…"), because the reader is performing a task.

### AWP-116 — The difficulty disclaimer
**Category:** Unnecessary meta-commentary
**Description:** The text warns that the material is hard before presenting it.
**Linguistic characteristics:** "This may be difficult to understand," "advanced readers only," "brace yourself."
**Why it can weaken writing:** It can create anxiety, and it is usually inaccurate: the difficulty is specific, not global.
**Recognition criteria:** Name what makes the material demanding (a prerequisite, a notation, a dataset). That is more useful than a warning.
**Original example:** "This section is quite technical, so it may be hard to follow."
**Improved example:** "This section assumes familiarity with Bayesian updating; the notation follows Gelman et al. (2013)."
**Explanation of improvement:** The prerequisite is stated, and the reader can decide.
**Appropriate exceptions:** Safety warnings before hazardous procedures are not meta-commentary; they are necessary.

---

## 30. Generic comparisons

### AWP-117 — The apples-and-oranges comparison
**Category:** Generic comparisons
**Description:** Two things are compared on a dimension where they are not equivalent.
**Linguistic characteristics:** A prototype compared with a production system; a library compared with a platform; different benchmarks.
**Why it can weaken writing:** The comparison produces a conclusion that does not follow and can mislead a decision.
**Recognition criteria:** Ask whether both items are measured the same way, at the same scale, for the same task.
**Original example:** "Our tool is faster than Kubernetes."
**Improved example:** "Our scheduler starts a single container in 40 ms; Kubernetes took 2.1 s to schedule the same pod on the same node."
**Explanation of improvement:** The task, environment, and measure match.
**Appropriate exceptions:** Deliberate category comparisons can be useful for illustration if the text marks the mismatch.

### AWP-118 — The prestige comparison
**Category:** Generic comparisons
**Description:** A product or idea is compared with a famous one to borrow credibility.
**Linguistic characteristics:** "The GitHub of X," "the Stripe of Y," "an Uber for Z."
**Why it can weaken writing:** The analogy names a business model, not a property, and it often says less than a plain description.
**Recognition criteria:** Ask what property is being borrowed. State that property directly.
**Original example:** "We are building the Stripe of internal tools."
**Improved example:** "We provide a single API for internal tools to charge other departments, with usage metering and monthly invoicing."
**Explanation of improvement:** The function replaces the analogy.
**Appropriate exceptions:** A shorthand analogy can orient investors quickly; follow it immediately with the specific mechanism.

### AWP-119 — The false equivalence
**Category:** Generic comparisons
**Description:** Two things are treated as comparable because they share a surface feature.
**Linguistic characteristics:** "Writing code is like writing prose"; "managing a team is like conducting an orchestra."
**Why it can weaken writing:** Shared vocabulary hides different constraints, and the analogy can lead to bad transfer.
**Recognition criteria:** List where the analogy holds and where it breaks. If the breaks matter for the decision, state them.
**Original example:** "Managing a team is like conducting an orchestra; everyone must play in harmony."
**Improved example:** "A team lead sets the tempo and resolves conflicts, but unlike a conductor, cannot choose who joins the orchestra."
**Explanation of improvement:** It names the analogy's limit.
**Appropriate exceptions:** Teaching analogies are valuable when the text explicitly marks the boundary.

### AWP-120 — The metric substitution
**Category:** Generic comparisons
**Description:** A measurable proxy is compared while the actual goal is something else.
**Linguistic characteristics:** Lines of code as a measure of quality; hours worked as a measure of output; stars as a measure of usefulness.
**Why it can weaken writing:** Optimizing the proxy can move away from the goal, and the comparison can make a worse choice look better.
**Recognition criteria:** Ask what the reader actually cares about and whether the metric tracks it. If not, report both or choose a better measure.
**Original example:** "Our team wrote 40% more code than last quarter."
**Improved example:** "The team closed 40% more support tickets, and the reopened-ticket rate stayed at 3%."
**Explanation of improvement:** The metric is tied to a customer outcome and checked for quality.
**Appropriate exceptions:** Proxies are acceptable when the real measure is expensive, provided the text says so and monitors for drift.

---

## Using the encyclopedia responsibly

**Frequency matters more than presence.** A single em dash, one rhetorical question, or one three-item list is normal English. A pattern becomes a quality problem when it recurs without purpose, when it obscures meaning, or when it appears in a genre that does not call for it.

**Genre matters more than fashion.** A legal contract, a lab report, and a text message follow different conventions. Formal, structured, and grammatically correct writing is not artificial by definition. See [context-awareness.md](context-awareness.md).

**Meaning outranks style.** Never remove a qualification, a technical term, or a necessary repetition to make a passage read more naturally. See [editing-guidelines.md](editing-guidelines.md) and [../tests/meaning-preservation.md](../tests/meaning-preservation.md).

**Detectors are not arbiters.** No pattern list can establish authorship. See [detector-reliability.md](detector-reliability.md).

Back to [SKILL.md](../SKILL.md).

