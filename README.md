# server-baseline image v1 (Debian 13 netinst + preseed)

**⚠ WARNING: booting this ISO ERASES THE FIRST DISK without asking.** It is a fully automatic installer meant for one empty VPS of
its owner. Do not boot it on a machine with data.

- Base: official `debian-13.7.0-amd64-netinst.iso` (sha256 `a7ef94ac2fb9a7fec454552abd629b7cc9d5155c886165a45649f5ce6167e355`,
  signature checked against the Debian CD signing key at build time).
- Changes: `/preseed.cfg` added to the installer initrd; isolinux boots the automatic install by default (3 s timeout).
- The installed system: a TEMPORARY user `godzilla` with a locked password and one temporary SSH public key (both replaced right
  after installation), root login and password login disabled
  in sshd, `openssh-server sudo` + `standard`, security updates enabled, powers off when done.
- No secrets inside: no passwords, no private keys.

The ISO is attached to the release; its SHA-256 is in `SHA256SUMS` there.
