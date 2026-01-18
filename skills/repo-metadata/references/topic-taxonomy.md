# GitHub Topics Taxonomy

Comprehensive reference for selecting relevant GitHub repository topics.

## Topic Rules

- **Lowercase only**: `machine-learning` not `Machine-Learning`
- **Hyphens for spaces**: `web-development` not `web_development`
- **Max 50 characters** per topic
- **Max 20 topics** per repository
- **No special characters**: Letters, numbers, hyphens only

## Core Categories

### Languages (pick 1-2)

```
python javascript typescript rust go java kotlin swift ruby php
c cpp csharp fsharp scala elixir clojure haskell ocaml erlang
lua perl r julia dart zig nim v crystal
```

### Runtimes / Platforms (pick 0-2)

```
nodejs deno bun dotnet jvm browser webassembly wasm
android ios macos linux windows cross-platform
```

### Package Managers / Registries (pick 0-1)

```
npm pip cargo crates-io pypi rubygems maven gradle nuget
homebrew apt snap docker-hub
```

### Web Frameworks (pick relevant)

**Frontend:**
```
react vue angular svelte solid nextjs nuxt remix gatsby
astro qwik htmx alpine tailwindcss
```

**Backend:**
```
express fastify nestjs koa hapi django flask fastapi
rails sinatra phoenix gin echo fiber actix axum
spring spring-boot quarkus micronaut
```

**Full-stack:**
```
nextjs nuxt remix blitz redwood t3-stack
```

### Data & ML (pick relevant)

**ML/AI:**
```
machine-learning deep-learning neural-network artificial-intelligence
pytorch tensorflow keras jax scikit-learn
llm large-language-model nlp natural-language-processing
computer-vision image-recognition generative-ai
transformers huggingface openai langchain
```

**Data:**
```
data-science data-analysis data-engineering data-pipeline
pandas numpy scipy matplotlib seaborn plotly
jupyter notebook data-visualization
sql database postgresql mysql mongodb redis
etl apache-spark apache-kafka apache-airflow
```

### DevOps & Infrastructure (pick relevant)

```
devops ci-cd continuous-integration continuous-deployment
docker kubernetes k8s helm terraform ansible
aws azure gcp google-cloud cloudflare vercel
serverless lambda edge-computing
monitoring logging observability prometheus grafana
```

### Developer Tools (pick relevant)

```
developer-tools devtools cli command-line terminal
code-quality linting formatting testing
documentation api-documentation openapi swagger
git github gitlab version-control
ide vscode vim neovim emacs
```

### Domain-Specific (pick 2-4 relevant)

**Security:**
```
security cybersecurity encryption authentication authorization
oauth jwt api-security penetration-testing vulnerability-scanner
```

**Finance:**
```
fintech finance trading cryptocurrency blockchain web3
payment-processing accounting
```

**Gaming:**
```
game-development gamedev unity unreal godot
graphics 3d rendering opengl vulkan webgl
```

**IoT/Hardware:**
```
iot internet-of-things embedded raspberry-pi arduino
hardware robotics sensors
```

**Communication:**
```
messaging chat real-time websocket grpc
email notifications push-notifications
```

### Project Characteristics (pick 1-3)

**Maturity:**
```
production-ready stable beta alpha experimental
```

**Style:**
```
minimal lightweight fast blazing-fast
batteries-included full-featured opinionated
type-safe strongly-typed
```

**Community:**
```
open-source hacktoberfest good-first-issues
beginner-friendly well-documented
```

## Topic Selection Strategy

### Recommended Distribution (10 topics)

| Category | Count | Priority |
|----------|-------|----------|
| Language | 1-2 | Required |
| Framework/Library | 1-2 | If applicable |
| Domain | 2-3 | Important |
| Features | 2-3 | Differentiators |
| Community/Style | 1-2 | Optional |

### Example Topic Sets

**Python Data Science Library:**
```
python data-science pandas numpy data-analysis
data-visualization jupyter pip open-source machine-learning
```

**React UI Component Library:**
```
react typescript components ui-library design-system
frontend npm tailwindcss accessible open-source
```

**Rust CLI Tool:**
```
rust cli command-line terminal devtools
fast cross-platform cargo open-source unix
```

**Go Kubernetes Tool:**
```
go golang kubernetes k8s devops
cloud-native infrastructure cli kubectl
```

**TypeScript API Framework:**
```
typescript nodejs api rest graphql
backend framework fastify type-safe npm
```

**Machine Learning Project:**
```
python machine-learning deep-learning pytorch
neural-network ai computer-vision transformers huggingface
```

## Topics to Always Consider

### If Open Source
```
open-source
```

### If Participating in Hacktoberfest
```
hacktoberfest
```

### If Beginner Friendly
```
beginner-friendly good-first-issues
```

### If Well Documented
```
well-documented
```

## Topics to Avoid

- **Too generic**: `code`, `software`, `project`, `tool`
- **Misspellings**: `javacript`, `pythn`
- **Redundant with language**: `python-library` (just use `python`)
- **Marketing terms**: `best`, `awesome`, `amazing`
- **Version-specific**: `python3`, `es6` (unless critical)
- **Overly specific**: `my-company-internal-tool`

## Topic Discovery Tips

1. **Check similar projects** - What topics do popular similar repos use?
2. **Search GitHub** - What terms would users search?
3. **Explore trending** - What topics are currently popular in your domain?
4. **Use GitHub's suggestions** - When adding topics, GitHub suggests related ones
5. **Check package registry** - npm/PyPI keywords often make good topics
