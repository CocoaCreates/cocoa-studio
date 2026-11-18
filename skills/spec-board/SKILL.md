---
name: spec-board
description: Builds post-meeting spec work for a client showing how their game day could look on their own boards. Covers animated full-screen moments, ribbon/fascia, scorer's table LED and marketing graphics in their brand, with a switch between clean and partner-sponsored versions. Use when someone says "build the spec for [school]", "show them the full screen / ribbon / scorer's table", "spec board", "mock their video board", or "make a sponsored version".
---

# Spec board

Make spec work only for clients whose `stage` is `met` or later. If the stage is `lead`, stop and tell the team member that spec work follows a meeting with Terrence.

## 1. Gather inputs
- Read `clients/<slug>/client.json`.
- Build the elements in `selected.spec_elements`. If that list is empty, build the default set: fullscreen (4 moments), ribbon, scorers-table, and marketing graphics (game day 4:5, final 1:1, story 9:16, email 3:1, announcement 1:1).
- Include partner versions unless `selected.sponsored_variants` is false.
- Use the board sizes from `boards[]`, or the canvases in `../studio-standards/references/board-canvases.md`.

## 2. Build the spec page (always)
1. Copy `assets/spec-template.html` to `cocoa-previews/<slug>/spec/index.html`.
2. Swap the **BRAND CONFIG** block: `--c1` primary, `--c2` accent, `--c3` deep, `--on-c1` and `--on-c2`, `--display` and `--body` fonts. Update the Google Fonts link to match.
3. Replace all client copy:
   - Header, hero, nickname, venue names and rights-holder name.
   - Moment text, such as "[Short] From Deep", "[Short] Win" and the noise prompt.
   - Footer ownership line.
4. Keep the stand-ins: "Player Name", "Opponent", "Visitor" and the dashed "Partner logo". Only swap in real sponsor names or logos when the client supplied them and asked to see them.
5. Match aspect ratios to the real boards (`.screen.full`, `.screen.ribbon`, `.screen.table`). Add or remove elements to match `spec_elements`; `references/spec-elements.md` describes each one.
6. Check the page:
   - Render it with Playwright at 1280px and 390px, in both clean mode and `?partners=1` mode.
   - Look at each screenshot. Fix any overlapping text, words clipped at board edges, and text crossing stripes without a backing panel.
   - Confirm `scrollWidth` is 390 on mobile.
7. Publish with the publish-preview skill to `https://preview.cocoacreates.com/<slug>/spec/`. `?partners=1` opens in partner mode.

## 3. Upgrade motion (when tools are connected)
Follow `references/motion-tools.md`:
- **Higgsfield:** generate branded background plates, a hype-open draft or crowd b-roll. Place stills or loops into the spec page as `<video autoplay muted loop playsinline>` with a still poster.
- **After Effects MCP** (designer's machine): build production comps per element at the real board pixel size, then render MP4s and PNG stills. Add them to the page or to a download package.
- **Photoshop / Adobe:** cut out player photos the client supplied, resize to every canvas, and make social variations.
If none is connected, the HTML/CSS motion in the template is the deliverable.

## 4. Record and hand off
- Add `{ "type": "spec", "url": ..., "date": ... }` to `deliverables`, and set `stage` to `spec-sent` only after Terrence confirms he sent it.
- Give the team member the clean link and the partner-mode link to pass to Terrence.
