# Release 1.1.46

## Focus and overlay behavior

- **Hide while the game is not in focus is disabled by default.** Existing explicit on/off choices are retained.
- Fixed unsafe focus/visibility transitions when returning to the game. Automatic hiding no longer minimizes the HUD, and passive restoration does not activate it.
- Alt click-through changes no longer show an already hidden HUD. A hidden active HUD releases its keyboard focus.
- Applied passive transitions to the mini-map, floating dock/widgets and Combat Assist. Deliberately opened settings/history/replay windows retain normal interaction.

## World-boss personal damage

- Show your own skill breakdown while ordinary foreign damage remains unresolved.
- Choose **1-50 skills or all skills**, with a default of 8, including AUTO mode.
- Select from **20 columns**, including damage, DPS, critical rate, multi-hit count/damage, damage share and Double Critical.
- Row/column preferences persist. Controls and scrolling survive combat updates; limiting visible skills preserves full own totals and percentages.
- Renamed the displayed Smite statistic to **Double Critical**, retaining existing combat/history fields.

## History and boss identity

- Reduced initial work when opening large fights: 100 skill rows initially, more rows on demand and graphs built when opened.
- Detached history loads by fight ID, serializes requests, discards stale replies and displays loading/errors. Closing cancels delayed reopening.
- Fixed repeated Kromede registration losing the canonical boss name/code after another NPC appeared.
- Included saved player-limit and verified force/subparty display fixes while retaining all raw participants and observations.

## Combat replays and skill icons

- Added a separate **Combat replays** window with play/pause, 0.25-4x speed, forward/backward seeking, actor selection, zoom/pan and an activity/death timeline.
- Show observed positions, HP, casts, effects, damage and healing; hidden playback pauses.
- Included original client maps for **19 party dungeons/59 Map IDs**, with verified coordinate transforms and whole-map/fight-area views.
- Audited **7,012 PC skill variants** against Global client data, corrected **35 family mappings**, including **Noble Aura**, and added **194 exact variant exceptions** plus four missing original images.

## Known limitations

- Other players' ordinary damage at public bosses is not yet located in known packet formats. Full damage rankings, including your own party/raid, are not guaranteed; absence of those events from every received packet is not proven.
- Eight client-table icon references have no matching installed texture. Unsupported dungeon maps use a labeled coordinate plot; automatic floor selection is not implemented.
- Fresh in-game Alt+Tab/game restore checks are still needed for the exact reported center-cursor symptom. Live combat/capture and actual installation/update gates remain before wider distribution.

## Validation and download

- **387 Rust tests passed; 7 skipped**, plus cargo check and the optimized x64 release build.
- Full browser checks passed for **27 obfuscated scripts**, including the exact **883 final asset hashes** after native processing.
- Verified **1,300 source identities**, all five version files and native/installer metadata as **1.1.46**.
- Source/built browser tests cover missing/off/on focus preferences. Isolated native Windows checks cover 40 hide/show cycles, Alt mouse modes, focus/capture preservation, active hiding, minimized recovery and a stopped owner UI queue.
- Two actual Kromede recordings passed mapped replay controls with all five players and the boss positioned in Fire Temple.
- Npcap prerequisite checks passed all **10 installer languages** and three cases; all five disposable generated update/restart callback tests passed.

Installer: [aion2t-dps-setup-1.1.46-x64.exe](aion2t-dps-setup-1.1.46-x64.exe) (29,348,445 bytes).

SHA-256: `89bd1c9c9616a89a9f4d88c81ff0462b59b596999fdf9547c9fa8ab469f3960c`.
