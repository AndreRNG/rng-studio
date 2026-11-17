# Modifications

This is a modified version of PdfCraft (https://github.com/storytold/pdfcraft) by the ArtCraft team,
modified by RNG Media S.L. in November 2026. It is distributed as PDFrog under the original
licence, MIT OR Apache-2.0 (LICENSE-MIT, LICENSE-APACHE, NOTICE). PDFrog is not an ArtCraft product
and is not endorsed by the ArtCraft team.

Changed areas:

- Name and branding: the app is called PDFrog in the window title, title bar, Home, About, Help menu,
  dialogs, error messages, command labels, desktop/AppStream/MSI/macOS metadata and the PDF Producer
  entry. The ArtCraft name, wordmark and mark are removed, along with the ArtCraft/Discord community
  card, title-bar Discord button and Help links to ArtCraft, GitHub and Discord. The only link is
  https://www.rng.media.
- Icons: the PDFrog frog icon replaces the PdfCraft lion icon in every size and format (PNG, ICO,
  ICNS, SVG wrapper).
- App id: ai.storyteller.pdfcraft became media.rng.pdfrog (Wayland app id, .desktop, AppStream,
  Flatpak manifests, macOS bundle id). Icon, desktop, metainfo and Flatpak files were renamed to match.
  Settings and data folders keep their upstream names. Crate, module and binary names are unchanged.
- Network: the update check (at start and from the Help menu) and its preference are disabled, the
  AppImage update information is no longer embedded, and Contributors entries no longer link to
  GitHub profiles. The app makes no network requests on its own.
- About: new Licences tab showing the NOTICE, MIT and Apache-2.0 texts; credit line "PDFrog is based
  on PdfCraft by the ArtCraft team, licensed MIT OR Apache-2.0, modified by RNG Media S.L."
- Theme: graphite "glass" dark theme with a red accent (and red light accent), larger corner radius.
- Packaging: vendor/manufacturer/maintainer set to RNG Media S.L.; Windows install folder
  `RNG Media\PDFrog`; Explorer menu texts, shortcuts and registered-application names say PDFrog;
  macOS bundle name and credits updated.
- Documentation and legal: this file, NOTICE modification note, app-icon README/LICENSE and
  ATTRIBUTION entries for the new icon.
