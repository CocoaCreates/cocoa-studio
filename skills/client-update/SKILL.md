---
name: client-update
description: Updates a Cocoa client file after a meeting, call or new information. Records meeting notes, the chosen package, spec elements to build, sponsors, board specs and deliverable links. Use when someone says "we met with [school]", "update [client]", "they picked Full Season", "log these notes", "they want the ribbon and scorer's table", or pastes meeting notes about a client.
---

# Update a client

1. Open `clients/<slug>/client.json` and `notes.md`. If there is no client folder, run the new-client skill first.
2. From what the team member gave you (notes, a transcript, a summary), update these fields:
   - `meetings[]`: date, who attended, a 2–4 sentence summary, and their interests.
   - `stage`: move it forward only, for example `lead` → `met` after a first meeting.
   - `selected.package`, `selected.addons`, `selected.spec_elements` and `selected.sponsored_variants`: fill these in only when the client said so. Otherwise note them as a recommendation in `notes.md`.
   - `boards[]` and `partners`: update with any specs or sponsor names the client shared.
   - `open_questions`: add new questions and remove answered ones.
3. Append a dated entry to `notes.md` with decisions, asks and next steps. Keep it factual, with no speculation about people.
4. Say what changed, and suggest the next build step:
   - After a first meeting with no spec yet, suggest the spec-board skill.
   - After the package is chosen, suggest updating the proposal.
   - When graphics are requested, suggest the marketing-graphics skill.
5. Commit to the cocoa-studio repo with a message like `uta: log Nov 11 meeting, Full Season selected`.

Never draft or send email to the client. Follow-up email is Terrence's job, so tell the team member what Terrence should send.
