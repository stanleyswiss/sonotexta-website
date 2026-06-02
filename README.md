# sonotexta-website

Static marketing site for **sonotexta.com** — a macOS voice-to-text dictation app.

**Hosting:** Hetzner box via Coolify (`178.105.213.87`). Traefik serves it and provisions TLS automatically.

**Auto-deploy:** every push to `main` triggers a Coolify rebuild. No manual upload step.

**Where things live:**
- `index.html`, `privacy.html`, `terms.html` — pages
- `icon.png`, `icon-small.png` — app icon
- `SonotextaDemo.mp4`, `VoiceFlowDemo.mp4` — demo videos
- `voiceflow/` — legacy paths preserved for backwards-compat with the old VoiceFlow brand name

**What's NOT here:** the macOS app DMGs and the Sparkle `appcast.xml`. Those live in [`voiceflow-updates`](https://github.com/stanleyswiss/voiceflow-updates) and are served from GitHub Pages at `https://stanleyswiss.github.io/voiceflow-updates/`. The download button on this site and the in-app Sparkle updater both point there directly.

**Promo counter:** the "X of 50 left" banner pulls from `https://voiceflow-proxy.voiceflowai.workers.dev/api/promo-counter` (Cloudflare Worker, separate).
