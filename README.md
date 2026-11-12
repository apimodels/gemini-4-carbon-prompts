# Gemini 4 Carbon Prompts and Examples: 223 Real Cases

English · [简体中文](README.zh-CN.md)

223 things people built, tested and compared with Google's Gemini 4 Carbon in its first weeks: 3D scenes, games, simulations, films and music made from code, real bug fixes and research, and dozens of same-prompt tests against Claude Fable 5.2, Gemini 4 Argon and others. Each case is credited to its creator and linked to the original post, with the prompt where the creator published one.

Disclosure: this collection is curated by [apimodels.app](https://apimodels.app), the API platform I work on. apimodels.app is a multi-model API gateway: one API key and Anthropic- and OpenAI-compatible endpoints, plus the native Gemini format, for Gemini 4 Carbon and more than 150 other image, video, audio and language models. Everything under [cases/](cases) is other people's work, described by us. A browsable version with the videos playing inline is the [Gemini 4 Carbon case library on apimodels.app](https://apimodels.app/gemini-4-carbon-prompts).

## In one paragraph

Gemini 4 Carbon (model id `gemini-4-carbon`) is Google's deeper-reasoning Gemini 4 model. Google built it on Gemini 4 Argon and describes the difference as more thinking tokens per turn; it was announced on 28 October 2026 for vetted cybersecurity defenders and opened to every paid Gemini API developer on 10 November. It reads text, images, video, audio and PDFs with a 1,048,576-token context and writes text, up to 65,536 tokens by default. Like other language models it does not render pixels or sound itself: the scenes, games and films below are code it wrote (Three.js, WebGL, Blender Python, CUDA C++, Web Audio), usually run by an agent, most often Google's Antigravity. The 223 cases were posted between 2026-10-21 and 2026-11-12; the earlier ones came from Arena tests and early access. 18 cases include the prompt as published, 33 only the creator's request or a paraphrase, and 172 no prompt; we never fill one in. On apimodels.app, Carbon costs $1.10 per 1M input tokens and $5.50 per 1M output through 30 November 2026 and $2.20 / $11 from 1 December, against Google's $2 / $10 and $4 / $20.

## Contents

- [Head-to-Head Tests](#head-to-head-tests) (96)
- [3D Scenes, Blender and Native Code](#3d-scenes-blender-and-native-code) (39)
- [Games](#games) (20)
- [Simulations, Science and Engineering](#simulations-science-and-engineering) (7)
- [Films, Music Videos and Sound](#films-music-videos-and-sound) (22)
- [SVG, Drawing and 2D Animation](#svg-drawing-and-2d-animation) (16)
- [Apps, Real Codebases and Tooling](#apps-real-codebases-and-tooling) (12)
- [Agents, Research and Writing](#agents-research-and-writing) (11)
- [Start here: the ten most-viewed cases on X](#start-here-the-ten-most-viewed-cases-on-x)
- [What the prompts that worked have in common](#what-the-prompts-that-worked-have-in-common)
- [How Carbon fared head to head](#how-carbon-fared-head-to-head)
- [Run it yourself](#run-it-yourself)
- [FAQ](#faq)
- [Credits, copyright and licence](#credits-copyright-and-licence)

Each case has its own page under [cases/](cases) with the creator, the original post, what was made, the tool, any numbers the creator reported and, where published, the prompt. X views and likes are as of 12 November 2026. Everything is also in [data/cases.json](data/cases.json).

## Start here: the ten most-viewed cases on X

1. [Agent teams find new exact solutions for fusion equations](cases/research/213-agent-teams-find-new-exact-solutions-for-fusion-equations.md) by @lucasjvds, about 248K views
2. [Airplane cutaway in 3D, Carbon vs Opus 5.5](cases/head-to-head/001-airplane-cutaway-in-3d-carbon-vs-opus-5-5.md) by @Mr_Salio, about 198K views
3. [Windows 11 running locally on a foldable iPhone](cases/code/201-windows-11-running-locally-on-a-foldable-iphone.md) by @ammaar, about 115K views
4. [Chrome Dino remake across Carbon, Opus, Astra and Terra](cases/head-to-head/007-chrome-dino-remake-across-carbon-opus-astra-and-terra.md) by @noclipepe, about 113K views
5. [Grass meadow with 52k blades in CUDA and C++](cases/3d/105-grass-meadow-with-52k-blades-in-cuda-and-c.md) by @GlitterPixely, about 109K views
6. [Voxel castle kingdom across Krypton, Carbon and Argon](cases/head-to-head/004-voxel-castle-kingdom-across-krypton-carbon-and-argon.md) by @lyraxana, about 102K views
7. [Rainbow jelly you can cut, nail and torch](cases/head-to-head/003-rainbow-jelly-you-can-cut-nail-and-torch.md) by @0xRhinoX, about 95K views
8. [Animated cutaway of a nine-cylinder radial engine](cases/head-to-head/009-animated-cutaway-of-a-nine-cylinder-radial-engine.md) by @olezhavich, about 88K views
9. [Robotic eye that blinks, focuses, then explodes into parts](cases/3d/101-robotic-eye-that-blinks-focuses-then-explodes-into-parts.md) by @noclipepe, about 85K views
10. [Underwater scene from a CUDA C++ VFX engine Carbon wrote](cases/3d/099-underwater-scene-from-a-cuda-c-vfx-engine-carbon-wrote.md) by @fofrAI, about 71K views

## What the prompts that worked have in common

- **Write a spec, not a wish.** Creators who gave Carbon one vague line mostly got average results. 亚里, who ran 15 projects, put it bluntly: don't make wishes at it. The striking results came from briefs that named the stack, the deliverable and what done looks like; one creator wrote a spec of about 10,000 characters for a three-minute violin concert film.
- **Show it a reference.** Carbon reads video. One creator gave it the gameplay video of a shooter Claude Fable 5.2 had built and asked for the same game or better; another gave it Anthropic's own Fable 5.2 demo video to rebuild as a web page.
- **Make it look at its own output.** The shooter rebuild ran a headless-Chrome screenshot loop that caught and fixed three bugs on its own, in 48 minutes for $3.82. Another creator had Carbon review its screenshots like a VFX supervisor four times, about two hours and $7.40 in all, turning a block of voxels into a convincing dinosaur.
- **Name the format.** "One HTML file. No external assets." is the whole second half of the 5,000-drone light show prompt. Simon Willison had to add "build that into a standalone HTML file" to get a page he could open on its own.
- **Split big builds across agents.** The largest builds used Antigravity's multi-agent /swarm mode: nine agents and 22,910 lines for a diorama builder in 1 hour 41 minutes, and five waves of agent critique for an open-world game.
- **Follow up.** One creator posted the same island and castle after the first prompt and after three follow-ups; the fire went from nine orange cubes to something close to real. The gap, in the author's words, came from the follow-ups.
- **Check what it says it finished.** In one six-app test every one of Carbon's final summaries claimed at least one feature that turned out broken or overstated. Ask it to click through the result in a browser before it reports back.

## How Carbon fared head to head

96 cases in this collection are same-prompt tests, most against Claude Fable 5.2 and Gemini 4 Argon. Against **Fable 5.2**, creators usually found Fable's visuals, animation and finish better, and Carbon's cost a small fraction of Fable's: $7.54 against $41.71 for three jobs in one test (Carbon still won two of them), $27.68 against $883.30 for three long builds in another, and a 70% against 53.3% score in a six-app benchmark that Fable won. Against **Gemini 4 Argon**, Carbon usually came out ahead but took longer and wrote more: 81 minutes and 186,000 output tokens against 14 minutes and 11,000 in one Blender test that Argon had failed. These are single runs by different people in different tools; read them as field reports. The full numbers are on the case pages, and our comparison pages put them next to the benchmarks: [Gemini 4 Carbon vs Argon](https://apimodels.app/gemini-4-carbon-vs-argon) and [Claude Fable 5.2 vs Gemini 4 Carbon](https://apimodels.app/claude-fable-5-2-vs-gemini-4-carbon).

## Head-to-Head Tests

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/head-to-head](https://apimodels.app/gemini-4-carbon-prompts/head-to-head)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 1 | [Airplane cutaway in 3D, Carbon vs Opus 5.5](cases/head-to-head/001-airplane-cutaway-in-3d-carbon-vs-opus-5-5.md) | [@Mr_Salio](https://x.com/Mr_Salio) | Not published | X, 198K views |
| 2 | [Low-poly running giraffe, Opus 5.5 vs Carbon](cases/head-to-head/002-low-poly-running-giraffe-opus-5-5-vs-carbon.md) | [@Haleeeemahh](https://x.com/Haleeeemahh) | Not published | X, 64K views |
| 3 | [Rainbow jelly you can cut, nail and torch](cases/head-to-head/003-rainbow-jelly-you-can-cut-nail-and-torch.md) | [@0xRhinoX](https://x.com/0xRhinoX) | Request only | X, 95K views |
| 4 | [Voxel castle kingdom across Krypton, Carbon and Argon](cases/head-to-head/004-voxel-castle-kingdom-across-krypton-carbon-and-argon.md) | [@lyraxana](https://x.com/lyraxana) | Not published | X, 102K views |
| 5 | [Editing a founders' pitch clip, Fable 5.2 vs Carbon](cases/head-to-head/005-editing-a-founders-pitch-clip-fable-5-2-vs-carbon.md) | [@motion_so](https://x.com/motion_so) | Not published | X, 49K views |
| 6 | [Animated road cyclist, Carbon vs Argon vs GPT-6 Astra](cases/head-to-head/006-animated-road-cyclist-carbon-vs-argon-vs-gpt-6-astra.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 66K views |
| 7 | [Chrome Dino remake across Carbon, Opus, Astra and Terra](cases/head-to-head/007-chrome-dino-remake-across-carbon-opus-astra-and-terra.md) | [@noclipepe](https://x.com/noclipepe) | Not published | X, 113K views |
| 8 | [Jelly DVD screensaver where Opus swapped in the Claude logo](cases/head-to-head/008-jelly-dvd-screensaver-where-opus-swapped-in-the-claude-logo.md) | [@0xRhinoX](https://x.com/0xRhinoX) | Request only | X, 26K views |
| 9 | [Animated cutaway of a nine-cylinder radial engine](cases/head-to-head/009-animated-cutaway-of-a-nine-cylinder-radial-engine.md) | [@olezhavich](https://x.com/olezhavich) | Request only | X, 88K views |
| 10 | [Nine tiny troublemakers on a dock full of tools](cases/head-to-head/010-nine-tiny-troublemakers-on-a-dock-full-of-tools.md) | [@0xPorterio](https://x.com/0xPorterio) | Request only | X, 42K views |
| 11 | [Animated road cyclist, Fable 5.5 vs Carbon in Arena](cases/head-to-head/011-animated-road-cyclist-fable-5-5-vs-carbon-in-arena.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 27K views |
| 12 | [Stickman fight animation, DeepSeek V4.1 Flash vs Carbon](cases/head-to-head/012-stickman-fight-animation-deepseek-v4-1-flash-vs-carbon.md) | [@leo114119](https://x.com/leo114119) | Not published | X, 47K views |
| 13 | [Night-city SUV scene, Fable 5.2 vs Carbon vs Argon](cases/head-to-head/013-night-city-suv-scene-fable-5-2-vs-carbon-vs-argon.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 21K views |
| 14 | [Voxel Gru dodging rockets rebuilt from a movie clip](cases/head-to-head/014-voxel-gru-dodging-rockets-rebuilt-from-a-movie-clip.md) | [@atomic_chat_hq](https://x.com/atomic_chat_hq) | Not published | X, 34K views |
| 15 | [U.S. White House in Three.js, Carbon vs Opus 5.5](cases/head-to-head/015-u-s-white-house-in-three-js-carbon-vs-opus-5-5.md) | [@exploraX_](https://x.com/exploraX_) | Not published | X, 21K views |
| 16 | [Pelican on a bicycle, Carbon vs Fable 5.5 in testing](cases/head-to-head/016-pelican-on-a-bicycle-carbon-vs-fable-5-5-in-testing.md) | [@leo114119](https://x.com/leo114119) | Not published | X, 54K views |
| 17 | [Rocket scene across Carbon, Fable 5.2, Opus 5.5 and Astra](cases/head-to-head/017-rocket-scene-across-carbon-fable-5-2-opus-5-5-and-astra.md) | [@Bhavani_00007](https://x.com/Bhavani_00007) | Not published | X, 21K views |
| 18 | [Rainbow jelly rematch against Fable 5.5](cases/head-to-head/018-rainbow-jelly-rematch-against-fable-5-5.md) | [@0xRhinoX](https://x.com/0xRhinoX) | Request only | X, 28K views |
| 19 | [Sailing ship at sea, Fable 5.2 vs Carbon](cases/head-to-head/019-sailing-ship-at-sea-fable-5-2-vs-carbon.md) | [@Da7_Tech](https://x.com/Da7_Tech) | Not published | X, 13K views |
| 20 | [Running tiger, Carbon vs Opus 5.5 vs Argon in Arena](cases/head-to-head/020-running-tiger-carbon-vs-opus-5-5-vs-argon-in-arena.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 12K views |
| 21 | [Floating island with a grazing cow, Opus 5.5 vs Carbon](cases/head-to-head/021-floating-island-with-a-grazing-cow-opus-5-5-vs-carbon.md) | [@Haleeeemahh](https://x.com/Haleeeemahh) | Not published | X, 12K views |
| 22 | [Stickman fight animation, Carbon vs Fable 5.2](cases/head-to-head/022-stickman-fight-animation-carbon-vs-fable-5-2.md) | [@DanielZambrini](https://x.com/DanielZambrini) | Not published | X, 23K views |
| 23 | [Country-estate mower scene, Fable 5.2 vs Carbon](cases/head-to-head/023-country-estate-mower-scene-fable-5-2-vs-carbon.md) | [@_MaxBlade](https://x.com/_MaxBlade) | Not published | X, 14K views |
| 24 | [T-rex riding a bike across four models](cases/head-to-head/024-t-rex-riding-a-bike-across-four-models.md) | [@olezhavich](https://x.com/olezhavich) | Not published | X, 27K views |
| 25 | [Working inline-four engine across four models](cases/head-to-head/025-working-inline-four-engine-across-four-models.md) | [@kinderlayer](https://x.com/kinderlayer) | Request only | X, 15K views |
| 26 | [Blender Sisyphus Shark scene with Fable 5.2 added](cases/head-to-head/026-blender-sisyphus-shark-scene-with-fable-5-2-added.md) | [@HeathIsidr64707](https://x.com/HeathIsidr64707) | Not published | X, 30K views |
| 27 | [Dinosaur obstacle run scored across four models](cases/head-to-head/027-dinosaur-obstacle-run-scored-across-four-models.md) | [@ridark_eth](https://x.com/ridark_eth) | Request only | X, 11K views |
| 28 | [Voxel floating kingdom, Opus 5.5 vs Carbon](cases/head-to-head/028-voxel-floating-kingdom-opus-5-5-vs-carbon.md) | [@marcthecreatorr](https://x.com/marcthecreatorr) | Request only | X, 6,033 views |
| 29 | [Running fox, released Carbon vs its Arena checkpoint](cases/head-to-head/029-running-fox-released-carbon-vs-its-arena-checkpoint.md) | [@srikanthvaluri](https://x.com/srikanthvaluri) | Request only | X, 7,251 views |
| 30 | [Running tiger, Carbon vs Gemini 4 Hydrogen in Arena](cases/head-to-head/030-running-tiger-carbon-vs-gemini-4-hydrogen-in-arena.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 5,563 views |
| 31 | [Rainbow jelly pumpkin you can carve and light](cases/head-to-head/031-rainbow-jelly-pumpkin-you-can-carve-and-light.md) | [@0xRhinoX](https://x.com/0xRhinoX) | Request only | X, 6,582 views |
| 32 | [Sunset city and muscle car drawn live with a pen](cases/head-to-head/032-sunset-city-and-muscle-car-drawn-live-with-a-pen.md) | [@olezhavich](https://x.com/olezhavich) | Request only | X, 23K views |
| 33 | [Tropical-island first-person shooter, Fable 5.2 vs Carbon](cases/head-to-head/033-tropical-island-first-person-shooter-fable-5-2-vs-carbon.md) | [@ValencianaAbel](https://x.com/ValencianaAbel) | Request only | X, 10K views |
| 34 | [Jelly and nails game, Fable 5.5 vs Carbon](cases/head-to-head/034-jelly-and-nails-game-fable-5-5-vs-carbon.md) | [@0xRhinoX](https://x.com/0xRhinoX) | Not published | X, 23K views |
| 35 | [Running zebra across Carbon, Fable 5.5, Opus 5.5 and Argon](cases/head-to-head/035-running-zebra-across-carbon-fable-5-5-opus-5-5-and-argon.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 8,951 views |
| 36 | [Animated SVG octopus cooking breakfast with eight tentacles](cases/head-to-head/036-animated-svg-octopus-cooking-breakfast-with-eight-tentacles.md) | [@olezhavich](https://x.com/olezhavich) | Request only | X, 8,711 views |
| 37 | [Running V8 you can X-ray, cut and explode](cases/head-to-head/037-running-v8-you-can-x-ray-cut-and-explode.md) | [@dromexa](https://x.com/dromexa) | Request only | X, 3,257 views |
| 38 | ['90s arcade fighter across four models](cases/head-to-head/038-90s-arcade-fighter-across-four-models.md) | [@runable_hq](https://x.com/runable_hq) | Not published | X, 14K views |
| 39 | [Tiger, eagle and sports car, Carbon vs Argon in Arena](cases/head-to-head/039-tiger-eagle-and-sports-car-carbon-vs-argon-in-arena.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 3,345 views |
| 40 | [Same prompt, Fable 5.2 at $18 vs Carbon at $6.2](cases/head-to-head/040-same-prompt-fable-5-2-at-18-vs-carbon-at-6-2.md) | [@laopai1990](https://x.com/laopai1990) | Not published | X, 17K views |
| 41 | [Mechanical watch you can X-ray, cut and explode](cases/head-to-head/041-mechanical-watch-you-can-x-ray-cut-and-explode.md) | [@dromexa](https://x.com/dromexa) | Request only | X, 2,551 views |
| 42 | [Charging bull at sunset, Carbon in Arena vs Opus 5.5](cases/head-to-head/042-charging-bull-at-sunset-carbon-in-arena-vs-opus-5-5.md) | [@jony_palino](https://x.com/jony_palino) | Not published | X, 5,118 views |
| 43 | [Sisyphus Shark scene in Blender, Carbon vs Opus 5.5](cases/head-to-head/043-sisyphus-shark-scene-in-blender-carbon-vs-opus-5-5.md) | [@HeathIsidr64707](https://x.com/HeathIsidr64707) | Request only | X, 6,603 views |
| 44 | [Sewing machine that X-rays, explodes and makes a stitch](cases/head-to-head/044-sewing-machine-that-x-rays-explodes-and-makes-a-stitch.md) | [@dromexa](https://x.com/dromexa) | Request only | X, 3,745 views |
| 45 | [Animated peacock SVG, Fable 5.2 vs Carbon](cases/head-to-head/045-animated-peacock-svg-fable-5-2-vs-carbon.md) | [@SahilPanhotra](https://x.com/SahilPanhotra) | Not published | X, 2,011 views |
| 46 | [Whale breaching scene, Carbon vs Opus 5.5](cases/head-to-head/046-whale-breaching-scene-carbon-vs-opus-5-5.md) | [@Bhavani_00007](https://x.com/Bhavani_00007) | Request only | X, 3,562 views |
| 47 | [3D soda animation in pure front-end code, Fable 5.5 vs Carbon](cases/head-to-head/047-3d-soda-animation-in-pure-front-end-code-fable-5-5-vs-carbon.md) | [@leo114119](https://x.com/leo114119) | Not published | X, 3,143 views |
| 48 | [Mage versus dragon game, Sonnet 5.5 vs Carbon](cases/head-to-head/048-mage-versus-dragon-game-sonnet-5-5-vs-carbon.md) | [@IndependentEco](https://x.com/IndependentEco) | Not published | X, 3,143 views |
| 49 | [Jaw lever biomechanics diagram, Carbon vs Fable 5.2](cases/head-to-head/049-jaw-lever-biomechanics-diagram-carbon-vs-fable-5-2.md) | [@aiZttt__](https://x.com/aiZttt__) | Not published | X, 6,667 views |
| 50 | [Ruined robot animation, Carbon vs Fable 5.2](cases/head-to-head/050-ruined-robot-animation-carbon-vs-fable-5-2.md) | [@itsPaulAi](https://x.com/itsPaulAi) | Not published | X, 11K views |
| 51 | [Pelican on a bicycle across Krypton, Carbon and Argon](cases/head-to-head/051-pelican-on-a-bicycle-across-krypton-carbon-and-argon.md) | [@srikanthvaluri](https://x.com/srikanthvaluri) | Not published | X, 2,314 views |
| 52 | [Robot that transforms into a car, Carbon vs Fable 5.1](cases/head-to-head/052-robot-that-transforms-into-a-car-carbon-vs-fable-5-1.md) | [@dromexa](https://x.com/dromexa) | Request only | X, 2,944 views |
| 53 | [Cockatiel on a branch, Qwen 4-Max vs Carbon](cases/head-to-head/053-cockatiel-on-a-branch-qwen-4-max-vs-carbon.md) | [@DrstaOne](https://x.com/DrstaOne) | Not published | X, 3,441 views |
| 54 | [Snow globe in one HTML file, Fable 5.2 vs Carbon](cases/head-to-head/054-snow-globe-in-one-html-file-fable-5-2-vs-carbon.md) | [@SahilPanhotra](https://x.com/SahilPanhotra) | Not published | X, 1,821 views |
| 55 | [Shanghai Bund scene across Carbon, Argon, Fable 5.2 and Opus 5.5](cases/head-to-head/055-shanghai-bund-scene-across-carbon-argon-fable-5-2-and-opus-5.md) | [@NFT_Chen](https://x.com/NFT_Chen) | Not published | X, 11K views |
| 56 | [Floating island with a cow, Fable 5.2 vs Carbon](cases/head-to-head/056-floating-island-with-a-cow-fable-5-2-vs-carbon.md) | [@Haleeeemahh](https://x.com/Haleeeemahh) | Not published | X, 2,199 views |
| 57 | [CPU versus graphics card explainer video, Fable 5.2 vs Carbon](cases/head-to-head/057-cpu-versus-graphics-card-explainer-video-fable-5-2-vs-carbon.md) | [@getviewgum](https://x.com/getviewgum) | Not published | X, 3,384 views |
| 58 | [Black hole simulation, Carbon vs Gemini 4 Hydrogen](cases/head-to-head/058-black-hole-simulation-carbon-vs-gemini-4-hydrogen.md) | [@leo114119](https://x.com/leo114119) | Not published | X, 3,209 views |
| 59 | [Bentley side view in Three.js, Carbon vs Opus 5.5](cases/head-to-head/059-bentley-side-view-in-three-js-carbon-vs-opus-5-5.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 1,177 views |
| 60 | [Bicycle riding a pelican through the sky, Carbon vs Fable 5.5](cases/head-to-head/060-bicycle-riding-a-pelican-through-the-sky-carbon-vs-fable-5-5.md) | [@Haleeeemahh](https://x.com/Haleeeemahh) | Not published | X, 3,041 views |
| 61 | [Rebuilding Anthropic's Fable 5.2 launch demo as a web page](cases/head-to-head/061-rebuilding-anthropic-s-fable-5-2-launch-demo-as-a-web-page.md) | [@akokoi1](https://x.com/akokoi1) | Not published | X, 4,822 views |
| 62 | [Motor and generator demo, Carbon vs a Fable 5.2 run](cases/head-to-head/062-motor-and-generator-demo-carbon-vs-a-fable-5-2-run.md) | [@akokoi1](https://x.com/akokoi1) | Not published | X, 2,353 views |
| 63 | [Night-Tokyo drone coin game across Carbon, Fable and Opus](cases/head-to-head/063-night-tokyo-drone-coin-game-across-carbon-fable-and-opus.md) | [@muku_sns](https://x.com/muku_sns) | Request only | X, 396 views |
| 64 | [Interactive digital garden, Fable 5.2 vs Carbon](cases/head-to-head/064-interactive-digital-garden-fable-5-2-vs-carbon.md) | [@HIX_AI_](https://x.com/HIX_AI_) | Not published | X, 366 views |
| 65 | [Gyeongbokgung palace simulator, Fable 5.2 vs Carbon](cases/head-to-head/065-gyeongbokgung-palace-simulator-fable-5-2-vs-carbon.md) | [@msdkim](https://x.com/msdkim) | Not published | X, 277 views |
| 66 | [World music tour animated video, Carbon vs Fable 5.2](cases/head-to-head/066-world-music-tour-animated-video-carbon-vs-fable-5-2.md) | [@Gorden_Sun](https://x.com/Gorden_Sun) | Not published | X, 2,105 views |
| 67 | [Ramen stall in the rain in Blender across three models](cases/head-to-head/067-ramen-stall-in-the-rain-in-blender-across-three-models.md) | [@colerepo](https://x.com/colerepo) | Request only | X, 287 views |
| 68 | [15 Antigravity projects, from a GTA-style game to an ink page](cases/head-to-head/068-15-antigravity-projects-from-a-gta-style-game-to-an-ink-page.md) | 亚里 Yari | Full prompt | YouTube |
| 69 | [Three hard builds with full cost receipts across four models](cases/head-to-head/069-three-hard-builds-with-full-cost-receipts-across-four-models.md) | Pat Simmons (AI for Mortals) | Not published | YouTube |
| 70 | [KingBench 4: six app builds, Carbon vs Fable 5.2](cases/head-to-head/070-kingbench-4-six-app-builds-carbon-vs-fable-5-2.md) | AICodeKing | Not published | YouTube |
| 71 | [Five builds and games: Carbon vs Fable 5.2](cases/head-to-head/071-five-builds-and-games-carbon-vs-fable-5-2.md) | The Token Desk | Not published | YouTube |
| 72 | [Neon arcade racer, night-market voxel diorama and channel intro](cases/head-to-head/072-neon-arcade-racer-night-market-voxel-diorama-and-channel.md) | KostiKoNeuro | Excerpt | GitHub |
| 73 | [Horror game, EV landing page and walkable 3D loft](cases/head-to-head/073-horror-game-ev-landing-page-and-walkable-3d-loft.md) | Kami | Not published | YouTube |
| 74 | [Korean learning app, automation dashboard, animated explainer: Carbon vs Opus 5.5](cases/head-to-head/074-korean-learning-app-automation-dashboard-animated-explainer.md) | Dan Buica / AI Automation | Not published | YouTube |
| 75 | [Six projects in the Antigravity CLI with real API cost](cases/head-to-head/075-six-projects-in-the-antigravity-cli-with-real-api-cost.md) | Matheus Battisti - Hora de Codar | Not published | YouTube |
| 76 | [Ultra-realistic Minecraft-style game in Three.js after 5 hours of agents](cases/head-to-head/076-ultra-realistic-minecraft-style-game-in-three-js-after-5.md) | Vini Lana | Not published | YouTube |
| 77 | [Nine complex builds in the Antigravity CLI at medium effort](cases/head-to-head/077-nine-complex-builds-in-the-antigravity-cli-at-medium-effort.md) | AI超元域 | Not published | YouTube |
| 78 | [Carbon vs Argon: novel writing, front-end code, SVG, animated short](cases/head-to-head/078-carbon-vs-argon-novel-writing-front-end-code-svg-animated.md) | 碳基生物退役指南 | Not published | YouTube |
| 79 | [Carbon vs Argon across five dimensions, including security](cases/head-to-head/079-carbon-vs-argon-across-five-dimensions-including-security.md) | Piningillness | Not published | Bilibili |
| 80 | [Constrained sentences, archery SVG and browser OS UI: Carbon vs Fable 5.2](cases/head-to-head/080-constrained-sentences-archery-svg-and-browser-os-ui-carbon.md) | AI产品狙击手 | Not published | Bilibili |
| 81 | [Bench V3: seven tests at max reasoning through a third-party API](cases/head-to-head/081-bench-v3-seven-tests-at-max-reasoning-through-a-third-party.md) | Matt Johnston | Not published | YouTube |
| 82 | [Same five tests as Fable 5.2, plus a ship simulator](cases/head-to-head/082-same-five-tests-as-fable-5-2-plus-a-ship-simulator.md) | Uğur Keşkekçi | Not published | YouTube |
| 83 | [Duolingo-style app, automation plan, animated explainer: Carbon vs Fable 5.2](cases/head-to-head/083-duolingo-style-app-automation-plan-animated-explainer-carbon.md) | Dan Buica / AI Automation | Not published | YouTube |
| 84 | [Live vibe check: Notion backlog, Blender room rebuild, UI suite](cases/head-to-head/084-live-vibe-check-notion-backlog-blender-room-rebuild-ui-suite.md) | Every (Dan Shipper and team) | Not published | YouTube |
| 85 | [Early-access builds: open world, SDF dragon, fort rebuilt over 100+ passes](cases/head-to-head/085-early-access-builds-open-world-sdf-dragon-fort-rebuilt-over.md) | Prompt Engineering | Not published | YouTube |
| 86 | [Two weeks of early access across games, apps and video editing](cases/head-to-head/086-two-weeks-of-early-access-across-games-apps-and-video.md) | Paul J Lipsky | Not published | YouTube |
| 87 | [3D Marina Bay Sands, Pomodoro Mac app, Bear + Obsidian mash-up](cases/head-to-head/087-3d-marina-bay-sands-pomodoro-mac-app-bear-obsidian-mash-up.md) | Sam Witteveen | Not published | YouTube |
| 88 | [Browser OS, C++ skate game, subway FPS and 3D printing tests](cases/head-to-head/088-browser-os-c-skate-game-subway-fps-and-3d-printing-tests.md) | Bijan Bowen | Not published | YouTube |
| 89 | [Blender airport, cable-car game, Golden Gate build and lease check](cases/head-to-head/089-blender-airport-cable-car-game-golden-gate-build-and-lease.md) | AI with Surya | Not published | YouTube |
| 90 | [Seven tests via Cursor and Droid, including a mooncake gift box](cases/head-to-head/090-seven-tests-via-cursor-and-droid-including-a-mooncake-gift.md) | NiceKate AI (kate人不错) | Not published | YouTube |
| 91 | [3D pirate ship, Rube Goldberg machine and Newton's cradle](cases/head-to-head/091-3d-pirate-ship-rube-goldberg-machine-and-newton-s-cradle.md) | Ömer Göçmen | Not published | YouTube |
| 92 | [Video feedback, 3D games and slides via the API and Cursor](cases/head-to-head/092-video-feedback-3d-games-and-slides-via-the-api-and-cursor.md) | まさおAIじっくり解説ch | Not published | YouTube |
| 93 | [Pelican SVG with inverse kinematics and other code-native 3D demos](cases/head-to-head/093-pelican-svg-with-inverse-kinematics-and-other-code-native-3d.md) | dotAI情报站 | Not published | Bilibili |
| 94 | [Six fixed one-shot prompts through a third-party API, from pelican to Breakout](cases/head-to-head/094-six-fixed-one-shot-prompts-through-a-third-party-api-from.md) | hype or code | Full prompt | web page |
| 95 | [Hotel website, skillet launch ad and Apollo 11 Mission Clock](cases/head-to-head/095-hotel-website-skillet-launch-ad-and-apollo-11-mission-clock.md) | Runable | Not published | YouTube |
| 96 | [First impressions: 3D landmarks, painting worlds, visual explainers and UI](cases/head-to-head/096-first-impressions-3d-landmarks-painting-worlds-visual.md) | Arena | Not published | YouTube |

## 3D Scenes, Blender and Native Code

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/3d](https://apimodels.app/gemini-4-carbon-prompts/3d)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 97 | [Mechanical flower in Three.js with an unprompted bee](cases/3d/097-mechanical-flower-in-three-js-with-an-unprompted-bee.md) | [@thtbee_](https://x.com/thtbee_) | Not published | X, 59K views |
| 98 | [Three.js recreation of a train-cab video clip](cases/3d/098-three-js-recreation-of-a-train-cab-video-clip.md) | [@emollick](https://x.com/emollick) | Not published | X, 61K views |
| 99 | [Underwater scene from a CUDA C++ VFX engine Carbon wrote](cases/3d/099-underwater-scene-from-a-cuda-c-vfx-engine-carbon-wrote.md) | [@fofrAI](https://x.com/fofrAI) | Not published | X, 71K views |
| 100 | [Orrery where one control drives gears and petals](cases/3d/100-orrery-where-one-control-drives-gears-and-petals.md) | [@kimmonismus](https://x.com/kimmonismus) | Not published | X, 53K views |
| 101 | [Robotic eye that blinks, focuses, then explodes into parts](cases/3d/101-robotic-eye-that-blinks-focuses-then-explodes-into-parts.md) | [@noclipepe](https://x.com/noclipepe) | Request only | X, 85K views |
| 102 | [Open valley scene in custom C++ with no reused assets](cases/3d/102-open-valley-scene-in-custom-c-with-no-reused-assets.md) | [@Lentils80](https://x.com/Lentils80) | Not published | X, 9,430 views |
| 103 | [3D basketball court built without premade assets](cases/3d/103-3d-basketball-court-built-without-premade-assets.md) | [@LexnLin](https://x.com/LexnLin) | Not published | X, 8,904 views |
| 104 | [Jeweled sea creature sculpted and animated in Blender](cases/3d/104-jeweled-sea-creature-sculpted-and-animated-in-blender.md) | [@Stefan_3D_AI](https://x.com/Stefan_3D_AI) | Not published | X, 13K views |
| 105 | [Grass meadow with 52k blades in CUDA and C++](cases/3d/105-grass-meadow-with-52k-blades-in-cuda-and-c.md) | [@GlitterPixely](https://x.com/GlitterPixely) | Not published | X, 109K views |
| 106 | [Island castle and dragon: first prompt vs three follow-ups](cases/3d/106-island-castle-and-dragon-first-prompt-vs-three-follow-ups.md) | [@semichenkko](https://x.com/semichenkko) | Not published | X, 25K views |
| 107 | [Realistic interactive 3D horse from the classic horse prompt](cases/3d/107-realistic-interactive-3d-horse-from-the-classic-horse-prompt.md) | [@kasmiyouness1](https://x.com/kasmiyouness1) | Full prompt | X, 5,033 views |
| 108 | [Aquarium with angelfish, snail and shrimp from a multi-tool pipeline](cases/3d/108-aquarium-with-angelfish-snail-and-shrimp-from-a-multi-tool.md) | [@ai_for_success](https://x.com/ai_for_success) | Not published | X, 4,332 views |
| 109 | [Koi courtyard with water reflections and swimming fish](cases/3d/109-koi-courtyard-with-water-reflections-and-swimming-fish.md) | [@SahilPanhotra](https://x.com/SahilPanhotra) | Not published | X, 3,777 views |
| 110 | [Coca-Cola bottle drawn entirely in one shader](cases/3d/110-coca-cola-bottle-drawn-entirely-in-one-shader.md) | [@karanC_12](https://x.com/karanC_12) | Not published | X, 3,927 views |
| 111 | [Minecraft-style test in Three.js using Antigravity voice mode](cases/3d/111-minecraft-style-test-in-three-js-using-antigravity-voice.md) | [@oviniciuslana](https://x.com/oviniciuslana) | Not published | X, 2,376 views |
| 112 | [11.3 million voxels at 60fps in one HTML file](cases/3d/112-11-3-million-voxels-at-60fps-in-one-html-file.md) | [@Adidotdev](https://x.com/Adidotdev) | Not published | X, 2,242 views |
| 113 | [Destroyed Coventry Cathedral rebuilt from floorplans and photos](cases/3d/113-destroyed-coventry-cathedral-rebuilt-from-floorplans-and.md) | [@LeslieNooteboom](https://x.com/LeslieNooteboom) | Not published | X, 6,870 views |
| 114 | [Procedural mechanical falcon with a working watch movement](cases/3d/114-procedural-mechanical-falcon-with-a-working-watch-movement.md) | [@Adidotdev](https://x.com/Adidotdev) | Not published | X, 1,386 views |
| 115 | [Voxel floating kingdom with over three million voxels](cases/3d/115-voxel-floating-kingdom-with-over-three-million-voxels.md) | [@marcthecreatorr](https://x.com/marcthecreatorr) | Request only | X, 1,732 views |
| 116 | [Eiffel Tower model built from old drawings and photos](cases/3d/116-eiffel-tower-model-built-from-old-drawings-and-photos.md) | [@cobley_ben](https://x.com/cobley_ben) | Not published | X, 1,497 views |
| 117 | [Space video made with code and Blender](cases/3d/117-space-video-made-with-code-and-blender.md) | [@RJasonHA](https://x.com/RJasonHA) | Not published | X, 2,475 views |
| 118 | [Little universe with planets, Milky Way and shooting stars](cases/3d/118-little-universe-with-planets-milky-way-and-shooting-stars.md) | [@doe_naps](https://x.com/doe_naps) | Not published | X, 592 views |
| 119 | [Supercar chasing a steam train, scripted in Blender](cases/3d/119-supercar-chasing-a-steam-train-scripted-in-blender.md) | [@HeathIsidr64707](https://x.com/HeathIsidr64707) | Not published | X, 2,122 views |
| 120 | [Yonkers stands up as a giant mech over New York](cases/3d/120-yonkers-stands-up-as-a-giant-mech-over-new-york.md) | [@simonw](https://x.com/simonw) | Full prompt | X, 410 views |
| 121 | [Cyclist riding a golden eagle, one-shot in Three.js](cases/3d/121-cyclist-riding-a-golden-eagle-one-shot-in-three-js.md) | [@AI_Screening](https://x.com/AI_Screening) | Not published | X, 1,396 views |
| 122 | [Interactive New York City cruise tour in one HTML file](cases/3d/122-interactive-new-york-city-cruise-tour-in-one-html-file.md) | [@StatsWire](https://x.com/StatsWire) | Not published | X, 735 views |
| 123 | [Icelandic black-sand beach in Three.js over five rounds](cases/3d/123-icelandic-black-sand-beach-in-three-js-over-five-rounds.md) | [@RJasonHA](https://x.com/RJasonHA) | Not published | X, 757 views |
| 124 | [Endless marble-run tower where every step plays a note](cases/3d/124-endless-marble-run-tower-where-every-step-plays-a-note.md) | [@sunset_evm](https://x.com/sunset_evm) | Request only | X, 1,072 views |
| 125 | [Barbecue stall modeled in Antigravity](cases/3d/125-barbecue-stall-modeled-in-antigravity.md) | [@marcus_s_deng](https://x.com/marcus_s_deng) | Not published | X, 1,860 views |
| 126 | [Running zebra in Three.js](cases/3d/126-running-zebra-in-three-js.md) | [@ai_funss](https://x.com/ai_funss) | Not published | X, 1,652 views |
| 127 | [Rifle assembly and ballistics scene in Blender with no downloads](cases/3d/127-rifle-assembly-and-ballistics-scene-in-blender-with-no.md) | [@vipinxtwt](https://x.com/vipinxtwt) | Not published | X, 520 views |
| 128 | [5,000-drone light show over a night waterfront](cases/3d/128-5-000-drone-light-show-over-a-night-waterfront.md) | [@sunset_evm](https://x.com/sunset_evm) | Full prompt | X, 906 views |
| 129 | [Hypercar built by a swarm of Carbon agents](cases/3d/129-hypercar-built-by-a-swarm-of-carbon-agents.md) | [@SimonasLTU1](https://x.com/SimonasLTU1) | Not published | X, 781 views |
| 130 | [Sailing boat scene made in the Gemini mobile app](cases/3d/130-sailing-boat-scene-made-in-the-gemini-mobile-app.md) | [@EdwinCh43136084](https://x.com/EdwinCh43136084) | Not published | X, 545 views |
| 131 | [Pure CUDA + C++20 ray tracer: raindrops on a lotus pond](cases/3d/131-pure-cuda-c-20-ray-tracer-raindrops-on-a-lotus-pond.md) | Jian Zhang (GitHub opdaer, X @jianzhang1987) | Not published | GitHub |
| 132 | [181-part Song Dynasty mortise-and-tenon pavilion with exploded view](cases/3d/132-181-part-song-dynasty-mortise-and-tenon-pavilion-with.md) | Jian Zhang (GitHub opdaer) | Not published | GitHub |
| 133 | [PCB design in tscircuit: Fable 5.2 vs Carbon](cases/3d/133-pcb-design-in-tscircuit-fable-5-2-vs-carbon.md) | Seve | Full prompt | YouTube |
| 134 | [Reference-image 3D modelling and a Rube Goldberg machine vs Opus 5.5](cases/3d/134-reference-image-3d-modelling-and-a-rube-goldberg-machine-vs.md) | EWIY | Not published | Bilibili |
| 135 | [Paimon 3D model in Blender over a 6-hour run](cases/3d/135-paimon-3d-model-in-blender-over-a-6-hour-run.md) | 连接实验室 | Not published | Bilibili |

## Games

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/games](https://apimodels.app/gemini-4-carbon-prompts/games)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 136 | [Chrome Dino upgraded by four rounds of self-review](cases/games/136-chrome-dino-upgraded-by-four-rounds-of-self-review.md) | [@noclipepe](https://x.com/noclipepe) | Not published | X, 13K views |
| 137 | [Cozy puzzle game built entirely in AI Studio](cases/games/137-cozy-puzzle-game-built-entirely-in-ai-studio.md) | [@chanelluuh](https://x.com/chanelluuh) | Not published | X, 46K views |
| 138 | [Playable V12 hypercar coastal racing game in one HTML file](cases/games/138-playable-v12-hypercar-coastal-racing-game-in-one-html-file.md) | [@StatsWire](https://x.com/StatsWire) | Not published | X, 1,871 views |
| 139 | [Seaplane game with an infinite ocean and random islands](cases/games/139-seaplane-game-with-an-infinite-ocean-and-random-islands.md) | [@RoundtableSpace](https://x.com/RoundtableSpace) | Not published | X, 54K views |
| 140 | [Open-world pelican bike game across Google's campus](cases/games/140-open-world-pelican-bike-game-across-google-s-campus.md) | [@agenticjay](https://x.com/agenticjay) | Not published | X, 1,249 views |
| 141 | [Glassy Jenga physics game you can play by sound](cases/games/141-glassy-jenga-physics-game-you-can-play-by-sound.md) | [@AI_Andrew](https://x.com/AI_Andrew) | Not published | X, 18K views |
| 142 | [Rebuilding a Fable-made shooter from its gameplay video](cases/games/142-rebuilding-a-fable-made-shooter-from-its-gameplay-video.md) | [@mylifcc](https://x.com/mylifcc) | Request only | X, 7,165 views |
| 143 | [Boat racing game from a single prompt](cases/games/143-boat-racing-game-from-a-single-prompt.md) | [@athrix_codes](https://x.com/athrix_codes) | Not published | X, 1,176 views |
| 144 | [Pelican riding a bicycle turned into a game](cases/games/144-pelican-riding-a-bicycle-turned-into-a-game.md) | [@xluchuan](https://x.com/xluchuan) | Not published | X, 1,879 views |
| 145 | [Game rebuild from an Omni video that became a new game](cases/games/145-game-rebuild-from-an-omni-video-that-became-a-new-game.md) | [@gigabit_million](https://x.com/gigabit_million) | Not published | X, 779 views |
| 146 | [One-shot Mario-style 3D platformer via Vertex AI](cases/games/146-one-shot-mario-style-3d-platformer-via-vertex-ai.md) | [@Delroy715](https://x.com/Delroy715) | Not published | X, 4,366 views |
| 147 | [Simple racing game from a first test](cases/games/147-simple-racing-game-from-a-first-test.md) | [@bei351009016](https://x.com/bei351009016) | Not published | X, 2,087 views |
| 148 | [Desk Racer, a miniature kart game in the browser](cases/games/148-desk-racer-a-miniature-kart-game-in-the-browser.md) | [@anuragdotdev](https://x.com/anuragdotdev) | Request only | X, 1,022 views |
| 149 | [NIGHTSHIFT highway racing game built twice: Carbon vs Fable 5.2](cases/games/149-nightshift-highway-racing-game-built-twice-carbon-vs-fable-5.md) | Ediz Ege Mercan (GitHub EddizEge) | Not published | blog |
| 150 | [Cozy medieval diorama builder in a single 930 KB HTML file](cases/games/150-cozy-medieval-diorama-builder-in-a-single-930-kb-html-file.md) | FireTable | Full prompt | GitHub |
| 151 | [First-person battle mage game, judged blind: Fable 5.2 vs Carbon](cases/games/151-first-person-battle-mage-game-judged-blind-fable-5-2-vs.md) | Sound Human : Stop Slop | Full prompt | YouTube |
| 152 | [3D kart racer on a giant dinner table, $7 per model](cases/games/152-3d-kart-racer-on-a-giant-dinner-table-7-per-model.md) | AI That Works | Request only | YouTube |
| 153 | [Browser-playable FPS game from a one-sentence prompt](cases/games/153-browser-playable-fps-game-from-a-one-sentence-prompt.md) | SmartDeng_ | Not published | Bilibili |
| 154 | [Bridge-building contest re-run with Gemini models in Antigravity](cases/games/154-bridge-building-contest-re-run-with-gemini-models-in.md) | tzt诶喂 | Not published | Bilibili |
| 155 | [Fall Guys-style party game from scratch: Carbon vs Argon vs Fable 5.2](cases/games/155-fall-guys-style-party-game-from-scratch-carbon-vs-argon-vs.md) | GameAGI | Not published | YouTube |

## Simulations, Science and Engineering

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/simulations](https://apimodels.app/gemini-4-carbon-prompts/simulations)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 156 | [Closed-loop FEA-to-CAD part design](cases/simulations/156-closed-loop-fea-to-cad-part-design.md) | [@adamdotnew](https://x.com/adamdotnew) | Not published | X, 17K views |
| 157 | [Interactive 19th-century Parisian physics lab from one reference image](cases/simulations/157-interactive-19th-century-parisian-physics-lab-from-one.md) | [@thebuggeddev](https://x.com/thebuggeddev) | Not published | X, 51K views |
| 158 | [Cinematic 3D black hole simulation in pure code](cases/simulations/158-cinematic-3d-black-hole-simulation-in-pure-code.md) | [@pankajkumar_dev](https://x.com/pankajkumar_dev) | Request only | X, 3,564 views |
| 159 | [Humanoid robot simulation with six motion modes](cases/simulations/159-humanoid-robot-simulation-with-six-motion-modes.md) | [@masahirochaen](https://x.com/masahirochaen) | Full prompt | X, 11K views |
| 160 | [Electric motor and generator demo after a three-hour run](cases/simulations/160-electric-motor-and-generator-demo-after-a-three-hour-run.md) | [@akokoi1](https://x.com/akokoi1) | Not published | X, 8,747 views |
| 161 | [City subway simulator with POV mode and passengers](cases/simulations/161-city-subway-simulator-with-pov-mode-and-passengers.md) | [@jerrod_lew](https://x.com/jerrod_lew) | Not published | X, 1,033 views |
| 162 | [Periodic table of the elements made with Carbon](cases/simulations/162-periodic-table-of-the-elements-made-with-carbon.md) | [@mylifcc](https://x.com/mylifcc) | Not published | X, 1,411 views |

## Films, Music Videos and Sound

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/film-music](https://apimodels.app/gemini-4-carbon-prompts/film-music)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 163 | [Full music video made with only code](cases/film-music/163-full-music-video-made-with-only-code.md) | [@kickingkeys](https://x.com/kickingkeys) | Not published | X, 12K views |
| 164 | [Animated scene from one reference image in pure JS and Python](cases/film-music/164-animated-scene-from-one-reference-image-in-pure-js-and.md) | [@devteamdrew](https://x.com/devteamdrew) | Not published | X, 14K views |
| 165 | [Fifty-second Halloween walk with stereo audio](cases/film-music/165-fifty-second-halloween-walk-with-stereo-audio.md) | [@abhinavflac](https://x.com/abhinavflac) | Not published | X, 12K views |
| 166 | [Three-minute looping solo violin concert film from a long spec](cases/film-music/166-three-minute-looping-solo-violin-concert-film-from-a-long.md) | [@IamEmily2050](https://x.com/IamEmily2050) | Excerpt | X, 5,050 views |
| 167 | [Music prototype built from everyday sounds](cases/film-music/167-music-prototype-built-from-everyday-sounds.md) | [@alexanderchen](https://x.com/alexanderchen) | Not published | X, 17K views |
| 168 | [Short film made with plain code](cases/film-music/168-short-film-made-with-plain-code.md) | [@jony_palino](https://x.com/jony_palino) | Not published | X, 4,501 views |
| 169 | [Original song and music video with Carbon and a cloud GPU](cases/film-music/169-original-song-and-music-video-with-carbon-and-a-cloud-gpu.md) | [@shengtang135754](https://x.com/shengtang135754) | Not published | X, 4,728 views |
| 170 | [Music video showing off Carbon from a one-line prompt](cases/film-music/170-music-video-showing-off-carbon-from-a-one-line-prompt.md) | [@itnavi2022](https://x.com/itnavi2022) | Full prompt | X, 3,306 views |
| 171 | [Three-minute solo piano concert film of Beethoven's Allegretto](cases/film-music/171-three-minute-solo-piano-concert-film-of-beethoven-s.md) | [@IamEmily2050](https://x.com/IamEmily2050) | Request only | X, 3,010 views |
| 172 | [ETH versus BTC since 2015 video rendered in C++](cases/film-music/172-eth-versus-btc-since-2015-video-rendered-in-c.md) | [@losingle](https://x.com/losingle) | Full prompt | X, 704 views |
| 173 | [Period-drama short film with Carbon directing the pipeline](cases/film-music/173-period-drama-short-film-with-carbon-directing-the-pipeline.md) | [@shengtang135754](https://x.com/shengtang135754) | Not published | X, 2,829 views |
| 174 | [Arknights "Melantha" narrative music video built in Blender](cases/film-music/174-arknights-melantha-narrative-music-video-built-in-blender.md) | xplunger1337 | Full prompt | Bilibili |
| 175 | [Short films from 2,000 Higgsfield credits: Fable 5.2 vs Carbon](cases/film-music/175-short-films-from-2-000-higgsfield-credits-fable-5-2-vs.md) | Adam Campbell Cinema | Not published | YouTube |
| 176 | [From a 30-second dinosaur doodle to a 30-second film](cases/film-music/176-from-a-30-second-dinosaur-doodle-to-a-30-second-film.md) | Forn AI | Not published | YouTube |
| 177 | [Pure-code short film answering a Fable 5.2 film](cases/film-music/177-pure-code-short-film-answering-a-fable-5-2-film.md) | 花家颜 | Not published | Bilibili |
| 178 | [Stickman wuxia fight animation: Fable 5.2 vs Carbon](cases/film-music/178-stickman-wuxia-fight-animation-fable-5-2-vs-carbon.md) | Vzerolin | Not published | Bilibili |
| 179 | [Dance music video for "Claude-chan", led by Carbon](cases/film-music/179-dance-music-video-for-claude-chan-led-by-carbon.md) | hero1157 | Not published | Bilibili |
| 180 | [Recreating a Fable-made video, "Chinatown after the rain"](cases/film-music/180-recreating-a-fable-made-video-chinatown-after-the-rain.md) | 法斯特咱有 | Not published | Bilibili |
| 181 | [Same-prompt 3D rocket launch animation, judged blind by viewers](cases/film-music/181-same-prompt-3d-rocket-launch-animation-judged-blind-by.md) | 白色so | Not published | Bilibili |
| 182 | [/swarm art piece: 6,000 years of pelicans riding bicycles](cases/film-music/182-swarm-art-piece-6-000-years-of-pelicans-riding-bicycles.md) | orbitooo | Full prompt | Bilibili |
| 183 | [Yonkers stands up as a mech and stomps around NYC](cases/film-music/183-yonkers-stands-up-as-a-mech-and-stomps-around-nyc.md) | Simon Willison (simonw) | Full prompt | blog |
| 184 | [One-sentence video in Antigravity with every tool enabled](cases/film-music/184-one-sentence-video-in-antigravity-with-every-tool-enabled.md) | LRN095 | Not published | Bilibili |

## SVG, Drawing and 2D Animation

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/svg-2d](https://apimodels.app/gemini-4-carbon-prompts/svg-2d)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 185 | [Painting app that paints a portrait from a photo](cases/svg-2d/185-painting-app-that-paints-a-portrait-from-a-photo.md) | [@CodeByPoonam](https://x.com/CodeByPoonam) | Not published | X, 51K views |
| 186 | [Rainy-night SVG girl with an original music loop](cases/svg-2d/186-rainy-night-svg-girl-with-an-original-music-loop.md) | [@chetaslua](https://x.com/chetaslua) | Not published | X, 33K views |
| 187 | [Banana gondola illustration for the Banana Test](cases/svg-2d/187-banana-gondola-illustration-for-the-banana-test.md) | [@AdamHoltererer](https://x.com/AdamHoltererer) | Not published | X, 5,673 views |
| 188 | [SVG of crabs closing in on a cycling pelican](cases/svg-2d/188-svg-of-crabs-closing-in-on-a-cycling-pelican.md) | [@HarshithLucky3](https://x.com/HarshithLucky3) | Request only | X, 3,123 views |
| 189 | [SVG portrait of Sung Jinwoo with background music](cases/svg-2d/189-svg-portrait-of-sung-jinwoo-with-background-music.md) | [@notjazii](https://x.com/notjazii) | Request only | X, 13K views |
| 190 | [Galloping horse in pixel art](cases/svg-2d/190-galloping-horse-in-pixel-art.md) | [@AdamHoltererer](https://x.com/AdamHoltererer) | Not published | X, 1,969 views |
| 191 | [Lion juggling on a bicycle through four seasons](cases/svg-2d/191-lion-juggling-on-a-bicycle-through-four-seasons.md) | [@SahilPanhotra](https://x.com/SahilPanhotra) | Request only | X, 1,720 views |
| 192 | [Pelican on a bicycle in the Gemini app](cases/svg-2d/192-pelican-on-a-bicycle-in-the-gemini-app.md) | [@leo114119](https://x.com/leo114119) | Not published | X, 1,956 views |
| 193 | [SVG of a border collie riding a zebra riding a bicycle](cases/svg-2d/193-svg-of-a-border-collie-riding-a-zebra-riding-a-bicycle.md) | [@xueyu1125](https://x.com/xueyu1125) | Full prompt | X, 1,331 views |
| 194 | [Pelican animation with auto-click demo exported to MP4](cases/svg-2d/194-pelican-animation-with-auto-click-demo-exported-to-mp4.md) | [@xluchuan](https://x.com/xluchuan) | Not published | X, 856 views |
| 195 | [Detailed pelican on a bicycle on High in the Gemini app](cases/svg-2d/195-detailed-pelican-on-a-bicycle-on-high-in-the-gemini-app.md) | [@EdwinCh43136084](https://x.com/EdwinCh43136084) | Not published | X, 2,207 views |
| 196 | [Broken pelican output through a DeepSeek harness proxy](cases/svg-2d/196-broken-pelican-output-through-a-deepseek-harness-proxy.md) | [@leo114119](https://x.com/leo114119) | Not published | X, 697 views |
| 197 | [Reusing an Opus 5.5 "6,000 years of pelicans" prompt on Carbon](cases/svg-2d/197-reusing-an-opus-5-5-6-000-years-of-pelicans-prompt-on-carbon.md) | 羽升AI实践分享 | Not published | Bilibili |
| 198 | [Pelican-on-a-bicycle comparison site across four harnesses](cases/svg-2d/198-pelican-on-a-bicycle-comparison-site-across-four-harnesses.md) | CrazyRock114 | Not published | GitHub |
| 199 | [Pelican test: Fable 5.2 MAX vs Carbon](cases/svg-2d/199-pelican-test-fable-5-2-max-vs-carbon.md) | Lovely_Chuxue | Not published | Bilibili |
| 200 | [Pelican riding a horse: GPT gray-test model vs Carbon High](cases/svg-2d/200-pelican-riding-a-horse-gpt-gray-test-model-vs-carbon-high.md) | 不发光的偏方三八面体 | Not published | Bilibili |

## Apps, Real Codebases and Tooling

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/code](https://apimodels.app/gemini-4-carbon-prompts/code)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 201 | [Windows 11 running locally on a foldable iPhone](cases/code/201-windows-11-running-locally-on-a-foldable-iphone.md) | [@ammaar](https://x.com/ammaar) | Not published | X, 115K views |
| 202 | [New features for a floor plan generator](cases/code/202-new-features-for-a-floor-plan-generator.md) | [@chirovisuals](https://x.com/chirovisuals) | Not published | X, 4,256 views |
| 203 | [Shader fixes and QA for a Unity shadow-play video](cases/code/203-shader-fixes-and-qa-for-a-unity-shadow-play-video.md) | [@ShadeLurk](https://x.com/ShadeLurk) | Not published | X, 808 views |
| 204 | [Rerunning seven real business-code issues](cases/code/204-rerunning-seven-real-business-code-issues.md) | [@luoleiorg](https://x.com/luoleiorg) | Not published | X, 10K views |
| 205 | [Antigravity run that never edited a line of code](cases/code/205-antigravity-run-that-never-edited-a-line-of-code.md) | weiyunjun | Not published | V2EX |
| 206 | [44% prompt-cache hit rate for Factory-hosted gemini-4-carbon](cases/code/206-44-prompt-cache-hit-rate-for-factory-hosted-gemini-4-carbon.md) | marovole | Not published | GitHub |
| 207 | [Patching an abandoned fishing game's binary for diamond fish](cases/code/207-patching-an-abandoned-fishing-game-s-binary-for-diamond-fish.md) | gbolcer | Not published | GitHub |
| 208 | [Six merged production fixes replayed 20 times: Carbon vs Argon](cases/code/208-six-merged-production-fixes-replayed-20-times-carbon-vs.md) | paddo.dev | Not published | blog |
| 209 | [Long agentic coding sessions: Carbon vs Opus 5.5 vs Fable 5.2](cases/code/209-long-agentic-coding-sessions-carbon-vs-opus-5-5-vs-fable-5-2.md) | Bito | Not published | blog |
| 210 | [Strands SDK integration tests run against gemini-4-carbon](cases/code/210-strands-sdk-integration-tests-run-against-gemini-4-carbon.md) | strandly-the-agent | Not published | GitHub |
| 211 | [MCP connector for Carbon design reviews from inside Codex](cases/code/211-mcp-connector-for-carbon-design-reviews-from-inside-codex.md) | wpv-chan | Not published | GitHub |
| 212 | [Voice assistant from a PRD in 4.5 hours, plus bug fixes](cases/code/212-voice-assistant-from-a-prd-in-4-5-hours-plus-bug-fixes.md) | codeSTACKr | Not published | YouTube |

## Agents, Research and Writing

Browse this category with the videos playing: [https://apimodels.app/gemini-4-carbon-prompts/research](https://apimodels.app/gemini-4-carbon-prompts/research)

| # | Case | Creator | Prompt | Source |
| --- | --- | --- | --- | --- |
| 213 | [Agent teams find new exact solutions for fusion equations](cases/research/213-agent-teams-find-new-exact-solutions-for-fusion-equations.md) | [@lucasjvds](https://x.com/lucasjvds) | Not published | X, 248K views |
| 214 | [Carbon splitting a scene into tasks for a local model](cases/research/214-carbon-splitting-a-scene-into-tasks-for-a-local-model.md) | [@atomicagent_io](https://x.com/atomicagent_io) | Not published | X, 13K views |
| 215 | [Racing language models in a sailing simulator](cases/research/215-racing-language-models-in-a-sailing-simulator.md) | [@shekitup](https://x.com/shekitup) | Not published | X, 14K views |
| 216 | [Fourteen vertical data apps from public datasets](cases/research/216-fourteen-vertical-data-apps-from-public-datasets.md) | [@giyu_codes](https://x.com/giyu_codes) | Request only | X, 31K views |
| 217 | [Three cube moves performed with robot hands](cases/research/217-three-cube-moves-performed-with-robot-hands.md) | [@PhysAIAnalysis](https://x.com/PhysAIAnalysis) | Not published | X, 499 views |
| 218 | [Five-finger hand picking up an apple by its stem](cases/research/218-five-finger-hand-picking-up-an-apple-by-its-stem.md) | [@PhysAIAnalysis](https://x.com/PhysAIAnalysis) | Not published | X, 746 views |
| 219 | [Moving an apple over a wall onto a plate](cases/research/219-moving-an-apple-over-a-wall-onto-a-plate.md) | [@PhysAIAnalysis](https://x.com/PhysAIAnalysis) | Not published | X, 499 views |
| 220 | [Real robot told to fold a towel, without success](cases/research/220-real-robot-told-to-fold-a-towel-without-success.md) | [@sanatem](https://x.com/sanatem) | Full prompt | X, 344 views |
| 221 | [Five web-novel openings across five genres](cases/research/221-five-web-novel-openings-across-five-genres.md) | rbbbc | Not published | Bilibili |
| 222 | [One hard Sudoku, five tries each: Carbon vs Argon](cases/research/222-one-hard-sudoku-five-tries-each-carbon-vs-argon.md) | Singularity Feed (GitHub gnana70) | Not published | YouTube |
| 223 | [Reviewing an unfinished paper draft against other top models](cases/research/223-reviewing-an-unfinished-paper-draft-against-other-top-models.md) | 5555watch | Not published | Hacker News |

## Run it yourself

Call `gemini-4-carbon` on apimodels.app with an OpenAI-compatible request. Carbon thinks for a while before it answers, so raise the output limit, stream, and allow a long timeout:

```bash
curl https://api.apimodels.app/v1/chat/completions \
  -H "Authorization: Bearer $APIMODELS_API_KEY" \
  -H "Content-Type: application/json" \
  --max-time 900 \
  -d '{
    "model": "gemini-4-carbon",
    "reasoning_effort": "medium",
    "max_tokens": 32768,
    "stream": true,
    "messages": [{"role": "user", "content": "Build a 5,000-drone light show over a night waterfront. One HTML file. No external assets."}]
  }'
```

The native Gemini format works too: `POST https://api.apimodels.app/v1beta/models/gemini-4-carbon:generateContent`. Where else Carbon runs, why it sometimes does not, and the settings that matter: [How to use Gemini 4 Carbon](https://apimodels.app/how-to-use-gemini-4-carbon).

## FAQ

### Can Gemini 4 Carbon make 3D scenes, games or videos by itself?

Not directly. Carbon takes text, images, video, audio and PDFs and returns text. Every scene, game and film here was rendered from code it wrote: Three.js and WebGL pages, Blender Python, CUDA or C++ programs, Web Audio for sound. In a chat window you get the code or an HTML file; an agent such as Antigravity, Cursor or GitHub Copilot can run, render and test it.

### Which tool did people use?

Mostly Google's Antigravity, often with its /swarm multi-agent mode. Others used Cursor, GitHub Copilot, AI Studio, Vertex AI or the API from their own harness. Where the creator said, the case page names the tool.

### Is Carbon better than Claude Fable 5.2 for this kind of work?

Usually not on quality, often yes on cost. In most head-to-head tests here Fable 5.2 produced the better-looking, more complete result, while Carbon cost a fraction as much and sometimes won outright. Carbon also reads video, which several creators used to show it a reference.

### Is Carbon better than Gemini 4 Argon?

Mostly yes, at the cost of time and tokens. The two cost the same per token; Carbon usually produced the stronger result in these tests and took several times longer. Google still recommends Argon for most everyday coding.

### How much did these cost?

As the creators reported: $0.45 for a one-shot 3D platformer of 2,599 lines, $3.82 for the shooter rebuild, about $7.40 for four rounds of self-review, $7.54 for three jobs in one comparison and $27.68 for three long builds in another. Costs depend on thinking level and how long the agent runs.

### Can I reuse these prompts?

The works belong to their creators, and every case links to the original. Prompts are quoted with credit: in full when short, excerpted when long, and never filled in when unpublished. Check the original post before using a prompt commercially.

## Credits, copyright and licence

- **The works belong to their creators.** This repository hosts none of their videos, images or code; every case links to the original post or page.
- **Prompts are quoted with credit and a link.** Published prompts of up to 400 characters are quoted in full; longer ones are excerpted with a link to the full text; unpublished prompts are never filled in.
- Some cases recreate or pay homage to existing games, films, products or places, or come from companies showing their own products; the case notes say so. The rights in that source material belong to its owners.
- **Our own material** (the case write-ups, the summaries above and `data/cases.json`) is licensed under [CC BY 4.0](LICENSE). Please credit apimodels.app with a link.
- If you made one of these and want it removed or the credit corrected, open an issue and we'll handle it promptly.

Call Gemini 4 Carbon through apimodels.app: [model page](https://apimodels.app/models/gemini-4-carbon) · [how to use it](https://apimodels.app/how-to-use-gemini-4-carbon) · [API docs](https://apimodels.app/docs/llm)
