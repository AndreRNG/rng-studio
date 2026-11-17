# Modifications

This is a modified version of PhotoCraft (https://github.com/storytold/photocraft) by the ArtCraft
team, modified by RNG Media S.L. in November 2026. It is not ArtCraft software and is not endorsed
by the ArtCraft team. PhotoCraft is licensed MIT OR Apache-2.0 (see LICENSE-MIT, LICENSE-APACHE and
NOTICE); the upstream copyright notices are kept intact.

Changed areas:

- Branding: the product is named PhotoFalcon; window, menu, title bar, About and start screen text,
  Windows installer, macOS Info.plist, Linux desktop, AppStream and nfpm metadata.
- App id is `media.rng.photofalcon` (Wayland/X11 app id, desktop file, AppStream id, Flatpak id, macOS
  bundle and document type ids, icon names). Settings and data directory names are unchanged.
- App icon replaced with the PhotoFalcon icon (PNG set, `.ico`, `.icns`).
- Default theme changed to a graphite "glass" look with a red accent (`crates/ui-egui/src/theme.rs`).
- Start screen: upstream community, Discord, tutorial and GitHub links removed; the blue badge is the
  app icon.
- Help menu: Discord, ArtCraft website, GitHub and Report an Issue items removed; the website item
  opens https://www.rng.media. The Contributors list no longer links out.
- Upstream self-update unplugged (no update service is registered; Help > Check for Updates removed
  from the menu).
- About window: credit line and a Licences tab showing the MIT, Apache-2.0 and NOTICE texts.
- User-visible "PhotoCraft" in translated strings is shown as "PhotoFalcon"
  (`crates/ui-egui/src/i18n.rs`).
- Wording about the ArtCraft Launcher removed from the AI agents preferences text and error message.
- Windows install folder is `RNG Media\PhotoFalcon`, with a new MSI UpgradeCode and manufacturer
  RNG Media S.L.
- README replaced; `MODIFICATIONS.md` added.
