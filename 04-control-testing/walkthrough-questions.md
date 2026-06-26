# Walkthrough Questions

**Task:** Produce a walkthrough procedure for the procurement and 
payment cycle of a listed Malaysian property developer client, 
suitable for working paper filing under ISA 315 (Revised 2019). 
The procedure must distinguish inquiry from observation from 
inspection (the methodology of a walkthrough as opposed to a 
general process interview), tie each procedure to a specific 
control point and audit assertion, engage ISA 240 fraud-specific 
inquiries and ISA 550 related-party inquiries as structured 
sections, and address the property-developer-specific control 
points (QS certification, retention sums, JV partner and landowner 
related-party arrangements).

**Scenario used:** Listed Malaysian property developer (Bursa Main 
Market), reports under MFRS, year-end 30 June 2025. Procurement 
and payment cycle covering supplier invoice approval and payment 
authorisation, with specific consideration of construction 
contractor progress claims and retention sum mechanics.

**Model used:** Claude (claude.ai), web interface.

**Verification approach:** Three components: (a) verifying that v2's 
methodology matches ISA 315's walkthrough framework (observation of 
a single transaction processed end-to-end, not general interview); 
(b) verifying specific ISA paragraph references against the IAASB 
Handbook 2023–2024 edition for ISA 315 (Revised 2019), ISA 240, and 
ISA 550; (c) assessing whether the property-developer-specific 
elements (QS certification, retention sums, related-party 
considerations) are integrated into the body of the walkthrough or 
treated as afterthoughts.

---

## Prompt v1 (rough)
I'm an audit associate doing a walkthrough of the procurement and
payment process at a Malaysian property developer client. Give me
walkthrough questions to ask the AP team.

## What v1 got wrong

v1 produced a professionally-competent set of process-area questions 
covering procurement initiation through to system access controls, 
with property-developer-specific touches at the end. The output 
looked usable on the surface — but on closer inspection, contained 
several methodological failures that would matter in a real working 
paper filing. The full v1 output is reproduced at the end of this 
file. The key issues:

1. **Interview questions, not walkthrough procedures.** A walkthrough 
   under ISA 315 (Revised 2019) is an observation procedure — the 
   auditor observes a single transaction being processed end-to-end 
   while the control owner walks through each step. v1 produced 
   inquiry questions ("describe your process") rather than walkthrough 
   procedures ("show me one transaction processed yesterday"). The 
   methodological framing is wrong.

2. **No mapping to audit assertions.** Each walkthrough question 
   should test one or more specific assertions (occurrence, 
   completeness, accuracy, cut-off, authorisation, classification). 
   v1's questions are control-point-oriented but the assertion 
   they test is not stated. A walkthrough working paper without 
   assertion mapping cannot be used to evaluate control design 
   effectiveness.

3. **ISA 240 fraud inquiries reduced to a postscript.** Related-party 
   transactions, QS sign-off integrity, retention sum manipulation, 
   kickback risk, fictitious supplier risk — all are real procurement 
   fraud risks. v1 mentioned some in a closing paragraph 
   ("a few angles worth probing") but did not structure them as a 
   numbered ISA 240 inquiry section.

4. **Missing IT controls structure.** Modern AP processes have 
   critical IT controls — role-based access enforcing segregation 
   of duties, payment file integrity between ERP and bank, audit 
   log retention, user access provisioning. v1 mentioned access 
   review once but did not treat IT general controls as a distinct 
   area.

5. **Missing observation procedures.** A walkthrough working paper 
   should specify what the auditor will observe (one PO being 
   raised, one invoice being processed, one exception being 
   investigated). v1 had questions to ask but did not specify the 
   observation steps that constitute the walkthrough.

6. **No ISA 315 paragraph references.** ISA 315 (Revised 2019) 
   paragraphs 25–27 are the operative requirements for understanding 
   the entity's system of internal control. v1 did not engage with 
   the underpinning framework.

7. **Construction-progress receipt treated as widget receipt.** 
   For property developers, "goods receipt" is QS-certified 
   construction progress, not delivery of physical goods. The QS 
   certification is the central control point and v1 buried it in 
   a closing afterthought rather than structuring it as a core 
   control stage.

8. **Missing cut-off-specific questions.** Year-end cut-off is a 
   critical area in procurement (GRNI accruals, invoices straddling 
   year-end). v1 mentioned month-end accruals but did not structure 
   cut-off-specific procedures for the year-end audit.

9. **Missing payment file integrity controls.** The bank file 
   generation control (between ERP creation and bank platform upload) 
   is a critical IT-dependent control point. v1 missed this entirely.

10. **No walkthrough memo structure.** A walkthrough produces a 
    working paper memo recording what was observed, who participated, 
    what evidence was inspected, and the conclusion on control design 
    and implementation. v1 produced questions but did not structure 
    the output for a walkthrough memo with a conclusion framework.

---

## Prompt v2 (refined)
You are an ICAEW-qualified audit senior at a Big Four firm in Malaysia,
preparing a walkthrough procedure for the procurement and payment
cycle of a listed property developer client (Bursa Main Market,
reports under MFRS, year-end 30 June 2025).The walkthrough will be performed under ISA 315 (Revised 2019)
paragraphs 25–27, supplemented by ISA 240 fraud-specific inquiries
and ISA 550 related-party inquiries.A walkthrough under ISA 315 is an OBSERVATION procedure: the auditor
observes a single transaction being processed end-to-end while the
control owner walks through each step. It is not an interview about
the process in general, it is a procedure performed on one specific
transaction in real time. The output should reflect this methodology.Produce the walkthrough procedure structured as follows:
Walkthrough objective and scope — assertion(s) tested, control
objectives, ISA 315 paragraph cited, timing.
Pre-walkthrough preparation — documents to obtain, transactions
to identify, personnel to confirm in advance.
Walkthrough procedures structured by process stage. At each
 stage: specific INQUIRIES, specific OBSERVATIONS, specific
INSPECTIONS, the CONTROL ATTRIBUTE being tested, the AUDIT
ASSERTION being tested.
Cover at least: procurement initiation, PO issuance,
goods/services receipt (with QS certification for construction),
invoice processing, payment approval and execution, vendor master
maintenance.
ISA 240 fraud-specific inquiries — structured as a distinct
section. Address procurement-specific fraud risks: fictitious
suppliers, kickbacks, related-party concealment, vendor bank
   account fraud.
ISA 550 related-party inquiries — distinct section for
related-party identification in procurement, with reference to
MFRS 124.
IT general controls — distinct section covering role-based
access provisioning, payment file integrity between ERP and bank,
audit log retention, user access reviews.
Cut-off-specific procedures for year-end audit — GRNI accruals,
invoices straddling year-end, MFRS 137 boundary between accruals
and provisions.
Conclusion framework — design adequacy, implementation evidence,
exceptions to follow up. Bracket as [pending walkthrough
performance].
Constraints:
Do not produce generic open-ended interview questions of the form
"describe your process." All inquiries should be specific to a
control point and tied to an assertion.
Distinguish inquiry from observation from inspection at each stage.
Cite ISA 315 (Revised 2019), ISA 240, ISA 550 paragraph numbers
where specific. Flag references as "[to verify]" if uncertain.
This is a property developer client — engage construction progress
certification (QS), retention sums on contractor invoices, and JV
partner / landowner related-party considerations as core elements,
not afterthoughts.
Length: approximately 900 words.

## Example output (v2)

> **Procurement and Payment Cycle — Walkthrough Procedure**
> **Client:** [Bursa-listed Property Developer] | **FY End:** 30 June 2025
>
> **1. Walkthrough Objective and Scope**
>
> *Assertions tested:* Occurrence, accuracy, authorisation, cut-off, 
> and completeness over procurement expenditure and trade payables.
>
> *ISA basis:* ISA 315 (Revised 2019) paragraphs 25–27 *[see verification log: range should be verified against IAASB Handbook]* — the auditor 
> selects one specific transaction and traces it end-to-end through 
> the system in real time, observing each control as it operates.
>
> *Timing:* Interim fieldwork (October–November 2025), prior to 
> year-end substantive procedures.
>
> **2. Pre-Walkthrough Preparation**
>
> Before the walkthrough session, the auditor shall:
>
> - Identify one construction contractor payment (selecting a 
>   transaction involving retention sum release to maximise coverage 
>   of QS certification controls) and one operating expense payment.
> - Confirm attendance of procurement officer, QS/project manager, 
>   AP supervisor, and treasury/payment approver.
> - Obtain in advance: Approved Vendor List, Delegation of Authority 
>   matrix, ERP access role matrix, most recent user access review.
> - Map the selected transaction to its PR, PO, GRN/progress claim, 
>   invoice, and payment record before the walkthrough commences.
>
> **3. Walkthrough Procedures by Process Stage**
>
> *Stage A — Procurement Initiation*
>
> *Inquiry:* "Who raised this purchase requisition and what system 
> access level is required to do so? Can a person who raises a PR 
> also approve it?" [Assertion: authorisation; segregation]
>
> *Observation:* Watch the control owner navigate to the PR in the 
> ERP. Observe whether the system prevents the preparer from 
> self-approving.
>
> *Inspection:* Inspect the PR for preparer ID, approver ID, cost 
> centre, project code, and DOA threshold compliance.
>
> *Stage B — PO Issuance*
>
> *Inquiry:* "Is this vendor on the current Approved Vendor List? 
> Who performed the vendor onboarding and when was the last 
> revalidation of their bank account details?" [Assertion: 
> occurrence; accuracy]
>
> *Observation:* Watch the control owner search the vendor in the 
> ERP. Observe whether the system prevents PO issuance to a vendor 
> not on the AVL.
>
> *Inspection:* PO for approved vendor status, contracted rate vs 
> rate on PO, authorisation at correct DOA level. Vendor master 
> bank account last-change log.
>
> *Stage C — Goods/Services Receipt and QS Certification (Construction)*
>
> *Inquiry:* "For this progress claim, who issued the QS progress 
> certificate? Is that individual independent of the contractor? 
> Is the retention percentage applied automatically by the ERP or 
> calculated manually?" [Assertion: occurrence; accuracy]
>
> *Observation:* Match the progress claim to the QS certificate in 
> the system. Observe whether the system auto-calculates retention 
> deduction and prevents payment without a matched GRN or certified 
> progress claim.
>
> *Inspection:* (i) QS progress certificate including certified 
> percentage complete and any back-charges; (ii) GRN or site 
> confirmation; (iii) ERP three-way match status. Verify retention 
> amount against retention sum ledger.
>
> *Stage D — Invoice Processing*
>
> *Inquiry:* "Is the invoice date, amount, and SST treatment 
> reconciled to the PO before posting? Who has authority to override 
> a price variance and what is the tolerance threshold?" [Assertion: 
> accuracy; authorisation]
>
> *Observation:* Watch AP clerk match invoice to PO and GRN/certificate 
> in real time. Observe whether a price or quantity variance triggers 
> a system hold.
>
> *Inspection:* Invoice against PO: vendor name, amount, currency, 
> SST treatment, invoice date within contract period.
>
> *Stage E — Payment Approval and Execution*
>
> *Inquiry:* "Who can create a payment run and who can release it 
> to the bank? Are these the same individual? If the payment file 
> is transmitted electronically, how is file integrity between the 
> ERP and bank portal verified?" [Assertion: authorisation; accuracy]
>
> *Observation:* Watch payment approver review and release the 
> payment batch. Observe whether dual authorisation is required in 
> both the ERP and the bank portal.
>
> *Inspection:* Payment authorisation record for two-approver sign-off; 
> confirm beneficiary account matches vendor master (not a recently 
> changed account).
>
> *Stage F — Vendor Master Maintenance*
>
> *Inquiry:* "Who can add a new vendor or change an existing vendor's 
> bank account? Is that person the same individual who can approve 
> invoices or release payments?" [Assertion: authorisation; occurrence]
>
> *Observation:* Pull up the audit log for the selected vendor's 
> bank account field. Confirm the log shows who made the last change 
> and whether second-level approval was obtained.
>
> *Inspection:* Vendor master change log; cross-reference against 
> any payment made within 30 days of a bank account change.
>
> **4. ISA 240 Fraud-Specific Inquiries**
>
> *Per ISA 240 paragraph 17, the auditor shall inquire of management 
> regarding fraud risks.* *[see verification log: paragraph 17 is correct; Claude's self-flag was over-cautious]*
>
> *Fictitious supplier fraud:* "In the last 12 months, has any 
> vendor been added to the AVL by someone who is also an approver 
> on that vendor's invoices? Is there a periodic conflict-of-interest 
> declaration from procurement staff?"
>
> *Kickbacks / undisclosed rebates:* "Are procurement staff required 
> to declare gifts or hospitality from contractors? Who reviews 
> those declarations? Have there been any whistleblower complaints 
> relating to procurement in FY25?"
>
> *Related-party concealment:* "Are there any contractors or 
> consultants engaged this year in which a director, key management 
> personnel, or their close family members have an interest — 
> including indirectly through a holding company?"
>
> *Vendor bank account fraud (payment diversion):* "What is the 
> process when a vendor requests a bank account change by email? Is 
> the change confirmed by a call to a pre-existing contact number, 
> or only by replying to the email received?" [High inherent risk — 
> business email compromise is prevalent in the Malaysian construction 
> sector.]
>
> **5. ISA 550 Related-Party Inquiries**
>
> *Per ISA 550 paragraphs 12–13* *[see verification log: operative paragraphs are 13–14]*, the auditor shall inquire of management 
> regarding completeness of related-party disclosures.
>
> *JV partner transactions:* "Are any contractors or material 
> suppliers connected to JV partners or their associates? Have any 
> services been procured from the JV partner entity itself?"
>
> *Landowner arrangements:* "Where land was acquired under deferred 
> consideration or profit-sharing with the original landowner, are 
> there ongoing service contracts (project management, marketing) 
> with that landowner or related entities?"
>
> *MFRS 124 disclosure:* Inspect the draft MFRS 124 note against 
> the related-party register. For each related-party procurement 
> transaction, confirm nature and amount are disclosed; confirm 
> whether terms are stated as arm's-length and whether evidence 
> supports that assertion.
>
> **6. IT General Controls**
>
> *Access provisioning:* Inspect a sample user access request: 
> confirm manager approval, IT provisioning log, role assignment 
> consistent with job function.
>
> *Payment file integrity:* Inspect the configuration of the file 
> transfer between ERP and bank's host-to-host portal: confirm 
> hash/checksum validation or equivalent integrity control.
>
> *Audit log retention:* Confirm ERP audit logs are retained for 
> a minimum of seven years, consistent with Companies Act 2016 
> requirements *[see verification log: seven-year retention is correct under section 245; Claude's self-flag was over-cautious]*.
>
> *Periodic user access review:* Inspect the most recent quarterly 
> review sign-off: confirm performed by a business owner (not IT), 
> and that terminated employees and role changes were actioned.
>
> **7. Cut-Off Procedures — Year-End 30 June 2025**
>
> *GRNI accrual:* For goods received or progress certified on or 
> before 30 June 2025 where the vendor invoice had not been received 
> by year-end, inspect the GRNI listing. Agree a sample to QS 
> certificates or GRNs dated pre-30 June.
>
> *Straddling invoices:* Sample invoices dated within 14 days before 
> and after 30 June 2025. Confirm invoices relating to pre-year-end 
> activity are accrued in FY25.
>
> *MFRS 137 boundary:* For contractor claims in dispute at year-end 
> (variation orders contested, LAD deductions), assess whether the 
> obligation meets MFRS 137's definition of a provision (present 
> obligation, probable outflow, reliable estimate) as distinct from 
> a trade payable.
>
> *Retention sums:* Agree retention payable balance to individual 
> contractor retention schedules. Confirm classification as current 
> or non-current per expected release date.
>
> **8. Conclusion Framework [Pending Walkthrough Performance]**
>
> Following walkthrough completion, conclude on:
>
> *Design adequacy:* Does each key control (PR authorisation, 
> three-way match, QS certification, vendor master segregation, 
> dual-authorised payment release) appear designed to prevent or 
> detect the relevant misstatement or fraud risk?
>
> *Implementation evidence:* Has the selected transaction demonstrated 
> that each control operated as described? Document control owner 
> name and role, date observed, evidence inspected, and whether the 
> control operated without exception.
>
> *Exceptions identified:* Document for follow-up where any of the 
> following are noted: control not operating as described; segregation 
> of duties conflict observed in practice; missing QS certificate for 
> certified progress claim; vendor bank account changed within 30 
> days prior to payment with no secondary verification; related-party 
> vendor not appearing in MFRS 124 draft disclosure.
>
> *Impact on audit strategy:* If design or implementation deficiencies 
> are identified, document consequential impact on nature, timing, 
> and extent of substantive procedures over trade payables, accrued 
> liabilities, and construction costs — per ISA 315 (Revised 2019) 
> paragraph 30 *[see verification log: impact-on-substantive link sits in ISA 330, not ISA 315]*.

---

## Verification log

**Verified against:** IAASB Handbook 2023–2024 edition for ISA 315 
(Revised 2019), ISA 240, ISA 330, and ISA 550; MASB-issued MFRS 124 
and MFRS 137; Companies Act 2016 section 245 for record retention; 
my own knowledge of Malaysian property developer audit practice 
including QS certification mechanics, retention sum releases, and 
JV partner / landowner arrangements common in the sector.

### Improvements from v1 to v2

The refined prompt produced substantial improvements across every 
dimension v1 failed:

- **Methodology corrected.** v1 produced interview questions of the 
  "describe your process" form. v2 produces walkthrough procedures 
  with explicit inquiry/observation/inspection trio at each stage. 
  The shift from inquiry-style to observation-style is the central 
  methodological improvement — and matches what ISA 315 actually 
  requires of a walkthrough.
- **Assertion mapping added.** Each stage in v2 carries an explicit 
  bracketed assertion (authorisation, occurrence, accuracy, etc.). 
  v1 was control-point-oriented without assertion mapping.
- **ISA 240 fraud inquiries structured as Section 4.** v1 buried 
  fraud risks in a closing paragraph as "a few angles worth probing." 
  v2 structures four fraud risk categories (fictitious supplier, 
  kickbacks, related-party concealment, vendor bank account fraud) 
  with specific inquiries for each.
- **ISA 550 related-party inquiries structured as Section 5.** Three 
  property-developer-specific related-party risks engaged: JV partner 
  transactions, landowner arrangements with deferred consideration, 
  MFRS 124 disclosure cross-reference.
- **IT general controls structured as Section 6.** Four IT control 
  areas covered (access provisioning, payment file integrity, audit 
  log retention, user access review). v1 mentioned access review 
  once.
- **QS certification treated as core control point in Stage C.** v1 
  buried this in a closing afterthought. v2 makes Stage C 
  (Goods/Services Receipt and QS Certification) a structured stage 
  with three full procedures (inquiry / observation / inspection), 
  treating QS independence and retention calculation as central 
  control tests.
- **Observation procedures specified at every stage.** v1 had 
  questions to ask but did not specify the observation steps. v2 
  specifies what the auditor watches in real time at each stage.
- **Cut-off procedures added as Section 7.** Four cut-off areas 
  covered (GRNI accruals, straddling invoices, MFRS 137 boundary, 
  retention classification). v1 had a brief month-end accruals 
  question with no MFRS 137 framing.
- **Payment file integrity added.** v2 specifically tests the ERP 
  to bank portal file transfer integrity (hash/checksum validation). 
  v1 missed this entirely.
- **Conclusion framework structured.** v2 specifies four conclusion 
  dimensions (design adequacy, implementation evidence, exceptions 
  identified, impact on audit strategy) with five specific exception 
  types. v1 had no conclusion framework.

### Errors v2 still made

The errors that remain are precision-level rather than substantive. 
Two of them are over-cautious self-flags by Claude — citations that 
were actually correct but flagged as uncertain.

**1. ISA 240 paragraph 17 self-flagged as uncertain — citation is 
correct.** Claude wrote *"Per ISA 240 paragraph 17 [to verify — 
paragraph addresses management inquiries; fraud risk assessment 
procedures are at paragraphs 24–27]."* Verification against the 
IAASB Handbook confirms that paragraph 17 of ISA 240 is indeed the 
operative paragraph for inquiries of management regarding fraud — 
covering management's assessment of fraud risk, management's process 
for identifying and responding to fraud risk, management's 
communication to those charged with governance, and management's 
communication to employees. The self-flag was over-cautious. This 
is worth noting because **over-cautious flagging is itself a failure 
mode** — it suggests the model does not have complete confidence in 
references that are well-established.

**2. Companies Act 2016 seven-year retention self-flagged — claim 
is correct.** Claude wrote *"Companies Act 2016 requirements [to 
verify retention period]."* Section 245 of the Companies Act 2016 
specifies that accounting and other records shall be retained for 
seven years from the end of the financial year. The seven-year 
period Claude cited is correct. Self-flag was again over-cautious.

**3. ISA 550 paragraphs 12–13 cited — operative paragraphs are 
13–14.** Paragraph 13 of ISA 550 covers identification and disclosure 
inquiries; paragraph 14 covers nature of relationships and 
transactions. Paragraph 12 is the introduction to the section. Slight 
imprecision; self-flag was appropriate.

**4. ISA 315 (Revised 2019) paragraph 30 cited in Section 8 — 
operative paragraph for impact on substantive procedures is in ISA 
330, not ISA 315.** Paragraph 30 of ISA 315 (Revised) covers risk 
identification and assessment. The impact-on-substantive-procedures 
link sits in ISA 330 paragraphs 18–24 (responses to assessed risks). 
Citation is in the wrong standard.

**5. ISA 315 paragraphs 25–27 not self-flagged but range warrants 
verification.** The cited range (auditor's procedures to understand 
internal control) is approximately correct, but the exact paragraph 
numbers under ISA 315 (Revised 2019) should be verified against the 
IAASB Handbook. The standard was substantially restructured when 
revised in 2019.

**6. Missing variation orders and back-charges in Stage C.** 
Construction contracts almost always involve variation orders 
(changes to scope after the original contract) and back-charges 
(deductions for defects, delays, liquidated damages). These are 
high-judgement adjustments that the QS certifies and often contain 
disputes. v2 mentions back-charges in the Stage C inspection but 
does not include an explicit question about how variation orders 
are authorised before being included in progress claims.

**7. MFRS 137 paragraph numbers not cited in Section 7.** Given 
the discipline applied to ISA citations, MFRS 137 paragraph 14 
(general recognition criteria for provisions) or paragraphs 35–36 
(distinguishing provisions from contingent liabilities) could be 
cited where the boundary discussion appears.

**8. ISA 240 paragraphs 18 and 19 not addressed.** Paragraph 17 
covers inquiries of management. Paragraph 18 requires inquiries of 
those charged with governance, and paragraph 19 requires consideration 
of inquiring of others within the entity (internal audit, employees 
in different roles). A comprehensive ISA 240 fraud inquiry section 
would address all three inquiry levels. v2 is limited to management 
inquiries.

### What this teaches about AI verification on procedure design

This file demonstrates a fourth distinct AI failure-mode pattern, 
different from the patterns observed in the standards-summary, 
analytical-drafting, and memo-drafting files.

**For standards-summary tasks** (`isa-standard-summary.md`, 
`mfrs-comparison.md`): AI output is unreliable on technical specifics 
— paragraph numbers, version conflations, named documents. 
Verification requires authoritative source documents.

**For analytical-drafting tasks** (`ratio-commentary.md`, 
`variance-explanation.md`): AI output is reliable on structure and 
most substance when the prompt is well-specified, but reverts to 
general defaults wherever the prompt is silent.

**For memo drafting on contested judgements** (`memo-drafting.md`): 
AI output is structurally competent but defaults to pre-concluding 
contested issues unless the prompt explicitly frames the issue as 
contested.

**For procedure design** (this file): AI output is methodologically 
competent at producing process-area questions but defaults to inquiry 
form rather than walkthrough form. The shift from "asking about a 
process" to "observing a transaction" requires explicit prompt 
specification — without it, AI produces interview scripts.

A new observation specific to this file: **over-cautious self-flagging 
is itself a failure mode.** Claude flagged ISA 240 paragraph 17 and 
the Companies Act 2016 seven-year retention as uncertain when both 
were correct. This is less dangerous than under-flagging (which 
would assert incorrect references as fact), but it suggests the 
model lacks complete confidence in well-established references. For 
verification log purposes, over-cautious flags should be 
distinguished from genuinely uncertain references — both deserve 
verification, but the response differs (over-cautious flags get 
corrected to positive citations; genuinely uncertain flags get 
either verified or replaced).

### Recurring pattern to watch for

For procedure-design tasks (walkthroughs, audit programmes, control 
testing matrices), the prompt should explicitly:

- **Distinguish the audit procedure being designed from inquiry.** 
  A walkthrough is observation. A control test is re-performance or 
  inspection of evidence. An analytical procedure is comparison. 
  Each has different methodology. Without prompt specification, AI 
  defaults to inquiry form for all of them.
- **Require mapping to specific audit assertions.** Each procedure 
  should test one or more of: occurrence, completeness, accuracy, 
  cut-off, authorisation, classification, presentation. Without 
  assertion mapping, the procedure cannot be used to evaluate 
  control effectiveness or to support an audit opinion.
- **Require structured fraud and related-party inquiries** under 
  ISA 240 and ISA 550. AI defaults to general business risk framing; 
  the audit-specific framing must be explicit in the prompt.
- **Require IT general controls as a distinct section** when the 
  procedure involves a system. Modern AP, payroll, revenue, and 
  inventory processes are heavily IT-dependent. Without prompt 
  specification, AI tends to mention IT controls in passing rather 
  than treating them as a distinct testing area.
- **Distinguish the property-developer-specific elements** (or 
  industry-specific elements for any sector) as core control points, 
  not afterthoughts. AI tools default to generic procurement / 
  generic revenue / generic inventory frameworks unless industry 
  specificity is required by the prompt.
- **Always verify paragraph references**, including self-flagged 
  references that may have been over-cautious. Some flags will turn 
  out to be unnecessary (the citation was correct); others will 
  reveal genuine errors. Both are useful verification outputs.

A diagnostic prompt of this kind produces a walkthrough procedure 
that an audit senior could use to perform the walkthrough, rather 
than reframe from scratch. The verification step remains essential 
— for paragraph references especially — but the editing burden is 
much smaller than on a vague prompt.

---

## v1 output (for reference)

> Here's a practical set of walkthrough questions for your AP team 
> interview, organised by process stage:
>
> **Procurement Initiation**
> - Who is authorised to raise a purchase requisition (PR), and is 
>   there a system or manual form used? Walk me through how a PR 
>   gets created.
> - How does the system (or process) prevent a PR from being raised 
>   for a vendor not on the approved vendor list?
> - Who maintains the approved vendor list, and how often is it 
>   reviewed?
>
> [...full v1 output retained in repo for transparency. Key contested 
> elements include: interview-style framing throughout ("describe", 
> "walk me through how a PR gets created"); no observation procedures; 
> ISA 240 fraud risks reduced to closing paragraph; QS certification 
> mentioned only in closing afterthought; no ISA paragraph references; 
> no IT controls as distinct section; no conclusion framework.]

---

*Verification performed against IAASB Handbook 2023–2024 edition, 
MASB-issued MFRSs, and Companies Act 2016. The errors in v1 are 
characteristic of AI failure modes on procedure design when prompted 
vaguely. The corrections in v2 reflect the diagnostic value of 
well-designed prompts. Two of v2's self-flagged references were 
actually correct (ISA 240 paragraph 17; Companies Act 2016 
seven-year retention) — over-cautious flagging is itself a failure 
mode worth distinguishing from genuine uncertainty.*

*Last updated: 26/6/2026.*
