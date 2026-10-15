# CCS Task Tracker

Single-page prototype of an office request desk for the college (v2.5).

**Live:** https://zefanonuevo.github.io/ccs-task-tracker/ (or open `index.html` in a browser while online)

- Demo sign-in accounts for requesters, coordinator, dean, and office assistants (password: `demo`)
- Service catalog with working-hours SLA tracking, ticket board, time tracker, evaluations
- All data is simulated in the browser; nothing is stored or sent anywhere

## Version history

Every version since the start is in [CHANGELOG.md](CHANGELOG.md) and in the app on the **Versions** tab. It also opens from the sign-in screen.

## Design system

macOS-style design: neutral surfaces, one blue accent, system font stack, frosted toolbar, segmented tabs, and a System, Light or Dark theme switch.

Colors, shadows, easing, type and the theme switch styles load from the shared stylesheet in [ccs-design](https://github.com/zefanonuevo/ccs-design), which [ccs-scgss](https://github.com/zefanonuevo/ccs-scgss) also uses, so the two can later be merged into one site. Only the chart and status colors are defined in this file.

The page needs a network connection to load that stylesheet. Opened offline, it loses its colors.
