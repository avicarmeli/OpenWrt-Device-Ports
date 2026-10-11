# FREEFA AC1200M-U10 — OpenWrt port

**Status:** Custom OpenWrt build installed to SPI NOR and tested as a wired bridged access point. **Not yet merged upstream.**

## Identified hardware

| Component | Observed |
| --- | --- |
| SoC | MediaTek MT7628AN |
| RAM | 64 MiB |
| Flash | 8 MiB SPI NOR |
| 2.4 GHz | Integrated MT7628 wireless (mt76 driver) |
| 5 GHz | MediaTek MT7612EN PCIe (mt76 driver) |
| Serial console | UART, 57600 baud |
| Hardware revision | Not independently established |

## Factory flash layout

| MTD | Offset | Size | Name |
| --- | --- | --- | --- |
| mtd0 | 0x000000 | 0x030000 | u-boot |
| mtd1 | 0x030000 | 0x010000 | config |
| mtd2 | 0x040000 | 0x010000 | factory |
| mtd3 | 0x050000 | 0x7b0000 | firmware |

These values describe the **observed factory layout**. Preserve calibration data in the factory partition. Never reuse another unit's flash backup as an installation image.

## Working build and validation

OpenWrt source base commit: `58584c6f2829a7e5d77376ab68aae3dcc4a392d8`.

The following were validated on the tested unit:

- Boot from an initramfs image via U-Boot/TFTP.
- Installation of the custom sysupgrade image from initramfs.
- Boot from SPI flash and persistent JFFS2 overlay across reboot.
- 2.4 GHz and 5 GHz access point operation using mt76.
- Wired bridged AP networking, upstream DHCP, DNS and internet access.
- LuCI management, credentials and restart persistence.

**Scope:** The final configuration is a **wired AP**, not a tested wireless repeater or wireless mesh backhaul.

## Source publication status

The tested device changes comprise a DTS, a device entry in `target/linux/ramips/image/mt76x8.mk`, and network board configuration in `target/linux/ramips/mt76x8/base-files/etc/board.d/02_network`. Their exact current content has not yet been collected for review. No unverified DTS, binaries or flash instructions are published here.

See [validation](validation.md) and [installation safety](installation.md).

## Upstream checklist

- [ ] Review and publish the exact tested DTS and board patches.
- [ ] Confirm hardware identifiers, MAC addresses, factory calibration offsets and LED/button mappings.
- [ ] Rebuild cleanly from documented sources and compare expected artifacts.
- [ ] Check OpenWrt contribution conventions and image size constraints.
- [ ] Submit a focused upstream pull request.
