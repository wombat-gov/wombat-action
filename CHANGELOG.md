# Changelog

All notable changes to this project are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
Because this project is still on `0.x`, a minor release may contain breaking
changes; this release is the coordinated WAFPass → WOMBATpass rebrand.

## [0.2.0] - 2026-11-02

### Breaking changes

- Moved the Action from `WAF2p/wafpass-action` to
  **`wombat-gov/wombat-action`**. Workflows must update the `uses:` reference
  and pin the new release.
- Renamed the inputs `wafpass_version` and `wafpass_source` to
  **`wombat_version`** and **`wombat_source`**.
- The canonical install source is now `wombat-core`; examples that used
  `WAF2p/pass.git` must use `wombat-gov/wombat-core`.

The legacy inputs `wafpass_version` and `wafpass_source` are still accepted as
deprecated aliases and are mapped to their `wombat_*` equivalents. They will be
removed in a future release.

### Changed

- README examples now reference `wombat-gov/wombat-action@v0.2.0`.
- Branding, workflow names and documentation use WOMBATpass/wombat.
- Package metadata and repository URLs point at the `wombat-gov`
  organisation.
- The release version is `0.2.0`.

### Migration

1. Change `uses: WAF2p/wafpass-action@v0.1.1` to
   `uses: wombat-gov/wombat-action@v0.2.0`.
2. Rename `wafpass_version` to `wombat_version` and `wafpass_source` to
   `wombat_source`.
3. If you override `wombat_source`, use a `wombat-core` source such as
   `git+https://github.com/wombat-gov/wombat-core.git`.
4. Pin `@v0.2.0` (or the exact commit SHA) for reproducible pipelines.

### Companion releases

- `wombat-core` 1.2.0
- `wombat-server` 1.2.0
- `wombat-dashboard` 1.2.0
- `wombat-mcp` 0.2.0
