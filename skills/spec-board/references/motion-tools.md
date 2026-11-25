# Motion and design tools

Use whichever of these is connected in the session.

## Higgsfield (claude.ai connector)
- Best for: branded abstract background plates (light streaks and particles in the client's colors), crowd and arena atmosphere b-roll, and hype-open draft cuts.
- Start the session by calling its preset/instructions tool as its server instructions direct.
- Check the cost estimate before generating. Keep spec work to a few short clips.
- Prompt with the client's HEX colors and "no text, no logos, no real people". Add type and marks afterwards in HTML or After Effects, so nothing implies a real player or sponsor.
- Download the results into `cocoa-previews/<slug>/spec/media/`. Use 1080p H.264 MP4 under about 8 MB each, plus a poster JPG.

## After Effects MCP (local, designer's machine)
- The community server ([thellamainator/after-effects-mcp](https://github.com/thellamainator/after-effects-mcp)) bridges Claude to a running After Effects through a ScriptUI panel. Install it once per machine, following its README.
- Use it from Claude Code or the desktop app on that machine. It cannot run in a cloud session.
- Workflow:
  1. Create one comp per element at the real board pixel size (from `client.json` → `boards`) and 59.94 fps.
  2. Build shape layers and text in the brand fonts, and keyframe the same beats as the HTML spec.
  3. Render to the Media Encoder queue: MP4 for review, ProRes 4444 for the board.
- Save the `.aep` and the renders to the team's shared drive under `Clients/<slug>/Spec/`, not in git.

## Photoshop / Adobe (claude.ai Adobe connector)
- Call its mandatory init tool first.
- Use it to remove backgrounds from player photos the client supplied, crop and resize to each social canvas, and make social variations.
- Never alter official logos.

## When a requested tool is not connected
Do not substitute an HTML/CSS version. Set the request to `needs-answer` with a question saying which tool is missing and what would unblock it.
