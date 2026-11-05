<p align="center">
  <strong>Studio Pro</strong><br>
  A native suite for creative apps: Photo Pro for images, Audio Pro for sound, Effects Pro for motion graphics.
</p>

<p align="center">
  <img alt="Status: early alpha" src="https://img.shields.io/badge/status-early%20alpha-d69e2e?style=flat-square">
  <img alt="Platforms: Windows, macOS, Linux, FreeBSD and Web" src="https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20FreeBSD%20%7C%20Web-2f7bf5?style=flat-square">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white">
  <a href="LICENSES.md"><img alt="Licence: MIT OR Apache-2.0" src="https://img.shields.io/badge/licence-MIT%20OR%20Apache--2.0-2ea44f?style=flat-square"></a>
</p>

<p align="center">
  <a href="RELEASES.md"><img alt="Read the release policy" src="https://img.shields.io/badge/Release%20policy-Studio%20Pro-24292f?style=for-the-badge"></a>
  <a href="https://github.com/ThatAerospaceandTechGuy/studio-pro/issues"><img alt="Report an issue" src="https://img.shields.io/badge/Report%20an%20issue-GitHub%20Issues-0969da?style=for-the-badge"></a>
</p>

> [!IMPORTANT]
> **Studio Pro is in early alpha and has no public installers yet.** This
> repository is the public release home and issue tracker. The application source
> is maintained privately during early alpha. Watch the repository for the first
> build announcement.

Studio Pro is the suite. **Photo Pro** is its layer-based image editor for people
who want a native desktop application, real PSD files and local control. **Audio
Pro** is its waveform sound editor for WAV, MP3, FLAC and OGG audio. **Effects
Pro** is its motion-graphics and visual-effects editor for animated titles and
compositing. All three are built in Rust; Photo Pro uses a GPU compositor, Audio Pro uses native audio playback, and Effects Pro uses a GPU compositor.

## What it does

| | |
| --- | --- |
| **Image editing** | **Photo Pro** has Photoshop-style menus, shortcuts, panels and tools, including layers, masks, clipping masks, layer styles, adjustment layers, smart objects and smart filters. |
| **Motion graphics** | **Effects Pro** adds a layer-based compositor with keyframes, expressions, 3D cameras and lights, effects and a render queue. |
| **Sound editing** | **Audio Pro** opens WAV, MP3, FLAC and OGG, with waveform selection, playback, cut/copy/paste, trim, undo/redo, normalize, amplify, fades, reverse and 16-bit WAV export. |
| **Native performance** | Photo Pro's GPU compositor runs on wgpu (Metal, Vulkan, DirectX 12 and WebGPU), with copy-on-write tiles and multithreaded filters. None of the apps uses Electron or a webview on the desktop. |
| **Real files** | Photo Pro opens, edits and saves layered PSD and PSB documents, with round-trip coverage across a large real-world corpus. It also reads layered TIFF, Paint.NET PDN, OpenRaster, GIMP XCF, Krita KRA, Affinity documents (read-only) and SVG. |
| **Built for automation** | Every Photo Pro action is a command. Drive the same engine from the UI, the `studiopro-cli` command line, a JSON control channel or an MCP server. |

### Formats

PSD/PSB, layered TIFF, `.pcraft`, PDN, ORA, XCF, KRA, Affinity (read-only), SVG,
PNG, JPEG, TIFF, WebP, GIF, BMP, TGA, ICO, QOI, PNM, OpenEXR, Radiance HDR and
FITS. HEIC is available in official desktop builds; AVIF export is available with
the optional `avif` build feature.

### Colour and depth

RGB, Grayscale, CMYK and Lab documents at 8, 16 and 32 bits per channel, with ICC
colour management, Assign/Convert to Profile, soft proofing and gamut warning.

## Project status

| Item | Status |
| --- | --- |
| Apps | **Photo Pro** (images), **Audio Pro** (sound) and **Effects Pro** (motion graphics) |
| Public installers | **Not yet published** |
| Source code | Private during early alpha |
| Issue tracker | This repository |
| Licence | MIT **or** Apache-2.0, at your option |
| Desktop platforms | Windows, macOS, Linux and FreeBSD |
| Web | Photo Pro static WebAssembly build; Effects Pro web build in development |
| Stability | Early alpha — keep backups of important documents |

## Download and releases

There are **no public downloads yet**. When the first suite build is ready, this
repository will publish:

- platform packages for Photo Pro and Audio Pro on Windows, macOS, Linux and FreeBSD;
- Effects Pro announcements from its separate release home when that build is ready;
- a checksum file for every release;
- release notes and known limitations;
- the licence, notice and attribution files that ship with the binaries.

Release tags, asset naming, checksum and pre-release rules are documented in
[RELEASES.md](RELEASES.md). The source is maintained privately; public release
packages will be the supported way to use Studio Pro.

## Licence

Studio Pro is licensed under the **MIT License** or the **Apache License, Version
2.0**, at your option.

It is inspired by ArtCraft and retains the upstream copyright and licence
notices. The Studio Pro, Photo Pro, Audio Pro and Effects Pro names, application icons and
suite artwork are original to this project and are covered by the same terms. Studio
Pro is not affiliated with or endorsed by ArtCraft or its authors.

The licence texts and third-party notices are included in this repository:
[MIT](licenses/MIT.txt), [Apache-2.0](licenses/Apache-2.0.txt),
[NOTICE](NOTICE) and [ATTRIBUTION.md](ATTRIBUTION.md). See
[LICENSES.md](LICENSES.md) for the scope. Every binary release will bundle the
applicable notices.

The application source is maintained privately and is not distributed in this
repository.

## Security and support

- **Security reports:** follow [SECURITY.md](SECURITY.md). Do not post exploit
  details, credentials or malicious image files in a public issue.
- **Product and release support:** open an issue after reading
  [SUPPORT.md](SUPPORT.md).
- **Development updates:** watch the [releases page](https://github.com/ThatAerospaceandTechGuy/studio-pro/releases)
  for public build announcements.

## About this repository

This repository is the public release home and issue tracker for the Studio Pro
suite. It currently contains documentation only; it does not contain the
application source or public binaries.
