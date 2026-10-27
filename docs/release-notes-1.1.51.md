# Release 1.1.51

- Reduce DPS personal-detail work to one compact request and avoid copying unrelated combat history.
- Start optional overlay windows only when explicitly enabled in the current session. Preserve saved layout and selections; the launcher and background merchant service remain available. Closing Assist/notification overlays releases their WebViews.
- Reduce polling for hidden, empty or unconfigured Assist panels; cap countdown repainting. Boss cast and PvP update intervals are retained.
- Refresh merchant stock by its actual expiry, preserve queued categories across temporary readiness loss, and retry failed requests with bounded backoff. Share cached stock updates between consumers.
- Add an independent PvP button/window, plus configurable fade for the merchant and hidden-cube widgets.
- Keep compact pet progress (e.g. 4/105), show a larger price without a currency icon, and remove verbose waiting/cache-date text. Merchant card annotations are disabled pending further work.
- Retain the prior Premium merchant access, hotkey and hidden-cube direction fixes.

## Validation and remaining live checks

Native compile/tests, built frontend checks, bundled helper integrity and installer version checks are recorded in the release validation report. The helper previously passed 74 tests against its actual frozen modules; its binary is unchanged in this release.

No universal CPU reduction percentage is claimed. Compare total CPU and FPS after startup and during combat on the target machine. Fresh in-game stock rotation and PvP/fade behavior still need confirmation. Combat read projections changed; prior recorded damage parity checks passed. This build does not change damage formulas.

Installer: [aion2t-dps-setup-1.1.51-x64.exe](aion2t-dps-setup-1.1.51-x64.exe) (44,206,574 bytes).

SHA-256: `cf97dd396462d5968c5f4218e561455b56ddce65a5e33141c7fd97ba2e585f99`.
