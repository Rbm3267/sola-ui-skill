# Sola AIR UI skill

A skill for Claude and an extension for Gemini CLI that design with [Sola AIR](https://sola-air.dev): they write `.sola` components using only the components and props @sola-air-ui/ui 1.6.2 really ships, check them, and render a self-contained HTML preview (`skills/sola-ui/scripts/preview.mjs`, Node 18+, no install, no network).

This repo is generated from [Rbm3267/sola-air](https://github.com/Rbm3267/sola-air) by `scripts/build-skill.mjs` on each release. Open issues and pull requests there.

## Install

**Claude Code**

```bash
claude plugin marketplace add Rbm3267/sola-ui-skill
claude plugin install sola-ui@sola-air
```

**Claude.ai** (code execution on): zip the `skills/sola-ui` folder and upload it under Settings → Capabilities → Skills.

**Gemini CLI**

```bash
gemini extensions install https://github.com/Rbm3267/sola-ui-skill
```

It loads `GEMINI.md` and starts the `@sola-air-ui/mcp` server.

## What's inside

- `skills/sola-ui/SKILL.md`: instructions (the same text is `GEMINI.md`)
- `skills/sola-ui/reference/components.md`: every component, its import path and props, generated from the package
- `skills/sola-ui/examples/`: designs that are previewed and tested in a real browser in sola-air's CI
- `skills/sola-ui/scripts/preview.mjs` and `vendor/`: compiler 1.5.2, core 1.5.2, design tokens and the component sources

MIT licensed.
