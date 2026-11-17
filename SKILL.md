---
name: caomei-ip-image
description: Generate article illustrations using a consistent personal character and a reusable style defined by text, reference images, or both.
---

# Caomei IP image

## Identity
Caomei IP image is an article-illustration skill that uses a fixed personal IP character and a reusable custom illustration style to generate editorial insert images for articles.

## Non-negotiable scope
This skill modifies **only the style system**.

It must **not** alter the original article-illustration workflow in the following areas:
1. illustration quantity decision
2. cognition-anchor extraction
3. scene planning method
4. image structure and composition logic
5. delivery and insertion reporting logic

If a future request conflicts with these invariants, preserve the original logic and apply changes only to visual style.

## Main goal
Given:
- a source article,
- a confirmed personal IP character,
- and a confirmed custom style profile,

produce article illustrations that:
- preserve the original content-planning logic,
- use the fixed personal IP consistently,
- and use the same style for both the character and the article illustrations.

---

## Workflow

### Step 1 — gather inputs
Required inputs:
- article text
- character reference asset(s)
- custom style definition

Possible style inputs:
- **custom-text-style**: user describes the desired style in words
- **reference-image-style**: user uploads illustration reference image(s)
- **hybrid-style**: user uploads reference image(s) and gives text overrides

### Step 2 — build style profile
Create a reusable style profile containing:
- style name
- style source type
- palette
- line quality
- rendering/material feel
- character proportion language
- lighting logic
- background treatment
- composition tendencies
- constraints for reuse

Important:
This profile defines **how to draw**, not **what to draw**.

### Step 3 — build or load character IP
Use the confirmed personal photo / character reference to create or load the personal IP package.

Character package should include:
- character identity summary
- clean single-character reference
- optional turnarounds / supporting views
- character consistency notes

The character must be rendered in the confirmed custom style.

### Step 4 — analyze article
Analyze the article using the **original article logic**.

Do not change the original logic for:
- illustration count
- cognition-anchor selection
- scene planning
- decision between flow-breakdown mode and core-action mode

### Step 5 — determine illustration count
Determine image quantity using the original quantity logic.

Default count guidelines to preserve:
- <=500 words: 1 image
- 500–1500 words: 1–3 images
- 1500–3500 words: 3–5 images
- >3500 words: 4–8 images

If the user explicitly requests a number, follow the user request where feasible.
Do not inflate image count just because more scenes are possible.
Merge repetitive points.

### Step 6 — plan scenes
For each selected cognition anchor, create one illustration plan.

Each plan must include:
- anchor / key point
- intended mode: `flow-breakdown` or `core-action`
- who appears
- what action happens
- which 1–3 important objects or object group(s) appear
- what visible relationship/result makes the point clear
- suggested article insertion location

### Step 7 — enforce original structure
Each final image must preserve the original structural rules:
- one image = one key point
- use image to explain, not blocks of text
- keep it readable in ~3 seconds
- prefer action, object, and visible physical relationship
- avoid turning the image into a poster or infographic wall
- each cognition anchor becomes a separate image
- default output is an independent 16:9 illustration
- preserve generous whitespace / editorial simplicity
- default to a colorless / pure white background unless the user explicitly requests otherwise

### Step 8 — use expression/action library correctly
Expression and pose references are **supporting reference only**.

They help maintain:
- facial consistency
- emotional range
- body proportion consistency

They do **not** restrict scene creativity.
Article illustrations must generate actions, gestures, and expressions primarily from article meaning.
Do not limit the final scene to pre-existing poses.

### Step 9 — generate images
Generate images **one by one**, not as a combined multi-panel infographic.

Use:
- the confirmed style profile
- the confirmed character package
- the scene plan for that single cognition anchor

Style profile controls:
- how the image looks
- how the character and environment are rendered
- by default, the background remains colorless / pure white and visually quiet

Article plan controls:
- what the scene communicates

### Step 10 — quality check
Check each image for:
- character consistency
- style consistency
- fidelity to the selected cognition anchor
- one-image-one-point clarity
- excessive text / poster drift
- accidental copying of character-sheet layouts

Reject or revise if:
- multiple concepts are merged into one image without justification
- the image becomes a text-heavy infographic
- the scene deviates from the article’s chosen anchor
- character identity becomes unstable

### Step 11 — delivery
Preserve the original delivery style.

For each illustration, report:
- image filename/path
- which point it represents
- suggested insertion location in the article

If the source format supports insertion and insertion is requested, insert according to the original delivery logic.
Otherwise provide insertion guidance.

---

## Output principles

### What this skill changes
- style customization
- style persistence and reuse
- alignment between personal IP style and illustration style
- background rendering defaults within the style system (default: colorless / pure white)

### What this skill must not change
- count logic
- article understanding logic
- scene logic
- composition logic
- delivery logic

---

## Golden rule
**Caomei IP image = Original article-illustration skill logic × Custom reusable style system.**
