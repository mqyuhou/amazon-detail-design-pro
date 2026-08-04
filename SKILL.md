---
name: amazon-detail-design-pro
description: Create Amazon product detail page and A+ content layout design plans by decomposing reference detail-page screenshots, waiting for user confirmation, then generating a new product-specific layout plan from the user's product photos and product introduction. Use when the user asks in Chinese or English to analyze competitor/reference Amazon detail pages, split them into sections, extract section themes, style, copy, visuals, backgrounds, aspect ratios, and produce a full new e-commerce detail-page design brief with Nano Banana-ready visual asset descriptions, matching language, structure, density, and layout.
---

# 亚马逊详情设计改进版

## Core purpose

Use this skill to turn one or more Amazon/detail-page reference images into a section-by-section design blueprint, then transform that blueprint into a complete new layout design plan for the user's own product.

The skill is a staged, confirmation-driven workflow. Do not skip confirmation gates. Do not generate the final product-specific layout until the user has confirmed the reference-page decomposition and has provided product images plus product introduction.

## Required workflow

### Stage 1 — Ask for reference detail-page images

When the user starts this workflow and has not provided reference images, ask them to upload one or more reference detail-page images.

Use this message in Chinese by default:

> 请先上传详情页参考图，可以是单张，也可以是多张。建议上传同类产品、竞品或风格接近的亚马逊详情页长图/截图。上传后，我会先帮你拆解版面结构、文案、视觉内容、背景和排版方案。

If the user provides Amazon links instead of screenshots, ask for screenshots/images unless browsing is explicitly available in the current environment. The primary workflow is image-based.

### Stage 2 — Decompose the reference detail page

Analyze all uploaded reference images. Split each detail page into distinct sections/modules based on visual boundaries, background changes, content themes, and layout shifts.

For each section, output a complete decomposition using the structure in `references/detail_decomposition_template.md`.

Must include for every section:

- Section number and content theme.
- Aspect ratio estimate.
- Design style.
- Background description.
- Original copy content with the actual copy in **bold**.
- Visual content descriptions. Each visual element must be specific enough to generate as a separate Nano Banana/Gemini Image visual asset.
- Layout plan containing text layout, page specifications, and visual layout.
- Continuity note explaining how the background connects with adjacent sections and can be stitched into one long page.

After the decomposition, stop and wait for confirmation.

Use this confirmation prompt:

> 请确认这份详情页拆解方案是否满意。回复“确认/满意/继续”后，我会进入下一步，让你上传产品图和产品介绍；如果需要调整，请回复“修改”，并告诉我具体修改意见。

### Stage 3 — Handle decomposition confirmation or revision

If the user replies with confirmation language such as “确认”, “满意”, “可以”, “继续”, “ok”, or “yes”, proceed to Stage 4.

If the user replies with dissatisfaction or revision language such as “不满意”, “修改”, “调整”, “重来”, or “不对”, ask for concrete revision instructions if they have not already provided them:

> 请提交具体修改意见，例如需要重新划分哪些版面、补充哪些视觉内容、调整哪些风格描述、或修改哪些比例判断。我会根据你的意见重新输出一份拆解方案，并再次等待你确认。

If the revision instructions are already present, revise the decomposition directly and then repeat the Stage 2 confirmation prompt.

### Stage 4 — Ask for product images and product introduction

After the user confirms the decomposition, ask for the user's product materials.

Use this message:

> 请上传你的产品图和产品介绍。产品介绍可以包含：产品名称、核心卖点、功能特点、材质/规格、使用场景、目标人群、品牌调性、希望突出的差异化优势。上传后，我会基于已确认的参考版式，为你的产品生成新的详情页版式设计方案。

Do not proceed to final design generation until the user provides product images and at least a product introduction or basic product facts.

### Stage 5 — Generate the new layout design plan

Generate a complete new product-specific layout plan based on:

1. The confirmed reference decomposition.
2. The user's uploaded product images.
3. The user's product introduction and selling points.

Use the structure in `references/new_design_plan_template.md`.

Rules for this output:

- Produce a complete design plan for each section.
- Keep each section's layout framework, content framework, visual hierarchy, and visual-material arrangement consistent with the confirmed reference section.
- Do not use vague shortcut wording such as “沿用原结构”, “替换成新文案”, “新视觉素材”, “同上”, “参考上面”, or any other pointer-style omission.
- Write every section as a standalone, complete design brief.
- Generate new copy from the user's product information.
- Translate the copy into the same language used by the corresponding reference section.
- Match the copy length, character density, line rhythm, and text hierarchy of the reference section as closely as possible.
- Adapt the color palette to the user's product photos while preserving overall style consistency.
- Include style description and color palette in every section.
- Choose one aspect ratio per section from exactly: `3:2`, `4:3`, `1:1`, `3:4`, `2:3`, `9:16`.
- Set width to `1440px`; compute height according to the selected ratio and mention the resulting size.
- The height may vary by section; backgrounds should connect smoothly across sections.

Recommended height mapping for width 1440px:

| Ratio | Size |
|---|---:|
| 3:2 | 1440 × 960 px |
| 4:3 | 1440 × 1080 px |
| 1:1 | 1440 × 1440 px |
| 3:4 | 1440 × 1920 px |
| 2:3 | 1440 × 2160 px |
| 9:16 | 1440 × 2560 px |

After outputting the new layout plan, stop and wait for confirmation.

Use this confirmation prompt:

> 请确认这份新的详情页版式设计方案是否满意。回复“确认/满意/继续”表示方案通过；如果需要调整，请回复“修改”，并告诉我具体修改意见，我会重新输出修改后的方案。

### Stage 6 — Handle final design confirmation or revision

If the user confirms, acknowledge completion and offer the next practical step, such as generating image prompts, creating a designer handoff brief, or converting the plan into production checklist format.

If the user asks for revisions, collect concrete revision instructions if not already provided, then produce a revised full design plan. Do not only list changed items; output the revised sections completely enough for production.

## Analysis rules

### Section splitting

Split a reference page into sections using these signals:

- Major background change or transition.
- New headline/topic or selling point.
- Major layout shift.
- Product scene change.
- Feature demonstration block.
- Review, comparison, specification, or usage-scenario block.

If boundaries are ambiguous, choose the segmentation that would be most useful to a designer building a stitched long page.

### Aspect ratio selection

Estimate the reference section's approximate aspect ratio during decomposition. During final design, choose the closest allowed ratio from `3:2`, `4:3`, `1:1`, `3:4`, `2:3`, `9:16` based on content amount and visual complexity.

Prefer:

- `3:2` or `4:3` for compact hero/feature sections.
- `1:1` for balanced product-feature modules.
- `3:4` or `2:3` for dense content, multi-scene modules, process explanations, or comparison sections.
- `9:16` for tall immersive scenes, long usage scenarios, or modules with multiple stacked visual groups.

### Copy handling

For decomposition, preserve visible reference copy as much as possible and bold each copy item.

For final design, create new copy from the user's product information. Match the reference language section-by-section. If the reference copy is English, write the new copy in English. If the reference copy is German, Japanese, French, Spanish, Chinese, or another language, write the corresponding section copy in that language.

Keep copy concise and layout-ready. Avoid overexplaining.

### Visual asset descriptions

Every visual asset description must be concrete enough for image generation. Follow `references/visual_asset_prompt_rules.md`.

Include, when relevant:

- Subject/object.
- Product angle and pose.
- Material, texture, and surface detail.
- Scene/environment.
- Lighting and shadows.
- Composition and camera perspective.
- Background relationship.
- Style, realism level, and rendering quality.
- Negative constraints when useful, such as “no text, no logo, transparent background”.

### Background continuity

Treat the full detail page as a stitched long image. Every section must describe how its background connects with the previous and next sections, such as gradient continuation, same material surface, repeated texture, shared lighting direction, flowing decorative lines, or consistent environment depth.

### Avoid unsafe or unsupported claims

Do not claim to have found, browsed, or verified Amazon competitor pages unless the current environment actually provides browsing and the user requested it. If the workflow lacks reference images, ask the user to upload them.

Do not state factual product claims, certifications, medical claims, safety claims, or compliance claims unless provided by the user. Convert unsupported claims into softer design language or mark them as placeholders for verification.

## Output resources

Use these references when needed:

- `references/detail_decomposition_template.md` — output structure for Stage 2.
- `references/new_design_plan_template.md` — output structure for Stage 5.
- `references/visual_asset_prompt_rules.md` — Nano Banana-ready visual asset description rules.
- `references/revision_rules.md` — confirmation and revision behavior.
