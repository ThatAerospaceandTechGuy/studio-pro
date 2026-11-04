# Security policy

Studio Pro processes complex image and document formats and exposes CLI, JSON
control and MCP automation. Treat files, paths, metadata, automation requests and
command parameters as potentially malicious.

## Supported versions

Studio Pro is in early alpha and has **no public installers yet**. The application
source is maintained privately. Once public builds are published, the current
stable release and the latest pre-release will be listed here as supported.

## Reporting a vulnerability

Please use GitHub's private vulnerability reporting from the repository's
[Security tab](https://github.com/ThatAerospaceandTechGuy/studio-pro/security).
If private reporting is unavailable, open a minimal public issue asking the
maintainers for a private channel; do not include exploit details.

Do not post a working exploit, secret, sensitive crash dump or malicious image in
a public issue. Give the maintainers a reasonable opportunity to investigate and
coordinate a fix before publishing details.

A useful report includes:

- the affected Studio Pro release asset and build identifier, if available;
- the operating system, architecture, build profile and relevant feature flags;
- the affected component, format or command;
- the security impact and required attacker access;
- exact reproduction steps;
- expected and actual behaviour;
- sanitized logs or backtraces;
- whether the problem reproduces from a clean download;
- any known workaround or containment.

Remove credentials, personal paths, private document content and unrelated system
information from logs.

## Scope

Reports are welcome for:

- PSD/PSB, raster, `.pcraft`, ICC, LUT, pattern and embedded-object parsing;
- decompression bombs, oversized dimensions, integer overflow, memory exhaustion,
  recursion or hangs;
- import/export and filesystem path handling, including traversal, symlinks and
  unsafe overwrite behaviour;
- engine command validation and serialization/deserialization;
- the desktop control server, headless JSON server, MCP server and MCP-to-GUI
  bridge;
- authentication, authorization, capabilities, request and batch limits;
- GPU resource validation and driver-facing input handling;
- dependencies, CI, packaging, signing, checksums and release integrity.

General bugs without a security impact belong in the normal issue tracker.

## Current limitations

TCP control connections require a 256-bit bearer token before method dispatch and
enforce request-line, active-connection and batch-step limits. Authentication does
not provide per-client or per-tool capabilities, so an authenticated client still
receives the exposed control surface. Remote filesystem methods use separately
configured read and write workspace roots, and engine commands that use ambient
filesystem paths are denied at the automation boundary. Automation can change
individual safe preferences, but whole-preferences updates and
filesystem-bearing preference sections are refused; applying the Preferences
dialog through automation is also refused. JSON-depth, render, document-memory,
command-duration, client-identity, encryption and audit controls are not yet
implemented. The detailed source-backed security review is maintained privately.

## Safe testing

Test only against your own installation and data. Do not target other users,
GitHub infrastructure, the product site or third-party services. Do not attach
potentially harmful or non-redistributable files to a public issue.
