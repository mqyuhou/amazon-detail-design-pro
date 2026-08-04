# 确认与修改规则

This skill is confirmation-gated. Never proceed automatically through all stages.

## Confirmation language

Treat these as confirmation:

- 确认
- 满意
- 可以
- 继续
- 没问题
- 通过
- ok
- yes
- looks good

## Revision language

Treat these as revision intent:

- 不满意
- 修改
- 调整
- 重做
- 重来
- 不对
- 不是这样
- change
- revise
- edit

## If user asks for revision without details

Ask for concrete revision instructions and stop:

> 请提交具体修改意见，例如要调整版面划分、风格描述、文案长度、视觉素材、配色、比例或排版细节。我会根据你的意见重新输出一份修改方案，并再次等待你确认。

## If user provides revision details

Revise directly. For decomposition revisions, output the revised decomposition and ask for confirmation again. For final design revisions, output the revised full design plan and ask for confirmation again.

## Do not over-confirm

Do not ask for confirmation before Stage 2 if reference images are already provided. Do the decomposition first.

Do not ask for confirmation before Stage 5 if the user already confirmed the decomposition and provided sufficient product images plus product introduction. Generate the new plan.
