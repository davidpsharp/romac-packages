# RoMac packages

The releases of [RISC OS on Linux](https://github.com/adyoull/RISCOSonLinux) (Andrew Youll's
work, built on RISC OS Open's sources) that [RoMac](https://davidsharp.com/romac) has been
tested with, kept here so they stay available after RISC OS on Linux's own package repository
has moved on. That repository keeps only the newest two builds of each package.

RoMac's Configure → Updates offers only the versions in `tested-releases` here (each RoMac
fetches it when it checks for updates), and checks each download against the SHA-256 given
there. These files are those downloads.

## Releases

- **`baseline-2026-11-16`**: what RoMac first shipped and was used with day to day:
  RISC OS on Linux release 1.0.0057 of 16 November 2026 (`riscos-rom` 5.31-29,
  `riscos-support` 1.0.0057-1, `riscos-harddisc` 1.0.0054-1). Only the parts RoMac uses:
  - `riscos-rom-5.31-29-RISCOS.IMG`: the RISC OS ROM image
  - `riscos-support-1.0.0057-1-native.zip`: `NativeSupport,ffa` and `NativeBoot,feb`
  - `riscos-harddisc-1.0.0054-1-HardDisc4.zip`: HardDisc4 (unpack on a Mac with
    `ditto -x -k FILE DIR`, which keeps RISC OS file types in the `,xxx` names)

  Taken unchanged from the release's own files (its `riscos-generic.img.xz`, SHA-256
  `490c9e1b96ad99e7bf907624ee38a5c63626079c411f6eb00a6ddf027d417a08`).
- **`debs-2026-11-21`**: RISC OS on Linux's own packages (`.deb`) for `riscos-rom`,
  `riscos-support` and `riscos-harddisc`, exactly as published in its package repository
  (https://adyoull.github.io/riscos-rolpkg), each checked against the SHA-256 in that
  repository's package lists when downloaded (18 and 21 November 2026).
  RoMac offers `riscos-rom` 5.31-30, `riscos-support` 1.0.0081-1 and `riscos-harddisc`
  1.0.0072-1 from here (since 22 November 2026): the first set with RISC3D, for 3D on the
  Mac's GPU.

Each release has a `SHA256SUMS` file; check with `shasum -a 256 -c SHA256SUMS`.

## Licences

These files are RISC OS on Linux's, redistributed unchanged. RISC OS on Linux's own files are
under the licence in `RISC-OS-on-Linux-LICENSE.txt`; RISC OS and the other components keep
their own licences, listed in `RISC-OS-on-Linux-LICENCES.md`. Only the RISC OS parts are here:
no Linux kernel or Debian system.

Questions about these copies: [RoMac's home page](https://davidsharp.com/romac).
