# Verification-First AI for Appellate Practice

I'm a Texas appellate attorney building and testing AI workflows for high-stakes legal writing — a domain where a hallucinated citation is not a quirk but a sanctionable event.

Everything in this repository was built on my own dime, outside billable hours, and is free to copy, adapt, and use. No attribution required.

## Current work

**Verity — the citation-verification pipeline** (skill slug: `cite-check`). A multi-round process for auditing AI-assisted filings against ground-truth judicial opinions. Round 1 catches nonexistent cases. Round 2 verifies every quotation against the actual opinion. Round 3 checks parentheticals and characterizations of holdings. Designed to run on a real brief in minutes, with a human-approval gate between rounds.

**Benchmarked prompt library.** Reusable, genericized prompts for appellate workflows — record analysis, issue-spotting, outline building, drafting — each documented with where the model is reliable and where it fails.

**CLE curriculum (in development).** Converting these findings into accredited continuing legal education, so the work scales from one practice to the profession.

## What's in here

| Prompt | What it's for |
|---|---|
| [The Legislation Drafter](legislation-drafter.md) | Article V for laypeople. Turns a problem someone already understands into a properly formed bill, a plain-English vet memo, and a list of questions for a lawyer. Never gives legal advice. |
| [Motion for Rehearing → Petition for Review](petition-for-review.md) | Converting error-correction into review-worthiness. A conversion table maps each rehearing argument to a review-granting factor — or recommends dropping it — before a word of the petition is drafted. |
| [Oral Argument Preparation](oral-argument-prep.md) | A paired set: a comprehensive moot question bank weighted to financial exposure and aimed at your own side's weak points, and a short visual podium primer condensed from it — so the advocate and the moot panel are working from the same answers. |
| [Reporting Harassment at Work](harassment-report.md) | Builds the dated log and the report, in your own words. Distinguishes *I don't remember* from *I remember and there's no paper* — because those are opposite facts and only one of them is a weakness. Pause anytime; the record keeps your place. |
| [The College Application Keeper](college-applications.md) | For a student applying without a counselor, a parent who has done it before, or money for either. Most of what a private counselor does is bookkeeping — deadlines, fee waivers, aid forms, and a record of what you have actually done. That part can be given away. |
| [The Steady Companion](steady-companion.md) | Guardrails for AI in mental-health conversations — a standing prompt you write on a calm day, so the model meets you instead of managing you, and keeps your care team in the room instead of replacing them. |
| [The Genie Lamp](genie-lamp.md) | A starter kit for persistent memory. A model has no memory between sessions, so the state lives in files you re-inject at the top of each one. Includes the folder, the starting contents of every file, and the setup prompt. |
| [The Beginner Explorer's Pack](explorers-pack.md) | A starter continuity kit for anyone new to working with an AI across more than one session. Installs three habits — a ledger, versioned autosaves, and a handoff — so the work doesn't vanish when the session ends. |
| [The Prompt-Library Keeper](prompt-library-keeper.md) | The meta-prompt. Turns any good working prompt into a durable library entry and keeps the library consistent as it grows. Chat logs are disposable; the library is the real memory. |
| ["I Play Better When I'm Drunk"](state-dependent-memory.md) | State-dependent memory for AI-assisted work. A one-page grip card that reconstructs *how* a long document was made before asking you to defend what it says. |
| [My Genie Is Not White](my-genie-is-not-white.md) | A standing frame-check and lessons ledger for builder-default bias — the defaults of whoever built a system becoming invisible walls inside it. |

## Approach

Verification before launch. I come from a family of systems-builders (Aegis, mathematical modeling); this is the language version of that discipline. The question isn't whether lawyers will use AI — it's whether they'll use it with guardrails or without.

*First prompt: January 2026. This repository documents what came after.*
