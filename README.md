# sageroom.software

The holding site for **Sage Room Software**, live at <https://sageroom.software>.

It's a single static page — no build step, no framework. All source lives in
[`site/`](site/):

- `index.html` — the page
- `style.css` — styling
- `fonts/` — embedded fonts

## Deployment

The site is deployed on [Cloudflare Pages](https://pages.cloudflare.com/) via Git
integration: every push to `main` triggers an automatic deployment. Cloudflare serves
the contents of `site/` directly — there is no build command.

The publish directory and project name are configured in
[`wrangler.jsonc`](wrangler.jsonc) (`assets.directory` → `site`).

### Local preview

```sh
npx wrangler pages dev site
```

### Manual deploy

Deploys happen automatically on push, but you can also publish from the command line:

```sh
npx wrangler pages deploy site
```

## Editing

Edit the files in `site/` and push to `main`. Changes go live automatically once the
Cloudflare Pages deployment completes.
