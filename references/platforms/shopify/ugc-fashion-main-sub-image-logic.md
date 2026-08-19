# UGC Fashion Main / Gallery — Mixed Strategy (UGC Scene + Phone-UGC)

When the task involves UGC-style fashion e-commerce (Djerf Avenue, Réalisation Par, House of Sunny, influencer-led Shopify boutiques, "real girl" aesthetic, social-native fashion stores), default to this logic.

## The Mixed Strategy

UGC for fashion is NOT one style — it's two. A strong Shopify listing uses **both**:

| Style | Feel | Camera | Role | Examples |
|-------|------|--------|------|----------|
| **UGC Scene** | Aspirational, "I want that life" | Photographer-level (good camera, natural light, real location) | **Click-through + desire** — main image + first half of gallery | Djerf homepage (golden-hour beach, wheat field, city street) |
| **Phone-UGC** | Trust, "real girls actually wear this" | Actual phone camera roll (iPhone front/back, mirror selfie, friend snap) | **Trust + conversion** — second half of gallery | Mirror selfies, messy bedroom, parking lot, café table |

**The gallery flows from aspiration → trust.** First half makes them click. Second half makes them buy.

---

## Default 8-Image Structure (1 Main + 7 Gallery)

```
Main     [UGC Scene]   — Hero moment: golden-hour beach / field / street, aspirational
Gallery:
  G1     [UGC Scene]   — Full outfit / styling context: city street, coffee in hand
  G2     [UGC Scene]   — Side / motion: walking, turning, drape + silhouette
  G3     [UGC Scene]   — Detail close-up: fabric + key details in natural light
  G4     [Phone-UGC]   — Mirror selfie: bathroom or bedroom, phone in hand
  G5     [Phone-UGC]   — Candid friend snap: parking lot / café, genuine laugh
  G6     [Phone-UGC]   — Home timer selfie: cross-legged on bed, messy room
  G7     [Phone-UGC]   — Kitchen / getting-ready: friend grab shot, real clutter
```

**Ratio: 4 UGC Scene + 4 Phone-UGC.** Scene images lead. Phone images close.

---

## Part A: UGC Scene (Gallery G1-G3)

Shot by someone with a good eye and a decent camera, but in a real location. Think Djerf Avenue homepage: editorial composition in wheat fields, beaches, cobblestone streets — aspirational but never studio-fake.

### Key Characteristics

- Camera: mirrorless camera or high-end phone, NOT studio DSLR with heavy bokeh. Natural aperture.
- Light: golden hour, overcast diffused daylight, window light. Never studio flash.
- Location: real places with texture — beach at sunset, wheat field, cobblestone alley, corner café terrace, sun-drenched apartment.
- Model direction: relaxed, natural expression, slight movement — walking, adjusting hair, looking over shoulder, mid-laugh.
- Color: warm, slightly film-like. Cream, beige, terracotta, muted sage, warm grey.
- Props: coffee cup, straw tote, bicycle, sun hat, book, sunglasses. One or two max.

### UGC Scene Prompt Framework

```text
PRODUCT FIDELITY — copy exactly from reference: {garment category, color, fabric, piping/seams, key details}. The reference is the ground truth for the garment. No added patterns, no color shifts.

STYLE — UGC Scene fashion photograph, editorial composition in a real location. Shot with a mirrorless camera at natural aperture, golden-hour or soft overcast daylight, warm film-like tones. The image should feel aspirational and real at the same time — a candid moment captured well, NOT a studio fashion campaign.

SUBJECT — woman in her mid-20s, natural makeup, relaxed expression, slight smile, {pose — walking / looking over shoulder / adjusting hair / holding coffee / mid-laugh}.

SCENE — {real location with texture — cobblestone street corner, beach at sunset, wheat field, corner café terrace, sun-drenched apartment window, tree-lined park path}.

COMPOSITION — {1:1 or 3:4}, {full body / knee-up / 3/4 view}, garment clearly visible, natural negative space, warm natural light.

REQUIREMENTS — No text, no watermark, no studio backdrop, no fashion-editorial over-retouching, no harsh flash. Garment colors and details must match reference exactly.
```

---

## Part B: Phone-UGC (Gallery G4-G7)

**Shot on a real phone camera roll.** This is the "a friend took it" or "I took a mirror selfie" energy. These images close the trust gap: "regular people like me actually wear this."

### Phone-UGC Critical Rules

1. **PRODUCT FIDELITY** — always at the top of every prompt. Copy exactly from reference. Explicitly add `no stripes, no prints, no patterns whatsoever.`
2. **Pixel-level defects** — do NOT say "shot on iPhone." Say: `barrel distortion at edges, visible ISO noise in shadow areas, auto-HDR clipping on bright windows, phone-level sharpness with soft edges, JPEG compression artifacts, slight finger blur at frame edge, front-camera wide-angle distortion, slight underexposure from auto-metering.`
3. **Mundane, ugly-real settings** — do NOT say "apartment." Say: `small messy rental apartment bedroom, unmade IKEA duvet, charging cable on floor, pile of clothes on chair, cheap curtains, stained pillowcase.` The mess IS the authenticity signal.
4. **Ordinary person, NOT model** — do NOT say "natural beauty." Say: `ordinary woman, NOT a model, NOT an influencer, natural skin with visible texture and 1-2 blemishes, slightly shiny nose, no contour makeup, hair in messy bun actively falling out, slight double chin from low camera angle.`
5. **Composition flaws on purpose** — `framing slightly crooked 2-3 degree tilt, subject slightly off-center, photographer's shadow or coffee cup visible at bottom of frame, mirror reflection showing phone.`

### Phone-UGC Prompt Framework

```text
PRODUCT FIDELITY — copy exactly from reference: {garment category, color, fabric, piping/seams, key details}. The reference image is the ground truth for the garment. No stripes, no prints, no patterns whatsoever.

PHOTOGRAPHY STYLE — {mirror selfie / friend candid / timer selfie / grab shot} on iPhone, phone direct-out JPEG, zero editing. Specific visual evidence: barrel distortion at edges, visible ISO noise, auto-HDR clipping, phone-level sharpness with soft edges, {framing flaws — slight tilt / off-center / photographer's coffee cup at bottom / phone visible in mirror / finger blur at edge}.

SUBJECT — ordinary woman in mid-20s, NOT a model, NOT an influencer. Natural skin with visible texture and 1-2 blemishes, slightly shiny nose, no contour makeup, hair in messy bun/claw clip. {Pose — genuine laugh mid-sentence / looking at reflection / slouched cross-legged on bed / caught off-guard}.

SCENE — {ugly-real location — messy rental apartment bedroom with unmade bed + charging cable + clothes on chair, basic bathroom with IKEA mirror + toilet in reflection + drugstore toiletries, strip-mall parking lot outside Target, Formica café table with coffee rings and chipped ceramic mug, kitchen with dishes in sink}.

COMPOSITION — vertical 3:4, {full body / half-body / seated}, dress clearly visible, real background not blurred away.

REQUIREMENTS — No text, no watermark, no brand logos, no studio backdrop, no beauty retouching. Garment colors and details must match reference exactly.
```

---

## Phone-UGC Gallery Slot Assignments

| Slot | Type | Scene | Key Phone Evidence |
|------|------|-------|--------------------|
| G4 | Mirror selfie | Bathroom, IKEA mirror propped on wall, toilet visible in reflection | Phone in hand covering face, front-camera barrel distortion, harsh overhead light, drugstore clutter |
| G5 | Friend candid | Strip-mall parking lot, car door open, Target/supermarket visible | Motion blur, slight underexposure, friend's shadow at frame bottom, beat-up Converse |
| G6 | Timer selfie | Unmade bed, rumpled blanket, charging cable, clothes on chair | Low-angle distortion, ISO noise, slight underexposure, slouched posture, double chin |
| G7 | Kitchen grab | Kitchen with dishes, friend leaned against counter, holding spatula/coffee | Finger blur at edge, auto-WB too warm, JPEG compression in dark cabinets, genuine laugh |

---

## Gallery Flow Diagram

```
[Main] ─UGC Scene──→ [G1] ─UGC Scene──→ [G2] ─UGC Scene──→ [G3] ─UGC Scene──→
               aspiration / desire / click-through

[G4] ─Phone-UGC──→ [G5] ─Phone-UGC──→ [G6] ─Phone-UGC──→ [G7] ─Phone-UGC
            trust / "real girls wear this" / conversion
```

---

## What to Avoid (All Images)

1. Studio white/color backgrounds — kills UGC for both styles.
2. Fashion-editorial over-posing — symmetrical stance, hands on hips, straight-on stare.
3. Heavy retouching or skin smoothing — even for UGC Scene, keep it natural.
4. Text, badges, price tags, banners — UGC images are text-free. The image sells.
5. Copying real influencers or celebrities — use archetypes only.
6. For Phone-UGC specifically: no professional lighting, no perfect symmetry, no models who look like they have a beauty team.

---

## Trigger Phrases

User can request this workflow with any of the following:

- "UGC 主副图 / UGC 风格 / UGC 套图"
- "Djerf Avenue 风格"
- "UGC Scene + Phone-UGC"
- "8 张 UGC 主副图"
- "UGC mixed strategy"

---

## How to Ask (提问方式)

最简触发：

```text
UGC 主副图，产品图是 @image#1，8 张
```

完整触发：

```text
@skill:shopify-image-generator
产品图：@image#1
风格：UGC 主副图（UGC Scene + Phone-UGC 混合），8 张
```

Skill 会自动：
1. 识别产品特征（颜色、面料、版型、滚边、蝴蝶结等）
2. 执行 PRODUCT FIDELITY 写入每张 prompt（防止漂移）
3. 生成 8 个 prompt：前 4 张 → UGC Scene，后 4 张 → Phone-UGC
4. 组织主副图输出，保证前后风格一致
