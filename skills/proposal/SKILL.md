---
name: proposal
description: Builds a Cocoa game day proposal for a client in their brand, either as a slide deck or as an interactive proposal site with a package explorer and estimate builder. Use when someone says "build a proposal for [school]", "make a deck for [client]", "pricing deck", "packages presentation", or "interactive proposal site".
---

# Client proposal

Inputs: `clients/<slug>/client.json` and `../studio-standards/references/pricing.md`.

## Choose the format
- **Deck:** use the Slides artifact type when it is available; otherwise make a PPTX. Use 12 slides in this order:
  1. Cover (dark).
  2. Why it pays for itself (content fans watch, moments partners own, proof at renewal, and "the math" line).
  3. Lineup table.
  4. Starter.
  5. Essentials.
  6. Full Season (marked recommended unless the client file says otherwise).
  7. Championship (dark).
  8. High school.
  9. À la carte.
  10. What's included.
  11. Terms.
  12. Next steps, in the primary color, with Terrence's contact: Terrence@CocoaCreates.com · 319-389-6266.
- **Interactive site:** copy `proposal-site-template.html` to `cocoa-previews/<slug>/index.html`, then:
  - Swap the CSS color variables, fonts, names, venue and rights holder.
  - Keep the PACKAGES and ADDONS arrays in sync with pricing.md.
  - Publish with the publish-preview skill.

## Tailor it to the client
- Use their nickname, hashtag and venue names, for example "Welcome to [arena]" and "[Nickname] Win".
- Name their rights holder in the terms. If you don't know it, say "your partnerships team or multimedia rights partner".
- In the second-sport line, name their real other venue (for example football at their stadium).
- Recommend the package that fits the level and what the client said in meetings (`client.json` → `meetings`).
- Footer on every slide: "Prepared for [Name]".

## Finish
- Add the deliverable link to `client.json` → `deliverables`.
- Remind the team member that a deck artifact is private until it is shared.
- Hand the link to Terrence to send. Do not email it yourself.
