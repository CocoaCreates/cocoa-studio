---
name: publish-preview
description: Publishes a Cocoa client page or graphics set to preview.cocoacreates.com through the cocoa-previews GitHub repo and Netlify, then confirms the deploy. Use when someone says "publish it", "put it live", "push to the preview site", "deploy [client]", or "give me the link".
---

# Publish to preview.cocoacreates.com

- **Repo:** `CocoaCreates/cocoa-previews`, branch `main`.
- **Site:** Netlify site `cocoa-previews`, which deploys automatically on every push to `main`.
- **Paths:** each client folder is served at `https://preview.cocoacreates.com/<folder>/`.

1. **Get the repo.** Clone it, or fetch the latest from `main`. In a shallow clone, run `git fetch origin main` and rebase before pushing.
2. **Check the files before committing:**
   - Every HTML page has `<meta name="robots" content="noindex, nofollow">`.
   - There are no `localhost` or `file://` links.
   - Images are compressed (each JPG/PNG under about 1 MB; each MP4 under about 8 MB).
   - Nothing private is included: no meeting notes, no client.json, no contacts. Those stay in cocoa-studio.
3. **Commit and push** only the client's folder, with a message like `uta: add spec page`.
4. **Confirm the deploy** with the Netlify connector's deploy reader: find the latest deploy for the site and wait for state `ready`. If the deploy fails, read its log, fix the problem and push again.
5. **Hand off** the live URL. If the work came from a client file, add the URL to `client.json` → `deliverables`.

Never delete or overwrite another client's folder. Never change `netlify.toml`, the root `index.html` or DNS without Terrence's OK.
