# jeff-website

The source for [ljyjeff.com](https://ljyjeff.com): plain HTML and one CSS
file, served by GitHub Pages. No build step.

| Page | Path | Used for |
|---|---|---|
| Landing (coming soon) | `index.html` | ljyjeff.com, and Mistimed's marketing URL |
| Mistimed privacy policy | `privacy.html` | App Store Connect → Privacy Policy URL |
| Mistimed support | `support.html` | App Store Connect → Support URL |

`style.css` holds the colours from Mistimed's design tokens (light and dark).
`CNAME` tells GitHub Pages the custom domain.

The App Store links to the privacy and support URLs, so keep those paths
stable.

## Hosting setup (once)

1. **Pages:** Settings → Pages → Build and deployment → Source "Deploy from
   a branch", branch `main`, folder `/ (root)`. The custom domain fills in
   from `CNAME`.
2. **DNS** at the registrar for ljyjeff.com:
   - Apex `ljyjeff.com`: `A` records to `185.199.108.153`,
     `185.199.109.153`, `185.199.110.153` and `185.199.111.153` (optionally
     `AAAA` to `2606:50c0:8000::153` through `2606:50c0:8003::153`).
   - `www`: a `CNAME` to `ljyjeff.github.io`.
3. Once the DNS check passes in Settings → Pages, tick **Enforce HTTPS**.
4. Optional: verify the domain under your GitHub account's Settings →
   Pages, so no other account can claim it.
