# Sola AIR UI skill

A skill for Claude that designs with [Sola AIR](https://sola-air.dev): it writes `.sola` components using only the components and props @sola-air-ui/ui 1.9.0 really ships, checks them, and renders a self-contained HTML preview.

This repo is generated from [Rbm3267/sola-air](https://github.com/Rbm3267/sola-air) by `scripts/build-skill.mjs` on each release. Open issues and pull requests there.

## Install

**Claude Code**

```bash
claude plugin marketplace add Rbm3267/sola-ui-skill
claude plugin install sola-ui@sola-air
```

**Claude.ai** (code execution on): zip the `skills/sola-ui` folder and upload it under Settings → Capabilities → Skills.

## What's inside

- `skills/sola-ui/SKILL.md`: instructions
- `skills/sola-ui/reference/components.md`: every component, its import path and props, generated from the package
- `skills/sola-ui/examples/`: designs that are previewed and tested in a real browser in sola-air's CI
- `skills/sola-ui/scripts/preview.mjs` and `vendor/`: compiler 1.5.4, core 1.5.2, design tokens and the component sources

It reads only the `.sola` file you give it, makes no network requests, and needs no credentials. MIT licensed.
