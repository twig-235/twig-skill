# twig-skill

Personal AI skills for game development, maintained for OpenAI/Codex, Claude, and Grok.

## Skills

### [Game Character Art](skills/game-character-art/spec.md)

Creates a consistent character asset set containing `full.png`, `chat.png`, `grid.png`, and `icon.png`.

- [OpenAI / Codex adapter](skills/game-character-art/providers/openai/SKILL.md)
- [Claude adapter](skills/game-character-art/providers/claude/SKILL.md)
- [Grok adapter](skills/game-character-art/providers/grok/SKILL.md)
- [Prompt scaffolds](skills/game-character-art/prompts/assets.md)

#### Samples

| Moonlight swordswoman | Crimson swordsman |
| --- | --- |
| [![Moonlight swordswoman](examples/game-character-art/moonlight-swordswoman.webp)](examples/game-character-art/moonlight-swordswoman.webp) | [![Crimson swordsman](examples/game-character-art/crimson-swordsman.webp)](examples/game-character-art/crimson-swordsman.webp) |

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
