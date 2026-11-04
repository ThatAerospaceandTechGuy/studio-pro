<p align="center">
  <strong>Studio Pro</strong><br>
  A native, open-source image editor built in Rust.
</p>

<p align="center">
  <img alt="Status: early alpha" src="https://img.shields.io/badge/status-early%20alpha-d69e2e?style=flat-square">
  <img alt="Platforms: Windows, macOS, Linux, FreeBSD and Web" src="https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20FreeBSD%20%7C%20Web-2f7bf5?style=flat-square">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-000000?style=flat-square&amp;logo=rust&amp;logoColor=white">
  <a href="LICENSES.md"><img alt="Licence: MIT OR Apache-2.0" src="https://img.shields.io/badge/licence-MIT%20OR%20Apache--2.0-2ea44f?style=flat-square"></a>
</p>

<p align="center">
  <a href="https://github.com/ThatAerospaceandTechGuy/photo-pro"><img alt="View the source" src="https://img.shields.io/badge/View%20the%20source-photo--pro-24292f?style=for-the-badge"></a>
  <a href="https://github.com/ThatAerospaceandTechGuy/studio-pro/issues"><img alt="Report an issue" src="https://img.shields.io/badge/Report%20an%20issue-GitHub%20Issues-0969da?style=for-the-badge"></a>
</p>

> [!IMPORTANT]
> **Studio Pro is in early alpha and has no public installers yet.** The source
> and development builds live in [`photo-pro`](https://github.com/ThatAerospaceandTechGuy/photo-pro).
> This repository is the public home for release downloads, release notes and
> issue tracking. Watch the repository for the first build announcement.

Studio Pro is a layer-based image editor for people who want a native desktop
application, real PSD files and local control. It is an independent fork of the
open-source **PhotoCraft** project, built with Rust and a GPU compositor. It is
not affiliated with or endorsed by the upstream project or its authors.

<p align="center">
  <img src="https://raw.githubusercontent.com/ThatAerospaceandTechGuy/photo-pro/main/docs/images/studiopro-demo.jpg" alt="Studio Pro editing a painting with type and adjustment layers" width="100%">
</p>

## What it does

| | |
| --- | --- |
| **Familiar editing** | Photoshop-style menus, shortcuts, panels and tools, including layers, masks, clipping masks, layer styles, adjustment layers, smart objects and smart filters. |
| **Native performance** | A GPU compositor on wgpu (Metal, Vulkan, DirectX 12 and WebGPU), copy-on-write tiles and multithreaded filters. No Electron or webview in the desktop app. |
| **Real files** | Open, edit and save layered PSD and PSB documents, with round-trip coverage across a large real-world corpus. Also reads layered TIFF, Paint.NET PDN, OpenRaster, GIMP XCF, Krita KRA, Affinity documents (read-only) and SVG. |
| **Built for automation** | Every action is a command. Drive the same engine from the UI, the `studiopro-cli` command line, a JSON control channel or an MCP server. |

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
| Public installers | **Not yet published** |
| Source code | [`photo-pro`](https://github.com/ThatAerospaceandTechGuy/photo-pro) |
| Issue tracker | This repository |
| Licence | MIT **or** Apache-2.0, at your option |
| Desktop platforms | Windows, macOS, Linux and FreeBSD |
| Web | Static WebAssembly build |
| Stability | Early alpha — keep backups of important documents |

## Download and releases

There are **no public downloads yet**. When the first build is ready, this
repository will publish:

- platform packages for Windows, macOS, Linux and FreeBSD;
- a checksum file for every release;
- release notes and known limitations;
- the licence, notice and attribution files that ship with the binaries.

Release tags, asset naming, checksum and pre-release rules are documented in
[RELEASES.md](RELEASES.md). The source repository is the only supported way to
build Studio Pro today.

## Build from source

Studio Pro needs a recent stable Rust toolchain; the workspace pins its version
in `rust-toolchain.toml`.

```sh
git clone https://github.com/ThatAerospaceandTechGuy/photo-pro.git "Studio Pro"
cd "Studio Pro"

# Desktop app
cargo run --release -p studiopro

# Headless CLI
cargo run --release -p studiopro-cli -- --help
```

On Linux, install the native build dependencies listed in the source
repository's [`docs/development.md`](https://github.com/ThatAerospaceandTechGuy/photo-pro/blob/main/docs/development.md).
Packaging scripts for macOS, Windows, Linux, FreeBSD and the web are under
[`packaging/`](https://github.com/ThatAerospaceandTechGuy/photo-pro/tree/main/packaging).

## Licence

Studio Pro is free software licensed under the **MIT License** or the **Apache
License, Version 2.0**, at your option.

It is derived from PhotoCraft and retains the upstream copyright and licence
notices. The Studio Pro name, application icon and fork-specific artwork are
original to this fork and are covered by the same terms. Studio Pro is not
affiliated with or endorsed by PhotoCraft or its authors.

The canonical licence texts, `NOTICE` and `ATTRIBUTION.md` are maintained in the
[source repository](https://github.com/ThatAerospaceandTechGuy/photo-pro). See
[LICENSES.md](LICENSES.md) for the scope. Every binary release will bundle the
applicable notices.

## Security and support

- **Security reports:** follow [SECURITY.md](SECURITY.md). Do not post exploit
  details, credentials or malicious image files in a public issue.
- **Product and release support:** open an issue after reading
  [SUPPORT.md](SUPPORT.md).
- **Source changes:** see the
  [source repository](https://github.com/ThatAerospaceandTechGuy/photo-pro).

## About this repository

This repository is the public release home and issue tracker for Studio Pro. It
currently contains documentation only; it does not contain the application
source or public binaries.
