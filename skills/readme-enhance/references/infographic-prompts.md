# Infographic Prompt Patterns

NotebookLM-style infographic prompts for generating visual README overviews. These prompts create professional, information-dense graphics that capture project architecture, features, and purpose.

## Infographic Design Philosophy

NotebookLM-style infographics share these characteristics:
- **Information density**: Pack meaningful content without clutter
- **Visual hierarchy**: Clear sections with distinct purposes
- **Modern aesthetics**: Clean lines, subtle gradients, professional typography
- **Scannable layout**: Key information visible at a glance
- **Consistent styling**: Cohesive color palette and iconography

## Prompt Structure Template

```
Create a NotebookLM-style infographic for "[PROJECT_NAME]",
[LAYOUT_STYLE] layout optimized for GitHub README display (1280x640),

**Header Section:**
[Project name in bold typography], [tagline/description],
[key metric badge or icon]

**Architecture Section:**
[Component/system visualization description],
[Data flow or relationship arrows],
[Integration points if applicable]

**Features Section:**
[Feature 1 with icon]: [brief description]
[Feature 2 with icon]: [brief description]
[Feature 3 with icon]: [brief description]

**Technology Section:**
[Stack/language icons or badges]

**Footer/CTA:**
[Install command or quick start],
[Links represented as icons]

**Style:**
[Color palette], clean modern design, professional typography,
subtle shadows and depth, [domain-specific aesthetic]

**Technical:**
1280x640 pixels, high contrast for readability, PNG format

Negative: cluttered, low contrast, illegible text, realistic photos,
stock imagery, dated design elements
```

## Layout Styles by Project Type

### CLI/DevTools Layout (Feature-Focused 70%)

```
Create a NotebookLM-style infographic for "[PROJECT_NAME]",
horizontal feature-showcase layout (1280x640),

**Header (left 20%):**
Project name in monospace-inspired bold typography,
Terminal icon or CLI symbol,
Version badge

**Main Features Panel (center 50%):**
3-column grid of key capabilities:
- [Feature 1] with terminal/code icon
- [Feature 2] with automation/gear icon
- [Feature 3] with speed/lightning icon
Each with 2-3 word label and subtle description

**Workflow Strip (right 30%):**
Vertical flow diagram showing:
Input → Process → Output
with connecting arrows

**Footer:**
Installation command in code block style,
GitHub and docs icons

**Style:**
Dark slate (#1a1a2e) background, cyan (#06b6d4) accents,
terminal-inspired aesthetics, monospace elements,
clean geometric shapes

Negative: busy backgrounds, multiple fonts, realistic imagery
```

### Library/SDK Layout (Balanced 50/50)

```
Create a NotebookLM-style infographic for "[PROJECT_NAME]",
balanced API-showcase layout (1280x640),

**Header (top 15%):**
Library name in clean sans-serif,
Language logo, version badge,
One-line value proposition

**Left Panel - API Surface (45%):**
Stacked boxes showing key exports/functions:
- Primary API method
- Secondary capabilities
- Configuration options
Connected with subtle hierarchy lines

**Right Panel - Benefits (45%):**
Icon + text pairs:
- Performance benefit
- Developer experience benefit
- Integration benefit
Each with small supporting graphic

**Bottom Strip (10%):**
npm/pip/cargo install command,
Quick import example

**Style:**
Light background (#f8fafc), primary color accents,
professional documentation aesthetic,
code-block styling for examples

Negative: dark themes, complex diagrams, marketing fluff
```

### Framework Layout (Architecture-Focused 60%)

```
Create a NotebookLM-style infographic for "[PROJECT_NAME]",
architecture-centric layout (1280x640),

**Header (top 12%):**
Framework name with distinctive styling,
"Framework for [purpose]" tagline

**Architecture Diagram (center 55%):**
Layered component visualization:
- Top layer: User/Application
- Middle layer: Framework core components (3-4 boxes)
- Bottom layer: Integrations/Plugins
Connecting arrows showing data/control flow
Each component with icon and label

**Feature Sidebar (right 25%):**
Vertical list of key capabilities:
- Lifecycle hooks
- Plugin system
- [Key feature 3]
- [Key feature 4]

**Footer (8%):**
Getting started command,
Docs link icon

**Style:**
Gradient background (subtle), component boxes with shadows,
architectural diagram aesthetic, connection lines with arrows,
[framework color] as primary accent

Negative: flat design only, no depth, cluttered connections
```

### Application Layout (User-Flow + Features)

```
Create a NotebookLM-style infographic for "[PROJECT_NAME]",
user-journey layout (1280x640),

**Header (top 15%):**
App name with logo/icon,
"[What it does] for [who]" tagline,
Platform badges (web, mobile, desktop)

**User Flow (center 40%):**
Horizontal journey:
[Start] → [Core Action] → [Result]
Each step as rounded box with icon,
Curved connecting arrows

**Feature Grid (bottom 35%):**
2x3 or 3x2 grid of features:
Each cell: Icon + Feature name + 3-word benefit
Alternating subtle background colors

**CTA Strip (10%):**
"Try it now" or download button style,
Link icons

**Style:**
Friendly, approachable colors, rounded shapes,
app-store aesthetic, user-centric imagery,
[brand colors] palette

Negative: technical jargon, complex diagrams, dark themes
```

### Infrastructure Layout (Architecture-Heavy 70%)

```
Create a NotebookLM-style infographic for "[PROJECT_NAME]",
infrastructure architecture layout (1280x640),

**Header (compact 10%):**
Project name, infrastructure category badge,
Cloud/container icons

**System Diagram (center 65%):**
Multi-tier architecture visualization:
- Cloud/External layer (top)
- Application/Service layer (middle)
- Data/Storage layer (bottom)
Components as boxes with provider icons,
Network connections with protocol labels,
Security boundaries indicated

**Capabilities Sidebar (20%):**
Vertical feature list:
- Scalability indicator
- Security feature
- Monitoring capability
- Integration point

**Specs Footer (5%):**
Supported platforms/providers icons

**Style:**
Professional enterprise aesthetic,
Cloud diagram conventions (AWS/GCP style),
Blues and grays, high contrast for clarity,
Technical but accessible

Negative: consumer app aesthetics, playful elements
```

## Color Palettes by Domain

### DevTools/CLI
```
Background: #0f172a (dark slate), #1e293b (slate)
Primary: #06b6d4 (cyan), #14b8a6 (teal)
Accent: #f97316 (orange), #22c55e (green)
Text: #f8fafc (white), #94a3b8 (muted)
```

### AI/ML
```
Background: #1e1b4b (deep purple), #312e81 (indigo)
Primary: #8b5cf6 (violet), #a78bfa (light violet)
Accent: #06b6d4 (cyan), #3b82f6 (blue)
Text: #f8fafc (white), #c4b5fd (muted purple)
```

### Web/Frontend
```
Background: #f8fafc (light), #ffffff (white)
Primary: #3b82f6 (blue), #6366f1 (indigo)
Accent: #8b5cf6 (violet), #ec4899 (pink)
Text: #1e293b (dark), #64748b (muted)
```

### Data/Analytics
```
Background: #0c4a6e (dark blue), #164e63 (dark cyan)
Primary: #0ea5e9 (sky blue), #14b8a6 (teal)
Accent: #f59e0b (amber), #10b981 (emerald)
Text: #f0f9ff (light), #7dd3fc (muted blue)
```

### Security/Infrastructure
```
Background: #1e3a5f (navy), #1f2937 (gray)
Primary: #3b82f6 (blue), #2563eb (darker blue)
Accent: #fbbf24 (gold), #22c55e (green)
Text: #f8fafc (white), #9ca3af (muted gray)
```

## Icon Suggestions by Category

### Features
- Speed/Performance: lightning bolt, rocket, gauge
- Security: shield, lock, key
- Automation: gear, robot, flow arrows
- Integration: plug, puzzle piece, link
- Scalability: layers, expand arrows, cloud
- Developer Experience: code brackets, terminal, magic wand

### Technology
- Languages: Official logos (TS, Python, Rust, Go)
- Frameworks: React atom, Vue shield, etc.
- Cloud: AWS/GCP/Azure simplified icons
- Database: cylinder, table grid
- API: endpoint arrows, REST badge

### Actions
- Install: download arrow, package box
- Configure: sliders, settings gear
- Deploy: rocket, cloud upload
- Monitor: chart, eye, pulse

## Quality Modifiers

Add to any prompt for better results:

**For DALL-E 3**:
```
, professional quality, trending on Dribbble,
information design excellence, clear visual hierarchy
```

**For Stable Diffusion**:
```
, masterpiece, best quality, infographic style,
professional design, sharp details
```

**For Midjourney**:
```
--ar 2:1 --q 2 --stylize 250 --no text
```

## Universal Negative Prompts

Always include:
```
Negative: blurry text, illegible labels, cluttered layout,
inconsistent styling, stock photos, realistic people,
low contrast, pixelated, watermarks, dated design,
3D renders, gradients only, empty space, minimal content
```

## Responsive Considerations

For GitHub README display:
- Primary size: 1280x640 (2:1 ratio)
- Mobile fallback: Ensure key info visible at 640px width
- Text minimum: 14pt equivalent for readability
- Contrast ratio: WCAG AA (4.5:1) for text elements
