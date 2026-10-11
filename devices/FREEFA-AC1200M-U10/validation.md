# Validation record — FREEFA AC1200M-U10

This page records observations on one unit; it is not a certification for other hardware revisions.

| Test | Result | Notes |
| --- | --- | --- |
| UART console | PASS | 57600 baud |
| TFTP initramfs boot | PASS | Kernel and userspace started |
| Sysupgrade from initramfs | PASS | Explicitly performed once |
| Boot from SPI NOR | PASS | U-Boot loaded flash kernel |
| Overlay persistence | PASS | Test file survived reboot |
| 2.4 GHz Wi-Fi | PASS | Client connectivity reported |
| 5 GHz Wi-Fi | PASS | Associated client observed, 80 MHz VHT, 2 streams |
| Bridged Ethernet AP | PASS | LAN and former WAN switch ports bridged |
| DHCP, DNS, internet | PASS | Tested through Windows ICS uplink |
| LuCI login | PASS | User confirmed |
| Full reboot / Wi-Fi persistence | PASS | User confirmed |
| Wireless repeater / WDS | NOT TESTED | Wired AP only |
| Original full-flash recovery | NOT TESTED | Backups exist; no destructive recovery test |

## Installed image references

Custom sysupgrade SHA-256:
`d46872185f00625caed128a6209f66066a4ffdf6764173c4ea4d37a8466d727e`

Custom initramfs SHA-256:
`e8e9b0cb6b9f649838e5c294bc83f3b3c9813f6c05a6b90078573664fe3c6828`

These hashes are for provenance only. The corresponding binaries have not been published or independently reproduced from the source files in this repository.
