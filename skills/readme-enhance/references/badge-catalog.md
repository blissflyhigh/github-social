# Badge Catalog

Comprehensive shields.io badge patterns organized by category. All badges use the shields.io service for consistency.

## Badge Styles

Available styles (append `?style=STYLE` to any badge URL):
- `flat` - Default flat style
- `flat-square` - Flat with square corners
- `plastic` - Gradient 3D look
- `for-the-badge` - Large, bold style (recommended for headers)
- `social` - GitHub-style social buttons

## Core Status Badges

### Build Status

**GitHub Actions**:
```markdown
[![Build Status](https://img.shields.io/github/actions/workflow/status/OWNER/REPO/WORKFLOW.yml?branch=main&style=for-the-badge)](https://github.com/OWNER/REPO/actions)
```

**Detection**: Check `.github/workflows/` for workflow files. Common names:
- `ci.yml`, `build.yml`, `test.yml`, `main.yml`

### Version Badges

**npm**:
```markdown
[![npm version](https://img.shields.io/npm/v/PACKAGE?style=for-the-badge&logo=npm)](https://www.npmjs.com/package/PACKAGE)
```

**Crates.io (Rust)**:
```markdown
[![Crates.io](https://img.shields.io/crates/v/PACKAGE?style=for-the-badge&logo=rust)](https://crates.io/crates/PACKAGE)
```

**PyPI (Python)**:
```markdown
[![PyPI](https://img.shields.io/pypi/v/PACKAGE?style=for-the-badge&logo=python&logoColor=white)](https://pypi.org/project/PACKAGE)
```

**Go**:
```markdown
[![Go Version](https://img.shields.io/github/go-mod/go-version/OWNER/REPO?style=for-the-badge&logo=go)](https://go.dev/)
```

**GitHub Release**:
```markdown
[![GitHub Release](https://img.shields.io/github/v/release/OWNER/REPO?style=for-the-badge)](https://github.com/OWNER/REPO/releases)
```

### License Badges

**Auto-detect from LICENSE file**:
```markdown
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg?style=for-the-badge)](LICENSE)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge)](LICENSE)
```

**GitHub License (auto)**:
```markdown
[![License](https://img.shields.io/github/license/OWNER/REPO?style=for-the-badge)](LICENSE)
```

### Language Badges

**Primary Language**:
```markdown
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://go.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
```

## Engagement Badges

### GitHub Metrics

**Stars**:
```markdown
[![GitHub Stars](https://img.shields.io/github/stars/OWNER/REPO?style=for-the-badge&logo=github)](https://github.com/OWNER/REPO/stargazers)
```

**Forks**:
```markdown
[![GitHub Forks](https://img.shields.io/github/forks/OWNER/REPO?style=for-the-badge&logo=github)](https://github.com/OWNER/REPO/network/members)
```

**Issues**:
```markdown
[![GitHub Issues](https://img.shields.io/github/issues/OWNER/REPO?style=for-the-badge&logo=github)](https://github.com/OWNER/REPO/issues)
```

**Pull Requests**:
```markdown
[![GitHub PRs](https://img.shields.io/github/issues-pr/OWNER/REPO?style=for-the-badge&logo=github)](https://github.com/OWNER/REPO/pulls)
```

**Last Commit**:
```markdown
[![Last Commit](https://img.shields.io/github/last-commit/OWNER/REPO?style=for-the-badge&logo=github)](https://github.com/OWNER/REPO/commits)
```

**Contributors**:
```markdown
[![Contributors](https://img.shields.io/github/contributors/OWNER/REPO?style=for-the-badge&logo=github)](https://github.com/OWNER/REPO/graphs/contributors)
```

### Community Badges

**PRs Welcome**:
```markdown
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](https://github.com/OWNER/REPO/pulls)
```

**Good First Issues**:
```markdown
[![Good First Issues](https://img.shields.io/github/issues/OWNER/REPO/good%20first%20issue?style=for-the-badge&label=good%20first%20issues)](https://github.com/OWNER/REPO/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
```

## Download & Usage Badges

**npm Downloads**:
```markdown
[![npm downloads](https://img.shields.io/npm/dm/PACKAGE?style=for-the-badge&logo=npm)](https://www.npmjs.com/package/PACKAGE)
[![npm total downloads](https://img.shields.io/npm/dt/PACKAGE?style=for-the-badge&logo=npm)](https://www.npmjs.com/package/PACKAGE)
```

**PyPI Downloads**:
```markdown
[![PyPI Downloads](https://img.shields.io/pypi/dm/PACKAGE?style=for-the-badge&logo=python&logoColor=white)](https://pypi.org/project/PACKAGE)
```

**Crates.io Downloads**:
```markdown
[![Crates.io Downloads](https://img.shields.io/crates/d/PACKAGE?style=for-the-badge&logo=rust)](https://crates.io/crates/PACKAGE)
```

## Plugin & Integration Badges

### Claude Code Plugin

```markdown
[![Claude Code Plugin](https://img.shields.io/badge/Claude%20Code-Plugin-blueviolet?style=for-the-badge&logo=anthropic&logoColor=white)](https://claude.ai/code)
```

### MCP Server

```markdown
[![MCP Server](https://img.shields.io/badge/MCP-Server-purple?style=for-the-badge)](https://modelcontextprotocol.io/)
```

### IDE Extensions

```markdown
[![VS Code](https://img.shields.io/badge/VS%20Code-Extension-007ACC?style=for-the-badge&logo=visualstudiocode)](https://marketplace.visualstudio.com/)
[![JetBrains](https://img.shields.io/badge/JetBrains-Plugin-000000?style=for-the-badge&logo=jetbrains)](https://plugins.jetbrains.com/)
```

## Quality & Coverage Badges

### Code Coverage

**Codecov**:
```markdown
[![Codecov](https://img.shields.io/codecov/c/github/OWNER/REPO?style=for-the-badge&logo=codecov)](https://codecov.io/gh/OWNER/REPO)
```

**Coveralls**:
```markdown
[![Coveralls](https://img.shields.io/coveralls/github/OWNER/REPO?style=for-the-badge&logo=coveralls)](https://coveralls.io/github/OWNER/REPO)
```

### Code Quality

**Code Climate**:
```markdown
[![Code Climate](https://img.shields.io/codeclimate/maintainability/OWNER/REPO?style=for-the-badge&logo=codeclimate)](https://codeclimate.com/github/OWNER/REPO)
```

**Snyk**:
```markdown
[![Snyk](https://img.shields.io/snyk/vulnerabilities/github/OWNER/REPO?style=for-the-badge&logo=snyk)](https://snyk.io/test/github/OWNER/REPO)
```

## Documentation Badges

**Docs Site**:
```markdown
[![Documentation](https://img.shields.io/badge/docs-online-blue?style=for-the-badge&logo=readthedocs)](https://DOCS_URL)
```

**API Reference**:
```markdown
[![API Docs](https://img.shields.io/badge/API-Reference-green?style=for-the-badge)](https://API_DOCS_URL)
```

**TypeDoc**:
```markdown
[![TypeDoc](https://img.shields.io/badge/TypeDoc-Documentation-blue?style=for-the-badge&logo=typescript)](https://TYPEDOC_URL)
```

## Social & Communication Badges

**Discord**:
```markdown
[![Discord](https://img.shields.io/discord/SERVER_ID?style=for-the-badge&logo=discord&logoColor=white&label=Discord)](https://discord.gg/INVITE)
```

**Twitter/X**:
```markdown
[![Twitter Follow](https://img.shields.io/twitter/follow/USERNAME?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/USERNAME)
```

**Slack**:
```markdown
[![Slack](https://img.shields.io/badge/Slack-Join-4A154B?style=for-the-badge&logo=slack)](https://SLACK_INVITE_URL)
```

## Sponsorship Badges

**GitHub Sponsors**:
```markdown
[![Sponsor](https://img.shields.io/badge/Sponsor-❤-ea4aaa?style=for-the-badge&logo=githubsponsors)](https://github.com/sponsors/OWNER)
```

**Buy Me a Coffee**:
```markdown
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/USERNAME)
```

**Open Collective**:
```markdown
[![Open Collective](https://img.shields.io/opencollective/all/PROJECT?style=for-the-badge&logo=opencollective)](https://opencollective.com/PROJECT)
```

## Custom Badges

### Static Badge Template

```markdown
[![Custom](https://img.shields.io/badge/LABEL-MESSAGE-COLOR?style=for-the-badge&logo=LOGO)](URL)
```

**Color options**: brightgreen, green, yellowgreen, yellow, orange, red, blue, lightgrey, blueviolet, ff69b4, or any hex color (without #)

### Common Custom Badges

**Maintained**:
```markdown
[![Maintained](https://img.shields.io/badge/Maintained-yes-green?style=for-the-badge)](https://github.com/OWNER/REPO)
```

**Made With Love**:
```markdown
[![Made with Love](https://img.shields.io/badge/Made%20with-❤-red?style=for-the-badge)](https://github.com/OWNER/REPO)
```

**Powered By**:
```markdown
[![Powered by Claude](https://img.shields.io/badge/Powered%20by-Claude-blueviolet?style=for-the-badge&logo=anthropic)](https://anthropic.com)
```

## Badge Ordering Recommendation

For optimal visual hierarchy, order badges as follows:

1. **Status**: Build, CI/CD status
2. **Version**: Package version, release
3. **License**: License type
4. **Quality**: Coverage, code quality
5. **Language/Tech**: Primary language, framework
6. **Metrics**: Downloads, stars
7. **Engagement**: PRs welcome, issues
8. **Community**: Discord, Twitter
9. **Support**: Sponsors, donations

## Badge Line Limits

Recommended limits to avoid clutter:
- **Minimal**: 3-4 badges (version, license, build)
- **Standard**: 6-8 badges (+ language, stars, downloads)
- **Comprehensive**: 10-12 badges (+ community, quality)
- **Maximum**: 15 badges (avoid exceeding this)
