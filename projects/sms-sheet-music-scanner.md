---
name: SMS — Sheet Music Scanner
status: active
kickoff: 2026-04-19
external-path: D:\14 Vibe Coding Projects\CLaude Code\sms
---

# SMS — Sheet Music Scanner

**An external Claude Code project, not a vault artifact.** Code lives outside the vault by design — this file is a pointer so the project shows up on Philipp's project map.

## In one sentence

Photo of physical sheet music → AI interpretation + structured disambiguation questions Phil defines → **MusicXML v4** → imported into **MuseScore** for per-voice MP3 practice tracks.

## Why it exists

Phil sings bass in the church choir. He has a stack of physical sheets he wants to practice against the other three voices. **Soundslice** and similar tools have let him down repeatedly because they chase full automation and offer no structured disambiguation. SMS is the opinionated counter-design: human-in-the-loop from the start, with Phil defining the questions.

## Where it lives

- **Project folder:** `D:\14 Vibe Coding Projects\CLaude Code\sms\`
- **Orientation doc:** `sms/CLAUDE.md` (read this when working on the project)
- **Kickoff record:** `sms/docs/2026-04-19-kickoff.md` (frozen origin story)

## Status

**Pre-implementation.** Vision, scope, and v1 architecture agreed on 2026-04-19. No code yet.

## Decisions agreed

- Full 4-voice SATB scope (non-negotiable — needed for practice)
- Phone photos as v1 input (PDFs later if relevant)
- Claude vision + structured questions as v1 approach (Audiveris/Oemer held in reserve for a possible v2 hybrid)
- Success metric: ~80% note accuracy on 3–5 real choir sheets before deciding on hybrid architecture

## Next action

Open a fresh Claude Code session inside the `sms/` folder, let it read `CLAUDE.md`, and start the first build session by drafting the disambiguation question list.
