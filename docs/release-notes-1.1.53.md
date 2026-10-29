# Release 1.1.53

- Keep process-owned game TCP streams independent, with separate reassembly and scoped state. Refresh capture filters as connections change, retain bounded ownership grace and open replacement capture handles before draining old ones. Closing one socket no longer resets every stream.
- Reduce Combat Assist snapshot, cooldown lookup and redraw work. Reduce repeated damage snapshot copies and background history, replay, map, widget and logging work.
- Restyle Combat Assist presets to match the app; make CP/GS and class selectors compact.
- Add Grave Rat to the merchant Rare selection.
- Hide empty personal DPS headings, statistics and the empty placeholder while retaining the settings button.
- Improve early owned loopback connection capture for merchant accelerator sessions; unsupported candidates no longer block later flows. This does not guarantee support for every VPN or accelerator.
- Retain the previous overlay, Premium, localization, preset, hotkey and cube-direction fixes.

## Validation

Build and installer version 1.1.53 and SHA-256 were checked. Previously completed native, recorded-data and browser validation was reused; no test suites were rerun for this packaging pass. Capture and combat paths changed: fresh live instance transitions, names, DPS and Combat Assist should be checked before broad publication. Live hourly merchant refresh and accelerator coverage remain unverified. No measured user FPS or memory improvement is claimed.

Installer: [aion2t-dps-setup-1.1.53-x64.exe](aion2t-dps-setup-1.1.53-x64.exe) (44,740,655 bytes).

SHA-256: `44b8eb59600e76fdb00dea4582a47a3bd9cac0606f4a85fe3faa031e5d684f3b`.
