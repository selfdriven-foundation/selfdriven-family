# selfdriven.family site — build notes (v2, 29 Oct 2026)

Artifact: https://claude.ai/artifact/MYY1KKsPn1Xr86ykoCCYjM (version 2 = selfdriven.you style; version 1 = Foundation style)
Source: built from papers/selfdriven-family-foundational-unit-v1.0.md (paper v1.0, 29 October 2026).

## Structure
Single self-contained HTML page with two hash-routed views:
- Overview (default): hero with the concentric Person → Family/care circle → Community networks → Institutions and commons diagram, plus mode pills that jump to #mode-curious / #mode-caring / #mode-constructive / #mode-chill; status note (conceptual, not validated); §2 definition + layered language + ABS 2021 census bar + AIFS figures; §3 five functions; §4 rights band (UDHR Art. 16, CRC Art. 12/19, six affirmations); §5 shift table; §6 four modes as large cards (essence line + "Try this as a family" task); §7 coordination cycle diagram (Observe, Listen, Compose, Conduct, Learn, Renew or stop); §8 abundant intelligence; §9 six capabilities (marked as design proposal); §10 ten principles; §11 five flawed assumptions; §12–13 policy and communities; §14 pilot phases A–D, indicators, H1–H5 (H5 failure criterion); §15 charter with copy button and mode tags on the four mode-aligned lines; §16 conclusion; references and scope.
- Paper (#paper, #paper-s1 … #paper-s16, #paper-references): full paper rendered from Markdown via pandoc, sticky contents.
Each overview eyebrow carries a §N link into the matching paper section.

## Brand decisions (current: selfdriven.you dark 4Cs)
- Mark asked for the selfdriven.you style. Tokens: bg #09090f, surface #111118 / #18181f, text #f0eeff, muted #7e7a9a; modes curious #f5c842, caring #ff5f7e, constructive #00e5a0, chill #7b6cff (text #9b8fff).
- Fonts: Bricolage Grotesque 800 headings, DM Sans body, JetBrains Mono labels. No Poppins, no flamingo.
- Caring rose is the family accent (CTAs, § chips, highlights); the four mode colours carry the modes, the hero glow blobs, the census bar and the charter tags.
- Signature components: four animated glow blobs, hero pill with pulsing constructive dot, mode pills with tilt hover, custom dot/ring cursor (off on touch), scroll reveal.
- Dark-only by design (no light mode).
- Reveal uses CSS scroll timelines and is transform-only, so content is never hidden at rest.
- Logo: placeholder four-colour ring mark; swap in the real selfdriven.you logo (base64 from selfdriven.you index.html) when available.

## Build
template-you.html (current) / template.html (v1 Foundation style) + build.py (pandoc gfm → HTML fragment, ids renamed to paper-sN, tables wrapped, external links target=_blank).
