# MFRS vs IFRS Comparison

**Task:** Produce a structured comparison of three Malaysian Financial 
Reporting Standards (MFRS) with their IFRS equivalents, at the level 
needed by an ICAEW Professional Level candidate joining a Big Four 
audit team in Malaysia. The comparison focuses on standards relevant 
to a property developer audit (the sector context of my SkyWorld 
dashboard project).

**Standards used:** MFRS 9 / IFRS 9 (Financial Instruments), 
MFRS 15 / IFRS 15 (Revenue from Contracts with Customers), and 
MFRS 102 / IAS 2 (Inventories).

**Model used:** Claude (claude.ai), web interface.

**Verification sources:**
- MASB-issued PDFs of MFRS 9, MFRS 15, MFRS 102 (downloaded from 
  masb.org.my)
- IFRS Foundation text of IFRS 9, IFRS 15, IAS 2
- IAASB Handbook 2023–2024 (for ISA cross-references)
- Direct verification against masb.org.my for any claimed MASB-issued 
  documents

---

## Prompt v1 (rough)
What's the difference between MFRS and IFRS? I need to understand
for audit work in Malaysia.

## What v1 got wrong

A short, vague prompt produced an apparently confident overview with 
multiple substantive errors. The output is reproduced at the end of 
this file for reference. The key issues:

1. **Fabricated framework — "MFRS for SMEs."** v1 lists "MFRS for SMEs" 
   as a separate Malaysian framework, distinct from both MFRS and MPERS. 
   No such standard exists. Malaysia operates two parallel frameworks: 
   MFRS (for non-private entities) and MPERS (Malaysian Private Entities 
   Reporting Standard, based on IFRS for SMEs). Treating these as three 
   frameworks rather than two is a fundamental factual error.

2. **PERS / MPERS confusion.** v1 refers to "PERS (Private Entity 
   Reporting Standards)" as a current alternative for smaller private 
   companies. PERS was withdrawn effective 1 January 2016 and replaced 
   by MPERS. An auditor citing PERS for a current engagement would be 
   citing a framework no longer in force.

3. **Bearer plants framed as a Malaysian carve-out.** v1 states that 
   Malaysia carved out bearer plants from the fair value model under 
   MFRS 141, allowing them to be accounted for under MFRS 116. This 
   misrepresents history. The IASB itself amended IAS 41 and IAS 16 in 
   June 2014 to remove bearer plants from IAS 41's fair-value scope and 
   permit the cost model under IAS 16. This was a global IFRS amendment 
   adopted in Malaysia, not a Malaysian deviation from IFRS.

4. **Deferred adoption mis-identified.** v1 gestures at "financial 
   institutions under BNM oversight" as the example of deferred adoption 
   in Malaysia. The more notable Malaysian-specific deferral was for 
   Transitioning Entities (TEs) in property development and agriculture, 
   allowed to apply FRS rather than MFRS until 1 January 2018. v1 missed 
   this entirely while invoking a less relevant example.

5. **No paragraph numbers cited anywhere.** No claim in v1 can be 
   verified against a specific source paragraph. Same v1 weakness as 
   in the ISA 520 file.

6. **No specific comparison of MFRS 9, MFRS 15, or MFRS 102.** v1 
   produced a general framework overview rather than the standard-by-
   standard comparison the audit-practitioner question requires.

7. **Misses MFRS 1 (First-time Adoption) as the genuine technical 
   distinction.** The MFRS Preface in every Malaysian standard explicitly 
   states that effective and issuance dates inside individual MFRSs are 
   inapplicable in the MFRS framework because MFRS 1 governs transition. 
   This is the substantive Malaysian-specific structural feature; v1 
   doesn't mention it.

---

## Prompt v2 (refined)
You are an ICAEW-qualified audit senior advising a junior auditor
starting work in Malaysia on a multinational engagement. The junior
needs to understand how MFRS (Malaysian Financial Reporting Standards)
relates to IFRS, specifically for three standards relevant to a
property developer audit: MFRS 9 / IFRS 9, MFRS 15 / IFRS 15, and
MFRS 102 / IAS 2.
Produce a structured comparison with the following sections:
Framework overview — the relationship between MFRS and IFRS, the
role of the Malaysian Accounting Standards Board (MASB), and the
distinction between MFRS (for entities other than private entities)
and MPERS (Malaysian Private Entities Reporting Standard).
Standard-by-standard comparison (for each of MFRS 9, MFRS 15, and

MFRS 102):
The IFRS equivalent
Effective date in Malaysia vs IFRS effective date
Whether the MFRS text is identical, substantively equivalent,
or contains specific Malaysian modifications
Any specific Malaysian transitional provisions or local
implementation guidance worth noting

Practical audit implications — how the MFRS / IFRS relationship
affects audit documentation, particularly for multinational groups
where Malaysian subsidiaries report to an IFRS-based parent.

Constraints:
Cite specific MFRS / IFRS paragraph numbers where you make
substantive claims. If you are not certain, flag the reference
as "[to verify]".
Do not invent differences between MFRS and IFRS that do not exist.
If the standards are substantively identical, state that clearly.
Distinguish MFRS (private-non-private entities under MASB framework)
from MPERS (Malaysian Private Entities Reporting Standard).
Length: roughly 700 words total.

After producing the comparison, list any specific points where you
are uncertain of the exact text or paragraph number, so I can verify
against the MASB and IFRS Foundation sources.

## Example output (v2)

> **MFRS vs IFRS: Comparison for Property Developer Audit (Malaysia)**
>
> **1. Framework Overview**
> The Malaysian Accounting Standards Board (MASB) issues two parallel 
> frameworks. MFRS applies to all entities except private entities as 
> defined under the Companies Act 2016 *[see verification log: legal source partially mis-attributed]* — this includes listed 
> companies, financial institutions, and subsidiaries of foreign 
> multinationals. MPERS (Malaysian Private Entities Reporting Standard) 
> is a self-contained framework for qualifying private entities, broadly 
> analogous to the IFRS for SMEs standard but with Malaysian adaptations.
>
> MFRS is a word-for-word adoption of IFRS as issued by the IASB, with 
> effective dates that typically mirror the IASB's dates. MASB does not 
> ordinarily modify the substantive technical content of IFRS when 
> transposing it into MFRS — the numbering changes (IAS → MFRS, IFRS → 
> MFRS) but the paragraphs are reproduced verbatim. *[see verification log: misses MFRS 1 transition feature]*
>
> **2. Standard-by-Standard Comparison**
>
> *MFRS 9 / IFRS 9 — Financial Instruments*
> - IFRS equivalent: IFRS 9 (IASB effective 1 January 2018).
> - Malaysia effective date: 1 January 2018 — aligned with IASB.
> - Substantive differences: None. MFRS 9 reproduces IFRS 9 verbatim.
> - ECL model: IFRS 9 paragraphs 5.5.1–5.5.20 *[to verify]*; simplified 
>   approach for trade receivables at paragraph 5.5.15 *[to verify]*.
> - Transitional provisions: same relief as IASB, including the option 
>   not to restate comparatives (IFRS 9 paragraph 7.2.15) *[to verify]*.
>
> *MFRS 15 / IFRS 15 — Revenue from Contracts with Customers*
> - IFRS equivalent: IFRS 15 (IASB effective 1 January 2018).
> - Malaysia effective date: 1 January 2018 — aligned with IASB.
> - Substantive differences: None in the core standard text.
> - **MASB issued a non-mandatory Guidance Note addressing the application 
>   of MFRS 15 to property developers under the Malaysian Housing 
>   Development (Control and Licensing) Act 1966 (HDA).** *[see verification log: existence of this named document requires direct verification on masb.org.my]*
> - Key audit issue: over-time vs point-in-time recognition for SPA 
>   units under HDA — paragraphs 35–37 vs paragraph 38, with paragraph 
>   35(c) frequently the operative test.
>
> *MFRS 102 / IAS 2 — Inventories*
> - IFRS equivalent: IAS 2 (IASB effective 1 January 2005, no subsequent 
>   amendments affecting core measurement).
> - Malaysia effective date: MFRS 102 effective 1 January 2012 (on MFRS 
>   framework adoption) *[to verify]*.
> - Substantive differences: None. LIFO prohibition (paragraph 25), 
>   NRV requirement (paragraph 28), and cost formula rules all reproduced 
>   verbatim.
>
> **3. Practical Audit Implications**
> Because MFRS is word-for-word IFRS, group instructions from an 
> IFRS-based parent will generally be directly applicable to a Malaysian 
> subsidiary without translation adjustments. The auditor's documentation 
> obligation is to evidence that the MASB-issued version of the standard 
> was applied — not simply the IASB text — because MASB controls effective 
> dates and may issue transitional amendments on a different timetable.
>
> For property developer audits, the most significant documentation 
> burden arises under MFRS 15: the over-time versus point-in-time 
> determination requires detailed contract analysis, legal assessment 
> of HDA enforceability, and robust management judgement documentation.
>
> **Uncertainties self-flagged by Claude:**
> - MFRS 9 transitional guidance
> - MFRS 102 operative date
> - MASB Guidance Note on MFRS 15 — current status and precise title
> - Any MASB amendments post-2023

---

## Verification log

**Verified against:** MASB-issued PDFs of MFRS 9, MFRS 15, MFRS 102 
downloaded from masb.org.my; IFRS Foundation versions of IFRS 9, 
IFRS 15, IAS 2; direct search of masb.org.my for the claimed Guidance 
Note on MFRS 15.

### Improvements from v1 to v2

The refined prompt produced meaningful improvements:

- **Framework distinction corrected.** v1 fabricated "MFRS for SMEs" 
  as a separate framework and used the withdrawn "PERS" terminology. 
  v2 correctly identifies the two-framework structure: MFRS (non-private 
  entities) and MPERS (private entities, based on IFRS for SMEs).
- **Standard-by-standard structure delivered.** v1 produced a general 
  framework overview. v2 addressed each of MFRS 9, MFRS 15, and MFRS 102 
  individually with effective dates, equivalence statements, and 
  property-developer-specific application notes.
- **Bearer plants error not repeated.** v1 wrongly framed bearer plants 
  as a Malaysian carve-out from IFRS. v2 omits the topic, which is the 
  correct treatment given that bearer plants relate to MFRS 141 / IAS 41 
  and are not in scope of the three standards under comparison.
- **Paragraph references attempted.** v1 cited no paragraphs. v2 cites 
  specific paragraphs (5.5.15, 7.2.15, 25, 28, 35–37, 38) and self-flags 
  most of them as "[to verify]" — exactly the behaviour the prompt asked 
  for.
- **Self-flagged uncertainties at the end** with specific actionable 
  verification items.

### Errors v2 still made

Three categories of error remain, each requiring different verification 
discipline.

**1. Wrong legal source for MPERS scope.** v2 states "private entities 
as defined under the Companies Act 2016." The Companies Act 2016 
governs company classification generally, including the definition of 
a "private company." However, the framework authority for MPERS sits 
under the Financial Reporting Act 1997, which establishes MASB's 
standard-setting mandate. MPERS itself defines the eligibility 
criteria for the framework. The Companies Act 2016 is one input, but 
v2 attributes the framework scope to the wrong primary legal source.

**2. Misses the genuine MFRS-specific technical feature.** The Preface 
in every MFRS document (verified in MFRS 9, MFRS 15, and MFRS 102) 
explicitly states:

> *"In this regard the effective and issuance dates contained in this 
> Standard are those of the IASB's and are inapplicable in the MFRS 
> framework since MFRS 1 requirements will be applied by the first-time 
> adopter."*

This is the one substantive technical distinction between MFRS and 
IFRS at the framework level. MFRS 1 (First-time Adoption of Malaysian 
Financial Reporting Standards), the Malaysian equivalent of IFRS 1, 
governs how an entity transitions into the MFRS framework — and 
overrides the individual transition provisions inside other MFRSs. 
v2 doesn't mention MFRS 1 at all.

**3. Unverified named document — "MASB Guidance Note on MFRS 15 for 
property developers."** v2 states with specificity that MASB issued a 
non-mandatory Guidance Note addressing MFRS 15 application to property 
developers under the HDA.

[*Direct verification: insert what you found when you searched masb.org.my. 
Possible outcomes:*]

[*Outcome A — if the document exists:*]
A direct search of masb.org.my located the document, titled 
"[exact title]", issued [date]. v2's characterisation is broadly 
accurate, though [any specific corrections].

[*Outcome B — if the document does not exist:*]
A direct search of masb.org.my did not surface a document by this 
name. The underlying technical issue (HDA SPAs and over-time vs 
point-in-time recognition under MFRS 15) is well-established in 
Malaysian audit practice and has been addressed by Big Four firms 
and by the Malaysian Institute of Accountants, but no formal 
MASB-issued Guidance Note was located. This claim could not be 
verified and should not be relied upon.

[*Outcome C — if you find related but differently-titled MASB material:*]
A direct search of masb.org.my located [exact title of related 
document]. This is [type of document — e.g., FAQ, illustrative 
example, discussion paper] rather than a formal Guidance Note. v2's 
characterisation overstates the formality of the MASB pronouncement.

**4. Paragraph reference precision.** Several paragraph references 
were stated specifically (IFRS 9 paragraphs 5.5.1–5.5.20 for ECL; 
5.5.15 for simplified approach; 7.2.15 for transition relief). Where 
self-flagged as "[to verify]" the prompt instruction worked. The 
paragraph numbers are broadly correct as ranges. Specific point 
references (5.5.15, 7.2.15) should be verified against the IFRS 9 
text before being relied upon in working papers.

### What this teaches about AI verification on technical standards

Three distinct AI failure modes appeared in v2, each requiring a 
different verification habit:

**1. Plausible legal misattribution.** The Companies Act 2016 vs 
Financial Reporting Act 1997 issue is the kind of error where the 
output cites a real, related statute but the *specific* attribution 
is wrong. Only verifiable by reading the underlying statutes or 
checking MASB's own framework documentation. AI tools are particularly 
prone to this when multiple plausible legal sources exist for the 
same domain.

**2. Coherent omission.** The MFRS 1 transition feature is the most 
technically distinctive aspect of the MFRS framework, and v2 omits it 
entirely. The output reads complete because the framework overview 
section is coherent without it — but a working paper drafted from v2 
would miss the genuine technical distinction. Coherent omissions are 
the hardest category of AI error to catch because they leave no 
visible gap.

**3. Specific named document of uncertain existence.** The "MASB 
Guidance Note on MFRS 15 for property developers" is the most 
dangerous individual claim in v2. It names a specific document, 
characterises its status (non-mandatory), describes its content (HDA 
application), and embeds it in audit-practice commentary that reads 
authoritative. Citing such a document in a working paper without 
direct verification creates documentation risk: if the document does 
not exist, or has a different name, or has different status, the 
working paper is incorrect on a verifiable point.

### Recurring pattern to watch for

Across v1 and v2, the pattern is that AI output on Malaysian-specific 
audit topics is most reliable when it stays at the general framework 
level ("MFRS is word-for-word IFRS") and least reliable when it 
ventures into specific Malaysian-authored documents, statutory 
references, or named guidance. The verification step should focus 
heaviest scrutiny on:

- Named MASB-issued documents (Guidance Notes, Implementation Notes, 
  FAQs) — search directly on masb.org.my
- Specific statutory references (Companies Act 2016 vs Financial 
  Reporting Act 1997 vs MASB's own scoping) — verify against the 
  actual statute or the MASB framework documentation
- The MFRS 1 transition feature — confirm it appears in the Preface 
  of the specific MFRS in question

For any future prompt comparing Malaysian-specific frameworks or 
guidance to international standards, an explicit instruction should 
be added to the prompt: *"Do not name specific MASB-issued documents 
unless you can quote the exact title; if you can only describe a 
document's content but not its title, flag the existence of the 
document itself as '[to verify]'."*

---

## v1 output (for reference)

> MFRS (Malaysian Financial Reporting Standards) and IFRS (International 
> Financial Reporting Standards) are closely related — here's what you 
> need to know for audit work in Malaysia.
>
> [...full v1 output retained in repo for transparency...]

---

*Verification performed against MASB-issued PDFs of MFRS 9, MFRS 15, 
MFRS 102 (downloaded from masb.org.my, 2023–2024 editions); IFRS 
Foundation versions of IFRS 9, IFRS 15, IAS 2; and direct search of 
masb.org.my. Errors identified here are characteristic of AI failure 
modes when summarising frameworks with both international and 
jurisdiction-specific layers; the specific errors will differ across 
model versions and dates, but the verification discipline does not.*

*Last updated: 25/6/2026.*
