# Zero-Line Clinic Hub

Deploy only the files in this folder's root (index.html, manifest.json, sw.js, icons, robots.txt, sitemap.xml).

- `index.html` is the protected build: minified and obfuscated, with a host check. Deploy this.
- `source/` is your readable master. Keep it in a PRIVATE repository, never in the public site repo.
  To rebuild: edit `source/index.src.html`, then run `build.mjs` (Node) with Tailwind 3.4 and javascript-obfuscator.
- Host check: the protected build only runs on the hosts listed in `ALLOWED_HOSTS` (default: your GitHub Pages host, localhost).
  Build for another domain with `ALLOWED_HOSTS=yourdomain.com node build.mjs`.

Default doctor PIN is 1234. Change it in Settings > Sync before real use.
