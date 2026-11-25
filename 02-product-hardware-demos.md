# 02 — Product & Hardware Demo Prompts (Anti-Warp)

Ask an AI video model to spin a technical product `360°` and every small logo, knurled dial, and brushed aluminum chamfer will melt by second 2. Real commercial product teams avoid full rotations and instead use **2-plate locked geometry + restricted `20°–35°` camera arcs**.

---

## 1. Plate A: Orthographic Hardware Hero Still (Node 1)

```text
Commercial industrial design studio photograph, 85mm macro tilt-shift lens, f/5.6. Matte anodized obsidian aluminum portable audio DAC resting on a honed travertine stone plinth. Precision CNC-machined copper volume dial with fine diamond knurling on the top-right corner, recessed micro-LED power indicator emitting a pinpoint warm white glow. Crisp, clean directional studio Fresnel rim light carving out the chamfered metallic edge against a deep architectural charcoal seamless backdrop. Zero floating UI, zero watermarks, ultra-sharp surface micro-texture.
```

---

## 2. Plate B: Detail Macro Keyframe (Node 2)

```text
Tight 100mm macro commercial photograph matching the exact obsidian aluminum DAC and knurled copper dial from Plate A. Camera positioned low at a 20-degree three-quarter angle focusing tightly on the copper knurling ridges and brushed aluminum bevel. Soft specular light sweep travels across the chamfered edge while the background stone plinth falls into creamy optical bokeh.
```

---

## 3. Node 3: Anti-Warp Video Motion Prompts (720p Draft)

### Shot 1 — Controlled Specular Light Sweep (Zero Geometry Distortion)
```text
Camera locked on a motorized macro slider executing a smooth 15-degree slow push-in toward the knurled copper dial. A soft vertical studio softbox reflection glides steadily across the matte black anodized body from left to right, revealing brushed metal grain and chamfer highlights. The product remains completely stationary and rigid—zero warping, zero bending, zero text hallucination.
```

### Shot 2 — Shallow Rack-Focus Reveal
```text
Stationary macro lens with a smooth cinematic rack focus shifting from the foreground travertine stone grain to razor-sharp focus on the diamond-knurled copper volume dial and warm white micro-LED. Subtle ambient light shimmer along the machined bevel, rock-solid rigid hardware geometry throughout.
```

---

## Anti-Warp Rules for Commercial Hardware
1. **Cap rotation at `<= 35°`**: Never prompt `360-degree turntable spin` unless working from a real 3D mesh render.
2. **Move light instead of rotating text**: Sweeping a studio reflection across a stationary hero angle looks more expensive and keeps branding 100% legible.
3. **Cut between 2 locked angles**: Edit a 2.5s wide hero push-in directly into a 2.5s macro detail rack-focus rather than asking one continuous shot to zoom `10x`.
