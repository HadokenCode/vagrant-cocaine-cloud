# Yandex cocaine cloud for Vagrant

## Requirements

* Virtualbox
* Vagrant
* Ansible

## Usage

    vagrant up

Be calm - it can take time.

## Boxes

There are five boxes.

* `elliptics` holds one node of Reverbrain Elliptics. All other boxes uses
Elliptics as storage.
* `cocaine01` and `cocaine02` runs `cocaine-runtime`. Also, `cocaine-tools`
installed on both boxes
* `front` runs `cocaine-runtime` in gateway mode and `cocaine-native-proxy`
on port `8080`.
* `client` holds only `cocaine-tools`. Use for isolated scripts.

## Cluster control

To control cluster use `cluster.yaml`.

## Network

All `cocaine-runtime` nodes uses multicast for discovery. Also all nodes use
`mDNS` for dynamic host resolution.