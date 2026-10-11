# Installation status and safety

**This is not yet a public installation procedure.** The device port worked on one tested unit, but the exact tested source files, hardware revision and repeatable build have not yet been independently reviewed.

## Verified sequence (high-level record)

1. Preserve multiple full original SPI NOR flash backups and verify their checksums.
2. Use the serial U-Boot console and TFTP to boot a custom OpenWrt initramfs without writing flash.
3. Confirm RAM boot, Ethernet and Wi-Fi hardware discovery.
4. From the verified initramfs, perform a deliberate sysupgrade to the custom firmware image.
5. Reboot and validate flash boot, writable overlay, Ethernet bridging, both radios and LuCI.

The flash write was performed only after explicit approval during testing. **Do not follow this outline as a command-by-command installation guide.** No public flash commands or images are provided until source provenance and recovery steps are reviewed.

## Recovery

The original complete flash image was backed up and verified, but full restoration was **not tested**. Recovery instructions must not be presented as proven until independently verified.

## Future work

Publish exact source diffs, build configuration, device photos and a reproducible installation guide with hardware revision checks and warnings.
