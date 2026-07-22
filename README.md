# No AI slop

A personal fork of [petergyang/no-ai-slop](https://github.com/petergyang/no-ai-slop), customized for Claude.

Removes 20+ patterns of AI slop from writing. Also detects slop on request without rewriting. Works on emails, Slack messages, LinkedIn posts, newsletters, and long-form essays — each format has its own rule overrides.

## What it catches

| Pattern | Smells like |
|---------|-------------|
| Binary contrasts | "It's not X. It's Y." |
| Throat-clearing openers | "Here's the thing..." |
| Faux-insight setups | "What nobody tells you..." |
| Colon reveals | "The best part: it learns." |
| Superficial analysis | "...highlighting the team's commitment" |
| Importance puffery | "marks a pivotal moment" |
| Weasel attribution | "experts agree," "studies show" |
| Fake-strong verbs | "serves as a centralized hub" |
| Synonym cycling | the agent, then the assistant, then the tool |
| Negative listing | "Not a X. Not a Y. A Z." |
| Dramatic fragmentation | "That's it. That's the whole thing." |
| LinkedIn slop | "Humbled to share...", wall-of-white-space, engagement bait |

It also enforces the fundamentals: lead with the point, use active voice, prefer concrete numbers over abstractions.

## What's different from the original

- Format-aware: different rules for Slack, email, blog, newsletter, and LinkedIn
- Stricter on bullets (converted to prose by default), em dashes (banned entirely), and emoji (banned entirely)
- LinkedIn gets its own additional slop patterns
- Feedback loop: after every edit, the skill asks for your final version, diffs it against its rewrite, and proposes entries to `voice-notes.md`
- `voice-notes.md` accumulates writer-specific preferences across sessions

## Install

Paste this into Claude Code:

```
Install this skill globally: https://github.com/MariaVimer/no-ai-slop
```

## Use

**Edit a draft:**

```
/no-ai-slop

[your draft]
```

You get the edited draft, a short What changed section, and a prompt to share your final version for the feedback loop.

**Detect slop without rewriting:**

```
/no-ai-slop is this AI slop?

[the text]
```

You get every pattern found, with the quoted line and a short fix.

## Files

- `SKILL.md`: Editing rules, format overrides, and workflow
- `eval.md`: Pass/fail checks the skill runs on its own edits
- `voice-notes.md`: Writer-specific preferences accumulated from feedback loops

## License

MIT
