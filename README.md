# NixOS-Infect for PhoenixNAP's Bare Metal Cloud

This is a fork of [nixos-infect](https://github.com/elitak/nixos-infect) with
modifications to work on [PhoenixNAP](https://phoenixnap.com)'s "Bare Metal Cloud"
product. The main addition is network config conversion from netplan to NixOS, handling
the bonding and vlan setup used by PhoenixNAP.

This has been tested on Ubuntu installations with SSD and NVMe disks, dual-gigabit
and dual-10-gigabit ethernet interfaces.

Set the `PROVIDER` environment variable to `phoenixnap-bmc` to activate this mode.

See the [original readme](./README.orig.md) for more usage instructions. One day this may
get merged back into mainline `nixos-infect` but for now its modifications are too
significant and it drags in extra dependencies (e.g. `jq`) unnecessary for users of
other providers.
