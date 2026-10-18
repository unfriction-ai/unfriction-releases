# unfriction — public releases

This repository publishes **versioned compiled binaries** of **unfriction**, an experimental CLI for inspecting recorded AI coding-agent runs.

It is intentionally **not the application source repository**. The source and its development history are private; this public repository hosts release archives, checksums, and release notes through **[GitHub Releases](https://github.com/unfriction-ai/unfriction-releases/releases)**. Consequently, the repository's Code tab can contain little more than this README while its Releases page contains the distributable files.

## Install with Homebrew (recommended)

On an Apple Silicon or Intel Mac with [Homebrew](https://brew.sh/):

```sh
brew install unfriction-ai/tap/unfriction
unfriction --version
```

The initial release, **v0.1.0**, has been installed successfully using the [public Homebrew tap](https://github.com/unfriction-ai/homebrew-tap). For upgrading, testing, and removing the CLI, see the [tap's installation instructions](https://github.com/unfriction-ai/homebrew-tap#readme).

## Direct downloads and verification

The v0.1.0 release is packaged as:

| macOS architecture | Release archive |
| --- | --- |
| Apple Silicon (arm64) | `unfriction_0.1.0_darwin_arm64.tar.gz` |
| Intel (amd64) | `unfriction_0.1.0_darwin_amd64.tar.gz` |

The release also includes `checksums.txt` with SHA-256 hashes. Download the archive for your architecture and the checksum file from the [v0.1.0 release](https://github.com/unfriction-ai/unfriction-releases/releases/tag/v0.1.0), then verify the downloaded archive against the published checksum:

```sh
shasum -a 256 unfriction_0.1.0_darwin_arm64.tar.gz
```

Compare the output to the matching entry in `checksums.txt` (or the [Homebrew formula](https://github.com/unfriction-ai/homebrew-tap/blob/main/Formula/unfriction.rb) for the currently published version). Intel users should substitute the `darwin_amd64` archive. A mismatch means the file should not be installed.

An archive contains the `unfriction` executable. Homebrew is the recommended way to put it on your PATH and manage upgrades.

## Versioning and availability

unfriction uses **Semantic Versioning** with releases generated from Conventional Commits. The release process publishes macOS arm64/amd64 binaries and their checksums without exposing the private source tree or commit history. GitHub's auto-generated source snapshots of **this distribution repository** are not the application's source.

The current walking skeleton supports inspecting a single Codex turn without tool calls; later trace formats and acquisition analysis will be released as those features are implemented.

For installation and usage, see the [Homebrew tap](https://github.com/unfriction-ai/homebrew-tap). For available published versions, use the [Releases page](https://github.com/unfriction-ai/unfriction-releases/releases).
