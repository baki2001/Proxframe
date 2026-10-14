# Changelog

Release notes, newest first. Fixes for running hubs ship as patch versions, and new features wait for the next minor version. What comes next is in the [roadmap](ROADMAP.md).

## 0.6.0, 14 October 2026

- Alerts: add, test, change and remove Proxmox notification targets and rules from Proxframe. They run on Proxmox's own notification system, so they keep working when no browser is open.
- Overview "worth a look": old or missing backups, filling storage, expiring certificates.
- Warnings before risky package updates on a node.
- Read-only cluster membership and quorum, resource pools, Ceph overview, and datacenter settings.
- A redesigned interface with a collapsible sidebar and one look for tables and settings pages.
- "Show as command" for clone, move, template download and snapshot rollback and delete.
- Security: per-address limits on sign-in routes so a stranger cannot lock the admin out, request and upload timeouts, step-up checks on more risky settings, stricter response headers, secrets kept out of logs and error replies.

## 0.5.0 to 0.5.3, 8 to 11 October 2026: sign in safely

- Hub passkeys in front of sign-in, recovery codes and a terminal QR for `hub admin recover`.
- WebAuthn second factor and OpenID realms.
- A passkey or password check before risky actions.
- Add server with one-time join tokens.
- Releases are signed (Ed25519) and the hub and installer refuse unsigned ones.

## 0.4.x, early October 2026

New guest, Change, Try again, Show as command, node shell, realms, sign out everywhere, recovery codes, node updates and disks, HA and replication.

## 0.3

The Update button: one-click hub updates with automatic rollback.
