---
type: project-log
topic: LifeOS Obsidian vault setup
date: 2026-03-18
tags: obsidian, vault, setup, file-intel, canvas
---

# LifeOS Obsidian Vault Setup — 2026-03-18

## What Was Decided

- **Journal entries consolidated:** Moved 15 entries from `journal/daily/` → `daily/`. One folder for all daily notes. Streak intact (Mar 2-16).
- **Global context injection:** Added LifeOS CLAUDE.md to global `~/.claude/CLAUDE.md` so it loads in every Claude Code session. Cost: ~2-3K tokens out of 1M — worth it for cross-project awareness.
- **File-intel switched to OpenRouter:** Both Python scripts (`process_files_with_gemini.py`, `process_docs_to_obsidian.py`) rewritten to use OpenRouter API instead of Google Gemini SDK directly. Model: `google/gemini-3-flash-preview`. No `google-genai` dependency needed anymore.
- **Python confirmed working:** Python 3.12 on system, all packages installed (python-dotenv, python-docx, python-pptx, pillow, pdfplumber, openpyxl).

## Key Things to Remember

- `.env` at vault root holds `OPENROUTER_API_KEY` — used by both file-intel scripts
- Windows encoding fix added to both scripts (`sys.stdout.reconfigure(encoding="utf-8")`) — emojis in output caused crashes without it
- `/file-intel` tested successfully on a PDF (school trip letter) — full pipeline works
- JSON Canvas skill tested — created `daily-crypto-routine.canvas` from TBot project data
- `journal/` folder removed — all references updated (CLAUDE.md, journal command, memory)

## Structure After Changes

```
00-LifeOS/
├── daily/              ← journal entries live here now (was journal/daily/)
├── metrics/
├── brain-dumps/
├── briefs/
├── content/newsletter/
├── ideas/viva-engage/
├── projects/
├── research/
├── inbox/
├── archive/
├── scripts/            ← process_files_with_gemini.py, process_docs_to_obsidian.py
├── outputs/            ← file-intel output lands here
├── .env                ← OPENROUTER_API_KEY
├── requirements.txt
├── CLAUDE.md
└── daily-crypto-routine.canvas
```

## Next Actions

- None blocking — vault is fully operational
- Can import more files via `/file-intel` anytime
- Canvas skill available for visual maps of any content
