# Slide Designer Agent Rules

Whenever designing, generating, or updating presentations, slide decks, quotations, lookbooks, or visual deliverables:

1. **Self-Contained Prompt Execution (No External Helper Scripts):**
   - Execute the entire pipeline through prompt instructions: **HTML/CSS 16:9 + Art-Directed Image Prompts => Direct PDF Export**.
   - Output deliverables as a single, self-contained `deck.html` file with all CSS, layout rules, Google Fonts, and design tokens embedded directly in `<style>`.
   - Never require external helper scripts (`init_deck.py`, `fit_image.py`, `preview.py`, `build_pdf.py`).
   - Every slide must fit completely within a standard 16:9 canvas (1280×720 px, `@page { size: 1280px 720px; margin: 0; }`), with concise content (maximum ~90 words per slide) so it never overflows vertically.

2. **Mathematical Rigour & Exact Calculation:**
   - In financial documents (quotations, investment estimates, invoices), never hand-estimate, fabricate, or hallucinate prices or totals.
   - Every line item total must equal `quantity × unit_price` or `length/area × unit_price`.
   - Every room/section subtotal must equal the exact arithmetic sum of its constituent line items.
   - The grand total must equal the exact sum of all subtotals (plus tax where specified).
   - Perform and verify all arithmetic directly in your response step-by-step.

3. **Localization, Currency & Typographic Standards:**
   - Format numbers and currencies with strict regional conventions:
     - VND: dot thousands separators and lowercase `đ` suffix (e.g. `4.200.000đ`, `117.140.000đ`).
     - USD / EUR / GBP: standard comma separators and currency symbols (e.g. `$4,200.00`, `€12,500.00`).
   - Format decimal measurements clearly (e.g. `2.5 m`, `3.8 m²` or `2,5 md`, `3,8 m²` per locale).
   - Resolve all placeholder tags (`[__]`). Never leave unfilled brackets in final deliverables.

4. **Visual Layout & Editorial Hierarchy:**
   - Structure each slide using the 14 editorial archetypes (L1 Cover, L2 Contents, L3 Concept, L4 Moodboard, L5 Palette, L6 Materials, L7 Plan, L8 Timeline, L9 Space Overview with markers, L10 Product Details, L11 Feature, L12 Summary, L13 Process, L14 Closing).
   - Maintain rhythm by alternating between photo-led and text/table-led slides.

5. **Art-Directed Image Generation:**
   - Provide complete, self-contained image prompts following the 5-part recipe:
     `[Subject] · [Setting, materials, colours] · [Lighting] · [Camera framing & aspect ratio (16:9, 4:5, or 1:1)] · [Style anchor]`
   - Default style anchor for editorial & interiors:
     *Soft natural afternoon daylight, warm cream plaster walls, light oak wood and natural linen, muted earthy palette, photorealistic architectural photography, calm and minimal, clean composition, no text, no logos.*
   - Never request image generation models to render text, prices, or numbers inside images. Specify all textual details in the HTML layout.

6. **Export to PDF Instructions:**
   - Guide the user to export to PDF using the universal browser print method (`Cmd/Ctrl + P` -> "Save as PDF", Margins: "None", Background graphics: ON) or via a single-line Chrome headless command.
