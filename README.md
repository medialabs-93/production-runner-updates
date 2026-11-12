# Production Runner updates

This repository holds two things for Production Runner:

- **The installers**, as GitHub Releases (for example `Production-Runner-0.1.0.dmg` under `v0.1.0`).
- **The signed update feed** the app reads to find out whether a newer version exists:
  `pr-update.json` and its signature `pr-update.json.sig`, served by GitHub Pages at
  `https://medialabs-93.github.io/production-runner-updates/pr-update.json`.

The app only accepts a feed signed with a key it already trusts, and it checks every
installer it downloads against the checksum in that feed.

The feed is written and signed from the Production Runner repository
(`tool/make_update_feed.py`, then `tool/sign_update_feed.dart`; see `docs/UPDATE_FEED.md` there).
Both files are always replaced together, in one commit.
