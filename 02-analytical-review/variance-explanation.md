# Variance Explanation

**Task:** Produce audit working paper commentary explaining a 
material variance in a specific P&L line item under ISA 520 
analytical procedures. The commentary must identify what management's 
explanation does and does not tell the auditor, engage with relevant 
MFRS standards and ISA requirements, and specify both occurrence and 
completeness audit procedures.

**Scenario used:** A constructed scenario based on a realistic 
audit situation — a listed Malaysian electronics manufacturer 
(Bursa Main Market, MFRS reporter, exports ~70% of revenue) with 
Other Operating Expenses increasing 45.4% year-on-year. The scenario 
includes a deliberately weak management explanation, the kind a 
junior auditor would receive in real fieldwork and need to assess.

**Model used:** Claude (claude.ai), web interface.

**Verification approach:** This file's verification has two parts: 
(a) checking that v2's audit procedures and MFRS / ISA framings match 
standard audit practice for variance investigation, and (b) verifying 
specific paragraph references against the MASB-issued MFRS PDFs and 
the IAASB Handbook 2023–2024 edition. Sources used: MFRS 102, 
MFRS 116, MFRS 119, MFRS 124, MFRS 137, MFRS 138, MFRS 101 
(MASB-issued PDFs); ISA 500, ISA 520, ISA 550 (IAASB Handbook).

---

## Prompt v1 (rough)
A Malaysian listed manufacturing client's Other Operating Expenses
went up from RM 18.4m to RM 26.8m year-on-year (+45.4%). Management
says the increase is due to higher utility costs, professional fees,
and one-off restructuring expenses.
Help me write something for the audit working papers explaining this
variance.

## What v1 got wrong

v1 produced output that read as plausible audit working paper text 
on the surface but contained several substantive failures on closer 
inspection. The full v1 output is reproduced at the end of this file. 
The key issues:

1. **Fabricated breakdown of management's explanation.** Management 
   provided three vague one-line explanations (higher utility costs, 
   professional fees, one-off restructuring expenses). v1 expanded 
   each into specific sub-categories — *"electricity and fuel 
   consumption in line with expanded production activity and/or 
   tariff rate increases"*, *"fees incurred for legal, tax advisory, 
   and/or consulting services"*. These details were not in 
   management's actual explanation. A working paper must record 
   management's explanation as provided, then identify what's 
   missing, not invent the missing detail.

2. **Asserted materiality exceedance without materiality data.** v1 
   stated the variance *"exceeds the planning materiality threshold"* 
   when no materiality figure was provided in the prompt. A working 
   paper cannot assert materiality exceedance without an actual 
   materiality benchmark.

3. **Missed the capitalisation risk on professional fees.** 
   Professional fees can include costs that should be capitalised 
   under MFRS 116 (PPE) or MFRS 138 (Intangibles) — for example, 
   legal fees on asset acquisitions, consulting fees on 
   internally-generated intangibles. Misclassification means expense 
   overstatement and asset understatement. v1 tested only the 
   existence of the expense, not its proper classification.

4. **Missed the related-party risk under ISA 550.** Professional 
   fees are a common location for related-party transactions 
   (director's consulting firm, controlling shareholder's legal 
   practice). ISA 550 requires specific audit attention to related 
   parties. v1 did not engage this risk.

5. **Tested occurrence but not completeness.** The procedures listed 
   in v1 (review invoices, agree contracts) tested that recorded 
   expenses are real. They did not test whether expenses have been 
   completely recorded. Completeness testing for expenses requires 
   search for unrecorded liabilities (subsequent invoice review, 
   accruals testing) — a standard audit procedure that v1 omitted.

6. **Cited ISA 520 in the opening but did not reference the operative 
   paragraph.** ISA 520 paragraph 7 is the specific requirement to 
   investigate fluctuations differing from expected values, requiring 
   (a) inquiry of management and (b) other procedures. v1 said 
   *"written to ISA 520 standard"* but did not cite the operative 
   paragraph.

7. **No reference to ISA 500 (Audit Evidence).** Every corroboration 
   step in v1 (*"agreed to invoices,"* *"reviewed contracts"*) 
   engages ISA 500. The standard governs sufficiency and 
   appropriateness of audit evidence. v1 did not reference it.

8. **Template-form rather than substantive output.** v1 produced a 
   working paper template with bracketed fields throughout 
   (*"[Manufacturing Co.]"*, *"[ ]"* sampling thresholds, 
   *"[ explainable / requiring further follow-up ]"*). This signals 
   structure without substance — a real working paper would either 
   contain actual figures and conclusions, or explicitly state work 
   remaining.

---

## Prompt v2 (refined)
You are an ICAEW-qualified audit senior at a Big Four firm in Malaysia,
performing analytical review under ISA 520 on a listed manufacturing
client (Bursa Main Market, exports ~70% of revenue, reports under MFRS).
Below are the facts of the variance:

Account: Other Operating Expenses
FY24: RM 18,420,000
FY25: RM 26,780,000
Variance: +RM 8,360,000 (+45.4%)
Engagement planning materiality: RM 3,200,000
Performance materiality: RM 2,400,000

Management's explanation (as recorded by the engagement team):
"Increase due to higher utility costs, professional fees, and one-off
restructuring expenses incurred during the year."
Produce a working paper memo on this variance, structured as follows:
Variance identification — quantify the variance, assess against
planning and performance materiality, cite ISA 520 paragraph 7.
Assessment of management's explanation as provided — record
management's explanation verbatim. Identify what management's
explanation does NOT tell you (breakdown by sub-component,
quantification by line, nature and timing of restructuring, specific
service providers, etc.). Do not invent or expand the explanation
beyond what management actually said.
MFRS-specific risks raised by each component, addressing
specifically:
Utility costs: nature of cost (cost of production vs administrative)
Professional fees: capitalisation risk under MFRS 116 / MFRS 138;
related-party risk under ISA 550
Restructuring: recognition criteria under MFRS 137; employee
termination benefits under MFRS 119; separate disclosure under
MFRS 101 paragraphs 97–98
Audit procedures required — testing both occurrence (recorded
expenses are real and properly authorised) and completeness
(no unrecorded expenses), cross-referenced to ISA 500.
Conclusion framing — state what conclusion can be drawn from
the procedures described, and what remains outstanding. Do not
draw a final conclusion in the absence of evidence; bracket the
conclusion as [pending evidence review].

Constraints:
Do not invent specific RM figures for sub-components not provided
by management.
Do not paraphrase management's explanation in a way that adds
detail not actually given.
Cite MFRS / ISA paragraph numbers where you can; flag references
as "[to verify]" if uncertain.
Length: roughly 600 words.

## Example output (v2)

> **Audit Working Paper Memo**
> **Client:** [Client Name] | **Period:** FY2025 | **Prepared by:** [Senior] | **Date:** 25 June 2026
> **Area:** Other Operating Expenses — Analytical Review (ISA 520)
>
> **1. Variance Identification**
>
> Other Operating Expenses increased from RM 18,420,000 (FY24) to 
> RM 26,780,000 (FY25), representing an absolute increase of 
> **RM 8,360,000 (+45.4%)**.
>
> This variance exceeds both **planning materiality (RM 3,200,000)** 
> and **performance materiality (RM 2,400,000)**. Under **ISA 520 
> paragraph 7**, where analytical procedures identify fluctuations 
> that differ from expected values by a significant amount, the 
> auditor is required to investigate by making enquiries of management 
> and performing other audit procedures as necessary. This variance 
> triggers that obligation unambiguously on both materiality 
> thresholds.
>
> **2. Assessment of Management's Explanation**
>
> Management's explanation, as recorded by the engagement team, is 
> reproduced verbatim:
>
> > *"Increase due to higher utility costs, professional fees, and 
> > one-off restructuring expenses incurred during the year."*
>
> This explanation identifies three broad sub-components but is 
> **insufficient for audit purposes** in the following respects:
>
> - No quantification by sub-component.
> - No characterisation of "higher" utility costs (volume vs tariff).
> - Professional fees are unspecified (nature of services, identity 
>   of service providers, related-party status).
> - Restructuring described as "one-off" without detail (nature, 
>   timing, formal plan, cost categories).
>
> The explanation as given cannot be corroborated or rebutted without 
> further evidence.
>
> **3. MFRS-Specific Risks by Component**
>
> *Utility Costs.* For a manufacturing entity, utilities attributable 
> to production should be allocated to cost of goods manufactured 
> under **MFRS 102 paragraphs 10–12**, not expensed as other operating 
> costs. Misrouting to Other Operating Expenses would understate cost 
> of sales and distort gross margin.
>
> *Professional Fees.* Two risks. First, capitalisation risk: fees 
> incurred in acquiring or constructing PPE or developing intangibles 
> may require capitalisation under **MFRS 116** or **MFRS 138** 
> respectively, rather than immediate expensing. Second, related-party 
> risk: under **ISA 550**, the auditor must remain alert to 
> transactions with related parties; professional fee arrangements 
> with connected parties could represent undisclosed related-party 
> transactions requiring disclosure under **MFRS 124**.
>
> *Restructuring.* Recognition of a restructuring provision is 
> governed by **MFRS 137 paragraphs 71–83**, which require a 
> constructive obligation — specifically, a formal detailed plan 
> announced to those affected before the reporting date. Any employee 
> termination benefits must be assessed under **MFRS 119 paragraphs 
> 159–171** to determine whether they are short-term or other 
> long-term in nature. If material, restructuring items may require 
> separate line disclosure under **MFRS 101 paragraphs 97–98**.
>
> **4. Audit Procedures Required**
>
> *Occurrence (ISA 500):*
> - Obtain sub-ledger listing of Other Operating Expenses; agree to 
>   trial balance.
> - Sample-based vouching to invoices, contracts, payment records.
> - For professional fees: inspect engagement letters; cross-check 
>   provider names against related-party register.
> - For restructuring: obtain formal plan, board minutes, employee 
>   communications; assess against MFRS 137 recognition criteria.
> - Review prior-year accruals for no double-counting.
>
> *Completeness (ISA 500):*
> - Cut-off review: inspect invoices received post-year-end, assess 
>   accruals adequacy.
> - Compare utility invoices received July–August 2025 against 
>   year-end accruals.
> - Enquire whether restructuring-related costs fully captured, 
>   including contingent obligations not yet invoiced.
>
> **5. Conclusion Framing**
>
> Based on analytical procedures performed, Other Operating Expenses 
> shows a variance that is material in both absolute and percentage 
> terms, with management's explanation identifying three broad 
> drivers that individually carry distinct financial reporting risks 
> under MFRS and ISA 550.
>
> **[Pending evidence review].** No conclusion can be reached on 
> completeness, occurrence, or classification until the sub-ledger 
> listing has been obtained, sampled items vouched, the restructuring 
> plan (if any) reviewed against MFRS 137 criteria, professional fee 
> arrangements assessed for capitalisation and related-party 
> implications, and utility cost allocations confirmed. The adequacy 
> of management's explanation remains **unsubstantiated at this stage.**

---

## Verification log

**Verified against:** MASB-issued PDFs of MFRS 102, MFRS 116, MFRS 119, 
MFRS 124, MFRS 137, MFRS 138, MFRS 101 (downloaded from masb.org.my); 
IAASB Handbook 2023–2024 edition for ISA 500, ISA 520, ISA 550; 
ICAEW Audit and Assurance study materials for procedure norms.

### Improvements from v1 to v2

The refined prompt produced substantial improvements across every 
dimension v1 failed:

- **Fabrication of management's explanation eliminated.** v2 records 
  management's explanation verbatim in a blockquote, then identifies 
  four specific gaps. v1 had expanded each one-line explanation into 
  detailed sub-categories that management never provided.
- **Materiality figures used appropriately.** v2 applies the planning 
  and performance materiality figures provided in the prompt. v1 had 
  asserted materiality exceedance without any materiality data.
- **MFRS 102 utility classification risk added beyond what was asked.** 
  The prompt asked Claude to address utility costs only as "cost of 
  production vs administrative." v2 went further, explicitly engaging 
  MFRS 102 paragraphs 10–12 and flagging the gross margin distortion 
  risk if production utilities are misrouted to operating expenses. 
  This is a value-add observation an experienced audit senior would 
  make.
- **MFRS 116 / MFRS 138 capitalisation risk engaged.** v2 addresses 
  the risk that professional fees may include costs requiring 
  capitalisation under MFRS 116 (PPE) or MFRS 138 (Intangibles). 
  v1 missed this entirely.
- **ISA 550 related-party risk engaged.** v2 explicitly addresses 
  the related-party risk in professional fees and the disclosure 
  obligation under MFRS 124. v1 missed both standards.
- **MFRS 137 / MFRS 119 / MFRS 101 framework for restructuring 
  addressed.** v2 cites three interlinked standards: MFRS 137 for 
  recognition of the provision, MFRS 119 for termination benefits, 
  MFRS 101 for separate disclosure. v1 was silent on all three.
- **Completeness testing added.** v2 includes a separate Completeness 
  section with cut-off procedures, post-year-end invoice review, and 
  inquiry on contingent obligations. v1 tested only occurrence.
- **ISA 500 referenced for audit evidence framework.** v1 listed 
  procedures without grounding them in the audit evidence standard.
- **Conclusion properly bracketed.** v2 frames the conclusion as 
  [pending evidence review] with five outstanding items listed. v1 
  bracketed the conclusion as [ explainable / requiring further 
  follow-up ] without specifying what remains.
- **MFRS 124 distinguished from ISA 550.** v2 correctly distinguishes 
  the *audit standard* (ISA 550, governing the auditor's procedures 
  on related parties) from the *accounting standard* (MFRS 124, 
  governing the entity's disclosure obligation). Many AI outputs 
  conflate these.

### Errors v2 still made

The errors that remain are minor — precision-level rather than 
substantive.

**1. ECL staging framing language.** Not applicable to this file 
(ECL framing is a MFRS 9 issue more relevant to the ratio commentary 
file). v2 does not engage MFRS 9 in this variance scenario.

**2. No reference to ISA 330.** The completeness procedures listed in 
Section 4 engage ISA 330 (Auditor's Responses to Assessed Risks), 
particularly paragraph 22(b) on substantive procedures for assertions. 
Citing only ISA 500 is acceptable but the citation chain could be 
tighter. A more rigorous working paper would reference both standards.

**3. No reference to ISA 520 paragraph 5(d).** The materiality 
assessment in Section 1 engages ISA 520 paragraph 5(d) (the "amount 
of difference that is acceptable without further investigation"). 
v2 correctly applies the concept and cites paragraph 7 for the 
investigation requirement, but does not cite paragraph 5(d) as the 
prior threshold-setting requirement.

**4. MFRS 138 paragraph range not specified.** For internally-generated 
intangibles, the capitalisation criteria in MFRS 138 paragraphs 54–67 
govern when costs can be capitalised vs expensed. v2 cites MFRS 138 
generally but doesn't engage with this specific paragraph range.

**5. MFRS 119 / MFRS 137 interaction not drawn out.** MFRS 119 
paragraph 165 specifies that termination benefits are recognised at 
the *earlier* of (a) when the entity can no longer withdraw the offer, 
and (b) when restructuring costs are recognised under MFRS 137. The 
two standards have a precisely defined interaction that v2's working 
paper does not draw out explicitly. The substance is captured (both 
standards are referenced) but the linkage between them is not 
articulated.

### Verified paragraph references

Each specific paragraph citation in v2 has been verified against the 
source documents.

- **ISA 520 paragraph 7** ✓ — Confirmed against IAASB Handbook 
  2023–2024. Paragraph 7 reads: *"If analytical procedures performed 
  in accordance with this ISA identify fluctuations or relationships 
  that are inconsistent with other relevant information or that 
  differ from expected values by a significant amount, the auditor 
  shall investigate such differences by inquiring of management and 
  obtaining appropriate audit evidence relevant to management's 
  responses and performing other audit procedures as necessary..."*
  
- **MFRS 102 paragraphs 10–12** ✓ — Confirmed against MASB-issued 
  MFRS 102 PDF. Paragraph 10 covers cost of inventories generally; 
  paragraph 11 covers costs of purchase; paragraph 12 covers costs 
  of conversion including production overheads. Production utilities 
  fall under paragraph 12's allocation of fixed and variable 
  production overheads.
  
- **MFRS 137 paragraphs 71–83** ✓ — The paragraph range covers the 
  restructuring section of MFRS 137. The "constructive obligation" 
  and "detailed formal plan" criteria are within this range. 
  Reference is accurate.
  
- **MFRS 119 paragraphs 159–171** ✓ — Confirmed against MASB-issued 
  MFRS 119 PDF. Paragraphs 159–164 cover scope and definition of 
  termination benefits; 165–168 cover recognition; 169–170 cover 
  measurement; 171 covers disclosure. The most operative paragraph 
  for v2's claim about distinguishing short-term from other long-term 
  termination benefits is paragraph 169(b), which states: *"if the 
  termination benefits are not expected to be settled wholly before 
  twelve months after the end of the annual reporting period, the 
  entity shall apply the requirements for other long-term employee 
  benefits."* Claude flagged this reference as "[to verify]" — the 
  discipline worked, and direct verification confirms the reference 
  is accurate.
  
- **MFRS 101 paragraphs 97–98** ✓ — Previously verified in the 
  `mfrs-comparison.md` file. Paragraph 97 requires separate disclosure 
  of material items of income or expense; paragraph 98 gives examples 
  including restructuring.
  
- **MFRS 116, MFRS 138, MFRS 124, ISA 500, ISA 550** ✓ (general 
  references) — All cited correctly at the framework level. v2 does 
  not specify paragraph numbers within these standards but the 
  general attribution is accurate.

### What this teaches about AI verification on structured audit drafting

This file produces the strongest v2 output across the four files in 
this repository. Three reasons matter:

**1. The task has a more structured form than ratio commentary.** A 
working paper memo on a specific variance has a conventional 
structure: identify, quantify, assess, test, conclude. Structured 
tasks suit AI output well because the prompt can specify the 
structure precisely.

**2. The MFRS and ISA citations required are stable and well-documented.** 
Unlike the MFRS-IFRS comparison file, where named MASB documents 
created verification uncertainty, this file engages well-established 
paragraph references that are verifiable against the standards 
themselves.

**3. The prompt design directly mapped to v1's failure modes.** Each 
constraint in the v2 prompt addressed a specific v1 failure: 
"record management's explanation verbatim" addressed fabrication; 
"do not invent specific RM figures" addressed the same; 
"cross-referenced to ISA 500" addressed the citation gap; 
"both occurrence and completeness" addressed the testing gap; 
"[pending evidence review]" addressed the empty conclusion. The 
prompt design was specifically diagnostic.

The overall pattern across this file and the ratio commentary file 
is that **structured audit drafting is the strongest use case for AI 
in audit work, when prompts are diagnostic of failure modes and 
verification is performed against the operative standards.** This is 
a more positive framing than the standards-summary files (where 
verification surfaced more substantial errors), but it is a *honest* 
one — both findings are part of the same overall pattern: AI in audit 
work is useful where the task is structured and the verification 
sources are stable, and risky where the task is open-ended or the 
sources are jurisdiction-specific.

### Recurring pattern to watch for

When using AI for variance explanations or other structured working 
paper drafting:

- **Always provide management's explanation verbatim and instruct 
  the model not to expand it.** Fabrication of management explanations 
  is the most consistent failure mode.
- **Always provide actual materiality figures.** Without them, the 
  model will either invent thresholds or assert exceedance without 
  evidence.
- **Always specify both occurrence and completeness testing 
  explicitly.** Vague prompts produce occurrence-only procedures.
- **Always require paragraph-level citations to the operative MFRS 
  and ISA paragraphs.** Without this, the model will cite frameworks 
  generally without engaging specific requirements.
- **Always specify the framework links between standards.** 
  Restructuring engages MFRS 137 + MFRS 119 + MFRS 101 simultaneously; 
  related-party engages ISA 550 + MFRS 124 simultaneously. Without 
  prompting for the link, the model will reference standards in 
  isolation.

A diagnostic prompt of this kind can produce working paper output 
that an audit senior could edit and use, rather than rewrite from 
scratch. The verification step remains essential — for paragraph 
references especially — but the editing burden is much smaller than 
on a vague prompt.

---

## v1 output (for reference)

> Here's the working paper commentary, written to ISA 520 standard — 
> ready to drop in or adapt to your firm's template.
>
> Analytical Review — Other Operating Expenses Period: FY2025 | 
> Client: [Manufacturing Co.] | Prepared by: [ ] | Date: [ ]
>
> 1. Fluctuation Identified
> Other Operating Expenses increased by RM 8.4m from RM 18.4m (FY2024) 
> to RM 26.8m (FY2025), representing a year-on-year movement of 
> +45.4%. This exceeds the planning materiality threshold and 
> accordingly requires further explanation and corroboration.
>
> [...full v1 output retained in repo for transparency...]

---

*Verification performed against MASB-issued MFRSs and the IAASB 
Handbook 2023–2024 edition. The errors in v1 are characteristic of 
AI failure modes when prompted vaguely for structured audit drafting; 
the corrections in v2 reflect the diagnostic value of well-designed 
prompts. The specific errors will differ across model versions and 
tasks, but the prompt-discipline and verification pattern do not.*

*Last updated: 25/6/2026.*
