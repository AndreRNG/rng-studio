# Modifications

This is a modified version of DeckCraft (https://github.com/storytold/deckcraft) by the ArtCraft team, modified by RNG Media S.L. in November 2026. It is distributed as **SlideSeal** under the same terms as the original, MIT OR Apache-2.0 (see `LICENSE-MIT`, `LICENSE-APACHE` and `NOTICE`). SlideSeal is not made or endorsed by the ArtCraft team.

Changed areas:

- Branding: the app is called SlideSeal in the UI, window and dialog titles, About, menus, file dialogs, error messages, the CLI/MCP help, the web build page, and in files it writes (PDF creator/producer, PPTX `Application`, `.deckcraft` generator). Crate names, the `deckcraft` binary name, the `.deckcraft` file format and the built-in "DeckCraft" theme keep their upstream names so upstream changes merge easily.
- Icon and artwork: new SlideSeal app icon (PNG set, `.ico`, `.icns`, SVG), in-app logo, and macOS DMG background; the ArtCraft logos (`docs/brand/`) were removed.
- App id: `ai.storyteller.deckcraft` became `media.rng.slideseal` (Wayland app id, `.desktop`, AppStream metainfo, MIME file, Flatpak manifests, macOS bundle id). Settings, recovery and dictionary folders are unchanged.
- Theme: new graphite dark theme and red accent (`crates/ui-egui/src/theme.rs`).
- Network: automatic and manual update checks are disabled and the Help menu entry removed; the Flatpak manifests no longer request network or host-spawn access; AppImage update information is not embedded; the ArtCraft, GitHub and Discord links (Help, About, Home, CLI, MCP, installers, AppStream) were replaced by https://www.rng.media/; contributor names in Credits are plain text instead of GitHub links.
- Licences: About now has a Licences tab (also Help > Licences) showing the credit line and the embedded `LICENSE-MIT`, `LICENSE-APACHE` and `NOTICE`; the `NOTICE` trademark paragraph and `ATTRIBUTION.md` were updated; this file was added.
- Packaging: Linux (`.desktop`, metainfo, nfpm vendor/homepage/maintainer, AppImage, Flatpak), macOS (`Info.plist`, app/DMG names), and Windows (MSI product name, manufacturer, new UpgradeCode, install folder `RNGMedia\SlideSeal`, registry keys, ProgId) use SlideSeal names.
- `README.md` was replaced by a short SlideSeal README.
