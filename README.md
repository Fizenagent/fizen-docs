# Fizen Docs — Mintlify

Documentation site for Fizen, powered by Mintlify.

## Live site
→ docs.fizen.io (after setup)

## Project structure

```
fizen-docs/
├── mint.json                          ← Main config (colors, nav, logo)
├── welcome.mdx                        ← Homepage
├── events.mdx
├── general/
│   ├── story.mdx
│   ├── products.mdx
│   ├── practical-applications.mdx
│   └── achievements.mdx
├── cooperation/
│   ├── integration.mdx
│   └── business-collaboration.mdx
├── help-center/
│   ├── fizen-app.mdx
│   ├── fizen-pay.mdx
│   └── fizen-card/
│       ├── overview.mdx
│       ├── apply.mdx
│       ├── top-up.mdx
│       ├── spending.mdx
│       └── fees.mdx
├── information/
│   ├── brand-guidelines.mdx
│   ├── contact.mdx
│   ├── terms.mdx
│   ├── privacy.mdx
│   └── disclaimer.mdx
└── images/                            ← Add your images here
    ├── hero.png
    ├── fizen-card-virtual.png
    ├── app-overview.png
    └── leo-vu.jpg
```

## Setup (one time, ~30 minutes)

### Step 1 — Push to GitHub
1. Create a new GitHub repo named `fizen-docs` (Public)
2. Upload all files from this folder
3. Keep the folder structure exactly as-is

### Step 2 — Connect Mintlify
1. Go to [mintlify.com](https://mintlify.com) → Sign up
2. New project → Connect GitHub → select `fizen-docs` repo
3. Mintlify auto-detects `mint.json` and deploys

### Step 3 — Custom domain
1. Mintlify dashboard → Settings → Custom Domain
2. Enter `docs.fizen.io`
3. Copy the CNAME value Mintlify provides
4. Go to your DNS provider (Cloudflare/Namecheap):
   - Type: CNAME
   - Name: docs
   - Value: [paste from Mintlify]
5. Wait 5–30 min for DNS to propagate

### Step 4 — Add images
Upload your images to the `/images` folder in GitHub:
- `hero.png` — main app screenshot (welcome page)
- `fizen-card-virtual.png` — card image
- `app-overview.png` — app screenshot
- `leo-vu.jpg` — CEO photo
- Add Fizen logo files to `/logo/` folder

### Step 5 — Update logo in mint.json
Replace logo paths in `mint.json`:
```json
"logo": {
  "dark": "/logo/fizen-white.svg",
  "light": "/logo/fizen-dark.svg"
}
```

## How to edit content (daily workflow)

Every page is a `.mdx` file. Edit directly on GitHub:

1. Go to github.com → your `fizen-docs` repo
2. Click on the file you want to edit
3. Click the ✏️ pencil icon (top right)
4. Make your changes
5. Click "Commit changes" → Done

Mintlify auto-deploys within 1–2 minutes.

## MDX quick reference

```mdx
# Page title (H1)
## Section title (H2)

Normal paragraph text.

<Note>Blue info box</Note>
<Warning>Orange warning box</Warning>
<Info>Gray info box</Info>

<Card title="Card title" icon="credit-card" href="/link">
  Card description text
</Card>

<CardGroup cols={2}>
  <Card title="Card 1" icon="bolt">Text</Card>
  <Card title="Card 2" icon="globe">Text</Card>
</CardGroup>

<Steps>
  <Step title="Step 1">Description</Step>
  <Step title="Step 2">Description</Step>
</Steps>

| Column 1 | Column 2 |
|---|---|
| Row 1    | Value    |
```

Full component reference: [mintlify.com/docs/components](https://mintlify.com/docs/components)

## Mintlify plan

- **Starter (free)**: has "Powered by Mintlify" branding, no custom domain
- **Growth ($150/mo)**: removes branding, custom domain, analytics
- Recommend: start on Starter to test, upgrade when ready to go live on docs.fizen.io
