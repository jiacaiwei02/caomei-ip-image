# Caomei IP image

Caomei IP image references and adapts the article-illustration workflow from the original [Punk IP Article Illustrations Skill](https://github.com/adrianpunk/Punk-IP) by Adrian Punk.

## Purpose
Caomei IP image is a skill specification for generating article illustrations with:
- a fixed personal IP character,
- a user-defined illustration style,
- and the **original Punk-IP article illustration logic preserved**.

## What is changed
Only the **style system** is changed.

The original fixed style presets are replaced by:
1. `custom-text-style` — style defined by text
2. `reference-image-style` — style defined by uploaded reference illustration(s)
3. `hybrid-style` — style defined by both reference image(s) and text constraints

## What must remain unchanged
The following parts must remain aligned with the original skill logic:
- illustration count decision
- article cognition-anchor extraction
- scene planning
- composition structure
- per-image generation workflow
- delivery format and insertion reporting

## Key principle
> Change only **how to draw**.
> Do not change **how many to draw**, **what to draw**, **how to structure the picture**, or **how to deliver it**.

## Character turnaround

When creating a new character from photos or references, the skill delivers front, back, left-profile, and right-profile views for confirmation, along with a clean single-character reference image.

## Core files
- `SKILL.md` — master workflow
- `references/style-system.md` — custom style rules
- `references/original-logic-lock.md` — immutable original logic constraints
- `references/character-system.md` — character IP rules
- `references/delivery.md` — delivery and insertion rules


## Default background rule
The default final illustration background is **colorless / pure white** with generous whitespace.
Background color blocks, scenic backdrops, or decorative full-bleed environments should not be used unless the user explicitly asks for them or the original article logic truly requires them.

## Workflow reference

The article illustration workflow draws on [Punk IP Illustrations](https://github.com/adrianpunk/Punk-IP) by Adrian Punk. The current upstream release has a [Personal Use License](https://github.com/adrianpunk/Punk-IP/blob/main/LICENSE-PERSONAL.md). This repository contains the Caomei specification and does not bundle upstream repository files, scripts, character assets, or sample images.
