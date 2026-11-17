# Modifications

This is a modified version of FilmCraft (https://github.com/storytold/filmcraft) by the ArtCraft team, modified by RNG Media S.L. in November 2026. It is distributed as CutCat. FilmCraft is licensed MIT OR Apache-2.0 (see LICENSE-MIT, LICENSE-APACHE and NOTICE); CutCat is not made, endorsed or supported by the ArtCraft team.

Changed areas:

- Branding: the app is called CutCat (window titles, menus, dialogs, file-dialog names, installers, desktop/AppStream/Info.plist/MSI metadata); app id `media.rng.filmcraft`; new CutCat icon and wordmark (`assets/app-icon/`, `assets/brand/`). ArtCraft marks are not used in the app or its packages.
- Interface and look: "glass" dark theme, segmented mode switcher, Tabler icons (`assets/icons/tabler/`, `crates/ui-egui/src/tabler_icons.rs`), rounded timeline clips, scrollbars and zoom behaviour, clip fade handles (`panels/timeline/fades.rs`), a Premiere-style Home screen, no demo-project button, no header community button.
- Preferences: "At Startup" defaults to Home on an empty project.
- Network: update checks (startup and Help menu) are disabled, the Help menu "Check for Updates", Discord, ArtCraft and GitHub links are removed, contributor names no longer link to GitHub, Flatpak builds request no network or host-update permissions. The only link is https://www.rng.media.
- Licences: About ▸ Licences shows the NOTICE, MIT and Apache-2.0 texts; NOTICE records the modifications.
- Packaging: Windows install folder `RNG Media\CutCat` with a new MSI UpgradeCode, macOS bundle `CutCat.app`, Linux maintainer/vendor RNG Media S.L.
- Translations: UI strings in all catalogs renamed from FilmCraft to CutCat; ArtCraft/Discord strings removed.

Internal names (crate names, the `filmcraft` binary, `.fcproj` format, data directories) are unchanged so upstream changes can be merged.
