# Source inventory and upstream preparation

## Base source

The working OpenWrt source checkout was reported at:

`58584c6f2829a7e5d77376ab68aae3dcc4a392d8`

## Local changes observed

| Path | Git status | Role |
| --- | --- | --- |
| `target/linux/ramips/dts/mt7628an_freefa_ac1200m-u10.dts` | untracked | Hardware description |
| `target/linux/ramips/image/mt76x8.mk` | modified | Device image definition |
| `target/linux/ramips/mt76x8/base-files/etc/board.d/02_network` | modified | Switch and interface mapping |

The local checkout also contains temporary DTS backup variants and `.config.before-luci`. Those are investigation artifacts, **not** candidates for the upstream patch.

## Next steps

- [ ] Capture the current DTS and diffs for the two modified tracked files.
- [ ] Review GPIO, LED, switch-port and factory calibration mappings.
- [ ] Identify build configuration and image-size limits.
- [ ] Confirm current files match the tested firmware build, or clearly record differences.
- [ ] Prepare a minimal OpenWrt upstream patch.
- [ ] Perform a clean build and functional retest.

Do not publish private factory images or unreviewed flash commands.
