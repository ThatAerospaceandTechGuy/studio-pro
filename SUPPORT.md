# Support

Studio Pro is in early alpha and has **no public installers yet**. Support is
provided through GitHub issues on a best-effort basis. There is no account system,
support desk or guaranteed response time.

## Before you file

1. Read the [README](README.md) and [release policy](RELEASES.md).
2. Search [existing issues](https://github.com/ThatAerospaceandTechGuy/studio-pro/issues).
3. If you built from source, reproduce the problem from a clean checkout and note
   the commit.
4. Remove personal paths, document contents, credentials and other sensitive data
   from screenshots and logs.

## Open an issue

Use the [issue tracker](https://github.com/ThatAerospaceandTechGuy/studio-pro/issues)
and include:

- Studio Pro version or source commit;
- operating system, architecture and build profile;
- whether you used a release, a local build or the web build;
- the file format and, if possible, a minimal non-sensitive sample;
- exact reproduction steps;
- expected and actual behaviour;
- the complete error message, sanitized log or backtrace;
- any known workaround.

For build problems, include the failing command, the first useful error and the
Rust toolchain version. Do not paste an entire build log.

## Security reports

Do **not** open a public issue with exploit details or a malicious file. Follow
[SECURITY.md](SECURITY.md) and use the repository's private reporting channel.

## Source and releases

- Source code and build instructions: [`photo-pro`](https://github.com/ThatAerospaceandTechGuy/photo-pro).
- Public downloads: none yet. When packages are published, their assets, checksums
  and known limitations will be listed in [RELEASES.md](RELEASES.md).
- TCP, JSON and MCP automation are advanced surfaces. Include the exact command or
  request format when reporting a problem.

Product feedback and reproducible bug reports are welcome. Feature requests may be
closed if they are outside the current scope.
