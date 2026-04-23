# ChatGPT Images Prompt Pack

## Purpose

This file is the direct-use prompt pack for the first 10-image opening batch of `Sable Archive`.

## Current Tool Decision

The current primary image-generation tool is `ChatGPT Images`.

## Practical Ratio Rules

ChatGPT Images on web/app supports aspect ratio selection in the UI.
For this project, use these practical defaults:

- avatar and object assets: `1:1`
- character portraits: `4:5`
- scene and header assets: `16:9`

If the workflow later moves to API-based generation, the closest practical export sizes are:

- `1024x1024` for `1:1`
- `1024x1536` for vertical portrait work
- `1536x1024` for horizontal scene work

## Global Negative Prompt

Use this whenever a negative prompt field is available:

```text
explicit nudity, pornographic, modern fashion, neon cyberpunk, cheap fantasy armor, game splash art, generic ai art, plastic skin, immature face, anime, cartoon, text, watermark, glossy 3d logo, cluttered background, random jewelry overload
```

## Prompt Table

| ID | Asset Type | Recommended Ratio | Continuity Type | Depends On | Reference Upload | Prompt |
|---|---|---|---|---|---|---|
| `SA-S1-001` | Character | `4:5` | `new anchor` | `none` | `no` | `Sable Archive, Season One, The Court of Perfume and Dust, The Favored One, adult woman, quiet and dangerous, knowing gaze, half-turned toward the viewer, hand touching a translucent veil, black-and-gold silk, fine metallic ornaments, moonlit skin, carved arch shadows, incense haze, restrained luxury, strong sexual tension but non-explicit, cinematic medium close-up, highly authored, high detail` |
| `SA-S1-002` | Character | `4:5` | `same character` | `SA-S1-001` | `yes, strongly recommended` | `Sable Archive, Season One, The Court of Perfume and Dust, The Favored One, same woman as SA-S1-001, adult woman, seated on a low stone divan, one knee raised, barefoot, veil slipping from one shoulder, calm authority, dangerous softness, black-and-gold fabric, lantern glow and moonlight, incense smoke, carved interior, cinematic three-quarter portrait, non-explicit sensuality, clear character continuity` |
| `SA-S1-003` | Character | `4:5` | `new anchor` | `none` | `no` | `Sable Archive, Season One, The Court of Perfume and Dust, The Veiled Diplomat, adult woman, cold intelligence, elegant distance, unreadable expression, standing in profile beneath a high arch, layered dark veils, restrained gold accents, sealed document in hand, severe beauty, political presence, moonlit black-and-gold atmosphere, cinematic half-body portrait, minimal but expensive adornment` |
| `SA-S1-004` | Character | `4:5` | `same character` | `SA-S1-003` | `yes, strongly recommended` | `Sable Archive, Season One, The Court of Perfume and Dust, The Veiled Diplomat, same woman as SA-S1-003, adult woman, turning away after reading a private message, lowered gaze, hand gathering her veil, controlled tension, strategic mind, dark silk layers, carved corridor, gold lamps, cool emotional tone, cinematic mid-shot, highly restrained, exact character continuity` |
| `SA-S1-005` | Character | `4:5` | `new anchor` | `none` | `no` | `Sable Archive, Season One, The Court of Perfume and Dust, The Desert Huntress, adult woman, predatory grace, powerful body language, lean dangerous silhouette, standing against moonlit dunes near a ruined ceremonial gate, wind moving dark layered garments, sharp desert jewelry, hunter's stillness, watchful gaze, black bronze and muted gold palette, cinematic full-body portrait, non-explicit, unmistakably dangerous` |
| `SA-S1-006` | Character | `4:5` | `same character` | `SA-S1-005` | `yes, strongly recommended` | `Sable Archive, Season One, The Court of Perfume and Dust, The Desert Huntress, same woman as SA-S1-005, adult woman, low poised stance on stone steps, turning her head back toward the viewer, veil moving in the wind, hand near a ceremonial blade or chain ornament, wild sensuality under strict control, moonlit dust, torchlight, carved shadows, cinematic medium shot, exact character continuity` |
| `SA-S1-007` | Scene | `16:9` | `independent scene` | `none` | `no` | `Sable Archive, Season One, The Court of Perfume and Dust, exterior of the imperial archive at night, vast desert court architecture, towering carved arches, distant domes, moon above drifting sand, black sky, bronze lanterns, incense smoke from braziers, empty ceremonial road leading inward, luxurious but severe, no characters, strong negative space, cinematic wide shot, black-and-gold atmosphere` |
| `SA-S1-008` | Scene | `16:9` | `independent scene` | `none` | `no` | `Sable Archive, Season One, The Court of Perfume and Dust, interior ceremonial terrace overlooking the desert, polished stone floor with subtle sigil patterns, high arches, hanging lamps, incense haze, moonlit horizon, private ritual and political seduction atmosphere, no characters, medium-wide cinematic composition, elegant central staging area, black-and-gold luxury, quiet danger` |
| `SA-S1-009` | Object | `1:1` | `symbol continuity` | `avatar emblem language` | `optional` | `Sable Archive, Season One, The Court of Perfume and Dust, imperial seal key relic, black-and-gold ceremonial object, part signet and part key, engraved crescent and eye motifs, resting on dark stone under a narrow beam of moonlight, faint incense smoke, precious and ominous, close-up still life, exquisite material detail, symbolic design tied to the archive identity` |
| `SA-S1-010` | Object | `1:1` | `object continuity` | `realm material language` | `optional` | `Sable Archive, Season One, The Court of Perfume and Dust, noble woman's ritual incense vessel and veil ornament, dark silk, gold chain details, smoke curling upward, intimate still life composition, soft luxury with hidden danger, tactile materials, black-and-gold palette, low moonlight and warm ember glow, no human figure, cinematic close-up, elegant and memorable` |

## Continuity Labels

- `new anchor`: this image establishes the base identity for a recurring character
- `same character`: this image must stay visually consistent with the dependency asset
- `independent scene`: no character continuity required
- `symbol continuity`: should echo the emblem and archive symbol system
- `object continuity`: should match the realm's material and ceremonial language

## Continuity Reminder

For these prompts, the most continuity-sensitive assets are:

- `SA-S1-002` should reference `SA-S1-001`
- `SA-S1-004` should reference `SA-S1-003`
- `SA-S1-006` should reference `SA-S1-005`

When possible in ChatGPT Images:

- upload the earlier image
- ask for "same woman" continuity
- keep wardrobe language and emotional temperature stable

## Lowest-Friction Workflow

1. choose the ratio in ChatGPT Images
2. paste the prompt
3. check the `Continuity Type`, `Depends On`, and `Reference Upload` columns before generating
4. if required, add the previous approved image for continuity-sensitive prompts
5. generate 4 to 8 options
6. keep only the most authored result
