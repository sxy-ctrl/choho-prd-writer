# choho-prd-writer

帮助朝厚产品经理把需求草稿、会议结论或已有 PRD 扩写为可评审的需求文档，补齐交互、跨端联动、边界逻辑和可验证的验收条件。

支持新系统 0–1、小型功能优化、规则新增、新增功能、功能重构和 SaaS 流程优化。默认中文，保持已有文档结构，区分已确认事实、历史参考、建议与待确认决策。

## 使用

将仓库复制到你的 Agent 技能目录，使 `choho-prd-writer/SKILL.md` 位于技能目录下。

Codex 常见目录为 `~/.codex/skills/choho-prd-writer/`，Claude Code 常见目录为 `~/.claude/skills/choho-prd-writer/`。也可以直接让支持读取本地文件的 Agent 阅读 `SKILL.md` 后执行。

调用示例：

```text
使用 $choho-prd-writer，按小型功能优化类扩写以下需求，保留原编号。

使用 $choho-prd-writer，检查这份 PRD 的保存、跨端同步和失败恢复逻辑。

使用 $choho-prd-writer，按规则新增类补齐候选优先级、降级和无可行结果时的处理。
```

提供需求草稿、适用端/模块、希望修改的范围；如需匹配团队历史格式，请在自己的受控工作区提供可访问样例。

## 公开版资料范围

仓库包含 skill 指令、UI 元数据、模板、分类指南、边界检查和行为验收场景。不包含朝厚内部 PRD 原件、全文转录、设计稿、患者资料或含这些内容的完整安装包。公开版本身不具备访问历史资料的权限，也不会假装已经读取团队原稿。

## 文件结构

- `SKILL.md`：任务路由、取证、扩写与交付流程。
- `agents/openai.yaml`：技能展示与调用提示。
- `assets/prd-template.md`：完整功能与小迭代后备模板。
- `references/type-writing-guide.md`：六类需求的写法与深度。
- `references/style-and-sources.md`：团队样例的选择与核对约定。
- `references/boundary-review.md`：边界和联动推导清单。
- `references/evaluation-cases.md`：维护与试用的行为验收场景。

行为场景是验证输入与观察标准，不代表已完成模型评测。结构检查也不证明输出质量，应结合真实需求迭代。
