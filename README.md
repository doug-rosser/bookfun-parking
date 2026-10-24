# bookfun-parking

Static parking page for [bookfunproject.org](https://bookfunproject.org).

Single-page site: project description, link to the public BookFun repository
(<https://bitbucket.org/drosser9/bookfun>), and contact email. Deployed via
GitHub Pages with the custom domain `bookfunproject.org`.

## Deploying

1. Push this repo to GitHub.
2. Repo **Settings → Pages**: Source = `Deploy from a branch`, branch `main` / `(root)`.
3. Add a **Custom domain**: `bookfunproject.org` (check "Enforce HTTPS").
4. In Squarespace DNS for the domain, replace the default records with:

   | Type | Host | Value |
   |---|---|---|
   | A | `@` | `185.199.108.153` |
   | A | `@` | `185.199.109.153` |
   | A | `@` | `185.199.110.153` |
   | A | `@` | `185.199.111.153` |
   | AAAA | `@` | `2606:50c0:8000::153` |
   | AAAA | `@` | `2606:50c0:8001::153` |
   | AAAA | `@` | `2606:50c0:8002::153` |
   | AAAA | `@` | `2606:50c0:8003::153` |

   (GitHub shows the exact values on the Custom domain settings page.)

5. Remove any Squarespace `WWW` CNAME, or add a `CNAME` record `www` → `<your-gh-username>.github.io` if you want `www.` to work (also add `www.bookfunproject.org` as a second custom domain on GitHub).

`index.html` is fully self-contained (no build step, no external assets).
