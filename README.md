# Know Each Other

> A Claude skill that helps AI truly understand *who you are* — not just what you want.

Most AI assistants start from zero every session. **Know Each Other** builds a persistent psychological portrait of you, so Claude can adapt to your thinking style, communication preferences, and decision-making patterns across all your projects.

---

## How It Works

```
First run                    Every session after
─────────────────────        ──────────────────────────────
  Conversation               Observe → Suggest → Confirm
       ↓
  Psychological                  📝 Worth saving?
  Translation                    USER_PROFILE.md
       ↓                           + new pattern
  Two files created            SOUL.md
                                   + new agreement
  ~/.claude/SOUL.md
  ~/.claude/USER_PROFILE.md   You confirm → written
```

### The Two Files

| File | What it holds |
|------|--------------|
| `~/.claude/SOUL.md` | Claude's personality: tone, feedback style, proactivity, communication habits |
| `~/.claude/USER_PROFILE.md` | Your psychological portrait: cognitive functions, decision style, work patterns |

Both are global — shared across every project.

---

## Three Phases

**① Initialize** *(first run)*

A natural two-part conversation — not a form:

- **Shape your agent** — What kind of collaborator do you want?
- **Who are you** — A dialogue across the four MBTI dimensions (E/I · N/S · T/F · J/P)

Claude then performs a *psychological translation*: your words → Jungian cognitive functions (Ne, Ni, Te, Ti, Fe, Fi, Se, Si) → a portrait that describes how you *think*, not just what you prefer.

**② Suggest updates** *(after meaningful conversations)*

```
📝 A few things worth adding to your profile:

USER_PROFILE.md → Observed patterns:
  + "Verified details repeatedly before moving on → Si signal"

SOUL.md → Special agreements:
  + "No comments in code by default"

Confirm to write, or suggest edits.
```

**③ Silent updates** *(clear, repeated signals)*

Consistent patterns are quietly incorporated. Major changes — like revising your MBTI type — always ask first.

---

## Trigger Phrases

Say any of these and the skill activates:

- *"You don't really understand me"*
- *"Remember how I like to work"*
- *"I want you to have a consistent personality"*
- *"What do you know about me?"*
- *"Let's initialize my profile"*

---

## Installation

```bash
# Copy into your Claude skills directory
cp -r . ~/.claude/skills/know-each-other/
```

The skill appears in your available skills list automatically.

---

## Psychological Foundation

The framework behind the skill:

- **MBTI 4 dimensions** — conversation scaffold for the initialization dialogue
- **Jungian 8 cognitive functions** — the actual analysis layer (Ne/Ni/Te/Ti/Fe/Fi/Se/Si)
- **Behavioral signal reading** — *how* you say things matters as much as *what* you say

Full reference → [`references/personality-frameworks.md`](references/personality-frameworks.md)

---

*A [Kiro](https://kiro.ai) skill — built for Claude.*
