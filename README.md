# GitHub Launch

**读懂你的项目，再写它的 GitHub 门面。**

一个面向 Codex 的 Agent Skill，根据源码、真实功能和目标读者，编排简洁、有辨识度的 README 与项目发布材料。

[开始使用](#开始使用) · [你会得到什么](#你会得到什么) · [本仓库实例](docs/self-launch.md) · [English](README_EN.md)

```text
$github-launch 为当前项目准备 GitHub 发布材料。
先读代码和示例，突出真实价值，保持简洁。
```

这份 README，就是它为自己编排的首个发布示例。

## 同一个 Skill，不同的项目顺序

| 你的项目 | 优先展示什么 |
| --- | --- |
| 命令行工具 | 一次输入、命令和可见输出 |
| 桌面或 Web 应用 | 真实界面、体验或下载入口 |
| SDK / 组件库 | 最小集成示例和兼容边界 |
| 研究 / 算法 | 结果、条件和复现路径 |
| Agent Skill | 一句可复制请求、所需材料与产物 |

结构跟着项目走。高 Star 仓库提供参考，源码和实际结果决定写什么。

## 开始使用

在 Codex 中发送：

```text
使用 $skill-installer，从 https://github.com/yuyu-wu-feng/github-launch
安装 skills/github-launch。
保留整个目录，包括 agents/ 和 references/。
```

安装后，在目标项目中使用：

```text
$github-launch 为当前项目编写 README 和 GitHub About、Topics。
读者是第一次接触它的开发者，中文，简洁，有可运行的例子。
```

只改 README，或只写版本说明，也可以直接限定范围：

```text
$github-launch 精简当前 README，保留必要的安装、兼容性和限制说明。
```

```text
$github-launch 根据 v0.2.0 到 v0.3.0 的实际变更编写 Release 草稿。
```

版本号是请求示例，使用时替换为目标项目真实存在的版本。

<details>
<summary>手动安装</summary>

下载或克隆本仓库，将 `skills/github-launch/` 整个文件夹复制到 `~/.agents/skills/`；Windows 对应 `%USERPROFILE%\.agents\skills\`。已有同名技能时先保留自己的修改。

若当前 Codex 安装器使用自定义技能目录，沿用该安装器的目标位置。安装后可在技能列表中查找 `github-launch`；未出现时重启 Codex。参见 [Codex 官方技能文档](https://developers.openai.com/zh-Hans/docs/build-skills)。

</details>

## 你会得到什么

提供项目目录或仓库链接即可开始。目标读者、语言和发布范围可以补充；没有指定时，会从现有材料判断。

| 请求 | 产物 |
| --- | --- |
| 优化 README | 直接更新 README，按真实使用路径重排内容 |
| 准备项目发布 | README + 可复制的 About 简介、Topics 与必要待办 |
| 编写 Release | 基于实际版本范围的变更说明、升级提示与已知问题 |

**亮点要有依据。** 优先使用自己的示例、截图、产物或测量；核对安装命令、链接与平台支持；缺少证据时收窄表述。

**简约要保留关键信息。** 可以删掉空泛宣传和重复章节，但保留影响上手的前提、兼容性和限制。

## 运行与边界

- 技能包由 Markdown 与 YAML 组成，没有安装脚本或额外运行依赖；需要能读取项目、编辑文件的 Codex。联网调研、运行示例和远端上传分别取决于宿主的工具与权限。
- 生成效果依赖项目材料和模型判断。目前已用于本仓库的发布文档，尚无跨项目效果评测；其他 Agent 宿主未验证。
- 默认生成本地材料。明确要求上传后，才会使用你的 GitHub 登录与权限执行远端操作。
- 不会自动选择许可证、编造性能数据，或把计划功能写成已经实现。

## 设计与参考

核心规则在 [SKILL.md](skills/github-launch/SKILL.md)，案例取舍在 [参考笔记](skills/github-launch/references/patterns.md)。

参考了 uv、shadcn/ui、LocalSend 等项目，以及 [Nature Skills](https://github.com/Yuan1z0825/nature-skills)、[Superpowers](https://github.com/obra/superpowers) 和 [Anthropic Skills](https://github.com/anthropics/skills) 的介绍方式。仅借鉴组织思路，未复制其技能实现；本项目与这些项目无隶属关系。

欢迎在 Issues 中提供具体项目、生成结果与希望改进的地方。
