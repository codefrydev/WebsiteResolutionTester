# Website Resolution Tester

Static single-page tool to open a URL in a sized popup window and try device viewport presets (desktop, tablet, Android-style, and iPhone 4–17 logical sizes).

## Run locally

Open `index.html` in a browser, or from this directory:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080/`. Allow popups for the origin so “Launch Test” can open the child window.

## Deploy notes

- **Canonical, Open Graph, Twitter, `sitemap.xml`, and `robots.txt`** are set for production at [`https://codefrydev.in/WebsiteResolutionTester/`](https://codefrydev.in/WebsiteResolutionTester/). If you move the app, update those URLs consistently in `index.html`, `robots.txt`, and `sitemap.xml`.
- For richer social previews, add a **1200×630** PNG (or WebP) and point `og:image` / `twitter:image` at it; the repo currently references `favicon.svg` as a lightweight default.
- Serve **`favicon.svg`** next to `index.html` (relative `href="favicon.svg"` works for this path). If you prefer a root-absolute icon, use `/WebsiteResolutionTester/favicon.svg`.
- Crawlers read **`https://codefrydev.in/robots.txt`** by default. If your `robots.txt` is only under this project folder, add a `Sitemap:` line for this app in the **site root** `robots.txt`, or ensure this project’s `robots.txt` is copied to a URL crawlers use.

## Files

| File | Role |
|------|------|
| `index.html` | UI, presets, JSON-LD, Analytics |
| `favicon.svg` | Favicon / touch icon |
| `robots.txt` | Crawler rules + sitemap hint |
| `sitemap.xml` | Single URL entry for the homepage |

## License

See [LICENSE](LICENSE) in the repository.
