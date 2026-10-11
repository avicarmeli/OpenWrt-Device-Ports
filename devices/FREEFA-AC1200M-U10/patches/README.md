# FREEFA AC1200M-U10 — Source changes

The working port was built from OpenWrt source commit `58584c6f2829a7e5d77376ab68aae3dcc4a392d8`.

The locally generated patch was reviewed and contains **177 lines** across three paths:

- `target/linux/ramips/dts/mt7628an_freefa_ac1200m-u10.dts` (new device tree)
- `target/linux/ramips/image/mt76x8.mk` (device image definition)
- `target/linux/ramips/mt76x8/base-files/etc/board.d/02_network` (switch ports)

## Confirmed build settings

- Board compatible: `freefa,ac1200m-u10`
- Device vendor/model: FREEFA AC1200M-U10
- Image limit: `7872k`
- Additional package: `kmod-mt76x2`
- Switch port configuration: `1:lan`, `4:wan`, `6@eth0`
- SPI NOR: 8 MiB; factory partition at `0x40000`; firmware at `0x50000`
- PCIe MT7612EN EEPROM: factory offset `0x8000`
- Integrated 2.4 GHz radio EEPROM: factory offset `0x0`

## Validation

The owner confirms the port was compiled, flashed, rebooted and tested successfully, including both wireless radios, wired Ethernet bridging and persistent configuration.

Some comments in the DTS still describe the port as uncompiled/untested and some GPIO mappings as provisional. Those comments are stale or narrower than the overall functional validation; they should be reviewed during upstream patch cleanup, not taken to mean the entire device port failed testing.

## Source preservation

The exact 177-line patch has been exported locally as `freefa-changes.patch`. **The complete patch has not yet been committed here.** Its contents should be committed verbatim in a subsequent step, before any upstream PR. Do not substitute this summary for source code.
