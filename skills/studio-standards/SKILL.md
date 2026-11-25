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
- **Design requests use only the tools named in the request.** Each request in Studio HQ carries a tool per piece (`assetPlan[].tool`: Photoshop, Illustrator, Higgsfield, After Effects, or Higgsfield + After Effects) and a style template. Build every piece in exactly that tool and in that style.
- **Never substitute.** Do not build a requested design as hand-coded HTML/CSS rendered to an image, and do not use Claude's own Design artifact type or any other Claude-native design tool in place of the requested one. HTML/CSS is only for web pages (proposal sites, spec pages, contact sheets) or when the request itself picks it.
- **When a requested tool can't be reached** (a connector refuses, After Effects needs the designer's Mac, a file can't be fetched), stop that piece and ask instead of substituting: set the request's `status` to `needs-answer` and write the question (see "Questions on requests" below).
- "Claude decides per piece" in a request means choose among the connected tools listed above, never HTML/CSS.

## Questions on requests (Studio HQ)

Questions must be answerable on the front end, not only in Claude's notes.

- To ask: set `status` to `needs-answer` and write `questions` as a list, each `{ "q": "one clear question", "options": ["optional", "quick picks"] }`. Keep `response` as a one-line summary.
- Studio HQ shows these in a "Questions for you" panel and on the request, with an answer box.
- When someone answers, HQ writes `answer` (latest text), appends to `answers` ([{at, text, items:[{q,a}]}]) and sets `status` back to `new`. Read `answer` before continuing, then clear `questions`.
- Always set `resultUrl` to a full https:// link when a request is done (a preview page, artifact or file link), so "Open result" works. Use full https:// URLs in `response` text.
