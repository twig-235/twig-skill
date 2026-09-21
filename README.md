# twig-skill

Personal AI skills for game development, maintained for OpenAI/Codex, Claude, and Grok.

## Skills

- `game-character-art`: creates a consistent `full.png`, `chat.png`, `grid.png`, and `icon.png` character set.

## Layout

Each skill keeps provider-independent requirements in `spec.md`, reusable visual references under `references/`, and provider adapters under `providers/`.

```text
skills/<skill>/
├─ spec.md
├─ references/
├─ prompts/
└─ providers/
   ├─ openai/SKILL.md
   ├─ claude/SKILL.md
   └─ grok/SKILL.md
```

Install or link the provider directory required by the AI environment together with the skill's `spec.md`, prompts, and references. Generated game assets belong in the consuming game repository and are excluded here.
