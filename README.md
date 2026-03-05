# skill-evaluator: Should I Install This? 🤔

I have 44 skills in my Claude Code setup. Meeting notes, content drafts, travel perks, PM frameworks. I built most of them myself.

The problem? Every week someone on X posts a new skill repo with a hundred stars and I feel the pull. *Maybe this one is the thing I've been missing.* So I'd install it, forget about it, and move on to the next one. Classic FOMO. 😅

Truth is, at some point I stopped and asked myself... is any of this actually making me better? Honest answer? I had no idea.

So I built a skill that evaluates other skills before I install them. You paste a link and it walks you through everything: what the skill does, whether it's relevant to you, whether it's safe, and whether it's actually worth keeping. **No code, no technical knowledge.** Just follow along.

## How it works

5 steps. You go through them one at a time (the skill literally won't let you skip ahead):

| | Step | What happens |
|---|---|---|
| 1️⃣ | **Understand** | Fetches the skill and gives you a plain-English summary. But here's the key: it doesn't just tell you *what* the skill does. It tells you if it matters to *you*, based on your workflow and what you already have |
| 2️⃣ | **Compare & Upgrade** | This one changed everything for me 🔥 If you already have something similar, it compares them side by side and shows you what to steal from the new one to make yours better. Overlap isn't a blocker, it's an upgrade opportunity |
| 3️⃣ | **Trust Check** | Especially if you're on a work laptop! Does this skill run shell commands? Touch sensitive files? You get a simple green/yellow/red rating. No guessing |
| 4️⃣ | **Decide & Act** | Scorecard + clear paths: install it all, cherry-pick the good stuff, or skip guilt-free |
| 5️⃣ | **Test Drive** | You immediately run the skill on something real. A 5-minute exercise, not a full project. This is what keeps skills from becoming shelfware |

## Why I built this

So... **most of the value came from Step 2, not Step 4.**

I expected this to help me decide what to install. Instead, it mostly helped me sharpen what I already had. The overlapping skills were the most valuable! Not because I installed them, but because I learned from them.

👉 Real example: I found a PM repo with a meeting notes skill. I already had my own. Instead of installing a second one, the comparison showed me 3 features theirs did better (tracking participants, logging disagreements, auto-saving to a file). So I just bolted those onto mine. One skill, now better. Zero clutter.

💡 That's the mentality. Don't collect more tools. Study what others build, steal what works, sharpen what you already have. Kaizen for your AI toolkit ✨

## Install

### Claude Code

```bash
mkdir -p ~/.claude/skills/skill-evaluator
curl -o ~/.claude/skills/skill-evaluator/SKILL.md \
  https://raw.githubusercontent.com/lisaqiyali-0105/skill-evaluator/main/SKILL.md
```

### Cursor

Copy `SKILL.md` to `.cursor/skills/skill-evaluator/SKILL.md` in your project.

### Other AI assistants

It follows the open SKILL.md standard. Just copy the file to wherever your tool reads skills from.

## How to use it

Paste a link to any skill, plugin, or GitHub repo and say something like:

- 👉 "Should I install this?"
- 👉 "How does this compare to what I already have?"
- 👉 "Is this relevant to my workflow?"

It takes over from there. Step by step, one at a time. You drive the pace.

## Where to find skills 👀

If you're not sure where to look, here are the big skill marketplaces:

| Marketplace | Size | Link |
|---|---|---|
| SkillsMP | 364,000+ | [skillsmp.com](https://skillsmp.com) |
| Agent Skills | 63,000+ | [agent-skills.cc](https://agent-skills.cc) |
| Skill For That | 10,000+ | [skillforthat.com](https://skillforthat.com) |
| PolySkill | LLM-agnostic | [polyskill.ai](https://polyskill.ai) |
| Claude Code Plugin Directory | 50+ curated | [claudecodeplugin.com](https://www.claudecodeplugin.com) |

These platforms handle discovery. Figuring out if any of it is actually worth your time? That's what this skill is for.

## License

MIT
