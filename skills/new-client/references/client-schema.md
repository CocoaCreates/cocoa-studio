# client.json schema

```json
{
  "slug": "uta",
  "name": "UT Arlington Athletics",
  "short": "UTA",
  "nickname": "Mavericks",
  "short_nickname": "Mavs",
  "level": "NCAA D1",
  "conference": "WAC",
  "hashtag": "#MavsUp",
  "website": "https://utamavs.com",
  "stage": "met",                       // lead | met | proposal-sent | spec-sent | signed | in-season
  "brand": {
    "primary":   { "hex": "#0064B1", "name": "UTA Blue" },
    "accent":    { "hex": "#F58025", "name": "UTA Orange" },
    "deep":      { "hex": "#0A1E3C", "name": "Navy" },
    "light":     { "hex": "#F4F6F9" },
    "on_primary": "#FFFFFF",
    "on_accent":  "#0A1E3C",
    "display_font": "Oswald",
    "body_font": "Public Sans",
    "font_note": "Official typeface not public; Oswald + Public Sans chosen as close matches",
    "confidence": "sourced"            // sourced | estimated
  },
  "venues": [
    { "name": "College Park Center", "sports": ["basketball", "volleyball"] }
  ],
  "boards": [
    { "venue": "College Park Center", "surface": "center-hung", "px": null, "aspect": "16:9", "pitch_mm": 3.9, "note": "four-sided Daktronics", "confidence": "estimated" }
  ],
  "partners": {
    "rights_holder": "Maverick Sports Properties",
    "known_sponsors": []                 // only names the client has shared with us
  },
  "contacts": [
    { "name": "", "title": "", "role": "decision maker" }   // public titles only
  ],
  "meetings": [
    { "date": "2026-11-11", "with": "", "summary": "", "interests": [] }
  ],
  "selected": {
    "package": null,                     // e.g. "Full Season"
    "addons": [],
    "spec_elements": [],                 // fullscreen | ribbon | scorers-table | stanchion | social | email | story | broadcast
    "sponsored_variants": true
  },
  "deliverables": [
    { "type": "proposal-deck", "url": "", "date": "" },
    { "type": "proposal-site", "url": "https://preview.cocoacreates.com/uta-game-day/", "date": "" },
    { "type": "spec", "url": "https://preview.cocoacreates.com/uta-game-day/spec/", "date": "" }
  ],
  "open_questions": [],
  "sources": [ { "fact": "", "url": "" } ]
}
```

Comments above are for reference only. Write the real file as valid JSON with no comments.
