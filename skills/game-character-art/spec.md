# Game character art specification

## Required files

The final character folder contains exactly four files:

- `full.png`: vertical full-body environmental illustration.
- `chat.png`: transparent adult-proportion dialogue cutout from head to just above the knees. Knees, shins, and boots stay outside the canvas.
- `grid.png`: transparent 4 × 4 SD action grid.
- `icon.png`: square head-and-shoulders roster portrait, readable near 100 px.

Do not leave drafts, previews, README files, backups, scripts, or derived animation strips in the character output folder.

## Identity anchor

Record face and eye color, hair shape, outfit layers and palette, signature weapon or accessory, gems, personality, and pose. Preserve them across every asset. Change proportions only for the SD grid.

## Art direction

Use the supplied screenshots only as character-art references. Match hand-painted 2D Korean dark-fantasy anime RPG rendering: confident fine linework, appealing angular faces, layered painterly shadows, matte engraved armor, restrained highlights, and smoky gothic atmosphere. Avoid glossy 3D rendering, plastic skin, excess bloom, and photorealism. Never bake UI text, levels, stars, frames, buttons, or selection marks into artwork.

Keep the art style fixed to the supplied game references for every character and asset. Do not randomize rendering style, brushwork, anatomy language, or realism level. Compare `full.png`, `chat.png`, and `icon.png` side by side at similar face sizes before acceptance. If one is darker, more realistic, or otherwise stylistically different, regenerate it using the matching assets as explicit identity and style references.

For each new character, choose a distinct `full.png` environment from several fitting possibilities based on their role, personality, palette, and story. Vary architecture, weather, time of day, viewpoint, and lighting across characters; do not reuse one fixed backdrop. The environment should support the character and preserve silhouette readability. Keep `chat.png` and `grid.png` transparent. The `icon.png` may have a subtle matching painted background.

## Grid order

Each row has four chronological frames from left to right:

1. Idle: stance, breathing or sway, blink, return.
2. Attack: windup, strike, follow-through or effect, recovery.
3. Exploration/work: scan, step, inspect clue or map, signal discovery.
4. Hit: brace, impact, recoil or stagger, recovery.

Keep every sprite, weapon, hair strand, and effect inside its cell. Use transparent gutters, consistent scale, and a stable foot baseline. Temporarily split the grid for validation, then discard derived sheets.

## Workflow

1. Inspect the consuming game's loaders and neighboring assets.
2. Create and approve `full.png` as the identity source.
3. Derive the transparent above-knee `chat.png` while keeping adult proportions.
4. Derive the square `icon.png` for small-card legibility.
5. Derive the transparent four-row `grid.png` in SD proportions.
6. Validate dimensions, alpha, edges, anatomy, weapon continuity, identity, grid bounds, and action readability.
