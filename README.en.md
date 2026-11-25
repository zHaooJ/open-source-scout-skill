<div align="center">

# 🔭 Open Source Scout

**Find open-source projects that fit what you want to do.**

Guided requirements · Project discovery · Evidence checks · Practical comparisons

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Format: Agent Skill](https://img.shields.io/badge/Format-Agent%20Skill-5263EB)
![Designed for: Codex](https://img.shields.io/badge/Designed%20for-Codex-222222)

[简体中文](README.md) · **English**

</div>

---

## What is it?

Open Source Scout is a Codex skill for discovering and comparing open-source projects. It helps turn an incomplete idea into a recommendation with understandable tradeoffs and traceable evidence.

You do not need a finished requirements document. When your goal is unclear, it uses short multiple-choice questions to narrow the direction. When enough is known, it searches, checks relevant sources, and explains what each candidate does and what you would need to build yourself.

```text
Use $open-source-scout to find a long-term memory module for my own agent.
I need to track project progress, decisions, and outstanding work.
I have no language or deployment preference yet.
```

## Where it helps

| Your starting point | What the skill does |
| --- | --- |
| A vague idea | Clarifies the use case and explores representative approaches |
| A concrete goal | Finds candidates and checks the requirements that affect suitability |
| A shortlist | Compares the projects using shared criteria |
| A product to replace | Checks which capabilities an open-source alternative actually covers |
| A learning or contribution goal | Looks at examples, code structure, contribution entry points, and maintenance |

## How it works

1. Reuse the goal and constraints already stated in the conversation.
2. Ask about missing user choices when they would change the next step.
3. Discover candidates across relevant approaches and verify their identity.
4. Check important capabilities, licensing, edition boundaries, dependencies, and maintenance.
5. Introduce each project, compare tradeoffs, and explain when the recommendation would change.

These are flexible modes rather than a mandatory questionnaire. Someone who is unsure can explore examples first. Someone with a clear request can proceed directly to research.

**A typical clarification:**

> What should the memory module remember first?
>
> A. User preferences and background  
> B. Project progress, decisions, and pending tasks  
> C. Lessons from successful and failed attempts  
> D. Not sure — explain the differences

This is an illustrative question, not a fixed intake form or a live search result.

## Install in Codex

Download the [GitHub repository](https://github.com/zHaooJ/open-source-scout), or clone it:

```bash
git clone https://github.com/zHaooJ/open-source-scout.git
```

Place the `open-source-scout` directory containing `SKILL.md` in your personal skills directory:

| Platform | Default location |
| --- | --- |
| Windows | `%USERPROFILE%\.codex\skills\open-source-scout\` |
| macOS / Linux | `~/.codex/skills/open-source-scout/` |

If you use a custom `CODEX_HOME`, use its `skills/open-source-scout/` directory. Preserve local changes before replacing an existing installation.

The entrypoint should be directly at `skills/open-source-scout/SKILL.md`, not nested inside another download directory. You can copy the full repository; the runtime files are `SKILL.md`, `agents/`, and `references/`.

Invoke it in a Codex conversation:

```text
Use $open-source-scout to compare these repositories for my project.
Explain what each one does, how I would integrate it, and the main limitations.
```

If it is not discovered, check the directory structure and try a new conversation or restart your client. Skill discovery details depend on the Codex version you use.

The instructions are primarily written in Chinese and direct the agent to use the user's language. This English README describes the same workflow; it is not a separate implementation.

## What a result includes

- A short description of what each main candidate is and how it is normally used.
- Its role in your task: ready-to-use application, component, framework, or reference implementation.
- Comparisons across the same relevant criteria, including work you need to do yourself.
- Sources for important claims and a clear distinction between documentation, inspected code, and observed runtime behavior.
- A recommendation, conditions for choosing an alternative, and consequential unknowns.
- A small next verification step when adoption needs more evidence.

Stars and unsupported scores do not replace suitability checks. Candidate counts and research depth follow the task rather than a fixed quota.

## Requirements and limits

- This repository provides agent instructions, not a standalone search engine or hosted service.
- Live research requires the host to provide web search, repository access, or equivalent tools. No specific MCP server, API key, model, or database is required by the skill itself.
- Without network access, it can clarify requirements and analyze supplied materials, but cannot claim current verification.
- Codex is the intended entry point. Compatibility with other `SKILL.md` hosts has not been established here.
- A research request does not by itself include installing or executing candidate projects, deploying them, or contacting maintainers.
- Results depend on the model, available tools, accessible evidence, and the task. A documented feature is not proof that it works in your environment.

## Repository guide

| File | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Core instructions and routing |
| [agents/openai.yaml](agents/openai.yaml) | Codex UI metadata and default prompt |
| [references/intake.md](references/intake.md) | Adaptive requirements gathering |
| [references/search-and-evidence.md](references/search-and-evidence.md) | Search and evidence checks |
| [references/comparison-and-delivery.md](references/comparison-and-delivery.md) | Comparison, recommendations, and feedback |
| [docs/workflow.md](docs/workflow.md) | Workflow rationale, in Chinese |
| [examples/conversations.md](examples/conversations.md) | Illustrative conversations and output, in Chinese |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Contribution guidance, in Chinese |
| [docs/publishing.md](docs/publishing.md) | Repository publishing notes, in Chinese |
| [CHANGELOG.md](CHANGELOG.md) | Changes to the package |

## Acknowledgments

Search depth, source roles, evidence reuse, and codebase comparison were informed by the [literature search](https://github.com/mikubaka88/CCFA-Skills/tree/main/ccf-literature-searcher) and [codebase selection](https://github.com/mikubaka88/CCFA-Skills/blob/main/ccf-research-engineer/references/codebase-and-implementation.md) materials in [CCFA-Skills](https://github.com/mikubaka88/CCFA-Skills). The requirements interview and project selection rules were written independently. No installation of that repository is needed.

## License

[MIT](LICENSE). Referenced materials and discovered projects retain their own licenses.
