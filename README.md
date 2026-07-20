# chkt.org

The landing page for [CHKT](https://github.com/FOSSCharlie/chkt), a
self-hosted, stupidly simple todo list.

**Live site:** [chkt.org](https://chkt.org)

## What's here

This repo is just one file: `index.html`. No build step, no
dependencies to install, no framework — open it in a browser and
that's the whole site.

The page includes a fully working miniature version of the real app
right in the hero section (add a task, check one off, delete one) so
visitors can try the interface before installing anything.

## Local preview

Since it's a single static file, you can preview it by opening
`index.html` directly in a browser, or serve it locally with
whatever you have handy, e.g.:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deployment

The site is hosted on **GitHub Pages**, deployed straight from the
`main` branch of this repo (root folder). Pushing to `main` updates
the live site automatically — no CI/CD pipeline required.

The custom domain (`chkt.org`) is configured via:
- A `CNAME` file in this repo (added automatically by GitHub when the
  custom domain is set in **Settings → Pages**)
- DNS `A` records at the domain registrar pointing to GitHub Pages'
  IP addresses

## Related

- [FOSSCharlie/chkt](https://github.com/FOSSCharlie/chkt) — the CHKT
  app itself (Docker image, source code, releases)

## Changelog

See [CHANGELOG.md](./CHANGELOG.md) for a history of changes to this
site.

## License

MIT — same as the CHKT app. See the
[main repo's license](https://github.com/FOSSCharlie/chkt/blob/main/LICENSE).
