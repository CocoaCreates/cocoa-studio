---
name: marketing-graphics
description: Makes on-brand athletic marketing graphics for a Cocoa client. Covers game day social posts, final scores, upcoming-game promos for email newsletters, team announcements, themed nights, stories and sponsor thank-yous, with or without partner elements. Use when someone says "make a game day graphic for [school]", "email header for the next game", "social post announcing...", "final score graphic", or "graphics pack".
---

# Marketing graphics

1. **Inputs:** read `clients/<slug>/client.json` for the palette, fonts and nickname. From the request, get the graphic type, the facts (opponent, date, time, venue, score, names) and whether it includes a partner.
   - Use only the facts given.
   - For anything missing, use a clear stand-in ("Opponent", "Player Name") and list it in your reply.
2. **Build** each graphic in the tool the request names for that piece (`assetPlan[].tool`) and in the request's style template, at the exact canvas size from `references/formats.md`. Never fall back to hand-coded HTML/CSS or a Claude-native design tool; if the named tool can't be reached, ask on the request (studio-standards, "Questions on requests"). In every tool:
   - Use the client's palette and fonts.
   - Use the visual language of the spec page: skewed accent stripes, big condensed display type and a deep-color base.
   - Put text over imagery only on a solid or gradient backing.
3. **Export** PNG/JPG at 2x from that tool. Motion versions come from the requested motion tool: Higgsfield for plates, After Effects for comps (see `../spec-board/references/motion-tools.md`). After Effects runs on the designer's Mac.
4. **Variants:** make clean and partner versions when asked. The partner version gets a "Presented by [Partner logo]" lockup at the bottom.
5. **Check** each PNG yourself: nothing cut off, contrast OK, no typos in names or dates.
6. **Deliver:**
   - Save to `cocoa-previews/<slug>/graphics/<yyyy-mm-dd>-<name>/` with an `index.html` contact sheet.
   - Publish with publish-preview.
   - Send the PNGs to the team member.

Never use real player photos or official logos unless the client supplied them in `clients/<slug>/assets/`.
