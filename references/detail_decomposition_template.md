# 详情页拆解输出模板

Use this template after the user uploads one or more reference detail-page images.

## Output title

# 详情页参考图拆解方案

## Opening summary

Briefly state:

- Number of reference images analyzed.
- Estimated total number of sections/modules.
- Overall design style.
- Main visual rhythm of the long page.

## Per-section template

Repeat this structure for every section.

```markdown
## 版面 [编号]：[版面主题]

### 1. 版面比例
- 估算长宽比：[ratio]
- 建议设计尺寸：宽度 1440px，高度根据内容适配
- 版面内容密度：[低/中/高]

### 2. 设计风格
[Describe the style in concrete terms: e.g. premium minimalist, tech clean, warm lifestyle, medical-grade clean, outdoor rugged, soft family-friendly, luxury beauty, etc.]

### 3. 背景设计
[Describe color, gradient, texture, environment, shadows, decorative lines, continuity, and how this section connects with adjacent sections.]

### 4. 文案内容
- 主标题：**[visible copy]**
- 副标题/说明：**[visible copy]**
- 卖点/标签：**[visible copy]**
- 其他文案：**[visible copy]**

If some copy is too small or unreadable, write:
- 不可辨识小字：**[位置 + 可能用途，例如底部参数说明/图标标签]**

### 5. 视觉内容拆解
- 视觉元素 1：[Nano Banana-ready description]
- 视觉元素 2：[Nano Banana-ready description]
- 视觉元素 3：[Nano Banana-ready description]

Each visual element must be described as a standalone asset or compositional element, not just named.

### 6. 排版方案
#### 文字排版
[Text hierarchy, font feeling, title size relationship, alignment, line spacing, contrast, button/tag/chip style if any.]

#### 页面规范
[Margins, safe area, grid, alignment rule, section padding, spacing between content groups, visual balance.]

#### 视觉内容排版
[Product position, scene/object position, layering, scale, perspective, overlap, shadows, direction of gaze/motion, focal point.]

### 7. 连续拼接说明
[Explain how this section's top/bottom background can connect with previous and next sections.]
```

## Final confirmation prompt

End exactly with a confirmation request similar to:

> 请确认这份详情页拆解方案是否满意。回复“确认/满意/继续”后，我会进入下一步，让你上传产品图和产品介绍；如果需要调整，请回复“修改”，并告诉我具体修改意见。
