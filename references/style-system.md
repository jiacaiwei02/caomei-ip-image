# Style system

## Purpose
Replace fixed built-in styles with a custom reusable style system.

## Allowed style modes

### 1. custom-text-style
The user defines the style in words.

Extract and normalize:
- overall medium (e.g. pastel crayon, watercolor, flat vector)
- line quality
- color palette
- texture / material feel
- lighting mood
- figure simplification
- background treatment
- shape language
- tone / emotional feel

### 2. reference-image-style
The user uploads illustration reference image(s).

Analyze the references to infer:
- color logic
- line quality
- rendering logic
- proportion language
- shape simplification
- texture / surface feel
- whitespace usage
- composition tendencies

The style references determine the visual language.
They do not replace the user’s personal IP identity.

### 3. hybrid-style
Use reference image(s) as the main style source, then apply textual overrides.

Examples of valid overrides:
- “keep the same line quality but reduce saturation”
- “same pastel texture but make the background cleaner”
- “same cute proportion, but slightly less childlike”

## Unified style application
The confirmed style profile must apply to both:
1. the personal IP character
2. the article illustrations

This means:
- same rendering language
- same line logic
- same palette family
- same texture logic
- same visual simplification language

## Style profile template

```yaml
style_name: "Caomei Custom Style"
style_mode: "custom-text-style | reference-image-style | hybrid-style"
source_assets:
  - optional_reference_1
  - optional_reference_2
palette:
  primary: []
  secondary: []
line_style: ""
rendering_style: ""
texture: ""
proportion_language: ""
lighting: ""
background_treatment: "default: colorless / pure white, unless user explicitly requests otherwise"
composition_tendency: ""
consistency_rules:
  apply_to_character: true
  apply_to_article_illustrations: true
  reuse_profile_for_future_articles: true
```

## Default background behavior
Unless the user explicitly requests another treatment, the final article illustrations should use a **colorless / pure white background** with generous whitespace.

This means:
- no solid colored full-page background by default
- no scenic decorative background by default
- no dense environmental fill by default
- keep the background visually quiet so the action, object relationship, and key point remain clear

Background elements may appear only when they are necessary to support the scene logic, but they should remain minimal and should not replace the default clean editorial white-space feel.

## Hard constraints
- style governs **how to draw**, not content planning
- style cannot override original article-planning logic
- style references should not cause direct copying of someone else’s exact artwork
- when conflicts occur, preserve article meaning and character identity while staying stylistically consistent
