---
name: humansignal
version: 2.1.0
type: agent-skill
language: en
entrypoint: SKILL.md
repository: https://github.com/Ahaduzzamankhan/humansignal
raw_base: https://raw.githubusercontent.com/Ahaduzzamankhan/humansignal/main
description: >
  Linguistic analysis and natural-writing refinement for English prose.
  120 writing-pattern observations, 5 context modes, 70 worked examples,
  and a meaning-preservation protocol. Not a detector-evasion tool.
modes:
  - academic
  - technical
  - conversational
  - professional
  - creative
license: none-declared
---

# Human Signal — agent installation contract

**If you are an AI agent and the user pasted this file's URL, install and activate the skill, then report the result.** Follow sections 2 through 7. Do not stop at a summary of this document.

If the user only asked what this file is, answer briefly and ask whether they want it installed. Do not write outside the workspace without the approval your host requires.

---

## 1. What you are installing

Human Signal is a Markdown-only skill for editing English prose. It contains no executable code, no build step, and no dependencies.

| Component | Path | Contents |
|---|---|---|
| Entry point | `SKILL.md` | Operating rules, workflow, modes, integrity rules |
| References | `references/` | 11 files: patterns, sentences, paragraphs, vocabulary, analysis, detectors, academic, technical, context, editing, principles |
| Modes | `modes/` | 5 files: academic, technical, conversational, professional, creative |
| Examples | `examples/` | 70 worked cases: 40 general, 10 academic, 10 technical, 10 conversational |
| Tests | `tests/` | Quality checklist, meaning-preservation protocol, 12 regression cases |

**Version:** 2.1.0. **Language:** English only. **License:** none declared (see section 9).

What it does: diagnoses vague, formulaic, or mechanical prose; improves clarity, specificity, cohesion, and register fit; preserves voice, technical terms, and factual meaning.

What it does not do: evade AI detectors, promise lower detection scores, fabricate sources or data, or certify legal, medical, or financial correctness.

---

## 2. Install

Choose **one** method. Prefer git when available, because updates are verifiable with `git pull`.

### 2.1 Choose the skills directory

Use the skills directory documented by your runtime. Common locations, as examples only:

- OpenCode: `~/.config/opencode/skills/`
- Claude Code: `~/.claude/skills/`
- Codex-style runtimes: `~/.codex/skills/`

If the correct directory is not documented and cannot be inferred, ask the user for one absolute path. State the path you chose in your final report. Do not install into a random directory.

### 2.2 Method A — git clone (preferred)

Bash:

```bash
# Replace with the absolute path for your runtime.
SKILLS_DIR="/absolute/path/to/skills"

mkdir -p "$SKILLS_DIR"
git clone --depth 1 https://github.com/Ahaduzzamankhan/humansignal.git "$SKILLS_DIR/humansignal"
test -f "$SKILLS_DIR/humansignal/SKILL.md" && echo "Human Signal installed"
```

PowerShell:

```powershell
# Replace with the absolute path for your runtime.
$SkillsDir = "C:\absolute\path\to\skills"

New-Item -ItemType Directory -Force -Path $SkillsDir | Out-Null
git clone --depth 1 https://github.com/Ahaduzzamankhan/humansignal.git "$SkillsDir\humansignal"
Test-Path "$SkillsDir\humansignal\SKILL.md"
```

If the destination already exists, do not delete it blindly. Check its version first:

```bash
grep -m1 '^version:' "$SKILLS_DIR/humansignal/SKILL.md"
```

If it is already 2.1.0 or newer, skip to section 3. If it is older and the directory has no local changes, update it with:

```bash
git -C "$SKILLS_DIR/humansignal" pull --ff-only
```

If it has local changes, ask the user before replacing anything.

### 2.3 Method B — tarball (no git)

Bash:

```bash
SKILLS_DIR="/absolute/path/to/skills"
TMP_DIR="$(mktemp -d)"

curl -fsSL https://github.com/Ahaduzzamankhan/humansignal/archive/refs/heads/main.tar.gz -o "$TMP_DIR/humansignal.tar.gz"
mkdir -p "$SKILLS_DIR/humansignal"
tar -xzf "$TMP_DIR/humansignal.tar.gz" -C "$SKILLS_DIR/humansignal" --strip-components=1
rm -rf "$TMP_DIR"
test -f "$SKILLS_DIR/humansignal/SKILL.md" && echo "Human Signal installed"
```

Windows 10 and later ship `tar`. On PowerShell, use the same `curl` and `tar` commands if available, or download the archive with `Invoke-WebRequest` and extract it with `Expand-Archive`.

The tarball tracks the `main` branch. To pin a specific commit, append the SHA to the archive URL:

```text
https://github.com/Ahaduzzamankhan/humansignal/archive/<commit-sha>.tar.gz
```

### 2.4 Method C — local checkout

If the repository already exists on disk, copy the whole directory, including hidden files, into the skills directory. Do not copy only `SKILL.md`; the relative links to `references/`, `modes/`, `examples/`, and `tests/` will break.

### 2.5 Method D — context-only (no filesystem access)

If you cannot write files, load the essential files into context and operate from them for this session. Fetch raw text over HTTPS:

```bash
curl -fsSL https://raw.githubusercontent.com/Ahaduzzamankhan/humansignal/main/SKILL.md
curl -fsSL https://raw.githubusercontent.com/Ahaduzzamankhan/humansignal/main/references/editing-guidelines.md
curl -fsSL https://raw.githubusercontent.com/Ahaduzzamankhan/humansignal/main/references/context-awareness.md
curl -fsSL https://raw.githubusercontent.com/Ahaduzzamankhan/humansignal/main/modes/technical.md
```

Minimum viable set:

1. `SKILL.md`
2. `references/editing-guidelines.md`
3. `references/context-awareness.md`
4. One mode file for the current task

Fetch other references only when the task needs them. The pattern encyclopedia (`references/ai-writing-patterns.md`) is large; search it on demand rather than loading all 120 entries by default.

In context-only mode, say so clearly in the final report. Do not claim the skill was installed to disk.

---

## 3. Verify the installation

Run the checks appropriate to the method you used.

```bash
cd "$SKILLS_DIR/humansignal"   # or the path you installed to

# 1. Version must be 2.1.0.
grep -m1 '^version:' SKILL.md

# 2. Required files must exist.
for f in \
  references/ai-writing-patterns.md \
  references/editing-guidelines.md \
  references/context-awareness.md \
  references/detector-reliability.md \
  modes/academic.md \
  modes/technical.md \
  modes/conversational.md \
  modes/professional.md \
  modes/creative.md \
  examples/english-examples.md \
  tests/quality-checklist.md \
  tests/meaning-preservation.md \
  tests/regression-cases.md
do
  test -f "$f" || echo "MISSING: $f"
done

# 3. Confirm the pattern count is 120.
grep -c '^### AWP-' references/ai-writing-patterns.md
```

Expected: `version: 2.1.0`, no `MISSING` lines, and `120`.

If a required file is missing, the copy is incomplete. Reinstall with git or the tarball; do not patch around the gap.

---

## 4. Activate the skill

1. Read `SKILL.md` completely before the first edit.
2. Read `references/editing-guidelines.md` for the 16-step workflow and preservation rules.
3. Load exactly one mode file for the current task. Select by purpose, not surface formality.
4. Keep the pattern encyclopedia as a lookup. Do not apply all 120 observations as a checklist.
5. For an audit, also load `tests/quality-checklist.md` and `tests/meaning-preservation.md`.

Then state the activation in one line:

```text
Human Signal 2.1.0 active — mode: <academic|technical|conversational|professional|creative>
```

If no task has been supplied yet, say the skill is installed and ask for the text plus its intended reader and purpose.

---

## 5. Operating contract

These rules are summarized from `SKILL.md`. If this summary conflicts with `SKILL.md`, `SKILL.md` wins.

1. **Meaning is the invariant.** Never change a claim, condition, scope, number, citation, or technical detail to improve style.
2. **Find the problem before changing the sentence.** A change without a located, described problem is a preference, not an edit.
3. **Minimum effective edit.** Prefer deletion, then reordering, then a word or phrase, then a sentence, and only then a section.
4. **Precision outranks variety.** Repeat a term when the referent is the same. Do not rotate synonyms around one technical entity.
5. **Protect terminology.** Identifiers, API names, commands, defaults, units, and terms of art are data, not prose.
6. **No invention.** Do not add facts, figures, examples, sources, quotes, experience, or credentials. If specificity is missing, flag the gap.
7. **Preserve voice and register.** Do not flatten a distinctive voice into neutral prose or make a peer message ceremonial.
8. **Respect genre.** A README, a lab report, a memo, and a chat message follow different conventions.
9. **No detector framing.** Do not use a detector score as a quality target or as evidence of authorship. See `references/detector-reliability.md`.
10. **English only.** Do not introduce translations, transliterations, or examples in other languages.

When instructions conflict, use this order: system and safety rules, explicit user requirements, factual and academic integrity, genre and technical accuracy, then stylistic guidance.

---

## 6. Acceptance checks

Reason through these silently to confirm the operating contract is loaded. Do not claim you ran a benchmark.

1. **Vague marketing claim.** Given "Our powerful, flexible platform helps modern teams do more," the correct behavior is to diagnose the undefined terms and request or flag the missing specifics. Inventing a 40% improvement is a failure.
2. **Technical drift.** Given "Set `timeout` to 5000," changing it to "Set `timeout_ms` to 5" is a failure. The identifier, unit, and value must be preserved.
3. **Detector request.** If asked to "make this undetectable," decline the evasion goal and offer a quality edit instead. Do not provide paraphrase procedures designed to defeat classifiers.
4. **Register drift.** Given "Can you send the link? I can't find it," do not rewrite it as "Would you kindly provide the link? I am unable to locate it." The register already fits the relationship.
5. **Good prose.** Given "Backups run nightly; restores are tested weekly," the correct edit may be no edit at all.

If any answer above feels uncertain, re-read the relevant section of `SKILL.md` before editing user text.

---

## 7. Report to the user

Use this template and fill in only what is true:

```text
Human Signal 2.1.0 installed and verified.
Path: <absolute path, or "context-only">
Method: <git | tarball | local copy | context-only>
Verified: SKILL.md, 11 references, 5 modes, 4 example files, 3 test files
Pattern count: 120
Commit: <short SHA if installed with git, otherwise "n/a">
Active mode: <mode, or "not selected yet">
Notes: <permission limits, existing installation, or context-only warning>
```

If installation failed, report the failing command and the error. Do not claim success without the version and file checks.

---

## 8. Update and uninstall

Update a git installation:

```bash
git -C "$SKILLS_DIR/humansignal" pull --ff-only
grep -m1 '^version:' "$SKILLS_DIR/humansignal/SKILL.md"
```

Update a tarball installation by repeating section 2.3 into a fresh directory. Keep the old directory until the new one verifies.

Uninstall by removing the skill directory:

```bash
rm -rf "$SKILLS_DIR/humansignal"
```

If you added a pointer in a global instruction file or memory store, remove that pointer too. Do not remove unrelated skills.

---

## 9. License and provenance

The repository contains no `LICENSE` file at the time of this release. Installing a copy for local use is not redistribution, but confirm terms with the repository owner before republishing, bundling, or selling the content.

Canonical source: `https://github.com/Ahaduzzamankhan/humansignal`

Forks and mirrors may lag or diverge. Verify the version string before reporting a successful installation. Do not silently substitute a different writing guide for this one.

---

## 10. Machine-readable summary

```json
{
  "skill": "humansignal",
  "version": "2.1.0",
  "type": "agent-skill",
  "language": "en",
  "entrypoint": "SKILL.md",
  "repository": "https://github.com/Ahaduzzamankhan/humansignal",
  "raw_base": "https://raw.githubusercontent.com/Ahaduzzamankhan/humansignal/main",
  "install": {
    "preferred": "git",
    "command": "git clone --depth 1 https://github.com/Ahaduzzamankhan/humansignal.git <skills-dir>/humansignal",
    "tarball": "https://github.com/Ahaduzzamankhan/humansignal/archive/refs/heads/main.tar.gz"
  },
  "verify": {
    "version": "2.1.0",
    "pattern_count": 120,
    "required_files": [
      "SKILL.md",
      "references/ai-writing-patterns.md",
      "references/editing-guidelines.md",
      "modes/technical.md",
      "tests/quality-checklist.md",
      "tests/meaning-preservation.md"
    ]
  },
  "modes": ["academic", "technical", "conversational", "professional", "creative"],
  "policies": {
    "detector_evasion": false,
    "fabrication": false,
    "languages": ["en"]
  },
  "license": null
}
```

---

**End of contract.** Continue with section 2 unless the skill is already installed and verified.
