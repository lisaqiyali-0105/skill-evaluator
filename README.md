# /do-i-need-this 🤔 aka. Should I Install This Skill?

There are over 400,000 AI agent skills floating around the internet right now. 😵‍💫

I'm a non-technical PM who lives inside Claude Code and Cursor. Over the past two months, I've built 40+ custom skills. Weekly updates, content drafts, PM frameworks, data analytics tools. Skills are how I get work done, efficiently.

The problem? Every week someone on X posts a new skill repo. And every time, I feel the pull. *Maybe this one is the thing I've been missing.* So I rushed to hoard and install them all.

Until I forced myself to pause and ask: does this move the needle for the way I specifically work?

I didn't have a framework for answering that. So I built one. A skill that evaluates other skills (I know 😅). It's a guided process that takes any link to a skill I find online and walks me through evaluating it before I install it. **No code, no technical knowledge.** Just paste a link and follow along.

## How it works

5 steps. You go through them one at a time:

| | Step | What happens |
|---|---|---|
| 1️⃣ | **Understand + Assess Relevance** | Fetches the skill and gives you a plain-English summary. It doesn't just tell you *what* the skill does. It tells you if it matters to *you*, using what it knows about your workflow |
| 2️⃣ | **Compare & Upgrade** | This one changed everything for me 🔥 If you already have something similar, it compares them side by side and tells you what to steal from theirs to "upskill" yours (pun intended 😊) |
| 3️⃣ | **Trust & Security Check** | ⚠️ Non-negotiable, especially on a work laptop. Does this skill run shell commands? Touch sensitive files? Green/yellow/red rating. No guessing |
| 4️⃣ | **Decide & Act** | Scorecard + 3 clear paths: install it all, cherry-pick the good stuff, or skip guilt-free |
| 5️⃣ | **Test Drive** | Immediately run the skill on a real workflow. 5-minute exercise, not a full project. This is what keeps skills from becoming shelfware 🤷 |

## Why I built this

The biggest surprise? **Most of the value came from Step 2, not Step 4.**

I expected this to help me decide what to install. Instead, it mostly helped me improve what I already had. The overlapping skills were the most valuable! Not because I installed them, but because I learned from them.

👉 Real example: I found a PM repo with a meeting notes skill. I already had my own. The comparison showed me 3 features theirs did better (tracking participants, logging disagreements, auto-saving to a file). So I just bolted those onto mine. One skill, now better. Zero clutter.

💡 I'm a big fan of Kaizen. Always build on the shoulders of giants. Study what others build, steal what works, sharpen what you already have ✨

I didn't need more skills. I needed better versions of the ones I'd already built.

📖 [Read the full Substack article](https://lisaslens.substack.com/)

## Install

Works in Claude Code, Cursor, and any other tools that read the SKILL.md format.

### Claude Code

```bash
mkdir -p ~/.claude/skills/do-i-need-this
curl -o ~/.claude/skills/do-i-need-this/SKILL.md \
  https://raw.githubusercontent.com/lisaqiyali-0105/do-i-need-this/main/SKILL.md
```

### Cursor

Copy `SKILL.md` to `.cursor/skills/do-i-need-this/SKILL.md` in your project.

### Other AI assistants

It follows the open SKILL.md standard. Just copy the file to wherever your tool reads skills from.

Pro tip: If you don't know how to install a skill, simply ask Claude to guide you.

## How to use it

Paste a link to any skill, plugin, or GitHub repo and say:

- 👉 "Do I need this?"
- 👉 "How does this compare to what I already have?"
- 👉 "Should I install this?"

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

## The Bottom Line

As it is with many things in life, less is more. 🧠

Not fewer skills for the sake of decluttering, but fewer skills that each do exactly what you need.

Next time a shiny new repo pops up on your feed, ask yourself: do I actually need this, or am I just afraid of missing out?

That question might be the most valuable "skill" of all.

## License

MIT
