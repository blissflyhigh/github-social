# SVG Templates for Social Preview

Complete SVG templates for generating social preview images by domain. Each template follows the minimal/clean aesthetic with domain-specific visual elements.

## Base Template Structure

All templates share this foundation:

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg-gradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:[start-color]"/>
      <stop offset="100%" style="stop-color:[end-color]"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg-gradient)"/>

  <!-- Domain-specific visual elements go here -->

  <!-- Project name -->
  <text x="640" y="340"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', 'Segoe UI', sans-serif"
        font-size="72" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline (optional) -->
  <text x="640" y="400"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="24" font-weight="400"
        text-anchor="middle" fill="#94a3b8">
    Short tagline here
  </text>
</svg>
```

---

## DevTools / CLI Template

**Color Palette**:
- Background gradient: #0f172a → #1e293b
- Accent: #06b6d4 (cyan)
- Text: #f8fafc

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

  <!-- Terminal window frame (minimal style) -->
  <rect x="340" y="120" width="600" height="400" rx="8" fill="#0f172a" stroke="#334155" stroke-width="2"/>

  <!-- Terminal title bar dots -->
  <circle cx="375" cy="145" r="6" fill="#ef4444"/>
  <circle cx="400" cy="145" r="6" fill="#f59e0b"/>
  <circle cx="425" cy="145" r="6" fill="#22c55e"/>

  <!-- Command prompt accent line -->
  <rect x="375" y="200" width="400" height="3" rx="1" fill="#06b6d4"/>

  <!-- Cursor block -->
  <rect x="375" y="240" width="12" height="24" fill="#06b6d4" opacity="0.8"/>

  <!-- Project name -->
  <text x="640" y="340"
        font-family="'SF Mono', 'Fira Code', 'Consolas', monospace"
        font-size="48" font-weight="600"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="390"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" font-weight="400"
        text-anchor="middle" fill="#94a3b8">
    Command-line tool tagline
  </text>

  <!-- Decorative corner brackets -->
  <path d="M100 140 L100 100 L140 100" stroke="#06b6d4" stroke-width="3" fill="none" opacity="0.5"/>
  <path d="M1180 140 L1180 100 L1140 100" stroke="#06b6d4" stroke-width="3" fill="none" opacity="0.5"/>
  <path d="M100 500 L100 540 L140 540" stroke="#06b6d4" stroke-width="3" fill="none" opacity="0.5"/>
  <path d="M1180 500 L1180 540 L1140 540" stroke="#06b6d4" stroke-width="3" fill="none" opacity="0.5"/>
</svg>
```

---

## AI / ML Template

**Color Palette**:
- Background gradient: #1e1b4b → #312e81
- Accent: #8b5cf6 (violet), #a78bfa
- Text: #f8fafc

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#1e1b4b"/>
      <stop offset="100%" style="stop-color:#312e81"/>
    </linearGradient>
    <linearGradient id="node-glow" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#8b5cf6"/>
      <stop offset="100%" style="stop-color:#a78bfa"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Neural network nodes (abstract) -->
  <!-- Left column -->
  <circle cx="200" cy="200" r="20" fill="#8b5cf6" opacity="0.6"/>
  <circle cx="200" cy="320" r="25" fill="#8b5cf6" opacity="0.7"/>
  <circle cx="200" cy="440" r="20" fill="#8b5cf6" opacity="0.6"/>

  <!-- Center column -->
  <circle cx="440" cy="260" r="30" fill="#a78bfa" opacity="0.8"/>
  <circle cx="440" cy="380" r="30" fill="#a78bfa" opacity="0.8"/>

  <!-- Right column -->
  <circle cx="840" cy="260" r="30" fill="#a78bfa" opacity="0.8"/>
  <circle cx="840" cy="380" r="30" fill="#a78bfa" opacity="0.8"/>

  <!-- Far right -->
  <circle cx="1080" cy="200" r="20" fill="#8b5cf6" opacity="0.6"/>
  <circle cx="1080" cy="320" r="25" fill="#8b5cf6" opacity="0.7"/>
  <circle cx="1080" cy="440" r="20" fill="#8b5cf6" opacity="0.6"/>

  <!-- Connection lines -->
  <line x1="220" y1="200" x2="410" y2="260" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="220" y1="320" x2="410" y2="260" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="220" y1="320" x2="410" y2="380" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="220" y1="440" x2="410" y2="380" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="470" y1="260" x2="810" y2="260" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="470" y1="380" x2="810" y2="380" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="870" y1="260" x2="1060" y2="200" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="870" y1="260" x2="1060" y2="320" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="870" y1="380" x2="1060" y2="320" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>
  <line x1="870" y1="380" x2="1060" y2="440" stroke="#c4b5fd" stroke-width="1" opacity="0.3"/>

  <!-- Project name -->
  <text x="640" y="330"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="64" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="380"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="22" font-weight="400"
        text-anchor="middle" fill="#c4b5fd">
    AI/ML project tagline
  </text>
</svg>
```

---

## Web / Frontend Template

**Color Palette**:
- Background gradient: #0c4a6e → #075985
- Accent: #3b82f6 (blue), #60a5fa
- Text: #f8fafc

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

  <!-- Browser window mockup (minimal) -->
  <rect x="290" y="100" width="700" height="440" rx="8" fill="#1e293b" stroke="#475569" stroke-width="2"/>
  <rect x="290" y="100" width="700" height="35" rx="8" fill="#334155"/>

  <!-- URL bar -->
  <rect x="310" y="110" width="400" height="18" rx="4" fill="#475569"/>

  <!-- Browser dots -->
  <circle cx="680" cy="118" r="5" fill="#ef4444"/>
  <circle cx="700" cy="118" r="5" fill="#f59e0b"/>
  <circle cx="720" cy="118" r="5" fill="#22c55e"/>

  <!-- Component blocks (representing UI) -->
  <rect x="320" y="160" width="180" height="100" rx="4" fill="#3b82f6" opacity="0.3"/>
  <rect x="520" y="160" width="180" height="100" rx="4" fill="#3b82f6" opacity="0.2"/>
  <rect x="720" y="160" width="240" height="100" rx="4" fill="#3b82f6" opacity="0.25"/>
  <rect x="320" y="280" width="640" height="60" rx="4" fill="#60a5fa" opacity="0.15"/>

  <!-- Project name -->
  <text x="640" y="400"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="56" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="450"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" font-weight="400"
        text-anchor="middle" fill="#93c5fd">
    Web/Frontend project tagline
  </text>

  <!-- Decorative connecting lines -->
  <line x1="100" y1="320" x2="250" y2="320" stroke="#3b82f6" stroke-width="2" opacity="0.4"/>
  <line x1="1030" y1="320" x2="1180" y2="320" stroke="#3b82f6" stroke-width="2" opacity="0.4"/>
</svg>
```

---

## Data / Analytics Template

**Color Palette**:
- Background gradient: #1e3a5f → #0f172a
- Accent: #f59e0b (amber), #3b82f6 (blue)
- Text: #f8fafc

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#1e3a5f"/>
      <stop offset="100%" style="stop-color:#0f172a"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Bar chart (abstract) -->
  <rect x="200" y="400" width="60" height="120" fill="#3b82f6" opacity="0.6"/>
  <rect x="280" y="350" width="60" height="170" fill="#3b82f6" opacity="0.7"/>
  <rect x="360" y="280" width="60" height="240" fill="#f59e0b" opacity="0.8"/>
  <rect x="440" y="320" width="60" height="200" fill="#3b82f6" opacity="0.7"/>
  <rect x="520" y="380" width="60" height="140" fill="#3b82f6" opacity="0.6"/>

  <!-- Line chart (abstract) -->
  <polyline points="700,450 780,380 860,400 940,300 1020,340 1100,280"
            stroke="#f59e0b" stroke-width="3" fill="none" opacity="0.8"/>
  <circle cx="700" cy="450" r="5" fill="#f59e0b"/>
  <circle cx="780" cy="380" r="5" fill="#f59e0b"/>
  <circle cx="860" cy="400" r="5" fill="#f59e0b"/>
  <circle cx="940" cy="300" r="5" fill="#f59e0b"/>
  <circle cx="1020" cy="340" r="5" fill="#f59e0b"/>
  <circle cx="1100" cy="280" r="5" fill="#f59e0b"/>

  <!-- Project name -->
  <text x="640" y="180"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="64" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="230"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="22" font-weight="400"
        text-anchor="middle" fill="#94a3b8">
    Data analytics project tagline
  </text>
</svg>
```

---

## Security Template

**Color Palette**:
- Background gradient: #0f172a → #1e293b
- Accent: #22c55e (green), #eab308 (yellow)
- Text: #f8fafc

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

  <!-- Shield shape (abstract) -->
  <path d="M640 120 L780 180 L780 350 Q780 450 640 520 Q500 450 500 350 L500 180 Z"
        fill="none" stroke="#22c55e" stroke-width="3" opacity="0.6"/>
  <path d="M640 160 L740 205 L740 340 Q740 420 640 475 Q540 420 540 340 L540 205 Z"
        fill="#22c55e" opacity="0.15"/>

  <!-- Checkmark inside shield -->
  <path d="M580 320 L620 360 L700 280"
        stroke="#22c55e" stroke-width="6" stroke-linecap="round" stroke-linejoin="round" fill="none"/>

  <!-- Project name -->
  <text x="640" y="560"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="56" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Decorative lock icons (simplified) -->
  <rect x="180" y="280" width="40" height="30" rx="4" fill="none" stroke="#eab308" stroke-width="2" opacity="0.4"/>
  <path d="M190 280 L190 265 Q200 245 210 265 L210 280" fill="none" stroke="#eab308" stroke-width="2" opacity="0.4"/>

  <rect x="1060" y="280" width="40" height="30" rx="4" fill="none" stroke="#eab308" stroke-width="2" opacity="0.4"/>
  <path d="M1070 280 L1070 265 Q1080 245 1090 265 L1090 280" fill="none" stroke="#eab308" stroke-width="2" opacity="0.4"/>
</svg>
```

---

## Infrastructure / Cloud Template

**Color Palette**:
- Background gradient: #1e293b → #334155
- Accent: #06b6d4 (cyan), #64748b (slate)
- Text: #f8fafc

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#1e293b"/>
      <stop offset="100%" style="stop-color:#334155"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1280" height="640" fill="url(#bg)"/>

  <!-- Cloud shape (simplified) -->
  <ellipse cx="640" cy="200" rx="200" ry="80" fill="#475569" opacity="0.4"/>
  <ellipse cx="520" cy="220" rx="100" ry="50" fill="#475569" opacity="0.4"/>
  <ellipse cx="760" cy="220" rx="100" ry="50" fill="#475569" opacity="0.4"/>

  <!-- Server racks (abstract boxes) -->
  <rect x="280" y="380" width="120" height="160" rx="4" fill="#0f172a" stroke="#06b6d4" stroke-width="2"/>
  <rect x="295" y="400" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.6"/>
  <rect x="295" y="420" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.4"/>
  <rect x="295" y="440" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.3"/>

  <rect x="580" y="380" width="120" height="160" rx="4" fill="#0f172a" stroke="#06b6d4" stroke-width="2"/>
  <rect x="595" y="400" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.6"/>
  <rect x="595" y="420" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.4"/>
  <rect x="595" y="440" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.3"/>

  <rect x="880" y="380" width="120" height="160" rx="4" fill="#0f172a" stroke="#06b6d4" stroke-width="2"/>
  <rect x="895" y="400" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.6"/>
  <rect x="895" y="420" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.4"/>
  <rect x="895" y="440" width="90" height="12" rx="2" fill="#06b6d4" opacity="0.3"/>

  <!-- Connection lines to cloud -->
  <line x1="340" y1="380" x2="540" y2="260" stroke="#06b6d4" stroke-width="1" opacity="0.4"/>
  <line x1="640" y1="380" x2="640" y2="280" stroke="#06b6d4" stroke-width="1" opacity="0.4"/>
  <line x1="940" y1="380" x2="740" y2="260" stroke="#06b6d4" stroke-width="1" opacity="0.4"/>

  <!-- Project name -->
  <text x="640" y="200"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="56" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="580"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="20" font-weight="400"
        text-anchor="middle" fill="#94a3b8">
    Infrastructure project tagline
  </text>
</svg>
```

---

## Claude Code Plugin Template

**Color Palette**:
- Background gradient: #1e1b4b → #312e81 (Anthropic purple)
- Accent: #8b5cf6 (violet), #06b6d4 (cyan)
- Text: #f8fafc

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

  <!-- Plugin badge shape -->
  <rect x="520" y="140" width="240" height="36" rx="18" fill="#8b5cf6" opacity="0.3"/>
  <text x="640" y="165"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="16" font-weight="600"
        text-anchor="middle" fill="#c4b5fd">
    Claude Code Plugin
  </text>

  <!-- Project name -->
  <text x="640" y="280"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="72" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>

  <!-- Tagline -->
  <text x="640" y="340"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="24" font-weight="400"
        text-anchor="middle" fill="#a5b4fc">
    Plugin tagline here
  </text>

  <!-- Feature icons (simplified) -->
  <rect x="320" y="420" width="160" height="80" rx="8" fill="#8b5cf6" opacity="0.2"/>
  <text x="400" y="470"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" font-weight="500"
        text-anchor="middle" fill="#c4b5fd">
    Feature 1
  </text>

  <rect x="560" y="420" width="160" height="80" rx="8" fill="#8b5cf6" opacity="0.2"/>
  <text x="640" y="470"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" font-weight="500"
        text-anchor="middle" fill="#c4b5fd">
    Feature 2
  </text>

  <rect x="800" y="420" width="160" height="80" rx="8" fill="#8b5cf6" opacity="0.2"/>
  <text x="880" y="470"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="14" font-weight="500"
        text-anchor="middle" fill="#c4b5fd">
    Feature 3
  </text>

  <!-- Decorative corner accents -->
  <circle cx="100" cy="100" r="40" fill="#06b6d4" opacity="0.1"/>
  <circle cx="1180" cy="100" r="30" fill="#8b5cf6" opacity="0.1"/>
  <circle cx="100" cy="540" r="30" fill="#8b5cf6" opacity="0.1"/>
  <circle cx="1180" cy="540" r="40" fill="#06b6d4" opacity="0.1"/>
</svg>
```

---

## Dark Mode Variant Guidelines

To create dark mode variants, apply these transformations:

### Light → Dark Conversion

| Element | Light Mode | Dark Mode |
|---------|------------|-----------|
| Background start | #f8fafc | #0f172a |
| Background end | #e2e8f0 | #1e293b |
| Primary text | #0f172a | #f8fafc |
| Secondary text | #475569 | #94a3b8 |
| Accent colors | Keep same | Adjust brightness +10% |
| Opacity | Keep same | May need +0.1 for visibility |

### Example Dark Mode Template

```xml
<!-- Add "-dark" suffix to gradient id -->
<linearGradient id="bg-dark" x1="0%" y1="0%" x2="100%" y2="100%">
  <stop offset="0%" style="stop-color:#0f172a"/>
  <stop offset="100%" style="stop-color:#1e293b"/>
</linearGradient>

<!-- Swap text colors -->
<text fill="#f8fafc">...</text>  <!-- Primary -->
<text fill="#94a3b8">...</text>  <!-- Secondary -->
```

---

## Minimal Style Simplifications

When `svg_style: minimal`, reduce templates to essentials:

1. **Remove** decorative corner elements
2. **Keep** only 3-5 primary shapes
3. **Increase** whitespace (center content more)
4. **Simplify** gradients to 2 colors max
5. **Remove** secondary visual elements

Example minimal version:
```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1280 640">
  <rect width="1280" height="640" fill="#0f172a"/>

  <!-- Single accent shape -->
  <circle cx="640" cy="250" r="80" fill="#06b6d4" opacity="0.2"/>

  <!-- Project name only -->
  <text x="640" y="360"
        font-family="-apple-system, BlinkMacSystemFont, 'Inter', sans-serif"
        font-size="72" font-weight="700"
        text-anchor="middle" fill="#f8fafc">
    PROJECT-NAME
  </text>
</svg>
```
