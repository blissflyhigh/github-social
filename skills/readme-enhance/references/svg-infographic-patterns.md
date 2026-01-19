# SVG Infographic Patterns

Complete SVG templates for README infographics by project type. Each template uses a hybrid layout with customizable architecture/features balance.

## Base Infographic Structure

All infographics share this 1280x640 structure:

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER (15%): Project name, tagline, badge                 │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  MAIN CONTENT (70%):                                        │
│  Architecture panels, feature grids, flow diagrams          │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  FOOTER (15%): Install command, links                       │
└─────────────────────────────────────────────────────────────┘
```

---

## CLI / DevTools Layout (Feature-Focused 70%)

Best for command-line tools, developer utilities.

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0f172a"/>
      <stop offset="100%" style="stop-color:#1e293b"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Header -->
  <text x="640" y="55" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="36" font-weight="700" text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>
  <text x="640" y="85" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="18" text-anchor="middle" fill="#94a3b8">
    Short tagline describing the tool
  </text>

  <!-- Feature Grid (3 columns) -->
  <!-- Feature 1 -->
  <rect x="120" y="140" width="320" height="200" rx="8" fill="#1e293b" stroke="#334155" stroke-width="1"/>
  <circle cx="180" cy="200" r="24" fill="#06b6d4" opacity="0.2"/>
  <text x="180" y="207" font-family="-apple-system" font-size="24" text-anchor="middle" fill="#06b6d4">⚡</text>
  <text x="280" y="190" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" font-weight="600" fill="#f8fafc">Feature One</text>
  <text x="280" y="215" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" fill="#94a3b8">Brief description of this</text>
  <text x="280" y="235" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" fill="#94a3b8">capability goes here</text>

  <!-- Feature 2 -->
  <rect x="480" y="140" width="320" height="200" rx="8" fill="#1e293b" stroke="#334155" stroke-width="1"/>
  <circle cx="540" cy="200" r="24" fill="#06b6d4" opacity="0.2"/>
  <text x="540" y="207" font-family="-apple-system" font-size="24" text-anchor="middle" fill="#06b6d4">🔧</text>
  <text x="640" y="190" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" font-weight="600" fill="#f8fafc">Feature Two</text>
  <text x="640" y="215" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" fill="#94a3b8">Brief description of this</text>
  <text x="640" y="235" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" fill="#94a3b8">capability goes here</text>

  <!-- Feature 3 -->
  <rect x="840" y="140" width="320" height="200" rx="8" fill="#1e293b" stroke="#334155" stroke-width="1"/>
  <circle cx="900" cy="200" r="24" fill="#06b6d4" opacity="0.2"/>
  <text x="900" y="207" font-family="-apple-system" font-size="24" text-anchor="middle" fill="#06b6d4">📦</text>
  <text x="1000" y="190" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" font-weight="600" fill="#f8fafc">Feature Three</text>
  <text x="1000" y="215" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" fill="#94a3b8">Brief description of this</text>
  <text x="1000" y="235" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" fill="#94a3b8">capability goes here</text>

  <!-- Terminal Preview (small architecture element) -->
  <rect x="320" y="380" width="640" height="160" rx="8" fill="#0f172a" stroke="#334155" stroke-width="2"/>
  <rect x="320" y="380" width="640" height="28" rx="8" fill="#1e293b"/>
  <circle cx="345" cy="394" r="5" fill="#ef4444"/>
  <circle cx="365" cy="394" r="5" fill="#f59e0b"/>
  <circle cx="385" cy="394" r="5" fill="#22c55e"/>
  <text x="350" y="450" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#06b6d4">$ project-name --help</text>
  <text x="350" y="475" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#94a3b8">Usage: project-name [options] [command]</text>
  <text x="350" y="500" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#94a3b8">Commands: init, build, deploy</text>

  <!-- Footer -->
  <text x="640" y="590" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" text-anchor="middle" fill="#64748b">
    npm install -g project-name
  </text>
  <text x="640" y="615" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="12" text-anchor="middle" fill="#475569">
    MIT License • docs.example.com
  </text>
</svg>
```

---

## Library / SDK Layout (Balanced 50/50)

Best for APIs, libraries, SDKs.

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#1e1b4b"/>
      <stop offset="100%" style="stop-color:#312e81"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Header -->
  <text x="640" y="55" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="36" font-weight="700" text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>
  <text x="640" y="85" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="18" text-anchor="middle" fill="#c4b5fd">
    A library for doing something useful
  </text>

  <!-- Left: API Architecture (50%) -->
  <text x="320" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" font-weight="600" text-anchor="middle" fill="#a5b4fc">
    ARCHITECTURE
  </text>

  <!-- API layers -->
  <rect x="120" y="150" width="400" height="60" rx="4" fill="#8b5cf6" opacity="0.2" stroke="#8b5cf6" stroke-width="1"/>
  <text x="320" y="187" font-family="-apple-system" font-size="16" font-weight="500" text-anchor="middle" fill="#f8fafc">
    Public API Layer
  </text>

  <rect x="160" y="230" width="320" height="50" rx="4" fill="#a78bfa" opacity="0.15" stroke="#a78bfa" stroke-width="1"/>
  <text x="320" y="262" font-family="-apple-system" font-size="14" text-anchor="middle" fill="#e0e7ff">
    Core Logic
  </text>

  <rect x="200" y="300" width="240" height="45" rx="4" fill="#c4b5fd" opacity="0.1" stroke="#c4b5fd" stroke-width="1"/>
  <text x="320" y="328" font-family="-apple-system" font-size="13" text-anchor="middle" fill="#c4b5fd">
    Data Layer
  </text>

  <!-- Connection arrows -->
  <path d="M320 210 L320 230" stroke="#8b5cf6" stroke-width="2" fill="none"/>
  <path d="M320 280 L320 300" stroke="#a78bfa" stroke-width="2" fill="none"/>

  <!-- Right: Features (50%) -->
  <text x="960" y="130" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" font-weight="600" text-anchor="middle" fill="#a5b4fc">
    FEATURES
  </text>

  <!-- Feature list -->
  <rect x="760" y="150" width="400" height="55" rx="4" fill="#1e1b4b" stroke="#4c1d95" stroke-width="1"/>
  <text x="780" y="183" font-family="-apple-system" font-size="15" font-weight="500" fill="#f8fafc">
    ✓ Type-safe API
  </text>

  <rect x="760" y="215" width="400" height="55" rx="4" fill="#1e1b4b" stroke="#4c1d95" stroke-width="1"/>
  <text x="780" y="248" font-family="-apple-system" font-size="15" font-weight="500" fill="#f8fafc">
    ✓ Zero dependencies
  </text>

  <rect x="760" y="280" width="400" height="55" rx="4" fill="#1e1b4b" stroke="#4c1d95" stroke-width="1"/>
  <text x="780" y="313" font-family="-apple-system" font-size="15" font-weight="500" fill="#f8fafc">
    ✓ Tree-shakeable
  </text>

  <!-- Code example -->
  <rect x="120" y="380" width="1040" height="140" rx="8" fill="#0f0e1a" stroke="#4c1d95" stroke-width="1"/>
  <text x="150" y="420" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#c4b5fd">import</text>
  <text x="210" y="420" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#f8fafc">{ something }</text>
  <text x="345" y="420" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#c4b5fd">from</text>
  <text x="395" y="420" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#a5f3fc">'project-name'</text>
  <text x="150" y="455" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#94a3b8">// Simple usage example</text>
  <text x="150" y="485" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" fill="#f8fafc">const result = something.process(data)</text>

  <!-- Footer -->
  <text x="640" y="590" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" text-anchor="middle" fill="#64748b">
    npm install project-name
  </text>
  <text x="640" y="615" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="12" text-anchor="middle" fill="#6366f1">
    TypeScript • MIT License
  </text>
</svg>
```

---

## Framework Layout (Architecture-Focused 60%)

Best for frameworks with plugin systems, lifecycle hooks.

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0c4a6e"/>
      <stop offset="100%" style="stop-color:#075985"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Header -->
  <text x="640" y="50" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="32" font-weight="700" text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>
  <text x="640" y="78" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="16" text-anchor="middle" fill="#7dd3fc">
    A framework for building amazing things
  </text>

  <!-- Architecture Diagram (Center 60%) -->
  <!-- Top layer: User/App -->
  <rect x="440" y="110" width="400" height="50" rx="4" fill="#0369a1" stroke="#0ea5e9" stroke-width="2"/>
  <text x="640" y="142" font-family="-apple-system" font-size="16" font-weight="600" text-anchor="middle" fill="#f8fafc">
    Your Application
  </text>

  <!-- Arrow down -->
  <path d="M640 160 L640 185" stroke="#38bdf8" stroke-width="2" fill="none" marker-end="url(#arrow)"/>

  <!-- Framework core -->
  <rect x="340" y="190" width="600" height="120" rx="6" fill="#0c4a6e" stroke="#0ea5e9" stroke-width="2"/>
  <text x="640" y="220" font-family="-apple-system" font-size="18" font-weight="700" text-anchor="middle" fill="#f8fafc">
    Framework Core
  </text>

  <!-- Core components row -->
  <rect x="370" y="240" width="120" height="50" rx="4" fill="#0369a1" opacity="0.5"/>
  <text x="430" y="272" font-family="-apple-system" font-size="12" text-anchor="middle" fill="#bae6fd">Router</text>

  <rect x="510" y="240" width="120" height="50" rx="4" fill="#0369a1" opacity="0.5"/>
  <text x="570" y="272" font-family="-apple-system" font-size="12" text-anchor="middle" fill="#bae6fd">State</text>

  <rect x="650" y="240" width="120" height="50" rx="4" fill="#0369a1" opacity="0.5"/>
  <text x="710" y="272" font-family="-apple-system" font-size="12" text-anchor="middle" fill="#bae6fd">Lifecycle</text>

  <rect x="790" y="240" width="120" height="50" rx="4" fill="#0369a1" opacity="0.5"/>
  <text x="850" y="272" font-family="-apple-system" font-size="12" text-anchor="middle" fill="#bae6fd">Plugins</text>

  <!-- Arrows to plugins -->
  <path d="M640 310 L640 340" stroke="#38bdf8" stroke-width="2" fill="none"/>
  <path d="M440 310 L440 340" stroke="#38bdf8" stroke-width="1" opacity="0.5" fill="none"/>
  <path d="M840 310 L840 340" stroke="#38bdf8" stroke-width="1" opacity="0.5" fill="none"/>

  <!-- Plugin layer -->
  <rect x="140" y="345" width="200" height="80" rx="4" fill="#164e63" stroke="#22d3ee" stroke-width="1"/>
  <text x="240" y="375" font-family="-apple-system" font-size="13" font-weight="500" text-anchor="middle" fill="#f8fafc">Plugin A</text>
  <text x="240" y="400" font-family="-apple-system" font-size="11" text-anchor="middle" fill="#67e8f9">Database</text>

  <rect x="440" y="345" width="200" height="80" rx="4" fill="#164e63" stroke="#22d3ee" stroke-width="1"/>
  <text x="540" y="375" font-family="-apple-system" font-size="13" font-weight="500" text-anchor="middle" fill="#f8fafc">Plugin B</text>
  <text x="540" y="400" font-family="-apple-system" font-size="11" text-anchor="middle" fill="#67e8f9">Auth</text>

  <rect x="740" y="345" width="200" height="80" rx="4" fill="#164e63" stroke="#22d3ee" stroke-width="1"/>
  <text x="840" y="375" font-family="-apple-system" font-size="13" font-weight="500" text-anchor="middle" fill="#f8fafc">Plugin C</text>
  <text x="840" y="400" font-family="-apple-system" font-size="11" text-anchor="middle" fill="#67e8f9">Cache</text>

  <rect x="1040" y="345" width="100" height="80" rx="4" fill="#164e63" stroke="#22d3ee" stroke-width="1" stroke-dasharray="4"/>
  <text x="1090" y="392" font-family="-apple-system" font-size="11" text-anchor="middle" fill="#67e8f9">+ More</text>

  <!-- Features sidebar (right 30%) -->
  <text x="120" y="470" font-family="-apple-system" font-size="13" font-weight="600" fill="#7dd3fc">KEY FEATURES</text>
  <text x="120" y="500" font-family="-apple-system" font-size="13" fill="#f8fafc">✓ Plugin architecture</text>
  <text x="120" y="525" font-family="-apple-system" font-size="13" fill="#f8fafc">✓ Hot module reload</text>
  <text x="120" y="550" font-family="-apple-system" font-size="13" fill="#f8fafc">✓ Built-in testing</text>

  <!-- Footer -->
  <text x="640" y="590" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" text-anchor="middle" fill="#64748b">
    npx create-project-name my-app
  </text>
  <text x="640" y="615" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="12" text-anchor="middle" fill="#0ea5e9">
    docs.projectname.dev • MIT License
  </text>
</svg>
```

---

## Claude Code Plugin Layout

Best for Claude Code plugins, MCP servers.

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#1e1b4b"/>
      <stop offset="100%" style="stop-color:#312e81"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Plugin badge -->
  <rect x="520" y="25" width="240" height="32" rx="16" fill="#8b5cf6" opacity="0.25"/>
  <text x="640" y="47" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" font-weight="600" text-anchor="middle" fill="#c4b5fd">
    Claude Code Plugin
  </text>

  <!-- Header -->
  <text x="640" y="100" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="42" font-weight="700" text-anchor="middle" fill="#f8fafc">
    PLUGIN-NAME
  </text>
  <text x="640" y="135" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="18" text-anchor="middle" fill="#a5b4fc">
    Plugin tagline describing what it does
  </text>

  <!-- Workflow diagram -->
  <text x="640" y="180" font-family="-apple-system" font-size="12" font-weight="600"
        text-anchor="middle" fill="#8b5cf6">HOW IT WORKS</text>

  <!-- Step 1 -->
  <rect x="180" y="200" width="240" height="100" rx="8" fill="#1e1b4b" stroke="#4c1d95" stroke-width="1"/>
  <circle cx="220" cy="230" r="16" fill="#8b5cf6" opacity="0.3"/>
  <text x="220" y="235" font-family="-apple-system" font-size="14" font-weight="700"
        text-anchor="middle" fill="#c4b5fd">1</text>
  <text x="300" y="240" font-family="-apple-system" font-size="14" font-weight="600" fill="#f8fafc">Analyze</text>
  <text x="300" y="265" font-family="-apple-system" font-size="12" fill="#94a3b8">Reads project files</text>

  <!-- Arrow -->
  <path d="M420 250 L480 250" stroke="#8b5cf6" stroke-width="2" fill="none"/>
  <path d="M475 245 L485 250 L475 255" fill="#8b5cf6"/>

  <!-- Step 2 -->
  <rect x="520" y="200" width="240" height="100" rx="8" fill="#1e1b4b" stroke="#4c1d95" stroke-width="1"/>
  <circle cx="560" cy="230" r="16" fill="#8b5cf6" opacity="0.3"/>
  <text x="560" y="235" font-family="-apple-system" font-size="14" font-weight="700"
        text-anchor="middle" fill="#c4b5fd">2</text>
  <text x="640" y="240" font-family="-apple-system" font-size="14" font-weight="600" fill="#f8fafc">Generate</text>
  <text x="640" y="265" font-family="-apple-system" font-size="12" fill="#94a3b8">Creates output</text>

  <!-- Arrow -->
  <path d="M760 250 L820 250" stroke="#8b5cf6" stroke-width="2" fill="none"/>
  <path d="M815 245 L825 250 L815 255" fill="#8b5cf6"/>

  <!-- Step 3 -->
  <rect x="860" y="200" width="240" height="100" rx="8" fill="#1e1b4b" stroke="#4c1d95" stroke-width="1"/>
  <circle cx="900" cy="230" r="16" fill="#8b5cf6" opacity="0.3"/>
  <text x="900" y="235" font-family="-apple-system" font-size="14" font-weight="700"
        text-anchor="middle" fill="#c4b5fd">3</text>
  <text x="980" y="240" font-family="-apple-system" font-size="14" font-weight="600" fill="#f8fafc">Apply</text>
  <text x="980" y="265" font-family="-apple-system" font-size="12" fill="#94a3b8">Updates files</text>

  <!-- Feature cards -->
  <rect x="180" y="340" width="260" height="140" rx="8" fill="#312e81" stroke="#4c1d95" stroke-width="1"/>
  <text x="200" y="375" font-family="-apple-system" font-size="16" font-weight="600" fill="#f8fafc">Skills</text>
  <text x="200" y="400" font-family="-apple-system" font-size="13" fill="#a5b4fc">• skill-one</text>
  <text x="200" y="420" font-family="-apple-system" font-size="13" fill="#a5b4fc">• skill-two</text>
  <text x="200" y="440" font-family="-apple-system" font-size="13" fill="#a5b4fc">• skill-three</text>

  <rect x="510" y="340" width="260" height="140" rx="8" fill="#312e81" stroke="#4c1d95" stroke-width="1"/>
  <text x="530" y="375" font-family="-apple-system" font-size="16" font-weight="600" fill="#f8fafc">Commands</text>
  <text x="530" y="400" font-family="-apple-system" font-size="13" fill="#a5b4fc">/command-one</text>
  <text x="530" y="420" font-family="-apple-system" font-size="13" fill="#a5b4fc">/command-two</text>
  <text x="530" y="440" font-family="-apple-system" font-size="13" fill="#a5b4fc">/command-three</text>

  <rect x="840" y="340" width="260" height="140" rx="8" fill="#312e81" stroke="#4c1d95" stroke-width="1"/>
  <text x="860" y="375" font-family="-apple-system" font-size="16" font-weight="600" fill="#f8fafc">Agents</text>
  <text x="860" y="400" font-family="-apple-system" font-size="13" fill="#a5b4fc">• agent-one</text>
  <text x="860" y="420" font-family="-apple-system" font-size="13" fill="#a5b4fc">• agent-two</text>

  <!-- Footer -->
  <rect x="440" y="520" width="400" height="40" rx="6" fill="#0f0e1a"/>
  <text x="640" y="546" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" text-anchor="middle" fill="#06b6d4">
    claude plugin install owner/plugin-name
  </text>

  <text x="640" y="600" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="12" text-anchor="middle" fill="#6366f1">
    MIT License • github.com/owner/plugin-name
  </text>
</svg>
```

---

## Minimal Variant

For `svg_style: minimal`, reduce any template to essentials:

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0f172a"/>
      <stop offset="100%" style="stop-color:#1e293b"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Single accent shape -->
  <circle cx="640" cy="260" r="100" fill="#06b6d4" opacity="0.1"/>

  <!-- Project name -->
  <text x="640" y="320" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="56" font-weight="700" text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="370" font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" text-anchor="middle" fill="#94a3b8">
    Short tagline here
  </text>

  <!-- Simple install hint -->
  <text x="640" y="520" font-family="'SF Mono', 'Fira Code', monospace"
        font-size="14" text-anchor="middle" fill="#64748b">
    npm install project-name
  </text>
</svg>
```

---

## Dark Mode Conversion

To create dark mode variants:

1. **Swap backgrounds**: Light (#f8fafc) ↔ Dark (#0f172a)
2. **Adjust text colors**: Dark text → Light text
3. **Brighten accents**: Increase opacity or use lighter variants
4. **Save separately**: `infographic.svg` + `infographic-dark.svg`

Use `<picture>` element in README for automatic switching.
