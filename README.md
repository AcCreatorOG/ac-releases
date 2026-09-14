# AC releases

This public repository contains only the Windows installer, release notes, and
the small update file used by AC's **About & Updates** screen. It must never
contain AC source code, `memory.json`, personal reports, backups, or API keys.

## First publication

1. GitHub Pages will publish the `docs` folder.
2. Create the GitHub release tag `v1.0.0-beta.1` and attach the exact file
   named `AC-Setup-1.0.0-beta.1.exe`.
3. Generate `docs/update.json` with the installer URL and checksum.
4. Rebuild AC with the GitHub Pages update address in `ac_release.json`.
   This turns on the safe start-up update check for future installs.

## Future releases

For every new AC version:

1. Build and test the new installer locally.
2. Create a matching GitHub release and upload that exact installer.
3. Update `docs/update.json`.
4. Build the next installer with the same Pages update address embedded.

AC only tells a user that an update is available. It verifies the update
details before showing a button, then opens the release page only when the
user chooses to download it. It never silently installs an update.
