# No AI slop

This skill removes 17 patterns of AI slop from your writing and it can also help you detect slop.

## What it catches

The patterns it detects include:

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

It also enforces the fundamentals that make writing good: Lead with the point when it helps, use active voice, untangle hard-to-follow sentences, and prefer concrete numbers over abstractions.

## Install

Paste this into Claude Code, Codex, or your favorite AI harness:

"Install this skill globally: [https://github.com/petergyang/no-ai-slop](https://github.com/petergyang/no-ai-slop)"

## Use

The skill has two jobs. Editing is the main one.

**1. Edit a draft.** Paste it and invoke the skill:

```
/no-ai-slop

[your draft]
```

You get back the edited draft plus a short What changed section. The skill makes the minimum effective edit, then checks its own work against [eval.md](eval.md) without requiring separate agents.

**2. Detect slop.** Ask whether a piece reads as AI:

```
/no-ai-slop is this AI slop?

[the text]
```

You get every pattern it found, each with the quoted line and a suggested fix. It doesn't rewrite, score the draft, or guess whether AI wrote it. AI detectors guess. Named patterns are evidence you can check yourself.

## Files

1. `SKILL.md`: The editing rules and workflow. The whole skill.
2. `eval.md`: Pass/fail checks the skill runs on its own edits.
3. `agents/openai.yaml`: Metadata so the skill shows up in app UIs.

## Who made this

I'm [Peter Yang](https://creatoreconomy.so). I led product teams at Roblox, Reddit, and Twitch for 10+ years, and now I teach busy professionals how to become AI builders. This is one skill from my personal AI operating system. The full library, including my courses and workflows, lives at [Behind the Craft](https://behindthecraft.com).

## License

MIT
