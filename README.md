# Scoop bucket for SculptForge

[SculptForge](https://github.com/islandmed/SculptForge) is a free, open-source digital sculpting app for Windows,
macOS and Linux. This bucket installs it on Windows with [Scoop](https://scoop.sh).

```powershell
scoop bucket add sculptforge https://github.com/islandmed/scoop-sculptforge
scoop install sculptforge
scoop update sculptforge        # later, to update
```

You get the portable `.zip` build: a **SculptForge** Start Menu shortcut, and `sculptforge-cli` (the command line tool
and MCP server) on your `PATH`. This is the portable build: its settings and data live in `bin\data`, which Scoop keeps across
updates.

## What is in here

| File | What |
|---|---|
| `bucket/sculptforge.json` | The manifest: the `SculptForge-<version>-windows-x86_64.zip` of a [GitHub release](https://github.com/islandmed/SculptForge/releases), its SHA-256, the shortcut and the `sculptforge-cli` shim. `checkver` and `autoupdate` read new versions and checksums from the releases (`SHA256SUMS.txt`) |

The Windows builds are not code-signed yet: if SmartScreen appears the first time you run SculptForge, choose
**More info**, then **Run anyway**.

## How it is updated

Every SculptForge release updates the manifest as one step of the release script
([`scripts/release.sh`](https://github.com/islandmed/SculptForge/blob/main/scripts/release.sh)), so the bucket matches
the newest release the same day. There is nothing to bump by hand: please don't open version-bump pull requests here.

## Questions and problems

Bugs, install trouble and ideas go to [SculptForge's issues](https://github.com/islandmed/SculptForge/issues); the
[guide](https://sculptforge.app/guide/installing.html) covers installing on every platform, and the
[Discord](https://discord.gg/gWrYkEmQhH) is the place for questions. SculptForge is free software under the
[GPL-3.0-or-later](https://github.com/islandmed/SculptForge/blob/main/LICENSE): <https://sculptforge.app>.
