# Writing Image Prompts for Presentation Decks

Generate images using your native image generation capabilities or external image tools. Keep visual consistency across the entire deck using a shared style anchor.

---

## 1. Budget & Efficiency
- **Minimal Asset List:** Plan only essential hero images. Reuse images across slides where appropriate (e.g., cover hero re-used as the thank-you closing background).
- **Hero First:** Generate the cover and main space overviews first, then proceed to materials and product features.
- **User Assets:** When real project photos, floor plans, or manufacturer images are provided by the user, integrate them directly into the slide layout.

---

## 2. Shared Style Anchor
Formulate **one style sentence** for the entire deck and append it word-for-word to every image prompt to ensure visual consistency:

> *Soft natural afternoon daylight, warm cream plaster walls, light oak wood and natural linen, muted earthy palette, photorealistic architectural photography, calm and minimal, clean composition, no text, no logos.*

---

## 3. Prompt Formula

Each prompt follows the standard 5-part structure:
`[Subject] · [Setting, materials, colours] · [Lighting] · [Camera framing & aspect ratio] · [Style anchor]`

### Examples by Slide Type:

1. **Interior Hero (16:9 or 4:5):**
   > *Living room of a serene residence overlooking a minimalist garden, curved cream boucle sofa, organic travertine coffee table on a natural jute rug, soft afternoon sunlight filtering through wooden blinds, wide eye-level perspective, 16:9 aspect ratio. Soft natural afternoon daylight, warm cream plaster walls, light oak wood and natural linen, muted earthy palette, photorealistic architectural photography, calm and minimal, clean composition, no text, no logos.*

2. **Product / Furniture Studio Shot (4:3 or 5:4):**
   > *Studio product photograph of a low light oak shoe bench with upholstered grey-beige cushion and woven rattan drawer face, three-quarter angle view, seamless warm beige backdrop, gentle soft diffuse lighting, centred with generous negative space, 4:3 aspect ratio. Soft natural afternoon daylight, warm cream tones, clean and minimal, photorealistic, no text, no logos.*

3. **Material Swatch (1:1 Square / Circle):**
   > *Macro architectural close-up of natural light oak wood grain texture, satin matte finish, shallow depth of field, even diffused lighting, filling the entire square frame, 1:1 aspect ratio. Warm natural tones, photorealistic texture, no text, no logos.*

4. **Tall Vertical Strip (9:16):**
   > *Vertical architectural vignette of a sunlit dining nook with round oak table and woven chairs, warm sunlight cast on wall, slightly low perspective, 9:16 vertical aspect ratio. Soft natural daylight, warm cream and light oak tones, clean and minimal, photorealistic, no text, no logos.*

---

## 4. Prompting Rules
- **No Text in Prompts:** Never ask the image generation model to render prices, numbers, product names, or logos inside the image. Provide all typography in the HTML layout.
- **Concrete Descriptions:** Specify exact materials (travertine, boucle, light oak, linen) and colours rather than vague adjectives.
- **Consistent Lighting:** Keep the time of day and lighting mood identical across all prompts in the same deck.
