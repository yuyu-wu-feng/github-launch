# 用 GitHub Launch 发布 GitHub Launch

这是一次实际编排记录。输入是本仓库的技能文件，产物是本仓库的中英文 README 与发布字段，不是批量生成能力的基准测试。

## 输入

- [SKILL.md](../skills/github-launch/SKILL.md)：项目画像、阅读顺序、真实亮点、交付范围和验证规则。
- [参考笔记](../skills/github-launch/references/patterns.md)：不同项目类型的取舍依据。
- [Release 规则](../skills/github-launch/references/releases.md)：首次发布与版本变更的区别。
- [界面元数据](../skills/github-launch/agents/openai.yaml)：技能名称、简介和调用提示。

实际请求：用这个 skill 为它自己准备 GitHub 发布材料，并参考 Nature Skills 等技能项目的呈现方式。

## 编排决定

| 项目证据 | 页面决定 |
| --- | --- |
| 它是供 Codex 执行的技能，用户首先需要知道怎么调用 | 首屏给一句可复制请求 |
| 核心价值是按项目类型选顺序 | 用项目类型与前置内容的小表格说明差异 |
| 产物是 README、仓库字段和按需 Release 文本 | 明确列出请求与对应交付物 |
| 包含按需加载的参考文件 | 安装说明要求保留完整目录 |
| 没有产品界面，也没有跨项目量化评测 | 不放假截图、速度指标或效果承诺 |
| 当前只有一个技能 | 不复制合集的技能索引、社区运营板块和长目录 |

## 产物

- [中文 README](../README.md)
- [English README](../README_EN.md)
- [GitHub 发布字段](github-launch.md)

本次的可观察结果是这些具体文件及其引用关系。正文与技能声明已进行人工核对；格式和路径检查只证明文件结构有效，不证明在所有项目上都能获得同样结果。
