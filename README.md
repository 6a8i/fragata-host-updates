# Fragata Host updates

Update channel of [Fragata Host](https://github.com/6a8i/fragata-host): the package repositories used by the hosts
through `/etc/yum.repos.d/fragata.repo`.

- metadata and public key: GitHub Pages, `https://6a8i.github.io/fragata-host-updates/<version>/x86_64/`
  (branch `gh-pages`);
- packages: assets of the releases `packages-<version>-<build>`, one per build of a channel (`release.txt` of the
  channel names it; the first builds: `packages-<version>`);
- buildroot: the rebuilt packages the channel does not ship, which the builds of the channel install their build
  dependencies from (release `buildroot-<version>`, metadata under `buildroot-<version>/x86_64/`; unsigned, for
  builds only).

The packages are built from their sources (scripts/phase2 of fragata-host); those that do not build yet are the
upstream binaries. Every package and the repository metadata are signed by the Fragata Host key
([RPM-GPG-KEY-fragata](https://6a8i.github.io/fragata-host-updates/RPM-GPG-KEY-fragata),
fingerprint `99DB A3C8 83AC DAE7 189B  9714 4667 BAC6 840F 624B`).

The repositories are made and published by `scripts/packages` of
[fragata-host](https://github.com/6a8i/fragata-host/tree/main/scripts/packages).
