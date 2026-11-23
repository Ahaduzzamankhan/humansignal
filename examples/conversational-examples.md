# Conversational Examples

Version 2.1.0 · Human Signal

Ten worked examples in conversational writing. Each follows the same seven-part structure. The revisions preserve the relationship and the register; they do not turn messages into reports.

Related: [../modes/conversational.md](../modes/conversational.md) · [../references/context-awareness.md](../references/context-awareness.md) · [english-examples.md](english-examples.md)

---

## CON-01 — Ceremonial request

**Original:** "I hope this message finds you well. I am writing to respectfully request that you provide me with an update regarding the status of the migration project at your earliest convenience."

**Issues:** Three ceremonial frames; passive indirection; "at your earliest convenience" gives no deadline.

**Analysis:** The message contains one request: an update on the migration. Three sentences delay it, and the deadline is left to the reader's interpretation.

**Explanation:** Ceremony signals distance and can make a routine request feel heavier than it is. The missing deadline also makes the request easy to defer.

**Revised:** "Any update on the migration? I need to tell the vendor by Thursday whether the cutover is still on for the 12th."

**Improvements:** The question comes first, the deadline is explicit, and the reason is given.

**Meaning preserved:** Yes. The request is unchanged; the social distance is reduced, which fits a colleague relationship.

---

## CON-02 — Burying the ask

**Original:** "I've been looking at the logs from Tuesday and comparing them with the ones from last week, and I noticed that the error rate seems to have gone up a bit, though it might just be the deploy, and I was also thinking about the dashboard, which could probably use a new panel. Anyway, let me know what you think."

**Issues:** Three topics in one message; the ask is "let me know what you think," which is not an ask; no clear question.

**Analysis:** The message contains an observation (error rate), a hypothesis (the deploy), and an idea (dashboard panel). It ends with an open request for a reaction.

**Explanation:** The reader must decide which item matters and what response is wanted. In chat, that usually produces no response or a generic one.

**Revised:** "Error rate on the API doubled after Tuesday's deploy. Can you check whether the retry change went out? I'll look at the dashboard separately."

**Improvements:** One question, one hypothesis, one owner, one deferral.

**Meaning preserved:** Yes, except the dashboard idea is postponed rather than dropped. If the writer wanted a decision on it, it should be a second message.

---

## CON-03 — Over-formal chat

**Original:** "Furthermore, I would like to formally acknowledge your assistance with the deployment issue, which was resolved in a timely and efficient manner."

**Issues:** "Furthermore"; "formally acknowledge"; "timely and efficient manner"; no specific content.

**Analysis:** The message thanks someone in the register of a performance review. It does not say what the person did or why it helped.

**Explanation:** Register mismatch in a chat channel reads as cold or performative. Specific thanks is also more meaningful than generic praise.

**Revised:** "Thanks for catching the port conflict — that would have taken me another hour."

**Improvements:** Specific action, specific consequence, natural register.

**Meaning preserved:** Yes. The gratitude is retained and made concrete.

---

## CON-04 — Passive-aggressive follow-up

**Original:** "Just following up again on my previous email. I haven't heard back, which is a bit disappointing given the timeline. Let me know if this is a priority for you."

**Issues:** "Just"; repeated follow-up with no new information; implied criticism; passive-aggressive closing question.

**Analysis:** The message expresses frustration through implication. It does not state the deadline, the consequence, or a concrete request.

**Explanation:** Implied criticism puts the reader on the defensive without giving them a way to respond. A direct statement of need is fairer and more effective.

**Revised:** "I still need the signed contract by Friday to keep the 30 June start date. If that's not possible, tell me today and I'll ask for an extension."

**Improvements:** The deadline, the consequence, and the alternative are explicit. The tone is firm without being hostile.

**Meaning preserved:** Yes. The frustration is replaced by its cause, which is more useful.

---

## CON-05 — Filler praise

**Original:** "Great question! There are so many factors to consider here. First, you should check the logs. Second, you should check the configuration. Third, you should check the network. Hope this helps!"

**Issues:** Praise before content; generic three-step checklist; no diagnostic reasoning; "Hope this helps" with no next step.

**Analysis:** The answer lists three common causes without indicating which is likely or how to distinguish them. The opening praise delays the content.

**Explanation:** A checklist transfers the diagnostic work back to the reader. A useful answer narrows the likely cause and gives a test.

**Revised:** "Check the logs first. If you see `ECONNREFUSED`, the config is pointing at the old port — that's the usual cause after Tuesday's change. If the logs are clean, it's probably the network policy; send me the output and I'll take a look."

**Improvements:** A likely cause, a diagnostic signal, and a fallback replace the generic list.

**Meaning preserved:** Yes, if those are the plausible causes. The revision commits to a hypothesis, which the original avoided.

---

## CON-06 — Ambiguous pronoun request

**Original:** "Can you check it before tomorrow? I think it's wrong, but I'm not sure."

**Issues:** Two "it" pronouns with no antecedent; no location; no criterion for "wrong."

**Analysis:** The reader cannot tell what to check, where to find it, or what would count as correct. The message is short and unusable.

**Explanation:** Shared context is often assumed in chat, but pronouns still need a recoverable referent. Naming the object costs one clause and prevents a round trip.

**Revised:** "Can you check the staging config before tomorrow? I think `REDIS_URL` still points at the old cluster."

**Improvements:** The object and the suspected error are named.

**Meaning preserved:** Yes, assuming this was the intended referent. If the writer meant a document or a deploy, the same fix applies with a different noun.

---

## CON-07 — Formatting inflation in chat

**Original:**
> ## Update
> **Status:** In progress
> **Owner:** Me
> **Next steps:**
> - **Step 1:** Investigate
> - **Step 2:** Fix
> - **Step 3:** Verify

**Issues:** Headings and bold in a chat message; three content-free steps; no specifics.

**Analysis:** The formatting implies a status report, but the content is a placeholder. "Investigate," "fix," and "verify" describe every task.

**Explanation:** Formatting should match the channel and the content. In chat, a heading and three bold labels cost more attention than they return.

**Revised:** "Still on the payment bug. I've reproduced it locally; the next step is testing whether the retry change caused it. I'll know by 3."

**Improvements:** The status, the specific investigation, and a time for the next update replace the template.

**Meaning preserved:** Yes, at a higher level of specificity.

---

## CON-08 — Softened bad news

**Original:** "Unfortunately, there may have been a slight issue with the release, and it's possible that some users might experience some minor inconvenience."

**Issues:** Four hedges; "slight," "minor," "some" minimize; no scope or action.

**Analysis:** The message does not say what happened, how many users are affected, or what is being done. The hedges protect the writer at the reader's expense.

**Explanation:** Bad news should be stated plainly and early, with scope and next steps. Softening delays understanding and can damage trust when the facts emerge.

**Revised:** "The 14:02 release broke checkout for about 12 minutes. Roughly 400 orders failed; we've rolled back and are contacting affected customers. I'll post a timeline by 5."

**Improvements:** What happened, how long, how many, what was done, and what comes next.

**Meaning preserved:** No, unless these are the facts. The revision demonstrates the required specificity; the writer must supply the real numbers.

---

## CON-09 — Forced closing question

**Original:** "I've attached the revised budget. Let me know if you have any questions or concerns. Is there anything else I can help you with today?"

**Issues:** Two closing offers; the second is a support script in a peer conversation.

**Analysis:** The message ends with two generic invitations that give the reader nothing to respond to unless they already have a question.

**Explanation:** Generic closings are polite but low-information. A specific next step is more useful and often shorter.

**Revised:** "I've attached the revised budget. The only change is the cloud line, up $4,200. Can you approve it by Wednesday so finance can process it this cycle?"

**Improvements:** The change is summarized, and the ask has a deadline and a reason.

**Meaning preserved:** Yes, and it adds the decision the reader needs to make.

---

## CON-10 — Friendly but unclear

**Original:** "Hey! So about the thing we talked about — I think we should probably go with the other option, but let me know what you think, no rush."

**Issues:** "The thing," "the other option," "probably"; no referents; "no rush" removes any timeline.

**Analysis:** The message depends entirely on a conversation the reader may not remember in detail. It states a preference without naming the decision or the alternative.

**Explanation:** Conversational warmth does not require vagueness. Naming the decision and the choice makes the message easier to answer without making it colder.

**Revised:** "About the vendor choice — I'd go with the smaller one, mostly because the contract is month-to-month. Can you confirm by Friday?"

**Improvements:** The topic, the preference, the reason, and the timeline are explicit. The tone remains casual.

**Meaning preserved:** Yes, if that was the decision and the reason. The revision removes "probably," which was doing no work.

---

## Cross-example observations

- **Warmth and clarity are compatible.** None of the revisions is cold; several are warmer because they are specific.
- **Directness is not rudeness.** CON-04 and CON-08 become firmer and more respectful by stating facts instead of implying them.
- **Register is a constraint.** CON-01 and CON-03 would be wrong in the opposite direction: a close colleague does not need ceremony, but a first contact might.
- **Specificity usually requires information.** Where the original was vague, the revision is a model, not a substitution; the writer must supply the facts.

See [../modes/conversational.md](../modes/conversational.md) and [../references/context-awareness.md](../references/context-awareness.md).

Back to [SKILL.md](../SKILL.md).
