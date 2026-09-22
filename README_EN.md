# GitHub Launch

**Understand the project. Tell its story on GitHub.**

An Agent Skill for Codex that uses source code, actual capabilities, and the intended audience to shape concise READMEs and project launch materials.

[Get started](#get-started) · [What you get](#what-you-get) · [This repository as an example](docs/self-launch.md) · [中文](README.md)

```text
$github-launch Prepare GitHub launch materials for the current project.
Read the code and examples first. Highlight real value and keep it concise.
```

This README is the first publishing example prepared with the skill itself.

## One skill, different reading paths

| Your project | What usually comes first |
| --- | --- |
| CLI tool | A real input, command, and observable output |
| Desktop or web app | The actual interface and a way to try or download it |
| SDK / component library | A minimal integration and compatibility boundaries |
| Research / algorithm | Results, conditions, and reproduction steps |
| Agent Skill | A copyable request, required inputs, and deliverables |

The structure follows the project. Popular repositories offer ideas; source code and actual results determine the claims.

## Get started

Send this in Codex:

```text
Use $skill-installer to install skills/github-launch from
https://github.com/yuyu-wu-feng/github-launch.
Keep the complete folder, including agents/ and references/.
```

Then use it in your target project:

```text
$github-launch Write a README, GitHub About description, and Topics for this project.
Write in English for developers discovering it for the first time.
Keep it concise and include a runnable example.
```

You can also request a narrower edit or release draft:

```text
$github-launch Shorten the current README while preserving installation,
compatibility, and limitation details.
```

```text
$github-launch Draft release notes from the actual changes between v0.2.0 and v0.3.0.
```

These version numbers illustrate the request. Replace them with versions that exist in your project.

<details>
<summary>Manual installation</summary>

Download or clone this repository and copy the entire `skills/github-launch/` folder into `~/.agents/skills/`, or `%USERPROFILE%\.agents\skills\` on Windows. Preserve local changes if a skill with the same name is already installed.

If your Codex installer uses a custom skill location, follow that installer's destination. Look for `github-launch` in the skill list afterward; restart Codex if it does not appear. See the [official Codex skill documentation](https://developers.openai.com/zh-Hans/docs/build-skills).

</details>

## What you get

Start with a project directory or repository URL. You may specify the audience, language, and scope; otherwise, the skill infers them from available material.

| Request | Deliverables |
| --- | --- |
| Improve a README | An updated README organized around actual usage |
| Prepare a project launch | A README, copyable About description and Topics, and necessary follow-ups |
| Write release notes | Changes grounded in a real version range, upgrade guidance, and known issues |

**Claims need evidence.** Prefer the project's own examples, screenshots, outputs, or measurements. Check installation commands, links, and platform support. Narrow claims when evidence is missing.

**Keep the essentials.** Remove generic promotion and repetition while preserving prerequisites, compatibility, and limitations that affect adoption.

## Runtime and boundaries

- The skill contains Markdown and YAML, with no installation scripts or additional runtime dependencies. It needs Codex with project reading and file editing tools. Online research, example execution, and remote publishing depend on the host's tools and permissions.
- Results depend on project material and model judgment. It has been used for this repository's publishing documents; no cross-project effectiveness evaluation has been performed. Other Agent hosts have not been verified.
- By default, it prepares local material. It uses your GitHub session and permissions for remote operations only when you explicitly request uploading.
- It does not choose a license automatically, invent performance figures, or describe planned features as implemented.

## Design and references

The workflow is in [SKILL.md](skills/github-launch/SKILL.md), with editorial choices in the [reference notes](skills/github-launch/references/patterns.md).

Presentation ideas come from projects including uv, shadcn/ui, and LocalSend, as well as [Nature Skills](https://github.com/Yuan1z0825/nature-skills), [Superpowers](https://github.com/obra/superpowers), and [Anthropic Skills](https://github.com/anthropics/skills). Their skill implementations were not copied. This project is not affiliated with them.

Issues with a concrete project, generated output, and a description of the desired improvement are welcome.
