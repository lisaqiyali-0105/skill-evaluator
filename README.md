# skill-evaluator — Should I Install This?

A skill that helps you evaluate other skills before you install them.

There are 364,000+ AI agent skills on the internet. You don't need all of them. You need the right ones — and you need to know how to make the ones you already have better.

**skill-evaluator** is a guided process that takes any skill, plugin, or repo you find online and walks you through 5 steps: understand it, compare it to what you have, check if it's safe, decide what to do, and test it on something real.

Built for non-technical users. No code required. Just paste a link.

## The 5 Steps

| Step | What it does |
|---|---|
| **1. Understand** | Fetches the skill, summarizes it in plain English, and tells you whether it's relevant to YOUR workflow |
| **2. Compare & Upgrade** | Checks for overlap with your existing skills. If overlap exists, compares them side by side and recommends upgrades — steal the best parts from the new skill to improve yours |
| **3. Trust Check** | Reviews what the skill actually does on your machine. Gives a green/yellow/red safety rating |
| **4. Decide & Act** | Shows a scorecard and offers clear paths: install everything, install just what fits, or skip |
| **5. Test Drive** | Runs the skill on a real scenario immediately so you know if it's worth keeping before it becomes shelfware |

## Philosophy

**Curation over collection.** The skill marketplaces handle discovery. This skill handles evaluation.

The most valuable thing isn't finding more skills — it's getting more out of fewer skills. When you find overlap, don't just skip the new skill. Study it. Steal what it does better. Upgrade what you already have.

Think of it as Kaizen for your AI toolkit.

## Install

### Claude Code

Copy the `SKILL.md` file to your skills directory:

```bash
mkdir -p ~/.claude/skills/skill-evaluator
curl -o ~/.claude/skills/skill-evaluator/SKILL.md \
  https://raw.githubusercontent.com/lisaqiyali-0105/skill-evaluator/main/SKILL.md
```

### Cursor

Copy the `SKILL.md` file to `.cursor/skills/skill-evaluator/SKILL.md` in your project.

### Other AI Assistants

The `SKILL.md` file follows the open SKILL.md standard. Copy it to wherever your tool reads skills from.

## Usage

Just paste a link to any skill, plugin, or GitHub repo and ask:

- "Should I install this?"
- "What does this skill do?"
- "Is this relevant to my workflow?"
- "How does this compare to what I already have?"

The skill takes over from there.

## Example

```
You: I found this repo — https://github.com/someone/cool-skills — should I install it?

skill-evaluator: [Fetches, summarizes, checks relevance, compares with your existing skills,
                   runs safety check, presents scorecard, offers paths, and test-drives it with you]
```

## Where to Find Skills

Not sure where to look? Here are the major skill marketplaces:

| Marketplace | Size | Link |
|---|---|---|
| SkillsMP | 364,000+ | [skillsmp.com](https://skillsmp.com) |
| Agent Skills | 63,000+ | [agent-skills.cc](https://agent-skills.cc) |
| Skill For That | 10,000+ | [skillforthat.com](https://skillforthat.com) |
| PolySkill | LLM-agnostic | [polyskill.ai](https://polyskill.ai) |
| Claude Code Plugin Directory | 50+ curated | [claudecodeplugin.com](https://www.claudecodeplugin.com) |

Discovery is their job. Evaluation is this skill's job.

## License

MIT
