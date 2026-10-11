# Factory firmware analysis and serial-console access

This document records the original-firmware investigation of the FREEFA AC1200M-U10. It deliberately does **not** publish factory login credentials.

## Verified observations

- The device provides a UART console at **57600 baud**.
- A complete factory SPI NOR image was backed up before any flash write.
- Firmware analysis produced a candidate factory login credential.
- The candidate was successfully tested on the original firmware over UART.

The exact extraction commands, matching offsets and firmware version have not yet been recovered into this repository. Accordingly, this is **not yet a reproducible credential-extraction tutorial**.

## Evidence to collect

1. Confirm the exact factory-image SHA-256 and image size.
2. Record filesystem discovery and extraction commands, tool versions and output.
3. Document the origin of the candidate credential without disclosing the credential itself.
4. Record a redacted serial-console transcript demonstrating the successful login.
5. Determine whether the credential is device-specific or shared across firmware versions, before deciding whether any disclosure is appropriate.

## Security and privacy

Never upload complete flash dumps, factory calibration partitions, private keys, configuration backups, MAC addresses tied to an individual device, or working credentials without a separate review.

## Relation to the port

Factory firmware access was useful during reverse engineering. The working OpenWrt installation was independently performed via a U-Boot/TFTP initramfs and sysupgrade workflow. Factory login credentials are **not** required by this repository's future public installation guide.
