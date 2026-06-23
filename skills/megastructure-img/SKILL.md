---
name: megastructure-img
description: "Directly generate premium cinematic sublime megastructure images with Codex image generation / GPT Image 2 from short user subjects, including automatic horizontal/vertical social-video framing, luminous restrained film-still finish, and route-based subject translation. Use when the user asks for 巨构图, 巨构感, 巨构灵魂生图, 末日废土, 旧世界遗迹, 梦核巨构, dreamcore megastructure, 外星文明, 泰坦文明, alien/titan relic, megastructure image, B站/bilibili 横屏, 抖音/Douyin/TikTok 竖屏, 高清横屏, 高清竖屏, 电影感, 高级感, 胶片感, luminous overcast, 通透, 低饱和, 空气透视, 边缘光, monumental sci-fi scene, post-human landscape, human smallness, impossible walls, city-cliffs, rings, gates, suspended undersides, civilization-as-geology, 崇高, 克制, 冷静, 秩序感, or asks to generate/refine a megastructure image from a short theme. Default behavior: call the image generation tool immediately; do not output prompt breakdowns unless the user explicitly asks for prompts."
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

## Publishing Title Assistant

This is an auxiliary output system for publishing, not a reason to put words inside the image.

Default image generation must keep the image clean: no title, no Chinese text, no captions, no logo, no watermark, no typography. Megastructure images should feel like an unknown film still or recovered world fragment. Text belongs outside the image unless the user explicitly asks for a designed cover/poster.

When the user asks for **发布**, **标题**, **文案**, **简介**, **B站投稿**, **抖音发布**, **小红书图文**, **封面方案**, **一组图**, **组图**, **系列**, **选题**, or similar publishing help, generate the image(s) first and then add a concise Chinese publishing package.

Important usage pattern: users often want **one group of images around one theme**, not one isolated image. Treat `一组图 / 组图 / 系列图 / 一套图` as one unified theme with several visual variations. Keep the whole group under one core theme, one emotional route, and one publication title system unless the user explicitly asks for multiple unrelated topics.

### Output Modes

- **Image-only mode**: default. Generate the image and reply briefly, e.g. `已生成。`
- **Publishing mode**: image plus one primary title, one short description, tags, and optional alternate titles.
- **Series/group mode**: several images or visual directions under one theme, plus one group title and per-image subtitles when useful.
- **Cover/poster mode**: only if explicitly requested. Generate a clean no-text base image first when possible, then suggest external typography placement and copy. Do not ask the image model to render Chinese text by default because it often creates artifacts.

### Publishing Package Shape

Use this compact shape when the user requests publishing support:

```text
标题：巨构：[short poetic title]

简介：
[one or two short lines that imply a world, not a plot explanation]

标签：
#巨构 #AI绘画 #砼核 #科幻美学 [platform/topic tags]

备用标题：
1. 巨构：[alternate]
2. 巨构：[alternate]
3. 巨构：[alternate]
```

For a group of images, use one group theme plus per-image subtitles:

```text
组图主题：雪原尽头的巨型城市墙
组图标题：巨构：雪原尽头没有回声

1. 巨构：墙外没有回声
2. 巨构：白昼停在这里
3. 巨构：最后的道路
4. 巨构：不可进入之城
```

### Title Taste Rules

Good megastructure titles are short, poetic, and unresolved. They should make viewers feel there is a world behind the image without explaining it.

Prefer:

- `巨构：没有告别`
- `巨构：永恒的沉默`
- `巨构：钢铁草原`
- `巨构：白昼的边界`
- `巨构：神明离开后的大厅`

Avoid:

- Tool-forward titles: `AI巨构8K壁纸第12期`, `Midjourney提示词分享`, `GPT生成巨构图`.
- Over-explained titles: `一个人在雪原上看见巨大城市墙的科幻图片`.
- Cheap hype: `震撼全网`, `顶级大片`, `史诗级神图`, `视觉炸裂`.
- Full plot summaries. Keep the mystery.

Use title routes that match the visual route:

- **Boundary / wall / gate**: `白昼的边界`, `墙外没有回声`, `天空从这里断开`, `不可进入之地`, `世界尽头的门`.
- **Pilgrimage / witness**: `无人回应的朝圣`, `最后的目击者`, `我们只是短暂路过`, `他站在尺度之外`.
- **Unreturnable home / dead city**: `他们曾经住在这里`, `城市忘记了人的形状`, `没有人回来的街区`, `旧日住宅层`.
- **Monumental order / concretecore**: `沉默的混凝土`, `秩序没有温度`, `巨人的中枢`, `冷白色的神殿`.
- **Nature swallowed by structure**: `冰原之下`, `海是一面镜子`, `风穿过旧神的骨架`, `草原停止生长的地方`.
- **Sacred / golden / light**: `烈日永照的黄金乡`, `光之窒息`, `圣城没有入口`, `太阳被困在墙里`.

### Description Taste Rules

Descriptions should be one or two quiet lines. Write like a recovered caption, not marketing copy.

Examples:

```text
所有道路都停在这里。
墙没有门，也没有等待谁回来。
```

```text
造物主早就离开了。
只剩风，还在替它守夜。
```

```text
草原继续向前生长。
直到它碰见一堵没有名字的墙。
```

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

## Core Route System

This skill is a single mega-skill with route-based subject translation. Do not split these routes into separate skills unless a route becomes useful outside the megastructure premise.

Default route selection should be silent. The user gives a short subject; the skill chooses the strongest route, then builds one coherent image prompt. A route is not a style label. It is a psychological mechanism that explains why the image feels sublime.

### Route 1: Wasteland Relic / 末日废土旧世界遗迹

Use when the subject mentions 末日, 废土, 旧世界, 荒原, 遗迹, 断桥, 水坝, 干涸海床, 废弃机场, 废弃太空港, ruined infrastructure, post-apocalyptic world, dead civilization, or survivor-scale remains.

Core mechanism: the old world is dead, but its infrastructure remains too large for the present. The image should not be about survival action; it should be about a tiny witness standing under the leftover scale of a civilization that no longer answers.

Visual grammar:

- One dominant old-world structure: broken dam, severed bridge, exposed subway spine, collapsed orbital elevator, dead airport terminal, desert shipyard, rusted launch ring, highway canyon, dry reservoir wall, or abandoned arcology.
- Entry terrain: ash plain, cracked salt flat, dry basin, wind-shaped dust road, dead grassland, pale desert, or exposed seabed leading the eye toward the relic.
- Scale witness: one tiny back-facing survivor, a small vehicle, a broken camp, distant walkers, birds, or animals. The witness is a measuring device, not an action hero.
- Materials: concrete, weathered steel, eroded asphalt, dust-packed seams, rust scars, collapsed spans, exposed rebar, sand-stained walls, dead cables, and scale scars.
- Light: readable daylight, pale dust, silver edge light, open shadows, restrained amber only as late sun or small distant signal.

Avoid: zombies, guns, chase scenes, explosions, red apocalypse skies, Mad Max cosplay, gas-mask portraits, generic rubble piles, heroic survivor posters, and full destruction spectacle.

Example subjects:

- `末日废土，干涸海床里的旧世界水坝`
- `荒原尽头的废弃太空港`
- `旧高速公路像峡谷一样断在白色城市墙前`

### Route 2: Dreamcore Megastructure / 梦核巨构

Use when the subject mentions 梦核, 梦核巨构, 梦境巨构, dreamcore, dreamcore megastructure, impossible rooms, soft unreality, childhood memory, cloud streets, floating cities, or non-logical but emotionally vivid spaces. Treat older/looser phrases such as 奇妙梦境 or 梦境 as aliases for this dreamcore-megastructure route, not as cheerful fairy-tale or healing fantasy.

Core mechanism: the world is not scary because it is hostile; it is unforgettable because spatial logic has quietly softened or failed. This is dreamcore sublime: familiar spaces feel beautiful, empty, slightly uncanny, and too large to measure. The viewer recognizes ordinary places, but their scale, continuity, season, gravity, or adjacency is wrong.

Visual grammar:

- One dominant dreamcore form: sky staircase, cloud street, water-filled classroom, bedroom window opening onto a city-cliff, floating apartment slab, giant white door in a field, endless playground structure, impossible station, or road passing through multiple seasons.
- Familiar anchor: school corridor, residential window, bed, streetlight, stair, train platform, playground, mall atrium, rain puddle, cloud, sea, or sunset field.
- Abnormal deviation: gravity tilts, rooms open into sky, distant buildings are too large, seasons overlap, reflections become architecture, doors lead nowhere, or scale changes without explanation.
- Palette: can be more colorful than the default skill, but still restrained and filmic. Prefer milky daylight, dusk gradients, soft blue, pale peach, muted cyan, washed yellow, and clean air over candy saturation.
- Scale witness: one tiny childlike or adult silhouette, a small bicycle, a lone bed, a distant train, or a tiny figure at the edge of the impossible space.
- Mood: controlled dreamcore unease, quiet wonder, lucid childhood-memory distance, empty but breathable space. It may feel lonely or uncanny, but should not become horror, dystopian punishment, or a therapeutic cute dream.

Avoid: cute fantasy, candyland, cheerful healing-dream imagery, AI collage weirdness, cheap backrooms repetition, horror monsters, meme weirdcore eyes, random floating objects, overly saturated cartoon color, decorative surrealism with no dominant form, and full-frame oppressive gloom that hides the spatial idea.

Example subjects:

- `梦核巨构，云上的街道通向巨大的白色门`
- `梦里学校走廊尽头是一片海`
- `黄昏 playground 后面升起一座不该存在的城市墙`

### Route 3: Titan Alien Relic / 外星泰坦文明遗迹

Use when the subject mentions 外星文明, 泰坦文明, 星际文明, alien megastructure, Titan relic, Dyson sphere, ancient spacefaring civilization, non-human ruins, star-scale engineering, orbital shell, or planetary machine.

Core mechanism: human rules do not apply. The structure should feel older, larger, and less interested in humans than any human architecture. The tiny witness is not a conqueror or explorer hero; it is a late insect arriving after the civilization has already stopped explaining itself.

Visual grammar:

- One dominant non-human form: planet-surface gate, orbital shell fragment, star-harvesting ring, titan rib-canyon, black monolith field, cloud-buried dock, ice-moon signal tower, impossible arcology, suspended underside blocking the sky, or non-Euclidean city-cliff.
- Entry terrain: alien desert, basalt plain, ice moon, methane shore, cloud sea, red dust valley, obsidian crater, luminous mineral field, or derelict landing zone.
- Scale witness: tiny astronaut, rover, probe, expedition camp, ship silhouette, small human team, or dust-like birds/particles when humans are absent.
- Materials: not shiny generic sci-fi. Use matte mineral surfaces, pale ceramic stone, oxidized alien alloys, basalt, non-human panel repetition, impossible seams, erosion, star-burn scars, and unlabelled maintenance-scale marks.
- Light: cold stellar light, eclipsed sun, aurora wall, luminous atmospheric haze, bright planetary rim, or restrained gold/white energy as structure, not decoration.

Avoid: blue-purple crystal cities, generic spaceship concept art, laser battles, crowds, readable sci-fi UI, heroic astronauts, alien monster portraits, fantasy temples with aliens pasted on, and fully explained clean blueprint views.

Example subjects:

- `外星泰坦文明，冰卫星地平线上的巨型信号塔`
- `星球表面露出一截环绕恒星的古老结构`
- `人类探险队站在非欧几何黑色方碑群前`

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
- A silent route choice from **Core Route System** or **Route Selection**; translate the subject through the route's psychological mechanism rather than listing style words.
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

- **Wasteland Relic**: old-world infrastructure, dead highways, dry reservoirs, broken dams, abandoned airports, launch rings, ruined arcologies, and survivor-scale remains. Keep it quiet and structural, not zombie/action apocalypse.
- **Dreamcore Megastructure**: familiar places become spatially impossible through softened dreamcore logic: cloud streets, impossible schools, water-filled rooms, floating apartments, endless playgrounds, giant doors, and mismatched seasons. Keep it empty, vivid, uncanny, and restrained; not candy fantasy, cute healing dream, or random weirdcore collage.
- **Titan Alien Relic**: non-human civilization remains, orbital shells, star-scale rings, ice-moon towers, alien gates, basalt plains, and impossible geometry. Keep humans small and late, not heroic explorers or generic spaceship art.
- **Boundary**: walls, gates, cliffs, dams, quarantine edges, world edge.
- **Pilgrimage**: exhausted walkers, long path, distant city-wall, quiet approach.
- **Unreturnable Home**: faint windows, dead domestic scale, abandoned housing/city/school.
- **Cosmic Indifference**: rings, suspended undersides, orbital fragments, gods, aliens, planets, aurora, solar flare, deep time.
- **Monumental Order**: brutalist grids, windowless facades, state-scale temples, factories, archives, vaults, cold institutional geometry.
- **Luminous Relic**: pale curved walls, silver edge light, grass/shore/ice breathing space, quiet fog, and an unresolved sense of ancient engineering.

When in doubt, choose the route that best turns the subject into a force larger than human life, not a character or a prop.

## Subject Translation Notes

- For **末日 / 废土 / 旧世界遗迹 / wasteland**: do not make a survival action poster. Turn the subject into a silent old-world relic whose original function is dead but whose scale still dominates the present: dry reservoirs, broken dams, dead airports, highway canyons, launch rings, exposed subway spines, rusted shipyards, or ruined arcologies. Use pale dust, readable daylight, tiny witnesses, and one dominant ruin silhouette; avoid zombies, guns, red skies, explosions, and generic rubble.
- For **梦核 / 梦境巨构 / dreamcore / dreamcore megastructure**: do not make cheerful fairy-tale fantasy or random weird collage. Start from one recognizable space, then make one spatial rule fail: a school corridor opens onto the sea, a cloud street reaches a giant white door, a bedroom window faces a city-cliff, or a playground becomes an impossible structure. Keep one dominant form, one tiny witness, soft but disciplined color, readable luminous air, and controlled dreamcore unease.
- For **外星文明 / 泰坦文明 / alien / titan / Dyson / 星际文明**: do not make generic spaceship concept art or crystal fantasy cities. Translate the subject into non-human relic scale: orbital shell fragments, ice-moon signal towers, star-harvesting rings, basalt gate fields, cloud-buried docks, suspended undersides, or impossible city-cliffs. Use tiny probes/astronauts/camps only as scale proof; no lasers, UI, battles, or heroic exploration poses.
- For **grassland / Inner Mongolia / desert / tundra**: default to wind-shaped terrain, small witness, pale wall edges, and luminous atmospheric distance. Use open sky for broad pilgrimage/panorama scenes; for reference-like detail requests, reduce sky and press the terrain against a close cropped wall or ring base. Avoid neon cyberpunk unless explicitly requested.
- For **ocean / underwater**: do not default to abyssal black. Prefer luminous shallow-sea shelf, blue-green water columns, sun shafts, readable silhouettes, suspended particles, and a giant submerged wall/ring/city-cliff fading into depth.
- For **golden / sacred / pilgrimage**: use warm light as a focused narrative target inside a cool environment, not as a full-frame yellow filter.
- For **alien civilization**: make the logic non-human through shape, scale, crop, and repetition; avoid monsters, battles, or readable sci-fi UI.
- For **dark / night / underground**: keep the frame legible with open shadows, visible edges, and motivated small lights.

## Internal Prompt Shape

Write the image prompt as one polished natural-language block for GPT Image 2:

```text
Create a cinematic sublime megastructure image, [inferred aspect and platform constraints]. Subject: [subject].
Route: [silent selected route: Wasteland Relic / Dreamcore Megastructure / Titan Alien Relic / Boundary / Pilgrimage / Unreturnable Home / Cosmic Indifference / Monumental Order / Luminous Relic], translated through its psychological mechanism, not as a visible label.
Visual thesis: [one sentence about human smallness, a single overwhelming form, and calm scale fracture].
Composition: [horizontal panorama or vertical tower framing], low/base/ground-level viewpoint when possible, one tiny non-heroic witness near the bottom/lower third, vast [terrain], one impossible [structure] dominating the sky/horizon, cropped by the frame and disappearing into haze/cloud/mist/dust/water/distance. For high-detail reference-like outputs, use near-distance monumental crop, minimal sky, compressed scale, wall/structure surfaces occupying most of the frame, and terrain pressed against the base.
Reference-case composition logic: one dominant readable silhouette, large breathing negative space, tiny witness scale, natural terrain as an entry path, close crop when detail matters, edge light and atmospheric perspective instead of underexposed darkness.
Details: [route-specific terrain, familiar anchor, abnormal deviation, material, scale proof, weather, obscurity, body anchor, restrained light, low-saturation palette]. For Wasteland Relic, make dead infrastructure quiet and non-heroic; for Dreamcore Megastructure, make one familiar spatial rule fail while preserving a strong dominant form, luminous readable air, and controlled dreamcore unease; for Titan Alien Relic, make the relic non-human, matte, ancient, and uninterested in human logic. For engineered mineral surfaces, layer large ribs/buttresses/panels with fine erosion streaks, scrape lines, chipped edges, cracks, stains, patch repairs, tiny maintenance marks, ladder-like traces, and base grime; use raking side light so the texture reads.
Cinematic finish: premium cinema still quality, luminous restrained film look, controlled contrast, soft highlight roll-off, preserved highlights, open shadow detail, clear midtone separation, subtle 35mm film grain, restrained halation around distant lights, volumetric haze, precise atmospheric perspective, clean filmic texture.
Mood: quiet post-human silence, sublime loneliness, controlled order, contemplative distance, restrained filmic realism. For Dreamcore Megastructure, bias the mood toward controlled dreamcore unease, empty breathable wonder, and lucid childhood-memory distance rather than cheerful healing fantasy or oppressive horror.
Negative constraints: no text, captions, subtitles, logo, watermark, UI, app interface, typography, readable signs, hero pose, battle, crowd spectacle, oversaturated colors, warm decorative beauty, fully explained clean blueprint view, underexposed darkness by default, overprocessed HDR, plastic CGI, excessive lens flare, teal-orange cliche, muddy blacks, crushed shadows, blown highlights, oversharpened digital render.
```

Read [references/prompt-patterns.md](references/prompt-patterns.md) only when the subject needs extra structure, stronger visual routes, deeper sublime logic, cinematic look presets, video/BGM extension language, or failure fixes. Use [references/route-smoke-tests.md](references/route-smoke-tests.md) when validating the three current core routes after editing this skill.
