# The Prompt-Library Keeper

*The meta-prompt: it turns any good working prompt into a durable, reusable library entry and keeps the whole library consistent as it grows.*

Run it at the end of any project that produced a prompt worth keeping, or whenever adding or revising an entry. Its premise is that chat logs are disposable and the library is the real memory — so a prompt that isn't written down is a prompt that's already lost.

## The prompt

> Maintain my prompt library, stored at [LIBRARY LOCATION — where the library document lives, e.g., a Word file in a named folder]. I will hand you a working prompt (or a project that used one); genericize it and add it as a new entry, or revise an existing entry. First inventory the existing library so the new entry matches the others exactly and doesn't duplicate one.
>
> **Entry format, matched exactly to what's already there:** a titled section for each prompt with (1) a one-word-or-phrase name and a short parenthetical on its role/audience; (2) a Purpose paragraph — what the deliverable is, who uses it, where in the workflow it runs, what it needs; (3) the copy-paste prompt itself in a visually distinct block; (4) Guardrails — numbered failure-modes-to-avoid, each an actual observed problem stated as a behavior to demand; and (5) Style Points for the deliverable. End the document with a dated log table; add a row for every addition or revision, noting where the prompt was distilled from.
>
> **Genericizing rule:** strip every [CASE/PROJECT-SPECIFIC FACT — names, numbers, parties, dates] and keep only the shape of the task, expressed as placeholders in the form [NOUN CATEGORY — explanation of what the placeholder is FOR and how it relates to the rest of the prompt]. The user replaces the whole bracket; every placeholder must justify why the prompt needs that input, not merely name it.
>
> **Preservation discipline:** never overwrite the library file — save every material change as a new versioned copy whose filename states the version and what changed. Match the existing document's own formatting by editing its structure directly, not by regenerating it through a converter that would flatten the styling. After saving, show me the new entry rendered so I can eyeball it before it's final.
>
> Finally, at the end of every project — not just this one — study what we did for lessons learned and append them to [MEMORY STORE — the skill file or notes that persist across sessions], and proactively flag the moments when it's worth creating a new entry, a new skill, or some other durable memory structure. Ask before any large-token pass, and offer a leaner route as part of asking.

## Guardrails

1. **Add it in the same session it was born.** Chat logs vanish; a good prompt not written down is lost. The rule that recovered this very library after a log loss: capture the prompt the moment the project ends, never "later."
2. **Match the document, not a fresh template.** New entries are added by cloning the existing structure so they're indistinguishable from the originals. Regenerating the file through a converter flattens shading, headings, and tables — the entry looks bolted on.
3. **Placeholders must explain themselves.** Every bracket states its function, not just its slot. "[PARTY]" is useless; "[CLIENT PARTY — the side our firm represents, which sets whether each argument attacks or defends]" is reusable a year later by someone who wasn't in the room.
4. **Never overwrite; version everything.** Each material change is a new dated file. The library is institutional memory — a silent overwrite can erase a good prompt with no undo.
5. **Capture lessons, suggest structure.** End every project by appending lessons learned and flagging when a new skill/agent/memory belongs. The library grows better, not just bigger.

## Style

Consistency is the whole game: identical section structure, identical placeholder convention, identical shaded-block styling for every prompt, so the library reads as one authored work rather than an accretion. The log table is the changelog — terse, dated, origin noted. Keep the prompts themselves domain-portable: the format shouldn't assume any one practice area, so the library can travel.
