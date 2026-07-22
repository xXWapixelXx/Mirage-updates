# Mirage — update manifest

Public update feed for the private **Mirage** app. Mirage's in-app update check
reads `appcast.json` here.

## Publish a new version
1. Ship the new build (bump `MARKETING_VERSION`).
2. Edit `appcast.json`:
   - `version` — the new version (e.g. `1.5.0`)
   - `notes` — what's new (shown in-app)
   - `url` — where users get it (SideStore source, IPA link, or a page)
3. Commit + push. Mirage picks it up on next check (Settings → Updates).

Only bump `version` above the shipped build when an update is actually available.
