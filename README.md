# skill-evaluator — Should I Install This?

I have 44 skills in my Claude Code setup. Meeting notes, content drafts, travel perks, PM frameworks — you name it. I built most of them myself.

The problem? Every week someone on X posts a new skill repo with a hundred stars and I feel the pull. *Maybe this one is the thing I've been missing.* So I'd install it, forget about it, and move on to the next one. Classic skill hoarding.

At some point I stopped and asked: is any of this actually making me better? Honest answer — I had no idea.

So I built a skill that evaluates other skills before I install them. **Paste a link, get a guided walkthrough.** No code, no technical knowledge needed. It just walks you through the questions you should be asking but probably aren't.

## What it actually does

Five steps. Each one earns its place.

| Step | What happens |
|---|---|
| **1. Understand** | Fetches the skill, gives you a plain-English summary, and immediately tells you if it's relevant to *your* workflow — not just "what does this do" but "does this matter to me" |
| **2. Compare & Upgrade** | This is the one that changed everything. If you already have something similar, it compares them side by side and tells you what to steal from the new skill to make yours better |
| **3. Trust Check** | Especially if you're on a work laptop — does this skill run shell commands? Touch sensitive files? Green/yellow/red, no guessing |
| **4. Decide & Act** | Scorecard + clear paths: install it all, cherry-pick the good stuff, or skip guilt-free |
| **5. Test Drive** | Run it on something real, right now, before it becomes shelfware |

## Why I built this

Here's what I realized: **the value isn't in finding more skills. It's in getting more out of fewer skills.**

I tested this on my own meeting notes skill. Found a PM repo with a similar one. Instead of installing theirs alongside mine, the comparison showed me three features theirs did better — tracking participants, logging disagreements, auto-saving to a file. So I upgraded mine. One skill, now better, instead of two skills competing for attention.

That's the whole philosophy. Curation over collection. Study what others build, steal what works, sharpen what you already have. Kaizen for your AI toolkit.

The marketplaces handle discovery. This skill handles the part that actually matters — figuring out if something is worth your time.

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

The file follows the open SKILL.md standard — copy it to wherever your tool reads skills from.

## How to use it

Paste a link to any skill, plugin, or GitHub repo and say something like:

- "Should I install this?"
- "How does this compare to what I already have?"
- "Is this relevant to my workflow?"

It takes over from there.

## Where to find skills

If you're looking for skills to evaluate, here's where most of them live:

| Marketplace | Size | Link |
|---|---|---|
| SkillsMP | 364,000+ | [skillsmp.com](https://skillsmp.com) |
| Agent Skills | 63,000+ | [agent-skills.cc](https://agent-skills.cc) |
| Skill For That | 10,000+ | [skillforthat.com](https://skillforthat.com) |
| PolySkill | LLM-agnostic | [polyskill.ai](https://polyskill.ai) |
| Claude Code Plugin Directory | 50+ curated | [claudecodeplugin.com](https://www.claudecodeplugin.com) |

## License

MIT
