# ACFD EMS Protocols — Prototype

A mobile-first web app prototype for fire department EMS protocols. No login. No app store. Installs to home screen. Works offline.

## What's inside

- `index.html` — the entire app (single file, self-contained)
- All logic, styling, and data is in this one file
- Fake placeholder content across 7 categories (Foundations, Policies, Procedures, Cardiac, Trauma, Medications, Pediatric)
- Several protocols are fully fleshed out as examples (Cardiac Arrest, 12-Lead EKG, DNR, Epinephrine, Naloxone, STEMI, Tourniquet, Pediatric Dosing, etc.)

## Try it locally first

1. Open `index.html` in any browser
2. Tap around — search, filter by category, favorite protocols, open detail sheets
3. Nothing to install, no server needed

## Deploy to the web (free, 10 minutes)

### Step 1 — Push to GitHub

1. Create a GitHub account at github.com if you don't have one
2. Click the **+** icon → **New repository**
3. Name it `acfd-protocols` (or whatever you want), make it **Public**, click **Create repository**
4. On the new repo page, click **"uploading an existing file"**
5. Drag `index.html` into the upload area
6. Click **Commit changes**

### Step 2 — Deploy with Netlify

1. Go to netlify.com and sign in with your GitHub account
2. Click **Add new site** → **Import an existing project**
3. Choose **GitHub** → pick the `acfd-protocols` repo
4. Leave all settings default → click **Deploy**
5. Wait ~30 seconds. Netlify gives you a URL like `cheerful-kitten-abc123.netlify.app`
6. (Optional) Click **Site settings** → **Change site name** to something like `acfd-protocols.netlify.app`

### Step 3 — Install on your phone

**iPhone:**
1. Open the URL in Safari
2. Tap Share button → Add to Home Screen → Add

**Android:**
1. Open the URL in Chrome
2. Tap three-dot menu → Install app (or Add to Home screen)

Done. It now behaves like a native app. Works offline after the first open.

## How to edit content

### Easiest — edit on GitHub in the browser

1. Go to your repo on github.com
2. Click `index.html`
3. Click the pencil (edit) icon
4. Find the `CONTENT = {` section in the JavaScript — each protocol is a key
5. Edit the text, commit changes
6. Netlify auto-deploys within ~60 seconds
7. Next time the app opens, it has the new version

### To add a new protocol

1. Add the title to the appropriate `DATA` category's `items` array
2. Add the content block under `CONTENT = {` with the same title as the key
3. Commit — done

### HTML content tags you can use inside a protocol

- `<h3>Section Title</h3>` — red underlined section header
- `<p>Text here</p>` — paragraph
- `<ul><li>Item</li></ul>` — bulleted list
- `<ol><li>Step</li></ol>` — numbered list
- `<strong>bold</strong>` — bold text
- `<table><tr><th>Header</th></tr><tr><td>Cell</td></tr></table>` — table
- `<div class="callout">Note</div>` — yellow callout box
- `<div class="callout callout-danger">Warning</div>` — red warning callout
- `<div class="callout callout-info">Info</div>` — blue info callout
- `<div class="callout callout-success">Success</div>` — green callout
- Dose box: `<div class="dose-box"><div class="dose-label">Label</div><div class="dose-value">1 mg IV</div></div>`

## Features

- **Search** — types match across all protocols, highlights results
- **Category filters** — chips across the top
- **Favorites** — tap ★ on any protocol, it saves to your phone
- **Offline** — service worker caches everything after first load
- **Install-to-home-screen** — platform-aware tutorial on first visit
- **Online/offline indicator** — green/amber dot in header
- **No accounts, no servers, no fees**

## Costs

- GitHub: free
- Netlify: free (stays free unless you get huge traffic)
- Custom domain (optional): ~$12/year from Namecheap/Cloudflare

## Next steps when you're ready

1. Get chief / medical director blessing before distributing
2. Replace fake content with real protocols
3. Add department logo (replace the ACFD badge)
4. Print QR codes for stations linking to the URL
5. Do a 2-minute rollout demo at shift change
