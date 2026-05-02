## CNAME Protection

Do NOT modify or delete `CNAME` unless the user explicitly requests a custom
domain change.

**Why:** `CNAME` binds the custom domain `mikanmarusan.net` to the GitHub Pages
site. Removing or changing it breaks the GitHub-Pages-side custom-domain
routing — visitors are then served from the default `mikanmarusan.github.io`
host (or hit a 404 if that is also affected) instead of `mikanmarusan.net`.
DNS records for `mikanmarusan.net` live outside this repo and are not changed
by edits to `CNAME`.

**How to apply:** Treat `CNAME` as read-only. If a refactor or cleanup task
appears to touch it, stop and confirm with the user first.
