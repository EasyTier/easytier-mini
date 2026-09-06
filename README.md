# easytier-mini releases

This repository builds and publishes the compact
[`easytier-mini`](https://github.com/EasyTier/EasyTier/tree/main/easytier-contrib/easytier-mini)
client from the main EasyTier repository. The source code remains in
[`EasyTier/EasyTier`](https://github.com/EasyTier/EasyTier); this repository
contains release automation only.

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
