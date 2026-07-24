# "I Play Better When I'm Drunk": State-Dependent Memory for AI-Assisted Work

*A one-page grip card for the author of any long AI-assisted document — and the theory behind why the card is built the way it is.*

The premise: your memory of an AI-assisted document lives in the **prompts**, because the prompts were your generative acts. Replaying them is a retrieval key that unzips your memory of the whole document. So the card reconstructs *how the document was made* (the code you authored) **before** *what it contains* — because the making is the part you actually encoded.

Three findings converge on this. The **generation effect**: you remember what you produce far better than what you merely read. **Encoding specificity** (Tulving): a cue works to the degree it matches the conditions present when you learned. **State-dependent memory** (Goodwin — whence the title): what you learn in a given state you recall best back in that state, and the prompt layer is the state this document was written in. A 2025 study (Kosmyna et al., "Your Brain on ChatGPT") found authors of AI-assisted essays couldn't quote their own work — but it never tested memory for their *prompts*, the one part the authors actually generated.

## The prompt

> You have just completed [DELIVERABLE — the long document produced in this session, named so you summarize that document and nothing else]. Produce a ONE-PAGE cheat sheet for me, its author, with exactly these five sections, in this order:
>
> **1. What this is** — one sentence: document, posture, audience.
> **2. How it was made (the code)** — reconstruct my instruction history in order: what I asked for at each stage, the constraints I imposed, what I rejected or made you revise, and which judgment calls were mine versus defaults of yours that I accepted. Use my own phrasing from the session wherever possible — recognition is the memory hook. This section is about MY authorship, not your process.
> **3. What it contains** — a compressed map of the deliverable: each section and its core proposition in one line.
> **4. Load-bearing points** — the [SMALL NUMBER — how many keystone items to surface, typically 3–5] citations, facts, or moves the document cannot survive without.
> **5. Open flags** — anything unverified, assumed, or deferred, stated as a checklist.
>
> Hard rules: one page maximum. Nothing appears that is not in the deliverable or in this session's actual history — no smoothing, no invented rationale for choices I didn't make. Where you cannot reconstruct why something was done, write "not decided in session" rather than supplying a reason.

## Guardrails

1. **The code section is mandatory and comes before the contents.** The generation effect says you encode what you produce; encoding specificity says a cue works to the degree it matches the conditions at encoding. The prompt history IS the encoding conditions, written down — replay it first and the rest of the document should unzip.
2. **No retroactive rationalization.** An invented reason for a choice is a fabricated record of your own thinking. Unexplained choices are logged as "not decided in session," never smoothed over.
3. **One page is a cap, not a target.** A two-page sheet is a summary; one page forces the keystone discipline that makes the card usable under pressure.
4. **Run it in-session.** Chat logs are ephemeral and the prompt history is the source material; a sheet generated later from the document alone can only do the contents half, and must say so on its face.
5. **Teach with it.** If the author cannot defend the document from the sheet alone, the tool replaced them rather than amplified them — and the fix is more generation, not a better summary. Sequence generation before delegation; keep the encoding acts human.

## Style

Written to the author in the second person, plain and fast — a grip card, not a memo. The code section uses the author's own phrasing from the session; the contents section compresses aggressively; the flags section is a checklist the author can act on the next morning.
