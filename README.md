# AI Video Director Prompts 🎬

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Workflow: 3-Node State-Locked](https://img.shields.io/badge/Workflow-3--Node%20State--Locked-10b981.svg)](#the-3-node-director-framework)
[![Models: Kling · Seedance · Veo · Runway](https://img.shields.io/badge/Models-Kling%20%C2%B7%20Seedance%20%C2%B7%20Veo%20%C2%B7%20Runway-6366f1.svg)](#multi-model-routing-cheat-sheet)

A model-agnostic, production-tested collection of **multi-shot AI video prompts, camera movement vocabulary, and state-locked filmmaking workflows**.

Built for independent creators, commercial directors, and engineers tired of "slot-machine text-to-video prompting" where characters morph, product labels warp, and lighting flips between Shot 1 and Shot 2.

---

## Why Single-Prompt Video Fails (And How to Fix It)

When you ask a text-to-video model to invent **character anatomy**, **wardrobe/product texture**, **scene lighting**, and **camera physics** in a single prompt, every new generation re-rolls all four variables at once. Writing longer 200-word prompts actually increases instability.

### The 3-Node Director Framework

Instead of cramming everything into one text box, decouple your production into three locked visual states:

```text
[Node 1: Orthographic Reference Sheet]   -> Locks face, hair, wardrobe, or product geometry
                 │
                 ▼
[Node 2: Frozen Lighting Keyframe]       -> Locks exposure, lens perspective, mist, reflections
                 │
                 ▼
[Node 3: 720p Camera-Only Motion Pass]   -> Animates camera trajectory & environmental micro-physics
```

**Golden Rule**: Never describe your character's face or your product's logo inside the Node 3 video prompt if it is already locked in the Node 2 keyframe. Keep Node 3 prompts strictly about **motion, lens behavior, and ambient physics**, and draft pacing at **720p** before upscaling hero cuts.

---

## Prompt Packs

| # | Prompt Pack | Best For | Key Technique |
| :-: | :--- | :--- | :--- |
| 01 | [Character & Narrative Consistency](01-character-consistency.md) | Short films, brand mascots, multi-shot stories | 3-view studio turnaround + frozen twilight keyframe |
| 02 | [Product & Hardware Demos](02-product-hardware-demos.md) | Consumer electronics, beauty, industrial design | 2-plate anti-warp macro + controlled 20°–35° arc |
| 03 | [High-Converting Video Ads](03-high-converting-video-ads.md) | Paid social, DTC e-commerce, SaaS launches | 3-second visual hook + modular 3-beat shot list |
| 04 | [Liquid & Material Physics](04-liquid-and-material-physics.md) | Beverages, perfume, glass, chrome & textiles | Caustics lock + high-speed micro-motion cues |
| 05 | [Camera Motion Dictionary](05-camera-motion-dictionary.md) | Universal motion prompting across all models | Reliable lens moves vs. artifact-prone keywords |

---

## Quick-Start Example (Copy & Paste)

### Node 2 — Frozen Keyframe Prompt
```text
Editorial medium-format film still, 35mm lens at f/2.8. The exact subject from the 3-view reference sheet stands beside a still dark forest pond at blue hour, holding a warm amber blown-glass lantern at chest height. Soft golden practical light wraps across her cheekbone and wool coat collar; cool indigo twilight mist drifts behind dark pine silhouettes. Crisp water reflection of the lantern glow, natural film grain, zero UI text.
```

### Node 3 — Camera-Only Image-to-Video Motion Prompt (720p Draft)
```text
Slow, steady 12% forward dolly-in on a tripod slider. Gentle concentric ripples move across the dark pond surface, catching warm amber lantern reflections. Subtle twilight breeze lifts loose strands of hair and softens drifting background mist. Subject blinks naturally and slightly tilts chin toward the lantern light. Maintain exact facial structure, coat texture, and twilight exposure throughout.
```

---

## Multi-Model Routing Cheat Sheet

Different shots benefit from different motion engines. In practice, mixing models per shot outperforms forcing one model to do everything:

| Shot Type | Recommended Engines | Motion Prompt Strategy |
| :--- | :--- | :--- |
| **Dialogue / Subtle Human Expression** | Seedance 2.5, Kling 2.x, Veo 3 | Minimal head movement, focus on eye-line, breathing, and natural blink |
| **Hardware / Product Macro Reveal** | Kling 2.x, Runway Gen-4 | Restrict camera arc to `<= 35°` to prevent label/text hallucination |
| **Liquid Pour / Caustics / Smoke** | Veo 3, Seedance 2.5 | Specify viscosity, slow-motion cadence (`120fps feel`), and specular highlight drift |
| **Wide Atmospheric Establishing Shot** | Veo 3, Runway Gen-4, Luma | Slow lateral truck or gentle drone push; avoid rapid whip pans |
| **Long-Take Native Audio (20–30s)** | MAGI-2 (480B MoE), Seedance 2.5 | Anchor 3-view turnaround + frozen keyframe even with 20-item Omni-Reference to avoid multi-character blending |

### Running the 3-Node Graph in Practice

You can run Node 1 → Node 2 → Node 3 manually by hopping between separate image and video tabs, or wire them on a unified multi-model canvas so reference plates stay attached across shots. Useful workflow tools & references:

- **Multi-model canvas**: [PixTV AI Video Generator](https://www.pixtv.ai/ai-video-generator) (lets you keep Node 1 & Node 2 image plates locked on one board while routing shots across Seedance, Kling, Veo, and Runway)
- **Product demo reference**: [AI Product Video Generator Workflow](https://www.pixtv.ai/ai-product-video-generator) (2-plate hardware & label preservation patterns)
- **Performance ad reference**: [AI Marketing Video Generator Patterns](https://www.pixtv.ai/ai-marketing-video-generator) (3-second hook & modular ad testing)
- **Standalone engines**: Runway, Kling AI, Google Veo, Luma Dream Machine, ComfyUI local pipelines
- **Frontier model benchmark notes**: [MAGI-2 vs. Seedance 2.5 (2026 Comparison)](https://www.pixtv.ai/blog/magi-2-vs-seedance-2-5-comparison) (Video Arena v2.1 Elo, 8x H100 self-hosting reality, and 720p workflow cost control)

---

## Contributing

Pull requests with verified, reproducible prompt pairs (especially before/after failure-mode fixes across Kling, Seedance, Veo, Runway, or open-weights models like Wan/HunyuanVideo) are very welcome!

Please include:
1. Target model & resolution (`720p` / `1080p`)
2. Reference plate strategy (Turnaround / Keyframe / Text-only)
3. Exact prompt & observed failure modes avoided

## License

MIT License — free to use, adapt, and remix in personal or commercial pipelines. See [LICENSE](LICENSE).
