# The Genie Lamp

*A starter kit for persistent memory, for anyone who has none of it. Copy the files below, fill in your own answers, and you have the whole mechanism on day one.*

A language model has **no memory between sessions.** The context window is the entire state, and nothing survives the end of a conversation. Every session is anterograde amnesia — which is why re-explaining yourself feels maddening and never stops. **That's architecture, not a capability problem, and you can't fix it by asking nicely.**

So keep the state outside the model and re-inject it at the top of every session.

> **The model is the procedure. The file is the state.**

---

## Why this beats the alternatives

**In-context beats retrieval.** A rule that is loaded cannot fail to be noticed. A rule that has to be fetched can.

**It beats fine-tuning.** Training is slow, expensive, and irreversible. A file is editable in a second, and every line in it is dated and attributable. **You cannot audit a weight.**

**Store the rule, not the fact.** This is the part that makes it scale. When the model gets something wrong, write down the *general form* of the mistake, not the specific correction. Not *"the meeting is on Thursdays"* — instead, *I confuse these two recurring things; check which one before asserting either.* Facts grow linearly with everything you've ever discussed. **Policies compress.** That's why one file can cover a year and get denser rather than merely longer.

**Load the rules whole; keep the corpus on disk.** Rules are small and always relevant, so they belong in context. History and reference material are large and only sometimes relevant, so they live in the archive and get pulled when needed. Same compression principle, one level up.

---

## Name it something you'll actually maintain

A folder called `persistent_context_store` does not get maintained. A folder called **the lamp** does — you rub it, something comes out, and you keep it lit.

This sounds like a joke and it is load-bearing. The system only works if you keep feeding it on an ordinary Tuesday when nothing is exciting. **Whimsy is what makes the discipline survive contact with a Tuesday.** People who name their sourdough starter *Pilchard the Galactic Conqueror* keep their sourdough starter alive. Name yours whatever you will not abandon.

---

## The six things in it

| | |
|---|---|
| `WAKE.md` | The short one. The only file you paste every time. |
| `RULES.md` | Append-only. One dated line per correction. |
| `STYLE.md` | How you want things written, so you stop respecifying it. |
| `HANDOFF.md` | Rewritten at the end of every session. |
| `transcripts/` | The full text of every conversation, dated. |
| `archive/` | Dated copies taken *before* any change. Every time. |

**`transcripts/` is the folder everyone skips and the one that saves you.** When a session's context compacts, everything not written down is gone — including things you said that neither of you knew were important yet.

---

## Starting contents — copy these

### `WAKE.md`

```
# WAKE — start here

Read this before answering anything.

## Who I am
[Name, what I do, who I do it for.]

## What we're working on
[One or two lines. Update when it changes.]

## Standing rules
1. Verify at the destination. When you claim you did something, check that it
   landed and tell me what you actually checked.
2. When I correct you, write the general rule into RULES.md and show me the line.
3. Never overwrite. Only append.
4. Ask before doing anything irreversible.
5. [Your own. Add them as you learn what you keep repeating.]

## Where things are
- Rules ......... RULES.md
- Style ......... STYLE.md
- Last session .. HANDOFF.md
- History ....... transcripts/, archive/

Keep this file to one or two pages. If it grows past that, move the detail into
the archive and leave a pointer here.
```

### `RULES.md`

```
# RULES — append only

One dated line per correction. Write the GENERAL rule, never the specific fact.
Never edit or delete an earlier entry. If something is superseded, say so in the
new entry and leave the old one visible.

- [YYYY-MM-DD] ...
```

### `STYLE.md`

```
# STYLE

## Length
[How much you want at once. Be honest about what you can actually read.]

## Format
[Prose or bullets. Headings or not. Tables when.]

## Voice
[Words to avoid. Register. Whether you want hedging or a straight answer.]

## Never
[The things that make you close the window.]
```

### `HANDOFF.md`

```
# HANDOFF

Rewritten at the end of every working session. Overwrite this file; the dated
copy in archive/ is the history.

DATE:
STATE:      What this session was, and where it left off.
IN FLIGHT:  Unfinished work, with file paths and status.
OPEN:       Decisions pending. Who owes whom what.
RULED:      What I already decided, in my own words, so nobody reopens it.
ASK FIRST:  The one to three things to open the next session with.
DO NOT:     Live landmines.
```

---

## The setup prompt

Paste this into a fresh conversation and let it build the folder for you.

```
I want you to help me build a persistent memory system for our work together,
because you have no memory between sessions and I'm tired of re-explaining
myself.

Create a folder with these files and write the starting contents of each:

WAKE.md — the short one. Who I am, my standing rules, and pointers to
everything else. This is the only file I paste every time, so keep it lean — a
page or two. If it grows past that, move the detail into the archive and leave
a pointer.

RULES.md — append-only. Every time I correct you, add one dated line. Write the
GENERAL rule, never the specific fact. Never edit or delete an earlier entry;
if it's superseded, say so in the new one.

STYLE.md — how I want things written and formatted, so I stop respecifying it.

HANDOFF.md — you rewrite this at the end of every working session: what we did,
what state everything is in, what's still open, and what I've already ruled on
so you don't reopen it.

transcripts/ — save the full text of every conversation here, dated. When a
session's context window compacts, everything not written down is gone,
including things I said that neither of us knew were important yet.

archive/ — dated copies of the files above, taken BEFORE any change. Every
time. No exceptions.

Standing rules for you, permanently:

1. I paste WAKE.md at the start of every session. Read it before you answer
   anything.
2. When you claim you did something, verify it at the destination and tell me
   what you actually checked.
3. When I correct you, don't just fix it — write the rule in RULES.md and show
   me the line.
4. Never overwrite. Only append.
5. At the end of a working session, save the transcript and update HANDOFF.md.

Start by asking me the ten questions whose answers you'd most want at the top of
every future conversation.
```

---

## If you ever run more than one assistant at once

Two sessions writing to the same files will overwrite each other silently. The fix is a **baton**:

- **One holder at a time**, and a file at a fixed location is the *only* authority on who has it. Not memory, not vibes — a file.
- **Append rows, never edit them.** Every pass records who handed it over and on whose ruling.
- **Mistakes get struck through and marked VOID, not deleted.** The error stays visible.
- **Open items travel at the pass**, closing with your ruling in your own words, so nobody reopens something you already decided.
- **One office stands outside the baton.** Whoever runs the integrity check — file sizes, a zero-byte scan, does a backup actually exist — must be barred from holding the baton. If it writes on Monday, it audits its own work on Tuesday and the check is worthless. **That independence is the whole product.**

That last one is separation of duties. It is the part worth defending hardest, and it is the part people cut first.

---

## Three failure modes this exists to prevent

1. **Silent loss at compaction.** A long session compacts, and everything not written down is gone. The transcript folder is the only thing that survives it.
2. **The tidy that eats the copies.** Consolidating scattered files into one tidy file feels like good housekeeping, and it halves your copies. **Fewer copies is never tidier**, and a backup the assistant can reach is not a backup.
3. **Relitigating settled ground.** Without a written ruling, every session re-opens decisions you already made. `HANDOFF.md` closes them in your own words.

---

**Everything above is the entire mechanism.** A mature lamp is this, plus a year of not skipping the archive step.

*Free to copy and adapt. No attribution required.*
