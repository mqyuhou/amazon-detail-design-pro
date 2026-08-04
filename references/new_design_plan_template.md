# 新详情页版式设计方案模板

Use this template after the user has confirmed the reference decomposition and provided product images plus product introduction.

## Output title

# 新详情页版式设计方案

## Opening summary

Briefly state:

- Product name/category if available.
- Overall design direction.
- Main color palette.
- Number of sections.
- The selected output width: 1440px.

## Per-section template

Repeat this structure for every section. Do not use pointer-style wording such as “沿用原结构”, “同上”, “替换为”, or “参考前面”. Every section must be self-contained.

```markdown
## 版面 [编号]：[新版面主题]

### 1. 版面规格
- 匹配长宽比：[3:2 / 4:3 / 1:1 / 3:4 / 2:3 / 9:16]
- 设计分辨率：[1440 × height px]
- 内容密度：[低/中/高]

### 2. 风格描述
[Complete style description adapted to the user's product. Include mood, image style, visual quality, commercial positioning, and target-user feeling.]

### 3. 配色方案
- 主色：[color name + usage]
- 辅助色：[color name + usage]
- 强调色：[color name + usage]
- 背景色/过渡色：[color name + usage]
- 色彩搭配逻辑：[explain why it matches the product image and category]

### 4. 背景设计
[Describe the exact background for this section and how it connects with the previous/next sections.]

### 5. 文案内容
Write layout-ready copy in the same language as the matching reference section. Match the original section's hierarchy and approximate length.

- 主标题：**[new copy]**
- 副标题/说明：**[new copy]**
- 卖点/标签：**[new copy]**
- 辅助说明/参数：**[new copy]**

### 6. 视觉素材设计
- 视觉元素 1：[complete Nano Banana-ready prompt for product/scene/object]
- 视觉元素 2：[complete Nano Banana-ready prompt]
- 视觉元素 3：[complete Nano Banana-ready prompt]

Each visual element must describe subject, composition, material, lighting, perspective, background relationship, and no-text/no-logo constraints if needed.

### 7. 文字排版
[Title placement, subtitle placement, typography style, alignment, font weight, line count, line spacing, label style, relation to visuals.]

### 8. 页面规范
[Margins, safe area, grid, spacing, content block width, visual balance, continuity, section padding.]

### 9. 视觉内容排版
[Exact product and asset placement, scale, overlap, depth, shadows, foreground/background hierarchy, focal path.]

### 10. 拼接连续性
[Explain how top and bottom areas visually connect to adjacent sections in the long detail page.]
```

## Height mapping

Use these sizes for 1440px width:

- 3:2 = 1440 × 960 px
- 4:3 = 1440 × 1080 px
- 1:1 = 1440 × 1440 px
- 3:4 = 1440 × 1920 px
- 2:3 = 1440 × 2160 px
- 9:16 = 1440 × 2560 px

## Final confirmation prompt

End exactly with a confirmation request similar to:

> 请确认这份新的详情页版式设计方案是否满意。回复“确认/满意/继续”表示方案通过；如果需要调整，请回复“修改”，并告诉我具体修改意见，我会重新输出修改后的方案。
