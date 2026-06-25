# Ratio Commentary

**Task:** Produce analytical-review commentary on financial ratios for 
inclusion in audit working papers under ISA 520. The commentary must 
read as audit working paper text (not investor narrative or business 
commentary), engage with specific MFRS standards and audit procedures, 
and distinguish observation from inference.

**Data used:** Selected FY24 and FY25 ratios from SkyWorld Development 
Berhad, the Bursa Malaysia–listed property developer used as the 
subject of my Power BI dashboard project. The same underlying numbers 
that drive the dashboard's Page 3 (Liquidity & Gearing) and Page 4 
(Risk Flags) commentary.

**Model used:** Claude (claude.ai), web interface.

**Verification approach:** Unlike the standards-summary files in 
`01-research/`, this file does not verify Claude against an external 
authoritative source. The verification source is my own knowledge of 
the dashboard data, the underlying SkyWorld financials, and the audit 
commentary I wrote for the dashboard. The discipline being tested 
here is whether Claude can produce audit-grade analytical commentary 
when prompted appropriately and where it falls short when not.

---

## Prompt v1 (rough)
Here are the financial ratios for a Malaysian property developer over
two years:
FY24: Revenue RM 688m, Gross margin 36.8%, DSO 118 days, DIO 158 days,
DPO 172 days, CCC 104 days, ROE 12.6%, ROA 6.3%, D/E 0.58, Interest
coverage 10.9x
FY25: Revenue RM 445m, Gross margin 37.1%, DSO 202 days, DIO 297 days,
DPO 251 days, CCC 248 days, ROE 6.4%, ROA 3.7%, D/E 0.51, Interest
coverage 6.8x
Write commentary on these for me.

## What v1 got wrong

The under-specified prompt produced output that read as plausible 
business commentary but was substantively wrong for audit working 
paper use. The full v1 output is reproduced at the end of this file. 
The key issues:

1. **Wrong voice and audience.** Output read as CEO briefing or equity 
   research note ("Where things get concerning," "What to watch going 
   forward") rather than audit working paper language. Working paper 
   analytical review uses procedural framing: *"The movement in [X] 
   requires substantive testing under [Y]."*

2. **No MFRS or ISA citations.** Every ratio movement should connect 
   to a specific accounting or auditing standard (MFRS 102 inventory, 
   MFRS 9 receivables ECL, MFRS 15 revenue, ISA 570 going concern, 
   ISA 520 analytical procedures itself). v1 produced business 
   commentary without audit framing.

3. **Fabricated causal narratives.** Specific causal stories were 
   invented from the ratio data alone: *"project delays pushing 
   revenue recognition into future periods,"* *"disputed handovers,"* 
   *"lumpy project completion schedule,"* *"penalty clauses on 
   payables."* These were not derivable from the ratios provided and 
   would not survive review by an audit senior.

4. **Omits a provided data point.** Net gearing (-0.01 → 0.11) was 
   provided in the prompt but not mentioned in v1's commentary. A 
   working paper that omits provided data reads as incomplete.

5. **Forward-looking speculation.** The closing paragraph speculated 
   about FY26 revenue rebound, liquidity pressure, and supplier 
   relationship strain. Working papers document current-period risk 
   assessment and audit response, not future operating scenarios.

6. **Overconfident risk judgements.** Phrases like *"Nothing 
   pathological here"* and *"comfortable in absolute terms"* asserted 
   conclusions a working paper would document with reference to 
   engagement materiality and management representations, not assert 
   as standalone judgements.

7. **Property-developer industry context applied inconsistently.** 
   Claude correctly noted that DIO needs property-developer framing 
   in one place but treated the movements as if in a manufacturing 
   context in others.

8. **No audit response.** A working paper analytical review identifies 
   risk areas *and* the audit response (substantive procedures planned, 
   evidence to obtain, management representations required). v1 
   identified issues but did not connect them to procedures.

---

## Prompt v2 (refined)
You are an ICAEW-qualified audit senior at a Big Four firm in Malaysia,
reviewing a draft analytical review section for a property developer
client's FY25 audit working papers. The client is listed on Bursa
Malaysia and reports under MFRS.
Below are key ratios for FY24 and FY25. Please write commentary
suitable for inclusion in the analytical review section of the audit
working papers, structured as follows:
Headline observations — the two or three most material
movements, in priority order, with one-sentence implications.
Working capital cycle commentary — what the DSO, DIO, DPO,
and CCC movements indicate, framed against expectations for a
Malaysian property developer where multi-year project cycles
normalise long DIO.
Audit risk areas requiring substantive testing — tied to
specific MFRS standards (MFRS 102 inventory, MFRS 9 receivables
ECL, MFRS 15 revenue) where the ratio movements indicate elevated
risk.
Movements requiring caution in interpretation — any ratio
where the YoY percentage change is misleading due to small-base
distortion or other measurement artefact, and how to frame the
movement honestly.
Going concern observation — a brief note on what the data
does and does not say about going concern under ISA 570.

Constraints:
Do not invent management decisions, strategic intent, market
conditions, or industry context not derivable from the ratios.
Use the property-developer industry framing throughout. Long DIO
is normal; the YoY change is the analytically interesting move.
Flag any inference (as opposed to direct observation) explicitly.
Length: roughly 500 words.

[ratio table provided]

## Example output (v2)

> **Analytical Review — Property Developer Client | FY25 Audit Working Papers**
>
> **1. Headline Observations**
>
> *Revenue contraction (RM 688m → RM 445m; -35.3%).* This is the 
> most material movement in the period. A decline of this magnitude 
> warrants scrutiny of MFRS 15 revenue recognition timing — 
> specifically whether the percentage-of-completion *[see verification log: terminology drift]* or point-in-time 
> criteria have been applied consistently, and whether any recognised 
> revenue should have been deferred.
>
> *Cash conversion cycle deterioration (104 → 248 days; +144 days).* 
> The combined lengthening of DSO and DIO, only partially offset by 
> extended DPO, signals a significant tightening of operating 
> liquidity.
>
> *Return compression (ROE 12.6% → 6.4%; ROA 6.3% → 3.7%).* Returns 
> have roughly halved, primarily driven by the revenue decline rather 
> than margin erosion (gross margin is broadly stable at ~37%). This 
> divergence — stable margins, falling returns — is consistent with 
> underutilised asset base or slowed project completions, though this 
> remains an inference.
>
> **2. Working Capital Cycle Commentary**
>
> For a Malaysian property developer, elevated DIO is structurally 
> normal given multi-year development cycles; the absolute level is 
> less analytically significant than the year-on-year movement. DIO 
> increasing from 158 to 297 days (+139 days) against a backdrop of 
> sharply lower revenue is notable. This pattern is consistent with 
> either slower project completion velocity or reduced delivery of 
> completed units — inference, not observation — and elevates the 
> risk of inventory carrying values becoming irrecoverable.
>
> DSO widening from 118 to 202 days (+84 days) is significant. DPO 
> extending from 172 to 251 days (+79 days) partially mirrors the 
> DSO movement and may indicate the client is managing cash by 
> deferring supplier and contractor payments — inference — which 
> itself introduces trade payable completeness risk.
>
> **3. Audit Risk Areas Requiring Substantive Testing**
>
> - *MFRS 102 — Inventory:* DIO of 297 days on lower revenue elevates 
>   net realisable value (NRV) risk. Substantive procedures should 
>   include independent NRV assessments for slow-moving or stalled 
>   development land and work-in-progress.
> - *MFRS 9 — Receivables ECL:* DSO of 202 days requires robust 
>   staging assessment. The audit team should challenge the ECL model 
>   assumptions, particularly forward-looking overlays, and 
>   independently assess whether any receivables should be moved to 
>   Stage 2 or Stage 3. *[see verification log: minor framing issue — auditor tests management's classification, does not "move" receivables]*
> - *MFRS 15 — Revenue recognition:* The revenue decline of 35.3% 
>   with stable gross margins warrants testing of the completeness 
>   and cut-off of contract revenue.
>
> **4. Movements Requiring Caution in Interpretation**
>
> *Net gearing (-0.01 → 0.11):* The absolute change is small, and 
> the percentage movement is arithmetically large due to the 
> near-zero base in FY24 (net cash position). This should not be 
> characterised as a dramatic leverage increase; in absolute terms, 
> net gearing of 0.11x remains low. The directional shift from net 
> cash to modest net debt is directionally relevant but should be 
> framed proportionately.
>
> *Debt-to-equity (0.58 → 0.51):* This improvement is directionally 
> positive but may partly reflect equity base effects rather than 
> active deleveraging.
>
> **5. Going Concern Observation**
>
> The data does not, on its face, indicate a going concern risk under 
> ISA 570. Debt-to-equity has improved, interest coverage — while 
> reduced — remains adequate at 6.8x, and there is no evidence of 
> covenant breach in the ratios presented. However, the CCC 
> deterioration to 248 days and the shift to a net gearing position 
> of 0.11x warrant specific going concern enquiries: the audit team 
> should obtain and review loan facility terms (including financial 
> covenants referencing interest coverage or gearing thresholds), 
> management's 12-month cash flow projections, and any refinancing 
> arrangements falling due within the look-forward period. The 
> absence of a red flag is not equivalent to a positive going concern 
> conclusion.

---

## Verification log

**Verified against:** My own analysis of the SkyWorld FY22–FY25 
financial data, the audit commentary I wrote for the Power BI 
dashboard project (Pages 3 and 4), and general knowledge of MFRS 102, 
MFRS 9, MFRS 15, ISA 570, and ISA 520 from ICAEW Professional Level 
study materials and the IAASB Handbook 2023–2024 edition.

### Improvements from v1 to v2

The refined prompt produced substantial improvements across every 
dimension v1 failed:

- **Voice corrected.** v2 reads as audit working paper text. 
  Procedural language throughout: *"requires substantive testing,"* 
  *"the audit team should challenge,"* *"obtain and review loan 
  facility terms."* v1's investor-narrative voice is gone.
- **MFRS and ISA framing engaged.** MFRS 102, MFRS 9, MFRS 15, and 
  ISA 570 are explicitly cited and tied to specific audit procedures. 
  v1 contained no standards references at all.
- **Inferences explicitly flagged.** Five separate instances of 
  *"inference, not observation"* or *"remains an inference"* in v2. 
  v1 stated speculation as if it were analysis.
- **Net gearing addressed correctly.** v1 omitted this data point 
  entirely. v2 dedicates a paragraph to it, correctly identifying 
  the small-base distortion and framing the movement as a level 
  shift (from net cash to modest net debt) rather than a misleading 
  percentage change. This was the most important failure mode of v1 
  and v2 resolved it cleanly.
- **No forward-looking speculation.** v2 contains no claims about 
  FY26 performance, future revenue, or future liquidity pressure. 
  v1 closed with a full paragraph of forward speculation.
- **Audit response identified for each risk area.** v2 connects 
  ratio movements to specific substantive procedures (NRV testing, 
  ECL staging review, revenue completeness and cut-off testing, 
  covenant review). v1 identified issues but did not state how to 
  audit them.
- **Property-developer industry framing consistent.** v2 opens the 
  working capital section by establishing that long DIO is 
  structurally normal for the industry, then frames the movement as 
  the analytically interesting variable. v1 was inconsistent on this.
- **Genuine added insight.** v2's *"trade payable completeness risk"* 
  observation in Section 2 is a sharp audit point that goes beyond 
  what the prompt required — extended DPO can mask unrecorded 
  liabilities. This is the kind of observation an experienced audit 
  senior would make.

### Errors v2 still made

These are minor and largely terminology- or framing-level rather 
than substantive.

**1. MFRS 15 terminology drift.** v2 refers to *"percentage-of-completion"* 
revenue recognition. Under MFRS 15 (effective in Malaysia 1 January 
2018, equivalent to IFRS 15), the standard's own terminology is 
*"over-time recognition"* with *"input methods"* or *"output methods"* 
for measuring progress. The older POC terminology comes from MFRS 111 
(Construction Contracts), which MFRS 15 superseded. The concepts are 
substantively identical and Malaysian practice still uses POC 
colloquially, so this is not a substantive error — but a pedantic 
reviewer would note the terminology drift.

**2. ECL staging framing — minor "who does what" issue.** v2 states 
*"independently assess whether any receivables should be moved to 
Stage 2 or Stage 3."* Under MFRS 9, management classifies receivables 
across the three stages; the auditor tests whether management's 
classification is appropriate. The framing in v2 implies the auditor 
"moves" receivables between stages, which slightly misrepresents the 
division of responsibility. Substantively the audit response is 
correct — challenge ECL model assumptions and assess staging — but 
the language should read *"independently assess whether management's 
staging classification is appropriate"* rather than *"whether any 
receivables should be moved."*

**3. No specific paragraph numbers cited.** The prompt did not require 
paragraph citations, so this is on the prompt design rather than 
Claude. For real working paper purposes, ideal citations would be 
MFRS 102 paragraph 9 (lower of cost and NRV), MFRS 9 paragraphs 
5.5.1–5.5.20 (ECL model), MFRS 15 paragraphs 31–38 (recognition 
criteria over time vs point in time), ISA 570 paragraphs 12–15 
(going concern procedures), and ISA 520 paragraph 5 (substantive 
analytical procedures requirements).

**4. No reference to ISA 520 itself.** The commentary v2 produced is, 
itself, an analytical procedure under ISA 520. A working paper would 
typically cross-reference the standard at the top of the working 
paper (*"Analytical procedures performed in accordance with ISA 520 
paragraph 5"*). v2 doesn't include this framing.

**5. Closing line slight redundancy.** *"The ratios alone are 
insufficient to conclude either way"* and *"the absence of a red flag 
is not equivalent to a positive going concern conclusion"* convey the 
same idea. Either line on its own would work; both together is mildly 
redundant. Minor.

### What this teaches about AI verification on analytical-drafting tasks

The verification pattern for analytical-drafting tasks (like this one) 
is meaningfully different from the verification pattern for 
standards-summary tasks (like the ISA 520 and MFRS comparison files 
in `01-research/`).

**For standards-summary tasks:** AI output is unreliable on technical 
specifics — paragraph numbers, version conflations, named documents. 
Verification requires authoritative source documents (the IAASB 
Handbook, the MASB-issued MFRSs). Errors are factual and verifiable 
against a primary source.

**For analytical-drafting tasks:** AI output is reliable on structure 
and most substance *when the prompt is well-specified*, but reverts 
to general defaults wherever the prompt is silent. Verification is 
largely about checking that the prompt's constraints were actually 
applied. Where the prompt specifies (audit voice, MFRS framing, 
inference flagging, small-base handling, going concern bounded), 
v2 delivered. Where the prompt is silent (paragraph citations, POC 
vs over-time terminology, ISA 520 self-reference), v2 produces 
generally accurate but non-specific output.

This means the verification effort shifts: less time checking facts 
against primary sources, more time stress-testing the prompt design 
itself.

### Recurring pattern to watch for

The single most important observation across this file is that **the 
quality of analytical-drafting output is bounded by the specificity 
of the prompt.** v1 (vague prompt) produced business commentary. v2 
(role-defined, audience-defined, structure-defined, constraint-listed) 
produced audit working paper commentary that an audit senior could 
edit and use, rather than rewrite from scratch.

For any future analytical-drafting prompt — variance explanations, 
trend descriptions, control walkthroughs, audit memos — the prompt 
should explicitly state:

- **Role:** Who is producing the output (ICAEW-qualified audit senior, 
  Big Four manager, etc.)
- **Audience:** Who the output is for (audit working papers, partner 
  review file, management letter)
- **Framework:** Which MFRS / ISA / industry standard applies
- **Output structure:** Specific sections in priority order
- **Inference discipline:** Explicit instruction to flag inference vs 
  observation
- **Bounded conclusions:** Where the output must not over-reach 
  (e.g., going concern conclusions, materiality judgements)

A well-prompted analytical-drafting task can produce output close to 
audit-grade. A poorly-prompted one will produce plausible-sounding 
investor narrative. The verification log's job is to make that 
distinction visible.

---

## v1 output (for reference)

> **Overall picture: a revenue contraction year with a working capital crisis**
>
> The headline story is a 35% revenue decline from RM 688m to RM 445m. 
> That kind of drop in a property developer typically points to fewer 
> completed handovers — either project delays pushing revenue 
> recognition into future periods, or genuine sales softness.
>
> [...full v1 output retained in repo for transparency...]

---

*Verification performed against my own analysis of the SkyWorld 
financial data and the audit commentary written for the dashboard 
project. Errors identified here are characteristic of AI failure 
modes when prompted vaguely for analytical drafting; the specific 
errors will differ across model versions and tasks, but the 
prompt-discipline pattern does not.*

*Last updated: 25/6/2026.*
