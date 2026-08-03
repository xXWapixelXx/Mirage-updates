# Update manifest (maintainer notes)

This repo hosts Mirage's public update feed and the release downloads.

- `appcast.json` — read by the in-app update check (Settings → Updates).
- `source.json` — an AltStore / SideStore source.
- GitHub Releases here host the `.ipa` itself.

## Publish a new version

1. **Ship the build** in the app repo: bump `MARKETING_VERSION` and
   `CURRENT_PROJECT_VERSION`, update `CHANGELOG.md`, merge to `main`.
2. **Build the IPA** — `./export-ipa.sh` in the app repo. It is unsigned on
   purpose; SideStore / AltStore re-sign on-device, which is also what lets the
   Live Activity ship (a cable install can't sign the widget).
3. **Cut the release here** — tag `vX.Y.Z`, title `Mirage X.Y.Z — <tagline>`,
   attach `Mirage.ipa`.
4. **Update BOTH manifests:**
   - `appcast.json` — `version`, `notes` (prose, shown in-app), `url`.
   - `source.json` — prepend a new entry to `apps[0].versions` (newest first)
     with `version`, `date`, `localizedDescription`, `downloadURL` pointing at
     the release asset, `size` in bytes, and `minOSVersion`.
5. **Commit + push.** Mirage picks it up on the next check.

> `source.json` is easy to forget — it sat on 3.0.0 while `appcast.json` went to
> 3.0.3, so SideStore users saw no updates for three releases. Update both, every
> time. `size` must be the real byte count (`stat -f%z build/Mirage.ipa`).

Only bump `version` above the shipped build when an update is actually available.
