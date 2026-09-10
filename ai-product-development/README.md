# AI 产品开发全流程 Skill

将三份《产品开发全流程手册》提炼为可直接调用的中文技能，帮助 AI 根据 PRD 和现有项目完成技术适配、核心 Agent 开发、正式前端、上线与验收。

适合智能写作、知识库问答、流程自动化、创作工作台、语音和多媒体 Agent。保留现有项目架构；从当前阶段进入，按需求读取参考文件。

## 使用

把整个 `ai-product-development` 文件夹放入 Codex 的技能目录（默认 `~/.codex/skills/`；自定义 CODEX_HOME 时使用其 `skills/`）。若当前会话未显示新技能，重新开启会话后调用。

```text
使用 $ai-product-development 阅读我的 PRD 和现有项目。
先判断当前阶段，输出技术适配声明，然后推进本阶段开发与验收。
```

更多示例：

```text
使用 $ai-product-development，为这个分阶段确认的内容生成 Agent
做第一条真实闭环。现在没有 API Key，先完成可运行实现和 mock 测试，
明确列出真实模型待验项。
```

```text
使用 $ai-product-development，在现有前端增加任务断线恢复和产物预览，
保持已有框架和接口兼容，并验证刷新、重复提交和失败恢复。
```

```text
使用 $ai-product-development，检查已验收 MVP 的上线条件，
复用我的现有云资源，给出具体发布与数据恢复方案后按已授权范围部署。
```

## 文件导航

- [SKILL.md](SKILL.md)：主入口、阶段路由、三层决策与工作流。
- [核心开发](references/core-development.md)：技术适配、持久任务、模型契约与有限重试。
- [前端](references/frontend.md) / [语音媒体](references/voice-media.md)：状态、真实交互与设备验证。
- [部署](references/deployment.md)：veFaaS 默认路线、配置与产物、持久化、发布和回退。
- [验收](references/verification.md)：mock 与真实模型证据、浏览器、线上和交接。
- [技术适配模板](assets/technical-adaptation.md) / [阶段计划模板](assets/stage-plan.md) / [验收模板](assets/acceptance-handoff.md)。
- [来源与修正说明](references/source-decisions.md)：三份手册覆盖关系、冲突裁决与时效边界。

技能中的默认栈和 veFaaS 路线可以按 PRD、现有系统和平台约束调整。无 Key 可推进开发，不能宣布真实模型验收通过；自动检查不能代替真实浏览器与用户质量判断。

本目录是技能说明与模板，不是已实现的产品，也不包含云账号凭据、原始手册全文或自动部署脚本。
