# Roadmap

Versions in the order I plan to ship them. There are no dates. A version ships when its checks pass, and the next piece of work always comes from the lowest unfinished version. Fixes and read-only screens can ride along in any release.

| Version | What it adds | Status |
|---|---|---|
| 0.3 | One-click hub updates with automatic rollback | Shipped |
| 0.4 | New guest, Change, Try again, Show as command, node shell, node updates and disks, HA and replication | Shipped |
| 0.5 | Hub passkeys, recovery codes, WebAuthn, OpenID realms, a check before risky actions, signed releases | Shipped |
| 0.6 | Alerts to your own targets set up on Proxmox's notification system, the worth-a-look list, warnings before risky updates | Shipped |
| 0.7 | Guided first sign-in for a fresh install, my own security review of the hub and installer and a public threat model, fuzzing, the installer tested on fresh Proxmox 9.0 to 9.2 (single node and cluster), consoles checked on real nodes. Pulled forward into 0.7: backup restore with a restore test and a "last tested" date per guest, adding and removing disks and network cards, scheduled backup jobs, findings first on the Overview with an action on each, alerts from the hub's own findings, and a hub audit log | Next |
| 0.8 | Phone app for iOS and Android, biometric lock, several hubs, push notifications, Live Activities | Planned |
| 0.9 | Full guest editor, pending changes, raw config, cloud-init, guest agent, snapshot tree, clones, templates, scheduled snapshots | Planned |
| 0.10 | Migration preview, disks, guest firewall editing, restore, remote access page, host helper for temperatures and fans | Planned |
| 0.11 | Backup Server datastores, prune, verify, sync, tape, file restore, one Backups area for both products | Planned |
| 0.12 | Storage, disks, node network, DNS and time, package sources, certificates, guided ZFS disk replacement | Planned |
| 0.13 | Cluster create and join, HA rules, replication, SDN, firewall and access editing, notifications, backup jobs, pools, tags, Ceph | Planned |
| 0.14 | Accessibility audit, performance at scale, documentation, migration guide | Planned |
| 1.0 | Store releases, signed packages | Planned |

1.0 means parity with the Proxmox web interface. Everything used daily gets a hand-built screen, and forms generated from Proxmox's own API description cover the rest. The supported floor is Proxmox VE 9.0 and Backup Server 4.0.

After 1.0: reach from anywhere without open ports (testers decide whether it moves ahead of 0.8), several clusters in one view, reports, and Proxframe Clusters for k3s as a separate product in its own repository.

A waiting list is open at [proxframe.app](https://proxframe.app). The first 20 to 50 people come in after 0.7.

Before testers get in I run a security review of the hub and installer and publish what it finds and what I fix. I have no budget for a paid penetration test. A free outside review would be welcome.
