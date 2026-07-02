```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:deb (ubuntu 25.10) 
│     ├ Class          : os-pkgs 
│     ├ Type           : ubuntu 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0]   ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : bsdextrautils@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdextrautils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 847428c8a544f66d 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e93c77687887070cbc3d42d0d5fa3884f0af9b8f4224864929aa
│                       │       │                   e10887f6b9ae 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [1]   ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : bsdextrautils@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdextrautils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 847428c8a544f66d 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0841243ebd9fb187bc76b858e640cc8a8f1d617eb8a9e63ea095
│                       │       │                   0c92456a223f 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [2]   ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 411fc06346b75c80 
│                       │       ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:efb87ca3683745936d0367bc8657b19cc6c6ab92c57c2a46206b
│                       │       │                   a4c6d6bf48e5 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [3]   ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 411fc06346b75c80 
│                       │       ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:dd33786fde5dba2e4b0280889fdeb9639b421c95904eb627ff3c
│                       │       │                   a4ae6625d222 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [4]   ╭ VulnerabilityID : CVE-2026-11856 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-11856 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bc3ed6e41589073417e21d614504f69ec1e6a6ca348ee74edb64
│                       │       │                   8d43987f8885 
│                       │       ├ Description     : Successfully using libcurl to do a transfer to a specific
│                       │       │                   HTTP origin (`hostA`) with **Digest** authentication and
│                       │       │                   then changing the origin to a different one (`hostB`) for a
│                       │       │                    second transfer, reusing the same handle, makes libcurl
│                       │       │                   wrongly pass on the `Authorization:` header field meant for
│                       │       │                    `hostA`, to `hostB`. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-11856.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-11856 
│                       ├ [5]   ╭ VulnerabilityID : CVE-2026-8925 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8925 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e7fe23649cb440a27c33142f96eca03bd54f037432c0f35b14bb
│                       │       │                   a8ad092f9214 
│                       │       ├ Description     : The curl logic that works with SASL authentication could
│                       │       │                   end up cleaning up the GSASL context *twice* without
│                       │       │                   clearing the pointer in between, making it `free()` the
│                       │       │                   same pointer twice. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8925.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8925 
│                       ├ [6]   ╭ VulnerabilityID : CVE-2026-8927 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8927 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:cff45ae3ad3a073d7f3fc24fc5eed3db441327251d86316d8e51
│                       │       │                   ca68b46a6632 
│                       │       ├ Description     : When reusing a libcurl handle for sequential transfers
│                       │       │                   driven by environment-variable proxy configuration, libcurl
│                       │       │                    fails to clear the proxy authentication state between
│                       │       │                   requests. Specifically, if the initial transfer
│                       │       │                   authenticates against `proxyA` using Digest auth, a
│                       │       │                   subsequent transfer routed through `proxyB` erroneously
│                       │       │                   leaks the `Proxy-Authorization:` header intended solely for
│                       │       │                    `proxyA`. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8927.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8927 
│                       ├ [7]   ╭ VulnerabilityID : CVE-2026-9079 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9079 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:c9f9c4d51bea34b9f708a557106a3ff3ead52fcd14e4b00009f7
│                       │       │                   58d30d35cf31 
│                       │       ├ Description     : libcurl had a flaw that when instructed to clear proxy
│                       │       │                   authentication credentials which made it not do so, leaving
│                       │       │                    the old credentials around to get used for subsequent
│                       │       │                   tranfers that should not know nor use them. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9079.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9079 
│                       ├ [8]   ╭ VulnerabilityID : CVE-2026-10536 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-10536 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:100be96c263bcf1ee572dfda31af9bf79b9e09ba4b75dd9836d9
│                       │       │                   6f3569052e93 
│                       │       ├ Description     : A use-after-free vulnerability exists in libcurl when an
│                       │       │                   application configures an HTTP/2 stream-dependency tree via
│                       │       │                    `CURLOPT_STREAM_DEPENDS` or `CURLOPT_STREAM_DEPENDS_E`,
│                       │       │                   subsequently invokes `curl_easy_reset()`, and finally
│                       │       │                   terminates the handle with `curl_easy_cleanup()`. During
│                       │       │                   this final cleanup phase, libcurl attempts to access and
│                       │       │                   modify an internal structure that was already deallocated
│                       │       │                   during the reset operation. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-10536.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-10536 
│                       ├ [9]   ╭ VulnerabilityID : CVE-2026-12064 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-12064 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:589de41abe6ad0d3ff862e76cc78e08a95e78beecdded4a09c6b
│                       │       │                   f6683dd47e27 
│                       │       ├ Description     : When a user invokes curl using a schemeless URL combined
│                       │       │                   with `--proto-default` sftp (or scp), a disconnect occurs
│                       │       │                   between the tool layer and libcurl. The tool layer
│                       │       │                   incorrectly infers the URL scheme, which erroneously
│                       │       │                   bypasses the initialization of critical SSH security
│                       │       │                   options like CURLOPT_SSH_HOST_PUBLIC_KEY_SHA256 and
│                       │       │                   CURLOPT_SSH_KNOWNHOSTS. Conversely, the libcurl runtime
│                       │       │                   successfully honors CURLOPT_DEFAULT_PROTOCOL and
│                       │       │                   establishes the connection via SFTP/SCP as specified.
│                       │       │                   Because the tool layer skipped the security configuration,
│                       │       │                   these SSH host verification options are silently omitted,
│                       │       │                   causing curl to connect to an unverified SSH remote host
│                       │       │                   without throwing an error. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-12064.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-12064 
│                       ├ [10]  ╭ VulnerabilityID : CVE-2026-8286 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8286 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e3f82ab1468903b5919ee4955008a25686aba32569b4eed02bc2
│                       │       │                   45eee0107b2d 
│                       │       ├ Description     : A vulnerability exists where a new transfer that uses
│                       │       │                   STARTTLS to upgrade the connection might reuse an existing
│                       │       │                   live connection even though the TLS configuration
│                       │       │                   mismatches so it should not. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8286.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8286 
│                       ├ [11]  ╭ VulnerabilityID : CVE-2026-8458 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8458 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:125db0eaa511829b521a9d8c7743d0fd3e9fa2f124d04ead3270
│                       │       │                   f492c93c4919 
│                       │       ├ Description     : libcurl might in some circumstances reuse the wrong
│                       │       │                   connection when asked to do Negotiate-authenticated ones,
│                       │       │                   even when they are set to use different "services". libcurl
│                       │       │                    features a pool of recent connections so that subsequent
│                       │       │                   requests can reuse an existing connection to avoid
│                       │       │                   overhead. When reusing a connection a range of criteria
│                       │       │                   must be met. Due to a logical error in the code, a request
│                       │       │                   that was issued by an application could wrongfully reuse an
│                       │       │                    existing connection to the same server that was
│                       │       │                   authenticated using different services. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8458.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8458 
│                       ├ [12]  ╭ VulnerabilityID : CVE-2026-8924 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8924 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:96f35a6a745fcabee4bfe6508db420c56c0f571dd47e2d1b651a
│                       │       │                   3f1ff20ecd50 
│                       │       ├ Description     : A flaw in curl's cookie parsing logic allows a malicious
│                       │       │                   HTTP server to set "super cookies" that bypass the Public
│                       │       │                   Suffix List check. This enables an attacker-controlled
│                       │       │                   origin to inject cookies that curl will subsequently scope
│                       │       │                   and transmit to unrelated third-party domains. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8924.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8924 
│                       ├ [13]  ╭ VulnerabilityID : CVE-2026-8926 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8926 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b86ceb41e0069297a344c690624ef4b42e870fa6283a189b436d
│                       │       │                   82d69053a5ce 
│                       │       ├ Description     : When asking curl to use a `.netrc` file to find credentials
│                       │       │                    and at the same time specifying a URL with a username
│                       │       │                   (without a password), like `https://user@example.com/`,
│                       │       │                   curl could wrongly get and use the password for *another*
│                       │       │                   user set in the `.netrc` file for that host if such a one
│                       │       │                   exists and there is no match for the specified user. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8926.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8926 
│                       ├ [14]  ╭ VulnerabilityID : CVE-2026-9080 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9080 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6600a678b8beb15c7613c4f7ece60ddb3505404b3efd1db2ae0a
│                       │       │                   0e26cf6ccf59 
│                       │       ├ Description     : Calling `curl_easy_pause()` within the event-based
│                       │       │                   `CURLMOPT_SOCKETFUNCTION` callback triggers a
│                       │       │                   use-after-free vulnerability, where libcurl attempts to
│                       │       │                   store a flag using a dangling struct pointer immediately
│                       │       │                   after that pointer's memory has been freed. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9080.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9080 
│                       ├ [15]  ╭ VulnerabilityID : CVE-2026-9545 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9545 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bb11486f0635d28da97f59aec3496e8bd2cc68405dbedc87db4d
│                       │       │                   a0d557178bc1 
│                       │       ├ Description     : In this scenario, libcurl first uses a proper HTTP/3 server
│                       │       │                    for the initial transfers, and when it makes a second
│                       │       │                   transfer to the same site it has been replaced by the
│                       │       │                   attacker's impostor machine - without a valid certificate.
│                       │       │                   When libcurl returns to the hostname the second time with a
│                       │       │                    cached SSL session (`CURLOPT_SSL_SESSIONID_CACHE` is not
│                       │       │                   disabled) and early data enabled (the
│                       │       │                   `CURLSSLOPT_EARLYDATA` bit is set in`CURLOPT_SSL_OPTIONS`),
│                       │       │                    libcurl might send off the second request's bytes on that
│                       │       │                   new connection *before* enforcing the certificate
│                       │       │                   verification failure. Potentially leaking sensitive
│                       │       │                   information. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9545.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9545 
│                       ├ [16]  ╭ VulnerabilityID : CVE-2026-9547 
│                       │       ├ PkgID           : curl@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : curl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.3?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6bb869f5631f84e3 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9547 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:53b9968e0b270a1725374f1288ec0ce530fe73eaa5dd20c88c29
│                       │       │                   264b05a095d2 
│                       │       ├ Description     : When a libcurl-based application performs transfers via
│                       │       │                   `SCP://` or `SFTP://` and utilizes the
│                       │       │                   `CURLOPT_SSH_KEYFUNCTION` callback, it may silently accept
│                       │       │                   an untrusted server. This vulnerability occurs when a
│                       │       │                   server presents a host key type that does not match the
│                       │       │                   specific key type already recorded for that host in the
│                       │       │                   `known_hosts` file. Instead of rejecting the mismatch, the
│                       │       │                   callback mechanism fails to properly enforce the
│                       │       │                   restriction, allowing the connection to succeed without
│                       │       │                   warning and risking a potential man-in-the-middle attack.[
│                       │       │                   m 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9547.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9547 
│                       ├ [17]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libblkid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ddaca4141760dfcf 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fd8db8dab923fd7447a5b7adb1f717d6978b73592f10d7f75a79
│                       │       │                   7abce9be7b4c 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [18]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libblkid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ddaca4141760dfcf 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:729209186f8a037e558917758f970ff79b51dd015e23d40dbae1
│                       │       │                   e4b420619ef3 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [19]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:1ced2e8746d0d0d41c9a0281991cce2b7066163506920819abc6
│                       │       │                   2b02e6088283 
│                       │       ├ Title           : glibc: glibc: Denial of Service via iconv() function with
│                       │       │                   specific character sets 
│                       │       ├ Description     : The iconv() function in the GNU C Library versions 2.43 and
│                       │       │                    earlier may crash due to an assertion failure when
│                       │       │                   converting inputs from the IBM1390 or IBM1399 character
│                       │       │                   sets, which may be used to remotely crash an application.
│                       │       │                   
│                       │       │                   This vulnerability can be trivially mitigated by removing
│                       │       │                   the IBM1390 and IBM1399 character sets from systems that do
│                       │       │                    not need them. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-617 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 3 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:L 
│                       │       │                           ╰ V3Score : 5.3 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://inbox.sourceware.org/libc-announce/76814edf-
│                       │       │                  │       cf7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │       │                  ├ [14]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │       │                  ├ [15]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │       │                  ├ [16]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │       │                  ├ [17]: https://packages.fedoraproject.org/pkgs/glibc/glibc-
│                       │       │                  │       gconv-extra/ 
│                       │       │                  ├ [18]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │       │                  ├ [19]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007 
│                       │       │                  ├ [20]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │       │                  ╰ [21]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │       ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:55:54.12Z 
│                       ├ [20]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e2aca081f03bbac4cef332b4c89ce10a211914b1be0d24e4a0b5
│                       │       │                   1744420923de 
│                       │       ├ Title           : glibc: glibc: Incorrect DNS response parsing via crafted
│                       │       │                   DNS server response 
│                       │       ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │       │                   nsswitch.conf that specifies the library's DNS backend in
│                       │       │                   the GNU C Library version 2.34 to version 2.43 could, with
│                       │       │                   a crafted response from the configured DNS server, result
│                       │       │                   in a violation of the DNS specification that causes the
│                       │       │                   application to treat a non-answer section of the DNS
│                       │       │                   response as a valid answer. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ azure      : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 3 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2026-4437.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │       │                  ├ [15]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │       │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │       │                  ├ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │       │                  ╰ [18]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:56:34.227Z 
│                       ├ [21]  ╭ VulnerabilityID : CVE-2026-4438 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:af97d6c59b6a1ff589e7425813c2bc7bb01f874bf00130198632
│                       │       │                   f0685ea967d9 
│                       │       ├ Title           : glibc: glibc: Invalid DNS hostname returned via
│                       │       │                   gethostbyaddr functions 
│                       │       ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │       │                   nsswitch.conf that specifies the library's DNS backend in
│                       │       │                   the GNU C library version 2.34 to version 2.43 could result
│                       │       │                    in an invalid DNS hostname being returned to the caller in
│                       │       │                    violation of the DNS specification. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-20 
│                       │       │                  ╰ [1]: CWE-88 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ azure      : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 4 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2026-4438.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │       │                  ├ [15]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │       │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │       │                  ├ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │       │                  ╰ [18]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:56:34.367Z 
│                       ├ [22]  ╭ VulnerabilityID : CVE-2026-5435 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0b96a64b1d457bb0762e47684acd25c066dd4e3a05b8de26c712
│                       │       │                   c56e8f0974cd 
│                       │       ├ Title           : glibc: glibc: Out-of-bounds write via TSIG record processing 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.2 and newer fail
│                       │       │                   to enforce the caller-supplied buffer length, and can
│                       │       │                   result in an out-of-bounds write when printing TSIG
│                       │       │                   records. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.9 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-5435 
│                       │       │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.1777546
│                       │       │                  │      194.git.fweimer@redhat.com/ 
│                       │       │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-2
│                       │       │                  │      76f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-5435 
│                       │       │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34033 
│                       │       │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │       │                  │      f=advisories/GLIBC-SA-2026-0011 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5435 
│                       │       ├ PublishedDate   : 2026-04-28T13:19:22.29Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:59:01.13Z 
│                       ├ [23]  ╭ VulnerabilityID : CVE-2026-6238 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:47758461ab49ee44d95582dedff5849d267a4137f7f661f2c0ed
│                       │       │                   61f80671cfe1 
│                       │       ├ Title           : glibc: glibc: Application crash or uninitialized memory
│                       │       │                   read via crafted DNS response 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.0.1 to version
│                       │       │                   2.43 fail to validate the RDATA content against the RDATA
│                       │       │                   length in a DNS response when processing A6, CERT, LOC,
│                       │       │                   TKEY or TSIG records, which may allow an attacker to craft
│                       │       │                   a DNS response, causing a target application to crash or
│                       │       │                   read uninitialized memory.
│                       │       │                   
│                       │       │                   These functions are for application debugging only and
│                       │       │                   hence not in the path of code executed by the DNS resolver.
│                       │       │                     Further, they have been deprecated since version 2.34 and
│                       │       │                    should not be used by any new applications.  Applications
│                       │       │                   should consider porting away from these interfaces since
│                       │       │                   they may be removed in future versions. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-126 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-6238 
│                       │       │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.1777546
│                       │       │                  │      194.git.fweimer@redhat.com/ 
│                       │       │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-2
│                       │       │                  │      76f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-6238 
│                       │       │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34069 
│                       │       │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │       │                  │      f=advisories/GLIBC-SA-2026-0012 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6238 
│                       │       ├ PublishedDate   : 2026-04-28T19:37:47.523Z 
│                       │       ╰ LastModifiedDate: 2026-06-19T21:17:02.62Z 
│                       ├ [24]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:126ad83e992ca574a304b5c768d1218ecea596e1af57a7c8e4cd
│                       │       │                   5e58d8001c0a 
│                       │       ├ Title           : glibc: glibc: Denial of Service via iconv() function with
│                       │       │                   specific character sets 
│                       │       ├ Description     : The iconv() function in the GNU C Library versions 2.43 and
│                       │       │                    earlier may crash due to an assertion failure when
│                       │       │                   converting inputs from the IBM1390 or IBM1399 character
│                       │       │                   sets, which may be used to remotely crash an application.
│                       │       │                   
│                       │       │                   This vulnerability can be trivially mitigated by removing
│                       │       │                   the IBM1390 and IBM1399 character sets from systems that do
│                       │       │                    not need them. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-617 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 3 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:L 
│                       │       │                           ╰ V3Score : 5.3 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://inbox.sourceware.org/libc-announce/76814edf-
│                       │       │                  │       cf7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │       │                  ├ [14]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │       │                  ├ [15]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │       │                  ├ [16]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │       │                  ├ [17]: https://packages.fedoraproject.org/pkgs/glibc/glibc-
│                       │       │                  │       gconv-extra/ 
│                       │       │                  ├ [18]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │       │                  ├ [19]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007 
│                       │       │                  ├ [20]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │       │                  ╰ [21]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │       ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:55:54.12Z 
│                       ├ [25]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:40d64246b86dd2946cfbcedfda622d46f752b3be832076a64c0c
│                       │       │                   a92ab1749a9d 
│                       │       ├ Title           : glibc: glibc: Incorrect DNS response parsing via crafted
│                       │       │                   DNS server response 
│                       │       ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │       │                   nsswitch.conf that specifies the library's DNS backend in
│                       │       │                   the GNU C Library version 2.34 to version 2.43 could, with
│                       │       │                   a crafted response from the configured DNS server, result
│                       │       │                   in a violation of the DNS specification that causes the
│                       │       │                   application to treat a non-answer section of the DNS
│                       │       │                   response as a valid answer. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ azure      : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 3 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2026-4437.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │       │                  ├ [15]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │       │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │       │                  ├ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │       │                  ╰ [18]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:56:34.227Z 
│                       ├ [26]  ╭ VulnerabilityID : CVE-2026-4438 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:85d1d0e1652ce45ce2b82130ca0cfef5e6a7ca277c82645dfa81
│                       │       │                   cc171c28e788 
│                       │       ├ Title           : glibc: glibc: Invalid DNS hostname returned via
│                       │       │                   gethostbyaddr functions 
│                       │       ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │       │                   nsswitch.conf that specifies the library's DNS backend in
│                       │       │                   the GNU C library version 2.34 to version 2.43 could result
│                       │       │                    in an invalid DNS hostname being returned to the caller in
│                       │       │                    violation of the DNS specification. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-20 
│                       │       │                  ╰ [1]: CWE-88 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ azure      : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 4 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2026-4438.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │       │                  ├ [15]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │       │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │       │                  ├ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │       │                  ╰ [18]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:56:34.367Z 
│                       ├ [27]  ╭ VulnerabilityID : CVE-2026-5435 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:35279320afbc02b3a703511faf13118f3b6906e6393ad555fc7f
│                       │       │                   34240edd4e5f 
│                       │       ├ Title           : glibc: glibc: Out-of-bounds write via TSIG record processing 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.2 and newer fail
│                       │       │                   to enforce the caller-supplied buffer length, and can
│                       │       │                   result in an out-of-bounds write when printing TSIG
│                       │       │                   records. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.9 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-5435 
│                       │       │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.1777546
│                       │       │                  │      194.git.fweimer@redhat.com/ 
│                       │       │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-2
│                       │       │                  │      76f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-5435 
│                       │       │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34033 
│                       │       │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │       │                  │      f=advisories/GLIBC-SA-2026-0011 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5435 
│                       │       ├ PublishedDate   : 2026-04-28T13:19:22.29Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:59:01.13Z 
│                       ├ [28]  ╭ VulnerabilityID : CVE-2026-6238 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8c51716c3c97be46016384b2fc20b3896aa7616c942a954df71f
│                       │       │                   f62b3f0bf2ab 
│                       │       ├ Title           : glibc: glibc: Application crash or uninitialized memory
│                       │       │                   read via crafted DNS response 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.0.1 to version
│                       │       │                   2.43 fail to validate the RDATA content against the RDATA
│                       │       │                   length in a DNS response when processing A6, CERT, LOC,
│                       │       │                   TKEY or TSIG records, which may allow an attacker to craft
│                       │       │                   a DNS response, causing a target application to crash or
│                       │       │                   read uninitialized memory.
│                       │       │                   
│                       │       │                   These functions are for application debugging only and
│                       │       │                   hence not in the path of code executed by the DNS resolver.
│                       │       │                     Further, they have been deprecated since version 2.34 and
│                       │       │                    should not be used by any new applications.  Applications
│                       │       │                   should consider porting away from these interfaces since
│                       │       │                   they may be removed in future versions. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-126 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-6238 
│                       │       │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.1777546
│                       │       │                  │      194.git.fweimer@redhat.com/ 
│                       │       │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-2
│                       │       │                  │      76f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-6238 
│                       │       │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34069 
│                       │       │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │       │                  │      f=advisories/GLIBC-SA-2026-0012 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6238 
│                       │       ├ PublishedDate   : 2026-04-28T19:37:47.523Z 
│                       │       ╰ LastModifiedDate: 2026-06-19T21:17:02.62Z 
│                       ├ [29]  ╭ VulnerabilityID : CVE-2026-11856 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-11856 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:70f14f1bd828cb48726d6d0f243bb6be8087541cb0c7fc2410d8
│                       │       │                   516818449f45 
│                       │       ├ Description     : Successfully using libcurl to do a transfer to a specific
│                       │       │                   HTTP origin (`hostA`) with **Digest** authentication and
│                       │       │                   then changing the origin to a different one (`hostB`) for a
│                       │       │                    second transfer, reusing the same handle, makes libcurl
│                       │       │                   wrongly pass on the `Authorization:` header field meant for
│                       │       │                    `hostA`, to `hostB`. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-11856.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-11856 
│                       ├ [30]  ╭ VulnerabilityID : CVE-2026-8925 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8925 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:315f142b39ad378118b018a616e14bd7da9af98f3572ba7598e6
│                       │       │                   a6e9a6c7149b 
│                       │       ├ Description     : The curl logic that works with SASL authentication could
│                       │       │                   end up cleaning up the GSASL context *twice* without
│                       │       │                   clearing the pointer in between, making it `free()` the
│                       │       │                   same pointer twice. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8925.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8925 
│                       ├ [31]  ╭ VulnerabilityID : CVE-2026-8927 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8927 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b1be12ce52855352ff22a7992aff9d70da281408d7d365ffe4db
│                       │       │                   98d5d2e712e6 
│                       │       ├ Description     : When reusing a libcurl handle for sequential transfers
│                       │       │                   driven by environment-variable proxy configuration, libcurl
│                       │       │                    fails to clear the proxy authentication state between
│                       │       │                   requests. Specifically, if the initial transfer
│                       │       │                   authenticates against `proxyA` using Digest auth, a
│                       │       │                   subsequent transfer routed through `proxyB` erroneously
│                       │       │                   leaks the `Proxy-Authorization:` header intended solely for
│                       │       │                    `proxyA`. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8927.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8927 
│                       ├ [32]  ╭ VulnerabilityID : CVE-2026-9079 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9079 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2417d78601019a632e9fa7bec9e7a2f37b519ad26d3f57d0fcef
│                       │       │                   b0c61bd39f93 
│                       │       ├ Description     : libcurl had a flaw that when instructed to clear proxy
│                       │       │                   authentication credentials which made it not do so, leaving
│                       │       │                    the old credentials around to get used for subsequent
│                       │       │                   tranfers that should not know nor use them. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9079.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9079 
│                       ├ [33]  ╭ VulnerabilityID : CVE-2026-10536 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-10536 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:342e9bf5f439db8913f583217a9dd4b1a8ade99bd30314799c17
│                       │       │                   8dfd4517c546 
│                       │       ├ Description     : A use-after-free vulnerability exists in libcurl when an
│                       │       │                   application configures an HTTP/2 stream-dependency tree via
│                       │       │                    `CURLOPT_STREAM_DEPENDS` or `CURLOPT_STREAM_DEPENDS_E`,
│                       │       │                   subsequently invokes `curl_easy_reset()`, and finally
│                       │       │                   terminates the handle with `curl_easy_cleanup()`. During
│                       │       │                   this final cleanup phase, libcurl attempts to access and
│                       │       │                   modify an internal structure that was already deallocated
│                       │       │                   during the reset operation. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-10536.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-10536 
│                       ├ [34]  ╭ VulnerabilityID : CVE-2026-12064 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-12064 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:824e853d7b6a872c8dd5074156103ca426f0fd07c6ca189eaeac
│                       │       │                   66559e68778b 
│                       │       ├ Description     : When a user invokes curl using a schemeless URL combined
│                       │       │                   with `--proto-default` sftp (or scp), a disconnect occurs
│                       │       │                   between the tool layer and libcurl. The tool layer
│                       │       │                   incorrectly infers the URL scheme, which erroneously
│                       │       │                   bypasses the initialization of critical SSH security
│                       │       │                   options like CURLOPT_SSH_HOST_PUBLIC_KEY_SHA256 and
│                       │       │                   CURLOPT_SSH_KNOWNHOSTS. Conversely, the libcurl runtime
│                       │       │                   successfully honors CURLOPT_DEFAULT_PROTOCOL and
│                       │       │                   establishes the connection via SFTP/SCP as specified.
│                       │       │                   Because the tool layer skipped the security configuration,
│                       │       │                   these SSH host verification options are silently omitted,
│                       │       │                   causing curl to connect to an unverified SSH remote host
│                       │       │                   without throwing an error. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-12064.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-12064 
│                       ├ [35]  ╭ VulnerabilityID : CVE-2026-8286 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8286 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fef711405f42fdb17e69a2220fbabb38b6b4b9f8dc2e351de899
│                       │       │                   edba6229ad8a 
│                       │       ├ Description     : A vulnerability exists where a new transfer that uses
│                       │       │                   STARTTLS to upgrade the connection might reuse an existing
│                       │       │                   live connection even though the TLS configuration
│                       │       │                   mismatches so it should not. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8286.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8286 
│                       ├ [36]  ╭ VulnerabilityID : CVE-2026-8458 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8458 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8693781bbd0e127c591e8c3135e8cead0366f5b40ed10e89986d
│                       │       │                   c954807207d8 
│                       │       ├ Description     : libcurl might in some circumstances reuse the wrong
│                       │       │                   connection when asked to do Negotiate-authenticated ones,
│                       │       │                   even when they are set to use different "services". libcurl
│                       │       │                    features a pool of recent connections so that subsequent
│                       │       │                   requests can reuse an existing connection to avoid
│                       │       │                   overhead. When reusing a connection a range of criteria
│                       │       │                   must be met. Due to a logical error in the code, a request
│                       │       │                   that was issued by an application could wrongfully reuse an
│                       │       │                    existing connection to the same server that was
│                       │       │                   authenticated using different services. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8458.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8458 
│                       ├ [37]  ╭ VulnerabilityID : CVE-2026-8924 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8924 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:751f45de38aee6d48e6345d24d63a96636caaf21ed9b6e6f1fd7
│                       │       │                   91f812b929b7 
│                       │       ├ Description     : A flaw in curl's cookie parsing logic allows a malicious
│                       │       │                   HTTP server to set "super cookies" that bypass the Public
│                       │       │                   Suffix List check. This enables an attacker-controlled
│                       │       │                   origin to inject cookies that curl will subsequently scope
│                       │       │                   and transmit to unrelated third-party domains. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8924.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8924 
│                       ├ [38]  ╭ VulnerabilityID : CVE-2026-8926 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8926 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:782ff01709a92252c9b592566fc828a884d76197d6cddf34ffc4
│                       │       │                   4c07bd382a0e 
│                       │       ├ Description     : When asking curl to use a `.netrc` file to find credentials
│                       │       │                    and at the same time specifying a URL with a username
│                       │       │                   (without a password), like `https://user@example.com/`,
│                       │       │                   curl could wrongly get and use the password for *another*
│                       │       │                   user set in the `.netrc` file for that host if such a one
│                       │       │                   exists and there is no match for the specified user. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-8926.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-8926 
│                       ├ [39]  ╭ VulnerabilityID : CVE-2026-9080 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9080 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:676d1d3ca2aaca97b487ec114b8a5663fffb70d3940b2347e631
│                       │       │                   131c273ef7d1 
│                       │       ├ Description     : Calling `curl_easy_pause()` within the event-based
│                       │       │                   `CURLMOPT_SOCKETFUNCTION` callback triggers a
│                       │       │                   use-after-free vulnerability, where libcurl attempts to
│                       │       │                   store a flag using a dangling struct pointer immediately
│                       │       │                   after that pointer's memory has been freed. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9080.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9080 
│                       ├ [40]  ╭ VulnerabilityID : CVE-2026-9545 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9545 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:161a4cdd25649e44c49f05cbef18ceb9d7e3b3ae4818912e7fe2
│                       │       │                   8741016b30f4 
│                       │       ├ Description     : In this scenario, libcurl first uses a proper HTTP/3 server
│                       │       │                    for the initial transfers, and when it makes a second
│                       │       │                   transfer to the same site it has been replaced by the
│                       │       │                   attacker's impostor machine - without a valid certificate.
│                       │       │                   When libcurl returns to the hostname the second time with a
│                       │       │                    cached SSL session (`CURLOPT_SSL_SESSIONID_CACHE` is not
│                       │       │                   disabled) and early data enabled (the
│                       │       │                   `CURLSSLOPT_EARLYDATA` bit is set in`CURLOPT_SSL_OPTIONS`),
│                       │       │                    libcurl might send off the second request's bytes on that
│                       │       │                   new connection *before* enforcing the certificate
│                       │       │                   verification failure. Potentially leaking sensitive
│                       │       │                   information. 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9545.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9545 
│                       ├ [41]  ╭ VulnerabilityID : CVE-2026-9547 
│                       │       ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.3 
│                       │       ├ PkgName         : libcurl4t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.3?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8ef767c5a03f17d2 
│                       │       ├ InstalledVersion: 8.14.1-2ubuntu1.3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9547 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2a6e8e8f4f135a073ce8cfd33cd7ca9b1e5f6a9c123651bbd6e9
│                       │       │                   8b30670b28f0 
│                       │       ├ Description     : When a libcurl-based application performs transfers via
│                       │       │                   `SCP://` or `SFTP://` and utilizes the
│                       │       │                   `CURLOPT_SSH_KEYFUNCTION` callback, it may silently accept
│                       │       │                   an untrusted server. This vulnerability occurs when a
│                       │       │                   server presents a host key type that does not match the
│                       │       │                   specific key type already recorded for that host in the
│                       │       │                   `known_hosts` file. Instead of rejecting the mismatch, the
│                       │       │                   callback mechanism fails to properly enforce the
│                       │       │                   restriction, allowing the connection to succeed without
│                       │       │                   warning and risking a potential man-in-the-middle attack.[
│                       │       │                   m 
│                       │       ├ Severity        : LOW 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ╰ References       ╭ [0]: https://curl.se/L7HzKXisfJ/CVE-2026-9547.md 
│                       │                          ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2026-9547 
│                       ├ [42]  ╭ VulnerabilityID : CVE-2025-66382 
│                       │       ├ PkgID           : libexpat1@2.7.1-2ubuntu0.2 
│                       │       ├ PkgName         : libexpat1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.1-2ubuntu0.2?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : bb3ed74d0fd332c6 
│                       │       ├ InstalledVersion: 2.7.1-2ubuntu0.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:06165d356b82cef42ee15403a8ceca1ddccdd02074e35c0504f2
│                       │       │                   4e5d5fdcc410 
│                       │       ├ Title           : libexpat: libexpat: Denial of service via crafted file
│                       │       │                   processing 
│                       │       ├ Description     : In libexpat through 2.7.3, a crafted file with an
│                       │       │                   approximate size of 2 MiB can lead to dozens of seconds of
│                       │       │                   processing time. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-407 
│                       │       ├ VendorSeverity   ╭ nvd   : 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:
│                       │       │                  │        │           N/A:H 
│                       │       │                  │        ╰ V3Score : 5.5 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:L 
│                       │       │                           ╰ V3Score : 2.9 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2025/12/02/1 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2025-66382 
│                       │       │                  ├ [2]: https://cert-portal.siemens.com/productcert/html/ssa-
│                       │       │                  │      082556.html 
│                       │       │                  ├ [3]: https://cert-portal.siemens.com/productcert/html/ssa-
│                       │       │                  │      253495.html 
│                       │       │                  ├ [4]: https://github.com/libexpat/libexpat/issues/1076 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2025-66382 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2025-66382 
│                       │       ├ PublishedDate   : 2025-11-28T07:15:57.9Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T09:56:45.24Z 
│                       ├ [43]  ╭ VulnerabilityID : CVE-2024-2236 
│                       │       ├ PkgID           : libgcrypt20@1.11.0-7ubuntu0.1 
│                       │       ├ PkgName         : libgcrypt20 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libgcrypt20@1.11.0-7ubuntu0.1?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8f3635c00dca0a4f 
│                       │       ├ InstalledVersion: 1.11.0-7ubuntu0.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-2236 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ef438693eed4457c5a9b8fa1598b34975686fd40ca01b4642e7f
│                       │       │                   32ecb24074aa 
│                       │       ├ Title           : libgcrypt: vulnerable to Marvin Attack 
│                       │       ├ Description     : A timing-based side-channel flaw was found in libgcrypt's
│                       │       │                   RSA implementation. This issue may allow a remote attacker
│                       │       │                   to initiate a Bleichenbacher-style attack, which can lead
│                       │       │                   to the decryption of RSA ciphertexts. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-385 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ amazon     : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 1 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 5.9 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2024:9404 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2025:3530 
│                       │       │                  ├ [2] : https://access.redhat.com/errata/RHSA-2025:3534 
│                       │       │                  ├ [3] : https://access.redhat.com/security/cve/CVE-2024-2236 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2245218 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2245218 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2268268 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       024-2236 
│                       │       │                  ├ [8] : https://dev.gnupg.org/T7136 
│                       │       │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2024-9404.html 
│                       │       │                  ├ [10]: https://errata.rockylinux.org/RLSA-2024:9404 
│                       │       │                  ├ [11]: https://github.com/tomato42/marvin-toolkit/tree/mast
│                       │       │                  │       er/example/libgcrypt 
│                       │       │                  ├ [12]: https://gitlab.com/redhat-crypto/libgcrypt/libgcrypt
│                       │       │                  │       -mirror/-/merge_requests/17 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2024-2236.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2024-9404.html 
│                       │       │                  ├ [15]: https://lists.gnupg.org/pipermail/gcrypt-devel/2024-
│                       │       │                  │       March/005607.html 
│                       │       │                  ├ [16]: https://nvd.nist.gov/vuln/detail/CVE-2024-2236 
│                       │       │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2024-2236 
│                       │       ├ PublishedDate   : 2024-03-06T22:15:57.977Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T07:24:06.083Z 
│                       ├ [44]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : liblastlog2-2 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6aa63af50fb78d18 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:efeb6228913acd713c48264a7e71ca97ea462b8ec3fc785371e8
│                       │       │                   5df2701e1ab9 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [45]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : liblastlog2-2 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6aa63af50fb78d18 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ae4825cd574e0811a0055d044aba8cae9aafc656683ad982374d
│                       │       │                   00c248f8848a 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [46]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libmount1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e278fd35c2ddbe27 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:64b2a2d26fe29b7de1500eb4ac90967d2d47ffe0261558f13595
│                       │       │                   97ba1c9db2c7 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [47]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libmount1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e278fd35c2ddbe27 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f0034cb0d2c9e28097524b0cf344ac2339983bba2c6d83de5a27
│                       │       │                   4836dc2a4bd1 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [48]  ╭ VulnerabilityID : CVE-2026-13757 
│                       │       ├ PkgID           : libp11-kit0@0.25.5-3ubuntu1 
│                       │       ├ PkgName         : libp11-kit0 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libp11-kit0@0.25.5-3ubuntu1?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : d83476d4246a471f 
│                       │       ├ InstalledVersion: 0.25.5-3ubuntu1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-13757 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3f273f1f749d1b28a8d054f24604ad958b493b6e6e47ab890c01
│                       │       │                   177e4be2c106 
│                       │       ├ Title           : p11-kit: Stack exhaustion via unbounded recursion in RPC
│                       │       │                   attribute parsing 
│                       │       ├ Description     : A flaw was found in p11-kit. The RPC message attribute
│                       │       │                   parsing functions p11_rpc_message_get_attribute() and
│                       │       │                   p11_rpc_message_get_attribute_array_value() form a
│                       │       │                   mutually-recursive call chain with no recursion depth limit
│                       │       │                    when processing nested CKA_WRAP_TEMPLATE,
│                       │       │                   CKA_UNWRAP_TEMPLATE, and CKA_DERIVE_TEMPLATE attributes. An
│                       │       │                    unauthenticated attacker with local access to the p11-kit
│                       │       │                   RPC Unix domain socket can send a specially crafted request
│                       │       │                    with deeply nested template attributes, causing stack
│                       │       │                   exhaustion and crashing the p11-kit server process and its
│                       │       │                   dependent services. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-674 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 6.2 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-13757 
│                       │       │                  ├ [1]: https://bugzilla.redhat.com/show_bug.cgi?id=2494556 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-13757 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-13757 
│                       │       ├ PublishedDate   : 2026-06-29T19:16:40.907Z 
│                       │       ╰ LastModifiedDate: 2026-07-01T15:16:30.19Z 
│                       ├ [49]  ╭ VulnerabilityID : CVE-2026-42496 
│                       │       ├ PkgID           : libperl5.40@5.40.1-6build1 
│                       │       ├ PkgName         : libperl5.40 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libperl5.40@5.40.1-6build1?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : fcad69c24b9e2dff 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42496 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e8120f690b13a612ed8b32243160efdfcf4ac001d0a0f3c0a701
│                       │       │                   d5fd9c04cf22 
│                       │       ├ Title           : perl-archive-tar: perl-archive-tar: Path traversal via
│                       │       │                   crafted symlinks allows arbitrary file access 
│                       │       ├ Description     : Archive::Tar versions before 3.08 for Perl extract symlinks
│                       │       │                    with attacker controlled targets outside the extraction
│                       │       │                   directory.
│                       │       │                   
│                       │       │                   _make_special_file() passes the tar header's linkname to
│                       │       │                   symlink() without validating it against absolute paths or
│                       │       │                   .. segments. The secure-extract mode check that guards
│                       │       │                   regular file extraction does not cover the symlink target.
│                       │       │                   A subsequent open through the extracted name reads or
│                       │       │                   writes the attacker chosen path. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ╰ [1]: CWE-22 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ nvd        : 4 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ redhat     : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:
│                       │       │                  │        │           H/A:N 
│                       │       │                  │        ╰ V3Score : 9.1 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 8.2 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:30851 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:30852 
│                       │       │                  ├ [2] : https://access.redhat.com/errata/RHSA-2026:30856 
│                       │       │                  ├ [3] : https://access.redhat.com/errata/RHSA-2026:30857 
│                       │       │                  ├ [4] : https://access.redhat.com/security/cve/CVE-2026-42496 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2481314 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2481314 
│                       │       │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-30856.html 
│                       │       │                  ├ [8] : https://github.com/jib/archive-tar-new/commit/17c873
│                       │       │                  │       492a05eddc0de18c1485e0b2cccd5a9158.patch 
│                       │       │                  ├ [9] : https://linux.oracle.com/cve/CVE-2026-42496.html 
│                       │       │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-30856.html 
│                       │       │                  ├ [11]: https://lists.security.metacpan.org/cve-announce/msg
│                       │       │                  │       /40396459/ 
│                       │       │                  ├ [12]: https://metacpan.org/release/BINGOS/Archive-Tar-3.08
│                       │       │                  │       /changes 
│                       │       │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-42496 
│                       │       │                  ├ [14]: https://security.access.redhat.com/data/csaf/v2/vex/
│                       │       │                  │       2026/cve-2026-42496.json 
│                       │       │                  ├ [15]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ├ [16]: https://www.cve.org/CVERecord?id=CVE-2026-42496 
│                       │       │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-42497 
│                       │       ├ PublishedDate   : 2026-05-26T02:16:40.13Z 
│                       │       ╰ LastModifiedDate: 2026-06-30T03:19:37.663Z 
│                       ├ [50]  ╭ VulnerabilityID : CVE-2026-8376 
│                       │       ├ PkgID           : libperl5.40@5.40.1-6build1 
│                       │       ├ PkgName         : libperl5.40 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libperl5.40@5.40.1-6build1?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : fcad69c24b9e2dff 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8376 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a5160cb4a84f3330050fda9107b4b32b0d547385e746c42439f8
│                       │       │                   ed260ce95631 
│                       │       ├ Title           : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compili ... 
│                       │       ├ Description     : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compiling regular expressions with a repeated fixed
│                       │       │                   string on 32-bit builds.
│                       │       │                   
│                       │       │                   Perl_study_chunk in regcomp_study.c checked the size of the
│                       │       │                    joined substring buffer in characters rather than bytes.
│                       │       │                   For a quantified fixed substring with a large minimum
│                       │       │                   count, the byte length mincount * l could overflow SSize_t,
│                       │       │                    producing an undersized SvGROW allocation; the subsequent
│                       │       │                   copy writes past the end of the buffer.
│                       │       │                   A caller that compiles an attacker-controlled regular
│                       │       │                   expression on a 32-bit perl build triggers a heap buffer
│                       │       │                   overflow at compile time. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-680 
│                       │       ├ VendorSeverity   ╭ amazon: 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ nvd   : 4 
│                       │       │                  ├ photon: 4 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 9.8 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/26/1 
│                       │       │                  ├ [1]: https://github.com/Perl/perl5/commit/5e7f119eb2bb1181
│                       │       │                  │      be908701f22bf7068e722f1c.patch 
│                       │       │                  ├ [2]: https://github.com/Perl/perl5/pull/24433 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-8376 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-8376 
│                       │       ├ PublishedDate   : 2026-05-26T00:16:57.15Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T11:03:51.843Z 
│                       ├ [51]  ╭ VulnerabilityID : CVE-2026-2297 
│                       │       ├ PkgID           : libpython3.13@3.13.7-1ubuntu0.4 
│                       │       ├ PkgName         : libpython3.13 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13@3.13.7-1ubuntu0.4?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : d39243325c040cfa 
│                       │       ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:903e9b073b7611cccba9d841d92b777f27722d5f3a71e0fb761e
│                       │       │                   bd02e223b45e 
│                       │       ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │       ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │       │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │       │                    (a base class) and so does not use io.open_code() to read
│                       │       │                   the .pyc files. sys.audit handlers for this audit event
│                       │       │                   therefore do not fire. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-668 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 2 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/0
│                       │       │                  │       5/6 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:19177 
│                       │       │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │       │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │       │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │       │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │       │                  ├ [11]: https://bugzilla.redhat.com/2449649 
│                       │       │                  ├ [12]: https://bugzilla.redhat.com/2457409 
│                       │       │                  ├ [13]: https://bugzilla.redhat.com/2457932 
│                       │       │                  ├ [14]: https://bugzilla.redhat.com/2458049 
│                       │       │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │       │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │       │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │       │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │       │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │       │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │       │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │       │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │       │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │       │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │       │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │       │                  ├ [26]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │       │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-13837 
│                       │       │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-15282 
│                       │       │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-59375 
│                       │       │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-6075 
│                       │       │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-0672 
│                       │       │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-1502 
│                       │       │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-2297 
│                       │       │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-3644 
│                       │       │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4224 
│                       │       │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4519 
│                       │       │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4786 
│                       │       │                  ├ [38]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-6100 
│                       │       │                  ├ [39]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │       │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │       │                  ├ [41]: https://github.com/python/cpython/commit/482d6f8bdba
│                       │       │                  │       9da3725d272e8bb4a2d25fb6a603e 
│                       │       │                  ├ [42]: https://github.com/python/cpython/commit/69ddd9bb2cc
│                       │       │                  │       4bd69b1565647c18659c6a789ccd9 
│                       │       │                  ├ [43]: https://github.com/python/cpython/commit/876858c9f65
│                       │       │                  │       d9ab656c7fa639f268ce7856d89dd 
│                       │       │                  ├ [44]: https://github.com/python/cpython/commit/a51b1b512de
│                       │       │                  │       1d56b3714b65628a2eae2b07e535e 
│                       │       │                  ├ [45]: https://github.com/python/cpython/commit/e58e9802b9b
│                       │       │                  │       ec5cdbf48fc9bf1da5f4fda482e86 
│                       │       │                  ├ [46]: https://github.com/python/cpython/issues/145506 
│                       │       │                  ├ [47]: https://github.com/python/cpython/pull/145507 
│                       │       │                  ├ [48]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │       │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-19177.html 
│                       │       │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │       │                  ╰ [51]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │       ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:30:44.59Z 
│                       ├ [52]  ╭ VulnerabilityID : CVE-2026-2297 
│                       │       ├ PkgID           : libpython3.13-minimal@3.13.7-1ubuntu0.4 
│                       │       ├ PkgName         : libpython3.13-minimal 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-minimal@3.13.7-1ubuntu0
│                       │       │                  │       .4?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9682446bb647ab44 
│                       │       ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:83d2ce7bf546e4eea155128da9537e219f3b28eac09d18506afe
│                       │       │                   e1e1c8dc25d4 
│                       │       ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │       ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │       │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │       │                    (a base class) and so does not use io.open_code() to read
│                       │       │                   the .pyc files. sys.audit handlers for this audit event
│                       │       │                   therefore do not fire. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-668 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 2 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/0
│                       │       │                  │       5/6 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:19177 
│                       │       │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │       │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │       │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │       │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │       │                  ├ [11]: https://bugzilla.redhat.com/2449649 
│                       │       │                  ├ [12]: https://bugzilla.redhat.com/2457409 
│                       │       │                  ├ [13]: https://bugzilla.redhat.com/2457932 
│                       │       │                  ├ [14]: https://bugzilla.redhat.com/2458049 
│                       │       │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │       │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │       │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │       │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │       │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │       │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │       │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │       │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │       │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │       │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │       │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │       │                  ├ [26]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │       │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-13837 
│                       │       │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-15282 
│                       │       │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-59375 
│                       │       │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-6075 
│                       │       │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-0672 
│                       │       │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-1502 
│                       │       │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-2297 
│                       │       │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-3644 
│                       │       │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4224 
│                       │       │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4519 
│                       │       │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4786 
│                       │       │                  ├ [38]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-6100 
│                       │       │                  ├ [39]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │       │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │       │                  ├ [41]: https://github.com/python/cpython/commit/482d6f8bdba
│                       │       │                  │       9da3725d272e8bb4a2d25fb6a603e 
│                       │       │                  ├ [42]: https://github.com/python/cpython/commit/69ddd9bb2cc
│                       │       │                  │       4bd69b1565647c18659c6a789ccd9 
│                       │       │                  ├ [43]: https://github.com/python/cpython/commit/876858c9f65
│                       │       │                  │       d9ab656c7fa639f268ce7856d89dd 
│                       │       │                  ├ [44]: https://github.com/python/cpython/commit/a51b1b512de
│                       │       │                  │       1d56b3714b65628a2eae2b07e535e 
│                       │       │                  ├ [45]: https://github.com/python/cpython/commit/e58e9802b9b
│                       │       │                  │       ec5cdbf48fc9bf1da5f4fda482e86 
│                       │       │                  ├ [46]: https://github.com/python/cpython/issues/145506 
│                       │       │                  ├ [47]: https://github.com/python/cpython/pull/145507 
│                       │       │                  ├ [48]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │       │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-19177.html 
│                       │       │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │       │                  ╰ [51]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │       ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:30:44.59Z 
│                       ├ [53]  ╭ VulnerabilityID : CVE-2026-2297 
│                       │       ├ PkgID           : libpython3.13-stdlib@3.13.7-1ubuntu0.4 
│                       │       ├ PkgName         : libpython3.13-stdlib 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-stdlib@3.13.7-1ubuntu0.
│                       │       │                  │       4?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 80f30a21647be5ac 
│                       │       ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:7ccd8c92c560b517f964d9897c4a00a8ea4e6d949bdf925612ab
│                       │       │                   6c2f1b100c68 
│                       │       ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │       ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │       │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │       │                    (a base class) and so does not use io.open_code() to read
│                       │       │                   the .pyc files. sys.audit handlers for this audit event
│                       │       │                   therefore do not fire. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-668 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 2 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/0
│                       │       │                  │       5/6 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:19177 
│                       │       │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │       │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │       │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │       │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │       │                  ├ [11]: https://bugzilla.redhat.com/2449649 
│                       │       │                  ├ [12]: https://bugzilla.redhat.com/2457409 
│                       │       │                  ├ [13]: https://bugzilla.redhat.com/2457932 
│                       │       │                  ├ [14]: https://bugzilla.redhat.com/2458049 
│                       │       │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │       │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │       │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │       │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │       │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │       │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │       │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │       │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │       │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │       │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │       │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │       │                  ├ [26]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │       │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-13837 
│                       │       │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-15282 
│                       │       │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-59375 
│                       │       │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-6075 
│                       │       │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-0672 
│                       │       │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-1502 
│                       │       │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-2297 
│                       │       │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-3644 
│                       │       │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4224 
│                       │       │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4519 
│                       │       │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4786 
│                       │       │                  ├ [38]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-6100 
│                       │       │                  ├ [39]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │       │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │       │                  ├ [41]: https://github.com/python/cpython/commit/482d6f8bdba
│                       │       │                  │       9da3725d272e8bb4a2d25fb6a603e 
│                       │       │                  ├ [42]: https://github.com/python/cpython/commit/69ddd9bb2cc
│                       │       │                  │       4bd69b1565647c18659c6a789ccd9 
│                       │       │                  ├ [43]: https://github.com/python/cpython/commit/876858c9f65
│                       │       │                  │       d9ab656c7fa639f268ce7856d89dd 
│                       │       │                  ├ [44]: https://github.com/python/cpython/commit/a51b1b512de
│                       │       │                  │       1d56b3714b65628a2eae2b07e535e 
│                       │       │                  ├ [45]: https://github.com/python/cpython/commit/e58e9802b9b
│                       │       │                  │       ec5cdbf48fc9bf1da5f4fda482e86 
│                       │       │                  ├ [46]: https://github.com/python/cpython/issues/145506 
│                       │       │                  ├ [47]: https://github.com/python/cpython/pull/145507 
│                       │       │                  ├ [48]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │       │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-19177.html 
│                       │       │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │       │                  ╰ [51]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │       ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:30:44.59Z 
│                       ├ [54]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libsmartcols1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:27744228ecf1a8efaeece3fb4202d22bab675949aa11c873c6c3
│                       │       │                   a4096e3fb22d 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [55]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libsmartcols1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a7d2577310af04e140c79687f1fbbcde5dafda2c3d6b10673314
│                       │       │                   3554cef55719 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [56]  ╭ VulnerabilityID : CVE-2026-11822 
│                       │       ├ PkgID           : libsqlite3-0@3.46.1-8 
│                       │       ├ PkgName         : libsqlite3-0 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsqlite3-0@3.46.1-8?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 7522901a39cfac59 
│                       │       ├ InstalledVersion: 3.46.1-8 
│                       │       ├ FixedVersion    : 3.46.1-8ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-11822 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8eee996da59cfb55cf415e546afead2e9019c47603b74535aea3
│                       │       │                   e3311ee56c38 
│                       │       ├ Title           : SQLite before 3.53.2 contains memory corruption
│                       │       │                   vulnerabilities in the ... 
│                       │       ├ Description     : SQLite before 3.53.2 contains memory corruption
│                       │       │                   vulnerabilities in the FTS5 full-text search extension that
│                       │       │                    allow attackers to cause process crashes, memory
│                       │       │                   exhaustion, or arbitrary code execution by supplying a
│                       │       │                   crafted database with malformed FTS5 page data. Attackers
│                       │       │                   can trigger an out-of-bounds read in fts5LeafSeek() via an
│                       │       │                   attacker-controlled loop bound and a heap buffer overflow
│                       │       │                   write in fts5ChunkIterate() through a crafted continuation
│                       │       │                   page causing an integer underflow, exploitable when an FTS5
│                       │       │                    MATCH query is executed against the malicious database. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-122 
│                       │       ├ VendorSeverity   ╭ azure  : 3 
│                       │       │                  ├ bitnami: 3 
│                       │       │                  ├ photon : 3 
│                       │       │                  ╰ ubuntu : 2 
│                       │       ├ CVSS             ─ bitnami ╭ V40Vector: CVSS:4.0/AV:L/AC:L/AT:N/PR:N/UI:P/VC:
│                       │       │                            │            H/VI:H/VA:H/SC:N/SI:N/SA:N 
│                       │       │                            ╰ V40Score : 8.5 
│                       │       ├ References       ╭ [0]: https://nvd.nist.gov/vuln/detail/CVE-2026-11822 
│                       │       │                  ├ [1]: https://sqlite.org/releaselog/3_53_2.html 
│                       │       │                  ├ [2]: https://sqlite.org/src/info/061febcf41ca 
│                       │       │                  ├ [3]: https://sqlite.org/src/info/4a5ad516ea93 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8480-1 
│                       │       │                  ├ [5]: https://www.cve.org/CVERecord?id=CVE-2026-11822 
│                       │       │                  ╰ [6]: https://www.vulncheck.com/advisories/sqlite-before-me
│                       │       │                         mory-corruption-in-fts5-extension 
│                       │       ├ PublishedDate   : 2026-06-09T20:16:32.15Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:14:29.127Z 
│                       ├ [57]  ╭ VulnerabilityID : CVE-2026-11824 
│                       │       ├ PkgID           : libsqlite3-0@3.46.1-8 
│                       │       ├ PkgName         : libsqlite3-0 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsqlite3-0@3.46.1-8?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 7522901a39cfac59 
│                       │       ├ InstalledVersion: 3.46.1-8 
│                       │       ├ FixedVersion    : 3.46.1-8ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-11824 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:096c84406e415b6f91c78dc02a9b6f98aba696948b7171907a3f
│                       │       │                   bf81255b7d24 
│                       │       ├ Title           : SQLite before 3.53.2 contains a heap-based buffer overflow
│                       │       │                   vulnerabili ... 
│                       │       ├ Description     : SQLite before 3.53.2 contains a heap-based buffer overflow
│                       │       │                   vulnerability in the FTS5 full-text search extension that
│                       │       │                   allows attackers to cause a crash or execute arbitrary code
│                       │       │                    by supplying a crafted database with malicious
│                       │       │                   continuation page metadata specifying a szLeaf value
│                       │       │                   smaller than 4. Attackers can trigger an integer underflow
│                       │       │                   in fts5ChunkIterate() causing an inflated remaining byte
│                       │       │                   count during FTS5 MATCH query processing, leading to a heap
│                       │       │                    buffer overflow of attacker-controlled data in
│                       │       │                   applications compiled with SQLITE_ENABLE_FTS5. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-122 
│                       │       ├ VendorSeverity   ╭ azure  : 3 
│                       │       │                  ├ bitnami: 3 
│                       │       │                  ├ photon : 3 
│                       │       │                  ╰ ubuntu : 2 
│                       │       ├ CVSS             ─ bitnami ╭ V40Vector: CVSS:4.0/AV:L/AC:L/AT:N/PR:N/UI:P/VC:
│                       │       │                            │            H/VI:H/VA:H/SC:N/SI:N/SA:N 
│                       │       │                            ╰ V40Score : 8.5 
│                       │       ├ References       ╭ [0]: https://nvd.nist.gov/vuln/detail/CVE-2026-11824 
│                       │       │                  ├ [1]: https://sqlite.org/releaselog/3_53_2.html 
│                       │       │                  ├ [2]: https://sqlite.org/src/info/061febcf41ca 
│                       │       │                  ├ [3]: https://sqlite.org/src/info/4a5ad516ea93 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8480-1 
│                       │       │                  ├ [5]: https://www.cve.org/CVERecord?id=CVE-2026-11824 
│                       │       │                  ╰ [6]: https://www.vulncheck.com/advisories/sqlite-before-he
│                       │       │                         ap-buffer-overflow-via-fts5-fts5chunkiterate 
│                       │       ├ PublishedDate   : 2026-06-09T20:16:32.3Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:14:29.253Z 
│                       ├ [58]  ╭ VulnerabilityID : CVE-2025-15661 
│                       │       ├ PkgID           : libssh2-1t64@1.11.1-1ubuntu0.25.10.1 
│                       │       ├ PkgName         : libssh2-1t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssh2-1t64@1.11.1-1ubuntu0.25.10.1?
│                       │       │                  │       arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : a14a55ea43469cd7 
│                       │       ├ InstalledVersion: 1.11.1-1ubuntu0.25.10.1 
│                       │       ├ FixedVersion    : 1.11.1-1ubuntu0.25.10.2 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-15661 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:acd5acc523512df97f1bee176f1f9ebe55d482cb5e44dbe8d497
│                       │       │                   0a84ae39efcf 
│                       │       ├ Title           : libssh2: libssh2: Information disclosure and denial of
│                       │       │                   service via crafted SFTP response 
│                       │       ├ Description     : libssh2 through 1.11.1, fixed in commit 2dae302, contains
│                       │       │                   an out-of-bounds heap read vulnerability in the
│                       │       │                   sftp_symlink() function in src/sftp.c that allows a
│                       │       │                   malicious SSH server or man-in-the-middle attacker to
│                       │       │                   disclose heap memory contents or cause a crash by sending a
│                       │       │                    crafted SSH_FXP_NAME response. Attackers can supply a
│                       │       │                   link_len value larger than the actual packet data in
│                       │       │                   SSH_FXP_NAME responses for SFTP READLINK and REALPATH
│                       │       │                   operations, triggering a heap buffer over-read of up to
│                       │       │                   target_len minus one bytes due to the missing validation of
│                       │       │                    available packet buffer size before the memcpy
│                       │       │                   operation. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ╭ nvd   : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:
│                       │       │                  │        │           N/A:H 
│                       │       │                  │        ╰ V3Score : 6.5 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2025-15661 
│                       │       │                  ├ [1]: https://github.com/libssh2/libssh2/commit/2dae3024897
│                       │       │                  │      e1898d389835151f4e9606227721d 
│                       │       │                  ├ [2]: https://github.com/libssh2/libssh2/pull/1705 
│                       │       │                  ├ [3]: https://github.com/libssh2/libssh2/pull/1717 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2025-15661 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8486-1 
│                       │       │                  ├ [6]: https://www.cve.org/CVERecord?id=CVE-2025-15661 
│                       │       │                  ╰ [7]: https://www.vulncheck.com/advisories/libssh2-heap-buf
│                       │       │                         fer-over-read-via-sftp-symlink-in-sftp-c 
│                       │       ├ PublishedDate   : 2026-06-18T21:16:27.143Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T02:35:13.663Z 
│                       ├ [59]  ╭ VulnerabilityID : CVE-2026-55199 
│                       │       ├ PkgID           : libssh2-1t64@1.11.1-1ubuntu0.25.10.1 
│                       │       ├ PkgName         : libssh2-1t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssh2-1t64@1.11.1-1ubuntu0.25.10.1?
│                       │       │                  │       arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : a14a55ea43469cd7 
│                       │       ├ InstalledVersion: 1.11.1-1ubuntu0.25.10.1 
│                       │       ├ FixedVersion    : 1.11.1-1ubuntu0.25.10.2 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55199 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a7660850abc6b6ff499bbaa2b477b041bc210f977b0ee87fb3c0
│                       │       │                   9247d5239b39 
│                       │       ├ Title           : libssh2: libssh2: Denial of Service via crafted
│                       │       │                   SSH_MSG_EXT_INFO message 
│                       │       ├ Description     : libssh2 through 1.11.1, fixed in commit 1762685, contains a
│                       │       │                    pre-authentication denial of service vulnerability in the
│                       │       │                   SSH_MSG_EXT_INFO handler in src/packet.c that allows a
│                       │       │                   malicious SSH server to cause a client CPU exhaustion loop
│                       │       │                   by sending a crafted extension count value. A malicious
│                       │       │                   server can set nr_extensions to 0xFFFFFFFF during key
│                       │       │                   exchange, causing the client to spin in a tight CPU loop
│                       │       │                   for over 60 seconds because return values from
│                       │       │                   _libssh2_get_string() are unchecked and the session timeout
│                       │       │                    does not apply to CPU-bound loops. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-835 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           N/A:H 
│                       │       │                  │        ╰ V3Score : 7.5 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.9 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55199 
│                       │       │                  ├ [1]: https://github.com/libssh2/libssh2/commit/17626857d20
│                       │       │                  │      b3c9a1addfa45979dadcee1cd84a4 
│                       │       │                  ├ [2]: https://github.com/libssh2/libssh2/pull/1864 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-55199 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8486-1 
│                       │       │                  ├ [5]: https://www.cve.org/CVERecord?id=CVE-2026-55199 
│                       │       │                  ╰ [6]: https://www.vulncheck.com/advisories/libssh2-pre-auth
│                       │       │                         entication-dos-via-ssh-msg-ext-info-handler 
│                       │       ├ PublishedDate   : 2026-06-17T20:17:28.52Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T19:16:37.353Z 
│                       ├ [60]  ╭ VulnerabilityID : CVE-2026-55200 
│                       │       ├ PkgID           : libssh2-1t64@1.11.1-1ubuntu0.25.10.1 
│                       │       ├ PkgName         : libssh2-1t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssh2-1t64@1.11.1-1ubuntu0.25.10.1?
│                       │       │                  │       arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : a14a55ea43469cd7 
│                       │       ├ InstalledVersion: 1.11.1-1ubuntu0.25.10.1 
│                       │       ├ FixedVersion    : 1.11.1-1ubuntu0.25.10.2 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55200 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:be37bc4edc0bfcd7611928100576b2a16c5645d845a3b6ebcebd
│                       │       │                   1181072e0392 
│                       │       ├ Title           : libssh2: libssh2 - Out-of-Bounds Write via Unchecked
│                       │       │                   packet_length in transport.c 
│                       │       ├ Description     : libssh2 through 1.11.1, fixed in commit 7acf3df contains an
│                       │       │                    out-of-bounds write vulnerability in ssh2_transport_read()
│                       │       │                    that fails to enforce upper bounds on packet_length field.
│                       │       │                    Remote attackers can send crafted SSH packets with
│                       │       │                   excessively large packet_length values to corrupt heap
│                       │       │                   memory and achieve remote code execution. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-680 
│                       │       ├ VendorSeverity   ╭ azure : 3 
│                       │       │                  ├ nvd   : 3 
│                       │       │                  ├ photon: 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:
│                       │       │                  │        │           H/A:L 
│                       │       │                  │        ╰ V3Score : 8.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                           │           H/A:L 
│                       │       │                           ╰ V3Score : 7.1 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55200 
│                       │       │                  ├ [1]: https://github.com/libssh2/libssh2/commit/97acf3dfda8
│                       │       │                  │      0c91c3a8c9f2372546301d4a1a7a8 
│                       │       │                  ├ [2]: https://github.com/libssh2/libssh2/pull/2052 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-55200 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8486-1 
│                       │       │                  ├ [5]: https://web.archive.org/web/20260623211210/https://gi
│                       │       │                  │      thub.com/bikini/exploitarium/tree/main/libssh2-cve-20
│                       │       │                  │      26-55200-poc 
│                       │       │                  ├ [6]: https://www.cve.org/CVERecord?id=CVE-2026-55200 
│                       │       │                  ╰ [7]: https://www.vulncheck.com/advisories/libssh2-out-of-b
│                       │       │                         ounds-write-via-unchecked-packet-length-in-transport-
│                       │       │                         c 
│                       │       ├ PublishedDate   : 2026-06-17T20:17:28.667Z 
│                       │       ╰ LastModifiedDate: 2026-07-01T05:16:22.513Z 
│                       ├ [61]  ╭ VulnerabilityID : CVE-2026-40228 
│                       │       ├ PkgID           : libsystemd0@257.9-0ubuntu2.5 
│                       │       ├ PkgName         : libsystemd0 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@257.9-0ubuntu2.5?arch=amd
│                       │       │                  │       64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ec55cdfad517f3cc 
│                       │       ├ InstalledVersion: 257.9-0ubuntu2.5 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4152ff4537707037daccb65b93f08e7603402989f9f42f95309c
│                       │       │                   efa606a7afbb 
│                       │       ├ Title           : systemd: systemd-journald: Unintended output to user
│                       │       │                   terminals via logger command 
│                       │       ├ Description     : In systemd 259, systemd-journald can send ANSI escape
│                       │       │                   sequences to the terminals of arbitrary users when a
│                       │       │                   "logger -p emerg" command is executed, if ForwardToWall=yes
│                       │       │                    is set. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-669 
│                       │       ├ VendorSeverity   ╭ nvd   : 1 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 1 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 3.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 2.9 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/05/1 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-40228 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-40228 
│                       │       │                  ├ [3]: https://www.cve.org/CVERecord?id=CVE-2026-40228 
│                       │       │                  ╰ [4]: https://www.openwall.com/lists/oss-security/2026/04/0
│                       │       │                         8/1 
│                       │       ├ PublishedDate   : 2026-04-10T16:16:33.753Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:44:53.31Z 
│                       ├ [62]  ╭ VulnerabilityID : CVE-2026-40228 
│                       │       ├ PkgID           : libudev1@257.9-0ubuntu2.5 
│                       │       ├ PkgName         : libudev1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@257.9-0ubuntu2.5?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : f211373f8a95c023 
│                       │       ├ InstalledVersion: 257.9-0ubuntu2.5 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bbcc0c81770673b9cb4179f065ecac9a6bacfc0a29ecadebd855
│                       │       │                   d1db3179bae4 
│                       │       ├ Title           : systemd: systemd-journald: Unintended output to user
│                       │       │                   terminals via logger command 
│                       │       ├ Description     : In systemd 259, systemd-journald can send ANSI escape
│                       │       │                   sequences to the terminals of arbitrary users when a
│                       │       │                   "logger -p emerg" command is executed, if ForwardToWall=yes
│                       │       │                    is set. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-669 
│                       │       ├ VendorSeverity   ╭ nvd   : 1 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 1 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 3.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 2.9 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/05/1 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-40228 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-40228 
│                       │       │                  ├ [3]: https://www.cve.org/CVERecord?id=CVE-2026-40228 
│                       │       │                  ╰ [4]: https://www.openwall.com/lists/oss-security/2026/04/0
│                       │       │                         8/1 
│                       │       ├ PublishedDate   : 2026-04-10T16:16:33.753Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:44:53.31Z 
│                       ├ [63]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libuuid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 23db7c315eddf1f4 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:da1796babfb64413836c2aac8290f034c64f86a9d90fa1508ed9
│                       │       │                   6523aa07d81d 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [64]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libuuid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 23db7c315eddf1f4 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e179f9288a92746e9a9b559c22a089c46e122290654a7e1bf7c8
│                       │       │                   23a780946fa4 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [65]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:9a6f3b6c8a43fee722793c826177bff264ec128dc0457aa5045f
│                       │       │                   6b8aeec7a7a2 
│                       │       ├ Title           : glibc: glibc: Denial of Service via iconv() function with
│                       │       │                   specific character sets 
│                       │       ├ Description     : The iconv() function in the GNU C Library versions 2.43 and
│                       │       │                    earlier may crash due to an assertion failure when
│                       │       │                   converting inputs from the IBM1390 or IBM1399 character
│                       │       │                   sets, which may be used to remotely crash an application.
│                       │       │                   
│                       │       │                   This vulnerability can be trivially mitigated by removing
│                       │       │                   the IBM1390 and IBM1399 character sets from systems that do
│                       │       │                    not need them. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-617 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 3 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:L 
│                       │       │                           ╰ V3Score : 5.3 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://inbox.sourceware.org/libc-announce/76814edf-
│                       │       │                  │       cf7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │       │                  ├ [14]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │       │                  ├ [15]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │       │                  ├ [16]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │       │                  ├ [17]: https://packages.fedoraproject.org/pkgs/glibc/glibc-
│                       │       │                  │       gconv-extra/ 
│                       │       │                  ├ [18]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │       │                  ├ [19]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007 
│                       │       │                  ├ [20]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │       │                  ╰ [21]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │       ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:55:54.12Z 
│                       ├ [66]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:224d31844f556c4ad825d2523e2ab10893a99eb9cfddf301d6e1
│                       │       │                   fd4c0f5b9f1c 
│                       │       ├ Title           : glibc: glibc: Incorrect DNS response parsing via crafted
│                       │       │                   DNS server response 
│                       │       ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │       │                   nsswitch.conf that specifies the library's DNS backend in
│                       │       │                   the GNU C Library version 2.34 to version 2.43 could, with
│                       │       │                   a crafted response from the configured DNS server, result
│                       │       │                   in a violation of the DNS specification that causes the
│                       │       │                   application to treat a non-answer section of the DNS
│                       │       │                   response as a valid answer. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ azure      : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 3 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2026-4437.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │       │                  ├ [15]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │       │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │       │                  ├ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │       │                  ╰ [18]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:56:34.227Z 
│                       ├ [67]  ╭ VulnerabilityID : CVE-2026-4438 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a4553c04a223d3043e19d3b4e73d4285b55d2d118e520383d97a
│                       │       │                   bc5c729b50e3 
│                       │       ├ Title           : glibc: glibc: Invalid DNS hostname returned via
│                       │       │                   gethostbyaddr functions 
│                       │       ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │       │                   nsswitch.conf that specifies the library's DNS backend in
│                       │       │                   the GNU C library version 2.34 to version 2.43 could result
│                       │       │                    in an invalid DNS hostname being returned to the caller in
│                       │       │                    violation of the DNS specification. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-20 
│                       │       │                  ╰ [1]: CWE-88 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ azure      : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 4 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [7] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [10]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [11]: https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │       │                  ├ [12]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │       │                  ├ [13]: https://linux.oracle.com/cve/CVE-2026-4438.html 
│                       │       │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │       │                  ├ [15]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │       │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │       │                  ├ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │       │                  ╰ [18]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:56:34.367Z 
│                       ├ [68]  ╭ VulnerabilityID : CVE-2026-5435 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:9688b2068457f703a95787840e919fdaa81a194e4005cbb8016f
│                       │       │                   cd37068b8d84 
│                       │       ├ Title           : glibc: glibc: Out-of-bounds write via TSIG record processing 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.2 and newer fail
│                       │       │                   to enforce the caller-supplied buffer length, and can
│                       │       │                   result in an out-of-bounds write when printing TSIG
│                       │       │                   records. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.9 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-5435 
│                       │       │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.1777546
│                       │       │                  │      194.git.fweimer@redhat.com/ 
│                       │       │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-2
│                       │       │                  │      76f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-5435 
│                       │       │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34033 
│                       │       │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │       │                  │      f=advisories/GLIBC-SA-2026-0011 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5435 
│                       │       ├ PublishedDate   : 2026-04-28T13:19:22.29Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:59:01.13Z 
│                       ├ [69]  ╭ VulnerabilityID : CVE-2026-6238 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:171fd12e4476bf79a04219813651858061486af6570e62a4d65c
│                       │       │                   6175fb941d48 
│                       │       ├ Title           : glibc: glibc: Application crash or uninitialized memory
│                       │       │                   read via crafted DNS response 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.0.1 to version
│                       │       │                   2.43 fail to validate the RDATA content against the RDATA
│                       │       │                   length in a DNS response when processing A6, CERT, LOC,
│                       │       │                   TKEY or TSIG records, which may allow an attacker to craft
│                       │       │                   a DNS response, causing a target application to crash or
│                       │       │                   read uninitialized memory.
│                       │       │                   
│                       │       │                   These functions are for application debugging only and
│                       │       │                   hence not in the path of code executed by the DNS resolver.
│                       │       │                     Further, they have been deprecated since version 2.34 and
│                       │       │                    should not be used by any new applications.  Applications
│                       │       │                   should consider porting away from these interfaces since
│                       │       │                   they may be removed in future versions. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-126 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-6238 
│                       │       │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.1777546
│                       │       │                  │      194.git.fweimer@redhat.com/ 
│                       │       │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-2
│                       │       │                  │      76f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-6238 
│                       │       │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34069 
│                       │       │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │       │                  │      f=advisories/GLIBC-SA-2026-0012 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6238 
│                       │       ├ PublishedDate   : 2026-04-28T19:37:47.523Z 
│                       │       ╰ LastModifiedDate: 2026-06-19T21:17:02.62Z 
│                       ├ [70]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ PkgName         : login 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.
│                       │       │                  │       2?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │       ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fc770e4c0e617c635e67c218ee811945bf972dc52089b53f6206
│                       │       │                   b29d9025a40a 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [71]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ PkgName         : login 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.
│                       │       │                  │       2?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │       ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:45a697e2f3aea9b9d8bf73be591f4e20da590e8ed3b0de25522a
│                       │       │                   2db7b6a157c1 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [72]  ╭ VulnerabilityID : CVE-2024-56433 
│                       │       ├ PkgID           : login.defs@1:4.17.4-2ubuntu2 
│                       │       ├ PkgName         : login.defs 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu2?arch=all&d
│                       │       │                  │       istro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 685157e74dbd875c 
│                       │       ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bb8689e9fbc6ab22a936fd0e91ddbcadedd9ce3f5757b5b245d6
│                       │       │                   b569c69d2ce2 
│                       │       ├ Title           : shadow-utils: Default subordinate ID configuration in
│                       │       │                   /etc/login.defs could lead to compromise 
│                       │       ├ Description     : shadow-utils (aka shadow) 4.4 through 4.17.0 establishes a
│                       │       │                   default /etc/subuid behavior (e.g., uid 100000 through
│                       │       │                   165535 for the first user account) that can realistically
│                       │       │                   conflict with the uids of users defined on locally
│                       │       │                   administered networks, potentially leading to account
│                       │       │                   takeover, e.g., by leveraging newuidmap for access to an
│                       │       │                   NFS home directory (or same-host resources in the case of
│                       │       │                   remote logins by these local network users). NOTE: it may
│                       │       │                   also be argued that system administrators should not have
│                       │       │                   assigned uids, within local networks, that are within the
│                       │       │                   range that can occur in /etc/subuid. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-1188 
│                       │       ├ VendorSeverity   ╭ alma       : 1 
│                       │       │                  ├ azure      : 1 
│                       │       │                  ├ oracle-oval: 1 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 1 
│                       │       │                  ╰ ubuntu     : 1 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.6 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2025:20559 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2024-56433 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2334165 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2334165 
│                       │       │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       024-56433 
│                       │       │                  ├ [5] : https://errata.almalinux.org/9/ALSA-2025-20559.html 
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20559 
│                       │       │                  ├ [7] : https://github.com/shadow-maint/shadow/blob/e2512d57
│                       │       │                  │       41d4a44bdd81a8c2d0029b6222728cf0/etc/login.defs#L238
│                       │       │                  │       -L241 
│                       │       │                  ├ [8] : https://github.com/shadow-maint/shadow/issues/1157 
│                       │       │                  ├ [9] : https://github.com/shadow-maint/shadow/releases/tag/
│                       │       │                  │       4.4 
│                       │       │                  ├ [10]: https://linux.oracle.com/cve/CVE-2024-56433.html 
│                       │       │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2025-20559-0.html 
│                       │       │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2024-56433 
│                       │       │                  ╰ [13]: https://www.cve.org/CVERecord?id=CVE-2024-56433 
│                       │       ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [73]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : mount 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : f2821a9fde7aa805 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0f95250fa79e823ce61119af7b1225fddfe6dc931fd2306df5fd
│                       │       │                   4147adccc444 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [74]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : mount 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : f2821a9fde7aa805 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2e1ff9f2566a94640fda08c54758325806d235a7c0269f47714c
│                       │       │                   add3a477ceb2 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [75]  ╭ VulnerabilityID : CVE-2024-56433 
│                       │       ├ PkgID           : passwd@1:4.17.4-2ubuntu2 
│                       │       ├ PkgName         : passwd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu2?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 2d87ef360f209a3f 
│                       │       ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:32385986b023d0d37a0d63b701165165e7f16f7a6f83d36afaf4
│                       │       │                   ec0a4567ece6 
│                       │       ├ Title           : shadow-utils: Default subordinate ID configuration in
│                       │       │                   /etc/login.defs could lead to compromise 
│                       │       ├ Description     : shadow-utils (aka shadow) 4.4 through 4.17.0 establishes a
│                       │       │                   default /etc/subuid behavior (e.g., uid 100000 through
│                       │       │                   165535 for the first user account) that can realistically
│                       │       │                   conflict with the uids of users defined on locally
│                       │       │                   administered networks, potentially leading to account
│                       │       │                   takeover, e.g., by leveraging newuidmap for access to an
│                       │       │                   NFS home directory (or same-host resources in the case of
│                       │       │                   remote logins by these local network users). NOTE: it may
│                       │       │                   also be argued that system administrators should not have
│                       │       │                   assigned uids, within local networks, that are within the
│                       │       │                   range that can occur in /etc/subuid. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-1188 
│                       │       ├ VendorSeverity   ╭ alma       : 1 
│                       │       │                  ├ azure      : 1 
│                       │       │                  ├ oracle-oval: 1 
│                       │       │                  ├ redhat     : 1 
│                       │       │                  ├ rocky      : 1 
│                       │       │                  ╰ ubuntu     : 1 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.6 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2025:20559 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2024-56433 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2334165 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2334165 
│                       │       │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       024-56433 
│                       │       │                  ├ [5] : https://errata.almalinux.org/9/ALSA-2025-20559.html 
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20559 
│                       │       │                  ├ [7] : https://github.com/shadow-maint/shadow/blob/e2512d57
│                       │       │                  │       41d4a44bdd81a8c2d0029b6222728cf0/etc/login.defs#L238
│                       │       │                  │       -L241 
│                       │       │                  ├ [8] : https://github.com/shadow-maint/shadow/issues/1157 
│                       │       │                  ├ [9] : https://github.com/shadow-maint/shadow/releases/tag/
│                       │       │                  │       4.4 
│                       │       │                  ├ [10]: https://linux.oracle.com/cve/CVE-2024-56433.html 
│                       │       │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2025-20559-0.html 
│                       │       │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2024-56433 
│                       │       │                  ╰ [13]: https://www.cve.org/CVERecord?id=CVE-2024-56433 
│                       │       ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [76]  ╭ VulnerabilityID : CVE-2026-42496 
│                       │       ├ PkgID           : perl@5.40.1-6build1 
│                       │       ├ PkgName         : perl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/perl@5.40.1-6build1?arch=amd64&distro
│                       │       │                  │       =ubuntu-25.10 
│                       │       │                  ╰ UID : 287c0ac4b68f3d3b 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42496 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2436944bd7ea50740aa15c9f33b6e45b6f51da9bd16fb62eccad
│                       │       │                   fb4af5073e00 
│                       │       ├ Title           : perl-archive-tar: perl-archive-tar: Path traversal via
│                       │       │                   crafted symlinks allows arbitrary file access 
│                       │       ├ Description     : Archive::Tar versions before 3.08 for Perl extract symlinks
│                       │       │                    with attacker controlled targets outside the extraction
│                       │       │                   directory.
│                       │       │                   
│                       │       │                   _make_special_file() passes the tar header's linkname to
│                       │       │                   symlink() without validating it against absolute paths or
│                       │       │                   .. segments. The secure-extract mode check that guards
│                       │       │                   regular file extraction does not cover the symlink target.
│                       │       │                   A subsequent open through the extracted name reads or
│                       │       │                   writes the attacker chosen path. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ╰ [1]: CWE-22 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ nvd        : 4 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ redhat     : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:
│                       │       │                  │        │           H/A:N 
│                       │       │                  │        ╰ V3Score : 9.1 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 8.2 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:30851 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:30852 
│                       │       │                  ├ [2] : https://access.redhat.com/errata/RHSA-2026:30856 
│                       │       │                  ├ [3] : https://access.redhat.com/errata/RHSA-2026:30857 
│                       │       │                  ├ [4] : https://access.redhat.com/security/cve/CVE-2026-42496 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2481314 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2481314 
│                       │       │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-30856.html 
│                       │       │                  ├ [8] : https://github.com/jib/archive-tar-new/commit/17c873
│                       │       │                  │       492a05eddc0de18c1485e0b2cccd5a9158.patch 
│                       │       │                  ├ [9] : https://linux.oracle.com/cve/CVE-2026-42496.html 
│                       │       │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-30856.html 
│                       │       │                  ├ [11]: https://lists.security.metacpan.org/cve-announce/msg
│                       │       │                  │       /40396459/ 
│                       │       │                  ├ [12]: https://metacpan.org/release/BINGOS/Archive-Tar-3.08
│                       │       │                  │       /changes 
│                       │       │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-42496 
│                       │       │                  ├ [14]: https://security.access.redhat.com/data/csaf/v2/vex/
│                       │       │                  │       2026/cve-2026-42496.json 
│                       │       │                  ├ [15]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ├ [16]: https://www.cve.org/CVERecord?id=CVE-2026-42496 
│                       │       │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-42497 
│                       │       ├ PublishedDate   : 2026-05-26T02:16:40.13Z 
│                       │       ╰ LastModifiedDate: 2026-06-30T03:19:37.663Z 
│                       ├ [77]  ╭ VulnerabilityID : CVE-2026-8376 
│                       │       ├ PkgID           : perl@5.40.1-6build1 
│                       │       ├ PkgName         : perl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/perl@5.40.1-6build1?arch=amd64&distro
│                       │       │                  │       =ubuntu-25.10 
│                       │       │                  ╰ UID : 287c0ac4b68f3d3b 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8376 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:772f7bf2f23dab27bf5cda16cdd1d4791fb223ed820c8fc48227
│                       │       │                   203da5b6abab 
│                       │       ├ Title           : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compili ... 
│                       │       ├ Description     : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compiling regular expressions with a repeated fixed
│                       │       │                   string on 32-bit builds.
│                       │       │                   
│                       │       │                   Perl_study_chunk in regcomp_study.c checked the size of the
│                       │       │                    joined substring buffer in characters rather than bytes.
│                       │       │                   For a quantified fixed substring with a large minimum
│                       │       │                   count, the byte length mincount * l could overflow SSize_t,
│                       │       │                    producing an undersized SvGROW allocation; the subsequent
│                       │       │                   copy writes past the end of the buffer.
│                       │       │                   A caller that compiles an attacker-controlled regular
│                       │       │                   expression on a 32-bit perl build triggers a heap buffer
│                       │       │                   overflow at compile time. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-680 
│                       │       ├ VendorSeverity   ╭ amazon: 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ nvd   : 4 
│                       │       │                  ├ photon: 4 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 9.8 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/26/1 
│                       │       │                  ├ [1]: https://github.com/Perl/perl5/commit/5e7f119eb2bb1181
│                       │       │                  │      be908701f22bf7068e722f1c.patch 
│                       │       │                  ├ [2]: https://github.com/Perl/perl5/pull/24433 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-8376 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-8376 
│                       │       ├ PublishedDate   : 2026-05-26T00:16:57.15Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T11:03:51.843Z 
│                       ├ [78]  ╭ VulnerabilityID : CVE-2026-42496 
│                       │       ├ PkgID           : perl-base@5.40.1-6build1 
│                       │       ├ PkgName         : perl-base 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/perl-base@5.40.1-6build1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 44e80c5c00d2cfec 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42496 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fe2274772981b430a84d6cea56a60d6963bdd482e24fe5bab4e4
│                       │       │                   1e7a624755b6 
│                       │       ├ Title           : perl-archive-tar: perl-archive-tar: Path traversal via
│                       │       │                   crafted symlinks allows arbitrary file access 
│                       │       ├ Description     : Archive::Tar versions before 3.08 for Perl extract symlinks
│                       │       │                    with attacker controlled targets outside the extraction
│                       │       │                   directory.
│                       │       │                   
│                       │       │                   _make_special_file() passes the tar header's linkname to
│                       │       │                   symlink() without validating it against absolute paths or
│                       │       │                   .. segments. The secure-extract mode check that guards
│                       │       │                   regular file extraction does not cover the symlink target.
│                       │       │                   A subsequent open through the extracted name reads or
│                       │       │                   writes the attacker chosen path. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ╰ [1]: CWE-22 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ nvd        : 4 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ redhat     : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:
│                       │       │                  │        │           H/A:N 
│                       │       │                  │        ╰ V3Score : 9.1 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 8.2 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:30851 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:30852 
│                       │       │                  ├ [2] : https://access.redhat.com/errata/RHSA-2026:30856 
│                       │       │                  ├ [3] : https://access.redhat.com/errata/RHSA-2026:30857 
│                       │       │                  ├ [4] : https://access.redhat.com/security/cve/CVE-2026-42496 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2481314 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2481314 
│                       │       │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-30856.html 
│                       │       │                  ├ [8] : https://github.com/jib/archive-tar-new/commit/17c873
│                       │       │                  │       492a05eddc0de18c1485e0b2cccd5a9158.patch 
│                       │       │                  ├ [9] : https://linux.oracle.com/cve/CVE-2026-42496.html 
│                       │       │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-30856.html 
│                       │       │                  ├ [11]: https://lists.security.metacpan.org/cve-announce/msg
│                       │       │                  │       /40396459/ 
│                       │       │                  ├ [12]: https://metacpan.org/release/BINGOS/Archive-Tar-3.08
│                       │       │                  │       /changes 
│                       │       │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-42496 
│                       │       │                  ├ [14]: https://security.access.redhat.com/data/csaf/v2/vex/
│                       │       │                  │       2026/cve-2026-42496.json 
│                       │       │                  ├ [15]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ├ [16]: https://www.cve.org/CVERecord?id=CVE-2026-42496 
│                       │       │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-42497 
│                       │       ├ PublishedDate   : 2026-05-26T02:16:40.13Z 
│                       │       ╰ LastModifiedDate: 2026-06-30T03:19:37.663Z 
│                       ├ [79]  ╭ VulnerabilityID : CVE-2026-8376 
│                       │       ├ PkgID           : perl-base@5.40.1-6build1 
│                       │       ├ PkgName         : perl-base 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/perl-base@5.40.1-6build1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 44e80c5c00d2cfec 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8376 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f6b42f2679201423a3947d4f820b471540897a6328a0224f9479
│                       │       │                   814ca7f211aa 
│                       │       ├ Title           : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compili ... 
│                       │       ├ Description     : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compiling regular expressions with a repeated fixed
│                       │       │                   string on 32-bit builds.
│                       │       │                   
│                       │       │                   Perl_study_chunk in regcomp_study.c checked the size of the
│                       │       │                    joined substring buffer in characters rather than bytes.
│                       │       │                   For a quantified fixed substring with a large minimum
│                       │       │                   count, the byte length mincount * l could overflow SSize_t,
│                       │       │                    producing an undersized SvGROW allocation; the subsequent
│                       │       │                   copy writes past the end of the buffer.
│                       │       │                   A caller that compiles an attacker-controlled regular
│                       │       │                   expression on a 32-bit perl build triggers a heap buffer
│                       │       │                   overflow at compile time. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-680 
│                       │       ├ VendorSeverity   ╭ amazon: 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ nvd   : 4 
│                       │       │                  ├ photon: 4 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 9.8 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/26/1 
│                       │       │                  ├ [1]: https://github.com/Perl/perl5/commit/5e7f119eb2bb1181
│                       │       │                  │      be908701f22bf7068e722f1c.patch 
│                       │       │                  ├ [2]: https://github.com/Perl/perl5/pull/24433 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-8376 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-8376 
│                       │       ├ PublishedDate   : 2026-05-26T00:16:57.15Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T11:03:51.843Z 
│                       ├ [80]  ╭ VulnerabilityID : CVE-2026-42496 
│                       │       ├ PkgID           : perl-modules-5.40@5.40.1-6build1 
│                       │       ├ PkgName         : perl-modules-5.40 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/perl-modules-5.40@5.40.1-6build1?arch
│                       │       │                  │       =all&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 66ddcd30a076a03 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42496 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:182aa510c23e8d5e5ecc844dc84bed9417c185b4f0cdc7a06c9a
│                       │       │                   ba38193b23dd 
│                       │       ├ Title           : perl-archive-tar: perl-archive-tar: Path traversal via
│                       │       │                   crafted symlinks allows arbitrary file access 
│                       │       ├ Description     : Archive::Tar versions before 3.08 for Perl extract symlinks
│                       │       │                    with attacker controlled targets outside the extraction
│                       │       │                   directory.
│                       │       │                   
│                       │       │                   _make_special_file() passes the tar header's linkname to
│                       │       │                   symlink() without validating it against absolute paths or
│                       │       │                   .. segments. The secure-extract mode check that guards
│                       │       │                   regular file extraction does not cover the symlink target.
│                       │       │                   A subsequent open through the extracted name reads or
│                       │       │                   writes the attacker chosen path. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ╰ [1]: CWE-22 
│                       │       ├ VendorSeverity   ╭ alma       : 3 
│                       │       │                  ├ amazon     : 3 
│                       │       │                  ├ azure      : 3 
│                       │       │                  ├ nvd        : 4 
│                       │       │                  ├ oracle-oval: 3 
│                       │       │                  ├ redhat     : 3 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:
│                       │       │                  │        │           H/A:N 
│                       │       │                  │        ╰ V3Score : 9.1 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 8.2 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:30851 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:30852 
│                       │       │                  ├ [2] : https://access.redhat.com/errata/RHSA-2026:30856 
│                       │       │                  ├ [3] : https://access.redhat.com/errata/RHSA-2026:30857 
│                       │       │                  ├ [4] : https://access.redhat.com/security/cve/CVE-2026-42496 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/2481314 
│                       │       │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2481314 
│                       │       │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-30856.html 
│                       │       │                  ├ [8] : https://github.com/jib/archive-tar-new/commit/17c873
│                       │       │                  │       492a05eddc0de18c1485e0b2cccd5a9158.patch 
│                       │       │                  ├ [9] : https://linux.oracle.com/cve/CVE-2026-42496.html 
│                       │       │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-30856.html 
│                       │       │                  ├ [11]: https://lists.security.metacpan.org/cve-announce/msg
│                       │       │                  │       /40396459/ 
│                       │       │                  ├ [12]: https://metacpan.org/release/BINGOS/Archive-Tar-3.08
│                       │       │                  │       /changes 
│                       │       │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-42496 
│                       │       │                  ├ [14]: https://security.access.redhat.com/data/csaf/v2/vex/
│                       │       │                  │       2026/cve-2026-42496.json 
│                       │       │                  ├ [15]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ├ [16]: https://www.cve.org/CVERecord?id=CVE-2026-42496 
│                       │       │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-42497 
│                       │       ├ PublishedDate   : 2026-05-26T02:16:40.13Z 
│                       │       ╰ LastModifiedDate: 2026-06-30T03:19:37.663Z 
│                       ├ [81]  ╭ VulnerabilityID : CVE-2026-8376 
│                       │       ├ PkgID           : perl-modules-5.40@5.40.1-6build1 
│                       │       ├ PkgName         : perl-modules-5.40 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/perl-modules-5.40@5.40.1-6build1?arch
│                       │       │                  │       =all&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 66ddcd30a076a03 
│                       │       ├ InstalledVersion: 5.40.1-6build1 
│                       │       ├ FixedVersion    : 5.40.1-6ubuntu0.1 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-8376 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:acc9d2fcc0805292a9373a10d5203e02c3703839056f2b0aea61
│                       │       │                   f130fc69024d 
│                       │       ├ Title           : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compili ... 
│                       │       ├ Description     : Perl versions through 5.43.10 have a heap buffer overflow
│                       │       │                   when compiling regular expressions with a repeated fixed
│                       │       │                   string on 32-bit builds.
│                       │       │                   
│                       │       │                   Perl_study_chunk in regcomp_study.c checked the size of the
│                       │       │                    joined substring buffer in characters rather than bytes.
│                       │       │                   For a quantified fixed substring with a large minimum
│                       │       │                   count, the byte length mincount * l could overflow SSize_t,
│                       │       │                    producing an undersized SvGROW allocation; the subsequent
│                       │       │                   copy writes past the end of the buffer.
│                       │       │                   A caller that compiles an attacker-controlled regular
│                       │       │                   expression on a 32-bit perl build triggers a heap buffer
│                       │       │                   overflow at compile time. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-680 
│                       │       ├ VendorSeverity   ╭ amazon: 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ nvd   : 4 
│                       │       │                  ├ photon: 4 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 9.8 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/26/1 
│                       │       │                  ├ [1]: https://github.com/Perl/perl5/commit/5e7f119eb2bb1181
│                       │       │                  │      be908701f22bf7068e722f1c.patch 
│                       │       │                  ├ [2]: https://github.com/Perl/perl5/pull/24433 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-8376 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8467-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-8376 
│                       │       ├ PublishedDate   : 2026-05-26T00:16:57.15Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T11:03:51.843Z 
│                       ├ [82]  ╭ VulnerabilityID : CVE-2026-35338 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35338 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8e7d840ed201385b03cad365126b4b0980ddb97973abc2b9004f
│                       │       │                   2af389436ad9 
│                       │       ├ Title           : A vulnerability in the chmod utility of uutils coreutils
│                       │       │                   allows users  ... 
│                       │       ├ Description     : A vulnerability in the chmod utility of uutils coreutils
│                       │       │                   allows users to bypass the --preserve-root safety
│                       │       │                   mechanism. The implementation only validates if the target
│                       │       │                   path is literally / and does not canonicalize the path. An
│                       │       │                   attacker or accidental user can use path variants such as
│                       │       │                   /../ or symbolic links to execute destructive recursive
│                       │       │                   operations (e.g., chmod -R 000) on the entire root
│                       │       │                   filesystem, leading to system-wide permission loss and
│                       │       │                   potential complete system breakdown. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-22 
│                       │       ├ VendorSeverity   ╭ ghsa  : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:H/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 7.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/413055b378
│                       │       │                  │      fa6fe2299c5e5f538c8e6e841ab810 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10033 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35338 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35338 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:35.583Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.177Z 
│                       ├ [83]  ╭ VulnerabilityID : CVE-2026-35339 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35339 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:c648618f71b7343b0d904513571c5398f0fea2688704486ef575
│                       │       │                   96fb192b2c7e 
│                       │       ├ Title           : The recursive mode (-R) of the chmod utility in uutils
│                       │       │                   coreutils incor ... 
│                       │       ├ Description     : The recursive mode (-R) of the chmod utility in uutils
│                       │       │                   coreutils incorrectly handles exit codes when processing
│                       │       │                   multiple files. The final return value is determined solely
│                       │       │                    by the success or failure of the last file processed. This
│                       │       │                    allows the command to return an exit code of 0 (success)
│                       │       │                   even if errors were encountered on previous files, such as
│                       │       │                   'Operation not permitted'. Scripts relying on these exit
│                       │       │                   codes may proceed under a false sense of success while
│                       │       │                   sensitive files remain with restrictive or incorrect
│                       │       │                   permissions. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-253 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/abd581f62e
│                       │       │                  │      97d0b147306ac40eac13af71c6fbba 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/9793 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35339 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35339 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:35.767Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.29Z 
│                       ├ [84]  ╭ VulnerabilityID : CVE-2026-35340 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35340 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4d2c9e03c2b81ecf88b772bf68beef4e7233689532095d1f0525
│                       │       │                   7388341b7cb2 
│                       │       ├ Title           : A flaw in the ChownExecutor used by uutils coreutils chown
│                       │       │                   and chgrp c ... 
│                       │       ├ Description     : A flaw in the ChownExecutor used by uutils coreutils chown
│                       │       │                   and chgrp causes the utilities to return an incorrect exit
│                       │       │                   code during recursive operations. The final exit code is
│                       │       │                   determined only by the last file processed. If the last
│                       │       │                   operation succeeds, the command returns 0 even if earlier
│                       │       │                   ownership or group changes failed due to permission errors.
│                       │       │                    This can lead to security misconfigurations where
│                       │       │                   administrative scripts incorrectly assume that ownership
│                       │       │                   has been successfully transferred across a directory
│                       │       │                   tree. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-253 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/ebc08af9c3
│                       │       │                  │      4138f474b32ea0ef34bed3b086a3ed 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10035 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35340 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35340 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:35.923Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.393Z 
│                       ├ [85]  ╭ VulnerabilityID : CVE-2026-35341 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d7aa962eeb52a5711e85f84ea143f5dc1ca81533cff05c1c5613
│                       │       │                   a5b7b31d5180 
│                       │       ├ Title           : A vulnerability in uutils coreutils mkfifo allows for the
│                       │       │                   unauthorized ... 
│                       │       ├ Description     : A vulnerability in uutils coreutils mkfifo allows for the
│                       │       │                   unauthorized modification of permissions on existing files.
│                       │       │                    When mkfifo fails to create a FIFO because a file already
│                       │       │                   exists at the target path, it fails to terminate the
│                       │       │                   operation for that path and continues to execute a
│                       │       │                   follow-up set_permissions call. This results in the
│                       │       │                   existing file's permissions being changed to the default
│                       │       │                   mode (often 644 after umask), potentially exposing
│                       │       │                   sensitive files such as SSH private keys to other users on
│                       │       │                   the system. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-732 
│                       │       ├ VendorSeverity   ╭ ghsa  : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 7.1 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10020 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35341 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35341 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.06Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.5Z 
│                       ├ [86]  ╭ VulnerabilityID : CVE-2026-35342 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35342 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:7b0781da144648e7ef0fb8170d66bb49988d17559c49da68edad
│                       │       │                   6061b6792f01 
│                       │       ├ Title           : The mktemp utility in uutils coreutils fails to properly
│                       │       │                   handle an emp ... 
│                       │       ├ Description     : The mktemp utility in uutils coreutils fails to properly
│                       │       │                   handle an empty TMPDIR environment variable. Unlike GNU
│                       │       │                   mktemp, which falls back to /tmp when TMPDIR is an empty
│                       │       │                   string, the uutils implementation treats the empty string
│                       │       │                   as a valid path. This causes temporary files to be created
│                       │       │                   in the current working directory (CWD) instead of the
│                       │       │                   intended secure temporary directory. If the CWD is more
│                       │       │                   permissive or accessible to other users than /tmp, it may
│                       │       │                   lead to unintended information disclosure or unauthorized
│                       │       │                   access to temporary data. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-377 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/eb25ec328b
│                       │       │                  │      226d8fbbaa4058bf9187165bf06d51 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10566 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35342 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35342 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.217Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.61Z 
│                       ├ [87]  ╭ VulnerabilityID : CVE-2026-35343 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35343 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:aeb19d5ef6a1b827d32cda1b210d82342424c8ce4537fa469a83
│                       │       │                   0bad5744b654 
│                       │       ├ Title           : The cut utility in uutils coreutils incorrectly handles the
│                       │       │                    -s (only-d ... 
│                       │       ├ Description     : The cut utility in uutils coreutils incorrectly handles the
│                       │       │                    -s (only-delimited) option when a newline character is
│                       │       │                   specified as the delimiter. The implementation fails to
│                       │       │                   verify the only_delimited flag in the
│                       │       │                   cut_fields_newline_char_delim function, causing the utility
│                       │       │                    to print non-delimited lines that should have been
│                       │       │                   suppressed. This can lead to unexpected data being passed
│                       │       │                   to downstream scripts that rely on strict output
│                       │       │                   filtering. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-670 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/9bbb58b746
│                       │       │                  │      c41802278b0cba738eebbf21517cf7 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11143 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35343 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35343 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.357Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.723Z 
│                       ├ [88]  ╭ VulnerabilityID : CVE-2026-35344 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:749c6b0aa6b39c0cc1e2f5b555d72b9149e532f2f8316d017281
│                       │       │                   f46c3fc67c3a 
│                       │       ├ Title           : The dd utility in uutils coreutils suppresses errors during
│                       │       │                    file trunc ... 
│                       │       ├ Description     : The dd utility in uutils coreutils suppresses errors during
│                       │       │                    file truncation operations by unconditionally calling
│                       │       │                   Result::ok() on truncation attempts. While intended to
│                       │       │                   mimic GNU behavior for special files like /dev/null, the
│                       │       │                   uutils implementation also hides failures on regular files
│                       │       │                   and directories caused by full disks or read-only file
│                       │       │                   systems. This can lead to silent data corruption in backup
│                       │       │                   or migration scripts, as the utility may report a
│                       │       │                   successful operation even when the destination file
│                       │       │                   contains old or garbage data. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-252 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/9745 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35344 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35344 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.49Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.833Z 
│                       ├ [89]  ╭ VulnerabilityID : CVE-2026-35345 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f7df03dbc89adf0ab4e517e29e3c9284be56f7107bb35559d4b1
│                       │       │                   57dfc19d89d2 
│                       │       ├ Title           : A vulnerability in the tail utility of uutils coreutils
│                       │       │                   allows for the ... 
│                       │       ├ Description     : A vulnerability in the tail utility of uutils coreutils
│                       │       │                   allows for the exfiltration of sensitive file contents when
│                       │       │                    using the --follow=name option. Unlike GNU tail, the
│                       │       │                   uutils implementation continues to monitor a path after it
│                       │       │                   has been replaced by a symbolic link, subsequently
│                       │       │                   outputting the contents of the link's target. In
│                       │       │                   environments where a privileged user (e.g., root) monitors
│                       │       │                   a log directory, a local attacker with write access to that
│                       │       │                    directory can replace a log file with a symlink to a
│                       │       │                   sensitive system file (such as /etc/shadow), causing tail
│                       │       │                   to disclose the contents of the sensitive file. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ╰ [1]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 5.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10328 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35345 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35345 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.627Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:25.943Z 
│                       ├ [90]  ╭ VulnerabilityID : CVE-2026-35346 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35346 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:53841f7e5d83a24f8506dd6c5087c2b29c2838822fe0696dc4cc
│                       │       │                   9416a9bbbf30 
│                       │       ├ Title           : The comm utility in uutils coreutils silently corrupts data
│                       │       │                    by perform ... 
│                       │       ├ Description     : The comm utility in uutils coreutils silently corrupts data
│                       │       │                    by performing lossy UTF-8 conversion on all output lines.
│                       │       │                   The implementation uses String::from_utf8_lossy(), which
│                       │       │                   replaces invalid UTF-8 byte sequences with the Unicode
│                       │       │                   replacement character (U+FFFD). This behavior differs from
│                       │       │                   GNU comm, which processes raw bytes and preserves the
│                       │       │                   original input. This results in corrupted output when the
│                       │       │                   utility is used to compare binary files or files using
│                       │       │                   non-UTF-8 legacy encodings. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-176 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/b9372e509e
│                       │       │                  │      a9b278fe13763237067a261bb8c946 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/issues/10192 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/pull/10206 
│                       │       │                  ├ [4]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35346 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35346 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.76Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.057Z 
│                       ├ [91]  ╭ VulnerabilityID : CVE-2026-35347 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35347 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b5943988274d940b0c23c6a941ff4bcd2456ad7b098bd2d5975f
│                       │       │                   c7fc97785297 
│                       │       ├ Title           : The comm utility in uutils coreutils incorrectly consumes
│                       │       │                   data from no ... 
│                       │       ├ Description     : The comm utility in uutils coreutils incorrectly consumes
│                       │       │                   data from non-regular file inputs before performing
│                       │       │                   comparison operations. The are_files_identical function
│                       │       │                   opens and reads from both input paths to compare content
│                       │       │                   without first verifying if the paths refer to regular
│                       │       │                   files. If an input path is a FIFO or a pipe, this pre-read
│                       │       │                   operation drains the stream, leading to silent data loss
│                       │       │                   before the actual comparison logic is executed.
│                       │       │                   Additionally, the utility may hang indefinitely if it
│                       │       │                   attempts to pre-read from infinite streams like
│                       │       │                   /dev/zero. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-20 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 4.4 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/75f45e87e5
│                       │       │                  │      2ed95840494963ab9a28651165d56e 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/9545 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35347 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35347 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:36.903Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.167Z 
│                       ├ [92]  ╭ VulnerabilityID : CVE-2026-35348 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f68bacb597ea53dc9b3be6ab5867126e59d5251644c89755239a
│                       │       │                   a31b6229158d 
│                       │       ├ Title           : The sort utility in uutils coreutils is vulnerable to a
│                       │       │                   process panic  ... 
│                       │       ├ Description     : The sort utility in uutils coreutils is vulnerable to a
│                       │       │                   process panic when using the --files0-from option with
│                       │       │                   inputs containing non-UTF-8 filenames. The implementation
│                       │       │                   enforces UTF-8 encoding and utilizes expect(), causing an
│                       │       │                   immediate crash when encountering valid but non-UTF-8
│                       │       │                   paths. This diverges from GNU sort, which treats filenames
│                       │       │                   as raw bytes. A local attacker can exploit this to crash
│                       │       │                   the utility and disrupt automated pipelines. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-248 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/9696 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35348 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35348 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.04Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.27Z 
│                       ├ [93]  ╭ VulnerabilityID : CVE-2026-35349 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35349 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ef332af844b76d4776ad0d9215b9bde349f785c2a721bf78fdd5
│                       │       │                   c776b4fad209 
│                       │       ├ Title           : A vulnerability in the rm utility of uutils coreutils
│                       │       │                   allows a bypass  ... 
│                       │       ├ Description     : A vulnerability in the rm utility of uutils coreutils
│                       │       │                   allows a bypass of the --preserve-root protection. The
│                       │       │                   implementation uses a path-string check rather than
│                       │       │                   comparing device and inode numbers to identify the root
│                       │       │                   directory. An attacker or accidental user can bypass this
│                       │       │                   safeguard by using a symbolic link that resolves to the
│                       │       │                   root directory (e.g., /tmp/rootlink -> /), potentially
│                       │       │                   leading to the unintended recursive deletion of the entire
│                       │       │                   root filesystem. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-59 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ├ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:H/
│                       │       │                  │      │           A:H 
│                       │       │                  │      ╰ V3Score : 6.7 
│                       │       │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 7.7 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/5e5968cdbc
│                       │       │                  │      6618acd6c2402a8a98b503f278835e 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/9706 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35349 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35349 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.19Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.377Z 
│                       ├ [94]  ╭ VulnerabilityID : CVE-2026-35350 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d67499e87a721c3bbcc33dd879f9a0b48d4d2f8d9dd841e452e6
│                       │       │                   e53378696a8c 
│                       │       ├ Title           : The cp utility in uutils coreutils fails to properly handle
│                       │       │                    setuid and ... 
│                       │       ├ Description     : The cp utility in uutils coreutils fails to properly handle
│                       │       │                    setuid and setgid bits when ownership preservation fails.
│                       │       │                   When copying with the -p (preserve) flag, the utility
│                       │       │                   applies the source mode bits even if the chown operation is
│                       │       │                    unsuccessful. This can result in a user-owned copy
│                       │       │                   retaining original privileged bits, creating unexpected
│                       │       │                   privileged executables that violate local security
│                       │       │                   policies. This differs from GNU cp, which clears these bits
│                       │       │                    when ownership cannot be preserved. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-281 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:H/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 6.6 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/9750 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35350 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35350 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.327Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.48Z 
│                       ├ [95]  ╭ VulnerabilityID : CVE-2026-35351 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4864013ce2a53aa5828fd4da7347b7c7181ec4652390990db558
│                       │       │                   182750b3473f 
│                       │       ├ Title           : The mv utility in uutils coreutils fails to preserve file
│                       │       │                   ownership du ... 
│                       │       ├ Description     : The mv utility in uutils coreutils fails to preserve file
│                       │       │                   ownership during moves across different filesystem
│                       │       │                   boundaries. The utility falls back to a copy-and-delete
│                       │       │                   routine that creates the destination file using the
│                       │       │                   caller's UID/GID rather than the source's metadata. This
│                       │       │                   flaw breaks backups and migrations, causing files moved by
│                       │       │                   a privileged user (e.g., root) to become root-owned
│                       │       │                   unexpectedly, which can lead to information disclosure or
│                       │       │                   restricted access for the intended owners. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-281 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:H/UI:N/S:U/C:L/I:L/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 4.2 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/9714 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11706 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35351 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35351 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.457Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.587Z 
│                       ├ [96]  ╭ VulnerabilityID : CVE-2026-35352 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d25ece002a4ea6a418a099f40cd34623e585909df6a47d299a86
│                       │       │                   216163911792 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │       │                   exists in the m ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │       │                   exists in the mkfifo utility of uutils coreutils. The
│                       │       │                   utility creates a FIFO and then performs a path-based chmod
│                       │       │                    to set permissions. A local attacker with write access to
│                       │       │                   the parent directory can swap the newly created FIFO for a
│                       │       │                   symbolic link between these two operations. This redirects
│                       │       │                   the chmod call to an arbitrary file, potentially enabling
│                       │       │                   privilege escalation if the utility is run with elevated
│                       │       │                   privileges. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 7 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/04/4 
│                       │       │                  ├ [1]: http://www.openwall.com/lists/oss-security/2026/05/04/5 
│                       │       │                  ├ [2]: http://www.openwall.com/lists/oss-security/2026/05/04/6 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [4]: https://github.com/uutils/coreutils/issues/10020 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35352 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35352 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.597Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.69Z 
│                       ├ [97]  ╭ VulnerabilityID : CVE-2026-35353 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35353 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e8813ea1ba441cafbb179acd92b20d1579fbc808fba2a70b225e
│                       │       │                   e784a0aaa132 
│                       │       ├ Title           : The mkdir utility in uutils coreutils incorrectly applies
│                       │       │                   permissions  ... 
│                       │       ├ Description     : The mkdir utility in uutils coreutils incorrectly applies
│                       │       │                   permissions when using the -m flag by creating a directory
│                       │       │                   with umask-derived permissions (typically 0755) before
│                       │       │                   subsequently changing them to the requested mode via a
│                       │       │                   separate chmod system call. In multi-user environments,
│                       │       │                   this introduces a brief window where a directory intended
│                       │       │                   to be private is accessible to other users, potentially
│                       │       │                   leading to unauthorized data access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/037b9583bc
│                       │       │                  │      03d814e8516df54ebcda6f681fe1f8 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10036 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35353 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35353 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.723Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.8Z 
│                       ├ [98]  ╭ VulnerabilityID : CVE-2026-35354 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:341e1dcc423fafc7157442378e27808c0f1e64dd6cf3e1a35ca2
│                       │       │                   a6408c498650 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the mv ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the mv utility of uutils coreutils during
│                       │       │                   cross-device moves. The extended attribute (xattr)
│                       │       │                   preservation logic uses multiple path-based system calls
│                       │       │                   that perform fresh path-to-inode lookups for each
│                       │       │                   operation. A local attacker with write access to the
│                       │       │                   directory can exploit this race to swap files between
│                       │       │                   calls, causing the destination file to receive an
│                       │       │                   inconsistent mix of security xattrs, such as SELinux labels
│                       │       │                    or file capabilities. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10014 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35354 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35354 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.867Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:26.907Z 
│                       ├ [99]  ╭ VulnerabilityID : CVE-2026-35355 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35355 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b6ffd1f69d643555965f16da4fd7ec4cbc2459b8183814c3a395
│                       │       │                   65b6936935d2 
│                       │       ├ Title           : The install utility in uutils coreutils is vulnerable to a
│                       │       │                   Time-of-Che ... 
│                       │       ├ Description     : The install utility in uutils coreutils is vulnerable to a
│                       │       │                   Time-of-Check to Time-of-Use (TOCTOU) race condition during
│                       │       │                    file installation. The implementation unlinks an existing
│                       │       │                   destination file and then recreates it using a path-based
│                       │       │                   operation without the O_EXCL flag. A local attacker can
│                       │       │                   exploit the window between the unlink and the subsequent
│                       │       │                   creation to swap the path with a symbolic link, allowing
│                       │       │                   them to redirect privileged writes to overwrite arbitrary
│                       │       │                   system files. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 6.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/b5bbabc18a
│                       │       │                  │      1121908848d836f869a4e98eb63886 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10067 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35355 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35355 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:37.993Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.013Z 
│                       ├ [100] ╭ VulnerabilityID : CVE-2026-35356 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35356 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a2475e315989a195c0820a5aa9282e312bfca86832ff3f2992bc
│                       │       │                   7ef0325bea65 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the in ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the install utility of uutils coreutils when
│                       │       │                   using the -D flag. The command creates parent directories
│                       │       │                   and subsequently performs a second path resolution to
│                       │       │                   create the target file, neither of which is anchored to a
│                       │       │                   directory file descriptor. An attacker with concurrent
│                       │       │                   write access can replace a path component with a symbolic
│                       │       │                   link between these operations, redirecting the privileged
│                       │       │                   write to an arbitrary file system location. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 6.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/0c41299975
│                       │       │                  │      f3c1e21cf5ca968d42cad55ceb42a1 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10140 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35356 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35356 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.13Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.117Z 
│                       ├ [101] ╭ VulnerabilityID : CVE-2026-35357 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:9d10be4084e6b7ca479a2a2bf9442c499826a3bd3a46732f10c3
│                       │       │                   bc714768f859 
│                       │       ├ Title           : The cp utility in uutils coreutils is vulnerable to an
│                       │       │                   information dis ... 
│                       │       ├ Description     : The cp utility in uutils coreutils is vulnerable to an
│                       │       │                   information disclosure race condition. Destination files
│                       │       │                   are initially created with umask-derived permissions (e.g.,
│                       │       │                    0644) before being restricted to their final mode (e.g.,
│                       │       │                   0600) later in the process. A local attacker can race to
│                       │       │                   open the file during this window; once obtained, the file
│                       │       │                   descriptor remains valid and readable even after the
│                       │       │                   permissions are tightened, exposing sensitive or private
│                       │       │                   file contents. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10011 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35357 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35357 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.267Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.223Z 
│                       ├ [102] ╭ VulnerabilityID : CVE-2026-35358 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35358 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:1529294f43faa7e257c8255aacffeb42fb4878b247615d8d396a
│                       │       │                   31942a7fb9fa 
│                       │       ├ Title           : The cp utility in uutils coreutils, when performing
│                       │       │                   recursive copies ( ... 
│                       │       ├ Description     : The cp utility in uutils coreutils, when performing
│                       │       │                   recursive copies (-R), incorrectly treats character and
│                       │       │                   block device nodes as stream sources rather than preserving
│                       │       │                    them. Because the implementation reads bytes into regular
│                       │       │                   files at the destination instead of using mknod, device
│                       │       │                   semantics are destroyed (e.g., /dev/null becomes a regular
│                       │       │                   file). This behavior can lead to runtime denial of service
│                       │       │                   through disk exhaustion or process hangs when reading from
│                       │       │                   unbounded device nodes. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-706 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                  │      │           A:L 
│                       │       │                  │      ╰ V3Score : 4.4 
│                       │       │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/e6a3bb596f
│                       │       │                  │      149628ba973eec3d099f3bb69f2464 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/issues/9746 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/pull/11163 
│                       │       │                  ├ [4]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35358 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35358 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.393Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.33Z 
│                       ├ [103] ╭ VulnerabilityID : CVE-2026-35359 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:53472e82f2a8b3ab047f4cb350ea0da3ed6fdbba187ae291aa05
│                       │       │                   ea65a105472b 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability in
│                       │       │                   the cp utilit ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability in
│                       │       │                   the cp utility of uutils coreutils allows an attacker to
│                       │       │                   bypass no-dereference intent. The utility checks if a
│                       │       │                   source path is a symbolic link using path-based metadata
│                       │       │                   but subsequently opens it without the O_NOFOLLOW flag. An
│                       │       │                   attacker with concurrent write access can swap a regular
│                       │       │                   file for a symbolic link during this window, causing a
│                       │       │                   privileged cp process to copy the contents of arbitrary
│                       │       │                   sensitive files into a destination controlled by the
│                       │       │                   attacker. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ╰ [1]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10017 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35359 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35359 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.537Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.437Z 
│                       ├ [104] ╭ VulnerabilityID : CVE-2026-35360 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0770335c109f78b5818adff54092e9ce76286c424bfa6a2e7b5b
│                       │       │                   656a30c845e7 
│                       │       ├ Title           : The touch utility in uutils coreutils is vulnerable to a
│                       │       │                   Time-of-Check ... 
│                       │       ├ Description     : The touch utility in uutils coreutils is vulnerable to a
│                       │       │                   Time-of-Check to Time-of-Use (TOCTOU) race condition during
│                       │       │                    file creation. When the utility identifies a missing path,
│                       │       │                    it later attempts creation using File::create(), which
│                       │       │                   internally uses O_TRUNC. An attacker can exploit this
│                       │       │                   window to create a file or swap a symlink at the target
│                       │       │                   path, causing touch to truncate an existing file and
│                       │       │                   leading to permanent data loss. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 6.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10019 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35360 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35360 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.673Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.543Z 
│                       ├ [105] ╭ VulnerabilityID : CVE-2026-35361 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35361 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0992cbcfd9baee64d4db2ea293b251276c0c87b61e5e180cb7d3
│                       │       │                   0d7c770816aa 
│                       │       ├ Title           : The mknod utility in uutils coreutils fails to handle
│                       │       │                   security labels  ... 
│                       │       ├ Description     : The mknod utility in uutils coreutils fails to handle
│                       │       │                   security labels atomically by creating device nodes before
│                       │       │                   setting the SELinux context. If labeling fails, the utility
│                       │       │                    attempts cleanup using std::fs::remove_dir, which cannot
│                       │       │                   remove device nodes or FIFOs. This leaves mislabeled nodes
│                       │       │                   behind with incorrect default contexts, potentially
│                       │       │                   allowing unauthorized access to device nodes that should
│                       │       │                   have been restricted by mandatory access controls. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-281 
│                       │       │                  ╰ [1]: CWE-459 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:H/UI:N/S:U/C:L/I:L/
│                       │       │                  │      │           A:N 
│                       │       │                  │      ╰ V3Score : 3.4 
│                       │       │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 4.4 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/42b2ad83cd
│                       │       │                  │      cf6e959ecb378c5040c60d9c64becf 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10582 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35361 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35361 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.827Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.653Z 
│                       ├ [106] ╭ VulnerabilityID : CVE-2026-35362 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35362 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b44a236c34ccf17b08dc8e21be1ae99de4822cc1d00dd075e624
│                       │       │                   4d32a5e4b5ae 
│                       │       ├ Title           : The safe_traversal module in uutils coreutils, which
│                       │       │                   provides protecti ... 
│                       │       ├ Description     : The safe_traversal module in uutils coreutils, which
│                       │       │                   provides protection against Time-of-Check to Time-of-Use
│                       │       │                   (TOCTOU) symlink races using file-descriptor-relative
│                       │       │                   syscalls, is incorrectly limited to Linux targets. On other
│                       │       │                    Unix-like systems such as macOS and FreeBSD, the utility
│                       │       │                   fails to utilize these protections, leaving directory
│                       │       │                   traversal operations vulnerable to symlink race
│                       │       │                   conditions. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.6 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/30239e69a3
│                       │       │                  │      28e76d2377f2a0bc02fbde61c34280 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/9792 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35362 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35362 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:38.96Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.76Z 
│                       ├ [107] ╭ VulnerabilityID : CVE-2026-35363 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a0867b93c6b426e91e1c3a253ab101502e61fa3116a4bcd197dc
│                       │       │                   a2e2b111447b 
│                       │       ├ Title           : A vulnerability in the rm utility of uutils coreutils
│                       │       │                   allows the bypas ... 
│                       │       ├ Description     : A vulnerability in the rm utility of uutils coreutils
│                       │       │                   allows the bypass of safeguard mechanisms intended to
│                       │       │                   protect the current directory. While the utility correctly
│                       │       │                   refuses to delete . or .., it fails to recognize equivalent
│                       │       │                    paths with trailing slashes, such as ./ or .///. An
│                       │       │                   accidental or malicious execution of rm -rf ./ results in
│                       │       │                   the silent recursive deletion of all contents within the
│                       │       │                   current directory. The command further obscures the data
│                       │       │                   loss by reporting a misleading 'Invalid input' error, which
│                       │       │                    may cause users to miss the critical window for data
│                       │       │                   recovery. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-22 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:H/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 5.6 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/9749 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35363 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35363 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:39.12Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.867Z 
│                       ├ [108] ╭ VulnerabilityID : CVE-2026-35364 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f6eda8ecd75bfd656e0fa8914eec33de1d30179b379ca3dfb2f1
│                       │       │                   6727b8999ca1 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │       │                   exists in the m ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │       │                   exists in the mv utility of uutils coreutils during
│                       │       │                   cross-device operations. The utility removes the
│                       │       │                   destination path before recreating it through a copy
│                       │       │                   operation. A local attacker with write access to the
│                       │       │                   destination directory can exploit this window to replace
│                       │       │                   the destination with a symbolic link. The subsequent
│                       │       │                   privileged move operation will follow the symlink, allowing
│                       │       │                    the attacker to redirect the write and overwrite an
│                       │       │                   arbitrary target file with contents from the source. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 6.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10015 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35364 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35364 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:39.737Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:27.97Z 
│                       ├ [109] ╭ VulnerabilityID : CVE-2026-35365 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35365 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:5091af30f18a87465f41fc072385918c4dd76d4b20b19aada479
│                       │       │                   6664159cc0d7 
│                       │       ├ Title           : The mv utility in uutils coreutils improperly handles
│                       │       │                   directory trees  ... 
│                       │       ├ Description     : The mv utility in uutils coreutils improperly handles
│                       │       │                   directory trees containing symbolic links during moves
│                       │       │                   across filesystem boundaries. Instead of preserving
│                       │       │                   symlinks, the implementation expands them, copying the
│                       │       │                   linked targets as real files or directories at the
│                       │       │                   destination. This can lead to resource exhaustion (disk
│                       │       │                   space or time) if symlinks point to large external
│                       │       │                   directories, unexpected duplication of sensitive data into
│                       │       │                   unintended locations, or infinite recursion and repeated
│                       │       │                   copying in the presence of symlink loops. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-59 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:H/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 6.6 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/9654e4abaf
│                       │       │                  │      24449ef2279e9a16963edb5c8b8fef 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/10546 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35365 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35365 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:39.9Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.08Z 
│                       ├ [110] ╭ VulnerabilityID : CVE-2026-35366 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35366 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:062e0925e736716f3597255f4efe25f28461e57674e78903d6ce
│                       │       │                   6d7fe508840e 
│                       │       ├ Title           : The printenv utility in uutils coreutils fails to display
│                       │       │                   environment  ... 
│                       │       ├ Description     : The printenv utility in uutils coreutils fails to display
│                       │       │                   environment variables containing invalid UTF-8 byte
│                       │       │                   sequences. While POSIX permits arbitrary bytes in
│                       │       │                   environment strings, the uutils implementation silently
│                       │       │                   skips these entries rather than printing the raw bytes.
│                       │       │                   This vulnerability allows malicious environment variables
│                       │       │                   (e.g., adversarial LD_PRELOAD values) to evade inspection
│                       │       │                   by administrators or security auditing tools, potentially
│                       │       │                   allowing library injection or other environment-based
│                       │       │                   attacks to go undetected. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-754 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 4.4 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/0bfbbc00c7
│                       │       │                  │      895c0fb6ea94987b4aab99e3d7ee52 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/issues/9701 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/pull/9728 
│                       │       │                  ├ [4]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35366 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35366 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:40.167Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.19Z 
│                       ├ [111] ╭ VulnerabilityID : CVE-2026-35367 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:510dc2f0f01bf00914779a31fadfa15f05ff80cb2eff51206923
│                       │       │                   a529a2894e25 
│                       │       ├ Title           : The nohup utility in uutils coreutils creates its default
│                       │       │                   output file, ... 
│                       │       ├ Description     : The nohup utility in uutils coreutils creates its default
│                       │       │                   output file, nohup.out, without specifying explicit
│                       │       │                   restricted permissions. This causes the file to inherit
│                       │       │                   umask-based permissions, typically resulting in a
│                       │       │                   world-readable file (0644). In multi-user environments,
│                       │       │                   this allows any user on the system to read the captured
│                       │       │                   stdout/stderr output of a command, potentially exposing
│                       │       │                   sensitive information. This behavior diverges from GNU
│                       │       │                   coreutils, which creates nohup.out with owner-only (0600)
│                       │       │                   permissions. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-732 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10021 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35367 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35367 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:40.423Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.297Z 
│                       ├ [112] ╭ VulnerabilityID : CVE-2026-35368 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2640b2e5680d88e1ad29b82ea652c30684e095c93cf864b0796a
│                       │       │                   261a38ee9343 
│                       │       ├ Title           : A vulnerability exists in the chroot utility of uutils
│                       │       │                   coreutils when  ... 
│                       │       ├ Description     : A vulnerability exists in the chroot utility of uutils
│                       │       │                   coreutils when using the --userspec option. The utility
│                       │       │                   resolves the user specification via getpwnam() after
│                       │       │                   entering the chroot but before dropping root privileges. On
│                       │       │                    glibc-based systems, this can trigger the Name Service
│                       │       │                   Switch (NSS) to load shared libraries (e.g., libnss_*.so.2)
│                       │       │                    from the new root directory. If the NEWROOT is writable by
│                       │       │                    an attacker, they can inject a malicious NSS module to
│                       │       │                   execute arbitrary code as root, facilitating a full
│                       │       │                   container escape or privilege escalation. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-426 
│                       │       ├ VendorSeverity   ╭ ghsa  : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:C/C:H/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 7.9 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10327 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35368 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35368 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:40.56Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.4Z 
│                       ├ [113] ╭ VulnerabilityID : CVE-2026-35369 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35369 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:385ff2ef56856e3c9189479c67c7805dde45b472af5d29019999
│                       │       │                   d802221ab482 
│                       │       ├ Title           : An argument parsing error in the kill utility of uutils
│                       │       │                   coreutils inco ... 
│                       │       ├ Description     : An argument parsing error in the kill utility of uutils
│                       │       │                   coreutils incorrectly interprets kill -1 as a request to
│                       │       │                   send the default signal (SIGTERM) to PID -1. Sending a
│                       │       │                   signal to PID -1 causes the kernel to terminate all
│                       │       │                   processes visible to the caller, potentially leading to a
│                       │       │                   system crash or massive process termination. This differs
│                       │       │                   from GNU coreutils, which correctly recognizes -1 as a
│                       │       │                   signal number in this context and would instead report a
│                       │       │                   missing PID argument. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-20 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/2d3aebce67
│                       │       │                  │      12841bc08b9b94e9078be50a25fc10 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/9700 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35369 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35369 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:40.687Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.51Z 
│                       ├ [114] ╭ VulnerabilityID : CVE-2026-35370 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:896a7a58f8f06eb1b9facfb2bc1211fe3709a739c08d1e33820a
│                       │       │                   9601b1ceb6dd 
│                       │       ├ Title           : The id utility in uutils coreutils miscalculates the
│                       │       │                   groups= section o ... 
│                       │       ├ Description     : The id utility in uutils coreutils miscalculates the
│                       │       │                   groups= section of its output. The implementation uses a
│                       │       │                   user's real GID instead of their effective GID to compute
│                       │       │                   the group list, leading to potentially divergent output
│                       │       │                   compared to GNU coreutils. Because many scripts and
│                       │       │                   automated processes rely on the output of id to make
│                       │       │                   security-critical access-control or permission decisions,
│                       │       │                   this discrepancy can lead to unauthorized access or
│                       │       │                   security misconfigurations. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-863 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 4.4 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10006 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35370 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35370 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:40.833Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.613Z 
│                       ├ [115] ╭ VulnerabilityID : CVE-2026-35371 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:32642e68c93560bf5b0f7ebb28033229fd07e8ce8cc9a08a6d73
│                       │       │                   e1c46af96802 
│                       │       ├ Title           : The id utility in uutils coreutils exhibits incorrect
│                       │       │                   behavior in its  ... 
│                       │       ├ Description     : The id utility in uutils coreutils exhibits incorrect
│                       │       │                   behavior in its "pretty print" output when the real UID and
│                       │       │                    effective UID differ. The implementation incorrectly uses
│                       │       │                   the effective GID instead of the effective UID when
│                       │       │                   performing a name lookup for the effective user. This
│                       │       │                   results in misleading diagnostic output that can cause
│                       │       │                   automated scripts or system administrators to make
│                       │       │                   incorrect decisions regarding file permissions or access
│                       │       │                   control. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-451 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/issues/10006 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35371 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35371 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:40.987Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.723Z 
│                       ├ [116] ╭ VulnerabilityID : CVE-2026-35372 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35372 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e63ee2fe0e4f4604c1b8e25cbae95f8e60d1c7b7fb275bb8031a
│                       │       │                   510e7b49afae 
│                       │       ├ Title           : A logic error in the ln utility of uutils coreutils allows
│                       │       │                   the utility ... 
│                       │       ├ Description     : A logic error in the ln utility of uutils coreutils allows
│                       │       │                   the utility to dereference a symbolic link target even when
│                       │       │                    the --no-dereference (or -n) flag is explicitly provided.
│                       │       │                   The implementation previously only honored the
│                       │       │                   "no-dereference" intent if the --force (overwrite) mode was
│                       │       │                    also enabled. This flaw causes ln to follow a symbolic
│                       │       │                   link that points to a directory and create new links inside
│                       │       │                    that target directory instead of treating the symbolic
│                       │       │                   link itself as the destination. In environments where a
│                       │       │                   privileged user or system script uses ln -n to update a
│                       │       │                   symlink, a local attacker could manipulate existing
│                       │       │                   symbolic links to redirect file creation into sensitive
│                       │       │                   directories, potentially leading to unauthorized file
│                       │       │                   creation or system misconfiguration. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-61 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:H/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/394c4b17f2
│                       │       │                  │      f382b4be9f54389bcb79028de02f39 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11253 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35372 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35372 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:41.85Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.83Z 
│                       ├ [117] ╭ VulnerabilityID : CVE-2026-35373 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4426882955566f16f38fce005fb95fefe2f41d9918c0f64ca212
│                       │       │                   8763453b85cd 
│                       │       ├ Title           : A logic error in the ln utility of uutils coreutils causes
│                       │       │                   the program ... 
│                       │       ├ Description     : A logic error in the ln utility of uutils coreutils causes
│                       │       │                   the program to reject source paths containing non-UTF-8
│                       │       │                   filename bytes when using target-directory forms (e.g., ln
│                       │       │                   SOURCE... DIRECTORY). While GNU ln treats filenames as raw
│                       │       │                   bytes and creates the links correctly, the uutils
│                       │       │                   implementation enforces UTF-8 encoding, resulting in a
│                       │       │                   failure to stat the file and a non-zero exit code. In
│                       │       │                   environments where automated scripts or system tasks
│                       │       │                   process valid but non-UTF-8 filenames common on Unix
│                       │       │                   filesystems, this divergence causes the utility to fail,
│                       │       │                   leading to a local denial of service for those specific
│                       │       │                   operations. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-176 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                  │      │           A:L 
│                       │       │                  │      ╰ V3Score : 3.3 
│                       │       │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/pull/11403 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35373 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35373 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:41.997Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:28.933Z 
│                       ├ [118] ╭ VulnerabilityID : CVE-2026-35374 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:267c0a9aa8fd9b72a60c199bd5b417e9f3b9389f5a6c7c7b9d10
│                       │       │                   6c4757dd734f 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the sp ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the split utility of uutils coreutils. The
│                       │       │                   program attempts to prevent data loss by checking for
│                       │       │                   identity between input and output files using their file
│                       │       │                   paths before initiating the split operation. However, the
│                       │       │                   utility subsequently opens the output file with truncation
│                       │       │                   after this path-based validation is complete. A local
│                       │       │                   attacker with write access to the directory can exploit
│                       │       │                   this race window by manipulating mutable path components
│                       │       │                   (e.g., swapping a path with a symbolic link). This can
│                       │       │                   cause split to truncate and write to an unintended target
│                       │       │                   file, potentially including the input file itself or other
│                       │       │                   sensitive files accessible to the process, leading to
│                       │       │                   permanent data loss. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:H 
│                       │       │                         ╰ V3Score : 6.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/pull/11401 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35374 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35374 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:42.127Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.04Z 
│                       ├ [119] ╭ VulnerabilityID : CVE-2026-35375 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35375 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2f2f33f44549b8508c379543c7332269d9136659a665325a1da9
│                       │       │                   ff5dbb2c1669 
│                       │       ├ Title           : A logic error in the split utility of uutils coreutils
│                       │       │                   causes the corr ... 
│                       │       ├ Description     : A logic error in the split utility of uutils coreutils
│                       │       │                   causes the corruption of output filenames when provided
│                       │       │                   with non-UTF-8 prefix or suffix inputs. The implementation
│                       │       │                   utilizes to_string_lossy() when constructing chunk
│                       │       │                   filenames, which automatically rewrites invalid byte
│                       │       │                   sequences into the UTF-8 replacement character (U+FFFD).
│                       │       │                   This behavior diverges from GNU split, which preserves raw
│                       │       │                   pathname bytes intact. In environments utilizing non-UTF-8
│                       │       │                   encodings, this vulnerability leads to the creation of
│                       │       │                   files with incorrect names, potentially causing filename
│                       │       │                   collisions, broken automation, or the misdirection of
│                       │       │                   output data. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-176 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/d2b9550fe8
│                       │       │                  │      21a9a10bf0cec057509211357363f1 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11397 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35375 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35375 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:42.293Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.143Z 
│                       ├ [120] ╭ VulnerabilityID : CVE-2026-35376 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35376 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:344e3fb014935c335df76af18879b438f79fe3151c4fa98b1275
│                       │       │                   11304268ff82 
│                       │       ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the ch ... 
│                       │       ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability
│                       │       │                   exists in the chcon utility of uutils coreutils during
│                       │       │                   recursive operations. The implementation resolves recursive
│                       │       │                    targets using a fresh path lookup (via fts_accpath) rather
│                       │       │                    than binding the traversal and label application to the
│                       │       │                   specific directory state encountered during traversal.
│                       │       │                   Because these operations are not anchored to file
│                       │       │                   descriptors, a local attacker with write access to a
│                       │       │                   directory tree can exploit timing-sensitive rename or
│                       │       │                   symbolic link races to redirect a privileged recursive
│                       │       │                   relabeling operation to unintended files or directories.
│                       │       │                   This vulnerability breaks the hardening expectations for
│                       │       │                   SELinux administration workflows and can lead to the
│                       │       │                   unauthorized modification of security labels on sensitive
│                       │       │                   system objects. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-367 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L/
│                       │       │                  │      │           A:L 
│                       │       │                  │      ╰ V3Score : 4.5 
│                       │       │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:H/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 5.8 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/pull/11402 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35376 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35376 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:42.43Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.25Z 
│                       ├ [121] ╭ VulnerabilityID : CVE-2026-35377 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d6ba7d88535d047cc1db85fe43cf9f0af1231e5de1487138c407
│                       │       │                   138282940d4e 
│                       │       ├ Title           : A logic error in the env utility of uutils coreutils causes
│                       │       │                    a failure  ... 
│                       │       ├ Description     : A logic error in the env utility of uutils coreutils causes
│                       │       │                    a failure to correctly parse command-line arguments when
│                       │       │                   utilizing the -S (split-string) option. In GNU env,
│                       │       │                   backslashes within single quotes are treated literally
│                       │       │                   (with the exceptions of \\ and \'). However, the uutils
│                       │       │                   implementation incorrectly attempts to validate these
│                       │       │                   sequences, resulting in an "invalid sequence" error and an
│                       │       │                   immediate process termination with an exit status of 125
│                       │       │                   when encountering valid but unrecognized sequences like \a
│                       │       │                   or \x. This divergence from GNU behavior breaks
│                       │       │                   compatibility for automated scripts and administrative
│                       │       │                   workflows that rely on standard split-string semantics,
│                       │       │                   leading to a local denial of service for those
│                       │       │                   operations. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-20 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/pull/11512 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35377 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35377 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:42.577Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.357Z 
│                       ├ [122] ╭ VulnerabilityID : CVE-2026-35378 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35378 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bcd55af298a37565c08da5bea64cae3f9c737b6ff38c4f36a4ef
│                       │       │                   23d65ed40620 
│                       │       ├ Title           : A logic error in the expr utility of uutils coreutils
│                       │       │                   causes the progr ... 
│                       │       ├ Description     : A logic error in the expr utility of uutils coreutils
│                       │       │                   causes the program to evaluate parenthesized subexpressions
│                       │       │                    during the parsing phase rather than at the execution
│                       │       │                   phase. This implementation flaw prevents the utility from
│                       │       │                   performing proper short-circuiting for logical OR (|) and
│                       │       │                   AND (&) operations. As a result, arithmetic errors (such as
│                       │       │                    division by zero) occurring within "dead" branches,
│                       │       │                   branches that should be ignored due to short-circuiting,
│                       │       │                   are raised as fatal errors. This divergence from GNU expr
│                       │       │                   behavior can cause guarded expressions within shell scripts
│                       │       │                    to fail with hard errors instead of returning expected
│                       │       │                   boolean results, leading to premature script termination
│                       │       │                   and breaking GNU-compatible shell control flow. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-768 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/
│                       │       │                         │           A:L 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/76b2f7877f
│                       │       │                  │      558f3bfa78e3d4f49f022460f509b7 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11395 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35378 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35378 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:42.73Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.463Z 
│                       ├ [123] ╭ VulnerabilityID : CVE-2026-35379 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35379 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b6b24433acd1e574bcbfda49a6b780c29ef56ff1926422b9f2d8
│                       │       │                   47caa929fe67 
│                       │       ├ Title           : A logic error in the tr utility of uutils coreutils causes
│                       │       │                   the program ... 
│                       │       ├ Description     : A logic error in the tr utility of uutils coreutils causes
│                       │       │                   the program to incorrectly define the [:graph:] and
│                       │       │                   [:print:] character classes. The implementation mistakenly
│                       │       │                   includes the ASCII space character (0x20) in the [:graph:]
│                       │       │                   class and excludes it from the [:print:] class, effectively
│                       │       │                    reversing the standard behavior established by POSIX and
│                       │       │                   GNU coreutils. This vulnerability leads to unintended data
│                       │       │                   modification or loss when the utility is used in automated
│                       │       │                   scripts or data-cleaning pipelines that rely on standard
│                       │       │                   character class semantics. For example, a command executed
│                       │       │                   to delete all graphical characters while intending to
│                       │       │                   preserve whitespace will incorrectly delete all ASCII
│                       │       │                   spaces, potentially resulting in data corruption or logic
│                       │       │                   failures in downstream processing. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-684 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/358063f336
│                       │       │                  │      7cb23a1e5db314cfdbfeb607749b3d 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11405 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35379 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35379 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:42.887Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.57Z 
│                       ├ [124] ╭ VulnerabilityID : CVE-2026-35380 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35380 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f0f07bc994978db5b05e226c72cb0614c17278f354456e9fe8d7
│                       │       │                   21c8513a397b 
│                       │       ├ Title           : A logic error in the cut utility of uutils coreutils causes
│                       │       │                    the progra ... 
│                       │       ├ Description     : A logic error in the cut utility of uutils coreutils causes
│                       │       │                    the program to incorrectly interpret the literal two-byte
│                       │       │                   string '' (two single quotes) as an empty delimiter. The
│                       │       │                   implementation mistakenly maps this string to the NUL
│                       │       │                   character for both the -d (delimiter) and
│                       │       │                   --output-delimiter options. This vulnerability can lead to
│                       │       │                   silent data corruption or logic errors in automated scripts
│                       │       │                    and data pipelines that process strings containing these
│                       │       │                   characters, as the utility may unintentionally split or
│                       │       │                   join data on NUL bytes rather than the intended literal
│                       │       │                   characters. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-20 
│                       │       ├ VendorSeverity   ╭ ghsa  : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:H/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/593f5b191e
│                       │       │                  │      8b9c87e4292955999c2d0b5cbcce69 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11399 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35380 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35380 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:43.047Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.673Z 
│                       ├ [125] ╭ VulnerabilityID : CVE-2026-35381 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35381 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:cc0c7fea1d3767e261a9081c906a672697a7ee2008d4b94fd713
│                       │       │                   40ffd3e6eec4 
│                       │       ├ Title           : A logic error in the cut utility of uutils coreutils causes
│                       │       │                    the utilit ... 
│                       │       ├ Description     : A logic error in the cut utility of uutils coreutils causes
│                       │       │                    the utility to ignore the -s (only-delimited) flag when
│                       │       │                   using the -z (null-terminated) and -d '' (empty delimiter)
│                       │       │                   options together. The implementation incorrectly routes
│                       │       │                   this specific combination through a specialized
│                       │       │                   newline-delimiter code path that fails to check the record
│                       │       │                   suppression status. Consequently, uutils cut emits the
│                       │       │                   entire record plus a NUL byte instead of suppressing it.
│                       │       │                   This divergence from GNU coreutils behavior creates a data
│                       │       │                   integrity risk for automated pipelines that rely on cut -s
│                       │       │                   to filter out undelimited data. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-684 
│                       │       ├ VendorSeverity   ╭ ghsa  : 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/
│                       │       │                         │           A:N 
│                       │       │                         ╰ V3Score : 3.3 
│                       │       ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │       │                  ├ [1]: https://github.com/uutils/coreutils/commit/483f13e918
│                       │       │                  │      30c468262aa1e010e753d6ae99c898 
│                       │       │                  ├ [2]: https://github.com/uutils/coreutils/pull/11394 
│                       │       │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35381 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35381 
│                       │       ├ PublishedDate   : 2026-04-22T17:16:43.2Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:40:29.78Z 
│                       ├ [126] ╭ VulnerabilityID : CVE-2025-45582 
│                       │       ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │       ├ PkgName         : tar 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 41081f85f98b9d6a 
│                       │       ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-45582 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:dde95664ab9ae4d65b695ecb4f32f1763982fa5053233bfde9c3
│                       │       │                   03cbb71b54e1 
│                       │       ├ Title           : tar: Tar path traversal 
│                       │       ├ Description     : GNU Tar through 1.35 allows file overwrite via directory
│                       │       │                   traversal in crafted TAR archives, with a certain two-step
│                       │       │                   process. First, the victim must extract an archive that
│                       │       │                   contains a ../ symlink to a critical directory. Second, the
│                       │       │                    victim must extract an archive that contains a critical
│                       │       │                   file, specified via a relative pathname that begins with
│                       │       │                   the symlink name and ends with that critical file's name.
│                       │       │                   Here, the extraction follows the symlink and overwrites the
│                       │       │                    critical file. This bypasses the protection mechanism of
│                       │       │                   "Member name contains '..'" that would occur for a single
│                       │       │                   TAR archive that attempted to specify the critical file via
│                       │       │                    a ../ approach. For example, the first archive can contain
│                       │       │                    "x -> ../../../../../home/victim/.ssh" and the second
│                       │       │                   archive can contain x/authorized_keys. This can affect
│                       │       │                   server applications that automatically extract any number
│                       │       │                   of user-supplied TAR archives, and were relying on the
│                       │       │                   blocking of traversal. This can also affect software
│                       │       │                   installation processes in which "tar xf" is run more than
│                       │       │                   once (e.g., when installing a package can automatically
│                       │       │                   install two dependencies that are set up as untrusted
│                       │       │                   tarballs instead of official packages). NOTE: the official
│                       │       │                   GNU Tar manual has an otherwise-empty directory for each
│                       │       │                   "tar xf" in its Security Rules of Thumb; however,
│                       │       │                   third-party advice leads users to run "tar xf" more than
│                       │       │                   once into the same directory. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-24 
│                       │       ├ VendorSeverity   ╭ alma       : 2 
│                       │       │                  ├ oracle-oval: 2 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ├ rocky      : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 5.6 
│                       │       ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2025/11/0
│                       │       │                  │       1/6 
│                       │       │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:0067 
│                       │       │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2025-45582 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2379592 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2379592 
│                       │       │                  ├ [5] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-45582 
│                       │       │                  ├ [6] : https://errata.almalinux.org/9/ALSA-2026-0067.html 
│                       │       │                  ├ [7] : https://errata.rockylinux.org/RLSA-2026:0067 
│                       │       │                  ├ [8] : https://github.com/i900008/vulndb/blob/main/Gnu_tar_
│                       │       │                  │       vuln.md 
│                       │       │                  ├ [9] : https://linux.oracle.com/cve/CVE-2025-45582.html 
│                       │       │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-0067.html 
│                       │       │                  ├ [11]: https://lists.gnu.org/archive/html/bug-tar/2025-08/m
│                       │       │                  │       sg00012.html 
│                       │       │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2025-45582 
│                       │       │                  ├ [13]: https://www.cve.org/CVERecord?id=CVE-2025-45582 
│                       │       │                  ├ [14]: https://www.gnu.org/software/tar/ 
│                       │       │                  ├ [15]: https://www.gnu.org/software/tar/manual/html_node/In
│                       │       │                  │       tegrity.html 
│                       │       │                  ├ [16]: https://www.gnu.org/software/tar/manual/html_node/In
│                       │       │                  │       tegrity.html#Integrity 
│                       │       │                  ╰ [17]: https://www.gnu.org/software/tar/manual/html_node/Se
│                       │       │                          curity-rules-of-thumb.html 
│                       │       ├ PublishedDate   : 2025-07-11T17:15:37.183Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T09:25:34.87Z 
│                       ├ [127] ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : util-linux 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0539ff82722c9235d695735fb008b957bd1c5dfd124a77f91fa7
│                       │       │                   2b624a769861 
│                       │       ├ Title           : util-linux: TOCTOU in the mount program when setting up
│                       │       │                   loop devices 
│                       │       ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │       │                    to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │       │                   vulnerability has been identified in the SUID binary
│                       │       │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │       │                   setting up loop devices, validates the source file path
│                       │       │                   with user privileges via fork() + setuid() + realpath(),
│                       │       │                   but subsequently re-canonicalizes and opens it with root
│                       │       │                   privileges (euid=0) without verifying that the path has not
│                       │       │                    been replaced between both operations. Neither O_NOFOLLOW,
│                       │       │                    nor inode comparison, nor post-open fstat() are employed.
│                       │       │                   This allows a local unprivileged user to replace the source
│                       │       │                    file with a symlink pointing to any root-owned file or
│                       │       │                   device during the race window, causing the SUID binary to
│                       │       │                   open and mount it as root. Exploitation requires an
│                       │       │                   /etc/fstab entry with user,loop options whose path points
│                       │       │                   to a directory where the attacker has write permission, and
│                       │       │                    that /usr/bin/mount has the SUID bit set (the default
│                       │       │                   configuration on virtually all Linux distributions). The
│                       │       │                   impact is unauthorized read access to root-protected files
│                       │       │                   and block devices, including backup images, disk volumes,
│                       │       │                   and any file containing a valid filesystem. This issue has
│                       │       │                   been patched in version 2.41.4. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-59 
│                       │       │                  ├ [1]: CWE-269 
│                       │       │                  ╰ [2]: CWE-367 
│                       │       ├ VendorSeverity   ╭ azure       : 2 
│                       │       │                  ├ bottlerocket: 2 
│                       │       │                  ├ julia       : 2 
│                       │       │                  ├ redhat      : 2 
│                       │       │                  ╰ ubuntu      : 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-202
│                       │       │                  │      6-27456 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-
│                       │       │                  │      kit/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.
│                       │       │                  │      toml 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [5]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [128] ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : util-linux 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:416ae20813262a615395d0afef8e0a24856aa80f414aa6beba27
│                       │       │                   06f9f0508faa 
│                       │       ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │       │                   improper hostname canonicalization 
│                       │       ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │       │                   canonicalization in the `login(1)` utility, when invoked
│                       │       │                   with the `-h` option, can modify the supplied remote
│                       │       │                   hostname before setting `PAM_RHOST`. A remote attacker
│                       │       │                   could exploit this by providing a specially crafted
│                       │       │                   hostname, potentially bypassing host-based Pluggable
│                       │       │                   Authentication Modules (PAM) access control rules that rely
│                       │       │                    on fully qualified domain names. This could lead to
│                       │       │                   unauthorized access. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-289 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ╰ V3Score : 5.3 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 3.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │       │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │       ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [129] ╭ VulnerabilityID : CVE-2026-55693 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 1d6b3028159e64 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55693 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:5ab0cbf1e88c8e03714f1cd310cb9e152685c873d27daa973280
│                       │       │                   6db023998d91 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, the tree_count_words() function in
│                       │       │                   src/spellfile.c fills in the word-count fields of a
│                       │       │                   spell-file word trie by walking it iteratively with a depth
│                       │       │                    counter. The counter is bounded only by the trie structure
│                       │       │                    itself; it is never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (arridx[], curi[],
│                       │       │                   wordcount[]). A crafted .spl/.sug file pair, loaded when
│                       │       │                   the user invokes spell suggestion, can drive the descent
│                       │       │                   arbitrarily deep, so the function writes past the end of
│                       │       │                   those arrays. This is a stack out-of-bounds write that
│                       │       │                   corrupts the call frame and crashes the editor. This
│                       │       │                   vulnerability is fixed in 9.2.0653. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/a80874d9b84a01040e3
│                       │       │                  │      d1aef2d4a59e1934dafb7 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0653 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-w
│                       │       │                  │      gh4-64f7-q3jq 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55693 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.22Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T14:17:05.597Z 
│                       ├ [130] ╭ VulnerabilityID : CVE-2026-55892 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 1d6b3028159e64 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55892 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:404ac4b9d728b42b6030279736c5f6ff21cba61dd03776e87145
│                       │       │                   914cd724377e 
│                       │       ├ Title           : vim: Vim: Denial of Service via crafted spell file 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0662, the dump_prefixes() function in src/spell.c walks
│                       │       │                    a spell-file prefix trie iteratively with a depth counter
│                       │       │                   while dumping the prefixes that apply to a word. The
│                       │       │                   counter is bounded only by the trie structure itself; it is
│                       │       │                    never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (prefix[],
│                       │       │                   arridx[], curi[]). A crafted .spl file, loaded when the
│                       │       │                   user dumps the word list, can drive the descent arbitrarily
│                       │       │                    deep, so the function writes past the end of those arrays.
│                       │       │                    This is a stack out-of-bounds write that corrupts the call
│                       │       │                    frame and crashes the editor. This vulnerability is fixed
│                       │       │                   in 9.2.0662. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55892 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/8325b193bba5f01e7a7
│                       │       │                  │      d8241f 
│                       │       │                  ├ [2]: https://github.com/vim/vim/releases/tag/v9.2.0662 
│                       │       │                  ├ [3]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      m9w-fmpj-879h 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-55892 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-55892 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.69Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T19:16:44.667Z 
│                       ├ [131] ╭ VulnerabilityID : CVE-2026-55895 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 1d6b3028159e64 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55895 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8ae636ddf364969fab2acaabeb50c0094a0e9d65c7ae788207fa
│                       │       │                   6e9da702ffed 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a  ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a Vimscript code injection vulnerability exists
│                       │       │                   in s:NetrwLocalRmFile() in the netrw plugin
│                       │       │                   (runtime/pack/dist/opt/netrw/autoload/netrw.vim) when
│                       │       │                   deleting a local file from the browser. A filename derived
│                       │       │                   from the buffer's directory listing is interpolated into an
│                       │       │                    Ex command line passed to :execute with only the backslash
│                       │       │                    character escaped, allowing a crafted filename containing
│                       │       │                   a bar (|) to terminate the intended command and execute
│                       │       │                   arbitrary Vimscript, including shell commands via :call
│                       │       │                   system() and :!.  This vulnerability is fixed in
│                       │       │                   9.2.0663. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/55bc757a5d436e59d50
│                       │       │                  │      fe43f7cda94b118f86cb2 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0663 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-v
│                       │       │                  │      hh8-v6wx-hjjh 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55895 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:41.077Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.097Z 
│                       ├ [132] ╭ VulnerabilityID : CVE-2026-57452 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 1d6b3028159e64 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57452 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:5799cdc98f332def5cd1f39399bd75f19e78af7dcd00e7473244
│                       │       │                   b6b9b5e25fd1 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, wh ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, when Vim opens a file encrypted with the
│                       │       │                   VimCrypt~04! or VimCrypt~05!
│                       │       │                   method (xchacha20poly1305, requires the +sodium feature)
│                       │       │                   whose body is shorter than a single libsodium secretstream
│                       │       │                   header, an unsigned length calculation underflows and a
│                       │       │                   subsequent decryption call reads far past the end of the
│                       │       │                   input buffer, crashing Vim. This vulnerability is fixed in
│                       │       │                   9.2.0671. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-125 
│                       │       │                  ╰ [1]: CWE-191 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/c8777cec25dcfae89c4
│                       │       │                  │      2e9aff51af61f71c5745f 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0671 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-c
│                       │       │                  │      4j9-wr9j-4486 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57452 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.397Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:12:32.483Z 
│                       ├ [133] ╭ VulnerabilityID : CVE-2026-57455 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 1d6b3028159e64 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:03d4accf79dff3243f46b61dfa7e3a144b2d7aa484014456b5df
│                       │       │                   d4c93af0cfc2 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │       │                   in src/spell.c translates a word through a spell file's
│                       │       │                   SOFO (sound-folding) byte map into a caller-owned result
│                       │       │                   buffer. Its copy loop advances the output index ri with no
│                       │       │                   upper bound and terminates only on the input NUL, writing
│                       │       │                   one byte per input byte into the MAXWLEN-element stack
│                       │       │                   buffer the caller provides. A word longer than MAXWLEN,
│                       │       │                   passed to soundfold() (or reached via sound-based spell
│                       │       │                   suggestion) while a SOFO-based spell language is active,
│                       │       │                   therefore writes past the end of that buffer. This is a
│                       │       │                   stack out-of-bounds write that corrupts the call frame and
│                       │       │                   crashes the editor. This vulnerability is fixed in
│                       │       │                   9.2.0698. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7
│                       │       │                  │      f69588dd249e8ccfed41b 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      8mh-6qm3-25g4 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57455 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:23:21.857Z 
│                       ├ [134] ╭ VulnerabilityID : CVE-2026-57456 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 1d6b3028159e64 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2639dd033da076227a760a5bcd427ba73bfc34519913c72d5d5a
│                       │       │                   88bfdea584b6 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vi ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vim's Python omni-completion
│                       │       │                   (runtime/autoload/python3complete.vim and the legacy
│                       │       │                   pythoncomplete.vim) executes reconstructed function and
│                       │       │                   class definitions from the current buffer with exec() as
│                       │       │                   part of populating the completion dictionary. When
│                       │       │                   reconstructing that source, each scope's docstring is
│                       │       │                   inserted verbatim between triple quotes with no escaping,
│                       │       │                   so a hostile buffer can break out of the triple-quoted
│                       │       │                   literal and execute attacker-controlled Python during
│                       │       │                   omni-completion. This vulnerability is fixed in 9.2.0699.[
│                       │       │                   m 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd8
│                       │       │                  │      486ae04e21c2a81016ba8 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-p
│                       │       │                  │      pj8-wqjf-6fp3 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57456 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.51Z 
│                       ├ [135] ╭ VulnerabilityID : CVE-2026-55693 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.7?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : afa1bb226c666397 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55693 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:5a49623d9f519f0b70ffead6e8cddf315b9a46ff820679638439
│                       │       │                   cc9a81eaae45 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, the tree_count_words() function in
│                       │       │                   src/spellfile.c fills in the word-count fields of a
│                       │       │                   spell-file word trie by walking it iteratively with a depth
│                       │       │                    counter. The counter is bounded only by the trie structure
│                       │       │                    itself; it is never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (arridx[], curi[],
│                       │       │                   wordcount[]). A crafted .spl/.sug file pair, loaded when
│                       │       │                   the user invokes spell suggestion, can drive the descent
│                       │       │                   arbitrarily deep, so the function writes past the end of
│                       │       │                   those arrays. This is a stack out-of-bounds write that
│                       │       │                   corrupts the call frame and crashes the editor. This
│                       │       │                   vulnerability is fixed in 9.2.0653. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/a80874d9b84a01040e3
│                       │       │                  │      d1aef2d4a59e1934dafb7 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0653 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-w
│                       │       │                  │      gh4-64f7-q3jq 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55693 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.22Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T14:17:05.597Z 
│                       ├ [136] ╭ VulnerabilityID : CVE-2026-55892 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.7?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : afa1bb226c666397 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55892 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:288c874c3dfe27127e3133c76cd8b26e01d1e5d87eca60f99f04
│                       │       │                   d4ccc22fedee 
│                       │       ├ Title           : vim: Vim: Denial of Service via crafted spell file 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0662, the dump_prefixes() function in src/spell.c walks
│                       │       │                    a spell-file prefix trie iteratively with a depth counter
│                       │       │                   while dumping the prefixes that apply to a word. The
│                       │       │                   counter is bounded only by the trie structure itself; it is
│                       │       │                    never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (prefix[],
│                       │       │                   arridx[], curi[]). A crafted .spl file, loaded when the
│                       │       │                   user dumps the word list, can drive the descent arbitrarily
│                       │       │                    deep, so the function writes past the end of those arrays.
│                       │       │                    This is a stack out-of-bounds write that corrupts the call
│                       │       │                    frame and crashes the editor. This vulnerability is fixed
│                       │       │                   in 9.2.0662. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55892 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/8325b193bba5f01e7a7
│                       │       │                  │      d8241f 
│                       │       │                  ├ [2]: https://github.com/vim/vim/releases/tag/v9.2.0662 
│                       │       │                  ├ [3]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      m9w-fmpj-879h 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-55892 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-55892 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.69Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T19:16:44.667Z 
│                       ├ [137] ╭ VulnerabilityID : CVE-2026-55895 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.7?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : afa1bb226c666397 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55895 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:34ea7f8e5fe429edf1c5b3605526875eda18b50aab58f73cf19b
│                       │       │                   a8f57521fc0f 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a  ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a Vimscript code injection vulnerability exists
│                       │       │                   in s:NetrwLocalRmFile() in the netrw plugin
│                       │       │                   (runtime/pack/dist/opt/netrw/autoload/netrw.vim) when
│                       │       │                   deleting a local file from the browser. A filename derived
│                       │       │                   from the buffer's directory listing is interpolated into an
│                       │       │                    Ex command line passed to :execute with only the backslash
│                       │       │                    character escaped, allowing a crafted filename containing
│                       │       │                   a bar (|) to terminate the intended command and execute
│                       │       │                   arbitrary Vimscript, including shell commands via :call
│                       │       │                   system() and :!.  This vulnerability is fixed in
│                       │       │                   9.2.0663. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/55bc757a5d436e59d50
│                       │       │                  │      fe43f7cda94b118f86cb2 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0663 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-v
│                       │       │                  │      hh8-v6wx-hjjh 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55895 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:41.077Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.097Z 
│                       ├ [138] ╭ VulnerabilityID : CVE-2026-57452 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.7?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : afa1bb226c666397 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57452 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:160261982737b501cf1951dbad3e02bebf72ac0e6f8b0ede6927
│                       │       │                   b17834b2bef3 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, wh ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, when Vim opens a file encrypted with the
│                       │       │                   VimCrypt~04! or VimCrypt~05!
│                       │       │                   method (xchacha20poly1305, requires the +sodium feature)
│                       │       │                   whose body is shorter than a single libsodium secretstream
│                       │       │                   header, an unsigned length calculation underflows and a
│                       │       │                   subsequent decryption call reads far past the end of the
│                       │       │                   input buffer, crashing Vim. This vulnerability is fixed in
│                       │       │                   9.2.0671. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-125 
│                       │       │                  ╰ [1]: CWE-191 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/c8777cec25dcfae89c4
│                       │       │                  │      2e9aff51af61f71c5745f 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0671 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-c
│                       │       │                  │      4j9-wr9j-4486 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57452 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.397Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:12:32.483Z 
│                       ├ [139] ╭ VulnerabilityID : CVE-2026-57455 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.7?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : afa1bb226c666397 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:5fbac5d5f61e072d965b30f2895c60a10bbe94238e1aa869d090
│                       │       │                   cbcdb24248af 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │       │                   in src/spell.c translates a word through a spell file's
│                       │       │                   SOFO (sound-folding) byte map into a caller-owned result
│                       │       │                   buffer. Its copy loop advances the output index ri with no
│                       │       │                   upper bound and terminates only on the input NUL, writing
│                       │       │                   one byte per input byte into the MAXWLEN-element stack
│                       │       │                   buffer the caller provides. A word longer than MAXWLEN,
│                       │       │                   passed to soundfold() (or reached via sound-based spell
│                       │       │                   suggestion) while a SOFO-based spell language is active,
│                       │       │                   therefore writes past the end of that buffer. This is a
│                       │       │                   stack out-of-bounds write that corrupts the call frame and
│                       │       │                   crashes the editor. This vulnerability is fixed in
│                       │       │                   9.2.0698. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7
│                       │       │                  │      f69588dd249e8ccfed41b 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      8mh-6qm3-25g4 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57455 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:23:21.857Z 
│                       ├ [140] ╭ VulnerabilityID : CVE-2026-57456 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.7?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : afa1bb226c666397 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:aa8fa9a232a4fbbe172b4ffcf5e32e134d63d57577e472bd5654
│                       │       │                   6663a5206731 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vi ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vim's Python omni-completion
│                       │       │                   (runtime/autoload/python3complete.vim and the legacy
│                       │       │                   pythoncomplete.vim) executes reconstructed function and
│                       │       │                   class definitions from the current buffer with exec() as
│                       │       │                   part of populating the completion dictionary. When
│                       │       │                   reconstructing that source, each scope's docstring is
│                       │       │                   inserted verbatim between triple quotes with no escaping,
│                       │       │                   so a hostile buffer can break out of the triple-quoted
│                       │       │                   literal and execute attacker-controlled Python during
│                       │       │                   omni-completion. This vulnerability is fixed in 9.2.0699.[
│                       │       │                   m 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd8
│                       │       │                  │      486ae04e21c2a81016ba8 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-p
│                       │       │                  │      pj8-wqjf-6fp3 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57456 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.51Z 
│                       ├ [141] ╭ VulnerabilityID : CVE-2026-55693 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.7?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : ea3b4b04546d4d67 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55693 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:382174c8aca20013d45297a8f32bcca4d01dcd74aa9c7770bc27
│                       │       │                   9e2811690563 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, the tree_count_words() function in
│                       │       │                   src/spellfile.c fills in the word-count fields of a
│                       │       │                   spell-file word trie by walking it iteratively with a depth
│                       │       │                    counter. The counter is bounded only by the trie structure
│                       │       │                    itself; it is never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (arridx[], curi[],
│                       │       │                   wordcount[]). A crafted .spl/.sug file pair, loaded when
│                       │       │                   the user invokes spell suggestion, can drive the descent
│                       │       │                   arbitrarily deep, so the function writes past the end of
│                       │       │                   those arrays. This is a stack out-of-bounds write that
│                       │       │                   corrupts the call frame and crashes the editor. This
│                       │       │                   vulnerability is fixed in 9.2.0653. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/a80874d9b84a01040e3
│                       │       │                  │      d1aef2d4a59e1934dafb7 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0653 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-w
│                       │       │                  │      gh4-64f7-q3jq 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55693 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.22Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T14:17:05.597Z 
│                       ├ [142] ╭ VulnerabilityID : CVE-2026-55892 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.7?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : ea3b4b04546d4d67 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55892 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:c03388c582a77bfbee7aeca0a598c2c37b0e29fb4c665c3c7314
│                       │       │                   38191f0c0e65 
│                       │       ├ Title           : vim: Vim: Denial of Service via crafted spell file 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0662, the dump_prefixes() function in src/spell.c walks
│                       │       │                    a spell-file prefix trie iteratively with a depth counter
│                       │       │                   while dumping the prefixes that apply to a word. The
│                       │       │                   counter is bounded only by the trie structure itself; it is
│                       │       │                    never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (prefix[],
│                       │       │                   arridx[], curi[]). A crafted .spl file, loaded when the
│                       │       │                   user dumps the word list, can drive the descent arbitrarily
│                       │       │                    deep, so the function writes past the end of those arrays.
│                       │       │                    This is a stack out-of-bounds write that corrupts the call
│                       │       │                    frame and crashes the editor. This vulnerability is fixed
│                       │       │                   in 9.2.0662. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55892 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/8325b193bba5f01e7a7
│                       │       │                  │      d8241f 
│                       │       │                  ├ [2]: https://github.com/vim/vim/releases/tag/v9.2.0662 
│                       │       │                  ├ [3]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      m9w-fmpj-879h 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-55892 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-55892 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.69Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T19:16:44.667Z 
│                       ├ [143] ╭ VulnerabilityID : CVE-2026-55895 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.7?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : ea3b4b04546d4d67 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55895 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:38a5b2661d2033cac611c0e323fbd659bb2c6a07ece3b55ee1be
│                       │       │                   e97ac0938e26 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a  ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a Vimscript code injection vulnerability exists
│                       │       │                   in s:NetrwLocalRmFile() in the netrw plugin
│                       │       │                   (runtime/pack/dist/opt/netrw/autoload/netrw.vim) when
│                       │       │                   deleting a local file from the browser. A filename derived
│                       │       │                   from the buffer's directory listing is interpolated into an
│                       │       │                    Ex command line passed to :execute with only the backslash
│                       │       │                    character escaped, allowing a crafted filename containing
│                       │       │                   a bar (|) to terminate the intended command and execute
│                       │       │                   arbitrary Vimscript, including shell commands via :call
│                       │       │                   system() and :!.  This vulnerability is fixed in
│                       │       │                   9.2.0663. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/55bc757a5d436e59d50
│                       │       │                  │      fe43f7cda94b118f86cb2 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0663 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-v
│                       │       │                  │      hh8-v6wx-hjjh 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55895 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:41.077Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.097Z 
│                       ├ [144] ╭ VulnerabilityID : CVE-2026-57452 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.7?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : ea3b4b04546d4d67 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57452 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a8c22161659eed7ec54ed096363ed12f91f9cc6ca9ea92acf3e5
│                       │       │                   9c7bd7b67060 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, wh ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, when Vim opens a file encrypted with the
│                       │       │                   VimCrypt~04! or VimCrypt~05!
│                       │       │                   method (xchacha20poly1305, requires the +sodium feature)
│                       │       │                   whose body is shorter than a single libsodium secretstream
│                       │       │                   header, an unsigned length calculation underflows and a
│                       │       │                   subsequent decryption call reads far past the end of the
│                       │       │                   input buffer, crashing Vim. This vulnerability is fixed in
│                       │       │                   9.2.0671. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-125 
│                       │       │                  ╰ [1]: CWE-191 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/c8777cec25dcfae89c4
│                       │       │                  │      2e9aff51af61f71c5745f 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0671 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-c
│                       │       │                  │      4j9-wr9j-4486 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57452 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.397Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:12:32.483Z 
│                       ├ [145] ╭ VulnerabilityID : CVE-2026-57455 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.7?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : ea3b4b04546d4d67 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:28244f93b973149aaabeac2e0842aa917fcc9a02f75619851aa7
│                       │       │                   c9404513b228 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │       │                   in src/spell.c translates a word through a spell file's
│                       │       │                   SOFO (sound-folding) byte map into a caller-owned result
│                       │       │                   buffer. Its copy loop advances the output index ri with no
│                       │       │                   upper bound and terminates only on the input NUL, writing
│                       │       │                   one byte per input byte into the MAXWLEN-element stack
│                       │       │                   buffer the caller provides. A word longer than MAXWLEN,
│                       │       │                   passed to soundfold() (or reached via sound-based spell
│                       │       │                   suggestion) while a SOFO-based spell language is active,
│                       │       │                   therefore writes past the end of that buffer. This is a
│                       │       │                   stack out-of-bounds write that corrupts the call frame and
│                       │       │                   crashes the editor. This vulnerability is fixed in
│                       │       │                   9.2.0698. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7
│                       │       │                  │      f69588dd249e8ccfed41b 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      8mh-6qm3-25g4 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57455 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:23:21.857Z 
│                       ├ [146] ╭ VulnerabilityID : CVE-2026-57456 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.7?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : ea3b4b04546d4d67 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:41ebe32e21939621000e17c5bfef933582439170f12bb03e9cd8
│                       │       │                   c57db8009f0e 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vi ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vim's Python omni-completion
│                       │       │                   (runtime/autoload/python3complete.vim and the legacy
│                       │       │                   pythoncomplete.vim) executes reconstructed function and
│                       │       │                   class definitions from the current buffer with exec() as
│                       │       │                   part of populating the completion dictionary. When
│                       │       │                   reconstructing that source, each scope's docstring is
│                       │       │                   inserted verbatim between triple quotes with no escaping,
│                       │       │                   so a hostile buffer can break out of the triple-quoted
│                       │       │                   literal and execute attacker-controlled Python during
│                       │       │                   omni-completion. This vulnerability is fixed in 9.2.0699.[
│                       │       │                   m 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd8
│                       │       │                  │      486ae04e21c2a81016ba8 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-p
│                       │       │                  │      pj8-wqjf-6fp3 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57456 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.51Z 
│                       ├ [147] ╭ VulnerabilityID : CVE-2021-31879 
│                       │       ├ PkgID           : wget@1.25.0-2ubuntu3 
│                       │       ├ PkgName         : wget 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu3?arch=amd64&distr
│                       │       │                  │       o=ubuntu-25.10 
│                       │       │                  ╰ UID : 3ae34724b04a04d7 
│                       │       ├ InstalledVersion: 1.25.0-2ubuntu3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:85737dc2e90cb77f2bfcbb399e8e25b122718429c1e111e80a4c
│                       │       │                   046fe26ed136 
│                       │       ├ Title           : wget: authorization header disclosure on redirect 
│                       │       ├ Description     : GNU Wget through 1.21.1 does not omit the Authorization
│                       │       │                   header upon a redirect to a different origin, a related
│                       │       │                   issue to CVE-2018-1000007. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-601 
│                       │       ├ VendorSeverity   ╭ amazon     : 2 
│                       │       │                  ├ cbl-mariner: 2 
│                       │       │                  ├ nvd        : 2 
│                       │       │                  ├ photon     : 2 
│                       │       │                  ├ redhat     : 2 
│                       │       │                  ╰ ubuntu     : 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V2Vector: AV:N/AC:M/Au:N/C:P/I:P/A:N 
│                       │       │                  │        ├ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:
│                       │       │                  │        │           L/A:N 
│                       │       │                  │        ├ V2Score : 5.8 
│                       │       │                  │        ╰ V3Score : 6.1 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2021-31879 
│                       │       │                  ├ [1]: https://mail.gnu.org/archive/html/bug-wget/2021-02/ms
│                       │       │                  │      g00002.html 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2021-31879 
│                       │       │                  ├ [3]: https://savannah.gnu.org/bugs/?56909 
│                       │       │                  ├ [4]: https://security.netapp.com/advisory/ntap-20210618-00
│                       │       │                  │      02/ 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2021-31879 
│                       │       ├ PublishedDate   : 2021-04-29T05:15:08.707Z 
│                       │       ╰ LastModifiedDate: 2026-06-17T03:52:23.987Z 
│                       ├ [148] ╭ VulnerabilityID : CVE-2026-55693 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : e2b6c03c16b1e8ca 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55693 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3f9c86b214dcf1e9e9c3296a26139388594749696674757f6a62
│                       │       │                   591acf988fc5 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0653, the tree_count_words() function in
│                       │       │                   src/spellfile.c fills in the word-count fields of a
│                       │       │                   spell-file word trie by walking it iteratively with a depth
│                       │       │                    counter. The counter is bounded only by the trie structure
│                       │       │                    itself; it is never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (arridx[], curi[],
│                       │       │                   wordcount[]). A crafted .spl/.sug file pair, loaded when
│                       │       │                   the user invokes spell suggestion, can drive the descent
│                       │       │                   arbitrarily deep, so the function writes past the end of
│                       │       │                   those arrays. This is a stack out-of-bounds write that
│                       │       │                   corrupts the call frame and crashes the editor. This
│                       │       │                   vulnerability is fixed in 9.2.0653. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/a80874d9b84a01040e3
│                       │       │                  │      d1aef2d4a59e1934dafb7 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0653 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-w
│                       │       │                  │      gh4-64f7-q3jq 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55693 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.22Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T14:17:05.597Z 
│                       ├ [149] ╭ VulnerabilityID : CVE-2026-55892 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : e2b6c03c16b1e8ca 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55892 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4fcd6a5df080855fba869089d8b14940d5e15fa4181cd086f663
│                       │       │                   c88d4c137b2c 
│                       │       ├ Title           : vim: Vim: Denial of Service via crafted spell file 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0662, the dump_prefixes() function in src/spell.c walks
│                       │       │                    a spell-file prefix trie iteratively with a depth counter
│                       │       │                   while dumping the prefixes that apply to a word. The
│                       │       │                   counter is bounded only by the trie structure itself; it is
│                       │       │                    never checked against the size of the fixed
│                       │       │                   MAXWLEN-element stack arrays it indexes (prefix[],
│                       │       │                   arridx[], curi[]). A crafted .spl file, loaded when the
│                       │       │                   user dumps the word list, can drive the descent arbitrarily
│                       │       │                    deep, so the function writes past the end of those arrays.
│                       │       │                    This is a stack out-of-bounds write that corrupts the call
│                       │       │                    frame and crashes the editor. This vulnerability is fixed
│                       │       │                   in 9.2.0662. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 5.5 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55892 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/8325b193bba5f01e7a7
│                       │       │                  │      d8241f 
│                       │       │                  ├ [2]: https://github.com/vim/vim/releases/tag/v9.2.0662 
│                       │       │                  ├ [3]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      m9w-fmpj-879h 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-55892 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-55892 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:40.69Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T19:16:44.667Z 
│                       ├ [150] ╭ VulnerabilityID : CVE-2026-55895 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : e2b6c03c16b1e8ca 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55895 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4c41be03bd1410734ba0cec786490911793048da0a25773ad807
│                       │       │                   b759479a6411 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a  ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0663, a Vimscript code injection vulnerability exists
│                       │       │                   in s:NetrwLocalRmFile() in the netrw plugin
│                       │       │                   (runtime/pack/dist/opt/netrw/autoload/netrw.vim) when
│                       │       │                   deleting a local file from the browser. A filename derived
│                       │       │                   from the buffer's directory listing is interpolated into an
│                       │       │                    Ex command line passed to :execute with only the backslash
│                       │       │                    character escaped, allowing a crafted filename containing
│                       │       │                   a bar (|) to terminate the intended command and execute
│                       │       │                   arbitrary Vimscript, including shell commands via :call
│                       │       │                   system() and :!.  This vulnerability is fixed in
│                       │       │                   9.2.0663. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/55bc757a5d436e59d50
│                       │       │                  │      fe43f7cda94b118f86cb2 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0663 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-v
│                       │       │                  │      hh8-v6wx-hjjh 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-55895 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:41.077Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.097Z 
│                       ├ [151] ╭ VulnerabilityID : CVE-2026-57452 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : e2b6c03c16b1e8ca 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57452 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b156357c46489a1b6ae9a1de2bbc2754a24bdef918501ee0a659
│                       │       │                   a23444bed97e 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, wh ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0671, when Vim opens a file encrypted with the
│                       │       │                   VimCrypt~04! or VimCrypt~05!
│                       │       │                   method (xchacha20poly1305, requires the +sodium feature)
│                       │       │                   whose body is shorter than a single libsodium secretstream
│                       │       │                   header, an unsigned length calculation underflows and a
│                       │       │                   subsequent decryption call reads far past the end of the
│                       │       │                   input buffer, crashing Vim. This vulnerability is fixed in
│                       │       │                   9.2.0671. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-125 
│                       │       │                  ╰ [1]: CWE-191 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/c8777cec25dcfae89c4
│                       │       │                  │      2e9aff51af61f71c5745f 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0671 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-c
│                       │       │                  │      4j9-wr9j-4486 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57452 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.397Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:12:32.483Z 
│                       ├ [152] ╭ VulnerabilityID : CVE-2026-57455 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : e2b6c03c16b1e8ca 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:9ba24cee6e7a6a33f7c2ffd34ab9d8d6d48a3ec51b9915739cc5
│                       │       │                   94a9c23597bc 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, th ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │       │                   in src/spell.c translates a word through a spell file's
│                       │       │                   SOFO (sound-folding) byte map into a caller-owned result
│                       │       │                   buffer. Its copy loop advances the output index ri with no
│                       │       │                   upper bound and terminates only on the input NUL, writing
│                       │       │                   one byte per input byte into the MAXWLEN-element stack
│                       │       │                   buffer the caller provides. A word longer than MAXWLEN,
│                       │       │                   passed to soundfold() (or reached via sound-based spell
│                       │       │                   suggestion) while a SOFO-based spell language is active,
│                       │       │                   therefore writes past the end of that buffer. This is a
│                       │       │                   stack out-of-bounds write that corrupts the call frame and
│                       │       │                   crashes the editor. This vulnerability is fixed in
│                       │       │                   9.2.0698. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7
│                       │       │                  │      f69588dd249e8ccfed41b 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-q
│                       │       │                  │      8mh-6qm3-25g4 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57455 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T04:23:21.857Z 
│                       ├ [153] ╭ VulnerabilityID : CVE-2026-57456 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.7 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.7?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : e2b6c03c16b1e8ca 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.7 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                       │       │                  │         88dbb3a8ba81c54fa4d46 
│                       │       │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                       │       │                            06259639c712960695c95 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:c29f9358d97963a2ba81109503e180fc4c1dfc7f061b28800083
│                       │       │                   75435e53297d 
│                       │       ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vi ... 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0699, Vim's Python omni-completion
│                       │       │                   (runtime/autoload/python3complete.vim and the legacy
│                       │       │                   pythoncomplete.vim) executes reconstructed function and
│                       │       │                   class definitions from the current buffer with exec() as
│                       │       │                   part of populating the completion dictionary. When
│                       │       │                   reconstructing that source, each scope's docstring is
│                       │       │                   inserted verbatim between triple quotes with no escaping,
│                       │       │                   so a hostile buffer can break out of the triple-quoted
│                       │       │                   literal and execute attacker-controlled Python during
│                       │       │                   omni-completion. This vulnerability is fixed in 9.2.0699.[
│                       │       │                   m 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-94 
│                       │       ├ VendorSeverity   ╭ nvd   : 3 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ nvd ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H 
│                       │       │                        ╰ V3Score : 7.8 
│                       │       ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd8
│                       │       │                  │      486ae04e21c2a81016ba8 
│                       │       │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                       │       │                  ├ [2]: https://github.com/vim/vim/security/advisories/GHSA-p
│                       │       │                  │      pj8-wqjf-6fp3 
│                       │       │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-57456 
│                       │       ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                       │       ╰ LastModifiedDate: 2026-06-26T05:16:31.51Z 
│                       ╰ [154] ╭ VulnerabilityID : CVE-2026-27171 
│                               ├ PkgID           : zlib1g@1:1.3.dfsg+really1.3.1-1ubuntu2 
│                               ├ PkgName         : zlib1g 
│                               ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/zlib1g@1.3.dfsg%2Breally1.3.1-1ubuntu
│                               │                  │       2?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                               │                  ╰ UID : a2db0415a832ade 
│                               ├ InstalledVersion: 1:1.3.dfsg+really1.3.1-1ubuntu2 
│                               ├ Status          : affected 
│                               ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c258177
│                               │                  │         88dbb3a8ba81c54fa4d46 
│                               │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb
│                               │                            06259639c712960695c95 
│                               ├ SeveritySource  : ubuntu 
│                               ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27171 
│                               ├ DataSource       ╭ ID  : ubuntu 
│                               │                  ├ Name: Ubuntu CVE Tracker 
│                               │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                               ├ Fingerprint     : sha256:bc9f3bc8153732a9b3233e9c0dc811ae9de3fbcf2138555575cf
│                               │                   d8ad9cd3f1fa 
│                               ├ Title           : zlib: zlib: Denial of Service via infinite loop in CRC32
│                               │                   combine functions 
│                               ├ Description     : zlib before 1.3.2 allows CPU consumption via
│                               │                   crc32_combine64 and crc32_combine_gen64 because x2nmodp can
│                               │                    do right shifts within a loop that has no termination
│                               │                   condition. 
│                               ├ Severity        : LOW 
│                               ├ CweIDs           ─ [0]: CWE-1284 
│                               ├ VendorSeverity   ╭ amazon     : 1 
│                               │                  ├ azure      : 1 
│                               │                  ├ cbl-mariner: 1 
│                               │                  ├ julia      : 1 
│                               │                  ├ nvd        : 2 
│                               │                  ├ photon     : 2 
│                               │                  ├ redhat     : 1 
│                               │                  ╰ ubuntu     : 1 
│                               ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:
│                               │                  │        │           N/A:L 
│                               │                  │        ╰ V3Score : 2.9 
│                               │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                               │                  │        │           N/A:H 
│                               │                  │        ╰ V3Score : 5.5 
│                               │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:
│                               │                           │           N/A:L 
│                               │                           ╰ V3Score : 3.3 
│                               ├ References       ╭ [0] : https://7asecurity.com/blog/2026/02/zlib-7asecurity-
│                               │                  │       audit 
│                               │                  ├ [1] : https://7asecurity.com/blog/2026/02/zlib-7asecurity-
│                               │                  │       audit/ 
│                               │                  ├ [2] : https://7asecurity.com/reports/pentest-report-zlib-R
│                               │                  │       C1.1.pdf 
│                               │                  ├ [3] : https://access.redhat.com/security/cve/CVE-2026-27171 
│                               │                  ├ [4] : https://github.com/advisories/GHSA-h858-mf2m-8jf4 
│                               │                  ├ [5] : https://github.com/madler/zlib/issues/904 
│                               │                  ├ [6] : https://github.com/madler/zlib/releases/tag/v1.3.2 
│                               │                  ├ [7] : https://nvd.nist.gov/vuln/detail/CVE-2026-27171 
│                               │                  ├ [8] : https://ostif.org/zlib-audit-complete 
│                               │                  ├ [9] : https://ostif.org/zlib-audit-complete/ 
│                               │                  ╰ [10]: https://www.cve.org/CVERecord?id=CVE-2026-27171 
│                               ├ PublishedDate   : 2026-02-18T04:16:01.263Z 
│                               ╰ LastModifiedDate: 2026-06-17T10:26:47.357Z 
╰ [1] ╭ Target         : Java 
      ├ Class          : lang-pkgs 
      ├ Type           : jar 
      ├ Packages        
      ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2026-54512 
                        │     ├ VendorIDs        ─ [0]: GHSA-j3rv-43j4-c7qm 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.1 
                        │     │                  ╰ UID : 6bd66f14c6cb3d57 
                        │     ├ InstalledVersion: 2.21.1 
                        │     ├ FixedVersion    : 2.18.8, 3.1.4, 2.21.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                        │     │                  │         dbb3a8ba81c54fa4d46 
                        │     │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                        │     │                            259639c712960695c95 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54512 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:ca20fa3b981a076005450855605d40152f39a912dfb103e24c47be
                        │     │                   902aaa9a73 
                        │     ├ Title           : jackson-databind: jackson-databind: Arbitrary code execution
                        │     │                   via PolymorphicTypeValidator bypass 
                        │     ├ Description     : jackson-databind contains the general-purpose data-binding
                        │     │                   functionality and tree-model for Jackson Data Processor. From
                        │     │                    2.10.0 until 2.18.8, 2.21.4, and 3.1.4, jackson-databind's
                        │     │                   PolymorphicTypeValidator (PTV) is the primary safety
                        │     │                   mechanism guarding polymorphic deserialization. When
                        │     │                   polymorphic typing is enabled and a type identifier contains
                        │     │                   generic parameters (i.e. the type ID string contains <),
                        │     │                   DatabindContext._resolveAndValidateGeneric() validates only
                        │     │                   the raw container class name (the substring before <) against
                        │     │                    the configured PTV. If the container type is approved, the
                        │     │                   method parses the full canonical type string via
                        │     │                   TypeFactory.constructFromCanonical() and returns the fully
                        │     │                   parameterized type without ever validating the nested type
                        │     │                   arguments against the PTV. The nested type arguments are then
                        │     │                    resolved, instantiated, and populated as beans during
                        │     │                   deserialization. An attacker who controls the type ID can
                        │     │                   therefore place a denied class as a generic type parameter of
                        │     │                    an allowed container — for example
                        │     │                   java.util.ArrayList<com.evil.Gadget> when only
                        │     │                   java.util.ArrayList is allow-listed. The container passes the
                        │     │                    PTV check; com.evil.Gadget is loaded via Class.forName(name,
                        │     │                    true, loader), instantiated, and its properties are set from
                        │     │                    attacker-controlled JSON. This completely bypasses an
                        │     │                   explicitly configured PTV allow-list. This vulnerability is
                        │     │                   fixed in 2.18.8, 2.21.4, and 3.1.4. 
                        │     ├ Severity        : HIGH 
                        │     ├ CweIDs           ╭ [0]: CWE-184 
                        │     │                  ╰ [1]: CWE-502 
                        │     ├ VendorSeverity   ╭ ghsa  : 3 
                        │     │                  ╰ redhat: 3 
                        │     ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/
                        │     │                  │        │           A:H 
                        │     │                  │        ╰ V3Score : 8.1 
                        │     │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/
                        │     │                           │           A:H 
                        │     │                           ╰ V3Score : 8.1 
                        │     ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54512 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/43
                        │     │                  │      4d6c511de7fdd9872f29157aafb6162d12d8d5 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/issues/5988 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                  │      advisories/GHSA-j3rv-43j4-c7qm 
                        │     │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-54512 
                        │     │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-54512 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.203Z 
                        │     ╰ LastModifiedDate: 2026-06-27T21:01:36.47Z 
                        ├ [1] ╭ VulnerabilityID : CVE-2026-54513 
                        │     ├ VendorIDs        ─ [0]: GHSA-rmj7-2vxq-3g9f 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.1 
                        │     │                  ╰ UID : 6bd66f14c6cb3d57 
                        │     ├ InstalledVersion: 2.21.1 
                        │     ├ FixedVersion    : 2.18.8, 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                        │     │                  │         dbb3a8ba81c54fa4d46 
                        │     │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                        │     │                            259639c712960695c95 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54513 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:619c57ca25d25342af347d39e9a6d5606ae268d6d4858df2715ec8
                        │     │                   be8ac3f989 
                        │     ├ Title           : jackson-databind: Jackson-databind: Security bypass allows
                        │     │                   arbitrary code execution 
                        │     ├ Description     : jackson-databind contains the general-purpose data-binding
                        │     │                   functionality and tree-model for Jackson Data Processor. From
                        │     │                    2.10.0 until 2.18.8, 2.21.4, and 3.1.4,
                        │     │                   BasicPolymorphicTypeValidator.Builder.allowIfSubTypeIsArray()
                        │     │                    allowlists any array type based only on clazz.isArray(),
                        │     │                   without validating the array's component (element) type
                        │     │                   against the configured allowlist. A PTV built with
                        │     │                   allowIfSubTypeIsArray() plus an explicit concrete-type
                        │     │                   allowlist therefore still permits EvilType[] even though
                        │     │                   EvilType is not allowlisted. When Jackson deserializes the
                        │     │                   elements and no per-element type IDs are present, it
                        │     │                   instantiates the component type directly with no further PTV
                        │     │                   check, bypassing the allowlist. This vulnerability is fixed
                        │     │                   in 2.18.8, 2.21.4, and 3.1.4. 
                        │     ├ Severity        : HIGH 
                        │     ├ CweIDs           ─ [0]: CWE-184 
                        │     ├ VendorSeverity   ╭ ghsa  : 3 
                        │     │                  ╰ redhat: 3 
                        │     ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/
                        │     │                  │        │           A:H 
                        │     │                  │        ╰ V3Score : 8.1 
                        │     │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/
                        │     │                           │           A:H 
                        │     │                           ╰ V3Score : 8.1 
                        │     ├ References       ╭ [0] : https://access.redhat.com/security/cve/CVE-2026-54513 
                        │     │                  ├ [1] : https://bugzilla.redhat.com/show_bug.cgi?id=2492010 
                        │     │                  ├ [2] : https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [3] : https://github.com/FasterXML/jackson-databind/commit/0
                        │     │                  │       1d1692c8d0ed03e51a0e3c4f8a9e6908e4931e5 
                        │     │                  ├ [4] : https://github.com/FasterXML/jackson-databind/commit/2
                        │     │                  │       4529da29fdf46ff94ca38de9ebf31cd188f5e8e 
                        │     │                  ├ [5] : https://github.com/FasterXML/jackson-databind/issues/5
                        │     │                  │       981 
                        │     │                  ├ [6] : https://github.com/FasterXML/jackson-databind/issues/5
                        │     │                  │       983 
                        │     │                  ├ [7] : https://github.com/FasterXML/jackson-databind/pull/5984 
                        │     │                  ├ [8] : https://github.com/FasterXML/jackson-databind/security
                        │     │                  │       /advisories/GHSA-rmj7-2vxq-3g9f 
                        │     │                  ├ [9] : https://nvd.nist.gov/vuln/detail/CVE-2026-54513 
                        │     │                  ├ [10]: https://security.access.redhat.com/data/csaf/v2/vex/20
                        │     │                  │       26/cve-2026-54513.json 
                        │     │                  ╰ [11]: https://www.cve.org/CVERecord?id=CVE-2026-54513 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.333Z 
                        │     ╰ LastModifiedDate: 2026-06-30T03:21:03.13Z 
                        ├ [2] ╭ VulnerabilityID : CVE-2026-54514 
                        │     ├ VendorIDs        ─ [0]: GHSA-hgj6-7826-r7m5 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.1 
                        │     │                  ╰ UID : 6bd66f14c6cb3d57 
                        │     ├ InstalledVersion: 2.21.1 
                        │     ├ FixedVersion    : 2.18.8, 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                        │     │                  │         dbb3a8ba81c54fa4d46 
                        │     │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                        │     │                            259639c712960695c95 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54514 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:c7ba174ef1565176aca84c57843125fb4c45c942cfb36895b3c161
                        │     │                   9f73eab204 
                        │     ├ Title           : jackson-databind: jackson-databind: Information Disclosure
                        │     │                   via Eager DNS Resolution 
                        │     ├ Description     : jackson-databind contains the general-purpose data-binding
                        │     │                   functionality and tree-model for Jackson Data Processor. From
                        │     │                    2.0.0 until 2.18.8, 2.21.4, and 3.1.4,
                        │     │                   JDKFromStringDeserializer constructed InetSocketAddress with
                        │     │                   new InetSocketAddress(host, port), which performs eager DNS
                        │     │                   name resolution for hostname inputs at deserialization time.
                        │     │                   An application that binds untrusted JSON into a type
                        │     │                   containing an InetSocketAddress field issues an
                        │     │                   attacker-chosen DNS query during readValue, before any
                        │     │                   application-level validation or connect logic. The fix uses
                        │     │                   InetSocketAddress.createUnresolved(host, port), deferring DNS
                        │     │                    to an explicit connect. This vulnerability is fixed in
                        │     │                   2.18.8, 2.21.4, and 3.1.4. 
                        │     ├ Severity        : MEDIUM 
                        │     ├ CweIDs           ─ [0]: CWE-918 
                        │     ├ VendorSeverity   ╭ ghsa  : 2 
                        │     │                  ╰ redhat: 2 
                        │     ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/
                        │     │                  │        │           A:N 
                        │     │                  │        ╰ V3Score : 5.3 
                        │     │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/
                        │     │                           │           A:N 
                        │     │                           ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54514 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/1f
                        │     │                  │      5a1037b1e9e05920e755cb35f198bcd46667e4 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/pull/5951 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                  │      advisories/GHSA-hgj6-7826-r7m5 
                        │     │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-54514 
                        │     │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-54514 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.467Z 
                        │     ╰ LastModifiedDate: 2026-06-27T20:55:09.61Z 
                        ├ [3] ╭ VulnerabilityID : CVE-2026-54515 
                        │     ├ VendorIDs        ─ [0]: GHSA-5jmj-h7xm-6q6v 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.1 
                        │     │                  ╰ UID : 6bd66f14c6cb3d57 
                        │     ├ InstalledVersion: 2.21.1 
                        │     ├ FixedVersion    : 3.1.4, 2.18.9, 2.21.5, 2.22.1 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                        │     │                  │         dbb3a8ba81c54fa4d46 
                        │     │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                        │     │                            259639c712960695c95 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54515 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:38dca79a10221a20ae57f8ea3a1e88d2ca45a7294a0aeb77c37662
                        │     │                   a4247719c8 
                        │     ├ Title           : jackson-databind: jackson-databind: Ignored properties can be
                        │     │                    unexpectedly modified 
                        │     ├ Description     : jackson-databind contains the general-purpose data-binding
                        │     │                   functionality and tree-model for Jackson Data Processor. From
                        │     │                    2.8.0 until 2.18.9, 2.21.5, and 3.1.4, in
                        │     │                   BeanDeserializerBase.createContextual(), per-property
                        │     │                   @JsonIgnoreProperties exclusions are applied by
                        │     │                   _handleByNameInclusion(), producing a contextual deserializer
                        │     │                    whose BeanPropertyMap has the ignored properties removed.
                        │     │                   The subsequent per-property case-insensitivity block
                        │     │                   (triggered by
                        │     │                   @JsonFormat(ACCEPT_CASE_INSENSITIVE_PROPERTIES)) rebuilds
                        │     │                   from this._beanProperties (the original, unfiltered map)
                        │     │                   instead of contextual._beanProperties, then overwrites the
                        │     │                   filtered map — restoring every property
                        │     │                   _handleByNameInclusion had just removed. The ignored property
                        │     │                    becomes writable again. This vulnerability is fixed in
                        │     │                   2.18.9, 2.21.5, and 3.1.4. 
                        │     ├ Severity        : MEDIUM 
                        │     ├ CweIDs           ─ [0]: CWE-915 
                        │     ├ VendorSeverity   ╭ ghsa  : 2 
                        │     │                  ╰ redhat: 2 
                        │     ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/
                        │     │                  │        │           A:N 
                        │     │                  │        ╰ V3Score : 5.3 
                        │     │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/
                        │     │                           │           A:N 
                        │     │                           ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54515 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/0e
                        │     │                  │      1b0b211f7a53baa62ba2f4c9bd006c7bf4d5fa 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/issues/5962 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/issues/5964 
                        │     │                  ├ [5]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                  │      advisories/GHSA-5jmj-h7xm-6q6v 
                        │     │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-54515 
                        │     │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-54515 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.597Z 
                        │     ╰ LastModifiedDate: 2026-06-29T13:38:59.057Z 
                        ├ [4] ╭ VulnerabilityID : CVE-2026-54516 
                        │     ├ VendorIDs        ─ [0]: GHSA-9fxm-vc8v-hj55 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.1 
                        │     │                  ╰ UID : 6bd66f14c6cb3d57 
                        │     ├ InstalledVersion: 2.21.1 
                        │     ├ FixedVersion    : 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                        │     │                  │         dbb3a8ba81c54fa4d46 
                        │     │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                        │     │                            259639c712960695c95 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54516 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:bab5d1299d5b52b287e3c23b112430490a4be7f59e6c9541b90dc5
                        │     │                   b1a29d1abb 
                        │     ├ Title           : jackson-databind: jackson-databind: Security bypass due to
                        │     │                   improper handling of renamed properties 
                        │     ├ Description     : jackson-databind contains the general-purpose data-binding
                        │     │                   functionality and tree-model for Jackson Data Processor. From
                        │     │                    2.21.0 until 2.21.4 and 3.1.4,
                        │     │                   POJOPropertiesCollector._renameProperties() allows a property
                        │     │                    with @JsonProperty("renamed") on the getter and @JsonIgnore
                        │     │                   on the setter to be renamed rather than dropped. With
                        │     │                   MapperFeature.INFER_PROPERTY_MUTATORS enabled (default), the
                        │     │                   private backing field is retained; during deserialization
                        │     │                   BeanDeserializerFactory.addBeanProps() sees hasField()==true,
                        │     │                    builds a FieldProperty, and makes the backing field
                        │     │                   writable. An attacker supplying the renamed JSON key writes
                        │     │                   the backing field directly, bypassing the @JsonIgnore on the
                        │     │                   setter. This vulnerability is fixed in 3.1.4. 
                        │     ├ Severity        : MEDIUM 
                        │     ├ CweIDs           ─ [0]: CWE-915 
                        │     ├ VendorSeverity   ╭ ghsa  : 2 
                        │     │                  ╰ redhat: 2 
                        │     ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/
                        │     │                  │        │           A:N 
                        │     │                  │        ╰ V3Score : 5.3 
                        │     │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/
                        │     │                           │           A:N 
                        │     │                           ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54516 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/c3
                        │     │                  │      d56dd25d52319828147c5b9aeabf2d485c250a 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/commit/e8
                        │     │                  │      8cb17006b6af4883b973058f0bb6486e5074af 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/pull/5967 
                        │     │                  ├ [5]: https://github.com/FasterXML/jackson-databind/pull/5968 
                        │     │                  ├ [6]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                  │      advisories/GHSA-9fxm-vc8v-hj55 
                        │     │                  ├ [7]: https://nvd.nist.gov/vuln/detail/CVE-2026-54516 
                        │     │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-54516 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.723Z 
                        │     ╰ LastModifiedDate: 2026-06-27T20:52:12.103Z 
                        ├ [5] ╭ VulnerabilityID : CVE-2026-54517 
                        │     ├ VendorIDs        ─ [0]: GHSA-5hh8-q8hv-fr38 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.1 
                        │     │                  ╰ UID : 6bd66f14c6cb3d57 
                        │     ├ InstalledVersion: 2.21.1 
                        │     ├ FixedVersion    : 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                        │     │                  │         dbb3a8ba81c54fa4d46 
                        │     │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                        │     │                            259639c712960695c95 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54517 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:94a93efb96402a445b2b5a5577d9858a5e28ac651c9d14d6336870
                        │     │                   687176a4df 
                        │     ├ Title           : jackson-databind: jackson-databind: Information disclosure
                        │     │                   via improper JsonView filter application 
                        │     ├ Description     : jackson-databind contains the general-purpose data-binding
                        │     │                   functionality and tree-model for Jackson Data Processor. From
                        │     │                    2.21.0 until 2.21.4 and 3.1.4, in
                        │     │                   BeanDeserializer._deserializeUsingPropertyBased, the
                        │     │                   active-view (@JsonView) filter was applied only to creator
                        │     │                   properties; the regular property-buffering branch performed
                        │     │                   no prop.visibleInView(activeView) check. A change making
                        │     │                   SetterlessProperty.isMerging() return true routed setterless
                        │     │                   Collection/Map properties through this unguarded path, so a
                        │     │                   setterless collection annotated with a restricted @JsonView
                        │     │                   is populated from attacker JSON even when the active view
                        │     │                   excludes it. This vulnerability is fixed in 2.21.4 and
                        │     │                   3.1.4. 
                        │     ├ Severity        : MEDIUM 
                        │     ├ CweIDs           ─ [0]: CWE-863 
                        │     ├ VendorSeverity   ╭ ghsa  : 2 
                        │     │                  ╰ redhat: 2 
                        │     ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/
                        │     │                  │        │           A:N 
                        │     │                  │        ╰ V3Score : 5.3 
                        │     │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/
                        │     │                           │           A:N 
                        │     │                           ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54517 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/5b
                        │     │                  │      f23edb4221f7dd2ec8e71ff6d26c61640f261d 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/commit/94
                        │     │                  │      c5d215b3af1505098c686405d9641f041a9962 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/pull/5969 
                        │     │                  ├ [5]: https://github.com/FasterXML/jackson-databind/pull/5970 
                        │     │                  ├ [6]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                  │      advisories/GHSA-5hh8-q8hv-fr38 
                        │     │                  ├ [7]: https://nvd.nist.gov/vuln/detail/CVE-2026-54517 
                        │     │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-54517 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.853Z 
                        │     ╰ LastModifiedDate: 2026-06-27T20:51:09.987Z 
                        ╰ [6] ╭ VulnerabilityID : CVE-2026-54518 
                              ├ VendorIDs        ─ [0]: GHSA-rcqc-6cw3-h962 
                              ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                              ├ PkgPath         : openaf/openaf.jar 
                              ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                              │                  │       2.21.1 
                              │                  ╰ UID : 6bd66f14c6cb3d57 
                              ├ InstalledVersion: 2.21.1 
                              ├ FixedVersion    : 2.21.4 
                              ├ Status          : fixed 
                              ├ Layer            ╭ Digest: sha256:1ad31677c9a4fb95a24c7fe677753f787279c25817788
                              │                  │         dbb3a8ba81c54fa4d46 
                              │                  ╰ DiffID: sha256:3bc849b05d522c5f28e063c55b9e67c7829930191eb06
                              │                            259639c712960695c95 
                              ├ SeveritySource  : ghsa 
                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54518 
                              ├ DataSource       ╭ ID  : ghsa 
                              │                  ├ Name: GitHub Security Advisory Maven 
                              │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                              │                          osystem%3Amaven 
                              ├ Fingerprint     : sha256:4309b07578adef8c124a315f09508fed1bccf8e845142af1781291
                              │                   8350585122 
                              ├ Title           : jackson-databind: jackson-databind: Information disclosure
                              │                   and data manipulation via view-based access control bypass 
                              ├ Description     : jackson-databind contains the general-purpose data-binding
                              │                   functionality and tree-model for Jackson Data Processor. From
                              │                    2.21.0 until 2.21.4 and 3.1.4,
                              │                   UnwrappedPropertyHandler.processUnwrappedCreatorProperties()
                              │                   replays buffered JSON into creator parameters but never
                              │                   consults prop.visibleInView(activeView). The normal
                              │                   property-based creator path gates creator properties on the
                              │                   active view, but this unwrapped-creator replay path bypasses
                              │                   that check, so a constructor parameter annotated with both
                              │                   @JsonView(AdminView.class) and @JsonUnwrapped is populated
                              │                   from attacker JSON even when a more restrictive view is
                              │                   active. This vulnerability is fixed in 2.21.4 and 3.1.4. 
                              ├ Severity        : MEDIUM 
                              ├ CweIDs           ─ [0]: CWE-863 
                              ├ VendorSeverity   ╭ ghsa  : 2 
                              │                  ╰ redhat: 2 
                              ├ CVSS             ╭ ghsa   ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L/
                              │                  │        │           A:N 
                              │                  │        ╰ V3Score : 6.5 
                              │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L/
                              │                           │           A:N 
                              │                           ╰ V3Score : 6.5 
                              ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54518 
                              │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                              │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/72
                              │                  │      1fa07ebbd4aab4a659a1a68940878315c3e341 
                              │                  ├ [3]: https://github.com/FasterXML/jackson-databind/commit/d6
                              │                  │      33bc038f200c1397c07f1a2b46f58e72c91eea 
                              │                  ├ [4]: https://github.com/FasterXML/jackson-databind/pull/5971 
                              │                  ├ [5]: https://github.com/FasterXML/jackson-databind/pull/5973 
                              │                  ├ [6]: https://github.com/FasterXML/jackson-databind/security/
                              │                  │      advisories/GHSA-rcqc-6cw3-h962 
                              │                  ├ [7]: https://nvd.nist.gov/vuln/detail/CVE-2026-54518 
                              │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-54518 
                              ├ PublishedDate   : 2026-06-23T22:16:32.073Z 
                              ╰ LastModifiedDate: 2026-06-27T20:49:30.977Z 
```
