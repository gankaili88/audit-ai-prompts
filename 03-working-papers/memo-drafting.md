# Audit Memo Drafting

**Task:** Produce a working paper audit memorandum on a contentious 
revenue recognition judgement under MFRS 15, suitable for review by 
the engagement manager and partner and possibly the engagement 
quality review (EQR) partner under ISA 220 (Revised). The memo must 
test management's accounting position rather than restate it, engage 
the relevant MFRS and ISA framework with paragraph-level citations, 
identify quality control escalation requirements, and bracket the 
conclusion explicitly pending evidence review.

**Scenario used:** A constructed scenario based on a realistic and 
genuinely contentious Malaysian audit issue — a listed property 
developer client recognising revenue over time under MFRS 15 
paragraph 35(c) on residential property sales governed by Schedule H 
of the Housing Development (Control and Licensing) Act 1966 (HDA), 
using the cost-to-cost input method to measure progress. The scenario 
deliberately replicates the kind of judgement that would escalate to 
a written memo on the audit file with partner sign-off.

**Model used:** Claude (claude.ai), web interface.

**Verification approach:** For this file, verification has three 
components: (a) checking that v2's structural approach matches how a 
contentious audit memo should be drafted in real Big Four practice 
(audit-judgement verification); (b) verifying specific MFRS and ISA 
paragraph references against the MASB-issued PDFs and the IAASB 
Handbook 2023–2024 edition; and (c) testing whether Claude's legal 
characterisations of HDA Schedule H SPAs are asserted as fact (which 
would be fabrication) or flagged as matters requiring external legal 
opinion (which would be correct professional posture).

---

## Prompt v1 (rough)
A Malaysian property developer client is recognising revenue
over-time on residential property sales under MFRS 15. The contracts
are standard HDA Schedule H SPAs. They've recognised RM 142m revenue
to date on a project that's 38% complete.
Write an audit memo on this for me.

## What v1 got wrong

Despite being vague, the prompt produced a polished, structured 
nine-section Word document. The polish made the failures harder to 
spot — but on inspection, v1 contained several substantive failures 
that would not have survived manager review on a real audit. The 
full v1 output is reproduced at the end of this file. The key issues:

1. **Concluded before testing.** Section 2.1 of v1 stated the 
   over-time recognition policy *"is supportable under MFRS 15.35(c)"* 
   as an *"audit conclusion"* — before any audit procedures had been 
   performed. The memo was internally contradictory: Section 2.1 
   reached a conclusion, while Section 9 bracketed the conclusion as 
   pending procedures. A memo on a contentious issue cannot 
   pre-conclude the issue.

2. **Fabricated legal claims about HDA Schedule H.** v1 asserted as 
   established fact that *"the unit is customised to the purchaser's 
   specifications"* (not generally true in Malaysian Schedule H 
   practice — units are predominantly standard floor plans), that 
   *"the HDA prohibits resale or substitution"* (an overstated legal 
   characterisation), and that *"Schedule H payment terms... confirm 
   an enforceable right to payment for performance completed to date, 
   including a profit component"* (asserts the contested legal 
   conclusion as fact when this is precisely the question requiring 
   legal analysis).

3. **Fabricated authority reference.** Section 2.1 referenced 
   *"Malaysian Institute of Accountants (MIA) guidance"* without 
   citing the guidance by title, date, or reference. This is the 
   same named-document fabrication pattern observed in the 
   `mfrs-comparison.md` file. The reference is unverifiable as 
   stated and should not be relied upon.

4. **Circular numerical reasoning.** Section 3.1 derived an "implied 
   GDV" of RM 374m by dividing management's revenue (RM 142m) by 
   management's stage of completion (38%), then presented this 
   derived figure as a cross-check against management's inputs. The 
   fabricated GDV then propagated through Section 5.2's sensitivity 
   analysis (RM 7.36m and RM 7.6m revenue impact for ±2pp SOC 
   variance). A working paper that uses management's own inputs to 
   verify management's own conclusion is committing a basic circular 
   reasoning error.

5. **Missed the top audit risk.** v1's risk matrix did not include 
   the legal enforceability question on paragraph 35(c) as a 
   high-likelihood, high-impact risk. If Schedule H SPAs do not in 
   fact provide an enforceable right to payment for performance 
   completed to date including a reasonable profit margin, the 
   entire RM 142m cumulative revenue is misstated. This is the 
   central audit risk and v1 missed it.

6. **Missed the cost-to-cost vs output-method appropriateness 
   question.** When physical progress is observable through 
   architect-certified construction stages under Schedule H, the 
   question of whether cost-to-cost (input method under paragraphs 
   B17–B19) or stage certification (output method under paragraphs 
   B15–B16) more faithfully depicts performance is a substantive 
   audit question. v1 listed it as procedure 10 (analytical 
   procedure) but did not frame it as a substantive policy question.

7. **Scope creep.** v1 included a going concern section (ISA 570) 
   without any indicators warranting it, a full disclosure checklist 
   that belongs on a separate file, and contract assets/liabilities 
   testing that belongs on a separate schedule. The memo bundled 
   four different working paper deliverables into one document, 
   signalling pattern-matched template usage rather than considered 
   drafting.

8. **No engagement with ISA 220 quality control.** A contentious 
   revenue recognition memo of this scale (RM 142m cumulative revenue, 
   contested legal characterisation, listed entity) would engage 
   ISA 220 (Revised) quality management requirements: engagement 
   partner consultation, technical desk consultation, external legal 
   opinion, EQR review. v1 did not engage with any of these.

9. **No engagement with prior-period continuity.** RM 86m was 
   recognised in FY24 using the same approach. If FY25 concludes the 
   approach is incorrect, MFRS 108 prior-period restatement is 
   triggered. v1 did not address this.

10. **Over-engineered template format.** Nine sections, seven tables, 
    signature blocks, and a confidentiality footer — for one audit 
    issue. In real practice, this would be one to two pages of 
    analytical prose. The format signalled AI pattern-matching to 
    "audit memo template" rather than considered drafting for the 
    specific contested issue.

---

## Prompt v2 (refined)
You are an ICAEW-qualified audit senior at a Big Four firm in Malaysia,
drafting an audit memorandum for review by the engagement manager and
partner on a contentious revenue recognition judgement. The memo will
be filed on the audit file and may be reviewed by the engagement
quality review (EQR) partner under ISA 220.
Client: Listed Malaysian property developer (Bursa Main Market),
reports under MFRS.
The audit question to be addressed in this memo:
Is management's over-time recognition of revenue on Project Bayu under
MFRS 15 paragraph 35(c) appropriate, given (a) the legal characteristics
of Schedule H sale and purchase agreements under the Housing Development
(Control and Licensing) Act 1966 (HDA), and (b) the use of the cost-to-cost
input method to measure progress where physical construction stage is
also observable?
Facts:
184 sale and purchase agreements signed in FY25 for residential units
in Project Bayu, all governed by Schedule H of the HDA
Construction commenced January 2024; expected completion December 2026
As at 30 June 2025 (year-end), Project Bayu is 38% complete by
construction stage
Management has recognised RM 142m cumulative revenue (RM 86m in FY24
RM 56m in FY25) using over-time recognition with cost-to-cost input
method

Management's position: Schedule H SPAs satisfy MFRS 15 paragraph 35(c)
— entity's performance does not create an asset with alternative use
and entity has enforceable right to payment for performance completed
to date including a reasonable profit margin

Memo structure required:
Background — client, project, contract type, accounting position,
prior-period treatment (FY24 RM 86m recognised under same approach).
The audit question — state explicitly. Two sub-questions:
(a) does paragraph 35(c) apply to Schedule H SPAs?
(b) is cost-to-cost an appropriate measure of progress under
paragraphs B14–B19, given that architect-certified physical stage
is also observable?
Analysis of paragraph 35(c) applicability — engage the two limbs
of the test. For each limb, identify what audit evidence would be
required and what would constitute a counter-finding. Do NOT assert
the conclusion as fact.
Analysis of measure-of-progress appropriateness — evaluate under
paragraphs B14–B19. Address the shortcoming of input methods
identified at paragraph B19.
Prior-period continuity — if FY25 audit conclusion differs from
FY24 treatment, address MFRS 108 prior-period restatement.
Quality control engagement — identify ISA 220 requirements
triggered. Identify whether this should be an EQR matter.
Conclusion framing — bracket the conclusion explicitly as
[pending evidence review and management/partner consultation].
Do not draw a final conclusion. Identify the specific evidence
that would support each possible conclusion.

Constraints:
Do not fabricate authority references. If you cite "MIA guidance"
or any specific Big Four technical publication, you must give the
title, date, and reference. If you cannot, do not cite it.
Do not invent specific legal characterisations of HDA Schedule H
beyond what is publicly stated in the legislation itself.
Do not perform circular numerical cross-checks.
This memo addresses revenue recognition policy only. Do not include
going concern analysis, full disclosure checklist, contract
asset/liability testing, or other matters that belong on separate
working papers.
Cite MFRS 15 and ISA paragraph numbers where specific. Length:
approximately 800 words.

## Example output (v2)

> **AUDIT MEMORANDUM**
> **Revenue Recognition Policy — Project Bayu**
> *MFRS 15 Over-Time Recognition — Paragraph 35(c) Applicability and Measure of Progress*
>
> **Status:** DRAFT — Pending evidence review and partner consultation
>
> **1. Background**
>
> The client is a Malaysian property developer listed on the Main 
> Market of Bursa Malaysia Securities Berhad, reporting under MFRS. 
> Project Bayu is a residential development comprising 184 SPAs in 
> the prescribed form of Schedule H under the HDA. Construction 
> commenced January 2024; practical completion expected December 2026. 
> As at 30 June 2025, management's estimate of construction completion 
> is 38% by physical construction stage.
>
> Management recognises revenue from Project Bayu over time under 
> MFRS 15 paragraph 35(c), using the cost-to-cost input method. 
> Cumulative revenue recognised stands at RM 142 million (RM 86m FY24 
> + RM 56m FY25). The FY24 audit accepted the same methodology. The 
> consistency of treatment across periods is directly relevant to the 
> analysis at Section 5.
>
> **2. The Audit Question**
>
> The central audit question this memorandum addresses is whether 
> management's recognition of revenue over time on Project Bayu under 
> MFRS 15 paragraph 35(c) is appropriate, having regard to (a) the 
> legal characteristics of Schedule H SPAs under the HDA and (b) the 
> use of the cost-to-cost input method to measure progress where 
> physical construction stage is also observable.
>
> This breaks into:
> - **Sub-question A — Paragraph 35(c) applicability:** Do Schedule H 
>   SPAs satisfy both limbs of the criterion (no alternative use; 
>   enforceable right to payment for performance to date including 
>   reasonable profit margin)?
> - **Sub-question B — Measure of progress:** Under paragraphs B14–B19, 
>   is cost-to-cost the most appropriate method given that 
>   architect-certified physical stage of 38% is also observable?
>
> **3. Analysis of Paragraph 35(c) Applicability**
>
> Both limbs of paragraph 35(c) must be met concurrently. Failure of 
> either limb would preclude over-time recognition under this paragraph.
>
> *Limb (i) — No Alternative Use (paragraph 36):* Management asserts 
> that the residential units are constructed to specific configurations 
> per each Schedule H SPA and that the statutory prescribed form 
> contractually prevents substitution. Audit evidence required 
> includes: inspection of executed SPAs to verify unit specifications; 
> legal counsel consideration of whether HDA Schedule H creates a 
> contractual restriction within the meaning of paragraph 36 (matter 
> requiring legal analysis — see Section 6); enquiry on practical 
> restrictions arising from construction methodology. **Counter-finding 
> risk:** if SPAs permit substitution of an equivalent unit, or if 
> HDA Schedule H does not in law constitute the type of contractual 
> restriction contemplated by paragraph 36, this limb fails.
>
> *Limb (ii) — Enforceable Right to Payment for Performance Completed 
> to Date (paragraph 37):* Schedule H SPAs prescribe a milestone-based 
> progress payment structure. The critical audit question is whether 
> these milestone payment obligations, together with the statutory 
> framework of the HDA, constitute an enforceable right to compensation 
> for performance completed to date — including reasonable profit — in 
> the event of purchaser termination, as opposed to merely rights to 
> unpaid progress instalments. *This is a matter of legal 
> characterisation that the audit team is not qualified to resolve 
> without external legal opinion (see Section 6).* **Counter-finding 
> risk:** if the contractual and statutory framework is found to limit 
> the developer's recovery upon purchaser termination to progress 
> payments already due (rather than the full measure of compensation 
> for performance including profit margin), or if the HDA restricts 
> the developer's ability to retain amounts in excess of defined 
> liquidated damages *[see verification log: legal characterisation 
> stated as counter-finding risk; requires legal confirmation]*, this 
> limb may not be satisfied.
>
> **4. Analysis of Measure of Progress**
>
> Paragraphs B15–B16 describe output methods (direct measurement of 
> value delivered — physical units, milestones, surveys). Paragraphs 
> B17–B19 describe input methods (resources consumed relative to total 
> expected consumption — costs, labour hours).
>
> *Paragraph B19 shortcoming.* B19 specifically flags that if the 
> entity's inputs are not consumed in proportion to the transfer of 
> goods or services to the customer, a straight cost-to-cost ratio may 
> overstate or understate the stage of completion. For a residential 
> development, cost incurrence does not necessarily correlate with the 
> transfer of value to purchasers — for example, substructure and 
> foundation works are cost-intensive but may not represent a 
> commensurate transfer of control to the purchasers of the residential 
> units. Management's application of the cost-to-cost method should be 
> evaluated for whether any adjustment is required under paragraph B19.
>
> *Observable physical construction stage.* Management's own records 
> indicate a physical construction stage of 38% certified by the project 
> architect. This constitutes an output measure. The question for the 
> engagement is whether cost-to-cost is justified where an output 
> measure — architect certification — is independently observable and 
> may represent a more direct measure of progress under paragraphs 
> B15–B16. If the two measures yield materially consistent estimates, 
> the divergence may not be financially significant for FY25; however, 
> this cannot be concluded without reviewing both directly.
>
> **5. Prior-Period Continuity**
>
> Management applied the same approach in FY24 (RM 86m recognised), 
> and the FY24 audit accepted this treatment. If the FY25 audit 
> concludes over-time recognition under paragraph 35(c) is not 
> supportable, MFRS 108 paragraph 41 *[see verification log: paragraph 
> reference requires verification; operative requirement may be at 
> paragraph 42]* would require retrospective restatement. The entire 
> RM 142m cumulative revenue would require reversal and re-recognition 
> at completion or contractually defined handover.
>
> If the FY25 conclusion changes only the measure of progress (from 
> cost-to-cost to architect-certified physical stage) without disturbing 
> the over-time recognition conclusion, this would constitute a change 
> in accounting estimate under MFRS 108 paragraph 32 *[see verification 
> log: paragraph reference requires verification; operative requirement 
> may be at paragraph 36]* (prospective application), unless it can be 
> demonstrated that the prior-period application was in error.
>
> **6. Quality Control — ISA 220 Considerations**
>
> Under **ISA 220 paragraph 18 (Revised)** *[see verification log: 
> paragraph reference requires verification; engagement partner's 
> responsibility may sit across paragraphs 13–18 of ISA 220 (Revised)]*, 
> the engagement partner is responsible for the overall quality of the 
> engagement and must evaluate significant judgements. The revenue 
> recognition treatment for Project Bayu constitutes a significant 
> judgement (RM 142m cumulative; contested interpretation of paragraph 
> 35(c) in a Schedule H context; prior-period continuity risk). Direct 
> partner involvement is required before a conclusion is reached.
>
> *Technical Consultation.* Given the technical complexity and 
> divergent practice views across Malaysian property developers, 
> consideration should be given to consultation with the firm's MFRS 
> technical desk.
>
> *External Legal Opinion.* Two matters require legal analysis outside 
> the audit team's competence: (i) right-to-payment enforceability 
> under paragraph 37; (ii) no-alternative-use characterisation under 
> paragraph 36. The engagement partner should assess whether external 
> Malaysian property law counsel is required.
>
> *Engagement Quality Review.* Given the significance of the judgement, 
> the listed entity status, and the prior-period restatement risk, 
> this matter should be assessed against the firm's criteria for EQR 
> under **ISA 220 paragraph 21 (Revised)** *[see verification log: 
> paragraph reference requires verification]*.
>
> **7. Conclusion Framing**
>
> *No final audit conclusion is drawn in this memorandum. The final 
> conclusion is subject to (i) completion of the evidence procedures 
> identified in Sections 3 and 4; (ii) receipt and review of any 
> external legal opinion obtained pursuant to Section 6; and (iii) 
> engagement partner review and sign-off.*
>
> **Scenario A — Over-Time Recognition Confirmed.** Requires: external 
> legal opinion confirming paragraph 35(c) limbs are satisfied; audit 
> procedures over cost-to-cost computation confirming no paragraph B19 
> adjustment required (or that any required adjustment is quantified).
>
> **Scenario B — Point-in-Time Recognition Required.** Arises if legal 
> analysis concludes one or both limbs of paragraph 35(c) are not 
> satisfied. Consequence: full reversal of RM 142m cumulative revenue; 
> revenue deferred to point-in-time recognition (likely at vacant 
> possession). MFRS 108 retrospective restatement required, subject to 
> impracticability assessment.
>
> **Scenario C — Over-Time Confirmed but Measure of Progress Revised.** 
> Arises if paragraph 35(c) is satisfied but cost-to-cost requires 
> paragraph B19 adjustment, or architect-certified stage is more 
> faithful. Consequence: recomputation; assessment of materiality; 
> consideration of whether change in estimate (prospective) or 
> correction of error (retrospective).
>
> [Signature blocks: Senior, Manager, Partner]

---

## Verification log

**Verified against:** MASB-issued PDFs of MFRS 15, MFRS 108, MFRS 119 
where referenced; IAASB Handbook 2023–2024 for ISA 220 (Revised) and 
ISA 520; ICAEW Audit and Assurance study materials; my own analysis 
of Malaysian property developer audit practice and Schedule H SPAs.

### Improvements from v1 to v2

The refined prompt produced substantial improvements across every 
dimension v1 failed:

- **Concluded before testing → properly bracketed pending evidence.** 
  v2 explicitly states *"no final audit conclusion is drawn in this 
  memorandum"* and lists three possible scenarios (A, B, C) with the 
  evidence required for each. The internal contradiction in v1 
  (Section 2.1 concluding, Section 9 not concluding) is eliminated.
- **Fabricated legal claims → matters requiring external legal opinion.** 
  v1 asserted as fact that Schedule H SPAs satisfy both limbs of 
  paragraph 35(c). v2 explicitly identifies the right-to-payment 
  question as *"a matter of legal characterisation that the audit team 
  is not qualified to resolve without external legal opinion."*
- **No fabricated authority references.** v1's reference to "MIA 
  guidance" without title or date is gone. v2 does not invent named 
  documents.
- **No circular numerical reasoning.** v1's "implied GDV" derivation 
  (RM 142m ÷ 38% = RM 374m) used to "verify" management's own inputs 
  is eliminated. v2 defers quantitative analysis to substantive testing 
  schedules.
- **Legal enforceability question is now the central analytical focus.** 
  v1 missed this entirely as a high-impact audit risk. v2 makes it 
  the central question of Section 3.2 and explicitly identifies it 
  as the matter requiring external counsel.
- **Cost-to-cost vs output-method analysis substantively engaged.** 
  v2's Section 4 addresses paragraph B19's known shortcoming of input 
  methods and the existence of the architect-certified physical stage 
  as an observable output measure. The substructure/foundation cost 
  example is a genuine technical insight that an experienced audit 
  senior would document.
- **Scope creep eliminated.** v1 included going concern, full 
  disclosure checklist, and contract asset testing — none belong on 
  a revenue recognition policy memo. v2 removes all three.
- **ISA 220 quality control engagement.** v2's Section 6 engages 
  partner consultation, technical desk, external legal opinion, and 
  EQR — exactly the quality management framework a contentious memo 
  should engage.
- **Prior-period continuity addressed.** v2's Section 5 explicitly 
  engages MFRS 108 retrospective restatement vs change in accounting 
  estimate. v1 did not address this at all.
- **Format reduced from over-engineered nine-section template to 
  focused seven sections.** The memo now reads as a draft for partner 
  review rather than a filed document with pre-completed signature 
  blocks.

### Errors v2 still made

The errors that remain are precision-level rather than substantive. 
The audit-judgement framework is correct; specific paragraph 
references warrant verification.

**1. ISA 220 (Revised) paragraph references require verification.** 
v2 cites paragraph 18 (engagement partner responsibility) and 
paragraph 21 (EQR criteria) of ISA 220 (Revised). These should be 
verified against the IAASB Handbook 2023–2024 edition for ISA 220 
(Revised), which was effective for audits of financial statements 
for periods beginning on or after 15 December 2022 and renumbered 
when revised. The substance of v2's claims is correct (engagement 
partner has overall responsibility for engagement quality; EQR 
requirements are specified within ISA 220); the specific paragraph 
numbers may need adjustment. The engagement partner's overall 
responsibility may sit at paragraph 13 or span paragraphs 13–18.

**2. MFRS 108 paragraph references require verification.** v2 cites 
paragraph 41 for retrospective restatement and paragraph 32 for 
prospective application of change in estimate. Direct verification 
against the MASB-issued MFRS 108 PDF would confirm the operative 
paragraphs. Conventionally:
- Retrospective restatement of prior-period errors is operative at 
  paragraph 42 (paragraph 41 introduces the section).
- Prospective application of change in accounting estimate is 
  operative at paragraph 36 (paragraph 32 introduces the concept).

The conceptual framework v2 applies is correct; the specific 
paragraph numbers may need adjustment.

**3. Schedule H clauses referenced generically.** Schedule H has 
specific numbered clauses governing progress payments, late delivery 
liquidated damages, defects liability, and termination. A rigorous 
memo would cite specific Schedule H clauses by number where the 
clause is operative to the analysis. v2 refers to Schedule H 
provisions generically. Acceptable for a draft memo that explicitly 
identifies external legal opinion as required, but could be tighter.

**4. One legal characterisation in Section 3.2 counter-finding.** 
v2 states as a counter-finding risk that *"the HDA restricts the 
developer's ability to retain amounts in excess of defined liquidated 
damages."* This is a specific legal claim. v2 frames it as a 
counter-finding risk (i.e., a possibility to investigate) rather than 
as positive law, which is less egregious than v1's pattern of 
asserting legal conclusions. Acceptable for a draft, but rigorous 
practice would either cite the specific HDA provision (likely Schedule 
H clause governing LADs) or flag the assertion as requiring legal 
confirmation.

**5. MFRS 108 error vs change in accounting policy distinction not 
drawn out.** If FY24's application was based on the same facts and 
the same standard, and FY25 reaches a different conclusion on legal 
interpretation, whether this constitutes a "prior period error" 
under MFRS 108 paragraph 5 definition (requiring retrospective 
restatement under paragraph 42) or a "change in accounting policy" 
(requiring retrospective application under paragraphs 19–27) is 
itself a judgement. v2's Section 5 elides this distinction. Minor 
for a draft memo, but a comprehensive memo would address it.

### What this teaches about AI verification on contested audit judgements

This file produces the strongest v2 output across the five files in 
this project, and the reasons are instructive.

**1. The prompt was the most diagnostic.** Every constraint in the 
v2 prompt mapped to a specific v1 failure: *"do not fabricate authority 
references"* → addressed v1's fabricated MIA guidance citation; *"do 
not perform circular numerical cross-checks"* → addressed v1's implied 
GDV derivation; *"this memo addresses revenue recognition policy 
only"* → addressed v1's scope creep into going concern and disclosure 
checklists; *"do not assert the conclusion as fact"* → addressed v1's 
pre-conclusion in Section 2.1. Diagnostic prompts that name specific 
failure modes produce outputs that resolve those failure modes.

**2. The prompt framed the audit question as contested, not 
documented.** v1's vague prompt allowed Claude to treat the memo as 
a documentation exercise (recording an issue Claude assumed was 
settled). v2's prompt explicitly framed the question as one requiring 
analysis of two limbs of paragraph 35(c) plus the input/output method 
choice. Framing matters: when the prompt presupposes a contested 
issue, Claude engages with the contest.

**3. The prompt required quality control engagement.** Specifying 
ISA 220 partner consultation, technical desk, external legal opinion, 
and EQR triggered Claude to engage the firm's quality management 
processes. This produces output that reflects how a contentious memo 
would be handled in real Big Four practice rather than how an 
inexperienced student might draft it.

**4. The prompt required the conclusion to be bracketed with explicit 
scenarios.** Asking Claude to identify three possible scenarios (A: 
over-time confirmed; B: point-in-time required; C: measure of 
progress revised) with the evidence required for each transformed the 
conclusion section from a single bracketed line into a substantive 
framework for evidence evaluation. The structure of the conclusion 
mirrored the analytical structure of the memo.

The output format itself — a Word document with formatted headings, 
signature blocks, and confidentiality footer — is also revealing. 
When the prompt frames the task as a memo for review by manager and 
partner, Claude defaults to filed-document format rather than 
chat-output format. This is the format real working papers take and 
is appropriate for the task; for the verification log, the fact that 
Claude produced this format unprompted is itself worth noting.

### Recurring pattern to watch for

When using AI for working paper memos on contested audit judgements:

- **Always frame the audit question as contested and requiring 
  evidence, not as documentation of a settled issue.** Vague memo 
  prompts produce memos that pre-conclude.
- **Always prohibit fabrication of named authority references** 
  (MIA guidance, technical desk publications, regulatory statements). 
  If the model cannot cite by title and date, it should not cite.
- **Always require the memo to identify legal questions requiring 
  external counsel.** AI tools will otherwise assert legal 
  characterisations as established fact.
- **Always require ISA 220 (Revised) engagement** — partner 
  consultation, technical desk, external legal opinion, EQR. Without 
  prompting, the model treats the memo as the auditor's own 
  conclusion rather than as a draft for senior review.
- **Always bracket the conclusion with explicit alternative scenarios 
  and the evidence required for each.** Single-bracket conclusions 
  ([pending review]) tell the reader less than a structured framework 
  of possible outcomes.
- **Always bound the memo's scope** — going concern, disclosure 
  checklists, contract asset testing belong on separate working 
  papers. Without explicit bounding, the model bundles four 
  deliverables into one document.
- **Always verify specific paragraph references against the operative 
  standards.** Even strong v2 outputs may cite paragraph 18 when 
  paragraph 13 is operative; paragraph 41 when paragraph 42 is 
  operative. The precision discipline still applies.

A diagnostic prompt of this kind can produce a working paper memo 
that an engagement manager and partner could review and approve 
(subject to evidence completion), rather than rewrite. The 
verification step remains essential — especially for paragraph 
references — but the editing burden is much smaller than on a vague 
prompt.

---

## v1 output (for reference)

> **AUDIT WORKING PAPER — MEMORANDUM**
> [Engagement: Client Name — FY2025 Statutory Audit]
> [WP Ref: REV-01]
> Area: Revenue Recognition — MFRS 15 Over-Time Method
>
> **1. Purpose and Scope**
> This memorandum documents the audit procedures performed, evidence 
> obtained, and conclusions reached regarding the client's recognition 
> of revenue over time on residential property sales under MFRS 15 
> Revenue from Contracts with Customers.
>
> [...full v1 output retained in repo for transparency. Key contested 
> elements include: Section 2.1 audit conclusion "the over-time 
> recognition policy is supportable under MFRS 15.35(c)"; reference to 
> "Malaysian Institute of Accountants (MIA) guidance" without source; 
> Section 3.1 "implied GDV (Revenue ÷ SOC) = RM 374m (142 ÷ 38%)" 
> circular cross-check; Section 6 going concern bolt-on; nine-section 
> over-engineered template format.]

---

*Verification performed against MASB-issued MFRSs and the IAASB 
Handbook 2023–2024 edition. The errors in v1 are characteristic of 
AI failure modes when prompted vaguely for memos on contested 
issues; the corrections in v2 reflect the diagnostic value of 
well-designed prompts. Specific paragraph references in v2 require 
verification against operative standards. The audit-judgement 
framework v2 applies is correct.*

*Last updated: 25/6/2026.*
