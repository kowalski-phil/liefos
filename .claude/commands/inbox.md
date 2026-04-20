# Inbox Processor

You are processing Philipp's inbox — the drop zone where raw ideas, notes, and files land before being sorted. Read CLAUDE.md for full context about who Philipp is.

## Process

1. **Scan the inbox:** Read all files in `inbox/`. For each item, summarize what it is in one line.

2. **Present the triage list:** Show Philipp what's in his inbox as a numbered list with your suggested categorization:
   - **idea** → `ideas/` (content ideas, business ideas, project concepts)
   - **idea/viva** → `ideas/viva-engage/` (internal blog post ideas for Siemens)
   - **project** → `projects/` (active work with next actions)
   - **research** → `research/` (reference material, articles, analysis)
   - **brief** → `briefs/` (news, industry updates)
   - **content** → `content/` (newsletter drafts, YouTube scripts)
   - **skip** → leave in inbox (not ready to sort yet)
   - **delete** → suggest removal (but NEVER actually delete — only Philipp deletes)

   For each item, suggest a destination and brief reason. Ask Philipp to confirm or adjust.

3. **Enrich and sort:** For each confirmed item, create the enriched file in the target folder with this frontmatter. Then **MOVE the original to `archive/`** — keeping the original filename. NEVER use `rm` or delete. The flow is always: copy to target folder (enriched) → copy original to `archive/` → only then remove from `inbox/`.

   ```yaml
   ---
   title: "Short descriptive title"
   type: idea | project | research | content | brief
   status: incubating
   created: YYYY-MM-DD
   review-after: YYYY-MM-DD  # next Saturday from today
   tags: [relevant, tags, here]
   source: inbox
   ---
   ```

   Then include the original content below, lightly cleaned up but preserving Philipp's voice.

   **File naming:** `YYYY-MM-DD-slug.md` (use the creation date, not today's date if the item has one).

4. **Handle PDFs and non-markdown:** For PDFs or other binary files, don't move them — just note what they are and ask Philipp where they belong (or if they can be deleted). If a parsed/summary version already exists, mention that.

5. **Summary:** After processing, show:
   - What was moved and where
   - What was left in inbox and why
   - How many items now have `review-after` dates (these will resurface during journaling)

## Frontmatter Defaults

- `review-after`: next Saturday from today. If today IS Saturday, set it to today. Philipp can override per item.
- `status`: always starts as `incubating` unless Philipp says it's already active
- `tags`: suggest 2-4 tags based on content. Use existing tags from `ideas/` when possible for consistency.

## HARD RULE — No Deletions

**NEVER delete any file. Ever. Under any circumstances.**
- Processed inbox items go to `archive/` — the original, unmodified, with its original filename.
- The `archive/` folder is the graveyard. Nothing gets deleted from there either.
- If in doubt, leave the file where it is and ask Philipp.
- This rule has no exceptions.

## Important

- Don't over-polish the content. Philipp's raw notes are intentionally rough.
- If an item already has frontmatter, merge — don't overwrite existing fields.
- If an item clearly belongs to an existing project in `projects/`, mention the connection.
