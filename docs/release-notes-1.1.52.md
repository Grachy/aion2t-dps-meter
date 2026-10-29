# Release 1.1.52

- Restore saved Combat Assist and separate text-panel enablement after restart. This fixes the forced startup reset introduced in 1.1.51; layouts and selections remain saved.
- Offer all 440 class skill families across nine classes without first observing them in combat, with class/search filters and all-class effect selection.
- Add named Combat Assist presets with manual selection and optional automatic loading for the confirmed character. Effects on self are filtered by recipient, including allied buffs and hostile debuffs.
- Expand Premium performance settings to 12 independent controls. Separate boss casts/cooldowns from character cooldowns/effects; add merchant, cubes and PvP controls. Rename diagnostic recording to Replays.
- Reconcile official available skill, NPC and effect names in all ten locales; localize effects in the separate overlay, including live language changes. Correct map names and Chinese locale aliases.
- Allow the mini-map to select the zone, center and follow already observed session coordinates without character identity or a pet roster. Unknown mastery/progress remains unknown; pending login and real character switches hide stale positions. Coordinates must still be observed.
- Preserve previously verified Premium through a bounded 24-hour verification grace after signed expiry, with retry backoff. Explicit unlink, fresh signed denial and the documented unauthorized response still revoke access. Transient failures no longer erase paid choices.
- Add persistent tray recovery and early single-instance protection; restore the main meter after temporary game visibility changes.
- Preserve the merchant lock during Alt-clicks on tabs and controls; only its padlock unlocks the window by mouse.
- Add safe checklist rename migration using confirmed source-qualified character IDs, plus an explicit legacy merge with backup and latest readings rather than summed counters.
- Refine Global rDPS stat-bucket attribution and duplicate/exclusive-end effect handling while preserving raw damage accounting.
- Retain previous installer hotkey, Premium merchant and cube-direction fixes.

## Upgrade and validation

If 1.1.51 already saved Assist or the separate text panel as disabled, enable the desired panel once after updating; subsequent starts retain that choice.

The source changes previously passed 497 Rust tests and built-browser checks. At the user's request, this packaging pass checked only build success, embedded version and installer SHA-256, without rerunning the suites. Fresh live profile/position/combat checks remain recommended before broad publication. No CPU reduction percentage is claimed. Official name reconciliation uses the available extracted client databases; names unique to a newer client are not certified. Simplified Chinese uses Traditional game-name fallback where no official Simplified column exists.

Installer: [aion2t-dps-setup-1.1.52-x64.exe](aion2t-dps-setup-1.1.52-x64.exe) (44,719,215 bytes).

SHA-256: `bd8f43d789c4b4cea75609b2f86d0f16a8dc098ab9e5a499da2397438a2b40ab`.
