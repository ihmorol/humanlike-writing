# humanlike-writing

An agent skill that makes Claude (and other skill-aware agents) write and edit prose that reads like a careful person wrote it. It cuts formulaic AI wording, chatbot residue, padded structure, and fake profundity, and it keeps your facts, quotes, code, citations, and required formats exactly as they were.

It's a writing-quality skill. It isn't an AI-detector bypass, and it never invents experiences, sources, or numbers to sound more human.

## What's inside

- `SKILL.md`: the workflow and strict prose rules.
- `references/pattern-catalog.md`: 144 patterns, each with a rule, an example, a repair, and an evidence label.
- `references/voice-and-audit.md`: matching your writing sample, the "clean but soulless" check, a self-audit pass, and 9 extra patterns.
- `references/voice-and-context.md`: how the rules bend for academic writing, code, quotes, translations, and Wikipedia.
- `scripts/lint_writing.py`: an optional checker (Python 3 stdlib only) for banned words, em dashes, rhythm, and chatbot residue.

## Install

**Claude Code (plugin):**

```
/plugin marketplace add ihmorol/humanlike-writing
/plugin install humanlike-writing@humanlike-writing
```

**Any agent that supports the skills CLI (Claude Code, Codex, Cursor, and others):**

```bash
npx skills add ihmorol/humanlike-writing
```

**Manual:** copy `skills/humanlike-writing/` into your skills folder, for example `~/.claude/skills/humanlike-writing` or `~/.codex/skills/humanlike-writing`, then start a new session.

**Claude.ai / Claude desktop:** download `humanlike-writing.skill` from the [latest release](https://github.com/ihmorol/humanlike-writing/releases/latest) and upload it under Settings → Capabilities → Skills.

**Plain chat with no skill support:** attach `SKILL.md`, `references/pattern-catalog.md`, and `references/voice-and-audit.md`, then say "Follow the attached humanlike-writing skill for your prose in this conversation."

## Use

It triggers on its own when you ask for humanized or less robotic writing. You can also call it directly:

- "Rewrite this email with humanlike-writing. Keep every date and number."
- "Make this sound like me. Here's a sample of my writing: ..."
- "Audit this draft with humanlike-writing and show me the tells you fixed."
- "Use humanlike-writing for your replies for the rest of this chat."

Optional checker:

```bash
python skills/humanlike-writing/scripts/lint_writing.py draft.md --json
```

Exit code 1 means a literal rule was hit (a banned word, an em dash). It says nothing about who wrote the text.

## Credits

Pattern research draws on Wikipedia's "Signs of AI writing" guide and the sources listed in `references/sources-and-limits.md`. Voice calibration, the soul check, and the self-audit loop are adapted from [blader/humanizer](https://github.com/blader/humanizer) (MIT).

## License

MIT
