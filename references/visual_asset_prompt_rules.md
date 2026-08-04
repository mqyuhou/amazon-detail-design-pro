# Nano Banana 视觉素材描述规范

Use these rules whenever describing visual content for decomposition or final design plans.

## Required detail level

A good visual asset description should be usable as an image-generation prompt. Avoid generic phrases like “产品图”, “场景图”, “功能图标”, “背景装饰”.

Include as many of these details as applicable:

1. Subject: what object/person/product/scene is shown.
2. Product angle: front view, 45-degree view, side view, macro close-up, exploded view, top-down, hero angle.
3. Material and texture: matte plastic, brushed metal, transparent acrylic, soft silicone, woven fabric, ceramic gloss, wood grain, etc.
4. Environment: kitchen countertop, bathroom shelf, outdoor trail, home office desk, bedroom nightstand, studio gradient background, etc.
5. Lighting: softbox, natural morning light, rim light, dramatic spotlight, diffused shadow, clean commercial lighting.
6. Composition: centered hero object, left-side product cluster, floating icons around product, diagonal motion path, layered foreground and background.
7. Camera/perspective: eye-level, low angle, top-down flat lay, macro lens, shallow depth of field, orthographic technical view.
8. Style: photorealistic, premium e-commerce, clean tech, warm lifestyle, minimal luxury, medical clean, playful family style.
9. Background relationship: transparent background, matching gradient background, same floor plane, connected texture, soft shadow.
10. Constraints: no text, no watermark, no logo unless provided, no extra hands, no distorted product, isolated object if asset-only.

## Strong description pattern

Use this pattern:

```text
[Subject] shown as [composition/angle], with [material/texture details], placed in [environment/background], lit by [lighting], rendered in [style/quality], with [shadow/depth/background relationship], [constraints].
```

## Examples

Weak:

```text
产品使用场景图。
```

Strong:

```text
A photorealistic lifestyle scene showing the product placed on a warm oak kitchen countertop beside a ceramic mug and folded linen cloth, product angled 35 degrees toward camera, soft morning sunlight entering from the left, gentle shadows on the counter, shallow depth of field, premium Amazon A+ content style, no text, no watermark.
```

Weak:

```text
功能图标。
```

Strong:

```text
A set of three minimal 3D feature icons in matte white and soft blue: water droplet shield, quiet airflow wave, and long-lasting battery symbol, each icon floating inside a rounded translucent glass tile, soft studio lighting, subtle shadow, transparent background, no text, no logo.
```

## Decomposition vs final design

For reference decomposition, describe what appears in the uploaded image as faithfully as possible.

For final product design, generate new visual descriptions using the user's product photos and product introduction while preserving the confirmed section's layout logic.
