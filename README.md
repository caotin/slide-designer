# Slide Designer Plugin

**Slide Designer** is a professional presentation and editorial design toolkit for creating magazine-grade 16:9 slide decks, interior design quotations, client proposals, pitch decks, and visual lookbooks using self-contained HTML/CSS and direct vector PDF export.

---

## Key Features

1. **Self-Contained Single-File Architecture:**
   - 100% self-contained output: Generates a single `deck.html` with all CSS tokens, Google Fonts, and responsive 16:9 layouts embedded in `<style>`.
   - Zero external scripts required (no Python or Node.js helpers needed).
   - Strict 16:9 canvas (1280×720 px, `@page { size: 1280px 720px; margin: 0; }`) with concise copy (under 90 words per slide) to eliminate vertical overflow.

2. **Mathematical Rigour & Financial Integrity:**
   - Strict arithmetic verification: line item totals (`quantity × unit_price` or `area × unit_price`), space subtotals, grand totals, and tax.
   - All arithmetic is computed and verified step-by-step with zero price hallucination.

3. **14 Editorial Layout Archetypes (L1 – L14):**
   - Covers, Agendas, Concept narratives, Moodboards, 60/30/10 Color palettes, Material swatches with hardware standards, Floor plans, Space overviews with interactive visual markers, Product cards, Investment summaries, Execution roadmaps, and Thank You closing slides.

4. **Art-Directed AI Image Prompts:**
   - Standard 5-part prompt recipe with a consistent style anchor across the entire presentation.
   - Clean separation of visual photography and typographic data (no AI-generated text or prices inside images).

5. **Direct Vector PDF Export:**
   - One-click export via headless Chrome or standard browser print (`Cmd + P` / `Ctrl + P`).

---

## Directory Structure

```text
slide-designer/
├── plugin.json                 # Plugin manifest declaring name, prompts, and logo
├── README.md                   # Plugin documentation
├── LICENSE                     # MIT License
├── assets/
│   └── logo.svg                # Vector icon for Antigravity plugin UI
├── rules/
│   └── AGENTS.md               # Always-on design and mathematical verification rules
└── skills/
    └── slide-designer/
        ├── SKILL.md            # Core workflow, CSS tokens, and layout guidelines
        └── references/
            ├── layouts.md      # Detailed reference catalogue for L1-L14 layouts
            ├── image-prompts.md # Image prompt recipe and style anchors
            └── verification-checklist.md # 5-point quality checklist
```

---

## Getting Started

### Using the Slash Command
Trigger the skill in your chat prompt:
```text
/slide-designer create a 16:9 interior design quotation for a 2-bedroom Japandi apartment
```

### Exporting to PDF

#### Method A: Universal Browser Print
1. Open the generated `deck.html` in Chrome, Arc, or Edge.
2. Press `Cmd + P` (macOS) or `Ctrl + P` (Windows).
3. Set **Destination** to "Save as PDF".
4. Set **Margins** to "None".
5. Enable **"Background graphics"**.
6. Save your presentation.

#### Method B: Headless Chrome Command
```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new --disable-gpu --print-to-pdf=presentation.pdf deck.html
```

---

## License

MIT License. See [LICENSE](LICENSE) for details.
