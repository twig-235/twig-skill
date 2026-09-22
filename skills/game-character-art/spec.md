# Game character art specification

## Required files

The final character folder contains exactly four files:

- `full.png`: vertical full-body environmental illustration.
- `chat.png`: transparent adult-proportion dialogue cutout from head to just above the knees. Knees, shins, and boots stay outside the canvas.
- `grid.png`: transparent 4 × 4 SD action grid.
- `icon.png`: square head-and-shoulders roster portrait, readable near 100 px.

Do not leave drafts, previews, README files, backups, scripts, or derived animation strips in the character output folder.

## Identity anchor

Record face and eye color, hair shape, outfit layers and palette, signature weapon or accessory, gems, and personality. Preserve these identity anchors across every asset. Choose the full illustration pose and camera separately; do not carry them into the fixed chat, icon, or grid layouts. Change proportions only for the SD grid.

## Art direction

Use the supplied screenshots only as character-art references. Match hand-painted 2D Korean dark-fantasy anime RPG rendering: confident fine linework, appealing angular faces, layered painterly shadows, matte engraved armor, restrained highlights, and smoky gothic atmosphere. Avoid glossy 3D rendering, plastic skin, excess bloom, and photorealism. Never bake UI text, levels, stars, frames, buttons, or selection marks into artwork.

Keep the art style fixed to the official masters and supplied game references for every character and asset. Do not randomize rendering style, brushwork, anatomy language, or realism level. Compare `full.png`, `chat.png`, and `icon.png` side by side at similar face sizes before acceptance. If one is darker, more realistic, or otherwise stylistically different, regenerate it using the matching assets as explicit identity and style references.

For each new character, choose a distinct `full.png` environment from several fitting possibilities based on their role, personality, palette, and story. Vary architecture, weather, time of day, viewpoint, and lighting across characters; do not reuse one fixed backdrop. The environment should support the character and preserve silhouette readability. Keep `chat.png` and `grid.png` transparent. The `icon.png` may have a subtle matching painted background.

## Official style lock

The user-approved masters are `references/official/crimson_swordsman/` and `references/official/moonlight_swordswoman/`. Their four asset types are the authoritative style and proportion references. Verify every file against `references/official-style-lock.json` before use. A changed file is not automatically an approved replacement.

- For `full.png` generation, supply `references/style-only-crimson_swordsman.png` and `references/style-only-moonlight_swordswoman.png` as rendering references alongside a separate target identity image. These boards contain face, armor/material, and paint-detail crops from the hash-locked chat masters. Do not supply the official full-body masters as generation inputs; inspect them only for style QA. For `chat.png`, `icon.png`, and `grid.png`, use the corresponding official asset type as reference. References set rendering and asset proportions, not costume, pose, camera angle, or scenery.
- Keep style, identity, composition/pose, and environment separate in prompts. Style remains fine anime linework, simplified angular facial planes, layered matte painted shading, and restrained highlights. Identity fixes the target's face, hair, costume, palette, and weapon.
- Only an explicit user decision can replace these masters. Male or female martial artist images and recent generations are not official masters.
- Compare `full.png`, `chat.png`, and `icon.png` at equal face sizes, then compare the SD figures at equal standing heights. Judge SD head-to-body proportion without ponytails or accessories. Reject photorealistic drift, stretched anatomy, or a copied master background.

## Natural composition for full.png only

The full environmental illustration may use a front, left, right, three-quarter, or readable side view. The character need not look at the viewer. Before generation, record camera height, viewing direction, action/pose, figure placement, gaze, and environment. Compare the most recent 3-5 full illustrations for staging only, never as style masters; choose a combination that differs from the closest recent image in at least two of camera height, viewing direction, and action/pose. Vary weight shift, torso/head direction, distance, architecture, terrain, weather, light, and time of day. Walking, reading, preparing equipment, resting, leaning, or kneeling are valid when the full figure remains visible. Keep the face readable and leave UI-safe margins. If the user requests a specific composition, honor it. After generation, reject and regenerate an image whose camera height + viewing direction + action/pose repeat a recent image, or whose centered low-angle near-frontal three-quarter hero staging recurs. Changing only the background does not pass.

These pose and camera freedoms do **not** apply to the other assets: `chat.png` keeps the transparent above-knee adult-proportion dialogue cutout; `icon.png` stays a square, face-readable head-and-shoulders portrait; `grid.png` keeps the approved SD proportions, stable orientation, handedness, 4 × 4 action order, cell containment, and foot baseline. Do not transfer the full illustration's experimental camera angle or background into the cutout or sprite sheet.

## Grid order

Each row has four chronological frames from left to right:

1. Idle: stance, breathing or sway, blink, return.
2. Attack: windup, strike, follow-through or effect, recovery.
3. Exploration/work: scan, step, inspect clue or map, signal discovery.
4. Hit: brace, impact, recoil or stagger, recovery.

Keep every sprite, weapon, hair strand, and effect inside its cell. Use transparent gutters, consistent scale, and a stable foot baseline. Temporarily split the grid for validation, then discard derived sheets.

## Workflow

1. Inspect the consuming game's loaders and neighboring assets.
2. Create `full.png` using the style-only crops and the selected composition; compare its actual staging with recent full illustrations and regenerate repeats before approving it as the identity source.
3. Derive the transparent above-knee `chat.png` while keeping adult proportions.
4. Derive the square `icon.png` for small-card legibility.
5. Derive the transparent four-row `grid.png` in SD proportions.
6. Validate dimensions, alpha, edges, anatomy, weapon continuity, identity, grid bounds, and action readability.
