# Detector Technology and Reliability

Version 2.1.0 · Human Signal

## Purpose of this file

Writers and editors increasingly encounter "AI detection" scores. This file explains, in plain technical terms, what such systems measure, how they are evaluated, why they fail, and why a detector score cannot establish authorship. It does **not** describe how to evade detection. Human Signal improves writing quality; it does not optimize for detector output.

Two claims frame everything below:

1. **A detector estimates a statistical property of a text sample.** It does not observe how the text was produced.
2. **Detection accuracy is conditional.** It depends on the model, the domain, the language, the text length, and the population being tested. A number without those conditions is not evidence.

Related: [linguistic-analysis.md](linguistic-analysis.md) · [ai-writing-patterns.md](ai-writing-patterns.md) · [editing-guidelines.md](editing-guidelines.md)

---

## 1. What detection systems try to measure

Most detectors look for one or more of the following:

- **Predictability:** how unsurprising each token is given its context.
- **Variation:** how much predictability fluctuates across a text.
- **Distributional signatures:** frequencies of words, n-grams, or syntactic constructions that differ between human and machine corpora.
- **Learned representations:** features extracted by a neural network trained to separate two labeled sets.
- **Provenance artifacts:** watermarks, metadata, or sampling signatures inserted by a particular generator.

Each is a proxy. None directly measures "human authorship," which is not a property of the text's surface form.

## 2. Perplexity

**Definition.** Perplexity is a function of the probability a language model assigns to a sequence. For a token sequence \(w_1 \dots w_N\):

\[
\mathrm{PPL} = \exp\left(-\frac{1}{N}\sum_{i=1}^{N}\log p(w_i \mid w_1 \dots w_{i-1})\right)
\]

Lower perplexity means the model found the text more predictable.

**What it captures.** How well a particular model predicts the text. A text that follows common patterns closely will have low perplexity under a model trained on similar text.

**What it does not capture.** Authorship, quality, originality, or truth. Formulaic human writing (templates, legal boilerplate, sports recaps) also has low perplexity. Unusual human writing (experimental poetry, dense technical prose with rare terms) can have high perplexity.

**Critical dependency.** Perplexity is always relative to a specific model. A score computed with one model is not comparable to a score computed with another, and a threshold calibrated on one corpus does not transfer automatically.

**Practical consequence.** "This text has low perplexity" means "this model predicts it well." It does not mean "a machine wrote it," because the model may simply be familiar with the genre.

## 3. Burstiness

**Definition.** Burstiness measures how much a property varies across a text — commonly, the variance of sentence-level perplexity or token probability. High burstiness means the text alternates between predictable and surprising stretches; low burstiness means it is uniformly predictable.

**Why it was used.** Early detectors observed that machine-generated text often had more uniform token-level predictability than human text, which tends to mix routine phrasing with idiosyncratic choices.

**Limitations.**
- Burstiness depends on text length: short samples produce unstable estimates.
- It is genre-sensitive. Edited formal prose is deliberately uniform; transcribed speech is highly bursty.
- It can be altered by paraphrasing without changing authorship, which shows it is not a measure of authorship.

**What it is not.** Burstiness is not a validated measure of human style. It is one statistic among many, and its discriminative power varies by dataset.

## 4. Token distributions

**Definition.** A token distribution describes how likely each possible next token is at a given position. Detectors can summarize these distributions across a text: mean log-probability, entropy, rank of the observed token, and the shape of the tail.

**Signals sometimes used.**
- **Mean token rank:** the average rank of the chosen token under a reference model.
- **Entropy:** how spread out the model's predictions were.
- **Top-k concentration:** how often the chosen token was among the model's top candidates.
- **Tail behavior:** the frequency of low-probability choices.

**Caveats.**
- Tokenization differs across models, so distributions are not directly comparable.
- A text can be highly predictable in one model and surprising in another.
- Human writers who edit heavily produce text that looks "optimized" by these measures, because editing removes idiosyncratic first choices.

**Key point.** A token distribution is a property of a model–text pair, not an intrinsic property of the text.

## 5. N-gram analysis

**Definition.** N-gram analysis counts sequences of *n* tokens (or characters) and compares their frequencies with reference corpora.

**Uses.**
- **Repetition detection:** repeated trigrams can indicate templated text.
- **Stylometry:** function-word frequencies and common n-grams can distinguish authors or genres in some settings.
- **Plagiarism and provenance:** matching long n-grams against known sources.

**Strengths.** Transparent, fast, and interpretable. Useful for finding copied passages or mechanical repetition.

**Weaknesses.**
- **Sparsity:** most n-grams in a short text occur rarely, so estimates are noisy.
- **Genre confounding:** legal, scientific, and technical writing share formulaic n-grams by convention.
- **No semantic awareness:** fluent paraphrase defeats n-gram matching while preserving meaning.
- **Authorship vs. template:** a shared n-gram indicates shared phrasing, not shared authorship.

**Appropriate use.** As a screening tool for duplication and repetition, not as an authorship verdict.

## 6. Lexical diversity

**Definition.** Measures of how many distinct words a text uses relative to its length, such as type–token ratio, MTLD, and MATTR.

**Detection use.** Some systems treat unusually low or unusually high diversity as a signal. In practice, both directions occur in machine text, and both occur in human text.

**Why the signal is weak.**
- Diversity depends strongly on length, genre, and topic.
- Technical writing repeats terminology by necessity.
- Creative writing may deliberately repeat or deliberately vary.
- A single number cannot distinguish "repetitive because technical" from "repetitive because generated."

**Appropriate use.** As a diagnostic for editing (see [vocabulary-analysis.md](vocabulary-analysis.md)), not as evidence of authorship.

## 7. Linguistic feature extraction

**Definition.** The manual or semi-automated measurement of stylistic features: sentence length distribution, clause depth, punctuation rates, pronoun use, passive voice rate, vocabulary richness, discourse markers, and part-of-speech patterns.

**Strengths.** Interpretable, comparable across models, and grounded in established stylistics. Useful for describing a text's style.

**Weaknesses.**
- **Overlap:** human and machine distributions overlap heavily on every individual feature.
- **Genre effects:** a formal report and a chatbot answer can share many features.
- **Feature engineering bias:** the chosen features reflect the researcher's assumptions about what "machine text" looks like.
- **Aggregation:** individually weak features can be combined into a classifier, but the combination is only as good as its training data.

**Important distinction.** A feature can be *descriptively* useful ("this text has low sentence-length variance") without being *diagnostically* valid ("therefore a machine wrote it").

## 8. Transformer-based classifiers

**Definition.** A pretrained transformer is fine-tuned on labeled human and machine text to output a probability that a text belongs to the machine class.

**How they work.** The model learns distributed representations of tokens and context, then adjusts its weights to separate the two classes in the training set. At inference, it outputs a score, often calibrated afterward.

**Strengths.**
- Capture context beyond n-grams.
- Can learn subtle distributional differences within their training distribution.
- Often achieve high accuracy on held-out data from the same distribution.

**Weaknesses.**
- **Distribution shift:** performance drops when the test text differs from training data (different generator, domain, length, or editing process).
- **Short-text instability:** fewer tokens mean less evidence; scores become noisy.
- **Adversarial sensitivity:** paraphrasing, translation, or light editing can move scores substantially without changing authorship.
- **Opaque features:** the model does not report which properties drove its decision, so errors are hard to diagnose.
- **Label noise:** "human" and "machine" labels are often assigned by assumption rather than verified provenance.

**Interpretation.** A classifier output is a probability under a model and a dataset. It is not a fact about the text's origin.

## 9. Embedding-based classification

**Definition.** Texts are mapped to dense vectors (embeddings) using a pretrained encoder; a classifier is trained on those vectors.

**Strengths.** Efficient, works with limited labeled data, and can capture semantic and stylistic similarity.

**Weaknesses.**
- Embeddings compress style and content together; a classifier may learn topic rather than provenance.
- Domain shift degrades performance.
- Similarity to a "machine-like" cluster is not proof of machine authorship; human text in the same genre can sit in the same region.
- Interpretability is limited.

**Diagnostic caution.** If a detector's errors correlate with topic (e.g., it flags all political science essays), it has learned the corpus, not the phenomenon.

## 10. Statistical classification

**Definition.** Classical classifiers (logistic regression, naive Bayes, support vector machines, random forests) trained on engineered features or n-grams.

**Strengths.** Fast, interpretable, and easy to audit. Coefficients or feature importances show what the model used.

**Weaknesses.**
- Sensitive to feature choice and preprocessing.
- Assumes the training and test distributions match.
- Linear models may capture superficial cues (specific words, punctuation) that do not generalize.
- Reported accuracy can be inflated by near-duplicate texts across train and test splits.

**Use.** Statistical classifiers are most defensible when their features are reported, their splits are documented, and their performance is measured out of domain.

## 11. Dataset bias

**Definition.** Systematic differences between the training data and the population where the detector is applied.

**Common sources.**
- **Generator bias:** training text comes from one or a few models; newer or different models are out of distribution.
- **Domain bias:** training text comes from essays, news, or web text; medical, legal, and code text are underrepresented.
- **Length bias:** short texts are overrepresented or underrepresented relative to real use.
- **Language bias:** English dominates; other languages are poorly covered.
- **Label bias:** "human" samples may be edited, curated, or written by professionals, while "machine" samples may be raw and unedited.
- **Demographic and educational bias:** human corpora may overrepresent particular writers, making the detector flag writers who differ from that norm.

**Consequence.** A detector can be accurate on its benchmark and unreliable in a classroom, a newsroom, or a code review.

## 12. Training-data limitations

**Key limitations.**
1. **Provenance is often assumed.** Labels may reflect who submitted a text, not who wrote it.
2. **Contamination.** Public benchmarks can appear in pretraining data, inflating performance.
3. **Temporal drift.** Models and writing tools change; a detector trained last year may not recognize this year's output.
4. **Class imbalance.** Machine text may be easier to collect in large quantities, skewing the classifier.
5. **Editing.** Human-edited machine text and machine-edited human text blur the categories, yet labels usually remain binary.
6. **Consent and privacy.** Training corpora may include text without clear consent, which raises ethical and legal issues.

**Implication.** Reported accuracy describes performance on a particular labeled dataset, not on authorship in general.

## 13. False positives

**Definition.** A false positive occurs when a text is classified as machine-generated but was written (or substantially written) by a human.

**Why they happen.**
- The writer's style resembles the training corpus's machine class (formal, uniform, formulaic).
- The writer is a non-native speaker whose syntax differs from the human training distribution.
- The text is heavily edited, templated, or translated.
- The text is short, giving the model little evidence.
- The genre is formulaic (legal boilerplate, lab reports, sports summaries).

**Consequences.** False positives can lead to accusations, grade penalties, rejected submissions, or damaged reputations. Because the cost is asymmetric and the evidence is weak, a positive result should never be treated as proof.

**Mitigation in practice.** Require multiple independent forms of evidence, allow the writer to explain their process, and treat the score as one signal among many.

## 14. False negatives

**Definition.** A false negative occurs when machine-generated text is classified as human.

**Why they happen.**
- The text was paraphrased, translated, or edited by a human.
- The generator differs from the training distribution.
- The text is short or unusual in genre.
- The detector's threshold favors human classification to reduce false positives.

**Consequence.** False negatives mean a "human" score is also not proof. Detection systems trade errors against each other; lowering one rate typically raises the other.

## 15. Model calibration

**Definition.** Calibration describes whether predicted probabilities match observed frequencies. A well-calibrated model that outputs 0.8 should be correct about 80% of the time among cases where it outputs 0.8.

**Why it matters.** A raw classifier score is often not a probability. Neural networks can be overconfident, especially out of distribution. Without calibration, a "90%" score may correspond to much lower empirical accuracy.

**How calibration is assessed.**
- **Reliability diagrams:** bin predictions and compare mean predicted probability with observed frequency.
- **Expected Calibration Error (ECE):** a weighted average of the gap across bins.
- **Brier score:** mean squared error of probabilistic predictions.

**Post-hoc methods.** Temperature scaling, isotonic regression, and Platt scaling can improve calibration on a held-out set. They do not fix distribution shift; a model can be well calibrated in-domain and badly calibrated elsewhere.

**Practical implication.** Detector interfaces often present a percentage without calibration information. That percentage should not be read as "the probability a human wrote this."

## 16. Cross-domain generalization

**Definition.** The ability of a detector trained in one domain to perform in another.

**Evidence from evaluation practice.** Performance typically degrades under domain shift: different genres, different generators, different lengths, different editing levels, and different languages. A detector that performs well on student essays may perform poorly on technical documentation or poetry.

**Why generalization fails.**
- The model learns domain-specific cues rather than provenance cues.
- Token distributions differ by genre.
- Human baselines differ by genre (a legal contract is more formulaic than a diary).
- Label definitions differ across datasets.

**Best practice.** Evaluate on out-of-domain data, report the domains tested, and avoid claiming universal accuracy.

## 17. Multilingual limitations

**Definition.** The performance of detection systems across languages and multilingual text.

**Known issues.**
- Most detectors are trained predominantly on English.
- Tokenization and morphology differ; a model's token-level statistics do not transfer.
- Translation changes surface statistics substantially, which can move scores even when authorship does not change.
- Code-switching and mixed-language text are poorly represented in training data.
- Cultural and educational writing conventions vary, producing different "human" baselines.

**Consequence.** A detector's output in a non-English language, or on translated text, carries substantially more uncertainty than its benchmark suggests.

## 18. Detection uncertainty

**Definition.** The range of plausible conclusions consistent with a detector's output.

**Sources of uncertainty.**
- Sampling variance (short texts, unstable estimates).
- Model uncertainty (which reference model, which version).
- Distribution shift (domain, generator, language).
- Label uncertainty (who wrote the training text, and how was it verified?).
- Threshold choice (where the human/machine boundary is drawn).
- Calibration error.

**Reporting uncertainty.** A responsible report gives a score, the model and version, the threshold, the text length, the language, the domain, and the known error rates. Without these, a number is not interpretable.

## 19. Evaluation metrics

### Precision
\[
\mathrm{Precision} = \frac{TP}{TP + FP}
\]
Of the texts flagged as machine-generated, what fraction actually were (according to the labels)? Precision matters when a positive flag has serious consequences.

### Recall (sensitivity)
\[
\mathrm{Recall} = \frac{TP}{TP + FN}
\]
Of the texts that were machine-generated, what fraction did the detector catch? Recall matters when missing a case is costly.

### F1 score
\[
F_1 = 2 \cdot \frac{\mathrm{Precision} \cdot \mathrm{Recall}}{\mathrm{Precision} + \mathrm{Recall}}
\]
The harmonic mean of precision and recall. It summarizes both but hides the trade-off; two systems with the same F1 can have very different error profiles.

### Accuracy
\[
\mathrm{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
\]
The fraction of all cases classified correctly. Accuracy is misleading when classes are imbalanced: a detector that labels everything "human" can have high accuracy if most texts are human.

### False-positive rate
\[
\mathrm{FPR} = \frac{FP}{FP + TN}
\]
The fraction of human texts incorrectly flagged. This is the number that matters most to a writer accused by a detector.

### False-negative rate
\[
\mathrm{FNR} = \frac{FN}{FN + TP}
\]
The fraction of machine texts missed. This is the number that matters most to someone relying on detection to catch misuse.

### Base rates and the base-rate fallacy
Even a test with high sensitivity and specificity can have low positive predictive value when the condition is rare. If 2% of submissions are machine-generated and a detector has 95% sensitivity and 90% specificity, then among flagged texts:

\[
PPV = \frac{0.95 \times 0.02}{0.95 \times 0.02 + 0.10 \times 0.98} \approx 0.162
\]

About 16% of flagged texts would actually be machine-generated. The rest would be false positives. This arithmetic is the single strongest reason not to treat a flag as proof.

### Why one metric is not enough
A detector should be reported with precision, recall, FPR, FNR, calibration, the test distribution, and the threshold. A single accuracy figure is not sufficient for any consequential decision.

---

## Why detector output cannot establish authorship

1. **The target is not observable.** Authorship is a causal history, not a surface property. Detectors measure correlates of a corpus, not the act of writing.
2. **The base rate is unknown.** Without knowing how much of the population is machine-generated, a score cannot be converted into a posterior probability of authorship.
3. **The distributions overlap.** Human and machine writing overlap on every measured feature. Errors are structural, not incidental.
4. **The model is conditional.** Scores depend on the reference model, version, domain, length, and language.
5. **Editing breaks the link.** Paraphrasing, translation, and human editing can move scores without changing who wrote the ideas.
6. **Calibration is usually unreported.** A displayed percentage is often not a calibrated probability.
7. **The costs are asymmetric.** A false positive can harm a person's grade, job, or reputation; the score is not designed to bear that weight.
8. **The claim is unfalsifiable in practice.** There is no ground truth available in most disputes, so the detector's output cannot be validated case by case.

**Responsible use.** Detectors can support screening for duplication, flag texts for human review, or help researchers study corpus differences. They should not be used as sole evidence in disciplinary, academic, legal, or employment decisions.

---

## How Human Signal uses this material

- **No optimization for detector scores.** Human Signal does not paraphrase to lower detection, and it does not treat a low score as a quality goal.
- **Quality is judged by readers and by the text's purpose.** Accuracy, clarity, coherence, and appropriateness are the criteria.
- **Suspicious patterns are editing prompts.** A formulaic introduction is worth revising because it wastes the reader's time, not because a detector might notice it.
- **Uncertainty is stated.** When a claim about detection is made, the conditions and limitations are reported with it.

See [../tests/quality-checklist.md](../tests/quality-checklist.md) for the review criteria Human Signal actually applies.

---

## Key terms

| Term | Meaning |
|---|---|
| Perplexity | Exponential of average negative log-likelihood under a model |
| Burstiness | Variability of predictability across a text |
| Token distribution | Probability distribution over next tokens at a position |
| N-gram | Contiguous sequence of *n* tokens or characters |
| Type–token ratio | Distinct words divided by total words |
| Calibration | Agreement between predicted probabilities and observed frequencies |
| Precision | Share of positive flags that are correct |
| Recall | Share of true positives that are flagged |
| F1 | Harmonic mean of precision and recall |
| Base rate | Prevalence of the condition in the population |
| Distribution shift | Difference between training and deployment data |

Back to [SKILL.md](../SKILL.md).
