---
name: all
description: Run all github-social skills in sequence - metadata, social preview, and README enhancement
argument-hint: "[--apply] [--dry-run] [--skip-badges] [--skip-infographic]"
allowed-tools: ["Read", "Write", "Edit", "Glob", "Grep", "Bash", "MCPSearch"]
---

# Complete GitHub Social Enhancement

Run all github-social skills in sequence to fully optimize a repository's presentation:

1. **repo-metadata**: Generate optimized description and topics
2. **social-preview**: Generate social preview image
3. **readme-enhance**: Add badges and infographic to README

## Execution Steps

### 1. Parse Arguments

Handle optional flags:
- `--apply`: Apply all changes (update GitHub metadata, modify README, upload images)
- `--dry-run`: Preview all changes without applying any
- `--skip-badges`: Skip badge generation in README enhancement
- `--skip-infographic`: Skip infographic generation

Default behavior: Generate and preview, prompt before applying.

### 2. Load Configuration

Read `.claude/github-social.local.md` for all skill settings:
- Social preview provider and style
- Badge style preferences
- Infographic style preferences
- Upload settings

### 3. Analyze Project (Shared)

Perform comprehensive project analysis once, reuse across all skills:

1. Read README.md, package manifest, CLAUDE.md
2. Extract from git remote: owner, repo name, default branch
3. Identify:
   - Project name and version
   - Purpose and key features
   - Primary language and frameworks
   - CI/CD configuration
   - License type
   - Documentation sites
   - Community links

### 4. Execute Skills in Sequence

#### Step 4a: Repository Metadata

Generate optimized GitHub metadata:
- Description (max 350 chars, engaging, SEO-friendly)
- Topics (max 20, lowercase, hyphenated)

Output preview of changes.

#### Step 4b: Social Preview Image

Generate social preview:
- Create image prompt based on project analysis
- If provider configured, generate actual image
- Save to configured output path (default: `.github/social-preview.png`)

Output the image prompt (and image location if generated).

#### Step 4c: README Enhancement

Unless `--skip-badges` and `--skip-infographic` both set:
- Generate shields.io badges (unless `--skip-badges`)
- Generate infographic prompt (unless `--skip-infographic`)
- Prepare README.md updates

Output badge set and infographic prompt.

### 5. Present Summary

Display complete summary:

```
## GitHub Social Enhancement Summary

### Repository Metadata
- Description: "..." (X chars)
- Topics: topic-1, topic-2, topic-3, ...

### Social Preview
- Image prompt generated
- Output: .github/social-preview.png
- [Generated/Pending generation]

### README Enhancement
- Badges: X badges generated
- Infographic: Prompt ready
- README changes: [Preview/Applied]

### Next Steps
[Instructions based on --apply flag]
```

### 6. Apply Changes (if --apply or confirmed)

If `--apply` flag or user confirms:

1. **Update GitHub metadata** (via gh CLI):
   ```bash
   gh repo edit --description "..."
   gh repo edit --add-topic topic-1 --add-topic topic-2 ...
   ```

2. **Generate and upload social preview** (if provider configured):
   - Generate image via configured provider
   - Upload to repository if `upload_to_repo: true`

3. **Update README.md**:
   - Insert/update badge section
   - Add infographic placeholder/image

4. **Report results**:
   - Confirm each step completed
   - Provide GitHub settings links for manual steps

## Example Usage

```bash
# Preview all enhancements
/github-social:all

# Apply all changes automatically
/github-social:all --apply

# Dry run to see what would change
/github-social:all --dry-run

# Skip certain features
/github-social:all --apply --skip-infographic
/github-social:all --apply --skip-badges
```

## Tips

- Run without `--apply` first to review changes
- Ensure `gh` CLI is authenticated for metadata updates
- Configure `.claude/github-social.local.md` for image generation
- Social preview requires manual GitHub settings update after upload
- Use `--dry-run` to safely preview all changes

## Related Commands

- `/social-preview` - Generate social preview image only
- `/repo-metadata` - Generate metadata only
- `/readme-enhance` - Enhance README only
- `/github-social:setup` - Configure plugin settings
