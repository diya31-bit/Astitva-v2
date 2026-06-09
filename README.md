# Astitva — Personal Safety App

A Progressive Web App (PWA) for personal safety guidance, self-defence techniques, and helping others in dangerous situations.

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | Main app (all HTML, CSS, JS in one file) |
| `manifest.json` | PWA manifest — name, icons, theme |
| `sw.js` | Service worker — offline support |
| `icons/` | Place your app icons here (see below) |

---

## Icons needed

Create two PNG icons and place in the `icons/` folder:
- `icons/icon-192.png` — 192×192 px
- `icons/icon-512.png` — 512×512 px

Use a red shield on dark background to match the app. Free tools: Canva, Figma, or favicon.io.

---

## Deployment options (easiest first)

### Option 1 — Netlify (free, fastest)
1. Go to https://netlify.com and sign up free
2. Drag and drop your `astitva/` folder onto the Netlify dashboard
3. Netlify gives you a live URL instantly (e.g. `astitva.netlify.app`)
4. Users can open it in their phone browser and tap "Add to Home Screen"

### Option 2 — GitHub Pages (free)
1. Create a free GitHub account at https://github.com
2. Create a new repository called `astitva`
3. Upload all files from the `astitva/` folder
4. Go to Settings → Pages → Source: main branch → Save
5. Your app is live at `https://yourusername.github.io/astitva`

### Option 3 — Vercel (free)
1. Go to https://vercel.com, connect your GitHub
2. Import the `astitva` repo and deploy — done in 30 seconds

---

## Making it installable on phones

Once deployed, users can install it like a native app:

**Android (Chrome):**
1. Open the URL in Chrome
2. Tap the three-dot menu → "Add to Home Screen"
3. The app appears on the home screen with the Astitva icon

**iPhone (Safari):**
1. Open the URL in Safari
2. Tap the Share button (box with arrow)
3. Scroll down and tap "Add to Home Screen"
4. The app appears with the Astitva icon

---

## AI feature

The "Ask Astitva" tab uses the Claude API. To enable this in production:
- The API key is handled by the claude.ai environment in preview
- For your own deployment, you'll need a backend proxy to protect your Anthropic API key
- Recommended: a simple Netlify Function or Vercel serverless function as a proxy

---

## Customisation

- **Language:** Add a Hindi/regional language toggle in `index.html`
- **Helplines:** Update numbers in the "Ask Astitva" tab for your region
- **Colours:** Change `--red: #c0392b` in the CSS to update the theme
- **Offline content:** All guidance is already baked in and works offline

---

## Tech stack
- Vanilla HTML, CSS, JavaScript — no frameworks, no build step
- Google Fonts (Mukta + Playfair Display)
- Claude API (Anthropic) for AI guidance
- Service Worker for offline support
