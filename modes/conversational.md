# Conversational Mode

Version 2.1.0 · Human Signal

## Intended use

Chat messages, short email exchanges, forum replies, support conversations, internal threads, and any writing where the reader is a specific person in an ongoing relationship.

Use this mode when shared context is high, response time is short, and the purpose is to communicate rather than to document. Do not use it for contracts, specifications, or research reports; the compression will lose precision.

## Tone

Natural, direct, and considerate. The writer sounds like a person talking to a colleague, not like a company issuing a notice.

Warmth is optional; clarity is not. A reply can be friendly, neutral, or brisk, as long as it is not rude and does not bury the answer.

## Vocabulary

- Use everyday words: "use," "start," "fix," "check," "send."
- Contractions are normal: "I'll," "we're," "doesn't."
- Phrasal verbs are normal: "set up," "look into," "follow up."
- Domain terms are fine when both people share them; do not define them.
- Avoid: corporate jargon ("circle back," "align on," "bandwidth"), ceremonial phrasing ("please be advised"), and inflated verbs ("utilize," "commence").
- Emoji are acceptable when the relationship and channel support them; they are not punctuation.

## Sentence characteristics

- Short sentences, often with one clause.
- Fragments are acceptable in chat when the meaning is clear ("On it." "Makes sense.").
- Direct questions are normal: "Can you send the log?"
- Ellipsis of shared context is normal: "Same issue as yesterday."
- Avoid stacking hedges or formal frames; they read as distance.
- Match the other person's register. If they write two lines, do not reply with six paragraphs unless the content requires it.

## Paragraph structure

- Lead with the answer, the request, or the update.
- One topic per message where possible.
- Use a list only when there are genuinely several items.
- No headings in chat. In email, a short subject line and a first sentence that states the purpose.
- Put the deadline and the ask where they are easy to find.

## Common mistakes

1. **Burying the ask.** Three paragraphs of context before the question.
2. **Over-formality.** "I hope this message finds you well" in a thread with a teammate.
3. **Under-formality in a sensitive message.** Jokes or fragments when delivering bad news.
4. **Passive-aggressive hedging.** "Just following up again…" repeated with no new information.
5. **Over-explaining.** Telling a colleague how their own system works.
6. **Formatting inflation.** Headings and bold in a two-line reply.
7. **Forced engagement.** Ending every message with a question.
8. **Empty filler.** "Great question!" before an answer.
9. **Ambiguous pronouns.** "Can you check it?" with three possible referents.
10. **Missing context.** A reply that assumes a thread the reader cannot see.

## Editing rules

1. Put the purpose in the first sentence.
2. Cut greetings that delay the point, unless the relationship calls for them.
3. Make the ask and the deadline explicit.
4. Replace "let me know if you have any questions" with a specific next step.
5. Preserve the writer's warmth; do not make a friendly message cold.
6. Do not add slang the writer would not use.
7. Keep the message as short as the content allows, not shorter.
8. If the news is bad, state it plainly and early.
9. Match the channel: no headings in chat, no walls of text in a direct message.
10. Do not manufacture familiarity.

## Examples

**Before:**
> I hope this message finds you well. I am writing to inquire as to whether you might possibly be able to provide an update on the status of the deployment at your earliest convenience.

**After:**
> Is the deploy done? If not, what's blocking it?

**Why:** It asks the question, offers the useful follow-up, and removes six layers of ceremony.

**Before:**
> Great question! There are several factors to consider here. First, you should check the logs. Second, you should check the config. Third, you should check the network. Let me know if you need anything else!

**After:**
> Check the logs first — if you see `ECONNREFUSED`, the config is pointing at the old port. Otherwise it's probably the network policy.

**Why:** It replaces a generic checklist with a diagnostic path and a likely cause.

**Before:**
> Per my previous message, I wanted to circle back and align on the deliverables.

**After:**
> I still need the two test files by Friday. Can you send them today?

**Why:** It names the items, the deadline, and the new request.

**Before:**
> We need to talk about the incident.

**After:**
> The 14:02 deploy dropped requests for about 90 seconds. I rolled it back; can we review the logs at 4?

**Why:** It states what happened, what was done, and what happens next.

## Checklist

- [ ] The purpose is in the first sentence.
- [ ] The ask and deadline are explicit.
- [ ] The register matches the relationship and channel.
- [ ] No unnecessary ceremony.
- [ ] No jargon the reader does not share.
- [ ] Pronouns have clear referents.
- [ ] No formatting inflation.
- [ ] Warmth, if present, is the writer's own.
- [ ] Length matches the content.
- [ ] No forced closing question.

See [../references/context-awareness.md](../references/context-awareness.md) and [../examples/conversational-examples.md](../examples/conversational-examples.md).

Back to [SKILL.md](../SKILL.md).
