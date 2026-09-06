# easytier-mini releases

This repository builds and publishes the compact
[`easytier-mini`](https://github.com/EasyTier/EasyTier/tree/main/easytier-contrib/easytier-mini)
client from the main EasyTier repository. The source code remains in
[`EasyTier/EasyTier`](https://github.com/EasyTier/EasyTier); this repository
contains release automation only.

## Quick downloads

The current build is the
[`v2.7.0-preview.2`](https://github.com/EasyTier/easytier-mini/releases/tag/v2.7.0-preview.2)
development preview. Choose your platform below to download it directly.

| System | Architecture | Download |
| --- | --- | --- |
| Linux | x86-64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-x86_64-v2.7.0-preview.2.zip) |
| Linux | AArch64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-aarch64-v2.7.0-preview.2.zip) |
| Linux | RISC-V 64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-riscv64-v2.7.0-preview.2.zip) |
| Linux | LoongArch64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-loongarch64-v2.7.0-preview.2.zip) |
| Linux | ARMv7 hard float | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-armv7hf-v2.7.0-preview.2.zip) |
| Linux | ARMv7 soft float | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-armv7-v2.7.0-preview.2.zip) |
| Linux | ARM hard float | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-armhf-v2.7.0-preview.2.zip) |
| Linux | ARM soft float | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-arm-v2.7.0-preview.2.zip) |
| Linux | MIPS | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-mips-v2.7.0-preview.2.zip) |
| Linux | MIPSEL | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-linux-mipsel-v2.7.0-preview.2.zip) |
| FreeBSD 14+ | x86-64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-freebsd-14-x86_64-v2.7.0-preview.2.zip) |
| macOS | x86-64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-macos-x86_64-v2.7.0-preview.2.zip) |
| macOS | Apple Silicon | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-macos-aarch64-v2.7.0-preview.2.zip) |
| Windows | x86-64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-windows-x86_64-v2.7.0-preview.2.zip) |
| Windows | x86 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-windows-i686-v2.7.0-preview.2.zip) |
| Windows | ARM64 | [Download](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/easytier-mini-windows-arm64-v2.7.0-preview.2.zip) |

[Browse all releases](https://github.com/EasyTier/easytier-mini/releases) or
[download `SHA256SUMS`](https://github.com/EasyTier/easytier-mini/releases/download/v2.7.0-preview.2/SHA256SUMS)
to verify an archive.

## Release contents

Each release contains `easytier-mini` for the same non-GUI targets as the
EasyTier Core workflow:

- Linux: x86-64, AArch64, RISC-V 64, LoongArch64, ARMv7 hard/soft float,
  ARM hard/soft float, MIPS, and MIPSEL
- FreeBSD x86-64
- macOS x86-64 and Apple Silicon
- Windows x86-64, x86, and ARM64

Windows archives also contain the matching `wintun.dll`. Every release links
to the exact EasyTier source commit and includes SHA-256 checksums.

## Publishing a release

Run the **Release easytier-mini** workflow and provide:

- `source_ref`: an EasyTier tag, branch, or commit
- `release_tag`: the tag to create in this repository
- `prerelease`: whether the release is a development preview

Stable releases must use the same tag as the corresponding EasyTier release,
and the tag must match the version declared by the `easytier-mini` crate.
Prereleases may build an explicitly recorded development commit.
