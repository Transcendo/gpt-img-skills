# Megastructure Route Smoke Tests

Use these cases to verify that `megastructure-img` routes still produce the intended prompt structure after edits. They are not publishing prompts; they are sanity checks for route behavior.

## Pass criteria shared by all routes

A generated prompt or image should include:

- one dominant overwhelming form;
- a tiny non-heroic scale witness;
- a terrain or spatial path that leads the eye into the structure;
- crop, haze, weather, distance, or occlusion so the full structure is not fully explained;
- restrained cinematic finish with readable light and open shadows;
- no text, logo, watermark, UI, subtitles, readable signs, or typography.

## Case 1: Wasteland Relic

Input:

```text
抖音竖屏，末日废土，干涸海床里的旧世界水坝
```

Expected internal route:

```text
Wasteland Relic
```

Expected prompt ingredients:

- dry basin / cracked seabed / pale dust entry terrain;
- one broken concrete dam or reservoir wall as the dominant silhouette;
- tiny survivor, vehicle, camp, birds, or animals only as scale proof;
- weathered concrete, exposed rebar, rust scars, sand-stained walls, dead cables;
- readable daylight, pale dust, open shadows.

Must avoid:

- zombies, guns, gas-mask portraits, explosions, red apocalypse sky, action pose, rubble clutter.

## Case 2: Dream Megastructure

Input:

```text
小红书竖屏，奇妙梦境，云上的街道通向巨大的白色门
```

Expected internal route:

```text
Dream Megastructure
```

Expected prompt ingredients:

- one recognizable street, stair, school, platform, room, or playground anchor;
- one impossible spatial rule: street rising into clouds, door too large for any building, rooms opening into sky, reflections becoming architecture;
- one dominant dream form, not many random surreal objects;
- tiny figure, bicycle, bed, distant train, or similar scale witness;
- soft but disciplined color: milky daylight, pale peach, muted cyan, washed yellow, clean air.

Must avoid:

- candy fantasy, cute mascots, random floating-object clutter, meme weirdcore eyes, backrooms-yellow repetition, cartoon saturation.

## Case 3: Titan Alien Relic

Input:

```text
B站横屏，外星泰坦文明，冰卫星地平线上的巨型信号塔
```

Expected internal route:

```text
Titan Alien Relic
```

Expected prompt ingredients:

- alien ice moon, basalt plain, red dust valley, cloud sea, or another non-human terrain;
- one non-human relic: signal tower, orbital shell fragment, star-harvesting ring, planet-surface gate, suspended underside, titan rib-canyon;
- tiny astronaut, rover, probe, or expedition camp only as scale proof;
- matte mineral surfaces, pale ceramic stone, oxidized alien alloy, impossible seams, erosion, star-burn scars;
- cold stellar light, aurora haze, planetary rim light.

Must avoid:

- generic spaceship hero shot, lasers, battle, readable sci-fi UI, blue-purple crystal city, alien monster portrait, heroic astronaut pose.

## Current environment note

Image generation requires a configured provider. If the local environment has no image backend, validate route effectiveness with prompt compilation, keyword checks, and code-fence/frontmatter checks first; then run visual smoke tests once image generation is available.
