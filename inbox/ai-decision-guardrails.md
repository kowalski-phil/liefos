---
title: "AI Decision Guardrails — Two Practices for Critical Projects"
created: 2026-03-31
purpose: Embed in Siemens environment for OneMIKA and other critical projects
---

# AI Decision Guardrails

Two practices to prevent AI-assisted work from drifting in the wrong direction unnoticed.

---

## 1. Periodic Devil's Advocate Pass

**When:** Every Friday (or every other Friday) — scheduled, not optional.

**How it works:**
- Describe where the project currently stands in 3-5 sentences.
- Ask the AI: *"Argue against this approach. What are the biggest risks, wrong assumptions, or blind spots? What would you do differently if starting from scratch today?"*
- Review the output critically. If anything resonates, flag it for Monday.
- If the approach survives the challenge — proceed with more confidence.

**Why this matters:** AI presents every suggestion with equal confidence, whether it's brilliant or terrible. On solo projects where there's no colleague to push back, wrong directions can compound for weeks before you notice. This practice forces a structured reality check at regular intervals.

**Template prompt:**
> Here's where [project name] stands: [3-5 sentence summary of current state and approach].
>
> Now argue against this. Give me:
> 1. Three reasons this approach might be fundamentally flawed
> 2. What assumptions am I making that could be wrong?
> 3. If you were starting this project today with what we now know, what would you do differently?

---

## 2. Pre-Commit Decision Challenge

**When:** Before any critical decision that's hard to reverse — choosing a data source, committing to an architecture, defining a scope, selecting a tool.

**How it works:**
- Before executing, ask: *"Give me three reasons this won't work."*
- Takes 30 seconds. Costs nothing. Might save days.
- If the AI can't produce convincing counter-arguments, the decision is probably solid.
- If it produces something that makes you pause — investigate before committing.

**Why this matters:** The most expensive mistakes aren't the ones you catch immediately. They're the ones where a wrong assumption at step 1 makes everything after it look logical — until you hit a wall at step 47 and realize the foundation was off.

**Template prompt:**
> I'm about to [decision]. Before I commit, give me three concrete reasons this might not work or could cause problems later.

---

## The Operator Principle

These guardrails exist because of one core truth: **AI is the generator, you are the filter.** The machine will never stop you and say "wait — are we even solving the right problem?" That's your job. These two practices make that job easier by building structured skepticism into the workflow rather than relying on gut feel in the moment.
