---
name: README Enhancement Generator
description: This skill should be used when the user asks to "enhance readme", "add badges to readme", "create readme infographic", "improve readme marketing", "add shields.io badges", "create architecture diagram", "generate project infographic", "make readme more engaging", "add project badges", "create visual overview", or needs to improve README.md with marketing badges and visual infographics that capture project architecture, features, and purpose.
---

# README Enhancement Generator

Enhance GitHub repository README files with marketing badges and NotebookLM-style infographics that capture project architecture, features, technology, and purpose. Create engaging visual elements that attract users and communicate project value.

## Overview

This skill analyzes a project's codebase, documentation, and configuration to generate:
1. Marketing badges (shields.io format) for project metrics and status
2. A detailed infographic image prompt capturing architecture and features
3. Updated README.md with badges and infographic integrated

## Workflow

### Step 1: Check for Configuration

Look for optional settings file at `.claude/github-social.local.md`.

Parse YAML frontmatter for readme-enhance settings:
- `badge_style`: Badge style (flat, flat-square, plastic, for-the-badge)
- `badge_color`: Default badge color
- `infographic_style`: architecture | features | hybrid
- `infographic_output`: Output path for infographic image
- `update_readme`: Whether to modify README.md directly

If no config exists, use defaults:
- `badge_style`: for-the-badge
- `infographic_style`: hybrid
- `update_readme`: true

### Step 2: Analyze Project

Gather project context by reading available files:

**Primary sources**:
1. `README.md` - Current content, existing badges
2. `package.json` / `Cargo.toml` / `pyproject.toml` / `go.mod` - Name, version, description
3. `CLAUDE.md` - Project context and guidelines
4. `.github/workflows/` - CI/CD configuration
5. `LICENSE` - License type

**Extract these elements**:
- **Project name**: Official name from manifest
- **Version**: Current version number
- **License**: License type (MIT, Apache-2.0, etc.)
- **Primary language**: From file extensions or manifest
- **Package registry**: npm, crates.io, PyPI, Go modules
- **CI system**: GitHub Actions, CircleCI, Travis
- **Purpose**: What problem does it solve?
- **Architecture**: Key components and data flow
- **Features**: Top 3-5 capabilities
- **Technology stack**: Languages, frameworks, tools

### Step 3: Generate Badge Set

Create shields.io badges based on project analysis.

**Core Badges** (always include if applicable):

| Badge | Condition | Format |
|-------|-----------|--------|
| Version | Has package manifest | `![Version](https://img.shields.io/...)` |
| Build | Has CI workflow | GitHub Actions status badge |
| License | Has LICENSE file | License badge |
| Language | Detected primary | Language badge |

**Engagement Badges** (include for open source):
- GitHub Stars
- GitHub Issues
- Last Commit
- PRs Welcome

**Plugin-Specific Badges**:
- Claude Code Plugin badge (for Claude plugins)
- MCP Server badge (for MCP integrations)

**Context-Dependent Badges** (include if detected):
- Coverage (if test coverage configured)
- Documentation (if docs site exists)
- Downloads (if published to registry)
- Discord/Slack (if community links found)
- Sponsors (if FUNDING.yml exists)

**Badge Generation Rules**:
1. Detect repository owner and name from git remote
2. Use consistent style across all badges
3. Order badges by importance: status > version > metrics > engagement
4. Limit to 8-12 badges to avoid clutter

See `references/badge-catalog.md` for comprehensive badge patterns.

### Step 4: Design Infographic Concept

Create a NotebookLM-style infographic that visualizes the project.

**Determine Infographic Style** based on project type:

| Project Type | Detection | Style Weight |
|--------------|-----------|--------------|
| CLI Tool | Has bin field, command patterns | Feature-focused (70%) |
| Library/SDK | Exports APIs, no UI | Balanced (50/50) |
| Framework | Plugin system, lifecycle hooks | Architecture-focused (60%) |
| Application | Has UI, entry points | User flow + features |
| Infrastructure | Docker, K8s, cloud configs | Architecture-heavy (70%) |

**Infographic Sections**:

1. **Header Panel**
   - Project name with stylized typography
   - One-line tagline capturing essence
   - Key metric or badge (stars, downloads)

2. **Architecture Panel** (weight varies by type)
   - Component boxes with connections
   - Data flow arrows
   - Integration points
   - Layer visualization (if applicable)

3. **Features Panel** (weight varies by type)
   - Top 3-5 capabilities as icons + labels
   - Benefit statements
   - Use case snippets

4. **Technology Panel**
   - Stack visualization
   - Language/framework icons
   - Dependency highlights

5. **Call-to-Action Strip**
   - Install command
   - Quick start hint
   - Links (docs, GitHub)

See `references/infographic-prompts.md` for detailed prompt patterns.

### Step 5: Generate Infographic Prompt

Craft a detailed image generation prompt:

**Prompt Structure**:
```
NotebookLM-style infographic for [project-name], [style] layout,
[Header: project name, tagline],
[Architecture section: component visualization],
[Features section: capability icons and labels],
[Technology section: stack badges],
[Color palette based on domain],
clean modern design, professional typography,
1280x640 pixels for GitHub README display

Negative: cluttered, low contrast, hard to read text, realistic photos
```

**Color Palettes by Domain**:
- DevTools: Dark slate, cyan/teal accents
- AI/ML: Purple gradients, neural blue
- Web: Modern gradients, brand blues
- Data: Professional blues, accent oranges
- Security: Deep blues, trust greens

### Step 6: Update README.md

**Badge Placement Strategy**:

1. Locate existing badge section (lines starting with `![` after H1)
2. If found, replace entire badge block
3. If not found, insert after first H1 heading
4. Preserve any custom badges not matching generated patterns

**Badge Section Format**:
```markdown
# Project Name

[![License](badge-url)](link)
[![Version](badge-url)](link)
[![Build](badge-url)](link)
...
```

**Infographic Placement**:

1. After badge section, before main description
2. Use HTML for centering if desired
3. Include alt text for accessibility

**Infographic Section Format**:
```markdown
<p align="center">
  <img src=".github/readme-infographic.png" alt="Project Overview" width="800">
</p>
```

If infographic image not yet generated, add placeholder comment:
```markdown
<!-- TODO: Generate infographic with /readme-enhance -->
```

### Step 7: Output Results

**If update_readme is true**:
1. Write updated README.md with badges and infographic
2. Report changes made
3. Output infographic prompt for image generation

**If update_readme is false**:
1. Output badge markdown for manual insertion
2. Output infographic prompt
3. Provide placement instructions

## Error Handling

**No README.md found**:
Create minimal README with project name from manifest, then enhance.

**No package manifest found**:
Use git remote URL to extract project name, prompt for missing info.

**Git remote not configured**:
Ask user for repository owner/name for badge URLs.

**Existing custom badges**:
Preserve badges that don't match generated patterns, merge intelligently.

## Configuration Reference

Full configuration options in `.claude/github-social.local.md`:

```yaml
---
# Social preview settings (existing)
provider: dalle-3
style: minimalist

# README enhance settings (new)
badge_style: for-the-badge     # flat | flat-square | plastic | for-the-badge
badge_color: blueviolet        # Default color for custom badges
infographic_style: hybrid      # architecture | features | hybrid
infographic_output: .github/readme-infographic.png
update_readme: true            # Modify README.md directly
custom_badges: []              # Additional custom badges to include
exclude_badges: []             # Badge types to exclude
---
```

## Additional Resources

### Reference Files

For detailed patterns and comprehensive catalogs:
- **`references/badge-catalog.md`** - Complete badge patterns by category
- **`references/infographic-prompts.md`** - NotebookLM-style prompt templates
- **`references/readme-templates.md`** - Badge placement and README structure patterns

### Example Files

Working examples for different project types:
- **`examples/badges-devtools.md`** - Badge set for CLI/DevTools projects
- **`examples/badges-library.md`** - Badge set for libraries and SDKs
- **`examples/infographic-example.md`** - Complete infographic prompt example
