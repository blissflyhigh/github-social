# Repository Description Patterns

Templates and patterns for writing engaging GitHub repository descriptions by project type.

## Universal Structure

```
[Action/What] + [For whom/platform] + [Key benefit/feature]
```

Keep under 350 characters. Lead with the most important information.

## Patterns by Project Type

### Library / Package

**Pattern:**
```
[Verb] [capability] for [platform]. [Key differentiator or features].
```

**Examples:**
```
Parse and validate JSON schemas in TypeScript with detailed error messages and JSON Schema Draft 2020-12 support.
(112 chars)

Fast, lightweight state management for React. Zero dependencies, TypeScript-first, with built-in devtools integration.
(118 chars)

Generate type-safe API clients from OpenAPI specs. Supports REST, GraphQL, and gRPC with automatic retry logic.
(111 chars)
```

### CLI Tool

**Pattern:**
```
[Verb] [what] from the command line. [Key feature or benefit].
```

**Examples:**
```
Manage Kubernetes clusters from the command line with intelligent auto-completion and multi-context support.
(108 chars)

Analyze code quality and security vulnerabilities directly in your terminal. Supports 30+ languages.
(101 chars)

Automate git workflows with smart commits, interactive rebasing, and branch management.
(87 chars)
```

### Framework

**Pattern:**
```
[Adjective] framework for [building what]. [Philosophy or key feature].
```

**Examples:**
```
Minimal web framework for building APIs in Go. Convention over configuration with zero external dependencies.
(110 chars)

Full-stack TypeScript framework for building real-time applications. Server components, edge-ready, type-safe.
(111 chars)

Opinionated Python framework for ML pipelines. Reproducible experiments, automatic versioning, cloud-native.
(109 chars)
```

### Application / Tool

**Pattern:**
```
[What it is] that [what it does]. [Primary benefit].
```

**Examples:**
```
Desktop app for managing SSH connections and tunnels. Save configurations, organize by project, sync across devices.
(116 chars)

Visual database designer that generates migrations. Supports PostgreSQL, MySQL, and SQLite with team collaboration.
(115 chars)

Code review assistant that analyzes PRs for bugs, security issues, and style violations. Integrates with GitHub Actions.
(120 chars)
```

### Plugin / Extension

**Pattern:**
```
[Platform] [type] for [capability]. [Key features].
```

**Examples:**
```
VS Code extension for inline API documentation. Hover for docs, jump to definitions, auto-complete from OpenAPI specs.
(118 chars)

Claude Code plugin for generating social preview images. Analyzes project intent, supports DALL-E and Stable Diffusion.
(119 chars)

Webpack plugin for automatic bundle analysis. Visualize dependencies, find duplicates, optimize chunk splitting.
(112 chars)
```

### Data / ML Project

**Pattern:**
```
[Verb] [what] with [approach/tech]. [Scale or performance note].
```

**Examples:**
```
Train and deploy ML models with a unified API. Supports PyTorch, TensorFlow, and JAX with distributed training.
(112 chars)

Process large datasets in parallel with automatic memory management. Handles TB-scale data on commodity hardware.
(113 chars)

Fine-tune LLMs on custom data with LoRA and QLoRA. Supports Llama, Mistral, and Falcon with 4-bit quantization.
(111 chars)
```

## Power Words for Descriptions

### Action Verbs (Start with these)
- **Build/Create**: Build, Create, Generate, Design, Craft
- **Improve/Optimize**: Optimize, Accelerate, Enhance, Streamline, Simplify
- **Manage/Control**: Manage, Control, Orchestrate, Coordinate, Monitor
- **Analyze/Process**: Analyze, Parse, Process, Transform, Extract
- **Connect/Integrate**: Connect, Integrate, Bridge, Sync, Link

### Benefit Words
- **Speed**: Fast, Lightweight, Instant, Real-time, Blazing
- **Quality**: Type-safe, Robust, Reliable, Production-ready, Battle-tested
- **Ease**: Simple, Intuitive, Zero-config, Plug-and-play, Batteries-included
- **Scale**: Scalable, Distributed, Cloud-native, Enterprise-grade

### Avoid These
- "A/An/The" at the start
- "This is..."
- "Best/Ultimate/Amazing" (unsubstantiated superlatives)
- Version numbers
- Excessive punctuation (!!!)
- All caps
- Emojis in description

## Length Guidelines

| Type | Ideal Length | Maximum |
|------|--------------|---------|
| Concise | 80-120 chars | 150 chars |
| Standard | 120-180 chars | 250 chars |
| Detailed | 180-280 chars | 350 chars |

## SEO Considerations

Include searchable terms naturally:
- Primary language/framework name
- Problem domain keywords
- Common search terms for the category

**Good (includes searchable terms):**
```
TypeScript ORM for PostgreSQL and MySQL with migrations, type-safe queries, and automatic schema generation.
```

**Poor (missing searchable terms):**
```
Database tool with various features for working with data.
```

## A/B Testing Your Description

Before finalizing, ask:
1. Does it answer "What does this do?" in the first 10 words?
2. Would someone searching for this problem find these keywords?
3. Is it specific enough to differentiate from similar projects?
4. Does it avoid jargon that limits the audience?
5. Is the most important information at the beginning?
