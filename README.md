# Audit AI Prompts — A Working Library

A practical reference of prompts for using AI tools (primarily Claude) 
in external audit work. Built from my own experience as an ICAEW 
Professional Level candidate preparing to join a Big Four audit team.

This is not a list of "10 ChatGPT prompts every accountant needs." 
It's a working log of prompts I've refined, with the rough drafts that 
didn't work, the standards I had to check against, and the cases where 
the AI confidently produced something that was simply wrong.

## Why this exists

Big Four audit firms have invested billions in AI tooling, for e instance, PwC's GL.ai, 
KPMG's Clara, EY's Helix, Deloitte's Omnia and Zora. By the time I start 
as an associate, AI-assisted documentation and research will be normal 
audit infrastructure, not a novelty.

The risk is not that audit associates won't use AI. The risk is that 
they'll use it badly by accepting plausible-sounding outputs that 
misquote standards, fabricate paragraph numbers, or apply the wrong 
framework. ISAs and IFRSs are technical, version-sensitive, and 
unforgiving. An AI tool that gets ISA 315 (Revised 2019) confused 
with the prior version creates documentation risk for the firm.

This repository is my attempt to develop and document a disciplined 
way of working with AI on audit tasks.

## The framework

Every prompt in this repository follows the same five-part structure:

**1. Role** — Tell the model who it should respond as. "You are an 
ICAEW-qualified audit senior reviewing a junior's work" produces 
different output than "explain this to me."

**2. Context** — Give the specific situation. Industry, standard, 
materiality, what the engagement team is trying to achieve.

**3. Examples** — Where possible, show the model the format and 
depth expected. One good example beats three paragraphs of 
instruction.

**4. Output format** — Specify the structure. "Output as a 
working-paper memo with sections for purpose, procedures performed, 
results, conclusion." Vague instructions produce vague outputs.

**5. Verification step** — The most important. Every AI output is 
treated as a first draft requiring verification against primary 
sources (the standard itself, the annual report, the working paper 
binder). I document what I had to verify, and what the model got wrong.

## What's in this repository

- **01-research/** — Prompts for understanding standards, comparing 
  frameworks, and researching industry-specific audit risks.
- **02-analytical-review/** — Prompts for ISA 520 analytical procedures: 
  ratio commentary, variance explanations, trend analysis.
- **03-working-papers/** — Prompts for drafting documentation: memos, 
  walkthrough narratives, sampling rationale.
- **04-control-testing/** — Prompts for designing walkthrough 
  questions and writing up control deficiencies.

Each folder contains a README explaining its scope and individual 
prompt files structured as: the task, the prompt (v1 and refined v2), 
example output, and a verification log.

## What the AI gets wrong (and why I track it)

Documenting failures matters more than documenting successes. A 
selection of recurring issues I've logged:

- Citing ISA paragraph numbers that don't exist
- Conflating MFRS (Malaysian) with IFRS where small differences exist
- Applying ISA 315 pre-revision concepts to post-2019 audits
- Suggesting analytical thresholds that don't reflect engagement 
  materiality
- Producing memos in IAS-era language for an entity that reports under IFRS

The verification logs in each prompt file flag these so future use 
of the same prompt is faster and safer.

## About

Built by Gan Kai Li, ICAEW Professional Level candidate, incoming 
Big Four audit associate. Companion piece to my audit analytics 
portfolio: [https://github.com/gankaili88/skyworld-financial-ratios-dashboard]

This is a portfolio piece for personal CPD purposes and does not 
represent the views or methodology of any audit firm. The prompts 
here have not been used on real audit engagements.
