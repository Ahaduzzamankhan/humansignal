# Meaning Preservation

Version 2.1.0 · Human Signal

An edit that improves style and changes meaning is a failed edit. This file defines the verification protocol, the categories that must be preserved, the acceptable reasons for changing meaning, and the documentation required when a change is intentional.

Related: [../references/editing-guidelines.md](../references/editing-guidelines.md) · [quality-checklist.md](quality-checklist.md) · [regression-cases.md](regression-cases.md)

---

## 1. Principle

**Meaning is the invariant.** Style, structure, and vocabulary are variables. The truth conditions of the text — what it claims, under what conditions, with what strength — must survive the edit.

Corollaries:

- A shorter sentence is not better if it drops a qualification.
- A clearer claim is not better if it is a different claim.
- A more natural phrase is not better if it changes the referent.
- A confident sentence is not better if the original was appropriately uncertain.

---

## 2. What must be preserved

### 2.1 Original claims

Every proposition the text asserts must remain, unless the writer authorizes its removal.

- **Check:** list each claim in the original; locate it in the revision.
- **Failure:** a claim disappears because its sentence was merged or cut.
- **Note:** claims can be reorganized and reworded; they cannot be silently dropped.

### 2.2 Intended meaning

The writer's communicative intent, including implication and emphasis.

- **Check:** does the revision support the same inference the original invited?
- **Failure:** an ironic sentence becomes literal; a recommendation becomes a neutral survey.
- **Note:** if the intent was ambiguous, resolve it with the writer, not by guessing.

### 2.3 Technical details

Identifiers, versions, parameters, units, limits, and procedures.

- **Check:** diff every technical token against the source or implementation.
- **Failure:** `timeout_ms` becomes `timeout`; `5000` becomes `5`; "MiB" becomes "MB."
- **Note:** never "clean up" an identifier for readability.

### 2.4 Important qualifications

Conditions, exceptions, scope limits, and hedges that affect the truth of a claim.

- **Check:** for each claim, confirm its conditions survived.
- **Failure:** "in this sample" disappears; "may" becomes "does"; "associated with" becomes "causes."
- **Note:** qualifications are content, not clutter.

### 2.5 Citations

Sources and their attachment to claims.

- **Check:** every citation still supports the sentence it follows.
- **Failure:** a citation is moved to a sentence it does not support; a source is dropped during restructuring.
- **Note:** never add a citation to fill a gap.

### 2.6 Numerical information

Numbers, units, precision, denominators, dates, and ranges.

- **Check:** compare digit by digit; check unit conversions; check rounding.
- **Failure:** "12%" becomes "about 10%"; "n = 412" becomes "over 400"; a date shifts.
- **Note:** do not round, convert, or "simplify" numbers without authorization.

### 2.7 Relevant context

The setting, population, timeframe, and constraints that make the claims interpretable.

- **Check:** does the revision still say where, when, and for whom?
- **Failure:** a finding from one university becomes a general claim about students.
- **Note:** context can move to another sentence, but it must remain.

---

## 3. The verification protocol

### Step 1 — Segment the original

Break the original into claim units. A claim unit is the smallest statement that can be true or false. Mark:
- the claim;
- its conditions;
- its evidence;
- its strength (certainty, probability, possibility);
- its scope (population, time, place).

### Step 2 — Segment the revision

Do the same for the revision. Do not assume a one-to-one mapping; sentences may be merged or split.

### Step 3 — Match

For each original claim, find its counterpart. Record:

| Original claim | Revision counterpart | Status |
|---|---|---|
| | | Preserved / Reworded / Merged / Split / Removed / Changed |

### Step 4 — Classify differences

- **Preserved:** same truth conditions.
- **Reworded:** different words, same meaning.
- **Merged/split:** structural change, same propositions.
- **Removed:** claim absent. Requires a reason.
- **Changed:** truth conditions differ. Requires authorization.

### Step 5 — Verify the reverse direction

Check the revision for claims that were not in the original. Additions are the most common source of meaning change, especially when a vague statement is replaced with a specific one.

### Step 6 — Check strength and scope

For each matched pair, compare:
- modality (*may / can / will / must*);
- quantification (*all / most / some / one*);
- causality (*causes / predicts / is associated with*);
- certainty (*shows / suggests / is consistent with*).

A change in any of these is a meaning change even if the topic words are identical.

### Step 7 — Record and deliver

If all differences are stylistic, the check passes. If any difference is substantive, either restore the original meaning or document the change and its reason.

---

## 4. Failure modes

| Failure | Example | Consequence |
|---|---|---|
| **Qualification drop** | "may reduce" → "reduces" | Overstates evidence |
| **Scope expansion** | "in this sample" → "in general" | Overgeneralizes |
| **Causal inflation** | "associated with" → "causes" | Misrepresents design |
| **Precision invention** | "many" → "73%" | Fabricates data |
| **Terminology drift** | "tenant" → "customer" | Ambiguous reference |
| **Referent shift** | "this limit" now points to a different limit | Misleading |
| **Condition loss** | "if the cache is cold" removed | Instruction becomes unsafe |
| **Citation slippage** | source moved to a different claim | Misattribution |
| **Emphasis shift** | caveat moved to a footnote | Changes reader's takeaway |
| **Stance change** | skeptical claim becomes endorsing | Changes the author's position |
| **Example substitution** | specific case replaced by a generic one | Loses evidentiary value |
| **Number conversion** | 1,024 MB → 1,000 MB | Factual error |

---

## 5. When meaning may change

Meaning changes are permitted only under these conditions:

1. **The writer authorizes it.** They ask for a stronger claim, a narrower scope, or a different emphasis.
2. **A factual error is corrected.** The change must be documented with the source of the correction.
3. **An unsupported claim is removed or weakened.** This is a correction, not a distortion; it must be disclosed.
4. **A contradiction is resolved.** The writer must choose which statement stands.
5. **A genre conversion requires it.** A report summarized for a general audience may drop detail, but the dropped detail must not reverse the conclusion.

In all other cases, preserve the original meaning and flag the problem instead of fixing it by changing the claim.

---

## 6. Worked checks

### Check 1 — Qualification

**Original:** "The intervention may reduce readmission rates in older patients."

**Revision A:** "The intervention reduces readmission rates in older patients."
**Status:** Changed. Modality lost (*may* → *does*). Reject or restore the hedge.

**Revision B:** "In older patients, the intervention was associated with lower readmission rates."
**Status:** Preserved with clarification. The hedge remains, and the association is explicit. Acceptable if the original's evidence was correlational.

### Check 2 — Scope

**Original:** "In the two pilot schools, attendance improved by four percentage points."

**Revision A:** "Attendance improved by four percentage points."
**Status:** Changed. The pilot scope is gone. Restore "in the two pilot schools."

**Revision B:** "Attendance in the two pilot schools rose four percentage points."
**Status:** Preserved. Same scope, same measure.

### Check 3 — Specificity

**Original:** "The new process significantly reduced handling time."

**Revision A:** "The new process cut handling time from 14 to 6 minutes."
**Status:** Changed unless the writer supplied these figures. The revision invents precision. Reject or ask for the data.

**Revision B:** "The new process reduced handling time; the measured baseline and result are in the appendix."
**Status:** Preserved if the appendix exists. Otherwise, flag the missing measurement.

### Check 4 — Technical detail

**Original:** "Set `timeout` to 5000."

**Revision:** "Set `timeout_ms` to 5."
**Status:** Changed twice: identifier renamed and value converted without a unit change. Reject.

### Check 5 — Citation

**Original:** "Remote work raised productivity in one call-center study [12], though the effect may not generalize."

**Revision:** "Remote work raises productivity [12]."
**Status:** Changed. Qualification dropped, tense shifted, citation now supports a broader claim. Reject.

### Check 6 — Stance

**Original:** "The proposal is technically feasible, but the cost estimates are optimistic."

**Revision:** "The proposal is technically feasible and the cost estimates are reasonable."
**Status:** Changed. The author's skepticism is reversed. Reject.

---

## 7. Preservation matrix

Use this matrix for a fast review of a revised passage.

| Dimension | Question | Pass condition |
|---|---|---|
| Claims | Are all original claims present? | No silent removals |
| Strength | Is modality unchanged? | *May* stays *may* |
| Scope | Is the population/time/place unchanged? | No widening or narrowing |
| Causality | Is the design-claim match unchanged? | Correlation stays correlation |
| Numbers | Are values and units identical? | Digit-for-digit match |
| Terms | Are identifiers and key terms identical? | No synonym substitution |
| Conditions | Are exceptions and prerequisites present? | No dropped *if* clauses |
| Citations | Does each source still support its claim? | No slippage |
| Emphasis | Is the relative importance unchanged? | Caveats not demoted |
| Additions | Does the revision add any claim? | No invented facts |
| Voice | Is the author's stance unchanged? | No confidence inflation |
| Genre | Is the level of detail appropriate? | Compression does not reverse meaning |

---

## 8. Documentation of intentional changes

When a meaning change is authorized or required, record it in this form:

```
Location: [section / paragraph / sentence]
Original claim: [quote]
Revised claim: [quote]
Type of change: [weakened / narrowed / corrected / removed / reframed]
Reason: [writer request / factual correction / unsupported claim / contradiction]
Evidence: [source or writer instruction]
Effect on conclusions: [none / qualifies / changes]
```

Deliver this record with the edit when the user asked for an audit. For ordinary edits, summarize material changes in one or two sentences.

---

## 9. Red flags during verification

Stop and re-check if you notice any of these:

- The revision is much more specific than the original.
- The revision is much more confident than the original.
- A hedge or qualifier is gone.
- A citation moved.
- A number changed format or unit.
- A technical term was "cleaned up."
- A caveat became a footnote or a final sentence.
- A new example appeared that the writer did not provide.
- The conclusion is stronger than the body supports.
- The revision sounds better but says something different.

Any one of these requires a full claim-by-claim comparison before delivery.

---

## 10. Sign-off

```
Original text: ______________________________
Revised text: _______________________________
Claims checked: ______ / ______
Differences found: __________________________
Differences authorized: _____________________
Evidence for corrections: ___________________
Meaning verdict: PRESERVED / PRESERVED WITH NOTES / CHANGED
Reviewer: ___________________________________
Date: _______________________________________
```

A verdict of CHANGED is acceptable only when every change is documented and authorized. It is never acceptable to deliver a CHANGED text as if it were PRESERVED.

Back to [SKILL.md](../SKILL.md).
