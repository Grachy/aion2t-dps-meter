# Release 1.1.43

## Performance

- Reduced background work. Closing a utility window releases its memory and background tasks; unused history polling and idle overlay drawing have been removed.
- Added **Full** and **DPS-only** performance profiles. DPS-only mode disables optional tools and collection work while keeping the meter available.
- **Premium:** customize which optional features run from a compact dropdown in performance settings. Saved choices are retained when Premium expires and restored when it becomes active again.
- Crowded PvP processing now focuses on combat involving you and your verified party or raid, reducing work on unrelated players.

## Mini-map and tracking

- Replaced separate Select all / Deselect all controls with one **ALL** toggle. Click it to select every eligible pet; click again to clear the selection.
- Added **Cogni, Natura, Varian and Fera** buttons in the same compact row. Each selects only that type in the current location. Type choices follow map changes, and individual checkboxes remain editable.
- At **100% transparency**, the active pet's soul progress stays visible as numbers such as **4/75**, without the name, icon or panel background. The four header buttons, player marker and selected pet/resource markers remain visible.
- Selecting pets filters both the progress list and their map markers.
- Added individual resource subtype choices, including **Gems: Ruby, Sapphire and Diamond**, and made resource/pet markers easier to distinguish.
- Added a configurable mini-map show/hide hotkey, default **Ctrl+Shift+M**, to Hotkeys settings. **Ctrl+M** locks or unlocks the mini-map; its tooltip shows the shortcut.
- The **free mini-map** shows all pets in the current location, with an opaque map and no resource markers. **Premium** enables transparency, pet/type selection, resource filters and display options. The full map remains available as before; saved advanced mini-map preferences are retained across Premium expiry.

## Combat, parties and raids

- Improved verified party/raid membership and membership changes, including raid subparties. Group views preserve their totals and player detail links.
- World-boss views better separate unrelated adds and retain players observed only through periodic damage.
- **AUTO** is now the default when no combat mode was previously saved. Existing saved mode choices are preserved.

## Interface and updates

- Added checklist activity visibility choices so you can hide routines you do not use.
- Added Appearance controls for footer element sizes.
- Compact world-boss respawn rows preserve boss names, shorten time labels and collapse alert selectors to arrows.
- Update prompts now use a separate window instead of resizing or being clipped inside the meter.
- Fixed restart after silent updates, including legacy update calls. Successful replacements restart once; fresh silent installs and prerequisite failures do not launch the meter automatically.

## Known limitations

- Some other players' ordinary damage on crowded world bosses is still not accounted for. This release improves grouping and scope but **does not guarantee a complete damage ranking**.
- Resource and pet spawn markers show known locations, not live availability. Map position accuracy still depends on the observations available from the game.
- Dense live Abyss combat, party/raid transitions, Premium expiry, physical hotkeys and the actual update flow still need live verification before wider distribution. Recorded checks are not a substitute for those tests.

## Validation and download

- **349 Rust tests passed; 7 skipped.**
- Release build, **23 obfuscated scripts**, and full browser checks passed, including the final assets after Rust's CSS processing.
- Checked the mini-map at **280 × 220**, ALL/type selection, saved preferences and soul progress updates under full transparency.
- Npcap prerequisite checks passed installed, missing and actual-driver cases in all **10 installer languages**.
- All **five** disposable tests of the generated installer restart callback and hooks passed.
- Native executable and installer metadata both report **1.1.43**; the application is **Windows x64**. The delivery copy matches the original installer hash.

Installer: [aion2t-dps-setup-1.1.43-x64.exe](aion2t-dps-setup-1.1.43-x64.exe) (26,007,321 bytes).

SHA-256: `c27c8a3ab196e35175997a91fd2e443d3fb6106c036e32e00789a8eaf7323933`.
