# Cocoa Studio

The Cocoa Creative studio toolkit for the creative team. It is a Claude plugin plus a shared folder of client files.

The team handles client files, proposals, spec work, graphics and preview sites. Terrence handles prospecting and all client email; the toolkit never emails clients.

## What it does

| Say this in Claude | What happens |
|---|---|
| "Add a new client: [school]" | Researches the brand (colors, fonts, venues, board specs, rights holder) and creates `clients/<slug>/` |
| "We met with [school]. Here are the notes…" | Logs the meeting, the chosen package, the spec elements to build and open questions |
| "Build a proposal for [school]" | Makes a deck or an interactive proposal site in their brand, with Cocoa pricing |
| "Build the spec for [school]" | Makes the animated spec page (full screen, ribbon, scorer's table, marketing graphics) with a clean/partner switch |
| "Make a game day graphic / email header / final score for [school]" | Renders PNGs (and motion if asked) in their brand, with or without a partner |
| "Publish it" | Pushes to preview.cocoacreates.com and confirms the Netlify deploy |

The house rules (no "sales", no "Iowa", no free offers, the client's own palette) load automatically.

## Setup for each team member (one time)

1. **Team Claude account:** install the plugin (`cocoa-studio.plugin`) from the file Terrence shares.
2. **Connectors** (Settings › Connectors in the Team account; an admin may need to allow them first):
   - **GitHub:** access to `CocoaCreates/cocoa-studio` and `CocoaCreates/cocoa-previews`.
   - **Netlify:** the `cocoa-previews` site.
   - **Higgsfield:** for motion plates and video.
   - **Adobe:** Photoshop and Express.
3. **After Effects (designers only):** on a computer with After Effects, install the [After Effects MCP](https://github.com/thellamainator/after-effects-mcp) by following its README. Then use Claude Code or the Claude desktop app on that machine.
4. **Claude Code (optional):** `git clone` this repo and run `claude` in it. The plugin's skills and the client files are all here.

## Layout

```
cocoa-studio/
├── .claude-plugin/plugin.json
├── skills/            ← studio-standards, new-client, client-update, proposal,
│                         spec-board, marketing-graphics, publish-preview
└── clients/
    └── uta/           ← pilot client: client.json, notes.md, assets/
```

Client-facing pages live in the separate `cocoa-previews` repo and go live at `https://preview.cocoacreates.com/<slug>/`. Private notes and contacts stay here in cocoa-studio and are never published.

## Pilot

UT Arlington:
- Proposal: https://preview.cocoacreates.com/uta-game-day/
- Spec: https://preview.cocoacreates.com/uta-game-day/spec/ (add `?partners=1` for partner mode)
