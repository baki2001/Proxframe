# Security

Report security problems privately: **Security → Report a vulnerability** on this repository reaches only me. Please do not open a public issue.

Include the version, the steps to reproduce and what you think the impact is. A description is enough, since there is no code here to patch against. I usually answer within 72 hours and aim to fix critical problems within 14 days. I work alone, so if I am away the answer can take longer, and I will say so.

In scope: sign-in and sessions, getting more access than the signed-in Proxmox user has, one user seeing another's data, console access, script injection through text that comes from Proxmox, the installer, and the update and release signing. Out of scope: bugs in Proxmox itself, which belong with Proxmox, and anything that needs an attacker who already controls the Proxmox host or the hub's container.

If you want to test the hub or installer, write to me first so we agree on how. I answer findings in public, with credit unless you prefer otherwise. I have no budget for a paid penetration test, and a free outside review would be welcome.

The design is described in [docs/security.md](docs/security.md).
