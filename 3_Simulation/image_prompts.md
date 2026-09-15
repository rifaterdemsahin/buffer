# 🎨 UI & Asset Image Prompts

> **Stage 3: Simulation** — Documenting text prompts used to generate visual mockups and image assets.

---

## 🖼️ Active Prompts

### 1. Homepage UI Mockup (`mockup_index.png`)
- **Asset Name:** `mockup_index.png`
- **Target Platform / Screen:** Desktop web homepage (1920x1080)
- **AI Generator:** Midjourney v6 / DALL-E 3
- **Prompt:**
  ```text
  A clean, modern SaaS dashboard homepage UI. Sleek dark mode, neon teal and purple accent colors. Glassmorphism panels, interactive charts and analytics widgets. Ultra high-resolution, vector style, user interface design, no device frame --ar 16:9
  ```
- **Generated Date:** YYYY-MM-DD
- **Linked Asset:** [mockup_index.png](file:///Users/rifaterdemsahin/projects/delivery-pilot-template/3_Simulation/mockup_index.png)

---

### 2. Navigation Menu Mockup (`mockup_navigation.png`)
- **Asset Name:** `mockup_navigation.png`
- **Target Platform / Screen:** Mobile screen viewport (375x812)
- **AI Generator:** Midjourney v6 / DALL-E 3
- **Prompt:**
  ```text
  Mobile app interface showing a slide-out navigation drawer/menu. Clean typography, minimalist design, dark mode HSL tailwind colors. Flat icons, sleek UI, no phone frame --ar 9:16
  ```
- **Generated Date:** YYYY-MM-DD
- **Linked Asset:** [mockup_navigation.png](file:///Users/rifaterdemsahin/projects/delivery-pilot-template/3_Simulation/mockup_navigation.png)

---

### 3. LinkedIn Campaign Thumbnails — 2026-09-15 batch
- **Asset Names:** `3_Simulation/linkedin_campaign_2026-09-15/*.png` (12 files)
- **Target Platform / Screen:** LinkedIn post image (16:9)
- **Source:** Generated externally (outside this session) and supplied by the user from `~/Downloads`; not generated via an in-session prompt, so no prompt text to log — recorded here for asset traceability instead.
- **Pairing:** Each filename embeds `_<source-video-id>` mapping it to the source YouTube video (see `4_Formula/specs.md` SPEC-015). 3 tone variants per video: `A-safe-evolution`, `B-curiosity-tension`, `C-bold-contrarian`.
  - `3bwaZ-xUJcs` — "Master AI Before the Skills Gap Masters You"
  - `2EVPwgi8NZA` — "10 AI Tips to Learn Faster and Execute Like a Pro"
  - `WK66w51UMrs` — "Turn AI Into Your Personal Accountability Partner"
  - `3VgRz5GeYDA` — "One AI Habit Broke My Groundhog Day Loop"
- **Generated Date:** 2026-09-15
- **Linked Page:** [linkedin_scheduler.html](../5_Symbols/linkedin_scheduler.html)

---

## 📌 Guidelines for Image Generation
1. **No Device Frames:** Always request mockups *without* laptop, phone, or tablet frames (unless explicitly required) so the raw UI can be rendered directly.
2. **Aspect Ratios:** Match target displays:
   - `--ar 16:9` for desktop displays.
   - `--ar 9:16` for mobile mockups.
3. **Consistency:** Use consistent keyword modifiers (e.g., `modern UI`, `dark mode`, `glassmorphism`, specific accent hex colors) across prompts to maintain unified aesthetics.
