# Quality and testing

Proxframe is built with AI assistance. The weight sits on rules and checks that run on every change, so this page lists them.

The rules are short. API types for Proxmox are generated from its published API description and never typed by hand, and the same goes for the parsers for values like `net0` or `scsi1`. Browsers and phones only talk to the hub. Web components never fetch or poll; data arrives through one query layer fed by a live stream. Every screen that shows data has a designed state for loading, empty, error and no permission. Every architectural decision gets a written decision record in the same change. No test is ever skipped, loosened or deleted to get a change through, and any test change has to be explained.

Each change then runs through formatting, lint, type checks and unit tests for the Rust hub and the web app, a dependency licence and advisory check (plus a weekly advisory sweep), secret scanning and a size budget for the web bundle. Integration tests run against a simulator of the Proxmox API, and before a release against a real Proxmox with a restricted test user and a sandbox pool. The security tests cover script injection through every string that comes from Proxmox, property tests for the per-user permission filter, and hostile Proxmox answers. A second, independent review runs on every change before it merges.

Releases are built in their own job and signed with an Ed25519 key. The installer and the updater refuse an unsigned release, and the hub rolls itself back if a new version does not answer after an update.

The hub has had one security and code review so far: no critical or high findings and five medium ones, all fixed. Another runs before testers get in and again every couple of releases. I have no budget for a paid penetration test, and a free outside review would be welcome.
