# OpenWrt Device Ports

Community hardware enablement and reproducible OpenWrt porting notes for devices not yet supported upstream.

## Devices

| Device | SoC | Wireless | Status |
| --- | --- | --- | --- |
| [FREEFA AC1200M-U10](devices/FREEFA-AC1200M-U10/README.md) | MediaTek MT7628AN | 2.4 GHz integrated + MT7612EN 5 GHz PCIe | Custom OpenWrt build booted and tested; upstream submission pending |

## Project goals

- Document hardware identification, flash layouts and serial access.
- Publish reviewed, reproducible OpenWrt source changes and build instructions.
- Clearly separate **tested** installation procedures from **untested** recovery methods.
- Prepare device-specific contributions for the official OpenWrt source tree.

## Safety and provenance

Flashing third-party firmware can permanently damage a device. Verify the exact hardware revision, retain a full original flash backup and confirm a working recovery path before writing flash. Do not flash files intended for a different device.

The working FREEFA build was based on OpenWrt source commit `58584c6f2829a7e5d77376ab68aae3dcc4a392d8`. Its exact current source changes are being collected and reviewed before publication. No firmware image or installation command is offered here yet.

## Repository layout

Each device has its own documentation and upstream patch material under `devices/`. Device-specific OpenWrt contributions should ultimately be submitted as focused pull requests to upstream OpenWrt.

## Upstream

Official project: https://github.com/openwrt/openwrt
