# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.0] - 2025-01-18

### Added

- **[readme-enhance]**: New skill for README enhancement with marketing badges and infographics
  - Generates shields.io badges based on project analysis (version, build, license, downloads, language, etc.)
  - Creates NotebookLM-style infographic prompts capturing architecture and features
  - Hybrid infographic style adapts to project type (CLI, library, framework, app, infrastructure)
  - Direct README.md modification with intelligent badge section management
  - Comprehensive reference documentation for badge patterns and infographic prompts
- **[/readme-enhance]**: New command to enhance README with badges and infographic
  - Supports `--badges-only`, `--infographic-only`, and `--dry-run` flags
- **[/github-social:all]**: New command to run all skills in sequence
  - Executes repo-metadata, social-preview, and readme-enhance in order
  - Supports `--apply`, `--dry-run`, `--skip-badges`, and `--skip-infographic` flags
  - Shared project analysis for efficiency

### Changed

- Updated plugin version to 0.4.0
- Enhanced README documentation with new features and commands

## [0.3.0] - 2025-01-18

### Added

- **[social-preview]**: Added `upload_to_repo` option to automatically upload generated images to GitHub repository
  - Uses GitHub MCP tool for seamless integration
  - Configurable via `.claude/github-social.local.md`
- **[CI/CD]**: Added GitHub Actions workflow and templates
  - Pull request template
  - Copilot instructions

### Changed

- Improved social preview skill workflow documentation

## [0.2.0] - 2025-01-18

### Added

- **[repo-metadata]**: New skill for generating optimized repository descriptions and topics
  - SEO-friendly descriptions (max 350 chars)
  - Topic suggestions for discoverability (max 20 topics)
  - Apply changes via `gh` CLI or output for manual review
- **[/repo-metadata]**: New command with `--apply` flag for direct GitHub updates
- GitHub activity badges in README (stars, issues, last commit, PRs welcome)

### Changed

- Updated badge URLs for renamed repository

## [0.1.0] - 2025-01-18

### Added

- **[social-preview]**: Initial skill for generating GitHub social preview images
  - Analyzes project files (README, package.json, CLAUDE.md) to understand purpose
  - Generates detailed image prompts capturing project spirit
  - Supports multiple providers (DALL-E, Stable Diffusion, Midjourney, manual)
  - Outputs images meeting GitHub requirements (1280x640px, <1MB)
- **[/social-preview]**: Command to generate social preview images
- **[/github-social:setup]**: Interactive setup wizard for configuration
- Configuration via `.claude/github-social.local.md` with YAML frontmatter
- MIT License

[Unreleased]: https://github.com/zircote/github-social/compare/v0.4.0...HEAD
[0.4.0]: https://github.com/zircote/github-social/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/zircote/github-social/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/zircote/github-social/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/zircote/github-social/releases/tag/v0.1.0
