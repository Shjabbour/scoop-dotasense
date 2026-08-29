# DotaSense Scoop Bucket

[![Tests](https://github.com/Shjabbour/scoop-dotasense/actions/workflows/ci.yml/badge.svg)](https://github.com/Shjabbour/scoop-dotasense/actions/workflows/ci.yml)
[![Excavator](https://github.com/Shjabbour/scoop-dotasense/actions/workflows/excavator.yml/badge.svg)](https://github.com/Shjabbour/scoop-dotasense/actions/workflows/excavator.yml)

Official vendor-maintained [Scoop](https://scoop.sh) bucket for
[DotaSense](https://dotasense.com/), a free Dota 2 timer app for Windows.
DotaSense provides audio and visual reminders for camp stacks, runes, Roshan,
Tormentor, siege creeps, and custom events. The Windows app also includes an
optional always-on-top overlay and local Valve Game State Integration clock
synchronization.

## Install

```powershell
scoop bucket add dotasense https://github.com/Shjabbour/scoop-dotasense
scoop install dotasense/dotasense
```

The manifest downloads the exact versioned release from the public
[DotaSense release repository](https://github.com/Shjabbour/dota-releases/releases),
verifies its SHA-256 checksum, and extracts the Electron app without running the
NSIS installer.

## Update

```powershell
scoop update
scoop update dotasense
```

The bucket checks the public GitHub release feed and uses versioned download
URLs so updates remain reproducible.

## Current Windows release boundary

- Windows 10 or Windows 11, 64-bit only.
- The timer core is free; optional Pro features are separate.
- The current installer and extracted application are Authenticode-signed with
  Microsoft Artifact Signing. Scoop also verifies the published SHA-256 before
  extraction; review the
  [release evidence](https://dotasense.com/download#windows-release-evidence)
  before running it.
- DotaSense does not read or modify protected game memory, inject code, or alter
  Dota 2 binaries. Optional match-clock synchronization uses Valve's local Game
  State Integration feed.
- The app stores preferences under the normal Windows user profile. Removing the
  Scoop package can leave those preferences in place.

This is a DotaSense-owned bucket, not an entry in Scoop's community Extras
catalog. The [Extras package proposal](https://github.com/ScoopInstaller/Extras/issues/18634)
is following Scoop's separate issue-first review process.

## Help

- [DotaSense setup and safety FAQ](https://dotasense.com/faq)
- [Overlay setup guide](https://dotasense.com/guides/overlay-setup)
- [Report a packaging problem](https://github.com/Shjabbour/scoop-dotasense/issues/new/choose)

DotaSense is an independent third-party project and is not affiliated with,
sponsored by, or endorsed by Valve Corporation.
