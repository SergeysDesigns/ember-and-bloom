# Restaurant Website Template

Reusable template for building client restaurant websites. Built with Vite + React, deployed on Cloudflare Pages.

## First-time setup (do this once on your machine)

1. Install Node.js from https://nodejs.org (LTS version)
2. Install Git from https://git-scm.com
3. Open terminal and verify:
   ```
   node --version
   git --version
   ```

## New client workflow

### 1. Copy the template
```
cp -r restaurant-template marias-taqueria
cd marias-taqueria
```
On Windows (Command Prompt):
```
xcopy restaurant-template marias-taqueria /E /I
cd marias-taqueria
```

### 2. Install dependencies
```
npm install
```

### 3. Customize for the client
Edit these files:
- `src/content.js` — ALL restaurant info (name, menu, hours, contact, images)
- `src/styles.css` — Theme colors in the `:root` block
- `index.html` — Page title and meta description
- `public/favicon.svg` — Favicon letter/icon

### 4. Preview locally
```
npm run dev
```
Opens at http://localhost:5173 — auto-refreshes as you edit.

### 5. Push to GitHub
```
git init
git add .
git commit -m "initial build for Maria's Taqueria"
```
Create a new repo on github.com, then:
```
git remote add origin https://YOUR-USERNAME:YOUR-TOKEN@github.com/YOUR-USERNAME/marias-taqueria.git
git push -u origin main
```

### 6. Deploy on Cloudflare Pages
1. Log in to https://dash.cloudflare.com
2. Go to **Workers & Pages** → **Create** → **Connect to Git**
3. Select the repo → Framework preset: **Vite**
4. Build command: `npm run build`
5. Build output directory: `dist`
6. Click **Deploy**

### 7. Add custom domain
In Cloudflare Pages → your project → **Custom domains** → Add domain.
If the domain is registered with Cloudflare, DNS is automatic.
If registered elsewhere, add the CNAME record Cloudflare gives you.

## Updating a client site

```
cd marias-taqueria
# make edits to src/content.js or other files
npm run dev              # preview changes locally
git add .
git commit -m "updated menu prices"
git push
```
Cloudflare auto-deploys in ~30 seconds.

## File structure
```
├── index.html           # Entry HTML (edit title, meta tags)
├── package.json         # Dependencies
├── vite.config.js       # Build config (don't touch)
├── public/
│   └── favicon.svg      # Browser tab icon
└── src/
    ├── main.jsx         # React entry (don't touch)
    ├── styles.css       # Global styles + theme colors
    ├── content.js       # ⭐ ALL client content lives here
    ├── components.jsx   # Reusable UI pieces (don't touch)
    └── App.jsx          # Page layout (don't touch usually)
```

## For each new client you only edit:
1. `src/content.js` — menu, hours, contact, images
2. `src/styles.css` — colors
3. `index.html` — SEO title/description
