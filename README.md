# unfriction — public releases

This repository distributes **versioned compiled binaries** of **unfriction**, a command-line tool for inspecting recorded AI coding-agent executions.

It is intentionally **not the application source repository**. The application source and its development history are private. Public binary archives, checksums, and release notes are available through **[GitHub Releases](https://github.com/unfriction-ai/unfriction-releases/releases)**. The Code tab can therefore contain little more than this README while the Releases page hosts downloadable artifacts.

## Install with Homebrew (recommended)

On an Apple Silicon or Intel Mac with [Homebrew](https://brew.sh/):

```sh
brew install unfriction-ai/tap/unfriction
unfriction --version
unfriction inspect --help
```

See the [Homebrew tap](https://github.com/unfriction-ai/homebrew-tap) for upgrading, testing, and uninstalling.

## Direct downloads and verification

Visit the [latest release](https://github.com/unfriction-ai/unfriction-releases/releases/latest) or [all releases](https://github.com/unfriction-ai/unfriction-releases/releases) and download the archive matching your macOS architecture.

Release archives follow these patterns (replace `<version>` with the selected release version, without the leading `v`):

| macOS architecture | Archive name pattern |
| --- | --- |
| Apple Silicon (arm64) | `unfriction_<version>_darwin_arm64.tar.gz` |
| Intel (amd64) | `unfriction_<version>_darwin_amd64.tar.gz` |

Each release also provides `checksums.txt`, containing SHA-256 hashes of its archives. Download it alongside the selected archive and calculate its checksum:

```sh
shasum -a 256 path/to/downloaded-archive.tar.gz
```

Compare the hash with the matching filename's entry in `checksums.txt`. If they differ, do **not** install that archive. The [Homebrew formula](https://github.com/unfriction-ai/homebrew-tap/blob/main/Formula/unfriction.rb) contains the checksum used by Homebrew for its currently configured release.

Archives contain the `unfriction` executable. Homebrew is recommended for installation, PATH management, and upgrades.

## Versions, features, and source

unfriction follows **Semantic Versioning**; release versions are determined from Conventional Commits. Supported trace formats and inspection capabilities may change between versions. Read the [latest release notes](https://github.com/unfriction-ai/unfriction-releases/releases/latest) for changes and run `unfriction inspect --help` for usage details in the installed binary.

The public distribution process does **not** publish the private source tree or its commit history. GitHub-generated source snapshots of this distribution repository are **not** the application's source code.

For installation instructions, see the [Homebrew tap](https://github.com/unfriction-ai/homebrew-tap).
