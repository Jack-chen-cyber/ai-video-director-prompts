# 04 — Liquid & Material Physics Prompts

Glass refraction, condensation, ice cubes, and slow-motion pours are where AI video shines—*if* you anchor refractive index and lighting direction in the still keyframe first.

---

## 1. Sparkling Citrus Beverage Pour

### Node 2 Keyframe
```text
High-speed commercial beverage photograph, 90mm macro lens, backlit studio strobe setup. Crystal-clear cut-glass tumbler packed with hand-carved transparent ice cubes resting on wet dark slate. Bright golden-amber sparkling citrus tonic illuminated from directly behind so effervescent micro-bubbles glow like champagne. Fine beads of cold condensation coat the exterior glass, crisp lime zest twist on the rim, deep obsidian studio background.
```

### Node 3 Motion (Slow-Motion Pour & Fizz)
```text
120fps high-speed macro cinema feel. A thin, laminar stream of golden sparkling tonic pours into the ice-filled glass from above frame, triggering an energetic cascade of tiny backlit bubbles rising through the crystal ice. Two condensation droplets glide slowly down the outer glass wall. Camera holds rock-steady with a subtle 5% push-in; glass geometry and ice edges stay crisp and refractive.
```

---

## 2. Luxury Perfume Mist & Caustics

### Node 2 Keyframe
```text
Architectural fragrance still life, 50mm medium-format lens. Heavy faceted crystal perfume flacon with a polished brushed-brass cap standing inside a shallow dark mirror tray of still water. A single tight studio Fresnel spotlight from upper-left projects dramatic diamond-like caustic light patterns across a matte warm terracotta plaster wall behind the bottle.
```

### Node 3 Motion (Fine Atomizer Mist)
```text
Slow, hypnotic 10% dolly-in. A delicate backlit plume of microscopic translucent fragrance mist drifts diagonally from upper-left through the tight Fresnel spotlight beam, catching tiny sparkling light particles. Gentle micro-ripples pulse outward in the shallow mirror water around the flacon base, casting shimmering golden caustics on the terracotta wall. Bottle and brass cap remain 100% rigid.
```

---

## Liquid Physics Prompt Tips
- **Specify lighting position**: Liquids look muddy without `backlit` or `rim-lit` cues.
- **Name the frame-rate feel**: Phrases like `120fps high-speed slow-motion feel` stabilize fluid trajectories much better than vague `slow motion`.
- **Separate rigid vs. fluid elements**: Explicitly state that the glass vessel remains `completely stationary and rigid` while only the liquid, bubbles, or mist move.
