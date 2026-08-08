# Oral Argument Preparation

*Two prompts that work as a pair: a comprehensive moot question bank for the team running the moots, and a short visual primer for the person who actually stands at the podium. Stripped of case-specific facts and free to use.*

The pairing is the point. The question bank is built first and vetted; the primer is **condensed from it, never re-derived** — otherwise the advocate is prepped against different answers than the moot panel is using.

**Placeholders** appear as `[NOUN CATEGORY — explanation of its function]`. Replace the whole bracket, including the explanation.

**Setup that makes both prompts work better.** Put text-extractable versions of every document in the folder — native .docx or text-layer PDFs, not bare scans. Include the trial court's decision document, not just the briefs; the deference and findings questions depend on it. And expect the assistant to ask what is missing before it starts — that check is built into the prompts on purpose.

---

## Prompt 1 — Moot Question Bank

*Roughly 40 questions with proposed answers, pivots, and record cites, for the attorneys running the moots. Weighted to financial exposure and pointed at the weaknesses of your own side's briefing — the questions a hot bench would actually ask.*

```
Using the briefs, the trial court's [DECISION DOCUMENT — findings of fact and
conclusions of law, memorandum opinion, or final judgment] and the [GOVERNING
AGREEMENT — the contract whose provisions are disputed on appeal] in this folder,
develop a list of questions for oral argument moots, focusing most on the weak
points of the briefing filed for [CLIENT PARTY — the party our firm represents],
not the opponent's weak points.

Weight the number of questions to the potential financial award at issue: the
greatest number of questions should relate to [HIGHEST-VALUE ISSUE — the largest
monetary component, e.g., affirming or reversing the principal damages award], and
fewer questions on [LOWER-VALUE ISSUES — secondary claims, e.g., fee awards,
escrow/holdback disputes, or cross-appeal theories with contingent upside].

Keep the [PRIMARY POSTURE — e.g., appellee/response] points separate from the
[SECONDARY POSTURE — e.g., cross-appellant] points. Include a third section with
potential traps for inconsistent answers between the two sides of our combined
position — places where an answer defending [FAVORABLE RULING BELOW] could
contradict an answer attacking [ADVERSE RULING BELOW], including standard-of-review
whiplash, notice or preservation positions that cut both ways, damages-model
characterizations that shift between theories, and knowledge or reliance positions
applied asymmetrically to the parties.

For every question, include a proposed answer and, where the honest answer is
uncomfortable, a pivot line to safer ground. Every answer must carry record
citations in the briefs' own citation convention.

Also include: (a) a one-page table of key record touchstones — the ten or so
citations the advocate must know cold, with a one-line explanation of why each
matters; and (b) a pre-moot verification checklist identifying every record cite or
exhibit-admission status that a proposed answer depends on, so the team can confirm
them before the first moot.

Before starting to build the document, tell me whether you need any other portions
of the record or cases downloaded from [RESEARCH SERVICE — e.g., Westlaw]. Both PDF
and .docx versions of each file are in the folder; use the extracted text wherever
that is more token-efficient. Estimate the total reading cost and ask my approval
before any large read.

Format: Word document.
```

### Guardrails — behaviours to demand if they don't happen automatically

1. **Missing-document check first.** The assistant should inventory the folder against the prompt's list and flag gaps — most commonly the trial court's decision document — before reading anything at length.
2. **Cost approval before the big read.** A full brief set runs 150K–250K+ words. Require an estimate, a full-plan option, and a leaner alternative, and choose deliberately.
3. **Extraction integrity.** Scanned documents converted to .docx can silently lose most of their text. Have the assistant compare extracted word count against page count (roughly 300–450 words per brief page); if the ratio is far off, use the text-layer PDF or OCR instead. *This caught a findings document that had extracted at one-quarter of its true length.*
4. **Read the opponent's framing directly.** Analyse the opposing briefs themselves — not your own response brief's characterisation of them. The panel will have read the originals.
5. **Separate analyses, then compare.** Analyse the response-side briefing and the cross-appeal briefing in separate passes and only then look for contradictions — the consistency traps emerge from the comparison, not from either pass alone.
6. **Candour requirement.** Instruct the assistant to flag your own side's concessions, thin spots, arguments raised too late, miscites, and typos — the point is to hear them in the moot, not at the podium.
7. **No invented record.** Anything the assistant could not verify against the source documents goes on the verification checklist, not silently into an answer.

### Style points for the deliverable

Number questions continuously; group by issue with the money at stake in each section heading's orbit. Preservation and waiver exposure noted on both sides. Fallback positions — remittitur, limited remand, severable modification — stated explicitly so the advocate never concedes more than the fallback. Work-product legend on every page. Close the document with the question-count arithmetic showing the weighting matches the financial stakes; it keeps the drafting honest.

---

## Prompt 2 — Podium Primer

*A short, visual companion for the person standing up — typically a supervising partner who reviewed everything at filing and has a general memory of the case but is far from in the weeds. One sitting to read. Run it after Prompt 1 so the two documents cross-reference.*

```
Now create a much simpler starter version for [ARGUING ADVOCATE — the person who
will stand at the podium, e.g., the supervising partner]. [He/She] reviewed
everything before filing and has a general memory of the facts and arguments but is
far from in the weeds. Do not overwhelm.

Build it from short graphic modules rather than prose:

  (1) the story in ninety seconds — deal, unravelling, dispute, judgment, in four
      short paragraphs;
  (2) a colour-coded scoreboard table of every claim and its result below (green
      for rulings we defend, red for rulings we attack) with a column showing who
      appeals each;
  (3) a money table listing each dollar figure at stake and where it lives on
      appeal, with a one-line priority statement;
  (4) a cast-of-characters table — every witness or actor the panel might name, and
      why each matters, including which testimony cuts both ways;
  (5) the [NUMBER — about six] findings or holdings to know verbatim, quoted
      exactly, colour-coded by whether they help or hurt;
  (6) the [NUMBER — about twelve] questions most likely to be asked, each with a
      podium-length answer of two to four sentences, colour-keyed by stakes — no
      long pivots, those live in the companion document;
  (7) three theme lines that work across both halves of the case, each with a
      one-line note on when to deploy it; and
  (8) a Do/Don't table covering vocabulary discipline, graceful concessions, and
      record passages the panel may read aloud.

Pull the questions and answers from the comprehensive question bank already
prepared — condensed, not re-derived. Note in the primer that the long-form versions
with record cites live in the companion document, which the team will use to run the
moots.

Format: Word document, roughly [LENGTH — six to eight] pages.
```

### Guardrails

1. **Derivative, not independent.** The primer condenses the vetted question bank. If the primer is drafted from scratch, the two documents will drift and the advocate will be prepped against different answers than the moot panel is using.
2. **Podium answers only.** Two to four sentences per answer. If an answer needs a record cite recited from memory, it belongs in the question bank, not the primer.
3. **Vocabulary discipline travels.** Any banned-word or required-phrase rules from the question bank — for example, a damages vocabulary that must not echo a losing theory — must appear in the primer's Do/Don't table. The advocate reads only this document.
4. **Bad facts included.** The findings module must include the findings that hurt, with the reconciling answer cross-referenced. **A primer of only good news prepares no one.**

### Style points

Tables and colour over prose; a consistent colour key throughout (green = ours/high stakes, red = theirs/cross-appeal, amber = middle issues). Verbatim quotes only in the findings module — everywhere else, plain English. The three theme lines should each do double duty across the response and cross-appeal, so any question can land on one of them. Work-product legend on every page.

---

*Part of a larger appellate prompt library. Free to copy and adapt; no attribution required.*
