---
name: linkedin-project-story-en
description: Review GitHub projects, local repositories, repository archives, README files, or project notes and turn them into factual, human-sounding English LinkedIn posts plus a LinkedIn-ready 16:9 animated-style explanatory image concept. Use when the user asks for an English project review, LinkedIn status or caption, portfolio post, repository walkthrough, "how it works" visual, storyboard, or image-generation prompt based on software project source material.
---

# LinkedIn Project Story EN

Transform a software project into a factual English LinkedIn story and one professional landscape explainer visual. Keep user-facing deliverables in English unless the user explicitly requests another language.

## Core Rules

- Do not invent features, metrics, users, deployment status, awards, or business claims.
- Separate confirmed facts from reasonable inferences.
- Prefer a polite, grounded, human voice over hype.
- Default to reviewer/user POV for public repositories.
- Use creator POV only when the user says they built or own the project.
- Include the exact source URL inside the LinkedIn caption when one is provided.
- Put the final caption and image prompt in separate fenced `text` blocks.
- Do not reveal secrets found in a repository. Warn about exposed credentials without quoting their values.
- Ask a follow-up only when the source is unavailable or the intended angle cannot be inferred safely.

## Workflow

1. Inspect the source material.
   - For a GitHub URL, inspect the repository with available web, browser, GitHub, or clone tools.
   - For a local path or archive, inspect the files directly.
   - Read the README, manifests, setup files, documentation, screenshots, demos, tests, and important entry points.
   - Use `references/repo-review-checklist.md` for non-trivial repositories.

2. Build a factual project brief.
   - Identify the purpose, target user, problem, main workflow, stack, implementation details, setup flow, and limitations.
   - Track which details are confirmed and which are inferred.

3. Select the correct point of view.
   - Use reviewer/user POV when the user is trying, studying, or sharing someone else's project.
   - Use creator POV when the user explicitly identifies the project as their own.
   - Use neutral explainer POV when the user requests documentation-style wording.

4. Draft the English LinkedIn post.
   - Follow `references/linkedin-style-guide.md`.
   - Include a natural hook, concise context, what the project does, how it works, one useful observation, a reflection, and a light closing.
   - Include the source URL near the bottom before hashtags by default:

     ```text
     Repo I tried:
     [URL]
     ```

   - Use 3 to 6 relevant hashtags only when helpful.
   - Keep the complete caption in one fenced `text` block.

5. Create the visual concept.
   - Follow `references/visual-storyboard-guide.md`.
   - Default to one 16:9 landscape animated-style software explainer.
   - Put the exact project name prominently in the visual.
   - Include the repository owner/name as a smaller subtitle when available.
   - Show an understandable input-to-process-to-output workflow.
   - Use English labels and a restrained professional palette.
   - Provide a complete image-generation prompt in one fenced `text` block.
   - Generate the actual image when the user requests it and an image tool is available.

6. Verify the output.
   - Confirm that the caption uses the correct POV.
   - Confirm that every factual claim is supported by the source or labeled as an inference.
   - Confirm that the exact source URL appears inside the caption.
   - Confirm that the project name and workflow appear in the visual prompt.
   - Confirm that the visual prompt specifies 16:9, English labels, and a professional restrained style.

## Default Output

Use this structure unless the user requests a different format:

````markdown
## Project Summary
- [Purpose]
- [Stack]
- [Main workflow]

## LinkedIn Status
```text
[Ready-to-post English caption]

Repo I tried:
[SOURCE URL]

[3-6 relevant hashtags]
```

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

## Accuracy Notes
- Confirmed: [facts supported by the source]
- Inferred: [reasonable interpretations]
- Not verified: [missing or unavailable information]
````

## Point-of-View Guidance

For reviewer/user POV, prefer phrases such as:

- "I spent some time exploring this GitHub repo..."
- "I tried this repo to understand how the workflow is structured..."
- "One thing I learned from this project..."
- "From a first-time user perspective..."

Avoid ownership claims such as "I built", "I created", "my project", or "I developed" unless creator POV is confirmed.

## File Output

Default to chat output. Create files only when requested, such as:

- `linkedin-post.md` for the caption and summary.
- `visual-concept.md` for the storyboard and image prompt.
- An image file when an image-generation tool creates an asset.

## References

- `references/repo-review-checklist.md`: inspect repositories and extract supported facts.
- `references/linkedin-style-guide.md`: write natural English LinkedIn copy.
- `references/visual-storyboard-guide.md`: design the explanatory visual and generation prompt.
