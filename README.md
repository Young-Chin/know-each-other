# Know Each Other

A Claude skill for building deep, personalized AI-human collaboration through psychological profiling.

## What It Does

Most AI assistants treat every conversation as a blank slate. **Know Each Other** changes that — it helps Claude truly understand who you are as a person: your cognitive style, decision-making patterns, and inner drives. The result is an AI partner that adapts to *you*, not the other way around.

It uses the **MBTI framework and Jungian cognitive functions** not as a personality label, but as a structured language to translate your behavior into psychological insight.

Two files are generated and shared across all your projects:

- **`~/.claude/SOUL.md`** — Claude's personality config: how it communicates, gives feedback, and collaborates with you
- **`~/.claude/USER_PROFILE.md`** — Your psychological portrait: cognitive functions, decision style, working patterns

## How It Works

### Phase 1: Initialization (first run)

A natural, two-part conversation — not a questionnaire:

1. **Shape your agent** — What kind of collaborator do you want? Communication style, feedback approach, level of proactivity, emotional tone.
2. **Who are you** — A dialogue guided by the four MBTI dimensions (E/I, N/S, T/F, J/P), designed to surface your cognitive structure, not just your preferences.

After the conversation, Claude performs a *psychological translation*: it interprets what you said through the lens of Jungian cognitive functions (Ne, Ni, Te, Ti, Fe, Fi, Se, Si) and writes profiles that describe how you *think*, not just what you like.

### Phase 2: Ongoing updates

After any meaningful conversation, the skill reviews what was observed and surfaces worth-saving insights:

```
📝 A few things worth adding to your profile:

USER_PROFILE.md → Observed patterns:
  + "Repeatedly verified implementation details before moving on → Si signal, relies on proven approaches"

SOUL.md → Special agreements:
  + "No comments in code by default"

Confirm to write, or suggest edits.
```

### Phase 3: Silent updates

Clear, consistent signals (e.g., the same cognitive pattern appearing three conversations in a row) are quietly incorporated. Major re-assessments — like revising your core MBTI type — always require your confirmation.

## Trigger Signals

The skill activates when you say things like:

- "You don't really know me yet"
- "Remember how I like to work"
- "I want you to have a consistent personality"
- "What do you know about me?"
- "Let's initialize my profile"

## Installation

This is a [Kiro CLI](https://kiro.ai) skill. To install:

1. Copy `SKILL.md` and `references/` into your Claude skills directory:
   ```
   ~/.claude/skills/know-each-other/
   ```
2. The skill will appear in your available skills list automatically.

## Psychological Framework

The skill draws on:

- **MBTI four dimensions** as a conversation scaffold
- **Jungian eight cognitive functions** for deeper personality analysis
- **Behavioral signal interpretation** — reading *how* you say things, not just what you say

Full reference material is in [`references/personality-frameworks.md`](references/personality-frameworks.md).

## Philosophy

People build deep working relationships not by memorizing each other's preference lists, but by understanding how the other person *thinks*. This skill applies that same principle to human-AI collaboration.

---

*A [Kiro](https://kiro.ai) skill — built for Claude.*
