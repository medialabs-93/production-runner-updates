# Production Runner updates

This repository only holds the update feed (`latest.json`) and the installer downloads (GitHub Releases) for
Production Runner. The app reads `latest.json` to find out whether a newer version is available.

The feed is written with `tool/release_feed.dart` from the Production Runner repository (see `docs/UPDATES.md` there).
