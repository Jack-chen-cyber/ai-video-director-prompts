# 01 — Character & Narrative Consistency Prompts

Multi-shot narrative videos break when the model has to re-imagine the actor's face, hairstyle, and wardrobe on every cut. Always lock identity in **Node 1** before staging scenes in **Node 2** and animating in **Node 3**.

---

## 1. Node 1: 3-View Studio Character Turnaround Sheet

Use this prompt in your preferred high-control image model to build a reusable visual anchor:

```text
Clean editorial casting turnaround sheet on a seamless warm light-grey studio cyclorama (#E8E6E1). Three full upper-body poses of the exact same 24-year-old East Asian woman arranged side-by-side: left = direct front view, center = 3/4 view, right = clean side profile. Natural arched eyebrows, expressive dark eyes, loose dark chestnut hair tucked behind one ear. Wearing a structured olive-moss tailored wool trench coat with matte horn buttons over an ivory rib-knit mock neck. Even diffused softbox studio lighting, crisp fabric weave detail, neutral calm expression, zero text overlays, zero watermarks, 16:9 sheet.
```

### Why This Works
- **Neutral studio cyclorama** prevents dramatic colored shadows from baking into the character reference.
- **Concrete wardrobe anchors** ("matte horn buttons", "ivory rib-knit mock neck") give downstream nodes unambiguous geometry to preserve.

---

## 2. Node 2: Frozen Scene & Lighting Keyframe

Pass the Node 1 turnaround sheet as your image reference and lock the exact environment and practical light source:

```text
Cinematic medium-format film still, 35mm anamorphic lens, shallow depth of field. Using the exact woman and olive-moss wool trench coat from the turnaround reference, stage her standing at the edge of a mirror-still forest pond at twilight. She holds a warm glowing amber blown-glass lantern near chest height. Soft golden tungsten light illuminates her face, hand, and wool collar; deep slate-blue twilight mist wraps the background pines. Crisp vertical reflection of the lantern light on dark water, subtle 35mm Kodak Vision3 grain, no text.
```

---

## 3. Node 3: 720p Camera-Only Motion Prompts

### Shot A — Slow Dolly-In (Establishing Mood)
```text
Slow, controlled 15% forward dolly-in on a stabilized rail. Gentle ripples expand slowly across the dark pond surface, bending the amber lantern reflection. Soft evening breeze shifts loose hair strands near her cheek and gently drifts background mist. Natural blink, calm steady gaze. Preserve exact face geometry, coat texture, and twilight color palette.
```

### Shot B — Subtle Over-the-Shoulder / Profile Shift
```text
Gentle 10-degree lateral arc to the right at eye level. Warm lantern glow stays steady on her wool collar as mist drifts slowly through the distant trees. Subtle breathing motion in shoulders, no sudden head turns, no morphing of coat buttons or glass lantern shape.
```

---

## Common Failure Modes & Fixes

| Failure Mode | Root Cause | Fix |
| :--- | :--- | :--- |
| Face shifts mid-clip | Rapid head turn (`> 45°`) without profile reference | Include profile view in Node 1 and restrict head motion to subtle tilts |
| Coat color drifts to brown/black | Ambiguous color naming under colored light | Pair concrete material + color ("olive-moss wool") with a separate warm key light |
| Flickering hands around props | Complex finger gripping motion requested in video prompt | Keep hands resting/holding steady in Node 2; animate only camera + ambient physics |
