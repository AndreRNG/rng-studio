# Modifications

This is a modified version of WordCraft (https://github.com/storytold/wordcraft) by the ArtCraft team, modified by RNG Media S.L. in November 2026. It is distributed as DocDuck under the original MIT OR Apache-2.0 licence; the original copyright notices are kept in [NOTICE](NOTICE), [LICENSE-MIT](LICENSE-MIT) and [LICENSE-APACHE](LICENSE-APACHE).

Changed areas:

- Name and branding: the product is called DocDuck; the dog icon replaces the WordCraft icon in every size (PNG, .ico, .icns, .svg); the ArtCraft logo files and README branding are removed; Discord, ArtCraft and GitHub links are replaced by https://www.rng.media or removed.
- App id: `ai.storyteller.wordcraft` is now `media.rng.docduck` (Wayland app id, desktop file, AppStream metainfo, Flatpak id, macOS bundle id, icon file names). Settings and data folders are unchanged.
- Interface (`crates/ui-egui`): DocDuck name throughout; red accent and a graphite dark theme; the Discord pill is off and replaced by an RNG Media website button; the Review ribbon Discord button is removed; About shows the DocDuck credit line and a new Licences tab (LICENSE-MIT, LICENSE-APACHE, NOTICE); contributor names are no longer links.
- Network: self-update is always off (Help > Check for Updates only explains this); the language-pack download backend is not started, so no pack or font downloads happen; the Flatpak no longer asks for network or host-Flatpak access; AppImage update info and Windows/AppImage update hooks no longer point at upstream.
- Engine and tools: user-visible messages, MCP server info (no community links), PDF creator/producer, LaTeX header comment, and sample document link say DocDuck / https://www.rng.media.
- Packaging (`packaging/`): Linux (.desktop, AppStream, nfpm, Flatpak, AppImage), macOS (bundle and DMG names, Info.plist), Windows (WiX package, registry names, install folder `RNG Media\DocDuck`, new UpgradeCode, version resource), FreeBSD; vendor RNG Media S.L.
- Not changed: crate names, module names, the `wordcraft` binary name and Rust identifiers (to keep merging upstream easy).
