# TopLive — Streaming Landing (v2)

Static marketing landing page. No build step, no backend, no dependencies.

## Run locally
Just serve the folder with any static server, e.g.:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Or open `index.html` directly in a browser (video autoplay may need a server).

## Structure
- `index.html` — entire page (markup + inline CSS + inline JS). Single file.
- `translations.js` — i18n dictionary, 22 languages. **Currently disabled** (the `<script>` include is commented out in `index.html`, and the language switcher is `display:none`). Re-enable by uncommenting both.
- `videos/` — hero carousel clips (video-1…5.mp4, Pexels stock).
- `*.jpg / *.png` — section imagery (Unsplash/Pexels stock + iOS app screens).
- `logo-mark.png` — TopLive icon used in nav/footer.

## Notes for investigation
- All text is in `index.html`. Strings carry `data-i18n="key"` attributes for the i18n engine (inactive while translations are disabled — English in the markup renders as-is).
- Animations are vanilla CSS/JS: starfield (CSS box-shadow + rotation), hero video carousel (slot rotation), Why/Pro-Tips spotlights (auto-rotate + progress), Final CTA marquee, scroll-reveal via IntersectionObserver.
- Tokens: primary `#6445ED`, LIVE pill `#34C759`, base `#0A0A12`. Fonts: Wix Madefor Display + Inter Tight (Google Fonts).
- Stock photos are placeholders pending licensed/branded assets before any public launch.
