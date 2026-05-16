# Cut Tracker PWA

A workout and calorie deficit tracker. Installs to your phone home screen like a real app.

## Easiest deployment: Vercel (free, ~5 minutes)

### Option A: Deploy from GitHub (recommended for updates later)

1. Create a free GitHub account at github.com if you don't have one
2. Create a new repo called `cut-tracker`
3. Upload all these files to that repo (drag and drop works on github.com)
4. Go to https://vercel.com and sign up with GitHub (free)
5. Click "Add New Project" → import your `cut-tracker` repo
6. Vercel auto-detects Vite. Click "Deploy"
7. Wait ~1 minute. You get a URL like `cut-tracker-xyz.vercel.app`

### Option B: Drag-and-drop deploy (fastest, no GitHub)

1. On your computer, open terminal in this folder
2. Run: `npm install` then `npm run build`
3. Go to https://app.netlify.com/drop
4. Drag the `dist` folder onto the page
5. Get instant URL

## Install on your phone

Once deployed, open the URL on your phone:

**iPhone (Safari):**
- Tap the Share button (square with up arrow)
- Scroll down → "Add to Home Screen"
- Tap Add

**Android (Chrome):**
- Tap the three-dot menu
- Tap "Install app" or "Add to Home Screen"

The icon appears on your home screen. Opens fullscreen, no browser bar, works offline after the first load.

## Local development (optional)

```bash
npm install
npm run dev
```

Open http://localhost:5173

## Your data

Stored in your browser's localStorage. It survives app updates and phone restarts, but lives only on that one device. Use the "Export Data" button in Settings to back up to a JSON file.

If you clear browser data or switch phones without exporting first, your history is gone. Export occasionally.

## File structure

```
cut-tracker-pwa/
├── package.json
├── vite.config.js          ← PWA config
├── index.html
├── public/
│   ├── favicon.svg
│   ├── icon-192.png        ← Home screen icon
│   └── icon-512.png
└── src/
    ├── main.jsx
    └── App.jsx             ← All app logic
```
