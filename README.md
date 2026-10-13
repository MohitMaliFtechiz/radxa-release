# ROCK 4D MiloPlay kiosk firmware releases

Flashable firmware images for the Radxa ROCK 4D, built from the patches in
[MohitMaliFtechiz/radxa](https://github.com/MohitMaliFtechiz/radxa) (Android
14 / RK3576, MiloPlay kiosk mode). See that repo for the source changes,
build instructions, and full per-release verification notes.

## Flashing

Each release has two files, both `xz`-compressed — decompress with
`xz -d <file>` before flashing, and verify the decompressed file's SHA-256
against the hash listed on that release page before writing it to a device.

- **`update.img`** — flash via `upgrade_tool`/RKDevTool to eMMC or UFS.
- **`gpt.img`** — a raw disk image; flash via balenaEtcher (or `dd`) to a
  microSD card.

Both require the board's SPI bootloader to already be flashed first; see
[Radxa's ROCK 4D documentation](https://docs.radxa.com/en/rock4/rock4d) for
that one-time step and general flashing guidance.
