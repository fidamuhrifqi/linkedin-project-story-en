# Animated-Style Visual Storyboard Guide

Create one LinkedIn-ready landscape image that explains the project at a glance and clearly identifies it.

## Default Direction

- Use a 16:9 landscape composition.
- Create a polished professional animated-style or motion-graphic explainer.
- Use short English labels.
- Keep text density low.
- Use muted neutrals, off-white, charcoal, slate, soft blue, teal, or green accents.
- Avoid childish cartoons, mascot-like characters, neon gradients, candy colors, toy-like visuals, fake screenshots, and tiny code text.

## Required Identity Block

Include:

- The exact project name as the main title.
- "How It Works" or "GitHub Repo Exploration" as a subtitle.
- `Repo: owner/name` when the repository identity is available.
- One short factual descriptor when useful.

Never create a generic unnamed workflow diagram.

## Workflow Content

Show the most important parts of the system:

- User or triggering actor.
- Input such as a GitHub URL, form, file, prompt, API request, or dataset.
- Processing such as parsing, backend services, AI models, databases, queues, or rendering.
- Output such as a dashboard, report, post, image, recommendation, or deployed application.
- Optional review, edit, publish, or feedback step.

## Prompt Template

```text
Create a polished 16:9 landscape LinkedIn animated-style explainer illustration for a software project named [PROJECT NAME]. Put "[PROJECT NAME]" as the large, clearly readable headline, with the smaller subtitle "Repo: [OWNER/REPOSITORY] - How It Works" when available. Show the workflow: [INPUT] -> [PROCESSING STEPS] -> [OUTPUT]. Use a professional motion-graphic composition with clean UI panels, abstract product objects, readable English labels, subtle depth, strong contrast, and a restrained muted palette such as off-white, charcoal, slate, soft blue, teal, or green accents. Avoid childish cartoon aesthetics, mascot-like figures, neon gradients, candy colors, overly vibrant palettes, toy-like visuals, tiny code text, unprovided brand logos, and fake screenshots. Make the workflow understandable in one glance and do not create a generic unnamed diagram.
```

## Prompt Requirements

Confirm that the prompt includes:

- Exact project name.
- Owner/repository name when available.
- Main workflow steps.
- 16:9 LinkedIn landscape format.
- Professional animated-style direction.
- Restrained, non-childish palette.
- English labels.
- An instruction to avoid generic unnamed diagrams.

## Output Template

````markdown
## Animated Image Concept
Format: 16:9 landscape LinkedIn
Style: professional animated-style explainer with restrained colors
Visual title: [PROJECT NAME] - How It Works
Subtitle: Repo: [OWNER/REPOSITORY]
Visual flow: [input] -> [process] -> [output]
Labels: [label 1], [label 2], [label 3]
Note: [key emphasis]

Prompt:
```text
[Complete image-generation prompt]
```
````
