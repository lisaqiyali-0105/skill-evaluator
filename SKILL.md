---
name: skill-evaluator
description: Use when the user shares a link to a skill, plugin, or GitHub repo they found online and wants to figure out if it's worth installing. Guides them through understanding, evaluating, and deciding — no technical knowledge required. Triggers on phrases like "should I install this?", "what does this skill do?", "I found this repo", or any pasted GitHub/marketplace link with a question about it.
---

# /skill-evaluator — Should I Install This?

## What This Is

A guided walkthrough that helps you evaluate any skill, plugin, or repo you find online — before you install it. Think of it as a personal curator for AI skills: you hand it a link, it tells you what you're looking at, whether it's relevant to your workflow, whether it's safe, and whether it's worth your time.

The philosophy: **curation over collection.** Don't hoard skills. Upgrade the ones you have by learning from what others build.

No technical knowledge required. Just paste a link and follow along.

---

## Step 1: Understand

**What is this, and does it matter to ME?**

When the user shares a link (GitHub repo, marketplace page, or raw SKILL.md URL):

1. **Fetch the page** using WebFetch or the appropriate tool
2. **Find the SKILL.md or README** — this is the skill's instruction manual
3. **Read the full contents** — don't skim, read everything

Then present a combined overview + relevance assessment. Use color indicators to make it scannable:

- 🟢 = strong match / positive signal
- 🟡 = partial match / worth noting
- 🔴 = mismatch / concern

Format:

> **[Skill name]** — [What it does AND why it matters, in one flowing sentence. Not just the "what" — include the "so what."]
>
> **How it works:** [2-3 sentences explaining the experience of using it. What do you do? What does it do back? What's the end result?]
>
> **What it needs from you:** [Any inputs, files, accounts, or setup required]
>
> ### Is this for you?
>
> 🟢/🟡/🔴 **[Strong match / Partial match / Not a match]**
>
> Here's what I know about you: [Brief summary — their role, what they work on, their tools]. This skill maps to your work because [specific connections]. [If partial or mismatch, explain what doesn't fit.]

If it's a strong or partial match, **don't wait** — go straight into the overlap check. Only pause here if it's a mismatch and you want to confirm whether to continue.

**Platform note:** This skill works in both Cursor and Claude Code. In Claude Code, the agent doesn't naturally pause between steps, so combine steps 1-3 into a single response when the assessment is clear. Only pause at decision points (the verdict, the test drive).

---

## Step 2: Compare & Upgrade

**Do I already have something like this — and what can I learn from the new one?**

Scan the user's existing skills, find overlaps, and turn them into upgrade opportunities.

1. **List all installed skills:** Read the contents of `~/.claude/skills/` (for Claude Code users)
2. **For each skill directory**, read the SKILL.md frontmatter (the `name` and `description` fields)
3. **Compare** the new skill's purpose against every existing skill
4. Use 🟢 (no overlap), 🟡 (adjacent), 🔴 (direct overlap) indicators for scannability

**If no overlap:**
> "🟢 This is net new — you don't have anything that does this yet."

**If overlap found — don't just flag it, compare and recommend upgrades:**

Read BOTH skill files in full. Then present a detailed comparison:

> "🔴 You already have **[existing skill name]** which does something similar. Here's the breakdown:"
>
> | Feature | Your skill | The new one |
> |---|---|---|
> | [Feature 1] | 🟢 / 🔴 [what yours does or doesn't] | 🟢 / 🔴 [what theirs does or doesn't] |
> | [Feature 2] | ... | ... |
>
> **Upgrades worth stealing from theirs:**
> [Numbered list of specific things in the new skill that would improve the user's existing skill]
>
> **Keep from yours (don't lose these):**
> [Numbered list of things the user's skill does better — protect these]
>
> **Recommended upgrade:**
> [Specific, actionable changes to make to the user's existing skill]

The goal is not "install or skip" — it's **"make what you already have better by learning from what's out there."** Overlap is an upgrade opportunity, not a blocker.

After presenting, ask: *"Want me to upgrade your existing skill with these improvements?"*

---

## Step 3: Trust Check

**Is this safe on my machine?**

This is the non-negotiable step, especially for people using work laptops or shared machines.

### Who made it?

- **Author/org:** [GitHub username or organization]
- **Repo popularity:** [Stars, forks, last updated date]
- **Track record:** [Do they have other popular repos? Are they a known entity?]

### What does it actually do?

Read the SKILL.md line by line and flag anything notable:

- **Reads files?** [Which ones, and why]
- **Writes or creates files?** [Where, and what kind]
- **Runs shell commands?** [What commands, and why — this is the biggest risk area]
- **Accesses the internet?** [What URLs, and for what purpose]
- **Installs anything?** [Dependencies, packages, tools]
- **Touches sensitive locations?** [Home directory, system files, credentials, .env files]

### Traffic light rating

**Lead with the verdict first**, then show the evidence.

🟢 **Green — Safe to install**
> "This skill only reads/writes files in expected locations, doesn't run risky commands, and comes from a credible source."

🟡 **Yellow — Probably fine, but review first**
> "This skill does [specific thing] which is worth understanding before you install. [Explain what to look for and why it might be okay.]"

🔴 **Red — Pause and investigate**
> "This skill [specific concern]. I'd recommend [specific action] before installing."

---

## Step 4: Decide & Act

**Scorecard first. Then paths. Then do it.**

Lead with the scorecard — that IS the conclusion:

> ### Skill Scorecard: [Skill Name]
>
> | Check | Result |
> |---|---|
> | **What it does** | [one sentence] |
> | **Solves your problem?** | ✅ Yes / ⚠️ Partially / ❌ No |
> | **Already have it?** | ✅ Net new / ⚠️ Some overlap with [name] / ❌ Duplicate |
> | **Safe to install?** | 🟢 / 🟡 / 🔴 |
> | **Effort to set up** | Low / Medium / High |

If the skill/repo contains multiple skills, add a row per skill showing which are relevant and which aren't.

Then offer clear paths:

> **Here are your options:**
>
> **Path A — Install everything.** Get the full set. Good if you want it all available for later, even if you won't use every skill today.
>
> **Path B — Install just the ones that fit.** I'd recommend [specific skills] based on your use case. Skip the rest for now — you can always add them later.
>
> **Path C — Skip for now.** No install. [Brief reason why this might make sense.]
>
> *Which path works for you?*

**Wait for their decision.** Then act:

- **Install:** Copy the skill to `~/.claude/skills/[skill-name]/SKILL.md`. Confirm what was installed.
- **Customize:** Show suggested edits, walk through changes, install the customized version.
- **Skip:** Acknowledge. Optionally note what they were looking for so you can flag better fits later.

---

## Step 5: Test Drive

**Don't let it become shelfware.** After installing, immediately test it on a real scenario so the user sees value (or doesn't) firsthand.

1. Ask: *"Want to take it for a spin right now? The best way to know if a skill is worth keeping is to use it once on something real."*

2. **If yes**, help the user pick a real scenario. Don't just ask them to come up with one — do the legwork:
   - Look at what the user already has (projects, files, existing skills, recent work) that the new skill could be applied to
   - Offer 2-3 concrete suggestions with a one-line explanation of why each is a good candidate
   - Highlight your top recommendation
   - Keep it small — a 5-minute test, not a full project

3. **Run the skill together.** Walk through it step by step. Let the user experience the full flow.

4. **After the test, ask for the honest verdict:**
   - *"Now that you've used it — was that useful? On a gut level, would you reach for this again?"*

5. **Based on their answer, finalize:**

   **If it clicked:** *"Great — it's staying. You'll know when to use it next time."*

   **If it was meh:** *"Sounds like it's not quite right. Want me to tweak it to fit better, or just uninstall it?"*

   **If it missed:** *"No shame in that. Let me remove it so it doesn't clutter your setup."* Then uninstall.

**The test drive is what separates curation from hoarding.**

---

## Conversation Rules

- **One step at a time.** Never jump ahead. Never combine steps.
- **Plain English only.** No jargon, no acronyms without explanation, no "clone the repo."
- **Always wait for a response** at decision points. The user drives the pace.
- **Be honest.** If a skill isn't great, say so. If there's risk, flag it clearly.
- **Keep it warm but efficient.** Friendly, not fluffy.
- **Be proactive.** Use what you know about the user to make assessments — don't wait for them to tell you what they need.
- **If the user seems unsure at any step**, pause and ask what's on their mind rather than pushing forward.

---

## Common Mistakes to Avoid

- **Skipping the safety check** — non-negotiable, especially on work machines
- **Being too generous with the verdict** — "it's fine!" is not helpful. Be specific about tradeoffs.
- **Assuming technical knowledge** — if you say "run this command," explain what it does first
- **Installing without explicit permission** — always ask before writing anything to their system
- **Treating overlap as a blocker** — overlap is an upgrade opportunity. Compare, steal the best parts, improve what you have.
- **Forgetting to check the actual SKILL.md contents** — don't evaluate based on the README alone; the SKILL.md is what runs on their machine
- **Skipping the test drive** — installing without testing is how skills become shelfware
