# Release 1.1.47

## Dungeon party damage

- Fixed party members being excluded from the damage table when the compressed party list was interpreted incompletely. The issue can affect any class or party composition, including two players of the same class.
- Use the complete verified roster in the current dungeon. Players remain separate; uncertain identities or conflicting servers are not merged.
- AUTO now counts the first eligible party hit, including several opening hits arriving between screen updates.
- The meter, boss details and new saved fights use the same participant scope. Existing saved history is not rewritten.

## Alt+click unlocking

- Improved Alt+left-click unlocking for the main HUD and mini-map.
- Unlock on the press and handle its matching release, including releasing Alt before the mouse button.
- Prevent the same gesture from immediately locking the window again. Existing hotkey bindings are retained.
- Respect hidden, minimized and covered windows.

Includes all previous 1.1.46 changes, including the final Combat Assist cooldown-reset and buff-selection fixes.

## Validation and limitations

- 398 Rust tests passed; 7 ignored, plus cargo check. These checks cover the unchanged source included in this installer and were not repeated solely for packaging.
- Three original recorded dungeon fights were replayed in six configurations. All five participants and exact boss damage totals were preserved, including the missing player's opening hits.
- Native Alt+click routing passed 40 isolated Windows cycles. The fresh release build passed the full browser suite for 27 obfuscated scripts, including early Alt release; all 883 final asset hashes match the checked build.
- Verified 1,306 source files, 14 previously checked fix-source/fixture hashes, five snapshot versions and native/installer metadata as 1.1.47. Optimized x64 native compilation and NSIS packaging succeeded.
- One recorded Nuakum replay omits its initial NPC spawn: live rows were checked against raw hits at the last pre-death update, while final details/history totals were checked against all recorded hits.
- Fresh in-game five-player combat, physical Alt+click and focus/restore checks remain before wider distribution. Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.

Installer: [aion2t-dps-setup-1.1.47-x64.exe](aion2t-dps-setup-1.1.47-x64.exe) (29,369,415 bytes).

SHA-256: `f12d3b501cc0d437253d29240b9fae0571647c3a1102510731757d1bffef29b6`.
