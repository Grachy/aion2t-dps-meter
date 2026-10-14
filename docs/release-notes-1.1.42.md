# Release 1.1.42

## New features

- **Movable tool dock:** open or hide the meter, full map, pet mini-map, checklist, compact checklist, world bosses, dungeon gathering rooms, activity timers and settings. Choose vertical or horizontal orientation, icon size, panel scale, background opacity and icon opacity independently.
- **Independent utility windows:** settings, maps, history, checklist, gathering rooms, world bosses and fight details open separately from the compact meter. Includes custom drag handles and small resize grips.
- **AUTO combat mode:** automatically selects ordinary PvE, bosses, PvP and own training-dummy combat. PvP requires confirmed player-versus-player damage; unknown NPC attacks no longer switch AUTO into PvP.
- **PvP team statistics:** current verified teams show damage/DPS, observed CP or GS, HP and active effects. CP uses the native icon and a light-blue label.
- **Approximate Global rDPS:** labelled **≈ rDPS**, using Global client coefficients, observed effect IDs/levels and shared debuffs on the actual damage target. Supporters with no direct damage remain visible in attributed results and history.
- **Compact checklist and activity overlays:** denser daily/weekly counters, visible completion ticks, clearer Arena/Battlefield icons, and activity timers with daily/weekly reset countdowns.
- **Pet mini-map:** movable, resizable and centred on the current player/location. Soul gains automatically enable farming trackers; tracked pets can also be selected manually. Shows one current farming stage: 5, 25 or 75 souls.
- **Map layers and collection progress:** separate toggles/icons for pets, hidden cubes and gathering resources. Map opacity fades the terrain/background while keeping player and target markers visible. The full map shows cumulative souls out of 105 and level 3/unfinished totals.
- **Separate training history:** training-dummy tests have their own tab, separated from ordinary fights and dungeon runs.

## Fixes and improvements

- Improved player identity and CP/GS readings, including additional Power Shard variants, first server discovery and character/actor changes. Unobserved values remain unknown.
- Gathering rooms show total/free slots, persistent empty rows, full dungeon mode/stage and server names; removed average CP and made the window substantially more compact.
- Fixed confirmed wipe/reset boundaries keeping separate attempts joined, including delayed hits after combat ends. Rows and timers reset with the new attempt.
- AUTO can display received damage from other confirmed players on a live world boss before your first attack and after you stop, while preserving your engaged-boss and recent PvP priority.
- Improved map position updates and delivery to both maps; skill direction vectors no longer become false world coordinates. The player marker is a direction-neutral diamond.
- Improved capture restart/retry handling and retention of zero-damage block/parry events. Optimized rDPS interval processing while preserving fight details, history and replay data.
- Fixed locked-panel fading and the persistent unlock hint. The hint expires; Alt+click still unlocks the panel.
- Fixed update prompts being clipped inside a small meter window.
- Restored metric/time to the lower left and combat mode/ping to the lower right. Fixed dark metric text and native Windows captions bleeding through the transparent dock.
- Dock buttons consistently toggle their tool windows; full-map headers, checklist labels and resize grips are more compact and clearer.

## Known limitations

- Global rDPS is an estimate from supported observed effects. Missing providers, effect levels, baseline stats or unobserved effects cannot receive precise attribution.
- Crowded world bosses may not supply ordinary hit amounts for most other players. This update cannot reconstruct absent damage or guarantee a complete leaderboard. Independent raid membership remains unverified.
- Map positions depend on available game observations; ordinary walking in an empty area can still lag or use an indicated estimate. Map spawn/resource markers are static locations, not live availability.
- Live EU combat, party effects, movement/character switching, and transparent-dock Alt+Tab/drag remain recommended checks before wider distribution.

## Validation

Native executable and installer metadata verified as **1.1.42**, with an x64 native executable. Release build, obfuscation of 21 scripts and built-browser UI checks passed. Npcap prerequisite checks passed installed/missing/actual cases across all 10 installer languages, and packaged Global/KR rDPS catalog copies match their sources.

Earlier source validation passed **329 Rust tests** (7 skipped), a recorded AUTO replay of **166,867 chunks**, focused identity/map/rDPS checks and actual native-window checks. These recorded checks do not substitute for a fresh live test of this installer.

Installer: `aion2t-dps-setup-1.1.42-x64.exe` (25,888,043 bytes).

SHA-256: `b9f313e79bdb46b332cc39673bfeb3a568f7c6b64618d16f12be3c511b61c75a`.
