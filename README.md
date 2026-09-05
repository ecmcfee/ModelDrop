# ModelDrop

An interactive calendar of open-weight LLM releases, 2019 to now.
Everything lives in a single static file: [`index.html`](index.html).

**Live site:** https://ecmcfee.github.io/ModelDrop/

## Viewing it locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000   # then visit http://localhost:8000
```

## How it deploys

`.github/workflows/deploy-pages.yml` publishes the repo root to GitHub Pages on
every push to `main` (and on demand via **Actions → Deploy to GitHub Pages → Run
workflow**). `.nojekyll` tells Pages to serve the files as-is instead of running
them through Jekyll.

## Custom domain

1. Add the domain under **Settings → Pages → Custom domain**.
2. At your DNS provider, point it at GitHub Pages:
   - apex (`example.com`) → `A` records to `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - subdomain (`www.example.com`) → `CNAME` to `ecmcfee.github.io`
3. Once DNS resolves, tick **Enforce HTTPS**.
