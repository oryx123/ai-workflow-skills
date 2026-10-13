# AI 落地 Skill 工具箱

免费、开源的 AI 工作流诊断工具。先找出值得自动化的一个流程，再决定工具、预算和开发范围。

目前提供 **`ai-workflow-audit`**：把真实业务流程整理成可执行的小试点，交付流程图、优先级、人工复核点、时间估算和验收方案。适合内容团队、独立创作者和小型业务团队。

## 安装

在项目目录安装到 Codex：

```bash
npx -y skills add oryx123/ai-workflow-skills --skill ai-workflow-audit --agent codex --yes
```

需要在所有项目使用时，增加 `--global`。使用 Claude Code 时，把 `--agent codex` 换成 `--agent claude-code`。其他客户端与参数见 [Skills CLI 文档](https://github.com/vercel-labs/skills)。

也可以直接打开 [SKILL.md](skills/ai-workflow-audit/SKILL.md)，将正文作为任务说明交给你的 AI 助手。

## 直接试一次

```text
使用 $ai-workflow-audit 帮我诊断一个流程：
我每周把 5 篇文章改成图文，每篇选观点 20 分钟、找配图 40 分钟、
排版 30 分钟、复核 10 分钟。目前用文档和一个设计工具。
我想先减少选观点和配图的重复劳动，发布仍由我自己确认。
请给我一个可以用 10 篇旧文章验收的小试点，暂时不购买新工具。
```

示例输入见 [内容团队的图文制作流程](examples/content-studio.md)。只想梳理问题时，可以先填写 [工作流信息表](skills/ai-workflow-audit/assets/workflow-intake.md)。

## 你会得到什么

| 交付物 | 用途 |
| --- | --- |
| 当前流程与瓶颈 | 找到重复劳动发生在哪一步 |
| 一个优先试点 | 控制第一轮范围和成本 |
| 人工复核与失败回退 | 明确 AI 处理与人工决策的边界 |
| 有依据的时间估算 | 区分已测量的数据和假设 |
| 验收样本、指标与下一步 | 用结果判断是否值得继续投入 |

这是诊断与试点设计 Skill；它不会自动登录账号、上传业务资料、发消息或改动生产系统。它不能替代行业资质、隐私审查或实际工程验收。AI 助手或模型服务可能另有使用成本，本仓库的内容免费。

## 视频里的配图工具

《中文文章配图：这个开源工具能画出观点》演示的是 **Ian Xiaohei Illustrations**，作者为 **Ian / helloianneo**。原项目：[helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)。请从原作者仓库了解和使用该工具。

本仓库的 `ai-workflow-audit` 用于诊断 AI 落地流程，和视频中的配图 Skill 是不同的工具。本仓库没有复制原作者的代码或图片。

## 交流与实际落地

如果你需要把试点接到实际业务系统里，可以用 [AI 落地需求交流模板](https://github.com/oryx123/ai-workflow-skills/issues/new?template=workflow-request.yml) 描述流程、已有系统和验收目标。Issues 是公开页面，请只提供可以公开的概括，不上传客户名单、业务原文、账号、密钥或私人联系方式。

## 许可

本仓库的原创 Skill、文档和示例采用 [MIT 许可](LICENSE)。第三方项目遵循各自的许可与署名要求。
