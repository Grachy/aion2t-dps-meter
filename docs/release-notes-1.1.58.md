# Release 1.1.58

- Correct multi-hit statistics using recorded chain events, and improve skill-use counts, critical-rate analysis, damage ranges and healing details. Older fights without the required data show unavailable metrics instead of misleading values; saved damage totals are not rewritten.
- Add persistent column settings to the fight-details gear menu. Move critical-rate mode and the option to hide skills with exactly 100% critical hits onto the Skills page; hiding rows preserves fight totals.
- Refine the fight-details layout and keep expanded skill evidence collapsed until requested.
- Add a dedicated Nightmare category to fight history and a Fight history button beside replays in the module overlay.
- Keep boss skill variants distinct in Combat Assist. Enable boss cast alerts during first Premium setup while preserving subsequent user choices.
- Separate the per-character 4-charge and per-server 16-charge morphed-energy counters in the full and compact checklists.
- Reduce merchant background processing, bound pending work and improve session cleanup and shutdown handling while retaining automatic stock checks.
- Reduce packet-buffer copying and fight-details rendering work, and bound detail caches.
- Retain the installer language selector and localized display-mode notice introduced in 1.1.57.

Installer: [aion2t-dps-setup-1.1.58-x64.exe](aion2t-dps-setup-1.1.58-x64.exe) (44,875,609 bytes).

SHA-256: ade0d62c43f6699ced0320b934510664ec66e210205d026deb45f36178ddafed
