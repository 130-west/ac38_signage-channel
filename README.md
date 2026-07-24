# AC38 ScreenCloud Channel

Static HTML zones for the America's Cup ScreenCloud channel.

## Workflow

- `dev` is the working branch.
- `main` is the live branch.
- Cloudflare Pages should use `main` as the production branch and preview deployments for `dev`.

## ScreenCloud URLs

Use one iframe/app reference per ScreenCloud zone:

- `/zones/header.html`
- `/zones/right-rail.html`
- `/zones/bottom-meet-teams.html`
- `/zones/bottom-standings.html`

The full-browser review pages are:

- `/previews/meet-teams.html`
- `/previews/standings.html`

## Local Preview

From this folder:

```sh
python3 -m http.server 8000
```

Then open:

```text
http://127.0.0.1:8000/previews/meet-teams.html
```
