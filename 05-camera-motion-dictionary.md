# 05 — Camera Motion & Micro-Physics Dictionary

A quick reference of **camera motion phrases that work reliably** across Kling, Seedance, Veo, Runway, and open-weights video models—and the risky phrases that cause geometry warping.

---

## Reliable Camera Moves (High Stability)

| Camera Move | Recommended Prompt Phrase | Best Use Case |
| :--- | :--- | :--- |
| **Slow Dolly-In** | `Slow, steady 12% forward dolly-in on a tripod rail` | Portraits, emotional beats, product hero reveals |
| **Subtle Pull-Back** | `Gentle controlled pull-back revealing surrounding environment` | Scene transitions, scale reveals |
| **Lateral Slider** | `Smooth 10% lateral truck left-to-right on a motorized slider` | Packshots, tabletop products, architectural parallax |
| **Restricted Arc** | `Controlled 20-degree orbital arc around the subject at eye level` | Adding 3D depth without warping logos or faces |
| **Rack Focus** | `Stationary lens executing a smooth rack focus from foreground to subject` | Macro hardware, jewelry, dramatic narrative shifts |
| **Locked Tripod** | `Static locked-off cinema camera on heavy tripod` | Liquid pours, mist, hair/fabric wind, subtle acting |

---

## High-Value Environmental Micro-Physics

When your camera move is subtle, **micro-physics** is what makes a clip feel shot on real cinema gear instead of a Ken Burns slideshow:

- **Water & Reflections**: `gentle concentric ripples bending the warm lantern reflection`
- **Atmosphere**: `slowly drifting twilight mist passing between background trees`
- **Light & Caustics**: `soft directional sunlight reflection gliding across brushed aluminum`
- **Human Micro-Motion**: `natural blink, subtle shoulder breathing, loose hair strands lifting in soft breeze`
- **Particles**: `microscopic dust motes / backlit fragrance mist floating through a tight Fresnel beam`

---

## Risky Phrases to Avoid (High Artifact Rate)

| Avoid Writing | Why It Fails | Use Instead |
| :--- | :--- | :--- |
| `360-degree fast orbit` | Hallucinates back-side geometry & melts text | `Controlled 20-degree arc` + cut to second locked angle |
| `FPV drone flying through keyhole` | Severe temporal morphing on real products/faces | `Steady forward dolly-in` with clean foreground parallax |
| `Dynamic chaotic action camera` | Triggers limb/finger duplication & shutter smear | `Subtle handheld documentary micro-drift` |
| `Zoom from macro eye to outer space` | Breaks optical continuity completely | Two separate locked keyframes connected by a clean edit cut |
