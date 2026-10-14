# Security design

Proxframe controls hypervisors, so a hole in it is a hole in your lab. The full threat model comes with 0.7, after the next security review.

Sign-in uses your Proxmox account in whatever realm you have: PAM, Proxmox, LDAP, Active Directory or OpenID. Second factors work the way Proxmox handles them. Every action then runs as that user, Proxmox decides whether it is allowed, and the action appears in Proxmox's task log under their name. The hub's own read-only token feeds the live view and is never used for an action someone asked for, so each person sees only what their Proxmox permissions show. Hub passkeys can sit in front of sign-in, and risky actions ask for a fresh passkey or password check.

The connection from the hub to Proxmox always verifies the certificate; the hub pins your Proxmox certificate's fingerprint and stops talking to it if that changes. Every string from Proxmox, such as names, notes and task logs, is treated as untrusted text. The web app has no raw HTML sinks and ships a strict content security policy with Trusted Types. Sign-in routes have per-address limits so a stranger cannot lock the admin out, and secrets stay out of logs and error replies. Consoles pass through the hub on short-lived single-use grants.

Releases are signed, and the installer and updater refuse unsigned ones. The hub's service runs as its own user with a restricted set of system calls.

To report a problem, see [SECURITY.md](../SECURITY.md).
