# ISA Standard Summary

**Task:** Produce a structured summary of a specific International Standard 
on Auditing (ISA), at the level needed by an ICAEW Professional Level 
candidate, with paragraph-level references that can be verified against 
the IAASB Handbook.

**Standard used as example:** ISA 520 — Analytical Procedures (Clarified, 
effective for audits of financial statements for periods beginning on or 
after December 15, 2009; verified against the 2023–2024 IAASB Handbook 
edition).

**Model used:** Claude (claude.ai), web interface.

---

## Prompt v1 (rough)
Summarise ISA 520 for me. I'm an audit student and I need to understand
what it covers.

## What v1 got wrong

A short, vague prompt produced a textbook-style overview with several 
substantive errors. The output is reproduced below at the bottom of this 
file for reference. The key issues:

1. **Scope error (most serious).** Stated that ISA 520 governs analytical 
   procedures at three stages: risk assessment, substantive, and overall 
   review. The standard explicitly limits itself to two, substantive 
   procedures and end-of-audit procedures (paragraph 1). Risk assessment 
   analytical procedures are governed by ISA 315 (Revised 2019), 
   paragraph 14(b).

2. **Misattributed requirement.** Stated that analytical procedures at 
   planning are "required" under ISA 520. No such requirement exists in 
   ISA 520. The requirement is in ISA 315 (Revised 2019).

3. **No paragraph numbers cited anywhere.** The reader cannot verify 
   any claim against the standard. Specific paragraph references 
   (1–7 and A1–A21) are entirely absent.

4. **No distinction between requirements and application material.** 
   The standard structures itself into requirements (paragraphs 1–7, 
   binding "shall" language) and application material (A1–A21, 
   explanatory). v1 conflates the two.

5. **Misstated paragraph 5(a).** The first sub-requirement of paragraph 5 
   is *suitability for the assertion*, which involves the assessed risks 
   of material misstatement and tests of details. v1 rendered this as 
   "plausibility of the relationship," which is closer to what A6 says 
   (application material) rather than paragraph 5(a).

6. **Added a step to paragraph 7.** Listed "corroborate with other audit 
   evidence" as a separate procedural step in investigating differences. 
   Paragraph 7 has two sub-requirements: (a) inquire and obtain evidence 
   about management's responses, (b) perform other procedures as 
   necessary. The corroboration framing comes from A20 (application 
   material), not the requirement itself.

7. **Internally inconsistent.** Listed two different "four factors" for 
   substantive analytical procedures in two different sections of the 
   same response — one closer to paragraph 5, one not.

---

## Prompt v2 (refined)
You are an ICAEW-qualified audit senior reviewing the work of an ICAEW
Professional Level student preparing for the Audit and Assurance exam.
The student needs to understand ISA 520 (Analytical Procedures) at the
level required to apply it on an audit engagement.
Produce a structured summary of ISA 520 with the following sections:
Scope and applicability — when and how ISA 520 is engaged in an audit,
including its interaction with ISA 315 (Revised 2019) and ISA 330.
Required uses of analytical procedures — the specific stages of an
audit where analytical procedures are mandatory (cite ISA 520
paragraph numbers).
Substantive analytical procedures — the four-step framework
(developing expectations, defining significant differences, performing
procedures, investigating differences) with the relevant paragraph
reference for each.
Common practical pitfalls — situations where analytical procedures
typically fail or are misapplied.
Interaction with materiality and risk assessment — how the threshold
for investigation links to performance materiality.

Constraints:
Cite specific ISA 520 paragraph numbers for every requirement you
describe. If you are not certain of a paragraph number, write
"[paragraph reference to verify]" rather than guessing.
Distinguish clearly between requirements (in the standard's "shall"
paragraphs) and application material (the "A" paragraphs).
Do not conflate ISA 520 with ISA 315 (Revised 2019), which covers
analytical procedures used as risk assessment procedures.
Length: roughly 600 words total.

After producing the summary, list any specific points where you are
uncertain of the exact wording or paragraph number, so I can verify
against the IAASB Handbook.

## Example output (v2)

> **ISA 520 – Analytical Procedures: Structured Summary**
>
> **1. Scope and Applicability**
> ISA 520 governs analytical procedures used as substantive procedures 
> and as an overall review at the completion stage. It does not cover 
> analytical procedures performed during risk assessment — those fall 
> under ISA 315 (Revised 2019), which addresses the auditor's procedures 
> for identifying and assessing risks of material misstatement. ISA 330 
> then governs the auditor's response to those assessed risks, including 
> the decision to use substantive analytical procedures as part of that 
> response. ISA 520 is therefore engaged after the risk assessment 
> phase — it governs how analytical procedures are executed once the 
> auditor has decided (per ISA 330) to rely on them substantively.
>
> **2. Required Uses — Mandatory Stages**
> ISA 520 imposes two mandatory uses:
> - **Para. 5:** The auditor shall design and perform analytical 
>   procedures near the end of the audit as an overall review.
>   *[see verification log: paragraph misattributed — actual reference is paragraph 6]*
> - **Para. 4 [paragraph reference to verify]:** Analytical procedures 
>   shall be used as substantive procedures where their use is more 
>   effective or efficient than tests of detail, in accordance with 
>   ISA 330.
>   *[see verification log: paragraph 4 is the Definition, not a requirement; the substantive-procedures requirement is paragraph 5]*
>
> **3. Substantive Analytical Procedures — Four-Step Framework**
> 1. Develop an expectation — Para. 5(a) / A5–A8 *[references to verify]*
> 2. Define a threshold for significant difference — Para. 5(b)
> 3. Execute the comparison — Para. 5
> 4. Investigate unexplained differences — Para. 7
>
> *[see verification log: this entire four-step framework does not match paragraph 5 of the standard; see below]*
>
> **4. Common Practical Pitfalls**
> - Circular expectations (deriving the expectation from the audited 
>   figures themselves)
> - Threshold set above performance materiality
> - Accepting management explanations without corroboration (cited 
>   as breach of para. 7) *[see verification log: paragraph 7 wording is narrower than this]*
> - Conflating ISA 315 risk-assessment APs with ISA 520 substantive APs
> - Omitting the overall review (cited as para. 5) *[see verification log: should be paragraph 6]*
>
> **5. Interaction with Materiality and Risk Assessment**
> The investigation threshold set in Step 2 must be consistent with 
> performance materiality (established under ISA 320). A threshold set 
> above performance materiality creates a gap: differences that are 
> individually material may go uninvestigated. The higher the assessed 
> risk of material misstatement for an assertion (per ISA 315/330), the 
> more precise the expectation must be and the lower the investigation 
> threshold should be.
>
> **Uncertainties to Verify Against the IAASB Handbook**
> - Para. 4 exact wording
> - A-paragraph numbers for the expectation-precision guidance (cited 
>   A4–A8 above; confirm in the current IAASB Handbook)
> - Para. 5(a)/(b) sub-paragraph lettering
> - Overall review vs. substantive AP paragraphs — confirm whether 
>   para. 5 carries both requirements

---

## Verification log

**Verified against:** IAASB Handbook 2023–2024 edition, ISA 520 
(Clarified, effective December 15, 2009).

### Improvements from v1 to v2

The refined prompt produced measurable improvements:

- **Scope corrected.** v2 correctly limits ISA 520 to substantive 
  procedures and overall review (paragraph 1), and correctly identifies 
  ISA 315 (Revised 2019) as the source of risk-assessment AP requirements.
- **Cross-references accurate.** ISA 330 is correctly identified as 
  governing the auditor's response to assessed risks; ISA 320 is correctly 
  identified as the source of performance materiality.
- **Paragraph references attempted.** v1 cited no paragraphs at all; v2 
  attempts paragraph-level references throughout (although several are 
  wrong — see below).
- **Self-flagged uncertainties.** The prompt instruction asking the model 
  to flag uncertainty produced a useful "Uncertainties to Verify" section 
  at the end. Each item flagged turned out to be a genuine error.

### Errors v2 still made

These were stated confidently and require correction against the IAASB Handbook.

**Paragraph 5 and paragraph 6 swapped.** v2 states paragraph 5 carries 
the overall review requirement. In the standard, **paragraph 5** is the 
requirement for substantive analytical procedures (with four 
sub-requirements (a)–(d)). **Paragraph 6** is the requirement for the 
overall review near the end of the audit.

**Paragraph 4 misattributed.** v2 cites paragraph 4 as the source of the 
substantive-procedures requirement. Paragraph 4 is the **Definition** of 
analytical procedures, not a requirement. The substantive-procedures 
requirement is paragraph 5.

**The four-step framework is invented.** This is the most important 
error and the most dangerous because it sounds correct.

v2 lists the four steps as: develop expectation, define threshold, 
execute comparison, investigate differences. This is closer to how the 
procedure flows in practice, or how some textbooks teach it, but it is 
not what paragraph 5 of ISA 520 actually says.

The actual four sub-requirements of paragraph 5 are:
- **(a) Suitability** — determine the suitability of particular 
  substantive analytical procedures for given assertions, taking 
  account of the assessed risks of material misstatement and tests of 
  details, if any.
- **(b) Reliability of data** — evaluate the reliability of data from 
  which the auditor's expectation of recorded amounts or ratios is 
  developed, taking account of source, comparability, nature and 
  relevance, and controls.
- **(c) Develop an expectation** — develop an expectation of recorded 
  amounts or ratios and evaluate whether the expectation is sufficiently 
  precise to identify a misstatement that may cause the financial 
  statements to be materially misstated.
- **(d) Acceptable difference** — determine the amount of any difference 
  of recorded amounts from expected values that is acceptable without 
  further investigation.

The error matters because v2's version omits **suitability** and 
**reliability of data** — the two pre-execution considerations that are 
arguably the most professionally distinctive parts of paragraph 5. 
A working paper drafted from v2's framework would lack these.

**Paragraph 7 wording stretched.** v2 cites "accepting management 
explanations without corroboration" as a breach of paragraph 7. 
Paragraph 7 requires the auditor to (a) inquire of management and 
obtain audit evidence relevant to management's responses, and 
(b) perform other audit procedures as necessary. The word "corroboration" 
comes from A20 (application material), not the binding requirement. 
The framing is defensible audit practice but not literally what 
paragraph 7 says.

**Section 4 paragraph misreference.** "Omitting the overall review 
(para. 5)" should read paragraph 6.

**Inferences stated as fact.** "A threshold set above performance 
materiality creates a gap" is reasonable audit-practice inference but 
is not stated this way in the standard or in A16. Worth distinguishing 
inference from quotation in a working paper.

### What this teaches about AI verification on technical standards

Three categories of failure appeared in v2, and each requires a 
different verification habit:

**1. Self-flagged uncertainty.** Claude flagged uncertainty about 
paragraph 4 wording, A-paragraph numbers, and sub-paragraph lettering — 
and each of these flagged items was genuinely wrong. The lesson: when 
the model says it is uncertain, take that seriously and verify those 
points first.

**2. Confidently-stated paragraph errors.** The paragraph 5 / 
paragraph 6 swap was stated without any uncertainty flag. These errors 
are only catchable by direct comparison to the standard. The lesson: 
verify all paragraph references, not just the ones the model flags.

**3. Confidently-stated conceptual errors.** The invented four-step 
framework is the most dangerous category. It sounds professional, 
matches what a junior auditor might be taught in firm methodology, and 
would survive casual peer review. Only someone who knows what 
paragraph 5 actually says can catch it. The lesson: for technical 
standards, the most important verification is conceptual — does the 
model's content match what the standard actually requires, not what it 
*sounds like* the standard might require.

### Recurring pattern to watch for

Across v1 and v2, the consistent failure mode is **conflating the 
pre-Clarity ISA 520 (2004 version) with the current Clarified ISA 520 
(2009)**. The pre-Clarity version contained risk-assessment provisions 
(paragraphs 8–9), included a planning-stage requirement, and had a 
different sub-paragraph structure (12a–12g). v1's three-stage framing 
came from this older content. v2 corrected the scope but still drifted 
toward older-style paragraph references in some places.

For any future prompt summarising an ISA or IFRS that has been revised, 
the verification step should specifically test whether the model is 
working from the current effective version or a superseded one. A 
useful diagnostic question: ask the model what the effective date of 
the version it is summarising is. If the date is wrong, the rest of 
the summary is suspect.

---

## v1 output (for reference)

> ISA 520 – Analytical Procedures
>
> ISA 520 governs when and how auditors use analytical procedures — 
> techniques that evaluate financial information by studying relationships 
> between data (financial and non-financial).
>
> […full v1 output omitted for length; key issues catalogued above…]

---

*Verification performed against IAASB Handbook 2023–2024 edition, 
ISA 520. Errors identified here are characteristic of AI failure modes 
when summarising auditing standards; the specific errors will differ 
across model versions and dates, but the verification discipline does not.*

*Last updated: 25/6/2026.*
