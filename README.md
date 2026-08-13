# netomat website (www.netomat.io)

Hugo site using [PaperMod](https://github.com/adityatelange/hugo-PaperMod) with the
[netomat-theme](../netomat-theme) brand layer on top.

## Local development

```bash
git clone --recurse-submodules git@github.com:netomat/website.git
hugo server -D          # serve with drafts at http://localhost:1313
hugo                    # production build into public/
```

## Updating the shared theme

```bash
git submodule update --remote themes/netomat
git add themes/netomat && git commit -m "Bump netomat theme"
```

Never override layouts locally — visual changes belong in the netomat-theme repo.

## Cloudflare Pages settings

- Build command: `hugo --gc --minify`
- Build output directory: `public`
- Environment variable: `HUGO_VERSION = 0.165.0`

Submodules are cloned automatically (netomat-theme resolves relative to this repo's
GitHub owner, so it must exist at `github.com/netomat/netomat-theme`).
