---
name: megastructure-img
description: "Directly generate premium cinematic sublime megastructure images with Codex image generation / GPT Image 2 from short user subjects, including automatic horizontal/vertical social-video framing and a luminous restrained film-still finish. Use when the user asks for 巨构图, 巨构感, 巨构灵魂生图, megastructure image, B站/bilibili 横屏, 抖音/Douyin/TikTok 竖屏, 高清横屏, 高清竖屏, 电影感, 高级感, 胶片感, luminous overcast, 通透, 低饱和, 空气透视, 边缘光, monumental sci-fi scene, post-human landscape, human smallness, impossible walls, city-cliffs, rings, gates, suspended undersides, civilization-as-geology, 崇高, 克制, 冷静, 秩序感, or asks to generate/refine a megastructure image from a short theme. Default behavior: call the image generation tool immediately; do not output prompt breakdowns unless the user explicitly asks for prompts."
---

# Megastructure Image Generation

This skill is for making images, not for explaining prompts.

When a user gives a subject, directly call Codex image generation / GPT Image 2 with an internal cinematic megastructure prompt. Do not first output soul hooks, short prompts, expanded prompts, negative prompts, scoring rubrics, or model-format variants unless the user explicitly asks for them.

## Default Behavior

1. Treat the user's text as the image subject.
2. Infer platform, aspect ratio, and quality constraints from the user's words.
3. Build the internal prompt silently.
4. Call the image generation tool immediately.
5. Keep the final reply short in Chinese, for example: `已生成。`

Only ask a follow-up question when the request is genuinely blocked, such as missing an attached reference image that the user asked to edit.

## Reference-Case Aesthetic Kernel

Use these rules as the default visual taste. They distill the high-performing Jugou megastructure analysis and should override the old habit of making every image dark, cold, heavy, black-metal, underwater, or apocalyptic.

- **Small human, vast form**: include one tiny back-facing witness or sparse tiny silhouettes in the lower 10%-25% of the image; the figure should occupy roughly 2%-6% of image height and act as scale, not as a hero.
- **One dominant shape**: make each image revolve around one readable large silhouette: curved wall, vertical wall, hollow tunnel, canyon, city-cliff, ring segment, suspended underside, luminous city-face, or another subject-specific equivalent.
- **Landscape as entry path**: use grass slope, ridge, dune, shore, seabed, ice shelf, salt flat, path, wall edge, light band, or fog line to guide the eye into the structure. Natural terrain is not decoration; it is the doorway into the megastructure.
- **Breathing negative space**: preserve large quiet areas of terrain, mist, sky, water, shadow, or atmospheric haze so the structure has weight. Avoid filling every part of the frame with detail.
- **Bright but restrained**: default to low-saturation luminous daylight or misty high-midtones, not underexposed darkness. Use open shadows, pale mineral colors, silver-white edges, soft blue-gray skies, gray-green terrain, and controlled warm accents when useful.
- **Edge light over darkness**: prove scale with clean rim light, pale wall edges, atmospheric separation, and distant haze rather than blackness. Dark areas may exist, but they must remain readable and should not dominate by default.
- **Fog as depth, not mud**: use mist, dust, rain, sea spray, or haze to hide the full extent of the structure while keeping foreground and main silhouette legible.
- **Detail density comes from crop**: when the user asks for a reference-like or highly detailed result, move closer instead of only asking for more detail. Let the wall, ring, cliff, gate, or underside fill most of the frame; reduce empty sky; use near-distance crop, base-of-structure viewpoint, or compressed telephoto scale so surface texture receives enough visual area.
- **Multi-scale surface hierarchy**: describe the structure with large silhouette, medium panels/ribs/seams, and fine weathering together. Use erosion streaks, scrape lines, chipped edges, hairline cracks, water stains, panel grids, patch repairs, tiny access slots, ladder traces, and grime near the base when the subject supports engineered mineral surfaces.
- **Repeat a motif mentally**: for single images, imply a world that could support a six-shot sequence: scale shock, breathing space, structure detail, depth path, motif return, unresolved final frame.
- **Do not copy references**: learn composition mechanics and mood; do not reproduce the exact three vertical curved walls, exact grass-slope human placement, exact tunnel with warm side patches, or exact golden city-wall angle.

## Design Philosophy

Generate the sublime, not merely a beautiful large object. Translate these ideas into concrete image language:

- **Scale fracture**: break normal human scale through a tiny witness, small vehicles, window slits, ladders, cables, birds, walkers, boats, or maintenance marks.
- **Safe terror**: the megastructure may feel capable of swallowing the world, but the camera holds a contemplative distance; avoid gore, attack, combat, and disaster climax.
- **Obscurity**: the full structure must remain unknowable through crop, haze, low cloud, bright mist, dust, rain, sea spray, depth, or distance. Do not reveal the whole object cleanly.
- **Negative pleasure**: the senses fail to measure the object while the frame remains calm, ordered, readable, and luminous enough to contemplate.
- **Ego shrinking**: the human figure is not the protagonist; it is a still witness that makes the structure feel impossible.
- **Civilization as geology**: translate architecture into landscape-scale walls, cliffs, dams, rings, tunnels, canyons, terraces, or city-faces that feel partly natural and partly engineered.
- **Quiet order**: prefer simple monumental geometry, restrained surface detail, and clear silhouettes over busy mechanical spectacle.
- **Premium film finish**: make the output feel like a high-end cinema still with controlled contrast, soft highlight roll-off, open shadow detail, subtle grain, atmospheric depth, and disciplined color.

Do not output these philosophy labels to the user. Use them only to build the hidden image prompt.

## Exposure, Color, And Light Guardrails

The default grade should resemble the reference analysis: low saturation, clear midtones, luminous atmosphere, and carefully placed highlights. It should not default to deep night, black metal, crushed shadows, or abyssal darkness unless the user's subject explicitly asks for that.

Always prefer:

- `luminous overcast daylight`, `misty high-midtone atmosphere`, `open shadows with detail`, `soft silver rim light`, `pale mineral color palette`, `clear atmospheric perspective`, `low-saturation daylight film look`
- `controlled contrast`, `soft highlight roll-off`, `preserved highlight detail`, `clean midtone separation`, `subtle 35mm film grain`, `restrained halation around distant lights`
- Directional raking side light for high-detail surfaces: soft light from upper left or upper right, bright rim highlights on edges, open readable recessed shadows, and mist used between forms rather than as a blanket over texture.
- Cool quiet palettes: pale blue-gray, gray-green, silver-white, mineral gray, faded grass green, muted ochre, ash white.
- Warm accents only as narrative targets: distant city glow, edge light, window slits, reflected low sun, or dust-lit wall face.

Avoid by default:

- `low-key`, `nocturne`, `abyssal`, `black metal everywhere`, `dead blue`, `crushed blacks`, `shadow-dominated`, `underexposed`, `dark fantasy`, `apocalyptic gloom`
- Overprocessed HDR, plastic CGI, hyper-sharp digital render, excessive lens flare, teal-orange cliche, muddy blacks, blown highlights, dirty vintage dust, scratches, and decorative color grading.

For explicitly dark subjects, keep darkness readable: preserve shadow detail, keep a visible silhouette edge, and include a luminous atmospheric plane or small narrative light.

## Internal Prompt Rules

Use this visual core:

`tiny witness + one dominant landscape-scale silhouette + luminous restrained atmosphere + atmospheric obscurity + civilization-as-geology + premium film-still finish + quiet post-human order`

Always include:

- The inferred aspect ratio and composition rules from **Aspect And Platform Rules**.
- One tiny back-facing human or sparse tiny silhouettes near the bottom of the frame.
- A ground-level, low-angle, base-of-structure, or edge-of-terrain perspective when possible; avoid top-down drone mastery unless the user explicitly asks for it.
- A natural terrain base: grassland, tundra, shore, seabed, salt flat, desert basin, cliff valley, ice field, ash plain, mountain shadow, or a subject-specific equivalent.
- A megastructure that exceeds normal building scale and cannot fit in the frame.
- Crop, haze, distance, bright mist, weather, water, dust, cloud, or occlusion so the full structure is impossible to see.
- One clear main shape with restrained secondary details.
- A visible path, ridge, slope, shoreline, wall edge, light band, fog line, or repeated arc that guides the eye.
- When the user references an image with strong texture or says the previous output needs more detail, bias toward close monumental crop: little or no open sky, the structure filling roughly the upper two-thirds or more of the frame, the terrain compressed against the base, and the witness still tiny. Avoid wide scenic distance unless the user explicitly wants a panorama.
- For engineered stone, concrete, metal, or mineral megastructures, include multi-scale material language: dominant silhouette, ribs or buttresses, panel seams, long weathering streaks, fine parallel scratches, chipped edges, cracks, stains, patch repairs, tiny maintenance marks, and base grime. Make the surface tactile, imperfect, and readable rather than smooth CGI.
- Calm order and restraint: simple readable geometry, sparse details, low saturation, controlled light.
- High-end cinematic finish: luminous daylight or motivated low light, soft highlight roll-off, open shadow detail, subtle 35mm grain, restrained halation, atmospheric depth, clean filmic texture.
- Quiet, non-heroic mood: no battle, no triumph, no poster spectacle.
- Strong no-text constraints: no text, logo, watermark, UI, typography, signature, readable signs.

Avoid:

- Explaining the prompt to the user before generation.
- Returning multiple prompt sections by default.
- Making a normal pretty landscape, tourist photo, hero poster, fantasy battle, action scene, close-up creature portrait, or warm decorative architecture.
- Letting the subject become merely a large object; it must feel like a world-scale force.
- Fully revealing the entire structure in a clean explanatory view; total legibility weakens the sublime effect.
- Solving scale only by making the image dark. Use light, haze, crop, negative space, and human-scale anchors instead.

## Aspect And Platform Rules

Infer output framing silently:

- If the user says **横屏**, **宽屏**, **16:9**, **B站**, **bilibili**, **YouTube**, or **8K 横屏**, generate horizontal **16:9**.
- If the user says **竖屏**, **9:16**, **抖音**, **Douyin**, **TikTok**, **快手**, **小红书**, or **手机壁纸**, generate vertical **9:16**.
- If the user explicitly gives both platform and orientation, the explicit orientation wins. Example: `B站竖屏` means vertical 9:16.
- If no platform or orientation is given, default to vertical **9:16**.

Use platform-aware composition:

- **Horizontal 16:9 / B站 / bilibili**: make a wide cinematic panorama, strong horizon, terrain depth, mountain/city/sky scale across the frame, tiny witness in the lower third, high-detail texture, compression-friendly clean silhouettes. Add: `horizontal 16:9, widescreen cinematic panorama, Bilibili-style high-definition scenic scale, luminous low-saturation film look, no subtitles, no logo, no watermark, no UI`.
- **Vertical 9:16 / 抖音 / Douyin / TikTok / 小红书**: make a tall upward composition, tiny witness at the bottom, megastructure rising vertically or blocking the sky, strong top-to-bottom depth, phone-screen readable silhouette. For reference-like high-detail vertical images, prefer near-distance crop with the structure filling most of the upper frame and only minimal sky. Add: `vertical 9:16, mobile short-video cover composition, high-definition vertical poster frame, luminous restrained atmosphere, no captions, no stickers, no app UI, no watermark`.
- **高清 / 4K / 8K**: add high-detail texture, crisp atmospheric perspective, soft highlight roll-off, open shadow detail, clean edges, subtle natural film grain. Do not claim actual pixel resolution in the final reply.

## Route Selection

Pick one dominant emotional route internally:

- **Boundary**: walls, gates, cliffs, dams, quarantine edges, world edge.
- **Pilgrimage**: exhausted walkers, long path, distant city-wall, quiet approach.
- **Unreturnable Home**: faint windows, dead domestic scale, abandoned housing/city/school.
- **Cosmic Indifference**: rings, suspended undersides, orbital fragments, gods, aliens, planets, aurora, solar flare, deep time.
- **Monumental Order**: brutalist grids, windowless facades, state-scale temples, factories, archives, vaults, cold institutional geometry.
- **Luminous Relic**: pale curved walls, silver edge light, grass/shore/ice breathing space, quiet fog, and an unresolved sense of ancient engineering.

When in doubt, choose the route that best turns the subject into a force larger than human life, not a character or a prop.

## Subject Translation Notes

- For **grassland / Inner Mongolia / desert / tundra**: default to wind-shaped terrain, small witness, pale wall edges, and luminous atmospheric distance. Use open sky for broad pilgrimage/panorama scenes; for reference-like detail requests, reduce sky and press the terrain against a close cropped wall or ring base. Avoid neon cyberpunk unless explicitly requested.
- For **ocean / underwater**: do not default to abyssal black. Prefer luminous shallow-sea shelf, blue-green water columns, sun shafts, readable silhouettes, suspended particles, and a giant submerged wall/ring/city-cliff fading into depth.
- For **golden / sacred / pilgrimage**: use warm light as a focused narrative target inside a cool environment, not as a full-frame yellow filter.
- For **alien civilization**: make the logic non-human through shape, scale, crop, and repetition; avoid monsters, battles, or readable sci-fi UI.
- For **dark / night / underground**: keep the frame legible with open shadows, visible edges, and motivated small lights.

## Internal Prompt Shape

Write the image prompt as one polished natural-language block for GPT Image 2:

```text
Create a cinematic sublime megastructure image, [inferred aspect and platform constraints]. Subject: [subject].
Visual thesis: [one sentence about human smallness, a single overwhelming form, and calm scale fracture].
Composition: [horizontal panorama or vertical tower framing], low/base/ground-level viewpoint when possible, one tiny non-heroic witness near the bottom/lower third, vast [terrain], one impossible [structure] dominating the sky/horizon, cropped by the frame and disappearing into haze/cloud/mist/dust/water/distance. For high-detail reference-like outputs, use near-distance monumental crop, minimal sky, compressed scale, wall/structure surfaces occupying most of the frame, and terrain pressed against the base.
Reference-case composition logic: one dominant readable silhouette, large breathing negative space, tiny witness scale, natural terrain as an entry path, close crop when detail matters, edge light and atmospheric perspective instead of underexposed darkness.
Details: [subject-specific terrain, material, scale proof, weather, obscurity, body anchor, restrained light, low-saturation palette]. For engineered mineral surfaces, layer large ribs/buttresses/panels with fine erosion streaks, scrape lines, chipped edges, cracks, stains, patch repairs, tiny maintenance marks, ladder-like traces, and base grime; use raking side light so the texture reads.
Cinematic finish: premium cinema still quality, luminous restrained film look, controlled contrast, soft highlight roll-off, preserved highlights, open shadow detail, clear midtone separation, subtle 35mm film grain, restrained halation around distant lights, volumetric haze, precise atmospheric perspective, clean filmic texture.
Mood: quiet post-human silence, sublime loneliness, controlled order, contemplative distance, restrained filmic realism.
Negative constraints: no text, captions, subtitles, logo, watermark, UI, app interface, typography, readable signs, hero pose, battle, crowd spectacle, oversaturated colors, warm decorative beauty, fully explained clean blueprint view, underexposed darkness by default, overprocessed HDR, plastic CGI, excessive lens flare, teal-orange cliche, muddy blacks, crushed shadows, blown highlights, oversharpened digital render.
```

Read [references/prompt-patterns.md](references/prompt-patterns.md) only when the subject needs extra structure, stronger visual routes, deeper sublime logic, cinematic look presets, video/BGM extension language, or failure fixes.
