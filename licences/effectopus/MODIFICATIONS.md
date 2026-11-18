# Modifications

This is a modified version of EffectCraft (https://github.com/storytold/effectcraft) by the ArtCraft team, modified by RNG Media S.L. in November 2026. It is distributed as **Effectopus** under the same terms as the original, MIT OR Apache-2.0 (see `LICENSE-MIT`, `LICENSE-APACHE` and `NOTICE`). Effectopus is not made or endorsed by the ArtCraft team.

Changed areas:

- Branding: the app is called Effectopus in the UI, window and dialog titles, About, menus, file dialogs, messages, the CLI/automation help, the web build, the Windows file properties and in files it writes. Crate names, the `effectcraft` binary name and the `.ecproj` file format keep their upstream names so upstream changes merge easily.
- Icon and artwork: new Effectopus app icon (PNG set, `.ico`, `.icns`, SVG wrappers, web favicon), in-app logo and macOS DMG background; the ArtCraft logos (`docs/brand/`) were removed.
- App id: `ai.storyteller.effectcraft` became `media.rng.effectopus` (Wayland app id, `.desktop`, AppStream metainfo, MIME file, Flatpak manifests, macOS bundle id). The settings folder is `Effectopus` (macOS, Windows) or `~/.config/effectopus` (Linux).
- Network: the automatic and manual update checks are disabled (no self-update); the Flatpak manifests no longer request network access; the header Discord/GitHub buttons were removed; the ArtCraft, GitHub and Discord links (Help, About, Home, error messages, installers, AppStream) were replaced by https://www.rng.media/. The Plug-in Library still fetches its community catalog, but only when the user presses Refresh.
- Licences: About has a Licences tab with the credit line and the embedded `NOTICE`, `LICENSE-MIT` and `LICENSE-APACHE`; `NOTICE` and `ATTRIBUTION.md` were updated; this file was added.
- Packaging: Linux (`.desktop`, metainfo, nfpm vendor/maintainer), macOS (`Info.plist`), and Windows (MSI manufacturer, new UpgradeCode, install folder `RNGMedia\Effectopus`, registry keys) use Effectopus / RNG Media names.
- `README.md` was replaced by a short Effectopus README.
