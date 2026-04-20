# LiteWallet

Marketing and documentation site for **LiteWallet** — a non-custodial Litecoin wallet for Windows, macOS, Linux, iOS, and Android with MWEB privacy, hardware wallet support, and open-source code.

🌐 **Live site:** [litewallet.dev](https://litewallet.dev)

---

## About LiteWallet

LiteWallet is a self-custody Litecoin wallet available on every major platform. Key features:

- **Non-custodial** — your keys, your coins. 12-word recovery phrase. No accounts, no KYC.
- **MWEB privacy** — opt-in confidential transactions via Litecoin's MimbleWimble Extension Block.
- **Cross-platform** — Windows, macOS, Linux, iOS, Android.
- **Hardware wallet support** — Ledger and Trezor.
- **Free and open source** — MIT License.

---

## Tech stack

This repository contains the **marketing site**, not the wallet application itself.

| Layer | Technology |
|---|---|
| Framework | Vite 7 + React 19 |
| Routing | react-router-dom v6 |
| Head management | react-helmet-async |
| Styling | Tailwind CSS v4 |
| UI components | shadcn/ui + Radix primitives |
| Prerendering | @prerenderer/rollup-plugin (per-route SSG) |
| Language | TypeScript |
| Build output | Static HTML + JS bundle |

---

## Project structure

```
.
├── public/                # Static assets (favicons, robots.txt, images)
├── src/
│   ├── components/        # Reusable UI components
│   │   ├── ui/            # shadcn/ui primitives
│   │   └── renderers/     # Page section renderers (Hero, FAQ, etc.)
│   ├── pages/             # Route components (57 pages)
│   ├── data/              # Page manifests (content + schema definitions)
│   ├── hooks/             # Custom React hooks
│   ├── lib/               # Utilities
│   ├── router.tsx         # Central route definitions
│   ├── App.tsx            # Root app shell
│   └── main.tsx           # Entry point
├── vite/
│   └── sitemap-plugin.ts  # Build-time sitemap generator
├── package.json
├── vite.config.ts         # Vite + prerender configuration
└── tsconfig.json
```

---

## Local development

### Prerequisites

- Node.js 20+ (tested on 24.x)
- npm 10+

### Setup

```bash
git clone https://github.com/alhimic11y/litewallet.git
cd litewallet
npm install --legacy-peer-deps
```

The `--legacy-peer-deps` flag is required due to React 19 being newer than some peer-dependency declarations in the Radix UI ecosystem.

### Development server

```bash
npm run dev
```

Opens at [http://localhost:8080](http://localhost:8080). Hot module reload is active.

### Production build

```bash
npm run build
```

Produces the `dist/` folder with:
- 57 prerendered HTML files (one per route) with full page content
- Minified JS/CSS bundles with code splitting (vendor-react, vendor-ui, vendor-charts)
- Sitemap XML files (sitemap-core, sitemap-guides, sitemap-news)
- `robots.txt`

Build time: approximately 45 seconds (includes headless Chromium prerendering of all routes).

### Preview built output

```bash
npm run preview
```

Serves the `dist/` folder locally for testing before deploy.

---

## Prerendering architecture

Every route is prerendered to static HTML at build time. This ensures:

- **Perfect SEO** — Googlebot, Bingbot see full content immediately, no JS execution required.
- **AI crawler visibility** — GPTBot, ClaudeBot, PerplexityBot see full content (these crawlers don't execute JavaScript).
- **Fast first paint** — HTML arrives rendered; JavaScript hydrates on top.
- **Static hosting compatible** — Any standard web host can serve `dist/`.

Each prerendered HTML file includes:
- Full page content (headings, paragraphs, lists, tables)
- Per-route `<title>`, meta description, and canonical URL
- Open Graph and Twitter Card meta tags
- JSON-LD structured data (FAQPage, Article, BreadcrumbList, Organization, etc.)
- Deferred JS bundle references for client-side hydration

The prerenderer uses `@prerenderer/rollup-plugin` with `@prerenderer/renderer-puppeteer`. Configured in `vite.config.ts`.

---

## Deployment

The site deploys as **static HTML + JS** to any standard web host that supports URL rewrites.

### Basic deployment

1. Run `npm run build`
2. Upload the entire contents of `dist/` to your web root

### Required server configuration

For SPA fallback on routes that lack prerendered HTML, add the included `.htaccess` (Apache) or equivalent `nginx` config:

**Apache (nginx):**
```apache
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ /index.html [L]
```

**nginx:**
```nginx
location / {
  try_files $uri $uri/ /index.html;
}
```

### SEO recommendations

For canonical URL enforcement (prevents duplicate content from HTTPS/WWW/trailing-slash variations), use the provided `.htaccess` which handles:

- HTTP → HTTPS redirects
- www → non-www redirects
- Trailing slash normalization
- `/index.html` → clean URL rewrites

---

## Content updates

Page content is defined in manifests under `src/data/`. Each manifest declares:

- Page metadata (title, description, canonical URL, OG image)
- Section order (hero, FAQ, comparison, etc.)
- Per-section content (headings, body text, list items)
- JSON-LD schema blocks for rich results

To update page copy:
1. Edit the relevant manifest file in `src/data/`
2. Rebuild: `npm run build`
3. Redeploy the updated `dist/`

---

## SEO features

- ✅ Per-route prerendered HTML
- ✅ Canonical URL enforcement (HTML + server-side)
- ✅ JSON-LD structured data on every page
- ✅ Open Graph + Twitter Card meta tags
- ✅ Split sitemap (core / guides / news) for large-site crawl optimization
- ✅ `robots.txt` with explicit sitemap declarations
- ✅ Semantic HTML5 (main, article, section, nav, aside)
- ✅ Lazy-loaded images
- ✅ Responsive design (mobile-first)

---

## Browser support

- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari 16+ (macOS, iOS)
- Mobile browsers on Android 10+ and iOS 16+

---

## License

MIT — see [LICENSE](./LICENSE).

---

## Links

- **Website:** [litewallet.dev](https://litewallet.dev)
- **Download:** [litewallet.dev/download](https://litewallet.dev/download)
- **FAQ:** [litewallet.dev/faq](https://litewallet.dev/faq)
- **Changelog:** [litewallet.dev/changelog](https://litewallet.dev/changelog)
