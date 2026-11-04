# Release policy

Studio Pro is in early alpha and has **no public releases yet**. This page defines
the release contract for the first and subsequent builds. The source lives in
[`photo-pro`](https://github.com/ThatAerospaceandTechGuy/photo-pro).

## Tags

| Channel | Tag pattern | Latest release? |
| --- | --- | --- |
| Stable | `vMAJOR.MINOR.PATCH` | Yes, newest stable release |
| Pre-release | `vMAJOR.MINOR.PATCH-rc.N` | No |
| Development build | Compile from source | Not published here |

A pre-release must be marked as a pre-release on GitHub and must never become the
latest stable release. Tags are immutable once published.

## Planned packages

The source packaging scripts target:

| Platform | Planned packages |
| --- | --- |
| Windows 10+ | Installer and portable ZIP (x64, x86, arm64) |
| macOS 11+ | Universal DMG for Apple silicon and Intel |
| Linux | AppImage, `.deb`, `.rpm`, `.tar.gz` and Flatpak (x86_64 and aarch64) |
| FreeBSD | `.tar.gz` |
| Web | Static WebAssembly build |
| CLI | `studiopro-cli` binary where packaging supports it |

Exact asset names and compatibility notes will be listed before the first public
release. Do not rely on a package name until it appears in a published release.

## Checksums and signing

- Every public release must include a `SHA256SUMS.txt` covering all release
  assets.
- The release notes must state whether each package is signed and how to verify
  it.
- Unsigned early builds must be labelled clearly.
- Checksums must be published in the same release as the binaries.

## Publishing checklist

1. Build each platform package from a clean source checkout.
2. Test opening, editing and saving representative PSD, TIFF, PNG and JPEG files.
3. Test the CLI and automation surfaces separately from the desktop UI.
4. Generate and verify `SHA256SUMS.txt`.
5. Bundle the licence, `NOTICE` and `ATTRIBUTION.md` files.
6. Write release notes with known limitations and backup guidance.
7. Publish as a pre-release until the build meets the stability bar.
8. Verify every published asset URL and checksum.
9. Promote to a stable release only after the pre-release has been tested.

## Stability

Studio Pro is early alpha. Keep backups of important documents and do not treat a
pre-release as production software. Public releases will state their supported
platforms and known limitations; older releases are not patched unless a security
fix requires it.

## Security and support

Security reports follow [SECURITY.md](SECURITY.md). Product and release issues
follow [SUPPORT.md](SUPPORT.md).

## Scope

This repository is the public release home. The application source is not stored
here, and no binaries are available yet.
