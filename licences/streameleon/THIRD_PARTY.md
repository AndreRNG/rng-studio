# Third-party code

Streameleon is written from scratch. No OBS Studio code (GPL-2.0) is used or copied. No GPL code is
linked into the binary.

## Rust crates (statically linked, all permissive)
Checked with `cargo metadata` on 2026-11-18: every crate is MIT, Apache-2.0, BSD-3-Clause, ISC,
Zlib, Unlicense, WTFPL or Unicode-3.0 (one crate is "MIT OR Apache-2.0 OR LGPL-2.1+", used under MIT).
Main ones:
- ashpd (MIT): xdg-desktop-portal ScreenCast
- pipewire / libspa (MIT): PipeWire bindings; stream setup follows the pipewire-rs examples (MIT)
- ffmpeg-next / ffmpeg-sys-next (WTFPL): FFmpeg bindings
- eframe / egui (MIT OR Apache-2.0): UI
- ab_glyph (Apache-2.0): text source rendering
- image (MIT OR Apache-2.0): image sources (PNG/JPEG/WebP)
- keyring (MIT OR Apache-2.0): stream key in the OS keyring
- rfd (MIT): file/folder pickers via the desktop portal
- serde, serde_json, chrono, tokio, parking_lot, anyhow, log, env_logger, ctrlc (MIT / Apache-2.0)

## Fonts
- Inter (SIL Open Font License 1.1), crates/app/assets/fonts/OFL-Inter.txt

## Design
- RNG design tokens (rng_design.rs) are RNG Media's own, shared across the app family.

## FFmpeg (LGPL-2.1+, dynamically linked only)
- Linux: links the system's libavcodec/libavformat/libavutil/libswscale at runtime. If the
  distro's FFmpeg includes libx264 the app can use it; we never ship x264.
- Windows/macOS builds (todo): bundle an LGPL-only FFmpeg build (`--disable-gpl
  --disable-nonfree`, shared libs, with libopenh264 BSD as the software H.264 encoder), plus the
  LGPL notice, the FFmpeg source offer and the exact configure line in the Licences screen.
- Hardware encoders used through FFmpeg: NVENC (nv-codec-headers, MIT), QSV (libvpl, MIT),
  AMF (MIT), VideoToolbox (system).
