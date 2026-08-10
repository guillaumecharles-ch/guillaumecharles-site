# guillaumecharles.com

One-page site for Guillaume Charles — independent Nexthink / digital employee experience advisory.

Static, single file, no build step and no dependencies. `index.html` is the whole site;
styles and the scroll-reveal script are inline.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy — GitHub Pages

1. Push this repo to GitHub (must be **public** for Pages on a free account).
2. Repo → **Settings** → **Pages** → Source: *Deploy from a branch*, Branch: `main`, folder: `/ (root)`.
3. The site goes live at `https://<username>.github.io/<repo>/` within a minute or two.

### Custom domain (guillaumecharles.com)

1. Create a file named `CNAME` in the repo root containing exactly:
   ```
   guillaumecharles.com
   ```
2. At your DNS provider, add these records:

   | Type  | Name  | Value                                                              |
   |-------|-------|--------------------------------------------------------------------|
   | A     | `@`   | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` |
   | CNAME | `www` | `<username>.github.io`                                             |

3. Repo → Settings → Pages → Custom domain → enter the domain → tick **Enforce HTTPS**
   (the certificate can take up to an hour to issue).

> Adding A records on `@` does not affect MX records, so email on the domain keeps working.

## Editing

The palette lives in the `:root` block at the top of `index.html` — Nexthink blue for
authority, amber for calls to action. Changing either is a one-line edit.
