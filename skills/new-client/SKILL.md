---
name: new-client
description: Creates a Cocoa client file for a school, team or district. Covers brand colors, fonts, venues, board specs, conference and partners. Use when someone says "add a new client", "set up [school]", "start a file for [team]", "research [school]'s branding", or names a school that has no folder in clients/ yet.
---

# New client file

Create `clients/<slug>/` in the cocoa-studio repo with `client.json`, `notes.md` and an empty `assets/` folder.

1. **Slug:** use a short, lowercase name with hyphens (`uta`, `nc-at`, `collierville-hs`). Check that `clients/<slug>/` does not already exist; if it does, use the client-update skill instead.
2. **Research the athletics brand from public sources:**
   - The athletics site: read its theme color meta tag and header and button colors, and note the nickname, the hashtag and the conference.
   - The school's brand or visual-identity guide, if one is published, for official HEX/PMS values and typefaces.
   - Venue names for each sport, plus any published board specs from facility, production or tech-packet pages and manufacturer press releases.
   - The multimedia rights or properties partner (Learfield, Playfly, a school-run "Sports Properties", etc.).
3. **Record only what you can source.** Put the URL beside each fact in `sources`. When a value is a guess, mark it with `"confidence": "estimated"`. Put anything unknown in `open_questions`.
4. **Choose web fonts** that echo the brand's type. If the official typeface is not on Google Fonts, pick a close Google Fonts match and note the substitution.
5. **Write `client.json`** following `references/client-schema.md`, and start `notes.md` with a dated "File created" line.
6. **Check contrast:** pick `on_primary` and `on_accent` text colors that reach 4.5:1 or better on their backgrounds.
7. **Report** a short summary to the team member: palette swatches as HEX values, fonts, venues, board specs found, and open questions.

Never record personal details about students or staff beyond names and public titles.
