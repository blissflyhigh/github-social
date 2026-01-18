---
name: readme-enhance
description: Enhance README.md with marketing badges and a NotebookLM-style infographic
argument-hint: "[--badges-only] [--infographic-only] [--dry-run]"
allowed-tools: ["Read", "Write", "Edit", "Glob", "Grep", "Bash"]
---

# README Enhancement Command

Enhance the current project's README.md with marketing badges (shields.io) and a NotebookLM-style infographic that captures project architecture, features, and purpose.

## Execution Steps

### 1. Parse Arguments

Handle optional flags:
- `--badges-only`: Generate only badges, skip infographic
- `--infographic-only`: Generate only infographic prompt, skip badges
- `--dry-run`: Preview changes without modifying README.md

### 2. Load Configuration

Check for `.claude/github-social.local.md` and parse settings:
- `badge_style`: for-the-badge (default), flat, flat-square, plastic
- `infographic_style`: hybrid (default), architecture, features
- `update_readme`: true (default)

### 3. Analyze Project

Load the `readme-enhance` skill and follow its analysis workflow:
1. Read README.md, package manifest, CLAUDE.md
2. Detect repository owner/name from git remote
3. Extract project purpose, features, technology stack
4. Identify CI workflow files for build badges
5. Detect license type

### 4. Generate Badges

Based on project analysis, generate appropriate shields.io badges:

**Always include** (if detectable):
- Version badge (npm/crates/pypi/GitHub release)
- License badge
- Build/CI status badge
- Primary language badge

**Include for engagement**:
- GitHub stars
- Downloads (if published)
- Last commit
- PRs welcome

**Context-specific**:
- Claude Code Plugin badge (if plugin.json exists)
- Coverage badge (if codecov/coveralls configured)
- Documentation badge (if docs site exists)

### 5. Generate Infographic Prompt

Create a detailed image generation prompt following the skill's infographic patterns:
- Analyze project type (CLI, library, framework, app, infrastructure)
- Choose appropriate layout style based on type
- Include architecture visualization if applicable
- Include feature highlights
- Apply domain-appropriate color palette

### 6. Update README.md

Unless `--dry-run` is specified:

**Badge insertion**:
1. Find existing badge section (after H1, lines starting with `[![`)
2. Replace existing badges or insert new section
3. Preserve any custom badges not matching generated patterns

**Infographic placeholder**:
1. Add centered image reference after badges
2. Point to `.github/readme-infographic.png`
3. Include alt text for accessibility

### 7. Output Results

Display:
1. Summary of badges generated
2. The infographic prompt for image generation
3. Changes made to README.md (or preview if `--dry-run`)
4. Next steps (generate image, upload to GitHub)

## Example Usage

```bash
# Full enhancement
/readme-enhance

# Preview without changes
/readme-enhance --dry-run

# Only add/update badges
/readme-enhance --badges-only

# Only generate infographic prompt
/readme-enhance --infographic-only
```

## Tips

- Run `/social-preview` after this command to generate the actual infographic image
- Use `/github-social:all` to run all enhancement commands in sequence
- Badges are optimized for the `for-the-badge` style by default
- Custom badges in your README are preserved during updates
