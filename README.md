# Sola AIR UI skill

A skill for Claude that designs with [Sola AIR](https://sola-air.dev): it writes `.sola` components using only the components and props @sola-air-ui/ui 1.9.2 really ships, checks them, and renders a self-contained HTML preview.

This repo is generated from [Rbm3267/sola-air](https://github.com/Rbm3267/sola-air) by `scripts/build-skill.mjs` on each release. Open issues and pull requests there.

## Install

**Claude Code**

```bash
claude plugin marketplace add Rbm3267/sola-ui-skill
claude plugin install sola-ui@sola-air
```

**Claude.ai** (code execution on, with access to the npm registry): zip the `skills/sola-ui` folder and upload it under Settings → Capabilities → Skills.

## What's inside

- `skills/sola-ui/SKILL.md`: instructions
- `skills/sola-ui/reference/components.md`: every component, its import path and props, generated from the package
- `skills/sola-ui/reference/AGENTS.md`: the full `.sola` language spec
- `skills/sola-ui/examples/`: designs, one per Markdown file, that pass the preview check in sola-air's CI

The plugin is Markdown and JSON only. To check and preview a design it runs `npx -y @sola-air-ui/preview@1.0.0`, which npx downloads from the npm registry with the compiler, core, design tokens and component sources. The preview reads only the `.sola` file you give it and writes one HTML file next to it. Nothing in the plugin reads credentials. MIT licensed.

For a version with the compiler bundled, which previews with no install and no network, copy `skills/sola` from [Rbm3267/sola-air](https://github.com/Rbm3267/sola-air) instead.
