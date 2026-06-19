---
name: megastructure-img
description: "Directly generate cinematic megastructure images with Codex image generation / GPT Image 2 from short user subjects, including automatic horizontal/vertical social-video framing. Use when the user asks for 巨构图, 巨构感, 巨构灵魂生图, megastructure image, B站/bilibili 横屏, 抖音/Douyin/TikTok 竖屏, 高清横屏, 高清竖屏, monumental sci-fi scene, post-apocalyptic scale, human smallness, cosmic indifference, impossible walls, city-cliffs, rings, gates, suspended undersides, civilization-as-geology, or asks to generate/refine a megastructure image from a short theme. Default behavior: call the image generation tool immediately; do not output prompt breakdowns unless the user explicitly asks for prompts."
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

## Internal Prompt Rules

Use this visual core:

`human smallness crushed by scale + sublime terrain + post-human silence + cropped landscape-scale structure`

Always include:

- The inferred aspect ratio and composition rules from **Aspect And Platform Rules**.
- One tiny back-facing human or sparse tiny silhouettes near the bottom of the frame.
- A natural terrain base: ice field, salt flat, tundra, sea, cliff valley, desert basin, ash plain, mountain shadow, or similar.
- A megastructure that exceeds normal building scale and cannot fit in the frame.
- Crop, haze, distance, or occlusion so the full structure is impossible to see.
- Quiet, non-heroic mood: no battle, no triumph, no poster spectacle.
- Strong no-text constraints: no text, logo, watermark, UI, typography, signature, readable signs.

Avoid:

- Explaining the prompt to the user before generation.
- Returning multiple prompt sections by default.
- Making a normal pretty landscape, tourist photo, hero poster, fantasy battle, action scene, or close-up creature portrait.
- Letting the subject become merely a large object; it must feel like a world-scale force.

## Aspect And Platform Rules

Infer output framing silently:

- If the user says **横屏**, **宽屏**, **16:9**, **B站**, **bilibili**, **YouTube**, or **8K 横屏**, generate horizontal **16:9**.
- If the user says **竖屏**, **9:16**, **抖音**, **Douyin**, **TikTok**, **快手**, **小红书**, or **手机壁纸**, generate vertical **9:16**.
- If the user explicitly gives both platform and orientation, the explicit orientation wins. Example: `B站竖屏` means vertical 9:16.
- If no platform or orientation is given, default to vertical **9:16**.

Use platform-aware composition:

- **Horizontal 16:9 / B站 / bilibili**: make a wide cinematic panorama, strong horizon, terrain depth, mountain/city/sky scale across the frame, tiny witness in the lower third, high-detail 8K-style texture, compression-friendly clean silhouettes. Add: `horizontal 16:9, widescreen cinematic panorama, Bilibili-style high-definition 8K scenic scale, no subtitles, no logo, no watermark, no UI`.
- **Vertical 9:16 / 抖音 / Douyin / TikTok / 小红书**: make a tall upward composition, tiny witness at the bottom, megastructure rising vertically or blocking the sky, strong top-to-bottom depth, phone-screen readable silhouette. Add: `vertical 9:16, mobile short-video cover composition, high-definition vertical poster frame, no captions, no stickers, no app UI, no watermark`.
- **高清 / 4K / 8K**: add high-detail texture, crisp atmospheric perspective, cinematic HDR, clean edges, natural film grain. Do not claim actual pixel resolution in the final reply.

## Route Selection

Pick one dominant emotional route internally:

- **Boundary**: walls, gates, cliffs, dams, world edge.
- **Pilgrimage**: exhausted walkers, long path, distant city-wall.
- **Unreturnable Home**: faint windows, dead domestic scale, abandoned housing/city/school.
- **Cosmic Indifference**: rings, suspended undersides, orbital fragments, gods, aliens, planets, aurora, solar flare, deep time.

## Internal Prompt Shape

Write the image prompt as one polished natural-language block for GPT Image 2:

```text
Create a cinematic megastructure image, [inferred aspect and platform constraints]. Subject: [subject].
Visual thesis: [one sentence about human smallness and scale].
Composition: [horizontal panorama or vertical tower framing], one tiny non-heroic witness near the bottom/lower third, vast [terrain], impossible [structure] dominating the sky/horizon, cropped by the frame and disappearing into haze.
Details: [materials, terrain, weather, scale proof, body anchor, light, palette].
Mood: quiet post-human silence, sublime loneliness, cosmic indifference, restrained filmic realism.
Negative constraints: no text, captions, subtitles, logo, watermark, UI, app interface, typography, readable signs, hero pose, battle, crowd spectacle, oversaturated colors.
```

Read [references/prompt-patterns.md](references/prompt-patterns.md) only when the subject needs extra structure, stronger visual routes, or failure fixes.
