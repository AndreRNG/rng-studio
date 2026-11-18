# Modifications

This is a modified version of VectorCraft (https://github.com/storytold/vectorcraft) by the ArtCraft team, modified by RNG Media S.L. in November 2026. It is distributed as **VectorViper** under the same terms as the original, MIT OR Apache-2.0 (see `LICENSE-MIT`, `LICENSE-APACHE` and `NOTICE`). VectorViper is not made or endorsed by the ArtCraft team.

Changed areas:

- Branding: the app is called VectorViper in the UI, window and dialog titles, About, menus, Home screen, file dialogs, error messages, the CLI/MCP help, the web build page, and in files it writes (PDF creator/producer, TIFF software tag, EMF description, `%%Creator` of EPS and AI files). Crate names, the `vectorcraft` binary name, the `.vectorcraft` file format (including the `generator` field and the markers inside PDF, EPS/AI and separation data that VectorCraft files carry), settings and data folder names, and Rust type names keep their upstream names so upstream changes merge easily and files stay compatible.
- Icon and artwork: the ArtCraft logos (`docs/brand/`) were removed. The app icon files are currently the upstream icon art under the VectorViper file names (placeholder until the VectorViper icon is added); the in-app mark is that same icon.
- App id: `ai.storyteller.vectorcraft` became `media.rng.vectorviper` (Wayland app id, `.desktop`, AppStream metainfo, MIME file, Flatpak manifests, icon file names, macOS bundle id). Settings, recovery and dictionary folders are unchanged.
- Theme: the accent colour is RNG red instead of coral (`crates/ui-egui/src/theme.rs`).
- Network: automatic and manual update checks are disabled and the Help menu entry removed; the Flatpak manifests no longer request network or host-spawn access; AppImage update information is not embedded; the Discord button (app bar, About, Home) and the ArtCraft, GitHub and Discord links (Help, About, Home, MCP, installers, AppStream) were removed or replaced by https://www.rng.media/; contributor names in Credits are plain text instead of GitHub links.
- Licences: About now has a Licences tab showing the credit line and the embedded `LICENSE-MIT`, `LICENSE-APACHE` and `NOTICE`; the `NOTICE` trademark paragraph, `ASSETS.md` and `AGENTS.md` were updated; this file was added.
- Packaging: Linux (`.desktop`, metainfo, nfpm vendor/homepage/maintainer, AppImage, Flatpak), macOS (`Info.plist`, app/DMG names), and Windows (MSI product name, manufacturer, new UpgradeCode, install folder `RNGMedia\VectorViper`, registry keys, ProgId) use VectorViper names.
- `README.md` was replaced by a short VectorViper README.
