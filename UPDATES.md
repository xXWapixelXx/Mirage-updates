# Update manifest (maintainer notes)

This repo hosts Mirage's public update feed. The in-app update check reads
`appcast.json`; `source.json` is an AltStore/SideStore source.

## Publish a new version
1. Ship the new build (bump `MARKETING_VERSION`).
2. Edit `appcast.json`:
   - `version` — the new version (e.g. `2.2.0`)
   - `notes` — what's new (shown in-app)
   - `url` — where users get it
3. Commit + push. Mirage picks it up on next check (Settings → Updates).

Only bump `version` above the shipped build when an update is actually available.
