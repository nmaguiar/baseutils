```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:deb (ubuntu 25.10) 
│     ├ Class          : os-pkgs 
│     ├ Type           : ubuntu 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : bsdextrautils@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdextrautils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 847428c8a544f66d 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:82e7845791fe42c20c588f60222f3069003b3cf11c31d9c39b768
│                       │      │                   b4e19da43e2 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [1]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : bsdextrautils@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdextrautils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 847428c8a544f66d 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0b5028210b451cab9a56a7941e6e2b65c6c50ba1f8f0f658100b2
│                       │      │                   15c91499bde 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [2]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 411fc06346b75c80 
│                       │      ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f921f0e28cbc9def72c6c0563d3d4832764c3695c788ed6290ac5
│                       │      │                   763f346f15c 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [3]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 411fc06346b75c80 
│                       │      ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fa7d45ea24d312cb6cbce2e7f29511c5cbe7f4042d47f00c0d6b0
│                       │      │                   68cadf7924f 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [4]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libblkid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : ddaca4141760dfcf 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3fd88c2ef161f863fe59f3787fd9fcf71d75ce4714adf1fc4333f
│                       │      │                   7a515934979 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [5]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libblkid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : ddaca4141760dfcf 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:dabd741d932f7421e1f480653ad5186fae2973c6d9e6e92d0a4ec
│                       │      │                   6b0701ee53c 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [6]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:dac1ab9d1d49eeda99ab1ea8d22d715c277bc6f9105d9f2fd89f7
│                       │      │                   133302b009f 
│                       │      ├ Title           : glibc: glibc: Denial of Service via iconv() function with
│                       │      │                   specific character sets 
│                       │      ├ Description     : The iconv() function in the GNU C Library versions 2.43 and
│                       │      │                   earlier may crash due to an assertion failure when
│                       │      │                   converting inputs from the IBM1390 or IBM1399 character
│                       │      │                   sets, which may be used to remotely crash an application.
│                       │      │                   
│                       │      │                   This vulnerability can be trivially mitigated by removing
│                       │      │                   the IBM1390 and IBM1399 character sets from systems that do
│                       │      │                   not need them. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-617 
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.3 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20587 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/8/ALSA-2026-20587.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [11]: https://inbox.sourceware.org/libc-announce/76814edf-c
│                       │      │                  │       f7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │      │                  ├ [12]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │      │                  ├ [13]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │      │                  ├ [14]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │      │                  ├ [15]: https://packages.fedoraproject.org/pkgs/glibc/glibc-g
│                       │      │                  │       conv-extra/ 
│                       │      │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │      │                  ├ [17]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007 
│                       │      │                  ├ [18]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │      │                  ╰ [19]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │      ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │      ╰ LastModifiedDate: 2026-04-20T22:16:23.623Z 
│                       ├ [7]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b1c920bde7bdacb367c889bf46dc78627c6a018103983e4f4cb08
│                       │      │                   9195012b4ed 
│                       │      ├ Title           : glibc: glibc: Incorrect DNS response parsing via crafted DNS
│                       │      │                    server response 
│                       │      ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │      │                   nsswitch.conf that specifies the library's DNS backend in
│                       │      │                   the GNU C Library version 2.34 to version 2.43 could, with a
│                       │      │                    crafted response from the configured DNS server, result in
│                       │      │                   a violation of the DNS specification that causes the
│                       │      │                   application to treat a non-answer section of the DNS
│                       │      │                   response as a valid answer. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-125 
│                       │      ├ VendorSeverity   ╭ alma  : 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ photon: 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ├ rocky : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [10]: https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │      │                  ├ [13]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │      │                  ╰ [15]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │      ╰ LastModifiedDate: 2026-04-07T18:41:36.647Z 
│                       ├ [8]  ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:826c4077d58be85b11fd79adb38e3f9bbb8e2abc32d5d0ce58df1
│                       │      │                   6a491fd1e29 
│                       │      ├ Title           : glibc: glibc: Invalid DNS hostname returned via
│                       │      │                   gethostbyaddr functions 
│                       │      ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │      │                   nsswitch.conf that specifies the library's DNS backend in
│                       │      │                   the GNU C library version 2.34 to version 2.43 could result
│                       │      │                   in an invalid DNS hostname being returned to the caller in
│                       │      │                   violation of the DNS specification. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-20 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ alma  : 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ├ rocky : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [10]: https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │      │                  ├ [13]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │      │                  ╰ [15]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │      ╰ LastModifiedDate: 2026-04-07T18:40:02.177Z 
│                       ├ [9]  ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1fbc475491e60ff59f81eddd802379eab3c05ddb47c66c3e1f767
│                       │      │                   7485d77241d 
│                       │      ├ Title           : glibc: glibc: Out-of-bounds write via TSIG record processing 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.2 and newer fail to
│                       │      │                    enforce the caller-supplied buffer length, and can result
│                       │      │                   in an out-of-bounds write when printing TSIG records. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-787 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-5435 
│                       │      │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.17775461
│                       │      │                  │      94.git.fweimer@redhat.com/ 
│                       │      │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-27
│                       │      │                  │      6f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-5435 
│                       │      │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34033 
│                       │      │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;f
│                       │      │                  │      =advisories/GLIBC-SA-2026-0011 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5435 
│                       │      ├ PublishedDate   : 2026-04-28T13:19:22.29Z 
│                       │      ╰ LastModifiedDate: 2026-05-05T17:38:37.03Z 
│                       ├ [10] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7894dbf05a4ec4a4d26467fa948dc96ee37fc019d3b534b42730f
│                       │      │                   ea3e99a1f4a 
│                       │      ├ Title           : glibc: glibc: Application crash or uninitialized memory read
│                       │      │                    via crafted DNS response 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.2 and newer fail to
│                       │      │                    validate the RDATA content against the RDATA length in a
│                       │      │                   DNS response when processing LOC, CERT, TKEY or TSIG
│                       │      │                   records, which may allow an attacker to craft a DNS
│                       │      │                   response, causing a target application to crash or read
│                       │      │                   uninitialized memory.
│                       │      │                   
│                       │      │                   These functions are for application debugging only and hence
│                       │      │                    not in the path of code executed by the DNS resolver. 
│                       │      │                   Further, they have been deprecated since version 2.34 and
│                       │      │                   should not be used by any new applications.  Applications
│                       │      │                   should consider porting away from these interfaces since
│                       │      │                   they may be removed in future versions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-126 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-6238 
│                       │      │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.17775461
│                       │      │                  │      94.git.fweimer@redhat.com/ 
│                       │      │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-27
│                       │      │                  │      6f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-6238 
│                       │      │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34069 
│                       │      │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;f
│                       │      │                  │      =advisories/GLIBC-SA-2026-0012 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6238 
│                       │      ├ PublishedDate   : 2026-04-28T19:37:47.523Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T17:57:24.007Z 
│                       ├ [11] ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:afbf5cf785e84081912c3c3566dacd055217cfc3eda2cc6296066
│                       │      │                   dc58cc2a5b6 
│                       │      ├ Title           : glibc: glibc: Denial of Service via iconv() function with
│                       │      │                   specific character sets 
│                       │      ├ Description     : The iconv() function in the GNU C Library versions 2.43 and
│                       │      │                   earlier may crash due to an assertion failure when
│                       │      │                   converting inputs from the IBM1390 or IBM1399 character
│                       │      │                   sets, which may be used to remotely crash an application.
│                       │      │                   
│                       │      │                   This vulnerability can be trivially mitigated by removing
│                       │      │                   the IBM1390 and IBM1399 character sets from systems that do
│                       │      │                   not need them. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-617 
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.3 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20587 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/8/ALSA-2026-20587.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [11]: https://inbox.sourceware.org/libc-announce/76814edf-c
│                       │      │                  │       f7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │      │                  ├ [12]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │      │                  ├ [13]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │      │                  ├ [14]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │      │                  ├ [15]: https://packages.fedoraproject.org/pkgs/glibc/glibc-g
│                       │      │                  │       conv-extra/ 
│                       │      │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │      │                  ├ [17]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007 
│                       │      │                  ├ [18]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │      │                  ╰ [19]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │      ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │      ╰ LastModifiedDate: 2026-04-20T22:16:23.623Z 
│                       ├ [12] ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a07e915d3a5ca15d7970f251b6863ded083a1c8ee986164ad9654
│                       │      │                   d523dae04b2 
│                       │      ├ Title           : glibc: glibc: Incorrect DNS response parsing via crafted DNS
│                       │      │                    server response 
│                       │      ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │      │                   nsswitch.conf that specifies the library's DNS backend in
│                       │      │                   the GNU C Library version 2.34 to version 2.43 could, with a
│                       │      │                    crafted response from the configured DNS server, result in
│                       │      │                   a violation of the DNS specification that causes the
│                       │      │                   application to treat a non-answer section of the DNS
│                       │      │                   response as a valid answer. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-125 
│                       │      ├ VendorSeverity   ╭ alma  : 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ photon: 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ├ rocky : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [10]: https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │      │                  ├ [13]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │      │                  ╰ [15]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │      ╰ LastModifiedDate: 2026-04-07T18:41:36.647Z 
│                       ├ [13] ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1e1096da94807e2139df721fc767ef11014c9ee7f3cdb15249732
│                       │      │                   88267dcbf23 
│                       │      ├ Title           : glibc: glibc: Invalid DNS hostname returned via
│                       │      │                   gethostbyaddr functions 
│                       │      ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │      │                   nsswitch.conf that specifies the library's DNS backend in
│                       │      │                   the GNU C library version 2.34 to version 2.43 could result
│                       │      │                   in an invalid DNS hostname being returned to the caller in
│                       │      │                   violation of the DNS specification. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-20 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ alma  : 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ├ rocky : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [10]: https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │      │                  ├ [13]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │      │                  ╰ [15]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │      ╰ LastModifiedDate: 2026-04-07T18:40:02.177Z 
│                       ├ [14] ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:37ea591758c6ef543e10cd727580e1879faf507941cb0c1385ff0
│                       │      │                   55d34861148 
│                       │      ├ Title           : glibc: glibc: Out-of-bounds write via TSIG record processing 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.2 and newer fail to
│                       │      │                    enforce the caller-supplied buffer length, and can result
│                       │      │                   in an out-of-bounds write when printing TSIG records. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-787 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-5435 
│                       │      │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.17775461
│                       │      │                  │      94.git.fweimer@redhat.com/ 
│                       │      │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-27
│                       │      │                  │      6f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-5435 
│                       │      │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34033 
│                       │      │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;f
│                       │      │                  │      =advisories/GLIBC-SA-2026-0011 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5435 
│                       │      ├ PublishedDate   : 2026-04-28T13:19:22.29Z 
│                       │      ╰ LastModifiedDate: 2026-05-05T17:38:37.03Z 
│                       ├ [15] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:72eb300a158607931ec2d4a9ad0db94571c329fab070d3063cb62
│                       │      │                   5145ba7bce2 
│                       │      ├ Title           : glibc: glibc: Application crash or uninitialized memory read
│                       │      │                    via crafted DNS response 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.2 and newer fail to
│                       │      │                    validate the RDATA content against the RDATA length in a
│                       │      │                   DNS response when processing LOC, CERT, TKEY or TSIG
│                       │      │                   records, which may allow an attacker to craft a DNS
│                       │      │                   response, causing a target application to crash or read
│                       │      │                   uninitialized memory.
│                       │      │                   
│                       │      │                   These functions are for application debugging only and hence
│                       │      │                    not in the path of code executed by the DNS resolver. 
│                       │      │                   Further, they have been deprecated since version 2.34 and
│                       │      │                   should not be used by any new applications.  Applications
│                       │      │                   should consider porting away from these interfaces since
│                       │      │                   they may be removed in future versions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-126 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-6238 
│                       │      │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.17775461
│                       │      │                  │      94.git.fweimer@redhat.com/ 
│                       │      │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-27
│                       │      │                  │      6f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-6238 
│                       │      │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34069 
│                       │      │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;f
│                       │      │                  │      =advisories/GLIBC-SA-2026-0012 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6238 
│                       │      ├ PublishedDate   : 2026-04-28T19:37:47.523Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T17:57:24.007Z 
│                       ├ [16] ╭ VulnerabilityID : CVE-2025-66382 
│                       │      ├ PkgID           : libexpat1@2.7.1-2ubuntu0.2 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.1-2ubuntu0.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : bb3ed74d0fd332c6 
│                       │      ├ InstalledVersion: 2.7.1-2ubuntu0.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:de864c5f1cbdd577263d660e3f21206f4d9e8656b969858e74fca
│                       │      │                   2e76e00f6f5 
│                       │      ├ Title           : libexpat: libexpat: Denial of service via crafted file
│                       │      │                   processing 
│                       │      ├ Description     : In libexpat through 2.7.3, a crafted file with an
│                       │      │                   approximate size of 2 MiB can lead to dozens of seconds of
│                       │      │                   processing time. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-407 
│                       │      ├ VendorSeverity   ╭ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 2.9 
│                       │      ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2025/12/02/1 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2025-66382 
│                       │      │                  ├ [2]: https://cert-portal.siemens.com/productcert/html/ssa-0
│                       │      │                  │      82556.html 
│                       │      │                  ├ [3]: https://cert-portal.siemens.com/productcert/html/ssa-2
│                       │      │                  │      53495.html 
│                       │      │                  ├ [4]: https://github.com/libexpat/libexpat/issues/1076 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2025-66382 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2025-66382 
│                       │      ├ PublishedDate   : 2025-11-28T07:15:57.9Z 
│                       │      ╰ LastModifiedDate: 2026-06-02T14:16:37.12Z 
│                       ├ [17] ╭ VulnerabilityID : CVE-2024-2236 
│                       │      ├ PkgID           : libgcrypt20@1.11.0-7ubuntu0.1 
│                       │      ├ PkgName         : libgcrypt20 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libgcrypt20@1.11.0-7ubuntu0.1?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 8f3635c00dca0a4f 
│                       │      ├ InstalledVersion: 1.11.0-7ubuntu0.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-2236 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6506faf6c3dbe05c4eace1aeced6188e6a9cf0b5a34528fe0eb39
│                       │      │                   63971711a54 
│                       │      ├ Title           : libgcrypt: vulnerable to Marvin Attack 
│                       │      ├ Description     : A timing-based side-channel flaw was found in libgcrypt's
│                       │      │                   RSA implementation. This issue may allow a remote attacker
│                       │      │                   to initiate a Bleichenbacher-style attack, which can lead to
│                       │      │                    the decryption of RSA ciphertexts. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-385 
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2024:9404 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2025:3530 
│                       │      │                  ├ [2] : https://access.redhat.com/errata/RHSA-2025:3534 
│                       │      │                  ├ [3] : https://access.redhat.com/security/cve/CVE-2024-2236 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2245218 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2245218 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2268268 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       24-2236 
│                       │      │                  ├ [8] : https://dev.gnupg.org/T7136 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2024-9404.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2024:9404 
│                       │      │                  ├ [11]: https://github.com/tomato42/marvin-toolkit/tree/maste
│                       │      │                  │       r/example/libgcrypt 
│                       │      │                  ├ [12]: https://gitlab.com/redhat-crypto/libgcrypt/libgcrypt-
│                       │      │                  │       mirror/-/merge_requests/17 
│                       │      │                  ├ [13]: https://linux.oracle.com/cve/CVE-2024-2236.html 
│                       │      │                  ├ [14]: https://linux.oracle.com/errata/ELSA-2024-9404.html 
│                       │      │                  ├ [15]: https://lists.gnupg.org/pipermail/gcrypt-devel/2024-M
│                       │      │                  │       arch/005607.html 
│                       │      │                  ├ [16]: https://nvd.nist.gov/vuln/detail/CVE-2024-2236 
│                       │      │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2024-2236 
│                       │      ├ PublishedDate   : 2024-03-06T22:15:57.977Z 
│                       │      ╰ LastModifiedDate: 2026-04-15T00:35:42.02Z 
│                       ├ [18] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : liblastlog2-2 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 6aa63af50fb78d18 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f11898a9c8e8707f03d8d58389d3de67ea42cdea6b22da2da228d
│                       │      │                   b3677a254f5 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [19] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : liblastlog2-2 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 6aa63af50fb78d18 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5dfe55fb154974f9576edfc77fa86b87bf3248bc9ad79efa4bd50
│                       │      │                   8191a9e72b9 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [20] ╭ VulnerabilityID : CVE-2026-34743 
│                       │      ├ PkgID           : liblzma5@5.8.1-1build2 
│                       │      ├ PkgName         : liblzma5 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblzma5@5.8.1-1build2?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-25.10 
│                       │      │                  ╰ UID : c6d7a6fa1546d4a2 
│                       │      ├ InstalledVersion: 5.8.1-1build2 
│                       │      ├ FixedVersion    : 5.8.1-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34743 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a5bf3e9db255c8e5e4718666400f513b5fd07f7627d9fd8516a0e
│                       │      │                   3f065899cb2 
│                       │      ├ Title           : xz: XZ Utils: Denial of Service via buffer overflow in index
│                       │      │                    decoding 
│                       │      ├ Description     : XZ Utils provide a general-purpose data-compression library
│                       │      │                   plus command-line tools. Prior to version 5.8.3, if
│                       │      │                   lzma_index_decoder() was used to decode an Index that
│                       │      │                   contained no Records, the resulting lzma_index was left in a
│                       │      │                    state where where a subsequent lzma_index_append() would
│                       │      │                   allocate too little memory, and a buffer overflow would
│                       │      │                   occur. This issue has been patched in version 5.8.3. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-122 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.3 
│                       │      ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/03/31/13 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-34743 
│                       │      │                  ├ [2]: https://github.com/tukaani-project/xz/commit/c8c22869e
│                       │      │                  │      780ff57c96b46939c3d79ff99395f87 
│                       │      │                  ├ [3]: https://github.com/tukaani-project/xz/releases/tag/v5.
│                       │      │                  │      8.3 
│                       │      │                  ├ [4]: https://github.com/tukaani-project/xz/security/advisor
│                       │      │                  │      ies/GHSA-x872-m794-cxhv 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-34743 
│                       │      │                  ├ [6]: https://tukaani.org/xz/index-append-overflow.html 
│                       │      │                  ├ [7]: https://ubuntu.com/security/notices/USN-8362-1 
│                       │      │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34743 
│                       │      ├ PublishedDate   : 2026-04-02T19:21:33.187Z 
│                       │      ╰ LastModifiedDate: 2026-04-15T17:33:17.68Z 
│                       ├ [21] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : e278fd35c2ddbe27 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:28526785211c35cb132d43bd8fb0b122bd80ffabd03cc175591b5
│                       │      │                   12228ffe14c 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [22] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : e278fd35c2ddbe27 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:11d4ab076379130c83b6c499bebc7794c0d1167c2e61f7a8d7360
│                       │      │                   dc693304eb9 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [23] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13@3.13.7-1ubuntu0.4?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : d39243325c040cfa 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7dc6ca6c076e53e1159b85101590be2dd50e1300c62254c2f2eb0
│                       │      │                   24266124054 
│                       │      ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │      ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │      │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │      │                   (a base class) and so does not use io.open_code() to read
│                       │      │                   the .pyc files. sys.audit handlers for this audit event
│                       │      │                   therefore do not fire. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-668 
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 1 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/05/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:19177 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │      │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │      │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │      │                  ├ [11]: https://bugzilla.redhat.com/2449649 
│                       │      │                  ├ [12]: https://bugzilla.redhat.com/2457409 
│                       │      │                  ├ [13]: https://bugzilla.redhat.com/2457932 
│                       │      │                  ├ [14]: https://bugzilla.redhat.com/2458049 
│                       │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │      │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │      │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │      │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │      │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │      │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │      │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │      │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │      │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │      │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │      │                  ├ [26]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │      │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-13837 
│                       │      │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-15282 
│                       │      │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-59375 
│                       │      │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-6075 
│                       │      │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-0672 
│                       │      │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-1502 
│                       │      │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-2297 
│                       │      │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-3644 
│                       │      │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4224 
│                       │      │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4519 
│                       │      │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4786 
│                       │      │                  ├ [38]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-6100 
│                       │      │                  ├ [39]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │      │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │      │                  ├ [41]: https://github.com/python/cpython/commit/482d6f8bdba9
│                       │      │                  │       da3725d272e8bb4a2d25fb6a603e 
│                       │      │                  ├ [42]: https://github.com/python/cpython/commit/69ddd9bb2cc4
│                       │      │                  │       bd69b1565647c18659c6a789ccd9 
│                       │      │                  ├ [43]: https://github.com/python/cpython/commit/876858c9f65d
│                       │      │                  │       9ab656c7fa639f268ce7856d89dd 
│                       │      │                  ├ [44]: https://github.com/python/cpython/commit/a51b1b512de1
│                       │      │                  │       d56b3714b65628a2eae2b07e535e 
│                       │      │                  ├ [45]: https://github.com/python/cpython/commit/e58e9802b9be
│                       │      │                  │       c5cdbf48fc9bf1da5f4fda482e86 
│                       │      │                  ├ [46]: https://github.com/python/cpython/issues/145506 
│                       │      │                  ├ [47]: https://github.com/python/cpython/pull/145507 
│                       │      │                  ├ [48]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │      │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │      │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ╰ [51]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [24] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13-minimal@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13-minimal 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-minimal@3.13.7-1ubuntu0.
│                       │      │                  │       4?arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 18ff49702a1cf723 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fe8510cd03a12d2e9ff3245d5ea779e1447ad5d79924008cc25ea
│                       │      │                   63667f9dbe9 
│                       │      ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │      ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │      │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │      │                   (a base class) and so does not use io.open_code() to read
│                       │      │                   the .pyc files. sys.audit handlers for this audit event
│                       │      │                   therefore do not fire. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-668 
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 1 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/05/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:19177 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │      │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │      │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │      │                  ├ [11]: https://bugzilla.redhat.com/2449649 
│                       │      │                  ├ [12]: https://bugzilla.redhat.com/2457409 
│                       │      │                  ├ [13]: https://bugzilla.redhat.com/2457932 
│                       │      │                  ├ [14]: https://bugzilla.redhat.com/2458049 
│                       │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │      │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │      │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │      │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │      │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │      │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │      │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │      │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │      │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │      │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │      │                  ├ [26]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │      │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-13837 
│                       │      │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-15282 
│                       │      │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-59375 
│                       │      │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-6075 
│                       │      │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-0672 
│                       │      │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-1502 
│                       │      │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-2297 
│                       │      │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-3644 
│                       │      │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4224 
│                       │      │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4519 
│                       │      │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4786 
│                       │      │                  ├ [38]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-6100 
│                       │      │                  ├ [39]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │      │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │      │                  ├ [41]: https://github.com/python/cpython/commit/482d6f8bdba9
│                       │      │                  │       da3725d272e8bb4a2d25fb6a603e 
│                       │      │                  ├ [42]: https://github.com/python/cpython/commit/69ddd9bb2cc4
│                       │      │                  │       bd69b1565647c18659c6a789ccd9 
│                       │      │                  ├ [43]: https://github.com/python/cpython/commit/876858c9f65d
│                       │      │                  │       9ab656c7fa639f268ce7856d89dd 
│                       │      │                  ├ [44]: https://github.com/python/cpython/commit/a51b1b512de1
│                       │      │                  │       d56b3714b65628a2eae2b07e535e 
│                       │      │                  ├ [45]: https://github.com/python/cpython/commit/e58e9802b9be
│                       │      │                  │       c5cdbf48fc9bf1da5f4fda482e86 
│                       │      │                  ├ [46]: https://github.com/python/cpython/issues/145506 
│                       │      │                  ├ [47]: https://github.com/python/cpython/pull/145507 
│                       │      │                  ├ [48]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │      │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │      │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ╰ [51]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [25] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13-stdlib@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13-stdlib 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-stdlib@3.13.7-1ubuntu0.4
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 12c1ecba4fa9bb94 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a1d65bc631defca7e885ad7a1327f773c91d9cf83b4b46caa6096
│                       │      │                   04bd4194163 
│                       │      ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │      ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │      │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │      │                   (a base class) and so does not use io.open_code() to read
│                       │      │                   the .pyc files. sys.audit handlers for this audit event
│                       │      │                   therefore do not fire. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-668 
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 1 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/05/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:19177 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │      │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │      │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │      │                  ├ [11]: https://bugzilla.redhat.com/2449649 
│                       │      │                  ├ [12]: https://bugzilla.redhat.com/2457409 
│                       │      │                  ├ [13]: https://bugzilla.redhat.com/2457932 
│                       │      │                  ├ [14]: https://bugzilla.redhat.com/2458049 
│                       │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │      │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │      │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │      │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │      │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │      │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │      │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │      │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │      │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │      │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │      │                  ├ [26]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │      │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-13837 
│                       │      │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-15282 
│                       │      │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-59375 
│                       │      │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-6075 
│                       │      │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-0672 
│                       │      │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-1502 
│                       │      │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-2297 
│                       │      │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-3644 
│                       │      │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4224 
│                       │      │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4519 
│                       │      │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4786 
│                       │      │                  ├ [38]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-6100 
│                       │      │                  ├ [39]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │      │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │      │                  ├ [41]: https://github.com/python/cpython/commit/482d6f8bdba9
│                       │      │                  │       da3725d272e8bb4a2d25fb6a603e 
│                       │      │                  ├ [42]: https://github.com/python/cpython/commit/69ddd9bb2cc4
│                       │      │                  │       bd69b1565647c18659c6a789ccd9 
│                       │      │                  ├ [43]: https://github.com/python/cpython/commit/876858c9f65d
│                       │      │                  │       9ab656c7fa639f268ce7856d89dd 
│                       │      │                  ├ [44]: https://github.com/python/cpython/commit/a51b1b512de1
│                       │      │                  │       d56b3714b65628a2eae2b07e535e 
│                       │      │                  ├ [45]: https://github.com/python/cpython/commit/e58e9802b9be
│                       │      │                  │       c5cdbf48fc9bf1da5f4fda482e86 
│                       │      │                  ├ [46]: https://github.com/python/cpython/issues/145506 
│                       │      │                  ├ [47]: https://github.com/python/cpython/pull/145507 
│                       │      │                  ├ [48]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │      │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │      │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ╰ [51]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [26] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:01a43efcd77138d29d183d92b883e49c4dc33af6d071fbcf27221
│                       │      │                   f58fa7d4f16 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [27] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ee8e5897e2dcc226123fc64f660e0c037f9dbef7065baed178f46
│                       │      │                   79ede15a861 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [28] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23db7c315eddf1f4 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4c1ef4bdb40f0694dc8dc48a32f518481343c502b4bdb33128c71
│                       │      │                   3ec68e2ae0d 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [29] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23db7c315eddf1f4 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5b89267d6bed8c379c669c1590d3ce0e8d3887c77dc0a18b276b7
│                       │      │                   d49ba5fd832 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [30] ╭ VulnerabilityID : CVE-2026-1757 
│                       │      ├ PkgID           : libxml2-16@2.14.5+dfsg-0.2ubuntu0.1 
│                       │      ├ PkgName         : libxml2-16 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libxml2-16@2.14.5%2Bdfsg-0.2ubuntu0.1?
│                       │      │                  │       arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 713b877d62e397e4 
│                       │      ├ InstalledVersion: 2.14.5+dfsg-0.2ubuntu0.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-1757 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:069f06a30e221669b336f6a124085f3b4db61ec51f0acf71c6fbb
│                       │      │                   e483e7ccb04 
│                       │      ├ Title           : libxml2: Memory Leak Leading to Local Denial of Service in
│                       │      │                   xmllint Interactive Shell 
│                       │      ├ Description     : A flaw was identified in the interactive shell of the
│                       │      │                   xmllint utility, part of the libxml2 project, where memory
│                       │      │                   allocated for user input is not properly released under
│                       │      │                   certain conditions. When a user submits input consisting
│                       │      │                   only of whitespace, the program skips command execution but
│                       │      │                   fails to free the allocated buffer. Repeating this action
│                       │      │                   causes memory to continuously accumulate. Over time, this
│                       │      │                   can exhaust system memory and terminate the xmllint process,
│                       │      │                    creating a denial-of-service condition on the local
│                       │      │                   system. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-401 
│                       │      ├ VendorSeverity   ╭ amazon: 1 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.2 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7519 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-1757 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2435940 
│                       │      │                  ├ [3]: https://gitlab.gnome.org/GNOME/libxml2/-/issues/1009 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-1757 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-1757 
│                       │      ├ PublishedDate   : 2026-02-02T13:15:58.58Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T10:16:50.683Z 
│                       ├ [31] ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:88ab381534d7d41af422bcd5c0fcb6b1f0a4afd9ef6523e9d32c5
│                       │      │                   aee5441668e 
│                       │      ├ Title           : glibc: glibc: Denial of Service via iconv() function with
│                       │      │                   specific character sets 
│                       │      ├ Description     : The iconv() function in the GNU C Library versions 2.43 and
│                       │      │                   earlier may crash due to an assertion failure when
│                       │      │                   converting inputs from the IBM1390 or IBM1399 character
│                       │      │                   sets, which may be used to remotely crash an application.
│                       │      │                   
│                       │      │                   This vulnerability can be trivially mitigated by removing
│                       │      │                   the IBM1390 and IBM1399 character sets from systems that do
│                       │      │                   not need them. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-617 
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.3 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20587 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/8/ALSA-2026-20587.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [11]: https://inbox.sourceware.org/libc-announce/76814edf-c
│                       │      │                  │       f7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │      │                  ├ [12]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │      │                  ├ [13]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │      │                  ├ [14]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │      │                  ├ [15]: https://packages.fedoraproject.org/pkgs/glibc/glibc-g
│                       │      │                  │       conv-extra/ 
│                       │      │                  ├ [16]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │      │                  ├ [17]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007 
│                       │      │                  ├ [18]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │      │                  ╰ [19]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │      ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │      ╰ LastModifiedDate: 2026-04-20T22:16:23.623Z 
│                       ├ [32] ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:056cecdcf8ddc75f4c0b803cbc690fe6b9b6ae475d3aa5e0196b6
│                       │      │                   aebba67be9b 
│                       │      ├ Title           : glibc: glibc: Incorrect DNS response parsing via crafted DNS
│                       │      │                    server response 
│                       │      ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │      │                   nsswitch.conf that specifies the library's DNS backend in
│                       │      │                   the GNU C Library version 2.34 to version 2.43 could, with a
│                       │      │                    crafted response from the configured DNS server, result in
│                       │      │                   a violation of the DNS specification that causes the
│                       │      │                   application to treat a non-answer section of the DNS
│                       │      │                   response as a valid answer. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-125 
│                       │      ├ VendorSeverity   ╭ alma  : 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ photon: 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ├ rocky : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [10]: https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │      │                  ├ [13]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │      │                  ╰ [15]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │      ╰ LastModifiedDate: 2026-04-07T18:41:36.647Z 
│                       ├ [33] ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:51a5c8e96b5a4908fa8e4c7c54ac93d773f8b7f9ab79343802c58
│                       │      │                   f27e7e7bf71 
│                       │      ├ Title           : glibc: glibc: Invalid DNS hostname returned via
│                       │      │                   gethostbyaddr functions 
│                       │      ├ Description     : Calling gethostbyaddr or gethostbyaddr_r with a configured
│                       │      │                   nsswitch.conf that specifies the library's DNS backend in
│                       │      │                   the GNU C library version 2.34 to version 2.43 could result
│                       │      │                   in an invalid DNS hostname being returned to the caller in
│                       │      │                   violation of the DNS specification. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-20 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ alma  : 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ├ rocky : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [9] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [10]: https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2026:20597 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │      │                  ├ [13]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │      │                  ╰ [15]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │      ╰ LastModifiedDate: 2026-04-07T18:40:02.177Z 
│                       ├ [34] ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e91de7af00f85975cec01b9c2f20c7c021fed0828ac8691ee74ba
│                       │      │                   709231172de 
│                       │      ├ Title           : glibc: glibc: Out-of-bounds write via TSIG record processing 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.2 and newer fail to
│                       │      │                    enforce the caller-supplied buffer length, and can result
│                       │      │                   in an out-of-bounds write when printing TSIG records. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-787 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-5435 
│                       │      │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.17775461
│                       │      │                  │      94.git.fweimer@redhat.com/ 
│                       │      │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-27
│                       │      │                  │      6f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-5435 
│                       │      │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34033 
│                       │      │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;f
│                       │      │                  │      =advisories/GLIBC-SA-2026-0011 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5435 
│                       │      ├ PublishedDate   : 2026-04-28T13:19:22.29Z 
│                       │      ╰ LastModifiedDate: 2026-05-05T17:38:37.03Z 
│                       ├ [35] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2a98b2bfe340abb56c70f1242ce984a6db5bef1368aed172a9612
│                       │      │                   325a39ab511 
│                       │      ├ Title           : glibc: glibc: Application crash or uninitialized memory read
│                       │      │                    via crafted DNS response 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.2 and newer fail to
│                       │      │                    validate the RDATA content against the RDATA length in a
│                       │      │                   DNS response when processing LOC, CERT, TKEY or TSIG
│                       │      │                   records, which may allow an attacker to craft a DNS
│                       │      │                   response, causing a target application to crash or read
│                       │      │                   uninitialized memory.
│                       │      │                   
│                       │      │                   These functions are for application debugging only and hence
│                       │      │                    not in the path of code executed by the DNS resolver. 
│                       │      │                   Further, they have been deprecated since version 2.34 and
│                       │      │                   should not be used by any new applications.  Applications
│                       │      │                   should consider porting away from these interfaces since
│                       │      │                   they may be removed in future versions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-126 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-6238 
│                       │      │                  ├ [1]: https://inbox.sourceware.org/libc-alpha/cover.17775461
│                       │      │                  │      94.git.fweimer@redhat.com/ 
│                       │      │                  ├ [2]: https://inbox.sourceware.org/libc-announce/7a655d55-27
│                       │      │                  │      6f-41fe-b550-feb3ebb2ce91@redhat.com/T/#u 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-6238 
│                       │      │                  ├ [4]: https://sourceware.org/bugzilla/show_bug.cgi?id=34069 
│                       │      │                  ├ [5]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;f
│                       │      │                  │      =advisories/GLIBC-SA-2026-0012 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6238 
│                       │      ├ PublishedDate   : 2026-04-28T19:37:47.523Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T17:57:24.007Z 
│                       ├ [36] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1d1505473b62d91fa1ced95ee93bf0e557831d22189eb1b7bdf3b
│                       │      │                   b4049953753 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [37] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ffd9728c7a34f8d3e1bbc2e763eb4c13941eabe38b181132886de
│                       │      │                   f35a8900643 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [38] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : login.defs@1:4.17.4-2ubuntu2 
│                       │      ├ PkgName         : login.defs 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu2?arch=all&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 685157e74dbd875c 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1bad4de11de4deef210c33b068dfd35cb017c12c6e59f1d31e9e6
│                       │      │                   30cc52d3999 
│                       │      ├ Title           : shadow-utils: Default subordinate ID configuration in
│                       │      │                   /etc/login.defs could lead to compromise 
│                       │      ├ Description     : shadow-utils (aka shadow) 4.4 through 4.17.0 establishes a
│                       │      │                   default /etc/subuid behavior (e.g., uid 100000 through
│                       │      │                   165535 for the first user account) that can realistically
│                       │      │                   conflict with the uids of users defined on locally
│                       │      │                   administered networks, potentially leading to account
│                       │      │                   takeover, e.g., by leveraging newuidmap for access to an NFS
│                       │      │                    home directory (or same-host resources in the case of
│                       │      │                   remote logins by these local network users). NOTE: it may
│                       │      │                   also be argued that system administrators should not have
│                       │      │                   assigned uids, within local networks, that are within the
│                       │      │                   range that can occur in /etc/subuid. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-1188 
│                       │      ├ VendorSeverity   ╭ alma       : 1 
│                       │      │                  ├ azure      : 1 
│                       │      │                  ├ oracle-oval: 1 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 1 
│                       │      │                  ╰ ubuntu     : 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.6 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2025:20559 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2024-56433 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2334165 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2334165 
│                       │      │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       24-56433 
│                       │      │                  ├ [5] : https://errata.almalinux.org/9/ALSA-2025-20559.html 
│                       │      │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20559 
│                       │      │                  ├ [7] : https://github.com/shadow-maint/shadow/blob/e2512d574
│                       │      │                  │       1d4a44bdd81a8c2d0029b6222728cf0/etc/login.defs#L238-L
│                       │      │                  │       241 
│                       │      │                  ├ [8] : https://github.com/shadow-maint/shadow/issues/1157 
│                       │      │                  ├ [9] : https://github.com/shadow-maint/shadow/releases/tag/4.4 
│                       │      │                  ├ [10]: https://linux.oracle.com/cve/CVE-2024-56433.html 
│                       │      │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2025-20559-0.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2024-56433 
│                       │      │                  ╰ [13]: https://www.cve.org/CVERecord?id=CVE-2024-56433 
│                       │      ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │      ╰ LastModifiedDate: 2026-04-15T00:35:42.02Z 
│                       ├ [39] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : f2821a9fde7aa805 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e55abf39f060976fdcf844844bd894615d18285ac306e6ac3a09c
│                       │      │                   28f724bc5d1 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [40] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : f2821a9fde7aa805 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:46ae7286e2f1876dd037152afd333a3bb96968eeb324067e02757
│                       │      │                   a86dd2df8a9 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [41] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : passwd@1:4.17.4-2ubuntu2 
│                       │      ├ PkgName         : passwd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu2?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 2d87ef360f209a3f 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5b8fbd12c4fa0ced542c002b2d7364b680d3548b1bd3af7340ba5
│                       │      │                   1fe7596e8b0 
│                       │      ├ Title           : shadow-utils: Default subordinate ID configuration in
│                       │      │                   /etc/login.defs could lead to compromise 
│                       │      ├ Description     : shadow-utils (aka shadow) 4.4 through 4.17.0 establishes a
│                       │      │                   default /etc/subuid behavior (e.g., uid 100000 through
│                       │      │                   165535 for the first user account) that can realistically
│                       │      │                   conflict with the uids of users defined on locally
│                       │      │                   administered networks, potentially leading to account
│                       │      │                   takeover, e.g., by leveraging newuidmap for access to an NFS
│                       │      │                    home directory (or same-host resources in the case of
│                       │      │                   remote logins by these local network users). NOTE: it may
│                       │      │                   also be argued that system administrators should not have
│                       │      │                   assigned uids, within local networks, that are within the
│                       │      │                   range that can occur in /etc/subuid. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-1188 
│                       │      ├ VendorSeverity   ╭ alma       : 1 
│                       │      │                  ├ azure      : 1 
│                       │      │                  ├ oracle-oval: 1 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 1 
│                       │      │                  ╰ ubuntu     : 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.6 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2025:20559 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2024-56433 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2334165 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2334165 
│                       │      │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       24-56433 
│                       │      │                  ├ [5] : https://errata.almalinux.org/9/ALSA-2025-20559.html 
│                       │      │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20559 
│                       │      │                  ├ [7] : https://github.com/shadow-maint/shadow/blob/e2512d574
│                       │      │                  │       1d4a44bdd81a8c2d0029b6222728cf0/etc/login.defs#L238-L
│                       │      │                  │       241 
│                       │      │                  ├ [8] : https://github.com/shadow-maint/shadow/issues/1157 
│                       │      │                  ├ [9] : https://github.com/shadow-maint/shadow/releases/tag/4.4 
│                       │      │                  ├ [10]: https://linux.oracle.com/cve/CVE-2024-56433.html 
│                       │      │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2025-20559-0.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2024-56433 
│                       │      │                  ╰ [13]: https://www.cve.org/CVERecord?id=CVE-2024-56433 
│                       │      ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │      ╰ LastModifiedDate: 2026-04-15T00:35:42.02Z 
│                       ├ [42] ╭ VulnerabilityID : CVE-2026-35338 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35338 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:56e74ffdbdf1a90a128fcf8c8443ce26fbc9a29b619594129d00a
│                       │      │                   be1a7e02928 
│                       │      ├ Title           : A vulnerability in the chmod utility of uutils coreutils
│                       │      │                   allows users  ... 
│                       │      ├ Description     : A vulnerability in the chmod utility of uutils coreutils
│                       │      │                   allows users to bypass the --preserve-root safety mechanism.
│                       │      │                    The implementation only validates if the target path is
│                       │      │                   literally / and does not canonicalize the path. An attacker
│                       │      │                   or accidental user can use path variants such as /../ or
│                       │      │                   symbolic links to execute destructive recursive operations
│                       │      │                   (e.g., chmod -R 000) on the entire root filesystem, leading
│                       │      │                   to system-wide permission loss and potential complete system
│                       │      │                    breakdown. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-22 
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:H/I:H/A:H 
│                       │      │                         ╰ V3Score : 7.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/413055b378f
│                       │      │                  │      a6fe2299c5e5f538c8e6e841ab810 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10033 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35338 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35338 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:35.583Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:28:50.307Z 
│                       ├ [43] ╭ VulnerabilityID : CVE-2026-35339 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35339 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:80b8150e34f289cfff2d6006471c4ecf7c625e6820cecdc48427f
│                       │      │                   40e8ffd97df 
│                       │      ├ Title           : The recursive mode (-R) of the chmod utility in uutils
│                       │      │                   coreutils incor ... 
│                       │      ├ Description     : The recursive mode (-R) of the chmod utility in uutils
│                       │      │                   coreutils incorrectly handles exit codes when processing
│                       │      │                   multiple files. The final return value is determined solely
│                       │      │                   by the success or failure of the last file processed. This
│                       │      │                   allows the command to return an exit code of 0 (success)
│                       │      │                   even if errors were encountered on previous files, such as
│                       │      │                   'Operation not permitted'. Scripts relying on these exit
│                       │      │                   codes may proceed under a false sense of success while
│                       │      │                   sensitive files remain with restrictive or incorrect
│                       │      │                   permissions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-253 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:H/A:N 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/abd581f62e9
│                       │      │                  │      7d0b147306ac40eac13af71c6fbba 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/9793 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35339 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35339 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:35.767Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:14:43.883Z 
│                       ├ [44] ╭ VulnerabilityID : CVE-2026-35340 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35340 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e6e650a499bed2c9f6170d7d78cf0e42f22be106ae6ec181d6c04
│                       │      │                   db95634bcf2 
│                       │      ├ Title           : A flaw in the ChownExecutor used by uutils coreutils chown
│                       │      │                   and chgrp c ... 
│                       │      ├ Description     : A flaw in the ChownExecutor used by uutils coreutils chown
│                       │      │                   and chgrp causes the utilities to return an incorrect exit
│                       │      │                   code during recursive operations. The final exit code is
│                       │      │                   determined only by the last file processed. If the last
│                       │      │                   operation succeeds, the command returns 0 even if earlier
│                       │      │                   ownership or group changes failed due to permission errors.
│                       │      │                   This can lead to security misconfigurations where
│                       │      │                   administrative scripts incorrectly assume that ownership has
│                       │      │                    been successfully transferred across a directory tree. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-253 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:H/A:N 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/ebc08af9c34
│                       │      │                  │      138f474b32ea0ef34bed3b086a3ed 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10035 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35340 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35340 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:35.923Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:12:01.5Z 
│                       ├ [45] ╭ VulnerabilityID : CVE-2026-35341 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cf3e52296aa378e7ded99abc10dff37955e4825d63ea3f6110773
│                       │      │                   94f5577f6bf 
│                       │      ├ Title           : A vulnerability in uutils coreutils mkfifo allows for the
│                       │      │                   unauthorized ... 
│                       │      ├ Description     : A vulnerability in uutils coreutils mkfifo allows for the
│                       │      │                   unauthorized modification of permissions on existing files.
│                       │      │                   When mkfifo fails to create a FIFO because a file already
│                       │      │                   exists at the target path, it fails to terminate the
│                       │      │                   operation for that path and continues to execute a follow-up
│                       │      │                    set_permissions call. This results in the existing file's
│                       │      │                   permissions being changed to the default mode (often 644
│                       │      │                   after umask), potentially exposing sensitive files such as
│                       │      │                   SSH private keys to other users on the system. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-732 
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:N 
│                       │      │                         ╰ V3Score : 7.1 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10020 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35341 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35341 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.06Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:05:55.067Z 
│                       ├ [46] ╭ VulnerabilityID : CVE-2026-35342 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35342 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6b814cb7ddc9bf317b1aea4d73f7fdd8832f1defc6c2d96e34f31
│                       │      │                   1696af55432 
│                       │      ├ Title           : The mktemp utility in uutils coreutils fails to properly
│                       │      │                   handle an emp ... 
│                       │      ├ Description     : The mktemp utility in uutils coreutils fails to properly
│                       │      │                   handle an empty TMPDIR environment variable. Unlike GNU
│                       │      │                   mktemp, which falls back to /tmp when TMPDIR is an empty
│                       │      │                   string, the uutils implementation treats the empty string as
│                       │      │                    a valid path. This causes temporary files to be created in
│                       │      │                   the current working directory (CWD) instead of the intended
│                       │      │                   secure temporary directory. If the CWD is more permissive or
│                       │      │                    accessible to other users than /tmp, it may lead to
│                       │      │                   unintended information disclosure or unauthorized access to
│                       │      │                   temporary data. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-377 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/eb25ec328b2
│                       │      │                  │      26d8fbbaa4058bf9187165bf06d51 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10566 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35342 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35342 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.217Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:11:32.34Z 
│                       ├ [47] ╭ VulnerabilityID : CVE-2026-35343 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35343 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:293c817ff073ae9c7bd98df9e2c5e98246e8512419ea13775a349
│                       │      │                   c3189737a00 
│                       │      ├ Title           : The cut utility in uutils coreutils incorrectly handles the
│                       │      │                   -s (only-d ... 
│                       │      ├ Description     : The cut utility in uutils coreutils incorrectly handles the
│                       │      │                   -s (only-delimited) option when a newline character is
│                       │      │                   specified as the delimiter. The implementation fails to
│                       │      │                   verify the only_delimited flag in the
│                       │      │                   cut_fields_newline_char_delim function, causing the utility
│                       │      │                   to print non-delimited lines that should have been
│                       │      │                   suppressed. This can lead to unexpected data being passed to
│                       │      │                    downstream scripts that rely on strict output filtering. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-670 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/9bbb58b746c
│                       │      │                  │      41802278b0cba738eebbf21517cf7 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11143 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35343 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35343 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.357Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:10:47.587Z 
│                       ├ [48] ╭ VulnerabilityID : CVE-2026-35344 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:22292da125f809ce107849243aec2728ed3dd813947d5794d6c6d
│                       │      │                   e2156658cea 
│                       │      ├ Title           : The dd utility in uutils coreutils suppresses errors during
│                       │      │                   file trunc ... 
│                       │      ├ Description     : The dd utility in uutils coreutils suppresses errors during
│                       │      │                   file truncation operations by unconditionally calling
│                       │      │                   Result::ok() on truncation attempts. While intended to mimic
│                       │      │                    GNU behavior for special files like /dev/null, the uutils
│                       │      │                   implementation also hides failures on regular files and
│                       │      │                   directories caused by full disks or read-only file systems.
│                       │      │                   This can lead to silent data corruption in backup or
│                       │      │                   migration scripts, as the utility may report a successful
│                       │      │                   operation even when the destination file contains old or
│                       │      │                   garbage data. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-252 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/9745 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35344 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35344 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.49Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:09:48.593Z 
│                       ├ [49] ╭ VulnerabilityID : CVE-2026-35345 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4bca2fcc3001e9b3045d72cd986bc3bcd949287a2affb54b2e39b
│                       │      │                   af808acd59f 
│                       │      ├ Title           : A vulnerability in the tail utility of uutils coreutils
│                       │      │                   allows for the ... 
│                       │      ├ Description     : A vulnerability in the tail utility of uutils coreutils
│                       │      │                   allows for the exfiltration of sensitive file contents when
│                       │      │                   using the --follow=name option. Unlike GNU tail, the uutils
│                       │      │                   implementation continues to monitor a path after it has been
│                       │      │                    replaced by a symbolic link, subsequently outputting the
│                       │      │                   contents of the link's target. In environments where a
│                       │      │                   privileged user (e.g., root) monitors a log directory, a
│                       │      │                   local attacker with write access to that directory can
│                       │      │                   replace a log file with a symlink to a sensitive system file
│                       │      │                    (such as /etc/shadow), causing tail to disclose the
│                       │      │                   contents of the sensitive file. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ╰ [1]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:L/A:N 
│                       │      │                         ╰ V3Score : 5.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10328 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35345 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35345 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.627Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:04:25.093Z 
│                       ├ [50] ╭ VulnerabilityID : CVE-2026-35346 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35346 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:20b892fe2e294e873012e82f6edc77d2259f450f7329cdfbc8f8f
│                       │      │                   99e9e47f03e 
│                       │      ├ Title           : The comm utility in uutils coreutils silently corrupts data
│                       │      │                   by perform ... 
│                       │      ├ Description     : The comm utility in uutils coreutils silently corrupts data
│                       │      │                   by performing lossy UTF-8 conversion on all output lines.
│                       │      │                   The implementation uses String::from_utf8_lossy(), which
│                       │      │                   replaces invalid UTF-8 byte sequences with the Unicode
│                       │      │                   replacement character (U+FFFD). This behavior differs from
│                       │      │                   GNU comm, which processes raw bytes and preserves the
│                       │      │                   original input. This results in corrupted output when the
│                       │      │                   utility is used to compare binary files or files using
│                       │      │                   non-UTF-8 legacy encodings. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-176 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/b9372e509ea
│                       │      │                  │      9b278fe13763237067a261bb8c946 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/issues/10192 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/pull/10206 
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35346 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35346 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.76Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:28:38.493Z 
│                       ├ [51] ╭ VulnerabilityID : CVE-2026-35347 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35347 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fb94290cf99722544b0c220c6e346f86afdd76f12b21c49fb86f1
│                       │      │                   e520212bee7 
│                       │      ├ Title           : The comm utility in uutils coreutils incorrectly consumes
│                       │      │                   data from no ... 
│                       │      ├ Description     : The comm utility in uutils coreutils incorrectly consumes
│                       │      │                   data from non-regular file inputs before performing
│                       │      │                   comparison operations. The are_files_identical function
│                       │      │                   opens and reads from both input paths to compare content
│                       │      │                   without first verifying if the paths refer to regular files.
│                       │      │                    If an input path is a FIFO or a pipe, this pre-read
│                       │      │                   operation drains the stream, leading to silent data loss
│                       │      │                   before the actual comparison logic is executed.
│                       │      │                   Additionally, the utility may hang indefinitely if it
│                       │      │                   attempts to pre-read from infinite streams like /dev/zero.[
│                       │      │                   m 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-20 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:L 
│                       │      │                         ╰ V3Score : 4.4 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/75f45e87e52
│                       │      │                  │      ed95840494963ab9a28651165d56e 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/9545 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35347 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35347 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.903Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:28:23.273Z 
│                       ├ [52] ╭ VulnerabilityID : CVE-2026-35348 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6b8711e16af3476c4bef5b128c3d75d25a1f3d2d787979eb570d8
│                       │      │                   843c14702af 
│                       │      ├ Title           : The sort utility in uutils coreutils is vulnerable to a
│                       │      │                   process panic  ... 
│                       │      ├ Description     : The sort utility in uutils coreutils is vulnerable to a
│                       │      │                   process panic when using the --files0-from option with
│                       │      │                   inputs containing non-UTF-8 filenames. The implementation
│                       │      │                   enforces UTF-8 encoding and utilizes expect(), causing an
│                       │      │                   immediate crash when encountering valid but non-UTF-8 paths.
│                       │      │                    This diverges from GNU sort, which treats filenames as raw
│                       │      │                   bytes. A local attacker can exploit this to crash the
│                       │      │                   utility and disrupt automated pipelines. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-248 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:H 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/9696 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35348 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35348 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.04Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T18:57:20.927Z 
│                       ├ [53] ╭ VulnerabilityID : CVE-2026-35349 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35349 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:579079f64660612cd02e827a57839d6360a913b9db4a59c35907b
│                       │      │                   4ea7a3242b0 
│                       │      ├ Title           : A vulnerability in the rm utility of uutils coreutils allows
│                       │      │                    a bypass  ... 
│                       │      ├ Description     : A vulnerability in the rm utility of uutils coreutils allows
│                       │      │                    a bypass of the --preserve-root protection. The
│                       │      │                   implementation uses a path-string check rather than
│                       │      │                   comparing device and inode numbers to identify the root
│                       │      │                   directory. An attacker or accidental user can bypass this
│                       │      │                   safeguard by using a symbolic link that resolves to the root
│                       │      │                    directory (e.g., /tmp/rootlink -> /), potentially leading
│                       │      │                   to the unintended recursive deletion of the entire root
│                       │      │                   filesystem. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-59 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ├ nvd   : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                  │      ╰ V3Score : 6.7 
│                       │      │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 7.7 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/5e5968cdbc6
│                       │      │                  │      618acd6c2402a8a98b503f278835e 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/9706 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35349 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35349 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.19Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:28:17.903Z 
│                       ├ [54] ╭ VulnerabilityID : CVE-2026-35350 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4fe82f7ef0dc9159a7df5486323a4b84082ee783c1957367c3c7f
│                       │      │                   2960645b163 
│                       │      ├ Title           : The cp utility in uutils coreutils fails to properly handle
│                       │      │                   setuid and ... 
│                       │      ├ Description     : The cp utility in uutils coreutils fails to properly handle
│                       │      │                   setuid and setgid bits when ownership preservation fails.
│                       │      │                   When copying with the -p (preserve) flag, the utility
│                       │      │                   applies the source mode bits even if the chown operation is
│                       │      │                   unsuccessful. This can result in a user-owned copy retaining
│                       │      │                    original privileged bits, creating unexpected privileged
│                       │      │                   executables that violate local security policies. This
│                       │      │                   differs from GNU cp, which clears these bits when ownership
│                       │      │                   cannot be preserved. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-281 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:H/A:L 
│                       │      │                         ╰ V3Score : 6.6 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/9750 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35350 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35350 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.327Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:04:01.207Z 
│                       ├ [55] ╭ VulnerabilityID : CVE-2026-35351 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b80c485717c2bb034d476a2193579a0b673ba95ac2700b965b316
│                       │      │                   2a470a0b38e 
│                       │      ├ Title           : The mv utility in uutils coreutils fails to preserve file
│                       │      │                   ownership du ... 
│                       │      ├ Description     : The mv utility in uutils coreutils fails to preserve file
│                       │      │                   ownership during moves across different filesystem
│                       │      │                   boundaries. The utility falls back to a copy-and-delete
│                       │      │                   routine that creates the destination file using the caller's
│                       │      │                    UID/GID rather than the source's metadata. This flaw breaks
│                       │      │                    backups and migrations, causing files moved by a privileged
│                       │      │                    user (e.g., root) to become root-owned unexpectedly, which
│                       │      │                   can lead to information disclosure or restricted access for
│                       │      │                   the intended owners. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-281 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:H/UI:N/S:U/C:L/I:L/A:L 
│                       │      │                         ╰ V3Score : 4.2 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/9714 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11706 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35351 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35351 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.457Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:28:10.22Z 
│                       ├ [56] ╭ VulnerabilityID : CVE-2026-35352 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:330ba4d74774194150d01d0cb885380e5c760c25d37acc075e158
│                       │      │                   e9feb96596f 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │      │                   exists in the m ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │      │                   exists in the mkfifo utility of uutils coreutils. The
│                       │      │                   utility creates a FIFO and then performs a path-based chmod
│                       │      │                   to set permissions. A local attacker with write access to
│                       │      │                   the parent directory can swap the newly created FIFO for a
│                       │      │                   symbolic link between these two operations. This redirects
│                       │      │                   the chmod call to an arbitrary file, potentially enabling
│                       │      │                   privilege escalation if the utility is run with elevated
│                       │      │                   privileges. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H 
│                       │      │                         ╰ V3Score : 7 
│                       │      ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/04/4 
│                       │      │                  ├ [1]: http://www.openwall.com/lists/oss-security/2026/05/04/5 
│                       │      │                  ├ [2]: http://www.openwall.com/lists/oss-security/2026/05/04/6 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/issues/10020 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35352 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35352 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.597Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T18:16:28.37Z 
│                       ├ [57] ╭ VulnerabilityID : CVE-2026-35353 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35353 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3a90b9f0eacbf5cd361779c9cdffb71d74cd7d64e3f56a3b11dff
│                       │      │                   6529c600678 
│                       │      ├ Title           : The mkdir utility in uutils coreutils incorrectly applies
│                       │      │                   permissions  ... 
│                       │      ├ Description     : The mkdir utility in uutils coreutils incorrectly applies
│                       │      │                   permissions when using the -m flag by creating a directory
│                       │      │                   with umask-derived permissions (typically 0755) before
│                       │      │                   subsequently changing them to the requested mode via a
│                       │      │                   separate chmod system call. In multi-user environments, this
│                       │      │                    introduces a brief window where a directory intended to be
│                       │      │                   private is accessible to other users, potentially leading to
│                       │      │                    unauthorized data access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/037b9583bc0
│                       │      │                  │      3d814e8516df54ebcda6f681fe1f8 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10036 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35353 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35353 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.723Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:27:39.04Z 
│                       ├ [58] ╭ VulnerabilityID : CVE-2026-35354 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2570cac357b4659703456c2bd0b4c0bf8c1ba73c92ef3e6599f72
│                       │      │                   38de4b04b08 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the mv ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the mv utility of uutils coreutils during cross-device
│                       │      │                   moves. The extended attribute (xattr) preservation logic
│                       │      │                   uses multiple path-based system calls that perform fresh
│                       │      │                   path-to-inode lookups for each operation. A local attacker
│                       │      │                   with write access to the directory can exploit this race to
│                       │      │                   swap files between calls, causing the destination file to
│                       │      │                   receive an inconsistent mix of security xattrs, such as
│                       │      │                   SELinux labels or file capabilities. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:N 
│                       │      │                         ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10014 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35354 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35354 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.867Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:04:08.917Z 
│                       ├ [59] ╭ VulnerabilityID : CVE-2026-35355 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35355 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:15f336d491492b949704d7c607091f9f6e94101a7d47eff951dc2
│                       │      │                   3934b521918 
│                       │      ├ Title           : The install utility in uutils coreutils is vulnerable to a
│                       │      │                   Time-of-Che ... 
│                       │      ├ Description     : The install utility in uutils coreutils is vulnerable to a
│                       │      │                   Time-of-Check to Time-of-Use (TOCTOU) race condition during
│                       │      │                   file installation. The implementation unlinks an existing
│                       │      │                   destination file and then recreates it using a path-based
│                       │      │                   operation without the O_EXCL flag. A local attacker can
│                       │      │                   exploit the window between the unlink and the subsequent
│                       │      │                   creation to swap the path with a symbolic link, allowing
│                       │      │                   them to redirect privileged writes to overwrite arbitrary
│                       │      │                   system files. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/b5bbabc18a1
│                       │      │                  │      121908848d836f869a4e98eb63886 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10067 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35355 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35355 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.993Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:27:34.007Z 
│                       ├ [60] ╭ VulnerabilityID : CVE-2026-35356 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35356 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:94fd33f532b55d6c9d8a3c9add869fa441a2cf6fd746e5fce0202
│                       │      │                   93c29fc68a4 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the in ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the install utility of uutils coreutils when using the
│                       │      │                   -D flag. The command creates parent directories and
│                       │      │                   subsequently performs a second path resolution to create the
│                       │      │                    target file, neither of which is anchored to a directory
│                       │      │                   file descriptor. An attacker with concurrent write access
│                       │      │                   can replace a path component with a symbolic link between
│                       │      │                   these operations, redirecting the privileged write to an
│                       │      │                   arbitrary file system location. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/0c41299975f
│                       │      │                  │      3c1e21cf5ca968d42cad55ceb42a1 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10140 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35356 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35356 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.13Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:27:28.787Z 
│                       ├ [61] ╭ VulnerabilityID : CVE-2026-35357 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7d78fb555cdf93a4baa1688be1be271f7dc4115ce313b67c88967
│                       │      │                   fe1dacc1525 
│                       │      ├ Title           : The cp utility in uutils coreutils is vulnerable to an
│                       │      │                   information dis ... 
│                       │      ├ Description     : The cp utility in uutils coreutils is vulnerable to an
│                       │      │                   information disclosure race condition. Destination files are
│                       │      │                    initially created with umask-derived permissions (e.g.,
│                       │      │                   0644) before being restricted to their final mode (e.g.,
│                       │      │                   0600) later in the process. A local attacker can race to
│                       │      │                   open the file during this window; once obtained, the file
│                       │      │                   descriptor remains valid and readable even after the
│                       │      │                   permissions are tightened, exposing sensitive or private
│                       │      │                   file contents. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N/A:N 
│                       │      │                         ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10011 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35357 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35357 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.267Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:02:53.557Z 
│                       ├ [62] ╭ VulnerabilityID : CVE-2026-35358 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35358 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:59599ee8d6e38e42ff1f2a260e12343ff2a4bdbec01ab54ac19ea
│                       │      │                   e976c76c0ba 
│                       │      ├ Title           : The cp utility in uutils coreutils, when performing
│                       │      │                   recursive copies ( ... 
│                       │      ├ Description     : The cp utility in uutils coreutils, when performing
│                       │      │                   recursive copies (-R), incorrectly treats character and
│                       │      │                   block device nodes as stream sources rather than preserving
│                       │      │                   them. Because the implementation reads bytes into regular
│                       │      │                   files at the destination instead of using mknod, device
│                       │      │                   semantics are destroyed (e.g., /dev/null becomes a regular
│                       │      │                   file). This behavior can lead to runtime denial of service
│                       │      │                   through disk exhaustion or process hangs when reading from
│                       │      │                   unbounded device nodes. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-706 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:L 
│                       │      │                  │      ╰ V3Score : 4.4 
│                       │      │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:H 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/e6a3bb596f1
│                       │      │                  │      49628ba973eec3d099f3bb69f2464 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/issues/9746 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/pull/11163 
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35358 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35358 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.393Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T19:03:00.59Z 
│                       ├ [63] ╭ VulnerabilityID : CVE-2026-35359 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b6ceb6fef906ca9cb4acc15cb418c2b48f6d0654e0915e58c6e5e
│                       │      │                   c58d5917487 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability in the
│                       │      │                    cp utilit ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability in the
│                       │      │                    cp utility of uutils coreutils allows an attacker to bypass
│                       │      │                    no-dereference intent. The utility checks if a source path
│                       │      │                   is a symbolic link using path-based metadata but
│                       │      │                   subsequently opens it without the O_NOFOLLOW flag. An
│                       │      │                   attacker with concurrent write access can swap a regular
│                       │      │                   file for a symbolic link during this window, causing a
│                       │      │                   privileged cp process to copy the contents of arbitrary
│                       │      │                   sensitive files into a destination controlled by the
│                       │      │                   attacker. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ╰ [1]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N/A:N 
│                       │      │                         ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10017 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35359 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35359 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.537Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:02:25.72Z 
│                       ├ [64] ╭ VulnerabilityID : CVE-2026-35360 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d68b79c6004662210e585622643566e8c5b7a96db9bfd9c6d693c
│                       │      │                   69433e47535 
│                       │      ├ Title           : The touch utility in uutils coreutils is vulnerable to a
│                       │      │                   Time-of-Check ... 
│                       │      ├ Description     : The touch utility in uutils coreutils is vulnerable to a
│                       │      │                   Time-of-Check to Time-of-Use (TOCTOU) race condition during
│                       │      │                   file creation. When the utility identifies a missing path,
│                       │      │                   it later attempts creation using File::create(), which
│                       │      │                   internally uses O_TRUNC. An attacker can exploit this window
│                       │      │                    to create a file or swap a symlink at the target path,
│                       │      │                   causing touch to truncate an existing file and leading to
│                       │      │                   permanent data loss. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10019 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35360 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35360 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.673Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:02:11.56Z 
│                       ├ [65] ╭ VulnerabilityID : CVE-2026-35361 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35361 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:604bc6fc420e18f18e3389727b11e5a892e0dbb562d1db414c306
│                       │      │                   2b064072ba8 
│                       │      ├ Title           : The mknod utility in uutils coreutils fails to handle
│                       │      │                   security labels  ... 
│                       │      ├ Description     : The mknod utility in uutils coreutils fails to handle
│                       │      │                   security labels atomically by creating device nodes before
│                       │      │                   setting the SELinux context. If labeling fails, the utility
│                       │      │                   attempts cleanup using std::fs::remove_dir, which cannot
│                       │      │                   remove device nodes or FIFOs. This leaves mislabeled nodes
│                       │      │                   behind with incorrect default contexts, potentially allowing
│                       │      │                    unauthorized access to device nodes that should have been
│                       │      │                   restricted by mandatory access controls. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-281 
│                       │      │                  ╰ [1]: CWE-459 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:H/UI:N/S:U/C:L/I:L/A:N 
│                       │      │                  │      ╰ V3Score : 3.4 
│                       │      │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N 
│                       │      │                         ╰ V3Score : 4.4 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/42b2ad83cdc
│                       │      │                  │      f6e959ecb378c5040c60d9c64becf 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10582 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35361 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35361 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.827Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:27:20.527Z 
│                       ├ [66] ╭ VulnerabilityID : CVE-2026-35362 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35362 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2730e52da9a6f5272c68b6d982330956bdd1d11336f0634fb0c0f
│                       │      │                   d8eaff2877a 
│                       │      ├ Title           : The safe_traversal module in uutils coreutils, which
│                       │      │                   provides protecti ... 
│                       │      ├ Description     : The safe_traversal module in uutils coreutils, which
│                       │      │                   provides protection against Time-of-Check to Time-of-Use
│                       │      │                   (TOCTOU) symlink races using file-descriptor-relative
│                       │      │                   syscalls, is incorrectly limited to Linux targets. On other
│                       │      │                   Unix-like systems such as macOS and FreeBSD, the utility
│                       │      │                   fails to utilize these protections, leaving directory
│                       │      │                   traversal operations vulnerable to symlink race
│                       │      │                   conditions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.6 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/30239e69a32
│                       │      │                  │      8e76d2377f2a0bc02fbde61c34280 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/9792 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35362 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35362 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.96Z 
│                       │      ╰ LastModifiedDate: 2026-04-27T12:26:40.533Z 
│                       ├ [67] ╭ VulnerabilityID : CVE-2026-35363 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:57b574b680d0c672dce788149ab3526322dfa23d3ccd571b2bcc7
│                       │      │                   3d76fe57b2b 
│                       │      ├ Title           : A vulnerability in the rm utility of uutils coreutils allows
│                       │      │                    the bypas ... 
│                       │      ├ Description     : A vulnerability in the rm utility of uutils coreutils allows
│                       │      │                    the bypass of safeguard mechanisms intended to protect the
│                       │      │                   current directory. While the utility correctly refuses to
│                       │      │                   delete . or .., it fails to recognize equivalent paths with
│                       │      │                   trailing slashes, such as ./ or .///. An accidental or
│                       │      │                   malicious execution of rm -rf ./ results in the silent
│                       │      │                   recursive deletion of all contents within the current
│                       │      │                   directory. The command further obscures the data loss by
│                       │      │                   reporting a misleading 'Invalid input' error, which may
│                       │      │                   cause users to miss the critical window for data recovery.[
│                       │      │                   m 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-22 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:H/A:L 
│                       │      │                         ╰ V3Score : 5.6 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/9749 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35363 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35363 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.12Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:02:00.463Z 
│                       ├ [68] ╭ VulnerabilityID : CVE-2026-35364 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8f583533e85fbc7921617a68b175f141513c51e07c13ea6be4aec
│                       │      │                   ac6afe480ce 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │      │                   exists in the m ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) race condition
│                       │      │                   exists in the mv utility of uutils coreutils during
│                       │      │                   cross-device operations. The utility removes the destination
│                       │      │                    path before recreating it through a copy operation. A local
│                       │      │                    attacker with write access to the destination directory can
│                       │      │                    exploit this window to replace the destination with a
│                       │      │                   symbolic link. The subsequent privileged move operation will
│                       │      │                    follow the symlink, allowing the attacker to redirect the
│                       │      │                   write and overwrite an arbitrary target file with contents
│                       │      │                   from the source. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10015 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35364 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35364 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.737Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:19:11.777Z 
│                       ├ [69] ╭ VulnerabilityID : CVE-2026-35365 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35365 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:75c36893d30bad0a0f2270dc15f1f0968886a15f65c6a5e7810ed
│                       │      │                   d824f12852c 
│                       │      ├ Title           : The mv utility in uutils coreutils improperly handles
│                       │      │                   directory trees  ... 
│                       │      ├ Description     : The mv utility in uutils coreutils improperly handles
│                       │      │                   directory trees containing symbolic links during moves
│                       │      │                   across filesystem boundaries. Instead of preserving
│                       │      │                   symlinks, the implementation expands them, copying the
│                       │      │                   linked targets as real files or directories at the
│                       │      │                   destination. This can lead to resource exhaustion (disk
│                       │      │                   space or time) if symlinks point to large external
│                       │      │                   directories, unexpected duplication of sensitive data into
│                       │      │                   unintended locations, or infinite recursion and repeated
│                       │      │                   copying in the presence of symlink loops. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-59 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:H/A:L 
│                       │      │                         ╰ V3Score : 6.6 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/9654e4abaf2
│                       │      │                  │      4449ef2279e9a16963edb5c8b8fef 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10546 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.7.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35365 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35365 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.9Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T18:53:45.707Z 
│                       ├ [70] ╭ VulnerabilityID : CVE-2026-35366 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35366 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9fe12dcc8c7f2f098232e3aca3be0140ed3b6b9ae10b3938aaad1
│                       │      │                   9f57eb4ebce 
│                       │      ├ Title           : The printenv utility in uutils coreutils fails to display
│                       │      │                   environment  ... 
│                       │      ├ Description     : The printenv utility in uutils coreutils fails to display
│                       │      │                   environment variables containing invalid UTF-8 byte
│                       │      │                   sequences. While POSIX permits arbitrary bytes in
│                       │      │                   environment strings, the uutils implementation silently
│                       │      │                   skips these entries rather than printing the raw bytes. This
│                       │      │                    vulnerability allows malicious environment variables (e.g.,
│                       │      │                    adversarial LD_PRELOAD values) to evade inspection by
│                       │      │                   administrators or security auditing tools, potentially
│                       │      │                   allowing library injection or other environment-based
│                       │      │                   attacks to go undetected. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-754 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N 
│                       │      │                         ╰ V3Score : 4.4 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/0bfbbc00c78
│                       │      │                  │      95c0fb6ea94987b4aab99e3d7ee52 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/issues/9701 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/pull/9728 
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35366 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35366 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.167Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T18:52:42.39Z 
│                       ├ [71] ╭ VulnerabilityID : CVE-2026-35367 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1c43e4d0c21f64c53fa1cda44c1540610c9dcffcab208f426acfd
│                       │      │                   379859183c5 
│                       │      ├ Title           : The nohup utility in uutils coreutils creates its default
│                       │      │                   output file, ... 
│                       │      ├ Description     : The nohup utility in uutils coreutils creates its default
│                       │      │                   output file, nohup.out, without specifying explicit
│                       │      │                   restricted permissions. This causes the file to inherit
│                       │      │                   umask-based permissions, typically resulting in a
│                       │      │                   world-readable file (0644). In multi-user environments, this
│                       │      │                    allows any user on the system to read the captured
│                       │      │                   stdout/stderr output of a command, potentially exposing
│                       │      │                   sensitive information. This behavior diverges from GNU
│                       │      │                   coreutils, which creates nohup.out with owner-only (0600)
│                       │      │                   permissions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-732 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10021 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35367 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35367 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.423Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:19:05.067Z 
│                       ├ [72] ╭ VulnerabilityID : CVE-2026-35368 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9a102305920a52f921ce6f8bc7f2251fb75bc3f1089ebc0a129b6
│                       │      │                   327d80bba89 
│                       │      ├ Title           : A vulnerability exists in the chroot utility of uutils
│                       │      │                   coreutils when  ... 
│                       │      ├ Description     : A vulnerability exists in the chroot utility of uutils
│                       │      │                   coreutils when using the --userspec option. The utility
│                       │      │                   resolves the user specification via getpwnam() after
│                       │      │                   entering the chroot but before dropping root privileges. On
│                       │      │                   glibc-based systems, this can trigger the Name Service
│                       │      │                   Switch (NSS) to load shared libraries (e.g., libnss_*.so.2)
│                       │      │                   from the new root directory. If the NEWROOT is writable by
│                       │      │                   an attacker, they can inject a malicious NSS module to
│                       │      │                   execute arbitrary code as root, facilitating a full
│                       │      │                   container escape or privilege escalation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-426 
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:C/C:H/I:H/A:H 
│                       │      │                         ╰ V3Score : 7.9 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10327 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35368 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35368 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.56Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:18:55.67Z 
│                       ├ [73] ╭ VulnerabilityID : CVE-2026-35369 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35369 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2963ab565e65535c46f88ade8a78c1faa191d570f99680fc13c08
│                       │      │                   3e7bd79c56b 
│                       │      ├ Title           : An argument parsing error in the kill utility of uutils
│                       │      │                   coreutils inco ... 
│                       │      ├ Description     : An argument parsing error in the kill utility of uutils
│                       │      │                   coreutils incorrectly interprets kill -1 as a request to
│                       │      │                   send the default signal (SIGTERM) to PID -1. Sending a
│                       │      │                   signal to PID -1 causes the kernel to terminate all
│                       │      │                   processes visible to the caller, potentially leading to a
│                       │      │                   system crash or massive process termination. This differs
│                       │      │                   from GNU coreutils, which correctly recognizes -1 as a
│                       │      │                   signal number in this context and would instead report a
│                       │      │                   missing PID argument. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-20 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:H 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/2d3aebce671
│                       │      │                  │      2841bc08b9b94e9078be50a25fc10 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/9700 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35369 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35369 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.687Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T18:50:23.537Z 
│                       ├ [74] ╭ VulnerabilityID : CVE-2026-35370 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3fd373b1f9d845401eb78a156a4f4475a5241e25a7dcd59e36458
│                       │      │                   44a552d02a7 
│                       │      ├ Title           : The id utility in uutils coreutils miscalculates the groups=
│                       │      │                    section o ... 
│                       │      ├ Description     : The id utility in uutils coreutils miscalculates the groups=
│                       │      │                    section of its output. The implementation uses a user's
│                       │      │                   real GID instead of their effective GID to compute the group
│                       │      │                    list, leading to potentially divergent output compared to
│                       │      │                   GNU coreutils. Because many scripts and automated processes
│                       │      │                   rely on the output of id to make security-critical
│                       │      │                   access-control or permission decisions, this discrepancy can
│                       │      │                    lead to unauthorized access or security
│                       │      │                   misconfigurations. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-863 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N 
│                       │      │                         ╰ V3Score : 4.4 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10006 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35370 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35370 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.833Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:02:44.33Z 
│                       ├ [75] ╭ VulnerabilityID : CVE-2026-35371 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bb59b22662505eb12561cda653760a7abe1d02a93e4f3be80d508
│                       │      │                   5ee14380665 
│                       │      ├ Title           : The id utility in uutils coreutils exhibits incorrect
│                       │      │                   behavior in its  ... 
│                       │      ├ Description     : The id utility in uutils coreutils exhibits incorrect
│                       │      │                   behavior in its "pretty print" output when the real UID and
│                       │      │                   effective UID differ. The implementation incorrectly uses
│                       │      │                   the effective GID instead of the effective UID when
│                       │      │                   performing a name lookup for the effective user. This
│                       │      │                   results in misleading diagnostic output that can cause
│                       │      │                   automated scripts or system administrators to make incorrect
│                       │      │                    decisions regarding file permissions or access control. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-451 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/issues/10006 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35371 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35371 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.987Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:02:06.183Z 
│                       ├ [76] ╭ VulnerabilityID : CVE-2026-35372 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35372 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:489dfbceec5098a3e7b8d872a15bc382e8e9aa3b008ac060bf521
│                       │      │                   90df97bfbdc 
│                       │      ├ Title           : A logic error in the ln utility of uutils coreutils allows
│                       │      │                   the utility ... 
│                       │      ├ Description     : A logic error in the ln utility of uutils coreutils allows
│                       │      │                   the utility to dereference a symbolic link target even when
│                       │      │                   the --no-dereference (or -n) flag is explicitly provided.
│                       │      │                   The implementation previously only honored the
│                       │      │                   "no-dereference" intent if the --force (overwrite) mode was
│                       │      │                   also enabled. This flaw causes ln to follow a symbolic link
│                       │      │                   that points to a directory and create new links inside that
│                       │      │                   target directory instead of treating the symbolic link
│                       │      │                   itself as the destination. In environments where a
│                       │      │                   privileged user or system script uses ln -n to update a
│                       │      │                   symlink, a local attacker could manipulate existing symbolic
│                       │      │                    links to redirect file creation into sensitive directories,
│                       │      │                    potentially leading to unauthorized file creation or system
│                       │      │                    misconfiguration. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-61 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:H/A:N 
│                       │      │                         ╰ V3Score : 5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/394c4b17f2f
│                       │      │                  │      382b4be9f54389bcb79028de02f39 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11253 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35372 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35372 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:41.85Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T18:49:46.51Z 
│                       ├ [77] ╭ VulnerabilityID : CVE-2026-35373 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5e4a2e3a4f1093313602737d6c6baadec1677734c6745459f724d
│                       │      │                   61754b2f8ec 
│                       │      ├ Title           : A logic error in the ln utility of uutils coreutils causes
│                       │      │                   the program ... 
│                       │      ├ Description     : A logic error in the ln utility of uutils coreutils causes
│                       │      │                   the program to reject source paths containing non-UTF-8
│                       │      │                   filename bytes when using target-directory forms (e.g., ln
│                       │      │                   SOURCE... DIRECTORY). While GNU ln treats filenames as raw
│                       │      │                   bytes and creates the links correctly, the uutils
│                       │      │                   implementation enforces UTF-8 encoding, resulting in a
│                       │      │                   failure to stat the file and a non-zero exit code. In
│                       │      │                   environments where automated scripts or system tasks process
│                       │      │                    valid but non-UTF-8 filenames common on Unix filesystems,
│                       │      │                   this divergence causes the utility to fail, leading to a
│                       │      │                   local denial of service for those specific operations. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-176 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:L 
│                       │      │                  │      ╰ V3Score : 3.3 
│                       │      │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:H 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/pull/11403 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35373 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35373 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:41.997Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T20:01:25.93Z 
│                       ├ [78] ╭ VulnerabilityID : CVE-2026-35374 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7f601d77b9354ac9659201e62acb84c6030fdd1c716ef9630583b
│                       │      │                   a7f021100ba 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the sp ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the split utility of uutils coreutils. The program
│                       │      │                   attempts to prevent data loss by checking for identity
│                       │      │                   between input and output files using their file paths before
│                       │      │                    initiating the split operation. However, the utility
│                       │      │                   subsequently opens the output file with truncation after
│                       │      │                   this path-based validation is complete. A local attacker
│                       │      │                   with write access to the directory can exploit this race
│                       │      │                   window by manipulating mutable path components (e.g.,
│                       │      │                   swapping a path with a symbolic link). This can cause split
│                       │      │                   to truncate and write to an unintended target file,
│                       │      │                   potentially including the input file itself or other
│                       │      │                   sensitive files accessible to the process, leading to
│                       │      │                   permanent data loss. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/pull/11401 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35374 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35374 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.127Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T19:22:14.457Z 
│                       ├ [79] ╭ VulnerabilityID : CVE-2026-35375 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35375 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5dbb3a181f154864b92e98b1843b070b0f57eb6250a76fa381f61
│                       │      │                   423f88972ff 
│                       │      ├ Title           : A logic error in the split utility of uutils coreutils
│                       │      │                   causes the corr ... 
│                       │      ├ Description     : A logic error in the split utility of uutils coreutils
│                       │      │                   causes the corruption of output filenames when provided with
│                       │      │                    non-UTF-8 prefix or suffix inputs. The implementation
│                       │      │                   utilizes to_string_lossy() when constructing chunk
│                       │      │                   filenames, which automatically rewrites invalid byte
│                       │      │                   sequences into the UTF-8 replacement character (U+FFFD).
│                       │      │                   This behavior diverges from GNU split, which preserves raw
│                       │      │                   pathname bytes intact. In environments utilizing non-UTF-8
│                       │      │                   encodings, this vulnerability leads to the creation of files
│                       │      │                    with incorrect names, potentially causing filename
│                       │      │                   collisions, broken automation, or the misdirection of output
│                       │      │                    data. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-176 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/d2b9550fe82
│                       │      │                  │      1a9a10bf0cec057509211357363f1 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11397 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35375 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35375 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.293Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T19:13:37.293Z 
│                       ├ [80] ╭ VulnerabilityID : CVE-2026-35376 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35376 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:83b4169bf6a7e7b8986d7a3ffa2e437695359e3afe8c8134e46e7
│                       │      │                   cb07a365df1 
│                       │      ├ Title           : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the ch ... 
│                       │      ├ Description     : A Time-of-Check to Time-of-Use (TOCTOU) vulnerability exists
│                       │      │                    in the chcon utility of uutils coreutils during recursive
│                       │      │                   operations. The implementation resolves recursive targets
│                       │      │                   using a fresh path lookup (via fts_accpath) rather than
│                       │      │                   binding the traversal and label application to the specific
│                       │      │                   directory state encountered during traversal. Because these
│                       │      │                   operations are not anchored to file descriptors, a local
│                       │      │                   attacker with write access to a directory tree can exploit
│                       │      │                   timing-sensitive rename or symbolic link races to redirect a
│                       │      │                    privileged recursive relabeling operation to unintended
│                       │      │                   files or directories. This vulnerability breaks the
│                       │      │                   hardening expectations for SELinux administration workflows
│                       │      │                   and can lead to the unauthorized modification of security
│                       │      │                   labels on sensitive system objects. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-367 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L/A:L 
│                       │      │                  │      ╰ V3Score : 4.5 
│                       │      │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:H/A:L 
│                       │      │                         ╰ V3Score : 5.8 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/pull/11402 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35376 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35376 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.43Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T19:06:31.93Z 
│                       ├ [81] ╭ VulnerabilityID : CVE-2026-35377 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8c211c61f704fb8101680bffea481f9abd928b5fff2cf9f216436
│                       │      │                   289293ef2a1 
│                       │      ├ Title           : A logic error in the env utility of uutils coreutils causes
│                       │      │                   a failure  ... 
│                       │      ├ Description     : A logic error in the env utility of uutils coreutils causes
│                       │      │                   a failure to correctly parse command-line arguments when
│                       │      │                   utilizing the -S (split-string) option. In GNU env,
│                       │      │                   backslashes within single quotes are treated literally (with
│                       │      │                    the exceptions of \\ and \'). However, the uutils
│                       │      │                   implementation incorrectly attempts to validate these
│                       │      │                   sequences, resulting in an "invalid sequence" error and an
│                       │      │                   immediate process termination with an exit status of 125
│                       │      │                   when encountering valid but unrecognized sequences like \a
│                       │      │                   or \x. This divergence from GNU behavior breaks
│                       │      │                   compatibility for automated scripts and administrative
│                       │      │                   workflows that rely on standard split-string semantics,
│                       │      │                   leading to a local denial of service for those operations.[
│                       │      │                   m 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-20 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:L 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/pull/11512 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-35377 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-35377 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.577Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:06:46.293Z 
│                       ├ [82] ╭ VulnerabilityID : CVE-2026-35378 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35378 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5c2860862bee96a18c9c53e34d94464dd15995cd0f48adf68154f
│                       │      │                   a1229e89b80 
│                       │      ├ Title           : A logic error in the expr utility of uutils coreutils causes
│                       │      │                    the progr ... 
│                       │      ├ Description     : A logic error in the expr utility of uutils coreutils causes
│                       │      │                    the program to evaluate parenthesized subexpressions during
│                       │      │                    the parsing phase rather than at the execution phase. This
│                       │      │                   implementation flaw prevents the utility from performing
│                       │      │                   proper short-circuiting for logical OR (|) and AND (&)
│                       │      │                   operations. As a result, arithmetic errors (such as division
│                       │      │                    by zero) occurring within "dead" branches, branches that
│                       │      │                   should be ignored due to short-circuiting, are raised as
│                       │      │                   fatal errors. This divergence from GNU expr behavior can
│                       │      │                   cause guarded expressions within shell scripts to fail with
│                       │      │                   hard errors instead of returning expected boolean results,
│                       │      │                   leading to premature script termination and breaking
│                       │      │                   GNU-compatible shell control flow. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-768 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:L 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/76b2f7877f5
│                       │      │                  │      58f3bfa78e3d4f49f022460f509b7 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11395 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35378 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35378 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.73Z 
│                       │      ╰ LastModifiedDate: 2026-05-04T18:48:36.02Z 
│                       ├ [83] ╭ VulnerabilityID : CVE-2026-35379 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35379 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:357845c45e48e767c96e25232f3481a98210d81d143c0c4460fb8
│                       │      │                   b97446a2488 
│                       │      ├ Title           : A logic error in the tr utility of uutils coreutils causes
│                       │      │                   the program ... 
│                       │      ├ Description     : A logic error in the tr utility of uutils coreutils causes
│                       │      │                   the program to incorrectly define the [:graph:] and
│                       │      │                   [:print:] character classes. The implementation mistakenly
│                       │      │                   includes the ASCII space character (0x20) in the [:graph:]
│                       │      │                   class and excludes it from the [:print:] class, effectively
│                       │      │                   reversing the standard behavior established by POSIX and GNU
│                       │      │                    coreutils. This vulnerability leads to unintended data
│                       │      │                   modification or loss when the utility is used in automated
│                       │      │                   scripts or data-cleaning pipelines that rely on standard
│                       │      │                   character class semantics. For example, a command executed
│                       │      │                   to delete all graphical characters while intending to
│                       │      │                   preserve whitespace will incorrectly delete all ASCII
│                       │      │                   spaces, potentially resulting in data corruption or logic
│                       │      │                   failures in downstream processing. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-684 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/358063f3367
│                       │      │                  │      cb23a1e5db314cfdbfeb607749b3d 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11405 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35379 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35379 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.887Z 
│                       │      ╰ LastModifiedDate: 2026-04-29T15:59:08.45Z 
│                       ├ [84] ╭ VulnerabilityID : CVE-2026-35380 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35380 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6cbda5d145f6e8dbcbe21658f75c0525ec5b6d3c3191957b01d1e
│                       │      │                   ba445bb04df 
│                       │      ├ Title           : A logic error in the cut utility of uutils coreutils causes
│                       │      │                   the progra ... 
│                       │      ├ Description     : A logic error in the cut utility of uutils coreutils causes
│                       │      │                   the program to incorrectly interpret the literal two-byte
│                       │      │                   string '' (two single quotes) as an empty delimiter. The
│                       │      │                   implementation mistakenly maps this string to the NUL
│                       │      │                   character for both the -d (delimiter) and --output-delimiter
│                       │      │                    options. This vulnerability can lead to silent data
│                       │      │                   corruption or logic errors in automated scripts and data
│                       │      │                   pipelines that process strings containing these characters,
│                       │      │                   as the utility may unintentionally split or join data on NUL
│                       │      │                    bytes rather than the intended literal characters. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-20 
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:H/A:N 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/593f5b191e8
│                       │      │                  │      b9c87e4292955999c2d0b5cbcce69 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11399 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35380 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35380 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:43.047Z 
│                       │      ╰ LastModifiedDate: 2026-04-29T15:57:19.427Z 
│                       ├ [85] ╭ VulnerabilityID : CVE-2026-35381 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35381 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:61ff95bb250630d67f56cab938f3452f36e65e4861138171e6e42
│                       │      │                   75ce94e56f2 
│                       │      ├ Title           : A logic error in the cut utility of uutils coreutils causes
│                       │      │                   the utilit ... 
│                       │      ├ Description     : A logic error in the cut utility of uutils coreutils causes
│                       │      │                   the utility to ignore the -s (only-delimited) flag when
│                       │      │                   using the -z (null-terminated) and -d '' (empty delimiter)
│                       │      │                   options together. The implementation incorrectly routes this
│                       │      │                    specific combination through a specialized
│                       │      │                   newline-delimiter code path that fails to check the record
│                       │      │                   suppression status. Consequently, uutils cut emits the
│                       │      │                   entire record plus a NUL byte instead of suppressing it.
│                       │      │                   This divergence from GNU coreutils behavior creates a data
│                       │      │                   integrity risk for automated pipelines that rely on cut -s
│                       │      │                   to filter out undelimited data. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-684 
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/commit/483f13e9183
│                       │      │                  │      0c468262aa1e010e753d6ae99c898 
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/11394 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/releases/tag/0.8.0 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35381 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35381 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:43.2Z 
│                       │      ╰ LastModifiedDate: 2026-04-24T19:19:34.493Z 
│                       ├ [86] ╭ VulnerabilityID : CVE-2025-45582 
│                       │      ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │      ├ PkgName         : tar 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : 41081f85f98b9d6a 
│                       │      ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-45582 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d45c06752beec1710e42c1a932f4922a22e9991c6e5d80b9b8bd4
│                       │      │                   91c07e2b430 
│                       │      ├ Title           : tar: Tar path traversal 
│                       │      ├ Description     : GNU Tar through 1.35 allows file overwrite via directory
│                       │      │                   traversal in crafted TAR archives, with a certain two-step
│                       │      │                   process. First, the victim must extract an archive that
│                       │      │                   contains a ../ symlink to a critical directory. Second, the
│                       │      │                   victim must extract an archive that contains a critical
│                       │      │                   file, specified via a relative pathname that begins with the
│                       │      │                    symlink name and ends with that critical file's name. Here,
│                       │      │                    the extraction follows the symlink and overwrites the
│                       │      │                   critical file. This bypasses the protection mechanism of
│                       │      │                   "Member name contains '..'" that would occur for a single
│                       │      │                   TAR archive that attempted to specify the critical file via
│                       │      │                   a ../ approach. For example, the first archive can contain
│                       │      │                   "x -> ../../../../../home/victim/.ssh" and the second
│                       │      │                   archive can contain x/authorized_keys. This can affect
│                       │      │                   server applications that automatically extract any number of
│                       │      │                    user-supplied TAR archives, and were relying on the
│                       │      │                   blocking of traversal. This can also affect software
│                       │      │                   installation processes in which "tar xf" is run more than
│                       │      │                   once (e.g., when installing a package can automatically
│                       │      │                   install two dependencies that are set up as untrusted
│                       │      │                   tarballs instead of official packages). NOTE: the official
│                       │      │                   GNU Tar manual has an otherwise-empty directory for each
│                       │      │                   "tar xf" in its Security Rules of Thumb; however,
│                       │      │                   third-party advice leads users to run "tar xf" more than
│                       │      │                   once into the same directory. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-24 
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.6 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2025/11/01/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:0067 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2025-45582 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2379592 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2379592 
│                       │      │                  ├ [5] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-45582 
│                       │      │                  ├ [6] : https://errata.almalinux.org/9/ALSA-2026-0067.html 
│                       │      │                  ├ [7] : https://errata.rockylinux.org/RLSA-2026:0067 
│                       │      │                  ├ [8] : https://github.com/i900008/vulndb/blob/main/Gnu_tar_v
│                       │      │                  │       uln.md 
│                       │      │                  ├ [9] : https://linux.oracle.com/cve/CVE-2025-45582.html 
│                       │      │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-0067.html 
│                       │      │                  ├ [11]: https://lists.gnu.org/archive/html/bug-tar/2025-08/ms
│                       │      │                  │       g00012.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2025-45582 
│                       │      │                  ├ [13]: https://www.cve.org/CVERecord?id=CVE-2025-45582 
│                       │      │                  ├ [14]: https://www.gnu.org/software/tar/ 
│                       │      │                  ├ [15]: https://www.gnu.org/software/tar/manual/html_node/Int
│                       │      │                  │       egrity.html 
│                       │      │                  ├ [16]: https://www.gnu.org/software/tar/manual/html_node/Int
│                       │      │                  │       egrity.html#Integrity 
│                       │      │                  ╰ [17]: https://www.gnu.org/software/tar/manual/html_node/Sec
│                       │      │                          urity-rules-of-thumb.html 
│                       │      ├ PublishedDate   : 2025-07-11T17:15:37.183Z 
│                       │      ╰ LastModifiedDate: 2025-11-02T01:15:32.307Z 
│                       ├ [87] ╭ VulnerabilityID : CVE-2026-5704 
│                       │      ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │      ├ PkgName         : tar 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : 41081f85f98b9d6a 
│                       │      ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5704 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:991f50d6c1454af3d5245bd7a5bb11e9e581319d947a94606ffb6
│                       │      │                   1cd6e693af5 
│                       │      ├ Title           : tar: tar: Hidden file injection via crafted archives 
│                       │      ├ Description     : A flaw was found in tar. A remote attacker could exploit
│                       │      │                   this vulnerability by crafting a malicious archive, leading
│                       │      │                   to hidden file injection with fully attacker-controlled
│                       │      │                   content. This bypasses pre-extraction inspection mechanisms,
│                       │      │                    potentially allowing an attacker to introduce malicious
│                       │      │                   files onto a system without detection. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-434 
│                       │      ├ VendorSeverity   ╭ nvd   : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:H
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:H
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 5 
│                       │      ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/04/11/10 
│                       │      │                  ├ [1]: http://www.openwall.com/lists/oss-security/2026/04/11/11 
│                       │      │                  ├ [2]: http://www.openwall.com/lists/oss-security/2026/04/12/2 
│                       │      │                  ├ [3]: https://access.redhat.com/security/cve/CVE-2026-5704 
│                       │      │                  ├ [4]: https://bugzilla.redhat.com/show_bug.cgi?id=2455360 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-5704 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5704 
│                       │      ├ PublishedDate   : 2026-04-06T16:16:42.14Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T20:08:59.92Z 
│                       ├ [88] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:af46598a2612c5037e96cb2a07acf19c833dad3cd3864dc3e2864
│                       │      │                   4c14c1db079 
│                       │      ├ Title           : util-linux: TOCTOU in the mount program when setting up loop
│                       │      │                    devices 
│                       │      ├ Description     : util-linux is a random collection of Linux utilities. Prior
│                       │      │                   to version 2.41.4, a TOCTOU (Time-of-Check-Time-of-Use)
│                       │      │                   vulnerability has been identified in the SUID binary
│                       │      │                   /usr/bin/mount from util-linux. The mount binary, when
│                       │      │                   setting up loop devices, validates the source file path with
│                       │      │                    user privileges via fork() + setuid() + realpath(), but
│                       │      │                   subsequently re-canonicalizes and opens it with root
│                       │      │                   privileges (euid=0) without verifying that the path has not
│                       │      │                   been replaced between both operations. Neither O_NOFOLLOW,
│                       │      │                   nor inode comparison, nor post-open fstat() are employed.
│                       │      │                   This allows a local unprivileged user to replace the source
│                       │      │                   file with a symlink pointing to any root-owned file or
│                       │      │                   device during the race window, causing the SUID binary to
│                       │      │                   open and mount it as root. Exploitation requires an
│                       │      │                   /etc/fstab entry with user,loop options whose path points to
│                       │      │                    a directory where the attacker has write permission, and
│                       │      │                   that /usr/bin/mount has the SUID bit set (the default
│                       │      │                   configuration on virtually all Linux distributions). The
│                       │      │                   impact is unauthorized read access to root-protected files
│                       │      │                   and block devices, including backup images, disk volumes,
│                       │      │                   and any file containing a valid filesystem. This issue has
│                       │      │                   been patched in version 2.41.4. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-59 
│                       │      │                  ├ [1]: CWE-269 
│                       │      │                  ╰ [2]: CWE-367 
│                       │      ├ VendorSeverity   ╭ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [89] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0fbfec579aab92e94903e00a0a82576f19a9b14c42e668a3ec43a
│                       │      │                   5d77b9f645a 
│                       │      ├ Title           : util-linux: util-linux: Access control bypass due to
│                       │      │                   improper hostname canonicalization 
│                       │      ├ Description     : A flaw was found in util-linux. Improper hostname
│                       │      │                   canonicalization in the `login(1)` utility, when invoked
│                       │      │                   with the `-h` option, can modify the supplied remote
│                       │      │                   hostname before setting `PAM_RHOST`. A remote attacker could
│                       │      │                    exploit this by providing a specially crafted hostname,
│                       │      │                   potentially bypassing host-based Pluggable Authentication
│                       │      │                   Modules (PAM) access control rules that rely on fully
│                       │      │                   qualified domain names. This could lead to unauthorized
│                       │      │                   access. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-289 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 5.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7180 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-3184 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2442570 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-3184 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-3184 
│                       │      ├ PublishedDate   : 2026-04-03T19:17:23.377Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [90] ╭ VulnerabilityID : CVE-2026-43961 
│                       │      ├ PkgID           : vim@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.5?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : 2541eefb3c0876e6 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cb99bfdc31a2b06394245f2559396dcf03c0e0505cd02b465d410
│                       │      │                   618f43cba9f 
│                       │      ├ Description     : [Unknown description] 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-66
│                       │                         │      hr-7p6x-x5j3 
│                       │                         ├ [1]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                         ╰ [2]: https://www.openwall.com/lists/oss-security/2026/05/14/7 
│                       ├ [91] ╭ VulnerabilityID : CVE-2026-46483 
│                       │      ├ PkgID           : vim@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.5?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : 2541eefb3c0876e6 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:66ce47ee46cc16f3e7920f1d6e71a657293a7ec0d3eac71f698fb
│                       │      │                   8d0b2de1029 
│                       │      ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0479, a command injection vulnerability exists in
│                       │      │                   tar#Vimuntar() in
│                       │      │                   runtime/autoload/tar.vim when decompressing .tgz archives on
│                       │      │                    Unix-like systems. The function builds :!gunzip and :!gzip
│                       │      │                   -d commands using shellescape(tartail) without the {special}
│                       │      │                    flag, allowing a crafted archive filename to trigger Vim
│                       │      │                   cmdline-special expansion and execute shell commands in the
│                       │      │                   user's context. This vulnerability is fixed in 9.2.0479. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-78 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ nvd   : 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │      │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 
│                       │      │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │      │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │      │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2f
│                       │      │                  │      pv-9ff7-xg5w 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │      ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │      ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ├ [92] ╭ VulnerabilityID : CVE-2026-43961 
│                       │      ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.5?arch=al
│                       │      │                  │       l&distro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : 8a15c1b947cca3b8 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6ee55ad8bc0795ae1918096b2f36bbb833659174388c04360086f
│                       │      │                   0bc8c57987d 
│                       │      ├ Description     : [Unknown description] 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-66
│                       │                         │      hr-7p6x-x5j3 
│                       │                         ├ [1]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                         ╰ [2]: https://www.openwall.com/lists/oss-security/2026/05/14/7 
│                       ├ [93] ╭ VulnerabilityID : CVE-2026-46483 
│                       │      ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.5?arch=al
│                       │      │                  │       l&distro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : 8a15c1b947cca3b8 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:aeb844d33bffca9653faedf1a76406343028a4bf748b9aa7f2e24
│                       │      │                   79afaef747a 
│                       │      ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0479, a command injection vulnerability exists in
│                       │      │                   tar#Vimuntar() in
│                       │      │                   runtime/autoload/tar.vim when decompressing .tgz archives on
│                       │      │                    Unix-like systems. The function builds :!gunzip and :!gzip
│                       │      │                   -d commands using shellescape(tartail) without the {special}
│                       │      │                    flag, allowing a crafted archive filename to trigger Vim
│                       │      │                   cmdline-special expansion and execute shell commands in the
│                       │      │                   user's context. This vulnerability is fixed in 9.2.0479. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-78 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ nvd   : 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │      │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 
│                       │      │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │      │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │      │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2f
│                       │      │                  │      pv-9ff7-xg5w 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │      ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │      ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ├ [94] ╭ VulnerabilityID : CVE-2026-43961 
│                       │      ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : vim-runtime 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.5?arch=a
│                       │      │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : a4708db604f82859 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:37988f5af02fd852d8df4cf8778d423e2677fd43a0834c9d59236
│                       │      │                   b8f06ae1f59 
│                       │      ├ Description     : [Unknown description] 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-66
│                       │                         │      hr-7p6x-x5j3 
│                       │                         ├ [1]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                         ╰ [2]: https://www.openwall.com/lists/oss-security/2026/05/14/7 
│                       ├ [95] ╭ VulnerabilityID : CVE-2026-46483 
│                       │      ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : vim-runtime 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.5?arch=a
│                       │      │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : a4708db604f82859 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c05be7cbfec5549954734c40205ee01ee4017f7d731aff3c88c54
│                       │      │                   73f44bed0e5 
│                       │      ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0479, a command injection vulnerability exists in
│                       │      │                   tar#Vimuntar() in
│                       │      │                   runtime/autoload/tar.vim when decompressing .tgz archives on
│                       │      │                    Unix-like systems. The function builds :!gunzip and :!gzip
│                       │      │                   -d commands using shellescape(tartail) without the {special}
│                       │      │                    flag, allowing a crafted archive filename to trigger Vim
│                       │      │                   cmdline-special expansion and execute shell commands in the
│                       │      │                   user's context. This vulnerability is fixed in 9.2.0479. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-78 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ nvd   : 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │      │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 
│                       │      │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │      │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │      │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2f
│                       │      │                  │      pv-9ff7-xg5w 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │      ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │      ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ├ [96] ╭ VulnerabilityID : CVE-2021-31879 
│                       │      ├ PkgID           : wget@1.25.0-2ubuntu3 
│                       │      ├ PkgName         : wget 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu3?arch=amd64&distro
│                       │      │                  │       =ubuntu-25.10 
│                       │      │                  ╰ UID : 3ae34724b04a04d7 
│                       │      ├ InstalledVersion: 1.25.0-2ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c6b25b9393c3cc5dfb4a5efa07254aae8253e08e6626e353d25cc
│                       │      │                   46e11ff921c 
│                       │      ├ Title           : wget: authorization header disclosure on redirect 
│                       │      ├ Description     : GNU Wget through 1.21.1 does not omit the Authorization
│                       │      │                   header upon a redirect to a different origin, a related
│                       │      │                   issue to CVE-2018-1000007. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-601 
│                       │      ├ VendorSeverity   ╭ amazon     : 2 
│                       │      │                  ├ cbl-mariner: 2 
│                       │      │                  ├ nvd        : 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V2Vector: AV:N/AC:M/Au:N/C:P/I:P/A:N 
│                       │      │                  │        ├ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ├ V2Score : 5.8 
│                       │      │                  │        ╰ V3Score : 6.1 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2021-31879 
│                       │      │                  ├ [1]: https://mail.gnu.org/archive/html/bug-wget/2021-02/msg
│                       │      │                  │      00002.html 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2021-31879 
│                       │      │                  ├ [3]: https://savannah.gnu.org/bugs/?56909 
│                       │      │                  ├ [4]: https://security.netapp.com/advisory/ntap-20210618-0002/ 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2021-31879 
│                       │      ├ PublishedDate   : 2021-04-29T05:15:08.707Z 
│                       │      ╰ LastModifiedDate: 2024-11-21T06:06:25.02Z 
│                       ├ [97] ╭ VulnerabilityID : CVE-2026-43961 
│                       │      ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.5?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : 526950e53908bbfb 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f83fad06915a5fffa5328bb2927b59e32b841427048f69ec2e9e8
│                       │      │                   b7283698a68 
│                       │      ├ Description     : [Unknown description] 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-66
│                       │                         │      hr-7p6x-x5j3 
│                       │                         ├ [1]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                         ╰ [2]: https://www.openwall.com/lists/oss-security/2026/05/14/7 
│                       ├ [98] ╭ VulnerabilityID : CVE-2026-46483 
│                       │      ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.5 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.5?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-25.10&epoch=2 
│                       │      │                  ╰ UID : 526950e53908bbfb 
│                       │      ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                       │      │                  │         1d723afca4c817561dec 
│                       │      │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                       │      │                            a78a39b4be2f6ef374c7 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:420642d0528386a78bd4d62f4fcc485ed3634e671757dfdb8aed1
│                       │      │                   43ad6df402f 
│                       │      ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0479, a command injection vulnerability exists in
│                       │      │                   tar#Vimuntar() in
│                       │      │                   runtime/autoload/tar.vim when decompressing .tgz archives on
│                       │      │                    Unix-like systems. The function builds :!gunzip and :!gzip
│                       │      │                   -d commands using shellescape(tartail) without the {special}
│                       │      │                    flag, allowing a crafted archive filename to trigger Vim
│                       │      │                   cmdline-special expansion and execute shell commands in the
│                       │      │                   user's context. This vulnerability is fixed in 9.2.0479. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-78 
│                       │      │                  ╰ [1]: CWE-88 
│                       │      ├ VendorSeverity   ╭ nvd   : 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │      │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 
│                       │      │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e65
│                       │      │                  │      f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │      │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │      │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2f
│                       │      │                  │      pv-9ff7-xg5w 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │      ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │      ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ╰ [99] ╭ VulnerabilityID : CVE-2026-34743 
│                              ├ PkgID           : xz-utils@5.8.1-1build2 
│                              ├ PkgName         : xz-utils 
│                              ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xz-utils@5.8.1-1build2?arch=amd64&dist
│                              │                  │       ro=ubuntu-25.10 
│                              │                  ╰ UID : b60b2d28dbfe3b61 
│                              ├ InstalledVersion: 5.8.1-1build2 
│                              ├ FixedVersion    : 5.8.1-1ubuntu0.1 
│                              ├ Status          : fixed 
│                              ├ Layer            ╭ Digest: sha256:2f30d729d0cffb42001e622690eb7acb4f39579d9cf3
│                              │                  │         1d723afca4c817561dec 
│                              │                  ╰ DiffID: sha256:ba3afff67b418de4ef9ecba9dd38bd52bd0af55348b1
│                              │                            a78a39b4be2f6ef374c7 
│                              ├ SeveritySource  : ubuntu 
│                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34743 
│                              ├ DataSource       ╭ ID  : ubuntu 
│                              │                  ├ Name: Ubuntu CVE Tracker 
│                              │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                              ├ Fingerprint     : sha256:d540a9abc074e21902a826c71cb52879a703a2b442f3fdfe8c228
│                              │                   f40fd9d2e78 
│                              ├ Title           : xz: XZ Utils: Denial of Service via buffer overflow in index
│                              │                    decoding 
│                              ├ Description     : XZ Utils provide a general-purpose data-compression library
│                              │                   plus command-line tools. Prior to version 5.8.3, if
│                              │                   lzma_index_decoder() was used to decode an Index that
│                              │                   contained no Records, the resulting lzma_index was left in a
│                              │                    state where where a subsequent lzma_index_append() would
│                              │                   allocate too little memory, and a buffer overflow would
│                              │                   occur. This issue has been patched in version 5.8.3. 
│                              ├ Severity        : LOW 
│                              ├ CweIDs           ─ [0]: CWE-122 
│                              ├ VendorSeverity   ╭ azure : 1 
│                              │                  ├ nvd   : 2 
│                              │                  ├ photon: 2 
│                              │                  ├ redhat: 2 
│                              │                  ╰ ubuntu: 1 
│                              ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                              │                  │        │           /A:L 
│                              │                  │        ╰ V3Score : 5.3 
│                              │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                              │                           │           /A:L 
│                              │                           ╰ V3Score : 5.3 
│                              ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/03/31/13 
│                              │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-34743 
│                              │                  ├ [2]: https://github.com/tukaani-project/xz/commit/c8c22869e
│                              │                  │      780ff57c96b46939c3d79ff99395f87 
│                              │                  ├ [3]: https://github.com/tukaani-project/xz/releases/tag/v5.
│                              │                  │      8.3 
│                              │                  ├ [4]: https://github.com/tukaani-project/xz/security/advisor
│                              │                  │      ies/GHSA-x872-m794-cxhv 
│                              │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-34743 
│                              │                  ├ [6]: https://tukaani.org/xz/index-append-overflow.html 
│                              │                  ├ [7]: https://ubuntu.com/security/notices/USN-8362-1 
│                              │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34743 
│                              ├ PublishedDate   : 2026-04-02T19:21:33.187Z 
│                              ╰ LastModifiedDate: 2026-04-15T17:33:17.68Z 
╰ [1] ╭ Target  : Java 
      ├ Class   : lang-pkgs 
      ├ Type    : jar 
      ╰ Packages 
```
