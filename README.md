# open-design-linux (builder)

Builds unpacked Linux tarballs for the [`open-design-bin`](https://aur.archlinux.org/packages/open-design-bin) AUR package.

Upstream: https://github.com/nexu-io/open-design

## How it works

`build-linux` runs on schedule + manual dispatch (`version`, `upstream_tag`),
builds with `pnpm tools-pack linux build --to dir`, and publishes
`open-design-linux-x64.tar.gz` (+ `.sha256`) as a `v<version>` release asset.
The AUR package downloads that asset — no AppImage, no FUSE.

## Manual run

Actions → build-linux → Run workflow → `version: 0.21.1`,
`upstream_tag: open-design-v0.21.1`.
