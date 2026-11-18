---
name: studio-standards
description: Cocoa Creative house standards for any client creative work. Use whenever working on a Cocoa client, school, team, proposal, spec board, game day graphics, preview site or brand file, or when someone asks "what are our rules", "what do we charge", or "how should this look".
---

# Cocoa Creative studio standards

Cocoa Creative (CEO and Creative Director: Terrence Thames) builds game day video board content, broadcast graphics, partner activations and marketing graphics for college athletics (mid-majors, D2s, HBCUs) and high schools.

## Who does what

- The creative team handles client files, proposals, spec work, graphics, preview sites and client updates.
- Terrence alone handles prospecting and all client email. Never send, draft or schedule email to a client or prospect from this toolkit. When a deliverable is ready to go out, tell the team member to hand the link to Terrence.

## Writing rules (all client-facing copy)

- Plain, warm, confident and concise.
- Never use the word "sales" to describe Cocoa's work. Say "partnerships", "revenue" or "partner activations".
- Never say Cocoa is in Iowa. If location comes up, say "the Heartland".
- No free offers. Spec work is made only for a client Terrence has already met, and only when the client file says `stage` is `met` or later.
- Use real facts about the client. Never invent statistics, quotes, player names, sponsors or partner logos. Use clearly marked stand-ins: "Player Name", "Opponent", a dashed "Partner logo" panel.
- Never use a client's official logo files unless the client supplied them (they live in `clients/<slug>/assets/`). Until then, use the school name set in the brand display face.

## Design rules

- High design with an "Apple website feel": big type, generous space and strong font pairings.
- Always build in the client's own palette from `clients/<slug>/client.json`. Never use generic styling.
- Light text on dark or primary colors; dark text on light accent colors such as gold or orange. Keep body text at 4.5:1 contrast or better.
- Every page must work at phone width (390px) with no sideways scroll.
- Respect `prefers-reduced-motion`.
- Client pages carry `noindex, nofollow`.

## Where things live

- Client data: `clients/<slug>/` in the cocoa-studio repo, containing `client.json`, `notes.md` and `assets/`.
- Client-facing pages: the `cocoa-previews` repo, served at `https://preview.cocoacreates.com/<slug>/`:
  - `/<slug>/` holds the proposal.
  - `/<slug>/spec/` holds the spec work.
  - `/<slug>/graphics/` holds the graphics sets.
- Pricing: `references/pricing.md`. Board canvas sizes: `references/board-canvases.md`.

## Connected tools the team may use

- GitHub (the cocoa-previews and cocoa-studio repos) and Netlify (the cocoa-previews site) for publishing.
- Higgsfield for AI motion and video backgrounds, b-roll style plates and hype-open drafts.
- Adobe (Photoshop, Express) for image cleanup, cutouts, resizing and social variations.
- After Effects MCP, on a designer's own machine with After Effects installed, for production motion comps and renders.
- Use whichever of these are connected. When one is missing, build the HTML/CSS version and say which tool would upgrade it.
