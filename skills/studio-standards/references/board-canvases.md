# Board canvases

Always use the client's real board specs from `client.json` → `boards`. When a spec is unknown, use these representative canvases. Label the result "representative size", and add the missing spec to the client file's `open_questions` so Terrence can ask for it.

| Surface | Representative canvas | Aspect | Notes |
|---|---|---|---|
| Center-hung / main video board | 1920×1080 | 16:9 | Most college boards are 16:9 or close to it. End-hung boards are often taller (e.g. 11×19 ft ≈ 10:17 portrait or 19:11 landscape). Check the specs. |
| Ribbon / fascia | 2880×120 | 24:1 | Real ribbons run 20:1 to 60:1. Design a looping track that tiles. |
| Scorer's table LED | 1536×192 | 8:1 | Appears in every sideline broadcast shot. Keep it legible at a distance. |
| Stanchion / corner | 768×384 | 2:1 | |
| Social feed | 1080×1350 | 4:5 | |
| Social square | 1080×1080 | 1:1 | |
| Story / Reel | 1080×1920 | 9:16 | |
| Email header | 1200×400 | 3:1 | Use 2× for retina. |
| Broadcast | 1920×1080 | 16:9 | Keep within title-safe margins (5%). |

Pixel math: physical size (mm) ÷ pixel pitch (mm) = pixels. For example, a 26 ft × 30 in table at 3.9 mm pitch is about 2032×195.
