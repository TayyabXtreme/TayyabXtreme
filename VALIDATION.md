# Verification — 10 October 2026

Both portrait PNGs match the original downloaded archive byte for byte, including alpha. They are RGBA PNGs measuring 1254 × 1254 and 1448 × 1086.

- All five SVGs parsed successfully as XML.
- Both embedded fonts loaded in Chromium; their bytes match the included WOFF2 files.
- All five SVGs were captured at 0, 2, 5, 9 and 13 seconds, with animation declarations removed, with reduced motion, and as HTML img elements. Evidence is in render_checks/.
- Roles cycle individually at 0/2, 5, 9 and 13 seconds. Interests cycle individually every four seconds.
- Static and reduced-motion fallbacks retain readable content.
- Typography, spacing, transparency and clipping were inspected.
- All five images loaded; no external asset requests or page errors were observed.
- Desktop and 390px mobile previews were captured. Mobile document and scroll widths both measured 390px.
- All five project links were confirmed as public repositories through GitHub's API.
- GitHub and portfolio returned HTTP 200. LinkedIn returned its automation-block response (999); its exact user-supplied URL is preserved, but public page availability could not be independently confirmed.
- No unknown metric counts or contribution-city section.
- CSS-only motion, no scripts or foreignObject. IDs are namespaced; fonts and PNGs are inline.

Repairs include brand vectors and sources, role/carousel timing, segment progress, separate ID drop/sway motion, clipping the foil sweep to the card, font defaults, and text encoding.

The final ZIP was reopened with CRC checks, extracted to a fresh directory, and every extracted file compared to its packaged SHA-256 hash. All required filenames were checked. See CHECKSUMS.sha256 and UPLOAD.md.

Local browser checks cannot guarantee identical animation playback in every GitHub renderer.
