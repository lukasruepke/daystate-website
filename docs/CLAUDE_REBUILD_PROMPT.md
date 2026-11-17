# DAYSTATE-Website in Claude nachbauen

**Kurz auf Deutsch:** Kopiere alles ab "PROMPT" in Claude und hänge diese Dateien an: `content.md` (alle Texte), `mirror/.../style.css`, `mirror/.../app.js` und die Screenshots `screenshot_desktop_es.png` und `screenshot_mobile_es.png`. Die Bilder liegen im Ordner `mirror/daystate-your-moment.ivybears-8790.chatgpt.site/assets/`. Lade sie hoch oder kopiere sie 1:1 ins Projekt. Die Originalseite ist auf Spanisch (es-CO) und hat eine englische Version unter /en/.

---
## PROMPT

You are rebuilding the website "DAYSTATE · Rituales en gotas | Colombia" 1:1 as a static multi-page site (HTML + one CSS + one small vanilla JS file; no framework needed). It has Spanish (es-CO) as the default at / and English at /en/, with hreflang alternates.

**Rules**
- Use the copy from the attached content.md VERBATIM. Do not rewrite, translate, or shorten it. Keep the page order, section order, headings levels, button labels (including the "↗" arrows), and image alt texts exactly.
- Match the attached screenshots visually (desktop 1440px, mobile 390px).
- If style.css/app.js are attached, use them as the ground truth for layout, spacing, and behaviour (announcement bar with close ×, sticky header, "Rituales ⌄" dropdown, ES/EN switch, mobile menu, ritual finder, waitlist form #lista-de-espera, cookie banner, FAQ accordions).

**Design tokens**
- Colors: cream #F1EEEC (page background/theme-color), white #FBF9F5, stone #CFC8C4, ink #2B2630 (text, dark sections), gold #C9A465 (accent), line rgba(43,38,48,.2) (hairlines).
- Spacing: --space: clamp(24px,5vw,80px).
- Typography: Jost (sans; body, nav, labels, uppercase eyebrows like "01 / A TU RITMO") + Cormorant Italic (serif italic display accents). Self-host as /assets/fonts/jost-latin.woff2 and /assets/fonts/cormorant-italic-latin.woff2.
- Style: minimal premium wellness look. Lots of whitespace, thin 1px lines, numbered section eyebrows, large headlines, and product cards that swap from a packshot to an infographic on hover.
- Logos: /assets/brand/daystate_logo_ink.svg (on light backgrounds), daystate_logo_cream.svg (on dark backgrounds). Favicon: /favicon.svg.

**Pages to build**
- /aviso-legal.html
- /bundles.html
- /bundles?ritual=beauty.html
- /bundles?ritual=complete.html
- /bundles?ritual=day-night.html
- /contacto.html
- /en/aviso-legal.html
- /en/bundles.html
- /en/bundles?ritual=beauty.html
- /en/bundles?ritual=complete.html
- /en/bundles?ritual=day-night.html
- /en/contacto.html
- /en/encuentra-tu-ritual.html
- /en/index.html
- /en/ingredientes.html
- /en/legal/cambios-devoluciones-y-retracto.html
- /en/legal/cookies.html
- /en/legal/envios.html
- /en/legal/politica-de-tratamiento-de-datos.html
- /en/legal/terminos-y-condiciones.html
- /en/nuestra-historia.html
- /en/preguntas-frecuentes.html
- /en/productos/bloom.html
- /en/productos/hair-skin-glow.html
- /en/productos/morning-complex.html
- /en/productos/night-complex.html
- /en/proximamente.html
- /en/proximamente?producto=FOCUS+.html
- /en/proximamente?producto=HAIR & SKIN GLOW+.html
- /en/proximamente?producto=MORNING COMPLEX+.html
- /en/proximamente?producto=MOVE.html
- /en/proximamente?producto=NIGHT COMPLEX+.html
- /en/rituales/beauty.html
- /en/rituales/manana.html
- /en/rituales/noche.html
- /en/suscripcion.html
- /en/tienda.html
- /encuentra-tu-ritual.html
- /index.html
- /ingredientes.html
- /legal/cambios-devoluciones-y-retracto.html
- /legal/cookies.html
- /legal/envios.html
- /legal/politica-de-tratamiento-de-datos.html
- /legal/terminos-y-condiciones.html
- /nuestra-historia.html
- /preguntas-frecuentes.html
- /productos/bloom.html
- /productos/hair-skin-glow.html
- /productos/morning-complex.html
- /productos/night-complex.html
- /proximamente.html
- /proximamente?producto=FOCUS+.html
- /proximamente?producto=HAIR & SKIN GLOW+.html
- /proximamente?producto=MORNING COMPLEX+.html
- /proximamente?producto=MOVE.html
- /proximamente?producto=NIGHT COMPLEX+.html
- /rituales/beauty.html
- /rituales/manana.html
- /rituales/noche.html
- /suscripcion.html
- /tienda.html

**Images (keep these paths; responsive variants use the --768/--1280 suffixes in srcset)**
- /assets/Infografiken/IG_W1-1_MORNING_COMPLEX_TU_MANANA--1280.webp
- /assets/Infografiken/IG_W1-1_MORNING_COMPLEX_TU_MANANA--480.webp
- /assets/Infografiken/IG_W1-1_MORNING_COMPLEX_TU_MANANA--768.webp
- /assets/Infografiken/IG_W1-3_NIGHT_COMPLEX_TU_NOCHE--1280.webp
- /assets/Infografiken/IG_W1-3_NIGHT_COMPLEX_TU_NOCHE--480.webp
- /assets/Infografiken/IG_W1-3_NIGHT_COMPLEX_TU_NOCHE--768.webp
- /assets/Infografiken/IG_W1-4_HAIR_SKIN_GLOW_TU_GLOW--1280.webp
- /assets/Infografiken/IG_W1-4_HAIR_SKIN_GLOW_TU_GLOW--480.webp
- /assets/Infografiken/IG_W1-4_HAIR_SKIN_GLOW_TU_GLOW--768.webp
- /assets/Infografiken/IG_W1-5_BLOOM_TU_RITUAL--1280.webp
- /assets/Infografiken/IG_W1-5_BLOOM_TU_RITUAL--480.webp
- /assets/Infografiken/IG_W1-5_BLOOM_TU_RITUAL--768.webp
- /assets/Lifestyle/Lifestyle_1_Bad_Morgen_MORNING_HAIR-SKIN--1280.webp
- /assets/Lifestyle/Lifestyle_1_Bad_Morgen_MORNING_HAIR-SKIN--480.webp
- /assets/Lifestyle/Lifestyle_1_Bad_Morgen_MORNING_HAIR-SKIN--768.webp
- /assets/Lifestyle/Lifestyle_2_Nachttisch_NIGHT--1280.webp
- /assets/Lifestyle/Lifestyle_2_Nachttisch_NIGHT--480.webp
- /assets/Lifestyle/Lifestyle_2_Nachttisch_NIGHT--768.webp
- /assets/Lifestyle/Lifestyle_3_Kueche_Limette_MORNING--1280.webp
- /assets/Lifestyle/Lifestyle_3_Kueche_Limette_MORNING--480.webp
- /assets/Lifestyle/Lifestyle_3_Kueche_Limette_MORNING--768.webp
- /assets/Packshots/W1-1_MORNING_COMPLEX_packshot--1280.webp
- /assets/Packshots/W1-1_MORNING_COMPLEX_packshot--480.webp
- /assets/Packshots/W1-1_MORNING_COMPLEX_packshot--768.webp
- /assets/Packshots/W1-1_MORNING_COMPLEX_packshot.jpg
- /assets/Packshots/W1-3_NIGHT_COMPLEX_packshot--1280.webp
- /assets/Packshots/W1-3_NIGHT_COMPLEX_packshot--480.webp
- /assets/Packshots/W1-3_NIGHT_COMPLEX_packshot--768.webp
- /assets/Packshots/W1-3_NIGHT_COMPLEX_packshot.jpg
- /assets/Packshots/W1-4_HAIR_SKIN_GLOW_packshot--1280.webp
- /assets/Packshots/W1-4_HAIR_SKIN_GLOW_packshot--480.webp
- /assets/Packshots/W1-4_HAIR_SKIN_GLOW_packshot--768.webp
- /assets/Packshots/W1-4_HAIR_SKIN_GLOW_packshot.jpg
- /assets/Packshots/W1-5_BLOOM_packshot--1280.webp
- /assets/Packshots/W1-5_BLOOM_packshot--480.webp
- /assets/Packshots/W1-5_BLOOM_packshot--768.webp
- /assets/Packshots/W1-5_BLOOM_packshot.jpg
- /assets/Packshots/W1_Lineup_public--1280.webp
- /assets/Packshots/W1_Lineup_public--480.webp
- /assets/Packshots/W1_Lineup_public--768.webp
- /assets/brand/daystate_logo_cream.svg
- /assets/brand/daystate_logo_ink.svg
- /assets/fonts/cormorant-italic-latin.woff2
- /assets/fonts/jost-latin.woff2

**SEO/meta:** For each page, use the title and description listed in content.md. Use og:image /assets/Packshots/W1_Lineup_public--1280.webp, twitter:card summary_large_image, and theme-color #F1EEEC.

Deliver the complete file tree with the full code for every file.
