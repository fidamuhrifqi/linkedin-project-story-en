# LinkedIn Project Story EN

An agent skill that reviews software projects and turns them into factual, human-sounding English LinkedIn posts with professional visual concepts.

It works with GitHub repositories, local source folders, repository archives, README files, and project notes. The skill is designed for developers who want to share what they built, tried, reviewed, or learned without inventing features or sounding like an advertisement.

## What It Produces

- A concise factual project summary.
- A ready-to-post English LinkedIn caption.
- Reviewer/user, creator, or neutral explainer point of view.
- A 16:9 LinkedIn visual storyboard.
- A complete image-generation prompt with the project name and workflow.
- Accuracy notes that separate confirmed facts from inferences.

## Why Use It

Writing a useful project post requires more than summarizing a README. This skill inspects the available source, identifies the actual workflow and stack, chooses the correct point of view, and produces a post that is professional without becoming promotional.

It also prevents a common mistake: presenting someone else's open-source project as if you created it.

## Repository Structure

```text
.
|-- README.md
|-- LICENSE
`-- linkedin-project-story-en/
    |-- SKILL.md
    |-- agents/
    |   `-- openai.yaml
    `-- references/
        |-- linkedin-style-guide.md
        |-- repo-review-checklist.md
        `-- visual-storyboard-guide.md
```

## Installation

### Codex

You do not need to clone the entire repository.

Ask Codex to install the skill directly from GitHub:

```text
Install this skill:
https://github.com/fidamuhrifqi/linkedin-project-story-en/tree/main/linkedin-project-story-en
```

Codex can use its built-in skill installer to download the skill into the local skills directory. Restart Codex after installation so the new skill is discovered.

You can also run the built-in installer manually.

macOS or Linux:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo fidamuhrifqi/linkedin-project-story-en \
  --path linkedin-project-story-en
```

Windows PowerShell:

```powershell
python "$HOME\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" `
  --repo fidamuhrifqi/linkedin-project-story-en `
  --path linkedin-project-story-en
```

The installer downloads only the skill folder and places it under `$CODEX_HOME/skills` or `~/.codex/skills`.

### Manual Installation

If the built-in installer is unavailable, download the repository ZIP or clone it, then copy only the `linkedin-project-story-en` folder into your Codex skills directory:

```bash
git clone https://github.com/fidamuhrifqi/linkedin-project-story-en.git
cp -R linkedin-project-story-en/linkedin-project-story-en ~/.codex/skills/
```

On Windows, the default destination is:

```text
%USERPROFILE%\.codex\skills\linkedin-project-story-en
```

Restart or reload Codex after manual installation.

### Other Skill-Compatible Agents

Copy the `linkedin-project-story-en` folder into the skills directory used by your agent. The package follows the standard `SKILL.md` structure and keeps supporting instructions under `references/`.

## Usage

Invoke the skill explicitly with `$linkedin-project-story-en`.

Review someone else's repository:

```text
Use $linkedin-project-story-en to review https://github.com/owner/project and write a medium-length English LinkedIn post from a reviewer POV.
```

Write about your own project:

```text
Use $linkedin-project-story-en for this local repository. I built this project, so use creator POV and explain the main technical lesson.
```

Create a post and an actual visual:

```text
Use $linkedin-project-story-en to review this repository, write the English LinkedIn caption, and generate the 16:9 explainer image.
```

Create only the post:

```text
Use $linkedin-project-story-en to write only a short English LinkedIn caption. Do not generate an image.
```

## Supported Inputs

- Public GitHub repository URL.
- Local repository path.
- ZIP or other repository archive.
- README or project documentation.
- Project notes and technical summaries.

The quality and accuracy of the result depend on the source material available to the agent.

## Default Output

The skill returns four sections:

1. `Project Summary` for purpose, stack, and workflow.
2. `LinkedIn Status` as one copyable text block.
3. `Animated Image Concept` with a storyboard and generation prompt.
4. `Accuracy Notes` for confirmed, inferred, and unverified details.

When a source URL is provided, the exact URL is included inside the LinkedIn caption before the hashtags.

## Design Principles

- Evidence before claims.
- Human and professional English.
- Correct project ownership point of view.
- Concrete technical observations.
- Restrained visuals instead of generic neon artwork.
- Copy-ready output with minimal cleanup.

## Customization

Edit the files under `linkedin-project-story-en/references/` to change:

- Caption tone, length, and hashtag guidance.
- Repository inspection priorities.
- Visual composition, palette, and prompt style.

Keep `SKILL.md` focused on the core workflow so the references are loaded only when needed.

## Security

The skill instructs the agent not to expose tokens, credentials, private keys, or `.env` values found during repository inspection. Always review generated content before publishing, especially when using private source material.

## License

MIT. See [LICENSE](LICENSE).
