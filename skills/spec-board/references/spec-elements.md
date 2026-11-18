# Spec elements

Each element has a clean version and a partner version. The partner version adds a presented-by lockup or panel using the dashed `.partner` placeholder, wrapped in `.sp` so the header switch shows and hides it.

## Full-screen moments (center-hung, 16:9)

| Moment | Clean | Partner version | Motion |
|---|---|---|---|
| 3-pointer | "[Short] / From Deep" over the primary color, a giant "3", accent stripes | "3-Point Tracker presented by", plus a "threes tonight" counter | Stripes sweep in, the 3 zooms, the words slide up |
| Starting lineup | Primary panel with player silhouette and outlined number, then name, position, hometown and 3 stats | "Starting Lineup presented by" | Panel wipe, the silhouette rises, info staggers in |
| Make Noise | Big crowd prompt with a noise meter | "Noise Meter presented by" | Text pulses, meter bars bounce |
| Win / final | "[Short] Win", score band, "Final" | "Player of the Game presented by" | Band wipe, scores zoom in |

Other moments to add on request:
- Dunk, block, timeout and halftime.
- "Welcome to [arena]".
- Free throw distraction.
- Kiss cam and fan cam frames.
- Senior Night tribute.
- Themed nights (Pink Out, Homecoming, Heritage).

## Ribbon / fascia (about 24:1)
- A score bug on the left, then a looping marquee of segments: nickname, "Defense", hashtag and venue.
- The partner version swaps every other segment for a partner panel.
- The track content is duplicated so a translateX(-50%) loop runs seamlessly.

## Scorer's table LED (about 8:1)
- Accent end caps, with "[School] [Nickname]" on the primary color and a light sweeping shine.
- The partner version gives about a third of the width to an "Official partner" panel.

## Marketing graphics
| Graphic | Size | Content |
|---|---|---|
| Game day social | 4:5 | "Game Day", matchup, time and venue, player silhouette |
| Final score | 1:1 | "Final", both scores, accent bar |
| Themed-night story | 9:16 | Theme title, one line of copy, silhouette |
| Email header | 3:1 | "Next Home Game" block, matchup, date and venue, "Get tickets" button |
| Announcement | 1:1 | Schedule release, signing or milestone |
| Also available | | Gameday countdown, starting five, halftime stats, player of the game, record-breaker, recruiting commit, season-ticket push, sponsor thank-you, broadcast lower-third |

Never show a flashing effect faster than 3 times a second.
