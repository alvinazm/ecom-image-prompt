# Fashion Main / Gallery Default Logic

When the task involves women's fashion, men's fashion, children's clothing, shoes, bags, accessories, outdoor wear, and other fashion categories for main and gallery images, default to using this logic to organize prompts. Main + gallery images are fundamentally a product lookbook: around the same garment, use different angles, different framing, and different poses to show fit, silhouette, fabric, detail, and styling contexts.

## Core Principles

- **Main image** drives first-click impression: model-worn, product fully visible, style clearly communicated. User must know instantly what's being sold.
- **Gallery images** carry the browsing experience: cannot just be slightly different versions of the same photo. Must vary by front, side, back, half-body, detail, and scene action shots.
- **Fashion main + gallery defaults to model + real scene.** Unless user explicitly requests flat-lay, ghost mannequin, or no-model shots, do not output empty garment or pure studio-only images.
- **When the user has not provided model info**, automatically fill in a reasonable model based on the garment style. **When the user has not provided a scene**, automatically fill in a suitable shooting scene based on season, silhouette, price tier, and reference image style.
- **Same set of main + gallery must feel like a single photoshoot**: same model, same hair/makeup/styling vibe, same garment, same core outfit pairing, same color tone and lighting.
- **Can switch camera positions within the same location** or transition from outdoor to adjacent indoor space, but do not jump to entirely different worlds per image.
- **Reference images** only inform shooting logic, model poses, framing, lighting, scene mood, and styling atmosphere. Do not copy the original model's identity, original brand, original copy, original store branding, or original product subject.

## Default Fill-in Rules

### When Model Info Is Missing

Auto-fill based on garment — do not stop to ask repeatedly:

- **Women's fashion**: Default Asian female model, 20-30 years old, natural fresh makeup, clean hairstyle, balanced figure, temperament matching the style.
- **Men's fashion**: Default male model, 20-35 years old, clean natural look, athletic-lean build, temperament matching commute, outdoor, or casual positioning.
- **Children's fashion**: Default child model at appropriate age, natural cute expressions, safe, bright, friendly imagery.
- **Unisex / cannot determine gender**: Default to the model most fitting the garment cut and target demographic. If still unclear, use "model with neutral, natural styling."
- **Do not** specify real celebrities, influencers, or reference-image identities. Only describe age range, temperament, hair/makeup, and poses.

### When Scene Info Is Missing

Auto-fill a common Shopify fashion scene based on garment style:

- **Soft minimal / Scandinavian / everyday women's**: Café terrace, textured concrete wall, greenery, cobblestone path, natural daylight street corner, clean indoor café space.
- **Commute / tailored / elevated basics**: Light grey urban street, modern office exterior, minimalist interior, clean white wall, natural window light.
- **Light outdoor / travel / sun-protective**: Park trail, seaside boardwalk, urban greenway, camping meadow, sunny street corner.
- **Athleisure / performance / technical**: Urban outdoor, mountain trail, sports field, cycling path, crisp light with dynamic feel.
- **Loungewear / sleepwear / intimates**: Bright bedroom, soft-furnished living room, window-side, light bedding or sofa.

If user provided reference images but didn't specify a scene, prioritize extracting the scene mood from the references. E.g. reference could be reverse-engineered as "light outdoor café terrace, natural light, textured wall, greenery, cobblestone, coffee in hand, relaxed lifestyle feel."

## Default Lookbook Structure

Main × 1 + Gallery × 4–6, priority order:

1. **Main**: Front or 3/4 front, full-body or knee-up composition, model-worn fully visible, product is the first visual focal point.
2. **Gallery 1**: Full-body front or walking pose. Show overall styling proportions, length, silhouette.
3. **Gallery 2**: 3/4 side or side-glance-back. Show garment drape, sleeve shape, shoulder line, ease.
4. **Gallery 3**: Back view or turning angle. Show back panel, hem, overall silhouette from behind.
5. **Gallery 4**: Half-body close-up. Show collar, buttons, drawstrings, embroidery, pattern, fabric texture in detail.
6. **Gallery 5**: Scene action shot. Sitting, walking, holding coffee, carrying bag, adjusting hat, fixing hem — emphasize real wear feel.
7. **Gallery 6**: Optional infographic or variant carry-through. Show color options, sizing, fabric benefits. Only include specific sizes and specs when user provides data.

If user only wants 4 gallery images, keep "full front, side/3/4, detail close-up, scene action." If user wants more, expand with back view, styling, fabric, sizing, color variants.

## Frame Variation Requirements

Each image must explicitly state what changed from the previous shot:

- **Angle variation**: Front, 3/4, side, back, slightly high, slightly low.
- **Framing variation**: Full body, knee-up, half-body, chest-up, detail macro.
- **Pose variation**: Standing, walking, looking back, hand tucking hair, holding cup, carrying bag, hands in pockets, adjusting hat brim.
- **Information variation**: Silhouette, fabric, detail, styling, scene, sizing, or color options.

Avoid writing vague prompts like "same model same scene take a few nice photos." Every gallery image must have a clear task.

## Main Image Prompt Framework

```text
Generate a Shopify fashion main image, 1:1 or 3:4 ratio. Product is {garment category, color, fabric, fit, key details}. {Model description} wearing, {scene description}, natural authentic fashion photography feel.

Composition: Model front or 3/4 front, product fully visible and clear, subject occupies 65%-80% of frame, garment silhouette, color, fabric texture, and key details accurate. Background has lifestyle feel but does not overpower the product.

Visual style: {soft minimal / outdoor lifestyle / tailored commute / premium studio / athleisure / etc.}, lighting {natural daylight / soft window light / crisp daylight}, color tone harmonious with product color.

Requirements: No text, no watermark, no heavy filters. Do not alter garment silhouette or color. Do not copy reference model identity, brand marks, or store identifiers.
```

## Gallery Image Prompt Framework

```text
Generate a Shopify fashion gallery image #{N}, 1:1 or 3:4 ratio. This image's task: {overall silhouette / side profile / back view / fabric detail / collar & cuff detail / scene styling / size info / color variant}.

Product consistency: {garment category, color, fabric, fit, key details} — same garment as main image, same {model description}, continuing the same {scene, lighting, color tone, styling, props}.

Frame variation: This image uses {angle}, {framing}, {pose}, focuses on {this image's information point}. Do not repeat the same pose as the main image.

Requirements: Authentic Shopify fashion lookbook photography. Product clearly visible without obstruction. Silhouette accurate. Color stable. No watermark. Only include text for sizing, specs, or campaign info when provided by user; otherwise default to no text.
```

## Reference Style Extraction Example

When user provides references like "cream yellow embroidered blouse + caramel shorts + café terrace / textured wall / greenery / cobblestone," extract as:

- **Style**: Soft minimal lifestyle, editorial street style.
- **Model**: Female, 20-30, natural makeup, soft waves or natural hair, warm and approachable.
- **Scene**: Café terrace, grey textured wall, greenery, cobblestone path, natural daylight. Can also extend to adjacent indoor café space.
- **Props**: Coffee cup in hand, woven bag, minimalist sandals — as styling atmosphere, not overpowering garment.
- **Composition**: Main front/3/4 knee-up or full-body. Gallery uses full-body walking, side profile, half-body close-up, hair-tucking, coffee-holding variations.
- **Forbidden**: Do not copy reference image text signage, store branding, model likeness, or original product details. Only keep shooting logic and atmosphere.
