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
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3e3ec0c444ac5c03fee9a2cd496e5e6d21a31c5ab81b087a72d5
│                       │       │                   f40a233e8052 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [1]   ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : bsdextrautils@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdextrautils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 847428c8a544f66d 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6a81cd214219ff68b8931664a79106249f795f214f0498427c42
│                       │       │                   25f0e6fc3ba9 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [2]   ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 411fc06346b75c80 
│                       │       ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:caa4eb5ca306e62c034e95814a311f6a84c16a14ef242f06a055
│                       │       │                   ee5bdd263bef 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [3]   ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │       ├ PkgName         : bsdutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 411fc06346b75c80 
│                       │       ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3fd5d37465a7fb9d3b17c1fe92806b9edead0fd87f18df90c33f
│                       │       │                   450b13337e9c 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [4]   ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libblkid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ddaca4141760dfcf 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:679b2a0edb64fed6d8844b04c78918d37011d6017413be45c070
│                       │       │                   389d6ac2b768 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [5]   ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libblkid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ddaca4141760dfcf 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:278cdf17ea797c6733c83ff9709d19a6ac376df75ee3308b2971
│                       │       │                   2555b7b4c3ef 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [6]   ╭ VulnerabilityID : CVE-2026-4046 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a88b78575eea113b4a8e127ccf819e8706c6d9f5f6cf49e67cb9
│                       │       │                   119645f07781 
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
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20587 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [5] : https://errata.almalinux.org/8/ALSA-2026-20587.html 
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2026:20587 
│                       │       │                  ├ [7] : https://inbox.sourceware.org/libc-announce/76814edf-
│                       │       │                  │       cf7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │       │                  ├ [8] : https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │       │                  ├ [9] : https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │       │                  ├ [11]: https://packages.fedoraproject.org/pkgs/glibc/glibc-
│                       │       │                  │       gconv-extra/ 
│                       │       │                  ├ [12]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │       │                  ├ [13]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007 
│                       │       │                  ├ [14]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │       │                  ╰ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │       ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │       ╰ LastModifiedDate: 2026-04-20T22:16:23.623Z 
│                       ├ [7]   ╭ VulnerabilityID : CVE-2026-4437 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d3e89f4a73a6cd131b8745039010a3b8b00ecf751773d7893270
│                       │       │                   e773c99f0087 
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
│                       │       ├ VendorSeverity   ╭ alma  : 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ photon: 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ├ rocky : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [8] : https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │       │                  ├ [9] : https://errata.rockylinux.org/RLSA-2026:19061 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │       │                  ├ [11]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │       │                  ├ [12]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │       │                  ╰ [13]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │       ╰ LastModifiedDate: 2026-04-07T18:41:36.647Z 
│                       ├ [8]   ╭ VulnerabilityID : CVE-2026-4438 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:26d06c7e5fc08bf29246f3ec7ed4ac7c3240b2ccfcd01a4e2a50
│                       │       │                   2420ebdf0963 
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
│                       │       ├ VendorSeverity   ╭ alma  : 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ├ rocky : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 4 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [8] : https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │       │                  ├ [9] : https://errata.rockylinux.org/RLSA-2026:19061 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │       │                  ├ [11]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │       │                  ├ [12]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │       │                  ╰ [13]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │       ╰ LastModifiedDate: 2026-04-07T18:40:02.177Z 
│                       ├ [9]   ╭ VulnerabilityID : CVE-2026-5435 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8e2ce3dd8141c54a767e04ad0e1c36642e7fb58b2091c083c191
│                       │       │                   67bf5b589bae 
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
│                       │       ╰ LastModifiedDate: 2026-05-05T17:38:37.03Z 
│                       ├ [10]  ╭ VulnerabilityID : CVE-2026-6238 
│                       │       ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc-bin 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 32f722fad25bcb3d 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a0b27d7215f705765c54909f7e82b7b0615a14eda37d0ee9899d
│                       │       │                   1f2a9096fcba 
│                       │       ├ Title           : glibc: glibc: Application crash or uninitialized memory
│                       │       │                   read via crafted DNS response 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.2 and newer fail
│                       │       │                   to validate the RDATA content against the RDATA length in a
│                       │       │                    DNS response when processing LOC, CERT, TKEY or TSIG
│                       │       │                   records, which may allow an attacker to craft a DNS
│                       │       │                   response, causing a target application to crash or read
│                       │       │                   uninitialized memory.
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
│                       │       ╰ LastModifiedDate: 2026-05-04T17:57:24.007Z 
│                       ├ [11]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:1b8b81c572b3726e772d8a26c2a2e75637a6fef897ab82636d0e
│                       │       │                   f98b6d8bee22 
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
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20587 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [5] : https://errata.almalinux.org/8/ALSA-2026-20587.html 
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2026:20587 
│                       │       │                  ├ [7] : https://inbox.sourceware.org/libc-announce/76814edf-
│                       │       │                  │       cf7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │       │                  ├ [8] : https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │       │                  ├ [9] : https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │       │                  ├ [11]: https://packages.fedoraproject.org/pkgs/glibc/glibc-
│                       │       │                  │       gconv-extra/ 
│                       │       │                  ├ [12]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │       │                  ├ [13]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007 
│                       │       │                  ├ [14]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │       │                  ╰ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │       ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │       ╰ LastModifiedDate: 2026-04-20T22:16:23.623Z 
│                       ├ [12]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e81ab1198cbeccd5fc055dc1a95b53c8f86c0e6a19ba39dd1942
│                       │       │                   96ccc452fb5a 
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
│                       │       ├ VendorSeverity   ╭ alma  : 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ photon: 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ├ rocky : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [8] : https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │       │                  ├ [9] : https://errata.rockylinux.org/RLSA-2026:19061 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │       │                  ├ [11]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │       │                  ├ [12]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │       │                  ╰ [13]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │       ╰ LastModifiedDate: 2026-04-07T18:41:36.647Z 
│                       ├ [13]  ╭ VulnerabilityID : CVE-2026-4438 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fd9dee9797e349cb431b6228180d5459d39bc9e2926489a40ad0
│                       │       │                   b37f51934756 
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
│                       │       ├ VendorSeverity   ╭ alma  : 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ├ rocky : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 4 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [8] : https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │       │                  ├ [9] : https://errata.rockylinux.org/RLSA-2026:19061 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │       │                  ├ [11]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │       │                  ├ [12]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │       │                  ╰ [13]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │       ╰ LastModifiedDate: 2026-04-07T18:40:02.177Z 
│                       ├ [14]  ╭ VulnerabilityID : CVE-2026-5435 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:49438a87cd5b8a135fe94e69dce45a1d0bd2a51e5b00221b6dcd
│                       │       │                   cfdb5edf7022 
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
│                       │       ╰ LastModifiedDate: 2026-05-05T17:38:37.03Z 
│                       ├ [15]  ╭ VulnerabilityID : CVE-2026-6238 
│                       │       ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : libc6 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 67fff5c1ddc17a00 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:eaf05633c73c0e96f7b37ffb0e9975eebb1e10f0d71fde3f5fb8
│                       │       │                   9ff69753c96f 
│                       │       ├ Title           : glibc: glibc: Application crash or uninitialized memory
│                       │       │                   read via crafted DNS response 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.2 and newer fail
│                       │       │                   to validate the RDATA content against the RDATA length in a
│                       │       │                    DNS response when processing LOC, CERT, TKEY or TSIG
│                       │       │                   records, which may allow an attacker to craft a DNS
│                       │       │                   response, causing a target application to crash or read
│                       │       │                   uninitialized memory.
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
│                       │       ╰ LastModifiedDate: 2026-05-04T17:57:24.007Z 
│                       ├ [16]  ╭ VulnerabilityID : CVE-2025-66382 
│                       │       ├ PkgID           : libexpat1@2.7.1-2ubuntu0.2 
│                       │       ├ PkgName         : libexpat1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.1-2ubuntu0.2?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : bb3ed74d0fd332c6 
│                       │       ├ InstalledVersion: 2.7.1-2ubuntu0.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:cf4dd91891e40850c734b265630ef220496f35a9d17b47a23df6
│                       │       │                   2d06862813d7 
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
│                       │       ╰ LastModifiedDate: 2026-06-02T14:16:37.12Z 
│                       ├ [17]  ╭ VulnerabilityID : CVE-2024-2236 
│                       │       ├ PkgID           : libgcrypt20@1.11.0-7ubuntu0.1 
│                       │       ├ PkgName         : libgcrypt20 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libgcrypt20@1.11.0-7ubuntu0.1?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 8f3635c00dca0a4f 
│                       │       ├ InstalledVersion: 1.11.0-7ubuntu0.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-2236 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8ff36a79569c30e59030fbe19d5289c7c6edacba49e1505bd15f
│                       │       │                   d3cc5176d996 
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
│                       │       ╰ LastModifiedDate: 2026-04-15T00:35:42.02Z 
│                       ├ [18]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : liblastlog2-2 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6aa63af50fb78d18 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8d8cc81b5b56277cf750086b067df4395fb0aeaab4999b13048a
│                       │       │                   53ac0ac7b6c9 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [19]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : liblastlog2-2 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 6aa63af50fb78d18 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:524cbbdbebb1f80d6eabc75a2103fbbc1f0292948ae94260578c
│                       │       │                   f6ff0bfc2eed 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [20]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libmount1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e278fd35c2ddbe27 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:9a01cfcef4311936aac5e00225aed10200becca1c030b4f51657
│                       │       │                   fc723277dba9 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [21]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libmount1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e278fd35c2ddbe27 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:08563960e36ec338c7756263d032aa5cd97f0bfc02aaa7df748f
│                       │       │                   09929404623a 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [22]  ╭ VulnerabilityID : CVE-2026-2297 
│                       │       ├ PkgID           : libpython3.13@3.13.7-1ubuntu0.4 
│                       │       ├ PkgName         : libpython3.13 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13@3.13.7-1ubuntu0.4?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : d39243325c040cfa 
│                       │       ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:9c3575c4d4b2d524d810762a8b20d5c8386a4d7b0a0fa9e0045c
│                       │       │                   11b86c30e82b 
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
│                       │       │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │       │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │       │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │       │                  ├ [26]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-13837 
│                       │       │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-15282 
│                       │       │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-59375 
│                       │       │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-6075 
│                       │       │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-0672 
│                       │       │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-1502 
│                       │       │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-2297 
│                       │       │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-3644 
│                       │       │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4224 
│                       │       │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4786 
│                       │       │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-6100 
│                       │       │                  ├ [37]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │       │                  ├ [38]: https://errata.rockylinux.org/RLSA-2026:10950 
│                       │       │                  ├ [39]: https://github.com/python/cpython/commit/482d6f8bdba
│                       │       │                  │       9da3725d272e8bb4a2d25fb6a603e 
│                       │       │                  ├ [40]: https://github.com/python/cpython/commit/69ddd9bb2cc
│                       │       │                  │       4bd69b1565647c18659c6a789ccd9 
│                       │       │                  ├ [41]: https://github.com/python/cpython/commit/876858c9f65
│                       │       │                  │       d9ab656c7fa639f268ce7856d89dd 
│                       │       │                  ├ [42]: https://github.com/python/cpython/commit/a51b1b512de
│                       │       │                  │       1d56b3714b65628a2eae2b07e535e 
│                       │       │                  ├ [43]: https://github.com/python/cpython/commit/e58e9802b9b
│                       │       │                  │       ec5cdbf48fc9bf1da5f4fda482e86 
│                       │       │                  ├ [44]: https://github.com/python/cpython/issues/145506 
│                       │       │                  ├ [45]: https://github.com/python/cpython/pull/145507 
│                       │       │                  ├ [46]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │       │                  ├ [47]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │       │                  ├ [48]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │       │                  ╰ [49]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │       ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │       ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [23]  ╭ VulnerabilityID : CVE-2026-2297 
│                       │       ├ PkgID           : libpython3.13-minimal@3.13.7-1ubuntu0.4 
│                       │       ├ PkgName         : libpython3.13-minimal 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-minimal@3.13.7-1ubuntu0
│                       │       │                  │       .4?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 18ff49702a1cf723 
│                       │       ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:dc16a3c470ab9ec23629ab86bc42aaa9939eeef9312037f4d760
│                       │       │                   9dd911c46dac 
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
│                       │       │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │       │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │       │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │       │                  ├ [26]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-13837 
│                       │       │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-15282 
│                       │       │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-59375 
│                       │       │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-6075 
│                       │       │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-0672 
│                       │       │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-1502 
│                       │       │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-2297 
│                       │       │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-3644 
│                       │       │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4224 
│                       │       │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4786 
│                       │       │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-6100 
│                       │       │                  ├ [37]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │       │                  ├ [38]: https://errata.rockylinux.org/RLSA-2026:10950 
│                       │       │                  ├ [39]: https://github.com/python/cpython/commit/482d6f8bdba
│                       │       │                  │       9da3725d272e8bb4a2d25fb6a603e 
│                       │       │                  ├ [40]: https://github.com/python/cpython/commit/69ddd9bb2cc
│                       │       │                  │       4bd69b1565647c18659c6a789ccd9 
│                       │       │                  ├ [41]: https://github.com/python/cpython/commit/876858c9f65
│                       │       │                  │       d9ab656c7fa639f268ce7856d89dd 
│                       │       │                  ├ [42]: https://github.com/python/cpython/commit/a51b1b512de
│                       │       │                  │       1d56b3714b65628a2eae2b07e535e 
│                       │       │                  ├ [43]: https://github.com/python/cpython/commit/e58e9802b9b
│                       │       │                  │       ec5cdbf48fc9bf1da5f4fda482e86 
│                       │       │                  ├ [44]: https://github.com/python/cpython/issues/145506 
│                       │       │                  ├ [45]: https://github.com/python/cpython/pull/145507 
│                       │       │                  ├ [46]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │       │                  ├ [47]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │       │                  ├ [48]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │       │                  ╰ [49]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │       ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │       ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [24]  ╭ VulnerabilityID : CVE-2026-2297 
│                       │       ├ PkgID           : libpython3.13-stdlib@3.13.7-1ubuntu0.4 
│                       │       ├ PkgName         : libpython3.13-stdlib 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-stdlib@3.13.7-1ubuntu0.
│                       │       │                  │       4?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 80f30a21647be5ac 
│                       │       ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d11c3914252e27d52c61fe06e6d107d23376ceac2f6309ee356f
│                       │       │                   8c900008920a 
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
│                       │       │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │       │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │       │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │       │                  ├ [26]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-13837 
│                       │       │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-15282 
│                       │       │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-59375 
│                       │       │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       025-6075 
│                       │       │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-0672 
│                       │       │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-1502 
│                       │       │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-2297 
│                       │       │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-3644 
│                       │       │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4224 
│                       │       │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4786 
│                       │       │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-6100 
│                       │       │                  ├ [37]: https://errata.almalinux.org/9/ALSA-2026-19177.html 
│                       │       │                  ├ [38]: https://errata.rockylinux.org/RLSA-2026:10950 
│                       │       │                  ├ [39]: https://github.com/python/cpython/commit/482d6f8bdba
│                       │       │                  │       9da3725d272e8bb4a2d25fb6a603e 
│                       │       │                  ├ [40]: https://github.com/python/cpython/commit/69ddd9bb2cc
│                       │       │                  │       4bd69b1565647c18659c6a789ccd9 
│                       │       │                  ├ [41]: https://github.com/python/cpython/commit/876858c9f65
│                       │       │                  │       d9ab656c7fa639f268ce7856d89dd 
│                       │       │                  ├ [42]: https://github.com/python/cpython/commit/a51b1b512de
│                       │       │                  │       1d56b3714b65628a2eae2b07e535e 
│                       │       │                  ├ [43]: https://github.com/python/cpython/commit/e58e9802b9b
│                       │       │                  │       ec5cdbf48fc9bf1da5f4fda482e86 
│                       │       │                  ├ [44]: https://github.com/python/cpython/issues/145506 
│                       │       │                  ├ [45]: https://github.com/python/cpython/pull/145507 
│                       │       │                  ├ [46]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │       │                  ├ [47]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │       │                  ├ [48]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │       │                  ╰ [49]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │       ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │       ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [25]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libsmartcols1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bc0da6f50bcb8eedc4fb0e3d0c768b866da918d8d49a911a61bb
│                       │       │                   1795855cdd9c 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [26]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libsmartcols1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=am
│                       │       │                  │       d64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bcbf2761e7dfddbd6d73176c8a14e6287007b8d3712c3aa67e49
│                       │       │                   7e9115d52dcb 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [27]  ╭ VulnerabilityID : CVE-2026-45447 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45447 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b55256624b32f4b849611ad0e4f553bf3515d7b9a19f24c75ed5
│                       │       │                   5a5d576e86d6 
│                       │       ├ Title           : Issue summary: A specially crafted PKCS#7 or S/MIME signed
│                       │       │                   message cou ... 
│                       │       ├ Description     : Issue summary: A specially crafted PKCS#7 or S/MIME signed
│                       │       │                   message could
│                       │       │                   trigger a use-after-free during PKCS#7 signature
│                       │       │                   verification.
│                       │       │                   
│                       │       │                   Impact summary: A use-after-free may result in process
│                       │       │                   crashes, heap
│                       │       │                   corruption, or potentially remote code execution.
│                       │       │                   When processing a PKCS#7 or S/MIME signed message, if the
│                       │       │                   SignedData
│                       │       │                   digestAlgorithms field is present as an empty ASN.1 SET,
│                       │       │                   OpenSSL may
│                       │       │                   incorrectly free a caller-owned BIO during PKCS7_verify().
│                       │       │                   A subsequent
│                       │       │                   use of the BIO by the calling application results in a
│                       │       │                   use-after-free
│                       │       │                   condition.
│                       │       │                   In the common case this occurs when the application later
│                       │       │                   calls
│                       │       │                   BIO_free() on the BIO originally passed to PKCS7_verify().
│                       │       │                   Depending
│                       │       │                   on allocator behavior and application-specific BIO usage
│                       │       │                   patterns, this
│                       │       │                   may result in a crash or other memory corruption. In some
│                       │       │                   application
│                       │       │                   contexts this may potentially be exploitable for remote
│                       │       │                   code execution.
│                       │       │                   Applications that process PKCS#7 or S/MIME signed messages
│                       │       │                   using OpenSSL
│                       │       │                   PKCS#7 APIs may be affected. Applications using the CMS
│                       │       │                   APIs for this
│                       │       │                   processing are not affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : HIGH 
│                       │       ├ CweIDs           ─ [0]: CWE-416 
│                       │       ├ VendorSeverity   ─ ubuntu: 3 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/3aad5eb7af4
│                       │       │                  │      de4ee0633c30a8541a54d9bbde63c 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/7d4a980c622
│                       │       │                  │      58c5910cc883936e0c8dbab4d75a8 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/9dfd688ad22
│                       │       │                  │      90fc5075cacbc9bf0c9a93eefed54 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/a541ae8bfe8
│                       │       │                  │      49a30cc885e8780715c0f488e496c 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/c505d7559da
│                       │       │                  │      5d5f9f2c3913c6883a5562ce7273e 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-45447 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:19.277Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T15:16:35.16Z 
│                       ├ [28]  ╭ VulnerabilityID : CVE-2026-34182 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34182 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4d11b5118a298e6a5d69693ee614d1ef58fb382515839d1cac05
│                       │       │                   831d9827d113 
│                       │       ├ Title           : Issue Summary: Cryptographic Message Services (CMS)
│                       │       │                   processing fails t ... 
│                       │       ├ Description     : Issue Summary: Cryptographic Message Services (CMS)
│                       │       │                   processing fails to perform
│                       │       │                   sufficient input validation on the cipher and tag length
│                       │       │                   fields of
│                       │       │                   AuthEnvelopedData containers, leading to various potential
│                       │       │                   compromises.
│                       │       │                   
│                       │       │                   Impact Summary: Attackers making use of these
│                       │       │                   vulnerabilities may achieve
│                       │       │                   key-equivalent functionality for a given CMS recipient
│                       │       │                   and/or bypass integrity
│                       │       │                   validation for a given message.
│                       │       │                   In one use case, an attacker may send a CMS message
│                       │       │                   containing
│                       │       │                   AuthEnvelopedData with the cipher specified as a non-AEAD
│                       │       │                   cipher.  OpenSSL
│                       │       │                   erroneously allows this selection, and attempts to decrypt
│                       │       │                   and validate the
│                       │       │                   message.
│                       │       │                   An on-path attacker who captures one legitimate AES-GCM
│                       │       │                   AuthEnvelopedData
│                       │       │                   addressed to the victim can re-emit it with the
│                       │       │                   recipientInfos set left
│                       │       │                   byte-for-byte intact, so the victim's private key still
│                       │       │                   unwraps the genuine CEK
│                       │       │                   (the content-encryption key), but with the inner OID
│                       │       │                   rewritten to AES-256-OFB
│                       │       │                   (Output Feedback Mode, an unauthenticated keystream mode)
│                       │       │                   and with an
│                       │       │                   attacker-chosen IV and ciphertext. The victim initializes
│                       │       │                   AES-256-OFB under the
│                       │       │                   real CEK, never consults the MAC field, and CMS_decrypt()
│                       │       │                   returns success.
│                       │       │                   If the application under attack responds to the attacker
│                       │       │                   with any indicator
│                       │       │                   showing success or failure of the decryption effort, it is
│                       │       │                   possible for the
│                       │       │                   attacker to use this as an oracle to obtain key equivalent
│                       │       │                   functionality for the
│                       │       │                   CEK used for the chosen recipient of the message.
│                       │       │                   In another use case, an attacker can reduce the tag length
│                       │       │                   of the chosen AEAD
│                       │       │                   cipher for a given AuthEnvelopedData container to be a
│                       │       │                   single byte long,
│                       │       │                   allowing an attacker to brute force CMS decryption,
│                       │       │                   producing an integrity
│                       │       │                   bypass for applications that trust CMS_decrypt() to reject
│                       │       │                   modified content.
│                       │       │                   The FIPS modules are not affected by this issue. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-354 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/03c1f4d45fb
│                       │       │                  │      963aee7d5833390c507cd290182bc 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/439ed7d2c09
│                       │       │                  │      62ce964482727264668bf277c333f 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7947e6a81eb
│                       │       │                  │      8776802f159fb6762cb7fcf7e34c7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/9fd97f8cfdc
│                       │       │                  │      2c0be214998de3b2b55c8edf6c7ac 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/d2ca86bcd43
│                       │       │                  │      e4f17d899f347101766b6107676e0 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34182 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.857Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T17:16:32.48Z 
│                       ├ [29]  ╭ VulnerabilityID : CVE-2026-34183 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34183 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8df68eb46278471f7344583f93155387755328f825573a777335
│                       │       │                   e710ee378c25 
│                       │       ├ Title           : Issue summary: Remote peer may exhaust heap memory of the
│                       │       │                   QUIC server  ... 
│                       │       ├ Description     : Issue summary: Remote peer may exhaust heap memory of the
│                       │       │                   QUIC
│                       │       │                   server or client by flooding it with packets containing
│                       │       │                   PATH_CHALLENGE
│                       │       │                   frames.
│                       │       │                   
│                       │       │                   Impact summary: A malicious remote peer can cause an
│                       │       │                   unbounded
│                       │       │                   memory allocation which can lead to an abnormal termination
│                       │       │                    of the
│                       │       │                   application acting as a QUIC client or server and a Denial
│                       │       │                   of Service.
│                       │       │                   A remote peer may exhaust heap memory by flooding the
│                       │       │                   local
│                       │       │                   QUIC stack with PATH_CHALLENGE frames. The local QUIC
│                       │       │                   stack
│                       │       │                   allocates a PATH_RESPONSE frame for every PATH_CHALLENGE it
│                       │       │                    receives.
│                       │       │                   The allocated PATH_RESPONSE frame gets freed only when the
│                       │       │                   remote
│                       │       │                   peer acknowledges reception of the PATH_RESPONSE frame
│                       │       │                   which will
│                       │       │                   not be done by a malicious peer.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue. The QUIC stack is outside of OpenSSL FIPS
│                       │       │                   module
│                       │       │                   boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-1325 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/5b306efb0b3
│                       │       │                  │      779dfdd0803b4afc9d08c91f11517 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/7d06955ebe0
│                       │       │                  │      ecf8adfd4c1e92018586da47ef9ac 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d2e9efbe490
│                       │       │                  │      0a373227deb136e8665401404ffac 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/fbaa83859c0
│                       │       │                  │      1ad64f497b757aaf51be7d05ed9eb 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-34183 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:05Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T16:17:01.217Z 
│                       ├ [30]  ╭ VulnerabilityID : CVE-2026-42764 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42764 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fadbb42535ac376ab30817b2c1269136a2269b83238400cba1db
│                       │       │                   865b21c82666 
│                       │       ├ Title           : Issue summary: Receiving a QUIC initial packet with an
│                       │       │                   invalid token m ... 
│                       │       ├ Description     : Issue summary: Receiving a QUIC initial packet with an
│                       │       │                   invalid token may
│                       │       │                   trigger a NULL pointer dereference in the OpenSSL QUIC
│                       │       │                   server with
│                       │       │                   address validation disabled.
│                       │       │                   
│                       │       │                   Impact summary: NULL pointer dereference typically causes
│                       │       │                   abnormal termination
│                       │       │                   of the affected QUIC server process and a Denial of
│                       │       │                   Service.
│                       │       │                   If the address validation is disabled in the OpenSSL QUIC
│                       │       │                   server
│                       │       │                   implementation, an attacker can crash the server by sending
│                       │       │                    an initial
│                       │       │                   packet with an invalid or expired token.
│                       │       │                   By default, the client address validation is enabled in the
│                       │       │                    OpenSSL QUIC server
│                       │       │                   implementation, which makes the default configuration not
│                       │       │                   vulnerable
│                       │       │                   to this issue. However if the SSL_LISTENER_FLAG_NO_VALIDATE
│                       │       │                    is used with
│                       │       │                   the SSL_new_listener() call, the address validation is
│                       │       │                   disabled making the
│                       │       │                   vulnerable code reachable.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/5e3ed291b8a
│                       │       │                  │      f0b03d5d3b9e56a1da69a187e9729 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/a45a0aba809
│                       │       │                  │      5682c88ff4fc4a784892b8c6f0677 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/bf29a458c1a
│                       │       │                  │      231eca87e384c62b9c2553fa57a91 
│                       │       │                  ├ [3]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-42764 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:07.693Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.23Z 
│                       ├ [31]  ╭ VulnerabilityID : CVE-2026-45445 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45445 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:1b7ed689697d9372a672f43fd2bfc5cef87c0856d6bca52ca26f
│                       │       │                   cf78601b34d7 
│                       │       ├ Title           : Issue summary: When an application drives an AES-OCB
│                       │       │                   context through t ... 
│                       │       ├ Description     : Issue summary: When an application drives an AES-OCB
│                       │       │                   context through the
│                       │       │                   public EVP_Cipher() one-shot interface, the
│                       │       │                   application-supplied
│                       │       │                   initialisation vector (IV) is silently discarded.
│                       │       │                   
│                       │       │                   Impact summary: Every message encrypted under the same key
│                       │       │                   uses the
│                       │       │                   same effective nonce regardless of the IV supplied by the
│                       │       │                   caller,
│                       │       │                   resulting in (key, nonce) reuse and loss of
│                       │       │                   confidentiality.  If the
│                       │       │                   same code path is used to compute the authentication tag,
│                       │       │                   the tag
│                       │       │                   depends only on the (key, IV) pair and not on the plaintext
│                       │       │                    or
│                       │       │                   ciphertext, allowing universal forgery of arbitrary
│                       │       │                   ciphertext from a
│                       │       │                   single captured message.
│                       │       │                   OpenSSL provides two ways to drive a cipher: the documented
│                       │       │                    streaming
│                       │       │                   interface (EVP_CipherUpdate / EVP_CipherFinal_ex) and a
│                       │       │                   lower-level
│                       │       │                   one-shot, EVP_Cipher(), whose documentation explicitly
│                       │       │                   recommends
│                       │       │                   against use by applications in favour of EVP_CipherUpdate()
│                       │       │                    and
│                       │       │                   EVP_CipherFinal_ex().  The OCB provider's streaming handler
│                       │       │                    flushes
│                       │       │                   the application-supplied IV into the OCB context before
│                       │       │                   processing
│                       │       │                   data; the one-shot handler did not.  Every call to
│                       │       │                   EVP_Cipher() on an
│                       │       │                   AES-OCB context therefore ran with the all-zero key-derived
│                       │       │                    offset
│                       │       │                   state left by cipher initialisation, regardless of the
│                       │       │                   caller's IV.
│                       │       │                   If EVP_EncryptFinal_ex() is subsequently used to obtain
│                       │       │                   the
│                       │       │                   authentication tag, the deferred IV setup runs at that
│                       │       │                   point and
│                       │       │                   clears the running checksum that should have been
│                       │       │                   accumulated over the
│                       │       │                   plaintext.  The resulting tag is a function of (key, IV)
│                       │       │                   only and
│                       │       │                   verifies against any ciphertext produced under the same
│                       │       │                   (key, IV)
│                       │       │                   pair.
│                       │       │                   The OpenSSL SSL/TLS implementation is not affected: AES-OCB
│                       │       │                    is not a
│                       │       │                   TLS cipher suite, and libssl does not call EVP_Cipher() in
│                       │       │                   any case.
│                       │       │                   Applications that drive AES-OCB through the documented
│                       │       │                   streaming AEAD
│                       │       │                   API (EVP_CipherUpdate / EVP_CipherFinal_ex) are not
│                       │       │                   affected.  Only
│                       │       │                   applications that combine the AES-OCB cipher with the
│                       │       │                   EVP_Cipher()
│                       │       │                   one-shot API are vulnerable.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue, as AES-OCB is outside the OpenSSL FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/323f0b6e7d5
│                       │       │                  │      30a4cb4336d50c88cb70f3ac2a451 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/787a6dfba81
│                       │       │                  │      b7b09c1e05ab31396c0cd7c36b3f7 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7ac4715234e
│                       │       │                  │      e72d9f3c93426a2c08554b5b771af 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/843c9b94ca9
│                       │       │                  │      c2ed248bb30127bb4f3d7af0d607c 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/983d54b5cce
│                       │       │                  │      8d16147548ed1a37892d1720bbab6 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-45445 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:18.993Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.507Z 
│                       ├ [32]  ╭ VulnerabilityID : CVE-2026-34180 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34180 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:fe8d416da8d3910cefc524445ba66a92ca40327ad74a5e684060
│                       │       │                   3d325a18dde5 
│                       │       ├ Title           : Issue summary: Parsing a crafted DER-encoded ASN.1
│                       │       │                   structure with a pr ... 
│                       │       ├ Description     : Issue summary: Parsing a crafted DER-encoded ASN.1
│                       │       │                   structure with a primitive
│                       │       │                   element whose content exceeds 2 gigabytes in length may
│                       │       │                   cause a heap buffer
│                       │       │                   over-read on 64-bit Unix and Unix-like platforms.
│                       │       │                   
│                       │       │                   Impact summary: The heap buffer over-read may crash the
│                       │       │                   application (Denial of
│                       │       │                   Service) or to load into the decoded ASN.1 object contents
│                       │       │                   of memory beyond the
│                       │       │                   end of the input buffer.  More typically such ASN.1
│                       │       │                   elements would instead be
│                       │       │                   truncated.
│                       │       │                   An integer truncation in OpenSSL's ASN.1 decoder causes the
│                       │       │                    content length of
│                       │       │                   an ASN.1 primitive element to be mishandled when it exceeds
│                       │       │                    2 gigabytes. In the
│                       │       │                   worst case the truncated length is treated as a request to
│                       │       │                   scan the binary
│                       │       │                   content for a terminating zero byte, possibly causing
│                       │       │                   OpenSSL to read either
│                       │       │                   less than or beyond the end of the allocated buffer.
│                       │       │                   Applications that pass attacker-supplied data to
│                       │       │                   d2i_X509(), d2i_PKCS7(), or
│                       │       │                   any other d2i_* decoding function are affected. OpenSSL's
│                       │       │                   own command-line
│                       │       │                   tools are not vulnerable, as data read through the BIO
│                       │       │                   layer is checked before
│                       │       │                   it reaches the affected code. The issue only affects 64-bit
│                       │       │                    Unix and Unix-like
│                       │       │                   platforms; 32-bit platforms and 64-bit Windows are not
│                       │       │                   affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by this issue,
│                       │       │                   as the affected code is outside the OpenSSL FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/1c6908e4fa5
│                       │       │                  │      fa568752221d8eaf561a809751e5d 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/cbe418ae978
│                       │       │                  │      539cf14a398a207dba834c0e93e83 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d93853c4211
│                       │       │                  │      0d6319e3df07842b488cb9f7ac5ff 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/da5d62af75f
│                       │       │                  │      69d6fbf7803743d7c56ac75461e43 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/f696c73c3e6
│                       │       │                  │      1b8c502d040af62e690c060908a16 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34180 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.6Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:22.627Z 
│                       ├ [33]  ╭ VulnerabilityID : CVE-2026-34181 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34181 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4825c05451b8ddf2a4c8081f238f05c373b48701906fb2625ce7
│                       │       │                   aa2962b5b3b1 
│                       │       ├ Title           : Issue Summary: The PKCS#12 file processing fails to perform
│                       │       │                    sufficient ... 
│                       │       ├ Description     : Issue Summary: The PKCS#12 file processing fails to perform
│                       │       │                    sufficient input
│                       │       │                   validation for files that use Password-Based Message
│                       │       │                   Authentication Code 1
│                       │       │                   (PBMAC1) integrity mechanism allowing a certificate and
│                       │       │                   private key forgery.
│                       │       │                   
│                       │       │                   Impact Summary: An attacker impersonating a user can cause
│                       │       │                   a service reading
│                       │       │                   PKCS#12 files to accept forged certificates and private
│                       │       │                   keys with a 1 in 256
│                       │       │                   probability.
│                       │       │                   If a service accepting PKCS#12 files is using passwords for
│                       │       │                    authenticating
│                       │       │                   the received files, the attacker can create unencrypted
│                       │       │                   PKCS#12 files that
│                       │       │                   use PBMAC1 authentication that specifies an HMAC key of
│                       │       │                   only one byte, allowing
│                       │       │                   them to craft a file that will be accepted with a 1 in 256
│                       │       │                   That would then cause the service to accept a certificate
│                       │       │                   and private key
│                       │       │                   controlled by the attacker.
│                       │       │                   The FIPS modules are not affected by this issue, as the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-354 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/0300eb9ddce
│                       │       │                  │      7a0895bf301a4b0c03a9da2313a0f 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/79eb76a937e
│                       │       │                  │      474bb7610a0a3dc57131dc8dc6610 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/85dcbb3abaa
│                       │       │                  │      4878af5c8fbbe11bce708fcf984a7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/ec36f2417c4
│                       │       │                  │      ddd8cabce4b4a60a3d7a7365f2d81 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-34181 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.74Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T17:16:32.29Z 
│                       ├ [34]  ╭ VulnerabilityID : CVE-2026-42766 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42766 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:51d3067191e0a954f1b2eeb4bd6469637018f15a0909de4010f7
│                       │       │                   5471aa7076dd 
│                       │       ├ Title           : Issue summary: A specially crafted password-encrypted CMS
│                       │       │                   message can  ... 
│                       │       ├ Description     : Issue summary: A specially crafted password-encrypted CMS
│                       │       │                   message
│                       │       │                   can trigger a NULL pointer dereference during CMS
│                       │       │                   decryption.
│                       │       │                   
│                       │       │                   Impact summary: This NULL pointer dereference leads to an
│                       │       │                   application crash
│                       │       │                   and a Denial of Service.
│                       │       │                   The CMS PasswordRecipientInfo.keyDerivationAlgorithm field
│                       │       │                   is defined as
│                       │       │                   OPTIONAL in the ASN.1 specification and may therefore be
│                       │       │                   absent in specially
│                       │       │                   crafted inputs. During the password-based CMS decryption
│                       │       │                   the OpenSSL
│                       │       │                   CMS implementation dereferences this field without first
│                       │       │                   checking whether it
│                       │       │                   was present.
│                       │       │                   An attacker who supplies such a CMS message to an
│                       │       │                   application performing
│                       │       │                   password-based CMS decryption can trigger an application
│                       │       │                   crash, leading to
│                       │       │                   a Denial of Service.
│                       │       │                   Applications that process password-encrypted CMS messages
│                       │       │                   may be affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/056d06c1918
│                       │       │                  │      fafbb98c1c85a02e4c47cc4e199ce 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/12bc26ffb3a
│                       │       │                  │      2be728c9b86e1cae277de5b33dfa4 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/3ff64913615
│                       │       │                  │      d648cfbb6a6f1cf5529ae7ea829d7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/ab52d88cb53
│                       │       │                  │      74876d59aee3c91f9e4ccce2b7ce4 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/da26f368732
│                       │       │                  │      b83e40e9d356fe61c3d3aaab6d2e8 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-42766 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:07.97Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.52Z 
│                       ├ [35]  ╭ VulnerabilityID : CVE-2026-42767 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42767 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0ef888d1bfde8387c6835faf795b433ddd6bda9359cdf272df09
│                       │       │                   ccde9f9b6bd6 
│                       │       ├ Title           : Issue summary: An attacker-controlled CMP (Certificate
│                       │       │                   Management Prot ... 
│                       │       ├ Description     : Issue summary: An attacker-controlled CMP (Certificate
│                       │       │                   Management Protocol)
│                       │       │                   server could trigger a NULL pointer dereference in a CMP
│                       │       │                   client application.
│                       │       │                   
│                       │       │                   Impact summary: A NULL pointer dereference causes a crash
│                       │       │                   of the
│                       │       │                   application and a Denial of Service.
│                       │       │                   An attacker controlling a CMP server (or acting as a
│                       │       │                   man-in-the-middle) could
│                       │       │                   craft a CMP response containing a CRMF (Certificate Request
│                       │       │                    Message Format)
│                       │       │                   CertRepMessage with an EncryptedValue structure where the
│                       │       │                   symmAlg field
│                       │       │                   has an algorithm OID but no parameters field. When the
│                       │       │                   OpenSSL CMP client
│                       │       │                   processes this response, the NULL dereference occurs,
│                       │       │                   causing a crash of
│                       │       │                   the CMP client.
│                       │       │                   Applications that process untrusted CMP/CRMF messages may
│                       │       │                   be affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/61a86a8cd73
│                       │       │                  │      546c9fea916f3d304c1293e05c046 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/665d5254083
│                       │       │                  │      affde9982efca7c41dd01cacc8774 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/810b722f772
│                       │       │                  │      652ad48042bcc7ab07e3414b11d0f 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/b90ff3b1bd3
│                       │       │                  │      3b1c18e6a09936d097c2eddef8873 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/e6f912907fc
│                       │       │                  │      2ec82a0fd07aae55172c5e5e3d90d 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-42767 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.093Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.683Z 
│                       ├ [36]  ╭ VulnerabilityID : CVE-2026-42768 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42768 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6d0f38ec6f502f3e2f44ba1245c10f0db688fedfff748422fa36
│                       │       │                   0cbe52e70f18 
│                       │       ├ Title           : Issue summary: The CMS_decrypt and PKCS7_decrypt functions
│                       │       │                   are vulnera ... 
│                       │       ├ Description     : Issue summary: The CMS_decrypt and PKCS7_decrypt functions
│                       │       │                   are vulnerable to
│                       │       │                   Bleichenbacher-style attack when an attacker is able to
│                       │       │                   provide the CMS or
│                       │       │                   S/MIME messages and observe the error code and/or
│                       │       │                   decryption output.
│                       │       │                   
│                       │       │                   Impact summary: The Bleichenbacher-style attack allows an
│                       │       │                   attacker to use the
│                       │       │                   victim's vulnerable application as a way to decrypt or sign
│                       │       │                    messages with the
│                       │       │                   victim's private RSA key.
│                       │       │                   The attack is possible in 2 variants.
│                       │       │                   1. The decryption API (CMS_decrypt(), PKCS7_decrypt()) is
│                       │       │                   used without
│                       │       │                   providing the recipient certificate. In this case OpenSSL
│                       │       │                   iterates over every
│                       │       │                   KeyTransRecipientInfo (KTRI) without stopping at the first
│                       │       │                   success.
│                       │       │                   An attacker who authors a message with two KTRI entries —
│                       │       │                   the first one
│                       │       │                   wrapping a real CEK under the victim's public key, the
│                       │       │                   second with an
│                       │       │                   arbitrary probe ciphertext — obtains opportunity to iterate
│                       │       │                    the 2nd KTRI to
│                       │       │                   get a valid PKCS#1 v1.5 padding if the error code of the
│                       │       │                   application is
│                       │       │                   available.
│                       │       │                   That is a Bleichenbacher oracle (Bleichenbacher, CRYPTO
│                       │       │                   '98): an
│                       │       │                   adaptive-chosen-ciphertext side channel from which the
│                       │       │                   attacker decrypts any
│                       │       │                   RSA ciphertext to the victim's key or forges any PKCS#1
│                       │       │                   v1.5 signature under
│                       │       │                   it.
│                       │       │                   2. When the decryption API (CMS_decrypt(), PKCS7_decrypt())
│                       │       │                    is provided with
│                       │       │                   the recipient certificate, and the recipient is not found,
│                       │       │                   a random
│                       │       │                   key is substituted.
│                       │       │                   An attacker who authors a message and is able to compare
│                       │       │                   both error code and
│                       │       │                   the result of the decryption, can mount a Bleichenbacher
│                       │       │                   oracle.
│                       │       │                   We are not aware of any applications that provide a remote
│                       │       │                   attacker
│                       │       │                   an opportunity to mount an attack described in these
│                       │       │                   scenarios. We consider
│                       │       │                   the existence of such application very unlikely, and for
│                       │       │                   this reason this
│                       │       │                   CVE has been evaluated as Low severity.
│                       │       │                   To avoid these attacks, when RSA PKCS#1 v1.5 Key Transport
│                       │       │                   is in use, the
│                       │       │                   invoked EVP_PKEY_decrypt() will use the implicit rejection
│                       │       │                   mechanism described
│                       │       │                   in draft-irtf-cfrg-rsa-guidance. In previous OpenSSL
│                       │       │                   releases the implicit
│                       │       │                   rejection was explicitly disabled.
│                       │       │                   The implicit rejection mechanism always returns a plaintext
│                       │       │                    value,
│                       │       │                   the symmetric key. This result is deterministic for the
│                       │       │                   ciphertext and the
│                       │       │                   private key.  The length of the decryption result can
│                       │       │                   happen to match the
│                       │       │                   length of the key of the symmetric cipher that was used for
│                       │       │                    the content
│                       │       │                   encryption. When a certificate is not provided, the last
│                       │       │                   RecipientInfo
│                       │       │                   producing a key that looks valid will be used. It may cause
│                       │       │                    getting garbage
│                       │       │                   content on decryption. As a proper way to deal with this a
│                       │       │                   recipient
│                       │       │                   certificate has to be provided to identify the particular
│                       │       │                   RecipientInfo for
│                       │       │                   decryption.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, and 3.4 are not affected
│                       │       │                    by this issue, as
│                       │       │                   CMS and S/MIME processing happens outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-514 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/a2ca7b2d73e
│                       │       │                  │      0ffc1eae183fe6e1741dac767cb4f 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/bbb151a8304
│                       │       │                  │      1705d9d001ed2f9c12f5523e1b54d 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/dd68364107a
│                       │       │                  │      58841c0a2546812518b65d3a23abd 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/f04b377be3d
│                       │       │                  │      821741c86d1f4bf84dee09f3d5c3e 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42768 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.223Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.84Z 
│                       ├ [37]  ╭ VulnerabilityID : CVE-2026-42769 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42769 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bcc71f6f0f3a23f72c4e0fcf38fb9967d54a6b42f93853a1bb44
│                       │       │                   5459520e2070 
│                       │       ├ Title           : Issue Summary: An error in the callback used to verify the
│                       │       │                   certificate ... 
│                       │       ├ Description     : Issue Summary: An error in the callback used to verify the
│                       │       │                   certificate
│                       │       │                   provided in a Root CA key update Certificate Management
│                       │       │                   Protocol (CMP)
│                       │       │                   message response rendered the certificate validation
│                       │       │                   ineffectual, which
│                       │       │                   could lead to escalation of credentials from the
│                       │       │                   Registration Authority (RA)
│                       │       │                   level to the root Certification Authority (root CA) level.
│                       │       │                   
│                       │       │                   Impact Summary: The Registration Autority could replace the
│                       │       │                    root CA
│                       │       │                   certificate for the CMP clients with an arbitrary root CA
│                       │       │                   certificate.
│                       │       │                   One of the parts of the Certificate Management Protocol
│                       │       │                   (CMP), specified in
│                       │       │                   RFC 9810, is Root Certification Authority (root CA) key
│                       │       │                   Rollover,
│                       │       │                   which is sent by the server in a message with type
│                       │       │                   'id-it-rootCaKeyUpdate'.
│                       │       │                   As part of these messages, 'newWithOld' certificate, the
│                       │       │                   new root CA
│                       │       │                   certificate signed with the old root CA key, is provided,
│                       │       │                   and verifying its
│                       │       │                   signature is crucial for transferring the trust from the
│                       │       │                   old CA key to the
│                       │       │                   new one.
│                       │       │                   The 'id-it-rootCaKeyUpdate' messages are expected to be
│                       │       │                   processed with
│                       │       │                   OSSL_CMP_get1_rootCaKeyUpdate(), that is expected to verify
│                       │       │                    the 'newWithOld'
│                       │       │                   certificate.  A typo in the certificate chain building code
│                       │       │                    led to adding
│                       │       │                   an incorrect certificate ('newWithOld' instead of
│                       │       │                   'oldRoot') to the
│                       │       │                   certificate chain, rendering the certificate verification
│                       │       │                   process ineffectual
│                       │       │                   (only the issuer name and the algorithm OIDs were verified
│                       │       │                   by other parts
│                       │       │                   of the verification code).
│                       │       │                   An attacker who already has credentials that satisfy the
│                       │       │                   CMP message
│                       │       │                   protection checks can generate a new key pair and use a
│                       │       │                   crafted self-signed
│                       │       │                   certificate in its 'id-it-rootCaKeyUpdate' CMP messages
│                       │       │                   which affected CMP
│                       │       │                   clients would accept as a new trust anchor.
│                       │       │                   Significant preconditions for the attack (having valid
│                       │       │                   RA-level credentials)
│                       │       │                   are the reason the issue was assigned Low severity.
│                       │       │                   The FIPS modules are not affected by this issue, as the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-295 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/54d0989997e
│                       │       │                  │      5fc26057009a9782c3441ce3842fb 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/777b363b16f
│                       │       │                  │      cf2153bb3ded39dc3838713667c44 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d35cd473a27
│                       │       │                  │      1bf3ce7bf3d32af53217fb83ae92c 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/d531f21c0fe
│                       │       │                  │      99067a66fc0ff1161ef127f9cd70b 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42769 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.027Z 
│                       ├ [38]  ╭ VulnerabilityID : CVE-2026-42770 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42770 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6ce1a6e6359cbb8a5ae6b87ad0c3623ea1b95380c0a479252ee0
│                       │       │                   a70b1989148a 
│                       │       ├ Title           : Issue summary: When EVP_PKEY_derive_set_peer() is called
│                       │       │                   with a DHX (X ... 
│                       │       ├ Description     : Issue summary: When EVP_PKEY_derive_set_peer() is called
│                       │       │                   with a DHX (X9.42)
│                       │       │                   peer key, the peer key is not properly checked for the
│                       │       │                   subgroup membership.
│                       │       │                   
│                       │       │                   Impact summary: A malicious peer which presents an X9.42
│                       │       │                   key carrying the
│                       │       │                   victim's p and g parameters, a forged q = r (a small prime
│                       │       │                   factor of the
│                       │       │                   cofactor (p−1)/q_local), and a public value Y of order r
│                       │       │                   can recover the
│                       │       │                   victim's private key after a small number of key exchange
│                       │       │                   attempts.
│                       │       │                   When EVP_PKEY_derive_set_peer() is called with a DHX
│                       │       │                   (X9.42) peer key, the
│                       │       │                   subgroup membership check Y^q ≡ 1 (mod p) is performed
│                       │       │                   using the peer's
│                       │       │                   own q parameter, not the local key's q. The peer's domain
│                       │       │                   parameters are
│                       │       │                   then matched against the domain parameters of the private
│                       │       │                   key, but the value
│                       │       │                   of q is not compared.
│                       │       │                   A malicious peer who presents an X9.42 key carrying the
│                       │       │                   victim's p, g,
│                       │       │                   a forged q = r (a small prime factor of the cofactor), and
│                       │       │                   a public
│                       │       │                   value Y of order r passes all checks. The shared secret
│                       │       │                   then takes only
│                       │       │                   r distinct values, leaking priv mod r. Repeating for each
│                       │       │                   small-prime
│                       │       │                   factor of the cofactor and combining via CRT recovers the
│                       │       │                   full private
│                       │       │                   key (Lim–Lee / small-subgroup-confinement attack).
│                       │       │                   The realistic attack surface is narrow: principally CMP
│                       │       │                   deployments with
│                       │       │                   long-lived RA/CA DHX keys and bespoke enterprise or
│                       │       │                   government applications
│                       │       │                   using X9.42 DHX static keys with interactive protocols and
│                       │       │                   therefore this
│                       │       │                   issue was assigned Low severity.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are
│                       │       │                   affected by this
│                       │       │                   issue. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/3da5a516cd2
│                       │       │                  │      635a320ff748503db2cef7c4b0f02 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/3ddbb7ab50b
│                       │       │                  │      d93dfc59cbe08e269a67605aeebdb 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/5f452bba2c6
│                       │       │                  │      81423d8fcffd120a19b757ee42e3c 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/7fbfde7677e
│                       │       │                  │      d8808828bf00ff01c937ca04bdda2 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/ca2237ab561
│                       │       │                  │      5641b662183b077f62c08d75e8070 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-42770 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.523Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.197Z 
│                       ├ [39]  ╭ VulnerabilityID : CVE-2026-45446 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45446 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:1a8ee3f073d3ce7c6987b711083ac6e001de8b3cbe636c0b025f
│                       │       │                   790d6aa50516 
│                       │       ├ Title           : Issue summary: The implementations of AES-SIV (RFC 5297)
│                       │       │                   and AES-GCM-S ... 
│                       │       ├ Description     : Issue summary: The implementations of AES-SIV (RFC 5297)
│                       │       │                   and AES-GCM-SIV
│                       │       │                   (RFC 8452) mishandle the authentication of AAD (Additional
│                       │       │                   Authenticated
│                       │       │                   Data) with an empty ciphertext allowing a forgery of such
│                       │       │                   messages.
│                       │       │                   
│                       │       │                   Impact summary: An attacker can forge empty messages with
│                       │       │                   arbitrary AAD
│                       │       │                   to the victim's application using these ciphers.
│                       │       │                   AES-SIV (RFC 5297) and AES-GCM-SIV (RFC 8452) are
│                       │       │                   nonce-misuse-resistant AEAD
│                       │       │                   modes: they accept a key, nonce, optional AAD (bytes that
│                       │       │                   are authenticated
│                       │       │                   but not encrypted), and plaintext, and produces ciphertext
│                       │       │                   plus a 16-byte
│                       │       │                   tag. On decrypt, `EVP_DecryptFinal_ex()` is documented to
│                       │       │                   return success only
│                       │       │                   if the tag is verified succesfully.
│                       │       │                   In OpenSSL's provider implementation of these ciphers, the
│                       │       │                   expected tag is
│                       │       │                   computed only when decryption function is invoked with
│                       │       │                   non-empty data.
│                       │       │                   If the caller supplies AAD and then calls
│                       │       │                   `EVP_DecryptFinal_ex()` without
│                       │       │                   invocation of the ciphertext update, which can happen when
│                       │       │                   the received
│                       │       │                   ciphertext length is zero, the tag is never recalculated
│                       │       │                   and still holds its
│                       │       │                   all-zeros value.
│                       │       │                   When AES-GCM-SIV is used, an attacker who sends arbitrary
│                       │       │                   AAD, empty
│                       │       │                   ciphertext, and all-zeros tag passes authentication under
│                       │       │                   any key they do not
│                       │       │                   know, single-shot. When AES-SIV is used, for mounting the
│                       │       │                   attack it's
│                       │       │                   necessary for the application to reuse the decryption
│                       │       │                   context without
│                       │       │                   resetting the key.
│                       │       │                   AES-SIV is implemented since OpenSSL 3.0. AES-GCM-SIV is
│                       │       │                   implemented since
│                       │       │                   OpenSSL 3.2.
│                       │       │                   No protocols implemented in OpenSSL itself
│                       │       │                   (TLS/CMS/PKCS7/HPKE/QUIC) support
│                       │       │                   either AES-GCM-SIV or AES-SIV. To mount an attack, the
│                       │       │                   applications must
│                       │       │                   implement their own protocol and use the EVP interface.
│                       │       │                   Also they must skip the
│                       │       │                   ciphertext update when a message with an empty ciphertext
│                       │       │                   arrives.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as these algorithms are not FIPS approved and the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/25b32cd9d41
│                       │       │                  │      d2bc01b6abc425bb4baf2c2236fdc 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/71e2a5d2635
│                       │       │                  │      18cf5866043bd60ee4994d59e53a3 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7fe3f33a3b3
│                       │       │                  │      a4c487aa4dcdbc87057f66ffd2b85 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/daca0f48e4a
│                       │       │                  │      69a2892a62262bad59e62a8a76598 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/eec5e9bf0d8
│                       │       │                  │      67333b8495e456f5235d225798a68 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-45446 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:19.137Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.733Z 
│                       ├ [40]  ╭ VulnerabilityID : CVE-2026-7383 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-7383 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:42fe51a91b1c1fb47c58db4f4bcf6cec9447108a6223243d9289
│                       │       │                   a21e3bf7d810 
│                       │       ├ Title           : Issue summary: A signed integer overflow when sizing the
│                       │       │                   destination b ... 
│                       │       ├ Description     : Issue summary: A signed integer overflow when sizing the
│                       │       │                   destination
│                       │       │                   buffer for Unicode output in ASN1_mbstring_ncopy() can lead
│                       │       │                    to a heap
│                       │       │                   buffer overflow.
│                       │       │                   
│                       │       │                   Impact summary: A heap buffer overflow may lead to a crash
│                       │       │                   or possibly
│                       │       │                   attacker controlled code execution or other undefined
│                       │       │                   behaviour.
│                       │       │                   In ASN1_mbstring_copy() and ASN1_mbstring_ncopy() the
│                       │       │                   size for Unicode output is computed in a signed int: by
│                       │       │                   left shift
│                       │       │                   of the input character count for BMPSTRING (UTF-16) and
│                       │       │                   UNIVERSALSTRING (UTF-32), and by summing per-character byte
│                       │       │                    counts
│                       │       │                   for UTF8STRING. The calculation overflows when the input
│                       │       │                   reaches
│                       │       │                   around 2^30 characters. In the worst case (UNIVERSALSTRING
│                       │       │                   at 2^30
│                       │       │                   characters) the size wraps to zero, OPENSSL_malloc(1) is
│                       │       │                   called, and
│                       │       │                   the subsequent character copy writes several gigabytes past
│                       │       │                    the
│                       │       │                   one-byte allocation.
│                       │       │                   X.509 certificate processing routes through
│                       │       │                   ASN1_STRING_set_by_NID(),
│                       │       │                   whose DIRSTRING_TYPE mask excludes UNIVERSALSTRING and
│                       │       │                   whose per-NID
│                       │       │                   size limits cap the input length; no network protocol or
│                       │       │                   certificate-handling path in OpenSSL exercises the
│                       │       │                   overflow.
│                       │       │                   Triggering the bug requires an application that calls
│                       │       │                   ASN1_mbstring_copy() or ASN1_mbstring_ncopy() directly, or
│                       │       │                   registers
│                       │       │                   a custom string type via ASN1_STRING_TABLE_add(), with
│                       │       │                   attacker-controlled input on the order of half a gigabyte
│                       │       │                   or more.
│                       │       │                   For these reasons this issue was assigned Low severity.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue, as the affected code is outside the OpenSSL
│                       │       │                   FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/4f8d2bddaa2
│                       │       │                  │      c8e06f9c33390ee1717059a6e4be6 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/80c15faaf78
│                       │       │                  │      042bbb8654a0e234c50c381732f74 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/bd17511070f
│                       │       │                  │      b39a67bfa19682affb765e706a974 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/c332adaced4
│                       │       │                  │      3bcbb85f97410597e951c11ec3083 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/d32350ae8ef
│                       │       │                  │      7426718f5aa9e383d4b51398ee255 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-7383 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:50.337Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:25.463Z 
│                       ├ [41]  ╭ VulnerabilityID : CVE-2026-9076 
│                       │       ├ PkgID           : libssl3t64@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : libssl3t64 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libssl3t64@3.5.3-1ubuntu3.3?arch=amd6
│                       │       │                  │       4&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : e5b53f5b1c6088b2 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9076 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:95358336f1660e54219420e6cee44a9c3f6cbc3d8fb9b45cddda
│                       │       │                   792c0c784238 
│                       │       ├ Title           : Issue summary: When CMS password-based decryption (RFC 3211
│                       │       │                    / PWRI key ... 
│                       │       ├ Description     : Issue summary: When CMS password-based decryption (RFC 3211
│                       │       │                    / PWRI key unwrap)
│                       │       │                   processes attacker-supplied CMS data, an attacker-chosen
│                       │       │                   stream-mode KEK
│                       │       │                   cipher can trigger a heap out-of-bounds read in
│                       │       │                   kek_unwrap_key().
│                       │       │                   
│                       │       │                   Impact summary: A heap buffer over-read may trigger a crash
│                       │       │                    which leads to
│                       │       │                   Denial of Service for an application if the input buffer
│                       │       │                   ends at a memory
│                       │       │                   page boundary and the following page is unmapped. There is
│                       │       │                   no information
│                       │       │                   disclosure as the over-read bytes are not revealed to the
│                       │       │                   attacker.
│                       │       │                   The key unwrapping function performs a check-byte test as
│                       │       │                   specified in the
│                       │       │                   RFC that reads 7 bytes from a heap allocation that is based
│                       │       │                    on the wrapped
│                       │       │                   key length from the message. There is a minimum length
│                       │       │                   check based on the
│                       │       │                   block length of the wrapping cipher. However the cipher is
│                       │       │                   selected from
│                       │       │                   an OID carried in the attacker's PWRI
│                       │       │                   keyEncryptionAlgorithm with no
│                       │       │                   requirement that the cipher be a block cipher. When an
│                       │       │                   attacker selects
│                       │       │                   a stream-mode cipher the guard will be ineffective and the
│                       │       │                   allocated buffer
│                       │       │                   containing the unwrapped key can be too small to fit the
│                       │       │                   check-bytes
│                       │       │                   specified in the RFC and a buffer over-read can happen.
│                       │       │                   Applications calling CMS_decrypt() or
│                       │       │                   CMS_decrypt_set1_password()
│                       │       │                   (equivalently openssl cms -decrypt -pwri_password ...) on
│                       │       │                   untrusted CMS
│                       │       │                   data are vulnerable to this issue. No password knowledge is
│                       │       │                    required: the
│                       │       │                   over-read happens during the unwrap attempt before any
│                       │       │                   authentication
│                       │       │                   succeeds.
│                       │       │                   The over-read is limited to a few bytes and is not written
│                       │       │                   to output, so
│                       │       │                   there is no information disclosure. Triggering a crash
│                       │       │                   requires the
│                       │       │                   allocation to border unmapped memory, which is unlikely
│                       │       │                   with the normal
│                       │       │                   allocator.
│                       │       │                   The FIPS modules are not affected by this issue. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/05b06636684
│                       │       │                  │      2f930fadd9a6e94df98030af431bb 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/3d8d5bc1056
│                       │       │                  │      b2f62da9fede23fedbf47e85187b0 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/715349a1d7c
│                       │       │                  │      6db970e6815dafb90915f07307f98 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/77bf00ab13f
│                       │       │                  │      6ff5e516535432f0328ed70ec0c26 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/eecbe330977
│                       │       │                  │      e8d023aae1ca2d9bdbe983ef3fdc6 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-9076 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:50.997Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:26.063Z 
│                       ├ [42]  ╭ VulnerabilityID : CVE-2026-40226 
│                       │       ├ PkgID           : libsystemd0@257.9-0ubuntu2.4 
│                       │       ├ PkgName         : libsystemd0 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@257.9-0ubuntu2.4?arch=amd
│                       │       │                  │       64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : b7d2a4bb150d8fb 
│                       │       ├ InstalledVersion: 257.9-0ubuntu2.4 
│                       │       ├ FixedVersion    : 257.9-0ubuntu2.5 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40226 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4f1aa3a0778a149306c6126ea06f500f264e2cd0a4667f6b5dff
│                       │       │                   bd788eb3f8f3 
│                       │       ├ Title           : systemd: systemd nspawn: Escape-to-host action via crafted
│                       │       │                   config file 
│                       │       ├ Description     : In nspawn in systemd 233 through 259 before 260, an
│                       │       │                   escape-to-host action can occur via a crafted optional
│                       │       │                   config file. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-348 
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:H/UI:N/S:U/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 6.4 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-40226 
│                       │       │                  ├ [1]: https://github.com/systemd/systemd/security/advisorie
│                       │       │                  │      s/GHSA-9mj4-rrc3-gjcx 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-40226 
│                       │       │                  ├ [3]: https://ubuntu.com/security/notices/USN-8402-1 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-40226 
│                       │       ├ PublishedDate   : 2026-04-10T16:16:33.447Z 
│                       │       ╰ LastModifiedDate: 2026-04-17T22:02:15.393Z 
│                       ├ [43]  ╭ VulnerabilityID : CVE-2026-40228 
│                       │       ├ PkgID           : libsystemd0@257.9-0ubuntu2.4 
│                       │       ├ PkgName         : libsystemd0 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@257.9-0ubuntu2.4?arch=amd
│                       │       │                  │       64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : b7d2a4bb150d8fb 
│                       │       ├ InstalledVersion: 257.9-0ubuntu2.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:72dc6f389b4320700e21bad65ad405f2c9784124ac8b4bc12e61
│                       │       │                   251fbc67cfc7 
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
│                       │       ╰ LastModifiedDate: 2026-05-05T02:16:04.82Z 
│                       ├ [44]  ╭ VulnerabilityID : CVE-2026-40226 
│                       │       ├ PkgID           : libudev1@257.9-0ubuntu2.4 
│                       │       ├ PkgName         : libudev1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@257.9-0ubuntu2.4?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 2df6338002659505 
│                       │       ├ InstalledVersion: 257.9-0ubuntu2.4 
│                       │       ├ FixedVersion    : 257.9-0ubuntu2.5 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40226 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4709a8c11fe21d7d28fe8ed90be05633414f1b45f77331b9df1f
│                       │       │                   37098f10bbcd 
│                       │       ├ Title           : systemd: systemd nspawn: Escape-to-host action via crafted
│                       │       │                   config file 
│                       │       ├ Description     : In nspawn in systemd 233 through 259 before 260, an
│                       │       │                   escape-to-host action can occur via a crafted optional
│                       │       │                   config file. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-348 
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:H/UI:N/S:U/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 6.4 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-40226 
│                       │       │                  ├ [1]: https://github.com/systemd/systemd/security/advisorie
│                       │       │                  │      s/GHSA-9mj4-rrc3-gjcx 
│                       │       │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-40226 
│                       │       │                  ├ [3]: https://ubuntu.com/security/notices/USN-8402-1 
│                       │       │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-40226 
│                       │       ├ PublishedDate   : 2026-04-10T16:16:33.447Z 
│                       │       ╰ LastModifiedDate: 2026-04-17T22:02:15.393Z 
│                       ├ [45]  ╭ VulnerabilityID : CVE-2026-40228 
│                       │       ├ PkgID           : libudev1@257.9-0ubuntu2.4 
│                       │       ├ PkgName         : libudev1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@257.9-0ubuntu2.4?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 2df6338002659505 
│                       │       ├ InstalledVersion: 257.9-0ubuntu2.4 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d9286db1722a28008b54c93261582b55a5313c4ffc67c310133e
│                       │       │                   a65cbef5577c 
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
│                       │       ╰ LastModifiedDate: 2026-05-05T02:16:04.82Z 
│                       ├ [46]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libuuid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 23db7c315eddf1f4 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:26ef4c5637e35e461ba61d2aefe85286963c4c910abfeb93faa6
│                       │       │                   65ed39e9b523 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [47]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : libuuid1 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 23db7c315eddf1f4 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:c2c488673661ae35e4d83492762dc8b26a6de617afadbc43e4eb
│                       │       │                   85ebf3cf056f 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [48]  ╭ VulnerabilityID : CVE-2026-1757 
│                       │       ├ PkgID           : libxml2-16@2.14.5+dfsg-0.2ubuntu0.1 
│                       │       ├ PkgName         : libxml2-16 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libxml2-16@2.14.5%2Bdfsg-0.2ubuntu0.1
│                       │       │                  │       ?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 31495ca6a00051cd 
│                       │       ├ InstalledVersion: 2.14.5+dfsg-0.2ubuntu0.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-1757 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:47a7802b40886337bdb02dd92a50b675ab60648b229a8b5a68a9
│                       │       │                   f2ef259b402b 
│                       │       ├ Title           : libxml2: Memory Leak Leading to Local Denial of Service in
│                       │       │                   xmllint Interactive Shell 
│                       │       ├ Description     : A flaw was identified in the interactive shell of the
│                       │       │                   xmllint utility, part of the libxml2 project, where memory
│                       │       │                   allocated for user input is not properly released under
│                       │       │                   certain conditions. When a user submits input consisting
│                       │       │                   only of whitespace, the program skips command execution but
│                       │       │                    fails to free the allocated buffer. Repeating this action
│                       │       │                   causes memory to continuously accumulate. Over time, this
│                       │       │                   can exhaust system memory and terminate the xmllint
│                       │       │                   process, creating a denial-of-service condition on the
│                       │       │                   local system. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-401 
│                       │       ├ VendorSeverity   ╭ amazon: 1 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 1 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           N/A:H 
│                       │       │                           ╰ V3Score : 6.2 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:7519 
│                       │       │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-1757 
│                       │       │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2435940 
│                       │       │                  ├ [3]: https://gitlab.gnome.org/GNOME/libxml2/-/issues/1009 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-1757 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-1757 
│                       │       ├ PublishedDate   : 2026-02-02T13:15:58.58Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T10:16:50.683Z 
│                       ├ [49]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:07a2a3a4c2ff2237918f994cd2e27a021ee5a9ac9f648d9fe93d
│                       │       │                   a395a332636b 
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
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20587 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2453117 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │       │                  ├ [4] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4046 
│                       │       │                  ├ [5] : https://errata.almalinux.org/8/ALSA-2026-20587.html 
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2026:20587 
│                       │       │                  ├ [7] : https://inbox.sourceware.org/libc-announce/76814edf-
│                       │       │                  │       cf7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │       │                  ├ [8] : https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │       │                  ├ [9] : https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │       │                  ├ [11]: https://packages.fedoraproject.org/pkgs/glibc/glibc-
│                       │       │                  │       gconv-extra/ 
│                       │       │                  ├ [12]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │       │                  ├ [13]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007 
│                       │       │                  ├ [14]: https://sourceware.org/git/?p=glibc.git;a=blob_plain
│                       │       │                  │       ;f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │       │                  ╰ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │       ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │       ╰ LastModifiedDate: 2026-04-20T22:16:23.623Z 
│                       ├ [50]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8a8a046319f9744ed16b69618bc37000b53679f6cfe4e2baba1f
│                       │       │                   b33221d95159 
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
│                       │       ├ VendorSeverity   ╭ alma  : 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ photon: 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ├ rocky : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:L 
│                       │       │                           ╰ V3Score : 6.5 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [8] : https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │       │                  ├ [9] : https://errata.rockylinux.org/RLSA-2026:19061 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │       │                  ├ [11]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │       │                  ├ [12]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │       │                  ╰ [13]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │       ╰ LastModifiedDate: 2026-04-07T18:41:36.647Z 
│                       ├ [51]  ╭ VulnerabilityID : CVE-2026-4438 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:677a16697d0635ed800fd7bf13c6aafb19c492a156eeeecf511e
│                       │       │                   a97a47d6af0a 
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
│                       │       ├ VendorSeverity   ╭ alma  : 2 
│                       │       │                  ├ azure : 2 
│                       │       │                  ├ photon: 2 
│                       │       │                  ├ redhat: 1 
│                       │       │                  ├ rocky : 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:
│                       │       │                           │           L/A:N 
│                       │       │                           ╰ V3Score : 4 
│                       │       ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:19061 
│                       │       │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │       │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │       │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │       │                  ├ [4] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │       │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │       │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4437 
│                       │       │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
│                       │       │                  │       026-4438 
│                       │       │                  ├ [8] : https://errata.almalinux.org/10/ALSA-2026-19061.html 
│                       │       │                  ├ [9] : https://errata.rockylinux.org/RLSA-2026:19061 
│                       │       │                  ├ [10]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │       │                  ├ [11]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │       │                  ├ [12]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │       │                  ╰ [13]: https://www.openwall.com/lists/oss-security/2026/03/
│                       │       │                          23/2 
│                       │       ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │       ╰ LastModifiedDate: 2026-04-07T18:40:02.177Z 
│                       ├ [52]  ╭ VulnerabilityID : CVE-2026-5435 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:736991c86d5f4f5172d3e2dd253c4ce04492b4fbcf9bea0191f5
│                       │       │                   5122064c3e40 
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
│                       │       ╰ LastModifiedDate: 2026-05-05T17:38:37.03Z 
│                       ├ [53]  ╭ VulnerabilityID : CVE-2026-6238 
│                       │       ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │       ├ PkgName         : locales 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : 217c1ce65d47a6c2 
│                       │       ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:364572a3469217bddb7b5ce15616f6ec4fbd2880c31ba1ceb836
│                       │       │                   3bc90eec99da 
│                       │       ├ Title           : glibc: glibc: Application crash or uninitialized memory
│                       │       │                   read via crafted DNS response 
│                       │       ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │       │                   fp_nquery in the GNU C Library version 2.2 and newer fail
│                       │       │                   to validate the RDATA content against the RDATA length in a
│                       │       │                    DNS response when processing LOC, CERT, TKEY or TSIG
│                       │       │                   records, which may allow an attacker to craft a DNS
│                       │       │                   response, causing a target application to crash or read
│                       │       │                   uninitialized memory.
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
│                       │       ╰ LastModifiedDate: 2026-05-04T17:57:24.007Z 
│                       ├ [54]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ PkgName         : login 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.
│                       │       │                  │       2?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │       ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a017856f6821c90da18149c8b7a3c4599bbd4aded0b670cab4aa
│                       │       │                   ed14955d78c6 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [55]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ PkgName         : login 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.
│                       │       │                  │       2?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │       ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f86157191ea329208aa2bf271e9f1492fc247e92ad7af3d26145
│                       │       │                   492dabcad89a 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [56]  ╭ VulnerabilityID : CVE-2024-56433 
│                       │       ├ PkgID           : login.defs@1:4.17.4-2ubuntu2 
│                       │       ├ PkgName         : login.defs 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu2?arch=all&d
│                       │       │                  │       istro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 685157e74dbd875c 
│                       │       ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:add6b17dbbb8c4243bf00ae4aeaec75d3c3c5344da2163ef146e
│                       │       │                   9f4f728d3a81 
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
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20145 
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
│                       │       ╰ LastModifiedDate: 2026-04-15T00:35:42.02Z 
│                       ├ [57]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : mount 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : f2821a9fde7aa805 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2a5682a74938cf21126276b20e43f1bd8ce1440e57872c5a600f
│                       │       │                   1a39f6f0915b 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [58]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : mount 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&dist
│                       │       │                  │       ro=ubuntu-25.10 
│                       │       │                  ╰ UID : f2821a9fde7aa805 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a78da953d3baa883247fad2b5a9373892aceea28308477e86239
│                       │       │                   a1111b22cccb 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [59]  ╭ VulnerabilityID : CVE-2026-45447 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45447 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ddb8da89f6a21fe2f89dcc52be883ed5d51d1e7d40fd6fcb6762
│                       │       │                   b2596c517190 
│                       │       ├ Title           : Issue summary: A specially crafted PKCS#7 or S/MIME signed
│                       │       │                   message cou ... 
│                       │       ├ Description     : Issue summary: A specially crafted PKCS#7 or S/MIME signed
│                       │       │                   message could
│                       │       │                   trigger a use-after-free during PKCS#7 signature
│                       │       │                   verification.
│                       │       │                   
│                       │       │                   Impact summary: A use-after-free may result in process
│                       │       │                   crashes, heap
│                       │       │                   corruption, or potentially remote code execution.
│                       │       │                   When processing a PKCS#7 or S/MIME signed message, if the
│                       │       │                   SignedData
│                       │       │                   digestAlgorithms field is present as an empty ASN.1 SET,
│                       │       │                   OpenSSL may
│                       │       │                   incorrectly free a caller-owned BIO during PKCS7_verify().
│                       │       │                   A subsequent
│                       │       │                   use of the BIO by the calling application results in a
│                       │       │                   use-after-free
│                       │       │                   condition.
│                       │       │                   In the common case this occurs when the application later
│                       │       │                   calls
│                       │       │                   BIO_free() on the BIO originally passed to PKCS7_verify().
│                       │       │                   Depending
│                       │       │                   on allocator behavior and application-specific BIO usage
│                       │       │                   patterns, this
│                       │       │                   may result in a crash or other memory corruption. In some
│                       │       │                   application
│                       │       │                   contexts this may potentially be exploitable for remote
│                       │       │                   code execution.
│                       │       │                   Applications that process PKCS#7 or S/MIME signed messages
│                       │       │                   using OpenSSL
│                       │       │                   PKCS#7 APIs may be affected. Applications using the CMS
│                       │       │                   APIs for this
│                       │       │                   processing are not affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : HIGH 
│                       │       ├ CweIDs           ─ [0]: CWE-416 
│                       │       ├ VendorSeverity   ─ ubuntu: 3 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/3aad5eb7af4
│                       │       │                  │      de4ee0633c30a8541a54d9bbde63c 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/7d4a980c622
│                       │       │                  │      58c5910cc883936e0c8dbab4d75a8 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/9dfd688ad22
│                       │       │                  │      90fc5075cacbc9bf0c9a93eefed54 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/a541ae8bfe8
│                       │       │                  │      49a30cc885e8780715c0f488e496c 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/c505d7559da
│                       │       │                  │      5d5f9f2c3913c6883a5562ce7273e 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-45447 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:19.277Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T15:16:35.16Z 
│                       ├ [60]  ╭ VulnerabilityID : CVE-2026-34182 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34182 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:4c518106b8ff1669310fcafff05d316affac1aa66d1fbf1b1e0e
│                       │       │                   819f68877677 
│                       │       ├ Title           : Issue Summary: Cryptographic Message Services (CMS)
│                       │       │                   processing fails t ... 
│                       │       ├ Description     : Issue Summary: Cryptographic Message Services (CMS)
│                       │       │                   processing fails to perform
│                       │       │                   sufficient input validation on the cipher and tag length
│                       │       │                   fields of
│                       │       │                   AuthEnvelopedData containers, leading to various potential
│                       │       │                   compromises.
│                       │       │                   
│                       │       │                   Impact Summary: Attackers making use of these
│                       │       │                   vulnerabilities may achieve
│                       │       │                   key-equivalent functionality for a given CMS recipient
│                       │       │                   and/or bypass integrity
│                       │       │                   validation for a given message.
│                       │       │                   In one use case, an attacker may send a CMS message
│                       │       │                   containing
│                       │       │                   AuthEnvelopedData with the cipher specified as a non-AEAD
│                       │       │                   cipher.  OpenSSL
│                       │       │                   erroneously allows this selection, and attempts to decrypt
│                       │       │                   and validate the
│                       │       │                   message.
│                       │       │                   An on-path attacker who captures one legitimate AES-GCM
│                       │       │                   AuthEnvelopedData
│                       │       │                   addressed to the victim can re-emit it with the
│                       │       │                   recipientInfos set left
│                       │       │                   byte-for-byte intact, so the victim's private key still
│                       │       │                   unwraps the genuine CEK
│                       │       │                   (the content-encryption key), but with the inner OID
│                       │       │                   rewritten to AES-256-OFB
│                       │       │                   (Output Feedback Mode, an unauthenticated keystream mode)
│                       │       │                   and with an
│                       │       │                   attacker-chosen IV and ciphertext. The victim initializes
│                       │       │                   AES-256-OFB under the
│                       │       │                   real CEK, never consults the MAC field, and CMS_decrypt()
│                       │       │                   returns success.
│                       │       │                   If the application under attack responds to the attacker
│                       │       │                   with any indicator
│                       │       │                   showing success or failure of the decryption effort, it is
│                       │       │                   possible for the
│                       │       │                   attacker to use this as an oracle to obtain key equivalent
│                       │       │                   functionality for the
│                       │       │                   CEK used for the chosen recipient of the message.
│                       │       │                   In another use case, an attacker can reduce the tag length
│                       │       │                   of the chosen AEAD
│                       │       │                   cipher for a given AuthEnvelopedData container to be a
│                       │       │                   single byte long,
│                       │       │                   allowing an attacker to brute force CMS decryption,
│                       │       │                   producing an integrity
│                       │       │                   bypass for applications that trust CMS_decrypt() to reject
│                       │       │                   modified content.
│                       │       │                   The FIPS modules are not affected by this issue. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-354 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/03c1f4d45fb
│                       │       │                  │      963aee7d5833390c507cd290182bc 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/439ed7d2c09
│                       │       │                  │      62ce964482727264668bf277c333f 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7947e6a81eb
│                       │       │                  │      8776802f159fb6762cb7fcf7e34c7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/9fd97f8cfdc
│                       │       │                  │      2c0be214998de3b2b55c8edf6c7ac 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/d2ca86bcd43
│                       │       │                  │      e4f17d899f347101766b6107676e0 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34182 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.857Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T17:16:32.48Z 
│                       ├ [61]  ╭ VulnerabilityID : CVE-2026-34183 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34183 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8d932a048ff86398a5b4909a2cbdfe6eaad810cc5129e59f39a4
│                       │       │                   3de2b0d93e7c 
│                       │       ├ Title           : Issue summary: Remote peer may exhaust heap memory of the
│                       │       │                   QUIC server  ... 
│                       │       ├ Description     : Issue summary: Remote peer may exhaust heap memory of the
│                       │       │                   QUIC
│                       │       │                   server or client by flooding it with packets containing
│                       │       │                   PATH_CHALLENGE
│                       │       │                   frames.
│                       │       │                   
│                       │       │                   Impact summary: A malicious remote peer can cause an
│                       │       │                   unbounded
│                       │       │                   memory allocation which can lead to an abnormal termination
│                       │       │                    of the
│                       │       │                   application acting as a QUIC client or server and a Denial
│                       │       │                   of Service.
│                       │       │                   A remote peer may exhaust heap memory by flooding the
│                       │       │                   local
│                       │       │                   QUIC stack with PATH_CHALLENGE frames. The local QUIC
│                       │       │                   stack
│                       │       │                   allocates a PATH_RESPONSE frame for every PATH_CHALLENGE it
│                       │       │                    receives.
│                       │       │                   The allocated PATH_RESPONSE frame gets freed only when the
│                       │       │                   remote
│                       │       │                   peer acknowledges reception of the PATH_RESPONSE frame
│                       │       │                   which will
│                       │       │                   not be done by a malicious peer.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue. The QUIC stack is outside of OpenSSL FIPS
│                       │       │                   module
│                       │       │                   boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-1325 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/5b306efb0b3
│                       │       │                  │      779dfdd0803b4afc9d08c91f11517 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/7d06955ebe0
│                       │       │                  │      ecf8adfd4c1e92018586da47ef9ac 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d2e9efbe490
│                       │       │                  │      0a373227deb136e8665401404ffac 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/fbaa83859c0
│                       │       │                  │      1ad64f497b757aaf51be7d05ed9eb 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-34183 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:05Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T16:17:01.217Z 
│                       ├ [62]  ╭ VulnerabilityID : CVE-2026-42764 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42764 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d98bd7922277ee470f6c409e951758d1be27e0614a711376e8a6
│                       │       │                   3ba775ce49e7 
│                       │       ├ Title           : Issue summary: Receiving a QUIC initial packet with an
│                       │       │                   invalid token m ... 
│                       │       ├ Description     : Issue summary: Receiving a QUIC initial packet with an
│                       │       │                   invalid token may
│                       │       │                   trigger a NULL pointer dereference in the OpenSSL QUIC
│                       │       │                   server with
│                       │       │                   address validation disabled.
│                       │       │                   
│                       │       │                   Impact summary: NULL pointer dereference typically causes
│                       │       │                   abnormal termination
│                       │       │                   of the affected QUIC server process and a Denial of
│                       │       │                   Service.
│                       │       │                   If the address validation is disabled in the OpenSSL QUIC
│                       │       │                   server
│                       │       │                   implementation, an attacker can crash the server by sending
│                       │       │                    an initial
│                       │       │                   packet with an invalid or expired token.
│                       │       │                   By default, the client address validation is enabled in the
│                       │       │                    OpenSSL QUIC server
│                       │       │                   implementation, which makes the default configuration not
│                       │       │                   vulnerable
│                       │       │                   to this issue. However if the SSL_LISTENER_FLAG_NO_VALIDATE
│                       │       │                    is used with
│                       │       │                   the SSL_new_listener() call, the address validation is
│                       │       │                   disabled making the
│                       │       │                   vulnerable code reachable.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/5e3ed291b8a
│                       │       │                  │      f0b03d5d3b9e56a1da69a187e9729 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/a45a0aba809
│                       │       │                  │      5682c88ff4fc4a784892b8c6f0677 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/bf29a458c1a
│                       │       │                  │      231eca87e384c62b9c2553fa57a91 
│                       │       │                  ├ [3]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-42764 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:07.693Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.23Z 
│                       ├ [63]  ╭ VulnerabilityID : CVE-2026-45445 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45445 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:993e7453671859bfc1f5da9ead857b40c11c97cd089ec2a0be0e
│                       │       │                   fe94ebe21011 
│                       │       ├ Title           : Issue summary: When an application drives an AES-OCB
│                       │       │                   context through t ... 
│                       │       ├ Description     : Issue summary: When an application drives an AES-OCB
│                       │       │                   context through the
│                       │       │                   public EVP_Cipher() one-shot interface, the
│                       │       │                   application-supplied
│                       │       │                   initialisation vector (IV) is silently discarded.
│                       │       │                   
│                       │       │                   Impact summary: Every message encrypted under the same key
│                       │       │                   uses the
│                       │       │                   same effective nonce regardless of the IV supplied by the
│                       │       │                   caller,
│                       │       │                   resulting in (key, nonce) reuse and loss of
│                       │       │                   confidentiality.  If the
│                       │       │                   same code path is used to compute the authentication tag,
│                       │       │                   the tag
│                       │       │                   depends only on the (key, IV) pair and not on the plaintext
│                       │       │                    or
│                       │       │                   ciphertext, allowing universal forgery of arbitrary
│                       │       │                   ciphertext from a
│                       │       │                   single captured message.
│                       │       │                   OpenSSL provides two ways to drive a cipher: the documented
│                       │       │                    streaming
│                       │       │                   interface (EVP_CipherUpdate / EVP_CipherFinal_ex) and a
│                       │       │                   lower-level
│                       │       │                   one-shot, EVP_Cipher(), whose documentation explicitly
│                       │       │                   recommends
│                       │       │                   against use by applications in favour of EVP_CipherUpdate()
│                       │       │                    and
│                       │       │                   EVP_CipherFinal_ex().  The OCB provider's streaming handler
│                       │       │                    flushes
│                       │       │                   the application-supplied IV into the OCB context before
│                       │       │                   processing
│                       │       │                   data; the one-shot handler did not.  Every call to
│                       │       │                   EVP_Cipher() on an
│                       │       │                   AES-OCB context therefore ran with the all-zero key-derived
│                       │       │                    offset
│                       │       │                   state left by cipher initialisation, regardless of the
│                       │       │                   caller's IV.
│                       │       │                   If EVP_EncryptFinal_ex() is subsequently used to obtain
│                       │       │                   the
│                       │       │                   authentication tag, the deferred IV setup runs at that
│                       │       │                   point and
│                       │       │                   clears the running checksum that should have been
│                       │       │                   accumulated over the
│                       │       │                   plaintext.  The resulting tag is a function of (key, IV)
│                       │       │                   only and
│                       │       │                   verifies against any ciphertext produced under the same
│                       │       │                   (key, IV)
│                       │       │                   pair.
│                       │       │                   The OpenSSL SSL/TLS implementation is not affected: AES-OCB
│                       │       │                    is not a
│                       │       │                   TLS cipher suite, and libssl does not call EVP_Cipher() in
│                       │       │                   any case.
│                       │       │                   Applications that drive AES-OCB through the documented
│                       │       │                   streaming AEAD
│                       │       │                   API (EVP_CipherUpdate / EVP_CipherFinal_ex) are not
│                       │       │                   affected.  Only
│                       │       │                   applications that combine the AES-OCB cipher with the
│                       │       │                   EVP_Cipher()
│                       │       │                   one-shot API are vulnerable.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue, as AES-OCB is outside the OpenSSL FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/323f0b6e7d5
│                       │       │                  │      30a4cb4336d50c88cb70f3ac2a451 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/787a6dfba81
│                       │       │                  │      b7b09c1e05ab31396c0cd7c36b3f7 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7ac4715234e
│                       │       │                  │      e72d9f3c93426a2c08554b5b771af 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/843c9b94ca9
│                       │       │                  │      c2ed248bb30127bb4f3d7af0d607c 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/983d54b5cce
│                       │       │                  │      8d16147548ed1a37892d1720bbab6 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-45445 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:18.993Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.507Z 
│                       ├ [64]  ╭ VulnerabilityID : CVE-2026-34180 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34180 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:957fac91c189fc1ad8f118c5005d154988cbdaffc912d2563f24
│                       │       │                   de0145633913 
│                       │       ├ Title           : Issue summary: Parsing a crafted DER-encoded ASN.1
│                       │       │                   structure with a pr ... 
│                       │       ├ Description     : Issue summary: Parsing a crafted DER-encoded ASN.1
│                       │       │                   structure with a primitive
│                       │       │                   element whose content exceeds 2 gigabytes in length may
│                       │       │                   cause a heap buffer
│                       │       │                   over-read on 64-bit Unix and Unix-like platforms.
│                       │       │                   
│                       │       │                   Impact summary: The heap buffer over-read may crash the
│                       │       │                   application (Denial of
│                       │       │                   Service) or to load into the decoded ASN.1 object contents
│                       │       │                   of memory beyond the
│                       │       │                   end of the input buffer.  More typically such ASN.1
│                       │       │                   elements would instead be
│                       │       │                   truncated.
│                       │       │                   An integer truncation in OpenSSL's ASN.1 decoder causes the
│                       │       │                    content length of
│                       │       │                   an ASN.1 primitive element to be mishandled when it exceeds
│                       │       │                    2 gigabytes. In the
│                       │       │                   worst case the truncated length is treated as a request to
│                       │       │                   scan the binary
│                       │       │                   content for a terminating zero byte, possibly causing
│                       │       │                   OpenSSL to read either
│                       │       │                   less than or beyond the end of the allocated buffer.
│                       │       │                   Applications that pass attacker-supplied data to
│                       │       │                   d2i_X509(), d2i_PKCS7(), or
│                       │       │                   any other d2i_* decoding function are affected. OpenSSL's
│                       │       │                   own command-line
│                       │       │                   tools are not vulnerable, as data read through the BIO
│                       │       │                   layer is checked before
│                       │       │                   it reaches the affected code. The issue only affects 64-bit
│                       │       │                    Unix and Unix-like
│                       │       │                   platforms; 32-bit platforms and 64-bit Windows are not
│                       │       │                   affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by this issue,
│                       │       │                   as the affected code is outside the OpenSSL FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/1c6908e4fa5
│                       │       │                  │      fa568752221d8eaf561a809751e5d 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/cbe418ae978
│                       │       │                  │      539cf14a398a207dba834c0e93e83 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d93853c4211
│                       │       │                  │      0d6319e3df07842b488cb9f7ac5ff 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/da5d62af75f
│                       │       │                  │      69d6fbf7803743d7c56ac75461e43 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/f696c73c3e6
│                       │       │                  │      1b8c502d040af62e690c060908a16 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34180 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.6Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:22.627Z 
│                       ├ [65]  ╭ VulnerabilityID : CVE-2026-34181 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34181 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d6f072ba3de8c8705b3441a63769ff464748e361673ea7ed8a46
│                       │       │                   39df3c19e61c 
│                       │       ├ Title           : Issue Summary: The PKCS#12 file processing fails to perform
│                       │       │                    sufficient ... 
│                       │       ├ Description     : Issue Summary: The PKCS#12 file processing fails to perform
│                       │       │                    sufficient input
│                       │       │                   validation for files that use Password-Based Message
│                       │       │                   Authentication Code 1
│                       │       │                   (PBMAC1) integrity mechanism allowing a certificate and
│                       │       │                   private key forgery.
│                       │       │                   
│                       │       │                   Impact Summary: An attacker impersonating a user can cause
│                       │       │                   a service reading
│                       │       │                   PKCS#12 files to accept forged certificates and private
│                       │       │                   keys with a 1 in 256
│                       │       │                   probability.
│                       │       │                   If a service accepting PKCS#12 files is using passwords for
│                       │       │                    authenticating
│                       │       │                   the received files, the attacker can create unencrypted
│                       │       │                   PKCS#12 files that
│                       │       │                   use PBMAC1 authentication that specifies an HMAC key of
│                       │       │                   only one byte, allowing
│                       │       │                   them to craft a file that will be accepted with a 1 in 256
│                       │       │                   That would then cause the service to accept a certificate
│                       │       │                   and private key
│                       │       │                   controlled by the attacker.
│                       │       │                   The FIPS modules are not affected by this issue, as the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-354 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/0300eb9ddce
│                       │       │                  │      7a0895bf301a4b0c03a9da2313a0f 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/79eb76a937e
│                       │       │                  │      474bb7610a0a3dc57131dc8dc6610 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/85dcbb3abaa
│                       │       │                  │      4878af5c8fbbe11bce708fcf984a7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/ec36f2417c4
│                       │       │                  │      ddd8cabce4b4a60a3d7a7365f2d81 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-34181 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.74Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T17:16:32.29Z 
│                       ├ [66]  ╭ VulnerabilityID : CVE-2026-42766 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42766 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:af2e67c584d661e357d6d405682487987c878aa47987bfee4d3b
│                       │       │                   efdb0409fc21 
│                       │       ├ Title           : Issue summary: A specially crafted password-encrypted CMS
│                       │       │                   message can  ... 
│                       │       ├ Description     : Issue summary: A specially crafted password-encrypted CMS
│                       │       │                   message
│                       │       │                   can trigger a NULL pointer dereference during CMS
│                       │       │                   decryption.
│                       │       │                   
│                       │       │                   Impact summary: This NULL pointer dereference leads to an
│                       │       │                   application crash
│                       │       │                   and a Denial of Service.
│                       │       │                   The CMS PasswordRecipientInfo.keyDerivationAlgorithm field
│                       │       │                   is defined as
│                       │       │                   OPTIONAL in the ASN.1 specification and may therefore be
│                       │       │                   absent in specially
│                       │       │                   crafted inputs. During the password-based CMS decryption
│                       │       │                   the OpenSSL
│                       │       │                   CMS implementation dereferences this field without first
│                       │       │                   checking whether it
│                       │       │                   was present.
│                       │       │                   An attacker who supplies such a CMS message to an
│                       │       │                   application performing
│                       │       │                   password-based CMS decryption can trigger an application
│                       │       │                   crash, leading to
│                       │       │                   a Denial of Service.
│                       │       │                   Applications that process password-encrypted CMS messages
│                       │       │                   may be affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/056d06c1918
│                       │       │                  │      fafbb98c1c85a02e4c47cc4e199ce 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/12bc26ffb3a
│                       │       │                  │      2be728c9b86e1cae277de5b33dfa4 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/3ff64913615
│                       │       │                  │      d648cfbb6a6f1cf5529ae7ea829d7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/ab52d88cb53
│                       │       │                  │      74876d59aee3c91f9e4ccce2b7ce4 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/da26f368732
│                       │       │                  │      b83e40e9d356fe61c3d3aaab6d2e8 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-42766 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:07.97Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.52Z 
│                       ├ [67]  ╭ VulnerabilityID : CVE-2026-42767 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42767 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:711a4ff01a550d77cb2f559450fe68573b06c1a0915ede557d63
│                       │       │                   dda2c8d7cde5 
│                       │       ├ Title           : Issue summary: An attacker-controlled CMP (Certificate
│                       │       │                   Management Prot ... 
│                       │       ├ Description     : Issue summary: An attacker-controlled CMP (Certificate
│                       │       │                   Management Protocol)
│                       │       │                   server could trigger a NULL pointer dereference in a CMP
│                       │       │                   client application.
│                       │       │                   
│                       │       │                   Impact summary: A NULL pointer dereference causes a crash
│                       │       │                   of the
│                       │       │                   application and a Denial of Service.
│                       │       │                   An attacker controlling a CMP server (or acting as a
│                       │       │                   man-in-the-middle) could
│                       │       │                   craft a CMP response containing a CRMF (Certificate Request
│                       │       │                    Message Format)
│                       │       │                   CertRepMessage with an EncryptedValue structure where the
│                       │       │                   symmAlg field
│                       │       │                   has an algorithm OID but no parameters field. When the
│                       │       │                   OpenSSL CMP client
│                       │       │                   processes this response, the NULL dereference occurs,
│                       │       │                   causing a crash of
│                       │       │                   the CMP client.
│                       │       │                   Applications that process untrusted CMP/CRMF messages may
│                       │       │                   be affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/61a86a8cd73
│                       │       │                  │      546c9fea916f3d304c1293e05c046 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/665d5254083
│                       │       │                  │      affde9982efca7c41dd01cacc8774 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/810b722f772
│                       │       │                  │      652ad48042bcc7ab07e3414b11d0f 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/b90ff3b1bd3
│                       │       │                  │      3b1c18e6a09936d097c2eddef8873 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/e6f912907fc
│                       │       │                  │      2ec82a0fd07aae55172c5e5e3d90d 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-42767 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.093Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.683Z 
│                       ├ [68]  ╭ VulnerabilityID : CVE-2026-42768 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42768 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a07fcbb109522f4fc5ce0bee1a3242ee0eac619a3962a124f923
│                       │       │                   4e9fe9feb9d3 
│                       │       ├ Title           : Issue summary: The CMS_decrypt and PKCS7_decrypt functions
│                       │       │                   are vulnera ... 
│                       │       ├ Description     : Issue summary: The CMS_decrypt and PKCS7_decrypt functions
│                       │       │                   are vulnerable to
│                       │       │                   Bleichenbacher-style attack when an attacker is able to
│                       │       │                   provide the CMS or
│                       │       │                   S/MIME messages and observe the error code and/or
│                       │       │                   decryption output.
│                       │       │                   
│                       │       │                   Impact summary: The Bleichenbacher-style attack allows an
│                       │       │                   attacker to use the
│                       │       │                   victim's vulnerable application as a way to decrypt or sign
│                       │       │                    messages with the
│                       │       │                   victim's private RSA key.
│                       │       │                   The attack is possible in 2 variants.
│                       │       │                   1. The decryption API (CMS_decrypt(), PKCS7_decrypt()) is
│                       │       │                   used without
│                       │       │                   providing the recipient certificate. In this case OpenSSL
│                       │       │                   iterates over every
│                       │       │                   KeyTransRecipientInfo (KTRI) without stopping at the first
│                       │       │                   success.
│                       │       │                   An attacker who authors a message with two KTRI entries —
│                       │       │                   the first one
│                       │       │                   wrapping a real CEK under the victim's public key, the
│                       │       │                   second with an
│                       │       │                   arbitrary probe ciphertext — obtains opportunity to iterate
│                       │       │                    the 2nd KTRI to
│                       │       │                   get a valid PKCS#1 v1.5 padding if the error code of the
│                       │       │                   application is
│                       │       │                   available.
│                       │       │                   That is a Bleichenbacher oracle (Bleichenbacher, CRYPTO
│                       │       │                   '98): an
│                       │       │                   adaptive-chosen-ciphertext side channel from which the
│                       │       │                   attacker decrypts any
│                       │       │                   RSA ciphertext to the victim's key or forges any PKCS#1
│                       │       │                   v1.5 signature under
│                       │       │                   it.
│                       │       │                   2. When the decryption API (CMS_decrypt(), PKCS7_decrypt())
│                       │       │                    is provided with
│                       │       │                   the recipient certificate, and the recipient is not found,
│                       │       │                   a random
│                       │       │                   key is substituted.
│                       │       │                   An attacker who authors a message and is able to compare
│                       │       │                   both error code and
│                       │       │                   the result of the decryption, can mount a Bleichenbacher
│                       │       │                   oracle.
│                       │       │                   We are not aware of any applications that provide a remote
│                       │       │                   attacker
│                       │       │                   an opportunity to mount an attack described in these
│                       │       │                   scenarios. We consider
│                       │       │                   the existence of such application very unlikely, and for
│                       │       │                   this reason this
│                       │       │                   CVE has been evaluated as Low severity.
│                       │       │                   To avoid these attacks, when RSA PKCS#1 v1.5 Key Transport
│                       │       │                   is in use, the
│                       │       │                   invoked EVP_PKEY_decrypt() will use the implicit rejection
│                       │       │                   mechanism described
│                       │       │                   in draft-irtf-cfrg-rsa-guidance. In previous OpenSSL
│                       │       │                   releases the implicit
│                       │       │                   rejection was explicitly disabled.
│                       │       │                   The implicit rejection mechanism always returns a plaintext
│                       │       │                    value,
│                       │       │                   the symmetric key. This result is deterministic for the
│                       │       │                   ciphertext and the
│                       │       │                   private key.  The length of the decryption result can
│                       │       │                   happen to match the
│                       │       │                   length of the key of the symmetric cipher that was used for
│                       │       │                    the content
│                       │       │                   encryption. When a certificate is not provided, the last
│                       │       │                   RecipientInfo
│                       │       │                   producing a key that looks valid will be used. It may cause
│                       │       │                    getting garbage
│                       │       │                   content on decryption. As a proper way to deal with this a
│                       │       │                   recipient
│                       │       │                   certificate has to be provided to identify the particular
│                       │       │                   RecipientInfo for
│                       │       │                   decryption.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, and 3.4 are not affected
│                       │       │                    by this issue, as
│                       │       │                   CMS and S/MIME processing happens outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-514 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/a2ca7b2d73e
│                       │       │                  │      0ffc1eae183fe6e1741dac767cb4f 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/bbb151a8304
│                       │       │                  │      1705d9d001ed2f9c12f5523e1b54d 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/dd68364107a
│                       │       │                  │      58841c0a2546812518b65d3a23abd 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/f04b377be3d
│                       │       │                  │      821741c86d1f4bf84dee09f3d5c3e 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42768 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.223Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.84Z 
│                       ├ [69]  ╭ VulnerabilityID : CVE-2026-42769 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42769 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:cd68d0237d210d7a1db41ed16cba93d4f489346185875cedbb4a
│                       │       │                   3bacddf17f7a 
│                       │       ├ Title           : Issue Summary: An error in the callback used to verify the
│                       │       │                   certificate ... 
│                       │       ├ Description     : Issue Summary: An error in the callback used to verify the
│                       │       │                   certificate
│                       │       │                   provided in a Root CA key update Certificate Management
│                       │       │                   Protocol (CMP)
│                       │       │                   message response rendered the certificate validation
│                       │       │                   ineffectual, which
│                       │       │                   could lead to escalation of credentials from the
│                       │       │                   Registration Authority (RA)
│                       │       │                   level to the root Certification Authority (root CA) level.
│                       │       │                   
│                       │       │                   Impact Summary: The Registration Autority could replace the
│                       │       │                    root CA
│                       │       │                   certificate for the CMP clients with an arbitrary root CA
│                       │       │                   certificate.
│                       │       │                   One of the parts of the Certificate Management Protocol
│                       │       │                   (CMP), specified in
│                       │       │                   RFC 9810, is Root Certification Authority (root CA) key
│                       │       │                   Rollover,
│                       │       │                   which is sent by the server in a message with type
│                       │       │                   'id-it-rootCaKeyUpdate'.
│                       │       │                   As part of these messages, 'newWithOld' certificate, the
│                       │       │                   new root CA
│                       │       │                   certificate signed with the old root CA key, is provided,
│                       │       │                   and verifying its
│                       │       │                   signature is crucial for transferring the trust from the
│                       │       │                   old CA key to the
│                       │       │                   new one.
│                       │       │                   The 'id-it-rootCaKeyUpdate' messages are expected to be
│                       │       │                   processed with
│                       │       │                   OSSL_CMP_get1_rootCaKeyUpdate(), that is expected to verify
│                       │       │                    the 'newWithOld'
│                       │       │                   certificate.  A typo in the certificate chain building code
│                       │       │                    led to adding
│                       │       │                   an incorrect certificate ('newWithOld' instead of
│                       │       │                   'oldRoot') to the
│                       │       │                   certificate chain, rendering the certificate verification
│                       │       │                   process ineffectual
│                       │       │                   (only the issuer name and the algorithm OIDs were verified
│                       │       │                   by other parts
│                       │       │                   of the verification code).
│                       │       │                   An attacker who already has credentials that satisfy the
│                       │       │                   CMP message
│                       │       │                   protection checks can generate a new key pair and use a
│                       │       │                   crafted self-signed
│                       │       │                   certificate in its 'id-it-rootCaKeyUpdate' CMP messages
│                       │       │                   which affected CMP
│                       │       │                   clients would accept as a new trust anchor.
│                       │       │                   Significant preconditions for the attack (having valid
│                       │       │                   RA-level credentials)
│                       │       │                   are the reason the issue was assigned Low severity.
│                       │       │                   The FIPS modules are not affected by this issue, as the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-295 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/54d0989997e
│                       │       │                  │      5fc26057009a9782c3441ce3842fb 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/777b363b16f
│                       │       │                  │      cf2153bb3ded39dc3838713667c44 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d35cd473a27
│                       │       │                  │      1bf3ce7bf3d32af53217fb83ae92c 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/d531f21c0fe
│                       │       │                  │      99067a66fc0ff1161ef127f9cd70b 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42769 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.027Z 
│                       ├ [70]  ╭ VulnerabilityID : CVE-2026-42770 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42770 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b692503fe21986fc674b731356813a3a726404842acc44dcaa1e
│                       │       │                   46545fde831b 
│                       │       ├ Title           : Issue summary: When EVP_PKEY_derive_set_peer() is called
│                       │       │                   with a DHX (X ... 
│                       │       ├ Description     : Issue summary: When EVP_PKEY_derive_set_peer() is called
│                       │       │                   with a DHX (X9.42)
│                       │       │                   peer key, the peer key is not properly checked for the
│                       │       │                   subgroup membership.
│                       │       │                   
│                       │       │                   Impact summary: A malicious peer which presents an X9.42
│                       │       │                   key carrying the
│                       │       │                   victim's p and g parameters, a forged q = r (a small prime
│                       │       │                   factor of the
│                       │       │                   cofactor (p−1)/q_local), and a public value Y of order r
│                       │       │                   can recover the
│                       │       │                   victim's private key after a small number of key exchange
│                       │       │                   attempts.
│                       │       │                   When EVP_PKEY_derive_set_peer() is called with a DHX
│                       │       │                   (X9.42) peer key, the
│                       │       │                   subgroup membership check Y^q ≡ 1 (mod p) is performed
│                       │       │                   using the peer's
│                       │       │                   own q parameter, not the local key's q. The peer's domain
│                       │       │                   parameters are
│                       │       │                   then matched against the domain parameters of the private
│                       │       │                   key, but the value
│                       │       │                   of q is not compared.
│                       │       │                   A malicious peer who presents an X9.42 key carrying the
│                       │       │                   victim's p, g,
│                       │       │                   a forged q = r (a small prime factor of the cofactor), and
│                       │       │                   a public
│                       │       │                   value Y of order r passes all checks. The shared secret
│                       │       │                   then takes only
│                       │       │                   r distinct values, leaking priv mod r. Repeating for each
│                       │       │                   small-prime
│                       │       │                   factor of the cofactor and combining via CRT recovers the
│                       │       │                   full private
│                       │       │                   key (Lim–Lee / small-subgroup-confinement attack).
│                       │       │                   The realistic attack surface is narrow: principally CMP
│                       │       │                   deployments with
│                       │       │                   long-lived RA/CA DHX keys and bespoke enterprise or
│                       │       │                   government applications
│                       │       │                   using X9.42 DHX static keys with interactive protocols and
│                       │       │                   therefore this
│                       │       │                   issue was assigned Low severity.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are
│                       │       │                   affected by this
│                       │       │                   issue. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/3da5a516cd2
│                       │       │                  │      635a320ff748503db2cef7c4b0f02 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/3ddbb7ab50b
│                       │       │                  │      d93dfc59cbe08e269a67605aeebdb 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/5f452bba2c6
│                       │       │                  │      81423d8fcffd120a19b757ee42e3c 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/7fbfde7677e
│                       │       │                  │      d8808828bf00ff01c937ca04bdda2 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/ca2237ab561
│                       │       │                  │      5641b662183b077f62c08d75e8070 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-42770 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.523Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.197Z 
│                       ├ [71]  ╭ VulnerabilityID : CVE-2026-45446 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45446 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ff83b8d311772c9bce761ce965a89276f5cca2519e25904f60e6
│                       │       │                   58274d150d44 
│                       │       ├ Title           : Issue summary: The implementations of AES-SIV (RFC 5297)
│                       │       │                   and AES-GCM-S ... 
│                       │       ├ Description     : Issue summary: The implementations of AES-SIV (RFC 5297)
│                       │       │                   and AES-GCM-SIV
│                       │       │                   (RFC 8452) mishandle the authentication of AAD (Additional
│                       │       │                   Authenticated
│                       │       │                   Data) with an empty ciphertext allowing a forgery of such
│                       │       │                   messages.
│                       │       │                   
│                       │       │                   Impact summary: An attacker can forge empty messages with
│                       │       │                   arbitrary AAD
│                       │       │                   to the victim's application using these ciphers.
│                       │       │                   AES-SIV (RFC 5297) and AES-GCM-SIV (RFC 8452) are
│                       │       │                   nonce-misuse-resistant AEAD
│                       │       │                   modes: they accept a key, nonce, optional AAD (bytes that
│                       │       │                   are authenticated
│                       │       │                   but not encrypted), and plaintext, and produces ciphertext
│                       │       │                   plus a 16-byte
│                       │       │                   tag. On decrypt, `EVP_DecryptFinal_ex()` is documented to
│                       │       │                   return success only
│                       │       │                   if the tag is verified succesfully.
│                       │       │                   In OpenSSL's provider implementation of these ciphers, the
│                       │       │                   expected tag is
│                       │       │                   computed only when decryption function is invoked with
│                       │       │                   non-empty data.
│                       │       │                   If the caller supplies AAD and then calls
│                       │       │                   `EVP_DecryptFinal_ex()` without
│                       │       │                   invocation of the ciphertext update, which can happen when
│                       │       │                   the received
│                       │       │                   ciphertext length is zero, the tag is never recalculated
│                       │       │                   and still holds its
│                       │       │                   all-zeros value.
│                       │       │                   When AES-GCM-SIV is used, an attacker who sends arbitrary
│                       │       │                   AAD, empty
│                       │       │                   ciphertext, and all-zeros tag passes authentication under
│                       │       │                   any key they do not
│                       │       │                   know, single-shot. When AES-SIV is used, for mounting the
│                       │       │                   attack it's
│                       │       │                   necessary for the application to reuse the decryption
│                       │       │                   context without
│                       │       │                   resetting the key.
│                       │       │                   AES-SIV is implemented since OpenSSL 3.0. AES-GCM-SIV is
│                       │       │                   implemented since
│                       │       │                   OpenSSL 3.2.
│                       │       │                   No protocols implemented in OpenSSL itself
│                       │       │                   (TLS/CMS/PKCS7/HPKE/QUIC) support
│                       │       │                   either AES-GCM-SIV or AES-SIV. To mount an attack, the
│                       │       │                   applications must
│                       │       │                   implement their own protocol and use the EVP interface.
│                       │       │                   Also they must skip the
│                       │       │                   ciphertext update when a message with an empty ciphertext
│                       │       │                   arrives.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as these algorithms are not FIPS approved and the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/25b32cd9d41
│                       │       │                  │      d2bc01b6abc425bb4baf2c2236fdc 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/71e2a5d2635
│                       │       │                  │      18cf5866043bd60ee4994d59e53a3 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7fe3f33a3b3
│                       │       │                  │      a4c487aa4dcdbc87057f66ffd2b85 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/daca0f48e4a
│                       │       │                  │      69a2892a62262bad59e62a8a76598 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/eec5e9bf0d8
│                       │       │                  │      67333b8495e456f5235d225798a68 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-45446 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:19.137Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.733Z 
│                       ├ [72]  ╭ VulnerabilityID : CVE-2026-7383 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-7383 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:7e1da58896d42d5c8128cf541fde0cbf72dd1e63685c84bf654e
│                       │       │                   a9d5ac0bc908 
│                       │       ├ Title           : Issue summary: A signed integer overflow when sizing the
│                       │       │                   destination b ... 
│                       │       ├ Description     : Issue summary: A signed integer overflow when sizing the
│                       │       │                   destination
│                       │       │                   buffer for Unicode output in ASN1_mbstring_ncopy() can lead
│                       │       │                    to a heap
│                       │       │                   buffer overflow.
│                       │       │                   
│                       │       │                   Impact summary: A heap buffer overflow may lead to a crash
│                       │       │                   or possibly
│                       │       │                   attacker controlled code execution or other undefined
│                       │       │                   behaviour.
│                       │       │                   In ASN1_mbstring_copy() and ASN1_mbstring_ncopy() the
│                       │       │                   size for Unicode output is computed in a signed int: by
│                       │       │                   left shift
│                       │       │                   of the input character count for BMPSTRING (UTF-16) and
│                       │       │                   UNIVERSALSTRING (UTF-32), and by summing per-character byte
│                       │       │                    counts
│                       │       │                   for UTF8STRING. The calculation overflows when the input
│                       │       │                   reaches
│                       │       │                   around 2^30 characters. In the worst case (UNIVERSALSTRING
│                       │       │                   at 2^30
│                       │       │                   characters) the size wraps to zero, OPENSSL_malloc(1) is
│                       │       │                   called, and
│                       │       │                   the subsequent character copy writes several gigabytes past
│                       │       │                    the
│                       │       │                   one-byte allocation.
│                       │       │                   X.509 certificate processing routes through
│                       │       │                   ASN1_STRING_set_by_NID(),
│                       │       │                   whose DIRSTRING_TYPE mask excludes UNIVERSALSTRING and
│                       │       │                   whose per-NID
│                       │       │                   size limits cap the input length; no network protocol or
│                       │       │                   certificate-handling path in OpenSSL exercises the
│                       │       │                   overflow.
│                       │       │                   Triggering the bug requires an application that calls
│                       │       │                   ASN1_mbstring_copy() or ASN1_mbstring_ncopy() directly, or
│                       │       │                   registers
│                       │       │                   a custom string type via ASN1_STRING_TABLE_add(), with
│                       │       │                   attacker-controlled input on the order of half a gigabyte
│                       │       │                   or more.
│                       │       │                   For these reasons this issue was assigned Low severity.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue, as the affected code is outside the OpenSSL
│                       │       │                   FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/4f8d2bddaa2
│                       │       │                  │      c8e06f9c33390ee1717059a6e4be6 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/80c15faaf78
│                       │       │                  │      042bbb8654a0e234c50c381732f74 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/bd17511070f
│                       │       │                  │      b39a67bfa19682affb765e706a974 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/c332adaced4
│                       │       │                  │      3bcbb85f97410597e951c11ec3083 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/d32350ae8ef
│                       │       │                  │      7426718f5aa9e383d4b51398ee255 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-7383 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:50.337Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:25.463Z 
│                       ├ [73]  ╭ VulnerabilityID : CVE-2026-9076 
│                       │       ├ PkgID           : openssl@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl@3.5.3-1ubuntu3.3?arch=amd64&d
│                       │       │                  │       istro=ubuntu-25.10 
│                       │       │                  ╰ UID : 946d2ac6c3cd4102 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9076 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2c40bf85dab5ff3498bcf1db3ca1289d4022efb696c09b299f6a
│                       │       │                   fb74880de03f 
│                       │       ├ Title           : Issue summary: When CMS password-based decryption (RFC 3211
│                       │       │                    / PWRI key ... 
│                       │       ├ Description     : Issue summary: When CMS password-based decryption (RFC 3211
│                       │       │                    / PWRI key unwrap)
│                       │       │                   processes attacker-supplied CMS data, an attacker-chosen
│                       │       │                   stream-mode KEK
│                       │       │                   cipher can trigger a heap out-of-bounds read in
│                       │       │                   kek_unwrap_key().
│                       │       │                   
│                       │       │                   Impact summary: A heap buffer over-read may trigger a crash
│                       │       │                    which leads to
│                       │       │                   Denial of Service for an application if the input buffer
│                       │       │                   ends at a memory
│                       │       │                   page boundary and the following page is unmapped. There is
│                       │       │                   no information
│                       │       │                   disclosure as the over-read bytes are not revealed to the
│                       │       │                   attacker.
│                       │       │                   The key unwrapping function performs a check-byte test as
│                       │       │                   specified in the
│                       │       │                   RFC that reads 7 bytes from a heap allocation that is based
│                       │       │                    on the wrapped
│                       │       │                   key length from the message. There is a minimum length
│                       │       │                   check based on the
│                       │       │                   block length of the wrapping cipher. However the cipher is
│                       │       │                   selected from
│                       │       │                   an OID carried in the attacker's PWRI
│                       │       │                   keyEncryptionAlgorithm with no
│                       │       │                   requirement that the cipher be a block cipher. When an
│                       │       │                   attacker selects
│                       │       │                   a stream-mode cipher the guard will be ineffective and the
│                       │       │                   allocated buffer
│                       │       │                   containing the unwrapped key can be too small to fit the
│                       │       │                   check-bytes
│                       │       │                   specified in the RFC and a buffer over-read can happen.
│                       │       │                   Applications calling CMS_decrypt() or
│                       │       │                   CMS_decrypt_set1_password()
│                       │       │                   (equivalently openssl cms -decrypt -pwri_password ...) on
│                       │       │                   untrusted CMS
│                       │       │                   data are vulnerable to this issue. No password knowledge is
│                       │       │                    required: the
│                       │       │                   over-read happens during the unwrap attempt before any
│                       │       │                   authentication
│                       │       │                   succeeds.
│                       │       │                   The over-read is limited to a few bytes and is not written
│                       │       │                   to output, so
│                       │       │                   there is no information disclosure. Triggering a crash
│                       │       │                   requires the
│                       │       │                   allocation to border unmapped memory, which is unlikely
│                       │       │                   with the normal
│                       │       │                   allocator.
│                       │       │                   The FIPS modules are not affected by this issue. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/05b06636684
│                       │       │                  │      2f930fadd9a6e94df98030af431bb 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/3d8d5bc1056
│                       │       │                  │      b2f62da9fede23fedbf47e85187b0 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/715349a1d7c
│                       │       │                  │      6db970e6815dafb90915f07307f98 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/77bf00ab13f
│                       │       │                  │      6ff5e516535432f0328ed70ec0c26 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/eecbe330977
│                       │       │                  │      e8d023aae1ca2d9bdbe983ef3fdc6 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-9076 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:50.997Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:26.063Z 
│                       ├ [74]  ╭ VulnerabilityID : CVE-2026-45447 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45447 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:d89c9ba8e0f7faab7fd03f8a0fd1b3fe3be9a897cc02b4834660
│                       │       │                   1b845257a3e8 
│                       │       ├ Title           : Issue summary: A specially crafted PKCS#7 or S/MIME signed
│                       │       │                   message cou ... 
│                       │       ├ Description     : Issue summary: A specially crafted PKCS#7 or S/MIME signed
│                       │       │                   message could
│                       │       │                   trigger a use-after-free during PKCS#7 signature
│                       │       │                   verification.
│                       │       │                   
│                       │       │                   Impact summary: A use-after-free may result in process
│                       │       │                   crashes, heap
│                       │       │                   corruption, or potentially remote code execution.
│                       │       │                   When processing a PKCS#7 or S/MIME signed message, if the
│                       │       │                   SignedData
│                       │       │                   digestAlgorithms field is present as an empty ASN.1 SET,
│                       │       │                   OpenSSL may
│                       │       │                   incorrectly free a caller-owned BIO during PKCS7_verify().
│                       │       │                   A subsequent
│                       │       │                   use of the BIO by the calling application results in a
│                       │       │                   use-after-free
│                       │       │                   condition.
│                       │       │                   In the common case this occurs when the application later
│                       │       │                   calls
│                       │       │                   BIO_free() on the BIO originally passed to PKCS7_verify().
│                       │       │                   Depending
│                       │       │                   on allocator behavior and application-specific BIO usage
│                       │       │                   patterns, this
│                       │       │                   may result in a crash or other memory corruption. In some
│                       │       │                   application
│                       │       │                   contexts this may potentially be exploitable for remote
│                       │       │                   code execution.
│                       │       │                   Applications that process PKCS#7 or S/MIME signed messages
│                       │       │                   using OpenSSL
│                       │       │                   PKCS#7 APIs may be affected. Applications using the CMS
│                       │       │                   APIs for this
│                       │       │                   processing are not affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : HIGH 
│                       │       ├ CweIDs           ─ [0]: CWE-416 
│                       │       ├ VendorSeverity   ─ ubuntu: 3 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/3aad5eb7af4
│                       │       │                  │      de4ee0633c30a8541a54d9bbde63c 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/7d4a980c622
│                       │       │                  │      58c5910cc883936e0c8dbab4d75a8 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/9dfd688ad22
│                       │       │                  │      90fc5075cacbc9bf0c9a93eefed54 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/a541ae8bfe8
│                       │       │                  │      49a30cc885e8780715c0f488e496c 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/c505d7559da
│                       │       │                  │      5d5f9f2c3913c6883a5562ce7273e 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-45447 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:19.277Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T15:16:35.16Z 
│                       ├ [75]  ╭ VulnerabilityID : CVE-2026-34182 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34182 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:95a1902c892337792a749b063a1140a80c6df7fc02c9034617ab
│                       │       │                   c3405b59c8d6 
│                       │       ├ Title           : Issue Summary: Cryptographic Message Services (CMS)
│                       │       │                   processing fails t ... 
│                       │       ├ Description     : Issue Summary: Cryptographic Message Services (CMS)
│                       │       │                   processing fails to perform
│                       │       │                   sufficient input validation on the cipher and tag length
│                       │       │                   fields of
│                       │       │                   AuthEnvelopedData containers, leading to various potential
│                       │       │                   compromises.
│                       │       │                   
│                       │       │                   Impact Summary: Attackers making use of these
│                       │       │                   vulnerabilities may achieve
│                       │       │                   key-equivalent functionality for a given CMS recipient
│                       │       │                   and/or bypass integrity
│                       │       │                   validation for a given message.
│                       │       │                   In one use case, an attacker may send a CMS message
│                       │       │                   containing
│                       │       │                   AuthEnvelopedData with the cipher specified as a non-AEAD
│                       │       │                   cipher.  OpenSSL
│                       │       │                   erroneously allows this selection, and attempts to decrypt
│                       │       │                   and validate the
│                       │       │                   message.
│                       │       │                   An on-path attacker who captures one legitimate AES-GCM
│                       │       │                   AuthEnvelopedData
│                       │       │                   addressed to the victim can re-emit it with the
│                       │       │                   recipientInfos set left
│                       │       │                   byte-for-byte intact, so the victim's private key still
│                       │       │                   unwraps the genuine CEK
│                       │       │                   (the content-encryption key), but with the inner OID
│                       │       │                   rewritten to AES-256-OFB
│                       │       │                   (Output Feedback Mode, an unauthenticated keystream mode)
│                       │       │                   and with an
│                       │       │                   attacker-chosen IV and ciphertext. The victim initializes
│                       │       │                   AES-256-OFB under the
│                       │       │                   real CEK, never consults the MAC field, and CMS_decrypt()
│                       │       │                   returns success.
│                       │       │                   If the application under attack responds to the attacker
│                       │       │                   with any indicator
│                       │       │                   showing success or failure of the decryption effort, it is
│                       │       │                   possible for the
│                       │       │                   attacker to use this as an oracle to obtain key equivalent
│                       │       │                   functionality for the
│                       │       │                   CEK used for the chosen recipient of the message.
│                       │       │                   In another use case, an attacker can reduce the tag length
│                       │       │                   of the chosen AEAD
│                       │       │                   cipher for a given AuthEnvelopedData container to be a
│                       │       │                   single byte long,
│                       │       │                   allowing an attacker to brute force CMS decryption,
│                       │       │                   producing an integrity
│                       │       │                   bypass for applications that trust CMS_decrypt() to reject
│                       │       │                   modified content.
│                       │       │                   The FIPS modules are not affected by this issue. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-354 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/03c1f4d45fb
│                       │       │                  │      963aee7d5833390c507cd290182bc 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/439ed7d2c09
│                       │       │                  │      62ce964482727264668bf277c333f 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7947e6a81eb
│                       │       │                  │      8776802f159fb6762cb7fcf7e34c7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/9fd97f8cfdc
│                       │       │                  │      2c0be214998de3b2b55c8edf6c7ac 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/d2ca86bcd43
│                       │       │                  │      e4f17d899f347101766b6107676e0 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34182 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.857Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T17:16:32.48Z 
│                       ├ [76]  ╭ VulnerabilityID : CVE-2026-34183 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34183 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a25243c3cdc3faf459cefdab6ffdcbe030281fcdc3281ea61a24
│                       │       │                   76b59959aa57 
│                       │       ├ Title           : Issue summary: Remote peer may exhaust heap memory of the
│                       │       │                   QUIC server  ... 
│                       │       ├ Description     : Issue summary: Remote peer may exhaust heap memory of the
│                       │       │                   QUIC
│                       │       │                   server or client by flooding it with packets containing
│                       │       │                   PATH_CHALLENGE
│                       │       │                   frames.
│                       │       │                   
│                       │       │                   Impact summary: A malicious remote peer can cause an
│                       │       │                   unbounded
│                       │       │                   memory allocation which can lead to an abnormal termination
│                       │       │                    of the
│                       │       │                   application acting as a QUIC client or server and a Denial
│                       │       │                   of Service.
│                       │       │                   A remote peer may exhaust heap memory by flooding the
│                       │       │                   local
│                       │       │                   QUIC stack with PATH_CHALLENGE frames. The local QUIC
│                       │       │                   stack
│                       │       │                   allocates a PATH_RESPONSE frame for every PATH_CHALLENGE it
│                       │       │                    receives.
│                       │       │                   The allocated PATH_RESPONSE frame gets freed only when the
│                       │       │                   remote
│                       │       │                   peer acknowledges reception of the PATH_RESPONSE frame
│                       │       │                   which will
│                       │       │                   not be done by a malicious peer.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue. The QUIC stack is outside of OpenSSL FIPS
│                       │       │                   module
│                       │       │                   boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-1325 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/5b306efb0b3
│                       │       │                  │      779dfdd0803b4afc9d08c91f11517 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/7d06955ebe0
│                       │       │                  │      ecf8adfd4c1e92018586da47ef9ac 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d2e9efbe490
│                       │       │                  │      0a373227deb136e8665401404ffac 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/fbaa83859c0
│                       │       │                  │      1ad64f497b757aaf51be7d05ed9eb 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-34183 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:05Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T16:17:01.217Z 
│                       ├ [77]  ╭ VulnerabilityID : CVE-2026-42764 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42764 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:70e9b54a3ab4cd6a1534b7a2e4e7310dadc66a2c477744da552f
│                       │       │                   ec7eac489011 
│                       │       ├ Title           : Issue summary: Receiving a QUIC initial packet with an
│                       │       │                   invalid token m ... 
│                       │       ├ Description     : Issue summary: Receiving a QUIC initial packet with an
│                       │       │                   invalid token may
│                       │       │                   trigger a NULL pointer dereference in the OpenSSL QUIC
│                       │       │                   server with
│                       │       │                   address validation disabled.
│                       │       │                   
│                       │       │                   Impact summary: NULL pointer dereference typically causes
│                       │       │                   abnormal termination
│                       │       │                   of the affected QUIC server process and a Denial of
│                       │       │                   Service.
│                       │       │                   If the address validation is disabled in the OpenSSL QUIC
│                       │       │                   server
│                       │       │                   implementation, an attacker can crash the server by sending
│                       │       │                    an initial
│                       │       │                   packet with an invalid or expired token.
│                       │       │                   By default, the client address validation is enabled in the
│                       │       │                    OpenSSL QUIC server
│                       │       │                   implementation, which makes the default configuration not
│                       │       │                   vulnerable
│                       │       │                   to this issue. However if the SSL_LISTENER_FLAG_NO_VALIDATE
│                       │       │                    is used with
│                       │       │                   the SSL_new_listener() call, the address validation is
│                       │       │                   disabled making the
│                       │       │                   vulnerable code reachable.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/5e3ed291b8a
│                       │       │                  │      f0b03d5d3b9e56a1da69a187e9729 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/a45a0aba809
│                       │       │                  │      5682c88ff4fc4a784892b8c6f0677 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/bf29a458c1a
│                       │       │                  │      231eca87e384c62b9c2553fa57a91 
│                       │       │                  ├ [3]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [4]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-42764 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:07.693Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.23Z 
│                       ├ [78]  ╭ VulnerabilityID : CVE-2026-45445 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45445 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2ffd5954e8de8da38d388516dfe6c0243ca3ffae2d6f977cc01d
│                       │       │                   d1abf15afcbc 
│                       │       ├ Title           : Issue summary: When an application drives an AES-OCB
│                       │       │                   context through t ... 
│                       │       ├ Description     : Issue summary: When an application drives an AES-OCB
│                       │       │                   context through the
│                       │       │                   public EVP_Cipher() one-shot interface, the
│                       │       │                   application-supplied
│                       │       │                   initialisation vector (IV) is silently discarded.
│                       │       │                   
│                       │       │                   Impact summary: Every message encrypted under the same key
│                       │       │                   uses the
│                       │       │                   same effective nonce regardless of the IV supplied by the
│                       │       │                   caller,
│                       │       │                   resulting in (key, nonce) reuse and loss of
│                       │       │                   confidentiality.  If the
│                       │       │                   same code path is used to compute the authentication tag,
│                       │       │                   the tag
│                       │       │                   depends only on the (key, IV) pair and not on the plaintext
│                       │       │                    or
│                       │       │                   ciphertext, allowing universal forgery of arbitrary
│                       │       │                   ciphertext from a
│                       │       │                   single captured message.
│                       │       │                   OpenSSL provides two ways to drive a cipher: the documented
│                       │       │                    streaming
│                       │       │                   interface (EVP_CipherUpdate / EVP_CipherFinal_ex) and a
│                       │       │                   lower-level
│                       │       │                   one-shot, EVP_Cipher(), whose documentation explicitly
│                       │       │                   recommends
│                       │       │                   against use by applications in favour of EVP_CipherUpdate()
│                       │       │                    and
│                       │       │                   EVP_CipherFinal_ex().  The OCB provider's streaming handler
│                       │       │                    flushes
│                       │       │                   the application-supplied IV into the OCB context before
│                       │       │                   processing
│                       │       │                   data; the one-shot handler did not.  Every call to
│                       │       │                   EVP_Cipher() on an
│                       │       │                   AES-OCB context therefore ran with the all-zero key-derived
│                       │       │                    offset
│                       │       │                   state left by cipher initialisation, regardless of the
│                       │       │                   caller's IV.
│                       │       │                   If EVP_EncryptFinal_ex() is subsequently used to obtain
│                       │       │                   the
│                       │       │                   authentication tag, the deferred IV setup runs at that
│                       │       │                   point and
│                       │       │                   clears the running checksum that should have been
│                       │       │                   accumulated over the
│                       │       │                   plaintext.  The resulting tag is a function of (key, IV)
│                       │       │                   only and
│                       │       │                   verifies against any ciphertext produced under the same
│                       │       │                   (key, IV)
│                       │       │                   pair.
│                       │       │                   The OpenSSL SSL/TLS implementation is not affected: AES-OCB
│                       │       │                    is not a
│                       │       │                   TLS cipher suite, and libssl does not call EVP_Cipher() in
│                       │       │                   any case.
│                       │       │                   Applications that drive AES-OCB through the documented
│                       │       │                   streaming AEAD
│                       │       │                   API (EVP_CipherUpdate / EVP_CipherFinal_ex) are not
│                       │       │                   affected.  Only
│                       │       │                   applications that combine the AES-OCB cipher with the
│                       │       │                   EVP_Cipher()
│                       │       │                   one-shot API are vulnerable.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue, as AES-OCB is outside the OpenSSL FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/323f0b6e7d5
│                       │       │                  │      30a4cb4336d50c88cb70f3ac2a451 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/787a6dfba81
│                       │       │                  │      b7b09c1e05ab31396c0cd7c36b3f7 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7ac4715234e
│                       │       │                  │      e72d9f3c93426a2c08554b5b771af 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/843c9b94ca9
│                       │       │                  │      c2ed248bb30127bb4f3d7af0d607c 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/983d54b5cce
│                       │       │                  │      8d16147548ed1a37892d1720bbab6 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-45445 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:18.993Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.507Z 
│                       ├ [79]  ╭ VulnerabilityID : CVE-2026-34180 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34180 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:40f909433d9026859f07682fc61ae1bf04e099baf16936bbd813
│                       │       │                   1896f25f0805 
│                       │       ├ Title           : Issue summary: Parsing a crafted DER-encoded ASN.1
│                       │       │                   structure with a pr ... 
│                       │       ├ Description     : Issue summary: Parsing a crafted DER-encoded ASN.1
│                       │       │                   structure with a primitive
│                       │       │                   element whose content exceeds 2 gigabytes in length may
│                       │       │                   cause a heap buffer
│                       │       │                   over-read on 64-bit Unix and Unix-like platforms.
│                       │       │                   
│                       │       │                   Impact summary: The heap buffer over-read may crash the
│                       │       │                   application (Denial of
│                       │       │                   Service) or to load into the decoded ASN.1 object contents
│                       │       │                   of memory beyond the
│                       │       │                   end of the input buffer.  More typically such ASN.1
│                       │       │                   elements would instead be
│                       │       │                   truncated.
│                       │       │                   An integer truncation in OpenSSL's ASN.1 decoder causes the
│                       │       │                    content length of
│                       │       │                   an ASN.1 primitive element to be mishandled when it exceeds
│                       │       │                    2 gigabytes. In the
│                       │       │                   worst case the truncated length is treated as a request to
│                       │       │                   scan the binary
│                       │       │                   content for a terminating zero byte, possibly causing
│                       │       │                   OpenSSL to read either
│                       │       │                   less than or beyond the end of the allocated buffer.
│                       │       │                   Applications that pass attacker-supplied data to
│                       │       │                   d2i_X509(), d2i_PKCS7(), or
│                       │       │                   any other d2i_* decoding function are affected. OpenSSL's
│                       │       │                   own command-line
│                       │       │                   tools are not vulnerable, as data read through the BIO
│                       │       │                   layer is checked before
│                       │       │                   it reaches the affected code. The issue only affects 64-bit
│                       │       │                    Unix and Unix-like
│                       │       │                   platforms; 32-bit platforms and 64-bit Windows are not
│                       │       │                   affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by this issue,
│                       │       │                   as the affected code is outside the OpenSSL FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/1c6908e4fa5
│                       │       │                  │      fa568752221d8eaf561a809751e5d 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/cbe418ae978
│                       │       │                  │      539cf14a398a207dba834c0e93e83 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d93853c4211
│                       │       │                  │      0d6319e3df07842b488cb9f7ac5ff 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/da5d62af75f
│                       │       │                  │      69d6fbf7803743d7c56ac75461e43 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/f696c73c3e6
│                       │       │                  │      1b8c502d040af62e690c060908a16 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-34180 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.6Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:22.627Z 
│                       ├ [80]  ╭ VulnerabilityID : CVE-2026-34181 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-34181 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:08b549b5b2ad6920e05a6c41541141e9fc6ad1a0ed7c56272aaf
│                       │       │                   cbdc8a5d7e3f 
│                       │       ├ Title           : Issue Summary: The PKCS#12 file processing fails to perform
│                       │       │                    sufficient ... 
│                       │       ├ Description     : Issue Summary: The PKCS#12 file processing fails to perform
│                       │       │                    sufficient input
│                       │       │                   validation for files that use Password-Based Message
│                       │       │                   Authentication Code 1
│                       │       │                   (PBMAC1) integrity mechanism allowing a certificate and
│                       │       │                   private key forgery.
│                       │       │                   
│                       │       │                   Impact Summary: An attacker impersonating a user can cause
│                       │       │                   a service reading
│                       │       │                   PKCS#12 files to accept forged certificates and private
│                       │       │                   keys with a 1 in 256
│                       │       │                   probability.
│                       │       │                   If a service accepting PKCS#12 files is using passwords for
│                       │       │                    authenticating
│                       │       │                   the received files, the attacker can create unencrypted
│                       │       │                   PKCS#12 files that
│                       │       │                   use PBMAC1 authentication that specifies an HMAC key of
│                       │       │                   only one byte, allowing
│                       │       │                   them to craft a file that will be accepted with a 1 in 256
│                       │       │                   That would then cause the service to accept a certificate
│                       │       │                   and private key
│                       │       │                   controlled by the attacker.
│                       │       │                   The FIPS modules are not affected by this issue, as the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-354 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/0300eb9ddce
│                       │       │                  │      7a0895bf301a4b0c03a9da2313a0f 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/79eb76a937e
│                       │       │                  │      474bb7610a0a3dc57131dc8dc6610 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/85dcbb3abaa
│                       │       │                  │      4878af5c8fbbe11bce708fcf984a7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/ec36f2417c4
│                       │       │                  │      ddd8cabce4b4a60a3d7a7365f2d81 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-34181 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:04.74Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T17:16:32.29Z 
│                       ├ [81]  ╭ VulnerabilityID : CVE-2026-42766 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42766 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b82f074b0d382679d27cf5f30b86140e7c27a9100e9c187a1ede
│                       │       │                   7ba50f2bde0a 
│                       │       ├ Title           : Issue summary: A specially crafted password-encrypted CMS
│                       │       │                   message can  ... 
│                       │       ├ Description     : Issue summary: A specially crafted password-encrypted CMS
│                       │       │                   message
│                       │       │                   can trigger a NULL pointer dereference during CMS
│                       │       │                   decryption.
│                       │       │                   
│                       │       │                   Impact summary: This NULL pointer dereference leads to an
│                       │       │                   application crash
│                       │       │                   and a Denial of Service.
│                       │       │                   The CMS PasswordRecipientInfo.keyDerivationAlgorithm field
│                       │       │                   is defined as
│                       │       │                   OPTIONAL in the ASN.1 specification and may therefore be
│                       │       │                   absent in specially
│                       │       │                   crafted inputs. During the password-based CMS decryption
│                       │       │                   the OpenSSL
│                       │       │                   CMS implementation dereferences this field without first
│                       │       │                   checking whether it
│                       │       │                   was present.
│                       │       │                   An attacker who supplies such a CMS message to an
│                       │       │                   application performing
│                       │       │                   password-based CMS decryption can trigger an application
│                       │       │                   crash, leading to
│                       │       │                   a Denial of Service.
│                       │       │                   Applications that process password-encrypted CMS messages
│                       │       │                   may be affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/056d06c1918
│                       │       │                  │      fafbb98c1c85a02e4c47cc4e199ce 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/12bc26ffb3a
│                       │       │                  │      2be728c9b86e1cae277de5b33dfa4 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/3ff64913615
│                       │       │                  │      d648cfbb6a6f1cf5529ae7ea829d7 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/ab52d88cb53
│                       │       │                  │      74876d59aee3c91f9e4ccce2b7ce4 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/da26f368732
│                       │       │                  │      b83e40e9d356fe61c3d3aaab6d2e8 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-42766 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:07.97Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.52Z 
│                       ├ [82]  ╭ VulnerabilityID : CVE-2026-42767 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42767 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:be324ef3d7af567c17f65d244aed634ec29edf027decbacee533
│                       │       │                   3b33030d974c 
│                       │       ├ Title           : Issue summary: An attacker-controlled CMP (Certificate
│                       │       │                   Management Prot ... 
│                       │       ├ Description     : Issue summary: An attacker-controlled CMP (Certificate
│                       │       │                   Management Protocol)
│                       │       │                   server could trigger a NULL pointer dereference in a CMP
│                       │       │                   client application.
│                       │       │                   
│                       │       │                   Impact summary: A NULL pointer dereference causes a crash
│                       │       │                   of the
│                       │       │                   application and a Denial of Service.
│                       │       │                   An attacker controlling a CMP server (or acting as a
│                       │       │                   man-in-the-middle) could
│                       │       │                   craft a CMP response containing a CRMF (Certificate Request
│                       │       │                    Message Format)
│                       │       │                   CertRepMessage with an EncryptedValue structure where the
│                       │       │                   symmAlg field
│                       │       │                   has an algorithm OID but no parameters field. When the
│                       │       │                   OpenSSL CMP client
│                       │       │                   processes this response, the NULL dereference occurs,
│                       │       │                   causing a crash of
│                       │       │                   the CMP client.
│                       │       │                   Applications that process untrusted CMP/CRMF messages may
│                       │       │                   be affected.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as the affected code is outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-476 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/61a86a8cd73
│                       │       │                  │      546c9fea916f3d304c1293e05c046 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/665d5254083
│                       │       │                  │      affde9982efca7c41dd01cacc8774 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/810b722f772
│                       │       │                  │      652ad48042bcc7ab07e3414b11d0f 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/b90ff3b1bd3
│                       │       │                  │      3b1c18e6a09936d097c2eddef8873 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/e6f912907fc
│                       │       │                  │      2ec82a0fd07aae55172c5e5e3d90d 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-42767 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.093Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.683Z 
│                       ├ [83]  ╭ VulnerabilityID : CVE-2026-42768 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42768 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:51e15e832844660d0b6be8cd321b3088413606e94f6ce5297306
│                       │       │                   215d2dac5ef9 
│                       │       ├ Title           : Issue summary: The CMS_decrypt and PKCS7_decrypt functions
│                       │       │                   are vulnera ... 
│                       │       ├ Description     : Issue summary: The CMS_decrypt and PKCS7_decrypt functions
│                       │       │                   are vulnerable to
│                       │       │                   Bleichenbacher-style attack when an attacker is able to
│                       │       │                   provide the CMS or
│                       │       │                   S/MIME messages and observe the error code and/or
│                       │       │                   decryption output.
│                       │       │                   
│                       │       │                   Impact summary: The Bleichenbacher-style attack allows an
│                       │       │                   attacker to use the
│                       │       │                   victim's vulnerable application as a way to decrypt or sign
│                       │       │                    messages with the
│                       │       │                   victim's private RSA key.
│                       │       │                   The attack is possible in 2 variants.
│                       │       │                   1. The decryption API (CMS_decrypt(), PKCS7_decrypt()) is
│                       │       │                   used without
│                       │       │                   providing the recipient certificate. In this case OpenSSL
│                       │       │                   iterates over every
│                       │       │                   KeyTransRecipientInfo (KTRI) without stopping at the first
│                       │       │                   success.
│                       │       │                   An attacker who authors a message with two KTRI entries —
│                       │       │                   the first one
│                       │       │                   wrapping a real CEK under the victim's public key, the
│                       │       │                   second with an
│                       │       │                   arbitrary probe ciphertext — obtains opportunity to iterate
│                       │       │                    the 2nd KTRI to
│                       │       │                   get a valid PKCS#1 v1.5 padding if the error code of the
│                       │       │                   application is
│                       │       │                   available.
│                       │       │                   That is a Bleichenbacher oracle (Bleichenbacher, CRYPTO
│                       │       │                   '98): an
│                       │       │                   adaptive-chosen-ciphertext side channel from which the
│                       │       │                   attacker decrypts any
│                       │       │                   RSA ciphertext to the victim's key or forges any PKCS#1
│                       │       │                   v1.5 signature under
│                       │       │                   it.
│                       │       │                   2. When the decryption API (CMS_decrypt(), PKCS7_decrypt())
│                       │       │                    is provided with
│                       │       │                   the recipient certificate, and the recipient is not found,
│                       │       │                   a random
│                       │       │                   key is substituted.
│                       │       │                   An attacker who authors a message and is able to compare
│                       │       │                   both error code and
│                       │       │                   the result of the decryption, can mount a Bleichenbacher
│                       │       │                   oracle.
│                       │       │                   We are not aware of any applications that provide a remote
│                       │       │                   attacker
│                       │       │                   an opportunity to mount an attack described in these
│                       │       │                   scenarios. We consider
│                       │       │                   the existence of such application very unlikely, and for
│                       │       │                   this reason this
│                       │       │                   CVE has been evaluated as Low severity.
│                       │       │                   To avoid these attacks, when RSA PKCS#1 v1.5 Key Transport
│                       │       │                   is in use, the
│                       │       │                   invoked EVP_PKEY_decrypt() will use the implicit rejection
│                       │       │                   mechanism described
│                       │       │                   in draft-irtf-cfrg-rsa-guidance. In previous OpenSSL
│                       │       │                   releases the implicit
│                       │       │                   rejection was explicitly disabled.
│                       │       │                   The implicit rejection mechanism always returns a plaintext
│                       │       │                    value,
│                       │       │                   the symmetric key. This result is deterministic for the
│                       │       │                   ciphertext and the
│                       │       │                   private key.  The length of the decryption result can
│                       │       │                   happen to match the
│                       │       │                   length of the key of the symmetric cipher that was used for
│                       │       │                    the content
│                       │       │                   encryption. When a certificate is not provided, the last
│                       │       │                   RecipientInfo
│                       │       │                   producing a key that looks valid will be used. It may cause
│                       │       │                    getting garbage
│                       │       │                   content on decryption. As a proper way to deal with this a
│                       │       │                   recipient
│                       │       │                   certificate has to be provided to identify the particular
│                       │       │                   RecipientInfo for
│                       │       │                   decryption.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, and 3.4 are not affected
│                       │       │                    by this issue, as
│                       │       │                   CMS and S/MIME processing happens outside the OpenSSL FIPS
│                       │       │                   module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-514 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/a2ca7b2d73e
│                       │       │                  │      0ffc1eae183fe6e1741dac767cb4f 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/bbb151a8304
│                       │       │                  │      1705d9d001ed2f9c12f5523e1b54d 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/dd68364107a
│                       │       │                  │      58841c0a2546812518b65d3a23abd 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/f04b377be3d
│                       │       │                  │      821741c86d1f4bf84dee09f3d5c3e 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42768 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.223Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:23.84Z 
│                       ├ [84]  ╭ VulnerabilityID : CVE-2026-42769 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42769 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:20e01933fa359f08119e21e05fc1a3c3890553eaa11640ac5654
│                       │       │                   5f40b92f0424 
│                       │       ├ Title           : Issue Summary: An error in the callback used to verify the
│                       │       │                   certificate ... 
│                       │       ├ Description     : Issue Summary: An error in the callback used to verify the
│                       │       │                   certificate
│                       │       │                   provided in a Root CA key update Certificate Management
│                       │       │                   Protocol (CMP)
│                       │       │                   message response rendered the certificate validation
│                       │       │                   ineffectual, which
│                       │       │                   could lead to escalation of credentials from the
│                       │       │                   Registration Authority (RA)
│                       │       │                   level to the root Certification Authority (root CA) level.
│                       │       │                   
│                       │       │                   Impact Summary: The Registration Autority could replace the
│                       │       │                    root CA
│                       │       │                   certificate for the CMP clients with an arbitrary root CA
│                       │       │                   certificate.
│                       │       │                   One of the parts of the Certificate Management Protocol
│                       │       │                   (CMP), specified in
│                       │       │                   RFC 9810, is Root Certification Authority (root CA) key
│                       │       │                   Rollover,
│                       │       │                   which is sent by the server in a message with type
│                       │       │                   'id-it-rootCaKeyUpdate'.
│                       │       │                   As part of these messages, 'newWithOld' certificate, the
│                       │       │                   new root CA
│                       │       │                   certificate signed with the old root CA key, is provided,
│                       │       │                   and verifying its
│                       │       │                   signature is crucial for transferring the trust from the
│                       │       │                   old CA key to the
│                       │       │                   new one.
│                       │       │                   The 'id-it-rootCaKeyUpdate' messages are expected to be
│                       │       │                   processed with
│                       │       │                   OSSL_CMP_get1_rootCaKeyUpdate(), that is expected to verify
│                       │       │                    the 'newWithOld'
│                       │       │                   certificate.  A typo in the certificate chain building code
│                       │       │                    led to adding
│                       │       │                   an incorrect certificate ('newWithOld' instead of
│                       │       │                   'oldRoot') to the
│                       │       │                   certificate chain, rendering the certificate verification
│                       │       │                   process ineffectual
│                       │       │                   (only the issuer name and the algorithm OIDs were verified
│                       │       │                   by other parts
│                       │       │                   of the verification code).
│                       │       │                   An attacker who already has credentials that satisfy the
│                       │       │                   CMP message
│                       │       │                   protection checks can generate a new key pair and use a
│                       │       │                   crafted self-signed
│                       │       │                   certificate in its 'id-it-rootCaKeyUpdate' CMP messages
│                       │       │                   which affected CMP
│                       │       │                   clients would accept as a new trust anchor.
│                       │       │                   Significant preconditions for the attack (having valid
│                       │       │                   RA-level credentials)
│                       │       │                   are the reason the issue was assigned Low severity.
│                       │       │                   The FIPS modules are not affected by this issue, as the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-295 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/54d0989997e
│                       │       │                  │      5fc26057009a9782c3441ce3842fb 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/777b363b16f
│                       │       │                  │      cf2153bb3ded39dc3838713667c44 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/d35cd473a27
│                       │       │                  │      1bf3ce7bf3d32af53217fb83ae92c 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/d531f21c0fe
│                       │       │                  │      99067a66fc0ff1161ef127f9cd70b 
│                       │       │                  ├ [4]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [5]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42769 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.377Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.027Z 
│                       ├ [85]  ╭ VulnerabilityID : CVE-2026-42770 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42770 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:598166923f6d39b36a4058e337b77e89d07959e56d5a691322a9
│                       │       │                   8032b56f5b93 
│                       │       ├ Title           : Issue summary: When EVP_PKEY_derive_set_peer() is called
│                       │       │                   with a DHX (X ... 
│                       │       ├ Description     : Issue summary: When EVP_PKEY_derive_set_peer() is called
│                       │       │                   with a DHX (X9.42)
│                       │       │                   peer key, the peer key is not properly checked for the
│                       │       │                   subgroup membership.
│                       │       │                   
│                       │       │                   Impact summary: A malicious peer which presents an X9.42
│                       │       │                   key carrying the
│                       │       │                   victim's p and g parameters, a forged q = r (a small prime
│                       │       │                   factor of the
│                       │       │                   cofactor (p−1)/q_local), and a public value Y of order r
│                       │       │                   can recover the
│                       │       │                   victim's private key after a small number of key exchange
│                       │       │                   attempts.
│                       │       │                   When EVP_PKEY_derive_set_peer() is called with a DHX
│                       │       │                   (X9.42) peer key, the
│                       │       │                   subgroup membership check Y^q ≡ 1 (mod p) is performed
│                       │       │                   using the peer's
│                       │       │                   own q parameter, not the local key's q. The peer's domain
│                       │       │                   parameters are
│                       │       │                   then matched against the domain parameters of the private
│                       │       │                   key, but the value
│                       │       │                   of q is not compared.
│                       │       │                   A malicious peer who presents an X9.42 key carrying the
│                       │       │                   victim's p, g,
│                       │       │                   a forged q = r (a small prime factor of the cofactor), and
│                       │       │                   a public
│                       │       │                   value Y of order r passes all checks. The shared secret
│                       │       │                   then takes only
│                       │       │                   r distinct values, leaking priv mod r. Repeating for each
│                       │       │                   small-prime
│                       │       │                   factor of the cofactor and combining via CRT recovers the
│                       │       │                   full private
│                       │       │                   key (Lim–Lee / small-subgroup-confinement attack).
│                       │       │                   The realistic attack surface is narrow: principally CMP
│                       │       │                   deployments with
│                       │       │                   long-lived RA/CA DHX keys and bespoke enterprise or
│                       │       │                   government applications
│                       │       │                   using X9.42 DHX static keys with interactive protocols and
│                       │       │                   therefore this
│                       │       │                   issue was assigned Low severity.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are
│                       │       │                   affected by this
│                       │       │                   issue. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/3da5a516cd2
│                       │       │                  │      635a320ff748503db2cef7c4b0f02 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/3ddbb7ab50b
│                       │       │                  │      d93dfc59cbe08e269a67605aeebdb 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/5f452bba2c6
│                       │       │                  │      81423d8fcffd120a19b757ee42e3c 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/7fbfde7677e
│                       │       │                  │      d8808828bf00ff01c937ca04bdda2 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/ca2237ab561
│                       │       │                  │      5641b662183b077f62c08d75e8070 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-42770 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:08.523Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.197Z 
│                       ├ [86]  ╭ VulnerabilityID : CVE-2026-45446 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45446 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:948e139782c97632c240441aa66df54845de42bb4a90f04e382b
│                       │       │                   b6a5ae1c4b07 
│                       │       ├ Title           : Issue summary: The implementations of AES-SIV (RFC 5297)
│                       │       │                   and AES-GCM-S ... 
│                       │       ├ Description     : Issue summary: The implementations of AES-SIV (RFC 5297)
│                       │       │                   and AES-GCM-SIV
│                       │       │                   (RFC 8452) mishandle the authentication of AAD (Additional
│                       │       │                   Authenticated
│                       │       │                   Data) with an empty ciphertext allowing a forgery of such
│                       │       │                   messages.
│                       │       │                   
│                       │       │                   Impact summary: An attacker can forge empty messages with
│                       │       │                   arbitrary AAD
│                       │       │                   to the victim's application using these ciphers.
│                       │       │                   AES-SIV (RFC 5297) and AES-GCM-SIV (RFC 8452) are
│                       │       │                   nonce-misuse-resistant AEAD
│                       │       │                   modes: they accept a key, nonce, optional AAD (bytes that
│                       │       │                   are authenticated
│                       │       │                   but not encrypted), and plaintext, and produces ciphertext
│                       │       │                   plus a 16-byte
│                       │       │                   tag. On decrypt, `EVP_DecryptFinal_ex()` is documented to
│                       │       │                   return success only
│                       │       │                   if the tag is verified succesfully.
│                       │       │                   In OpenSSL's provider implementation of these ciphers, the
│                       │       │                   expected tag is
│                       │       │                   computed only when decryption function is invoked with
│                       │       │                   non-empty data.
│                       │       │                   If the caller supplies AAD and then calls
│                       │       │                   `EVP_DecryptFinal_ex()` without
│                       │       │                   invocation of the ciphertext update, which can happen when
│                       │       │                   the received
│                       │       │                   ciphertext length is zero, the tag is never recalculated
│                       │       │                   and still holds its
│                       │       │                   all-zeros value.
│                       │       │                   When AES-GCM-SIV is used, an attacker who sends arbitrary
│                       │       │                   AAD, empty
│                       │       │                   ciphertext, and all-zeros tag passes authentication under
│                       │       │                   any key they do not
│                       │       │                   know, single-shot. When AES-SIV is used, for mounting the
│                       │       │                   attack it's
│                       │       │                   necessary for the application to reuse the decryption
│                       │       │                   context without
│                       │       │                   resetting the key.
│                       │       │                   AES-SIV is implemented since OpenSSL 3.0. AES-GCM-SIV is
│                       │       │                   implemented since
│                       │       │                   OpenSSL 3.2.
│                       │       │                   No protocols implemented in OpenSSL itself
│                       │       │                   (TLS/CMS/PKCS7/HPKE/QUIC) support
│                       │       │                   either AES-GCM-SIV or AES-SIV. To mount an attack, the
│                       │       │                   applications must
│                       │       │                   implement their own protocol and use the EVP interface.
│                       │       │                   Also they must skip the
│                       │       │                   ciphertext update when a message with an empty ciphertext
│                       │       │                   arrives.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4, and 3.0 are not
│                       │       │                   affected by this
│                       │       │                   issue, as these algorithms are not FIPS approved and the
│                       │       │                   affected code is
│                       │       │                   outside the OpenSSL FIPS module boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-325 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/25b32cd9d41
│                       │       │                  │      d2bc01b6abc425bb4baf2c2236fdc 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/71e2a5d2635
│                       │       │                  │      18cf5866043bd60ee4994d59e53a3 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/7fe3f33a3b3
│                       │       │                  │      a4c487aa4dcdbc87057f66ffd2b85 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/daca0f48e4a
│                       │       │                  │      69a2892a62262bad59e62a8a76598 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/eec5e9bf0d8
│                       │       │                  │      67333b8495e456f5235d225798a68 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-45446 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:19.137Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:24.733Z 
│                       ├ [87]  ╭ VulnerabilityID : CVE-2026-7383 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-7383 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:7a39251d6aefb1edc59e6b6a30d52dd9b2c00cfc2df7f52959a6
│                       │       │                   8613a924372c 
│                       │       ├ Title           : Issue summary: A signed integer overflow when sizing the
│                       │       │                   destination b ... 
│                       │       ├ Description     : Issue summary: A signed integer overflow when sizing the
│                       │       │                   destination
│                       │       │                   buffer for Unicode output in ASN1_mbstring_ncopy() can lead
│                       │       │                    to a heap
│                       │       │                   buffer overflow.
│                       │       │                   
│                       │       │                   Impact summary: A heap buffer overflow may lead to a crash
│                       │       │                   or possibly
│                       │       │                   attacker controlled code execution or other undefined
│                       │       │                   behaviour.
│                       │       │                   In ASN1_mbstring_copy() and ASN1_mbstring_ncopy() the
│                       │       │                   size for Unicode output is computed in a signed int: by
│                       │       │                   left shift
│                       │       │                   of the input character count for BMPSTRING (UTF-16) and
│                       │       │                   UNIVERSALSTRING (UTF-32), and by summing per-character byte
│                       │       │                    counts
│                       │       │                   for UTF8STRING. The calculation overflows when the input
│                       │       │                   reaches
│                       │       │                   around 2^30 characters. In the worst case (UNIVERSALSTRING
│                       │       │                   at 2^30
│                       │       │                   characters) the size wraps to zero, OPENSSL_malloc(1) is
│                       │       │                   called, and
│                       │       │                   the subsequent character copy writes several gigabytes past
│                       │       │                    the
│                       │       │                   one-byte allocation.
│                       │       │                   X.509 certificate processing routes through
│                       │       │                   ASN1_STRING_set_by_NID(),
│                       │       │                   whose DIRSTRING_TYPE mask excludes UNIVERSALSTRING and
│                       │       │                   whose per-NID
│                       │       │                   size limits cap the input length; no network protocol or
│                       │       │                   certificate-handling path in OpenSSL exercises the
│                       │       │                   overflow.
│                       │       │                   Triggering the bug requires an application that calls
│                       │       │                   ASN1_mbstring_copy() or ASN1_mbstring_ncopy() directly, or
│                       │       │                   registers
│                       │       │                   a custom string type via ASN1_STRING_TABLE_add(), with
│                       │       │                   attacker-controlled input on the order of half a gigabyte
│                       │       │                   or more.
│                       │       │                   For these reasons this issue was assigned Low severity.
│                       │       │                   The FIPS modules in 4.0, 3.6, 3.5, 3.4 and 3.0 are not
│                       │       │                   affected by
│                       │       │                   this issue, as the affected code is outside the OpenSSL
│                       │       │                   FIPS module
│                       │       │                   boundary. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-787 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/4f8d2bddaa2
│                       │       │                  │      c8e06f9c33390ee1717059a6e4be6 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/80c15faaf78
│                       │       │                  │      042bbb8654a0e234c50c381732f74 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/bd17511070f
│                       │       │                  │      b39a67bfa19682affb765e706a974 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/c332adaced4
│                       │       │                  │      3bcbb85f97410597e951c11ec3083 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/d32350ae8ef
│                       │       │                  │      7426718f5aa9e383d4b51398ee255 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-7383 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:50.337Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:25.463Z 
│                       ├ [88]  ╭ VulnerabilityID : CVE-2026-9076 
│                       │       ├ PkgID           : openssl-provider-legacy@3.5.3-1ubuntu3.3 
│                       │       ├ PkgName         : openssl-provider-legacy 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/openssl-provider-legacy@3.5.3-1ubuntu
│                       │       │                  │       3.3?arch=amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 9e1f84d8f35bd1a0 
│                       │       ├ InstalledVersion: 3.5.3-1ubuntu3.3 
│                       │       ├ FixedVersion    : 3.5.3-1ubuntu3.4 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-9076 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ea98173d439e804de1579f53d8964251d98c0cba598ce4ab89de
│                       │       │                   164ff2752860 
│                       │       ├ Title           : Issue summary: When CMS password-based decryption (RFC 3211
│                       │       │                    / PWRI key ... 
│                       │       ├ Description     : Issue summary: When CMS password-based decryption (RFC 3211
│                       │       │                    / PWRI key unwrap)
│                       │       │                   processes attacker-supplied CMS data, an attacker-chosen
│                       │       │                   stream-mode KEK
│                       │       │                   cipher can trigger a heap out-of-bounds read in
│                       │       │                   kek_unwrap_key().
│                       │       │                   
│                       │       │                   Impact summary: A heap buffer over-read may trigger a crash
│                       │       │                    which leads to
│                       │       │                   Denial of Service for an application if the input buffer
│                       │       │                   ends at a memory
│                       │       │                   page boundary and the following page is unmapped. There is
│                       │       │                   no information
│                       │       │                   disclosure as the over-read bytes are not revealed to the
│                       │       │                   attacker.
│                       │       │                   The key unwrapping function performs a check-byte test as
│                       │       │                   specified in the
│                       │       │                   RFC that reads 7 bytes from a heap allocation that is based
│                       │       │                    on the wrapped
│                       │       │                   key length from the message. There is a minimum length
│                       │       │                   check based on the
│                       │       │                   block length of the wrapping cipher. However the cipher is
│                       │       │                   selected from
│                       │       │                   an OID carried in the attacker's PWRI
│                       │       │                   keyEncryptionAlgorithm with no
│                       │       │                   requirement that the cipher be a block cipher. When an
│                       │       │                   attacker selects
│                       │       │                   a stream-mode cipher the guard will be ineffective and the
│                       │       │                   allocated buffer
│                       │       │                   containing the unwrapped key can be too small to fit the
│                       │       │                   check-bytes
│                       │       │                   specified in the RFC and a buffer over-read can happen.
│                       │       │                   Applications calling CMS_decrypt() or
│                       │       │                   CMS_decrypt_set1_password()
│                       │       │                   (equivalently openssl cms -decrypt -pwri_password ...) on
│                       │       │                   untrusted CMS
│                       │       │                   data are vulnerable to this issue. No password knowledge is
│                       │       │                    required: the
│                       │       │                   over-read happens during the unwrap attempt before any
│                       │       │                   authentication
│                       │       │                   succeeds.
│                       │       │                   The over-read is limited to a few bytes and is not written
│                       │       │                   to output, so
│                       │       │                   there is no information disclosure. Triggering a crash
│                       │       │                   requires the
│                       │       │                   allocation to border unmapped memory, which is unlikely
│                       │       │                   with the normal
│                       │       │                   allocator.
│                       │       │                   The FIPS modules are not affected by this issue. 
│                       │       ├ Severity        : LOW 
│                       │       ├ CweIDs           ─ [0]: CWE-125 
│                       │       ├ VendorSeverity   ─ ubuntu: 1 
│                       │       ├ References       ╭ [0]: https://github.com/openssl/openssl/commit/05b06636684
│                       │       │                  │      2f930fadd9a6e94df98030af431bb 
│                       │       │                  ├ [1]: https://github.com/openssl/openssl/commit/3d8d5bc1056
│                       │       │                  │      b2f62da9fede23fedbf47e85187b0 
│                       │       │                  ├ [2]: https://github.com/openssl/openssl/commit/715349a1d7c
│                       │       │                  │      6db970e6815dafb90915f07307f98 
│                       │       │                  ├ [3]: https://github.com/openssl/openssl/commit/77bf00ab13f
│                       │       │                  │      6ff5e516535432f0328ed70ec0c26 
│                       │       │                  ├ [4]: https://github.com/openssl/openssl/commit/eecbe330977
│                       │       │                  │      e8d023aae1ca2d9bdbe983ef3fdc6 
│                       │       │                  ├ [5]: https://openssl-library.org/news/secadv/20260609.txt 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8414-1 
│                       │       │                  ├ [7]: https://ubuntu.com/security/notices/USN-8414-2 
│                       │       │                  ╰ [8]: https://www.cve.org/CVERecord?id=CVE-2026-9076 
│                       │       ├ PublishedDate   : 2026-06-09T17:17:50.997Z 
│                       │       ╰ LastModifiedDate: 2026-06-10T08:16:26.063Z 
│                       ├ [89]  ╭ VulnerabilityID : CVE-2024-56433 
│                       │       ├ PkgID           : passwd@1:4.17.4-2ubuntu2 
│                       │       ├ PkgName         : passwd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu2?arch=amd64&dis
│                       │       │                  │       tro=ubuntu-25.10&epoch=1 
│                       │       │                  ╰ UID : 2d87ef360f209a3f 
│                       │       ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bfb475087d63a7f6472afed29316d0c65a2d5c16da7b962a8b0e
│                       │       │                   c6c33388a767 
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
│                       │       │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20145 
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
│                       │       ╰ LastModifiedDate: 2026-04-15T00:35:42.02Z 
│                       ├ [90]  ╭ VulnerabilityID : CVE-2026-35338 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35338 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bcfcf69beb44f45adc8d5fbfd7fdf40e69220c3764a9f23f6c8c
│                       │       │                   3b484e3877fc 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:28:50.307Z 
│                       ├ [91]  ╭ VulnerabilityID : CVE-2026-35339 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35339 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:7334c968dd4ca8020566f3b2f29cc187be3638b927392d90bbec
│                       │       │                   cb5d7a4edf3e 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:14:43.883Z 
│                       ├ [92]  ╭ VulnerabilityID : CVE-2026-35340 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35340 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:170185ada68eb8c7ed4ff6d4868c5bc4aeb2b2648fcec98f90ab
│                       │       │                   f8544baa0fcb 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:12:01.5Z 
│                       ├ [93]  ╭ VulnerabilityID : CVE-2026-35341 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6eb2cb92383e6778038f0e8cb1aa7aa751f975f09869618f3012
│                       │       │                   bfa90a512999 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:05:55.067Z 
│                       ├ [94]  ╭ VulnerabilityID : CVE-2026-35342 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35342 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a6377950e247d81de7416fb5ed0bd4caa908f563e534865664b6
│                       │       │                   9328971cabdf 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:11:32.34Z 
│                       ├ [95]  ╭ VulnerabilityID : CVE-2026-35343 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35343 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:776ede412a752ff87d90efa1b562d49802f45a8e025a121f9f9b
│                       │       │                   084eba2521b9 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:10:47.587Z 
│                       ├ [96]  ╭ VulnerabilityID : CVE-2026-35344 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:00a951b550eae38dfadd72203ffeb988b9e4147aacd15afc91e9
│                       │       │                   46b468e4b4b5 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:09:48.593Z 
│                       ├ [97]  ╭ VulnerabilityID : CVE-2026-35345 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6d030569beb92ef0bdbe5214e6eecc3adbedcb9740e23f5451bd
│                       │       │                   c9dbcf9abcc3 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:04:25.093Z 
│                       ├ [98]  ╭ VulnerabilityID : CVE-2026-35346 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35346 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3261e6cde94a191ab27c9c8f02c4e43171fab090c9e3b2060f7b
│                       │       │                   17055a0e839f 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:28:38.493Z 
│                       ├ [99]  ╭ VulnerabilityID : CVE-2026-35347 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35347 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:e737fadd81828c1379335d1528098f1f89464411ff90e13ddbb8
│                       │       │                   b0c8b462e2a1 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:28:23.273Z 
│                       ├ [100] ╭ VulnerabilityID : CVE-2026-35348 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:04bae7963d2564de7095d171518146ac6953a3d92b907cb93999
│                       │       │                   b25c613dfcdc 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T18:57:20.927Z 
│                       ├ [101] ╭ VulnerabilityID : CVE-2026-35349 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35349 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6359d927eb0b22769b2eac6246d54406c1128a4ede46f19c27f1
│                       │       │                   40b454c1fec7 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:28:17.903Z 
│                       ├ [102] ╭ VulnerabilityID : CVE-2026-35350 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:40948cc7eb1b79c0ebcb89e6f3fe40fac1f1f8eb03888a65ec25
│                       │       │                   913febd066dd 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:04:01.207Z 
│                       ├ [103] ╭ VulnerabilityID : CVE-2026-35351 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:928ee8f92373dbe22a2cfa2389bca39d99a3c49ac00b9df911b1
│                       │       │                   41f43d0717d9 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:28:10.22Z 
│                       ├ [104] ╭ VulnerabilityID : CVE-2026-35352 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:13d2018ebc8bec5f0b107fe3bde258aa286ed5cc3bc5219ac898
│                       │       │                   09600e5b60ab 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T18:16:28.37Z 
│                       ├ [105] ╭ VulnerabilityID : CVE-2026-35353 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35353 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0b3426d925dff114c251bf412c63d3b8b606cf2fff99f2100621
│                       │       │                   55b9c5acc5ea 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:27:39.04Z 
│                       ├ [106] ╭ VulnerabilityID : CVE-2026-35354 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f14907d8102d4609494de108193342239e31fa43d5f7d46340b6
│                       │       │                   c79562e3ed9b 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:04:08.917Z 
│                       ├ [107] ╭ VulnerabilityID : CVE-2026-35355 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35355 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:49fd5641aa483bf16754c8f99ac3c473dbd101ba0c799094822a
│                       │       │                   2bf13f3c8b36 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:27:34.007Z 
│                       ├ [108] ╭ VulnerabilityID : CVE-2026-35356 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35356 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:59e3aaebd631b82b7c40c36ddadb8d2a5f388abdbb60c66aa735
│                       │       │                   b0e1998f0768 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:27:28.787Z 
│                       ├ [109] ╭ VulnerabilityID : CVE-2026-35357 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3caf0625a293b62f896721f322a460e1b09b92965f747bc029df
│                       │       │                   d0faee228b53 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:02:53.557Z 
│                       ├ [110] ╭ VulnerabilityID : CVE-2026-35358 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35358 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3d42eabdbd6e072e7bc8ad8839fbae2e3c742697c444f23cd534
│                       │       │                   5f7c93d2ef34 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T19:03:00.59Z 
│                       ├ [111] ╭ VulnerabilityID : CVE-2026-35359 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:bb0c538093455995c93d456fe33af6fab6b34453bbd7a41b5ce5
│                       │       │                   e76eb7878172 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:02:25.72Z 
│                       ├ [112] ╭ VulnerabilityID : CVE-2026-35360 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:5c95c57167c4fa8b02355e2885e821cd3389b4971a58e81970ba
│                       │       │                   e3760d53e879 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:02:11.56Z 
│                       ├ [113] ╭ VulnerabilityID : CVE-2026-35361 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35361 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:cf4872446d52c4992e6b44252a3873c0b48f7cc65539acc98e0a
│                       │       │                   4eddf37cd179 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:27:20.527Z 
│                       ├ [114] ╭ VulnerabilityID : CVE-2026-35362 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35362 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:a26247c116ed02aab32fc5d08fee550c6ca6a1a9d7e6f16c4981
│                       │       │                   17ff74296d94 
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
│                       │       ╰ LastModifiedDate: 2026-04-27T12:26:40.533Z 
│                       ├ [115] ╭ VulnerabilityID : CVE-2026-35363 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f35abdba9fe3fe3f70c9fd6e5205629216ee0f32873438f2c42f
│                       │       │                   bd6481d6cfc4 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:02:00.463Z 
│                       ├ [116] ╭ VulnerabilityID : CVE-2026-35364 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:cee5ca0625697b5659c557f8d71aa1d13816a155720e0604df71
│                       │       │                   0f7fbbb768b1 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:19:11.777Z 
│                       ├ [117] ╭ VulnerabilityID : CVE-2026-35365 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35365 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:64a7a28bc40fdb86a285e2071d7bbbfe1254bfded1a81ad9446c
│                       │       │                   8958285e5004 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T18:53:45.707Z 
│                       ├ [118] ╭ VulnerabilityID : CVE-2026-35366 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35366 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:249960a0346f70e09dfa007e38edca85d6f99a6285535e39d14d
│                       │       │                   d29af5024ead 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T18:52:42.39Z 
│                       ├ [119] ╭ VulnerabilityID : CVE-2026-35367 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:57d8ded88b49c53a64504f3565473e55f7a7f24e7c36d9d242aa
│                       │       │                   c8b2d01a1361 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:19:05.067Z 
│                       ├ [120] ╭ VulnerabilityID : CVE-2026-35368 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:12bfb0f118000c77018996aa7a71cd17097a428522b487e3fc2e
│                       │       │                   db49c99cd4f2 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:18:55.67Z 
│                       ├ [121] ╭ VulnerabilityID : CVE-2026-35369 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35369 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ce541c9e3a8e1d7c43ad3f7bca07ebf90ac236e0681b2af34745
│                       │       │                   ced36a420626 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T18:50:23.537Z 
│                       ├ [122] ╭ VulnerabilityID : CVE-2026-35370 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3af27642bc878930f2332e3d4987f74efd6d676062c7f1a88cfb
│                       │       │                   f608515c34ef 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:02:44.33Z 
│                       ├ [123] ╭ VulnerabilityID : CVE-2026-35371 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:60526ed06b73a8328ee749e45ef19aa544aab9a9a9f978e3fd7c
│                       │       │                   1f61c85ad59d 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:02:06.183Z 
│                       ├ [124] ╭ VulnerabilityID : CVE-2026-35372 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35372 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:99446125cacd8b0308bd3dbc50610d09baa435585a275edd5604
│                       │       │                   f0372bcf7377 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T18:49:46.51Z 
│                       ├ [125] ╭ VulnerabilityID : CVE-2026-35373 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:0a22dc56dc29e94e124adc30e29beffaea18e2030f91d3f40a54
│                       │       │                   7ec21119d15b 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T20:01:25.93Z 
│                       ├ [126] ╭ VulnerabilityID : CVE-2026-35374 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6db0550067ae17600e580f12c3f806fc45abbf9b29533ec75aa9
│                       │       │                   d4460582c829 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T19:22:14.457Z 
│                       ├ [127] ╭ VulnerabilityID : CVE-2026-35375 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35375 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ec44f4b15f18d8c20f8817899eb3159741b4a20bf5ee0377feca
│                       │       │                   dd386b521d05 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T19:13:37.293Z 
│                       ├ [128] ╭ VulnerabilityID : CVE-2026-35376 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35376 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6782948eb79bc66392958b00ae418b77385dfd4942b841a20cfc
│                       │       │                   421289d5e1d0 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T19:06:31.93Z 
│                       ├ [129] ╭ VulnerabilityID : CVE-2026-35377 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:398eb455bcfb0078067510c31601c1a5e697b61ab87fbf31ab31
│                       │       │                   55d6381a1bd3 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:06:46.293Z 
│                       ├ [130] ╭ VulnerabilityID : CVE-2026-35378 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35378 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:503111172b7280d9365c442216fbc852bd59a64d02f3d9de1335
│                       │       │                   812db58bdd43 
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
│                       │       ╰ LastModifiedDate: 2026-05-04T18:48:36.02Z 
│                       ├ [131] ╭ VulnerabilityID : CVE-2026-35379 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35379 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:2e8402a3b1859f2951a343860d0e9645379da96bbd3881be80e4
│                       │       │                   69f3878cbeea 
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
│                       │       ╰ LastModifiedDate: 2026-04-29T15:59:08.45Z 
│                       ├ [132] ╭ VulnerabilityID : CVE-2026-35380 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35380 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:6fa3caac2dc5edd0692638e4803e1498936e21322b413dca8e2c
│                       │       │                   c57956ede6b4 
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
│                       │       ╰ LastModifiedDate: 2026-04-29T15:57:19.427Z 
│                       ├ [133] ╭ VulnerabilityID : CVE-2026-35381 
│                       │       ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │       ├ PkgName         : rust-coreutils 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=
│                       │       │                  │       amd64&distro=ubuntu-25.10 
│                       │       │                  ╰ UID : ebefeb85901fc403 
│                       │       ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35381 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8aa9b20229d9568d3568b3d33c00c48aea03ea878f25e0774549
│                       │       │                   d08a5a841034 
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
│                       │       ╰ LastModifiedDate: 2026-04-24T19:19:34.493Z 
│                       ├ [134] ╭ VulnerabilityID : CVE-2025-45582 
│                       │       ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │       ├ PkgName         : tar 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 41081f85f98b9d6a 
│                       │       ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-45582 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:53075295612ce50098fcf1731c1108456b19433d2bcdf68a3385
│                       │       │                   74759b6230c0 
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
│                       │       │                  ├ [7] : https://errata.rockylinux.org/RLSA-2026:0002 
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
│                       │       ╰ LastModifiedDate: 2025-11-02T01:15:32.307Z 
│                       ├ [135] ╭ VulnerabilityID : CVE-2026-5704 
│                       │       ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │       ├ PkgName         : tar 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&
│                       │       │                  │       distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 41081f85f98b9d6a 
│                       │       ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5704 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:aedc50ab8507aad387fe739b3312e605011bce93719e56efb12c
│                       │       │                   4d8442018db5 
│                       │       ├ Title           : tar: tar: Hidden file injection via crafted archives 
│                       │       ├ Description     : A flaw was found in tar. A remote attacker could exploit
│                       │       │                   this vulnerability by crafting a malicious archive, leading
│                       │       │                    to hidden file injection with fully attacker-controlled
│                       │       │                   content. This bypasses pre-extraction inspection
│                       │       │                   mechanisms, potentially allowing an attacker to introduce
│                       │       │                   malicious files onto a system without detection. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ─ [0]: CWE-434 
│                       │       ├ VendorSeverity   ╭ nvd   : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:
│                       │       │                  │        │           H/A:N 
│                       │       │                  │        ╰ V3Score : 5.5 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:
│                       │       │                           │           H/A:N 
│                       │       │                           ╰ V3Score : 5 
│                       │       ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/04/11
│                       │       │                  │      /10 
│                       │       │                  ├ [1]: http://www.openwall.com/lists/oss-security/2026/04/11
│                       │       │                  │      /11 
│                       │       │                  ├ [2]: http://www.openwall.com/lists/oss-security/2026/04/12/2 
│                       │       │                  ├ [3]: https://access.redhat.com/security/cve/CVE-2026-5704 
│                       │       │                  ├ [4]: https://bugzilla.redhat.com/show_bug.cgi?id=2455360 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-5704 
│                       │       │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-5704 
│                       │       ├ PublishedDate   : 2026-04-06T16:16:42.14Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T20:08:59.92Z 
│                       ├ [136] ╭ VulnerabilityID : CVE-2026-27456 
│                       │       ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : util-linux 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:8cf721ef841814cf4a1d1e9da1ae397b7e42be39c69c47958a47
│                       │       │                   b2ed0060ddf5 
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
│                       │       ├ VendorSeverity   ╭ azure : 2 
│                       │       │                  ├ julia : 2 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                  │        │           N/A:N 
│                       │       │                  │        ╰ V3Score : 4.7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:
│                       │       │                           │           N/A:N 
│                       │       │                           ╰ V3Score : 4.7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │       │                  ├ [1]: https://github.com/util-linux/util-linux/commit/5e390
│                       │       │                  │      467b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │       │                  ├ [2]: https://github.com/util-linux/util-linux/releases/tag
│                       │       │                  │      /v2.41.4 
│                       │       │                  ├ [3]: https://github.com/util-linux/util-linux/security/adv
│                       │       │                  │      isories/GHSA-qq4x-vfq4-9h9g 
│                       │       │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │       │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │       ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │       ╰ LastModifiedDate: 2026-04-22T16:08:55.1Z 
│                       ├ [137] ╭ VulnerabilityID : CVE-2026-3184 
│                       │       ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │       ├ PkgName         : util-linux 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64
│                       │       │                  │       &distro=ubuntu-25.10 
│                       │       │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │       ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:839a5d4a694ada2b99a7b2ef0b88d807a1981ee504a386cef28d
│                       │       │                   8d001260d706 
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
│                       │       ╰ LastModifiedDate: 2026-05-01T19:29:51.02Z 
│                       ├ [138] ╭ VulnerabilityID : CVE-2026-43961 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.5?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 2541eefb3c0876e6 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:3f90f4bf96af9156d9b2a500b0249413302e72650a76b4718a16
│                       │       │                   3fa5008f1a92 
│                       │       ├ Description     : [Unknown description] 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-6
│                       │                          │      6hr-7p6x-x5j3 
│                       │                          ├ [1]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │                          ├ [2]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                          ╰ [3]: https://www.openwall.com/lists/oss-security/2026/05/1
│                       │                                 4/7 
│                       ├ [139] ╭ VulnerabilityID : CVE-2026-46483 
│                       │       ├ PkgID           : vim@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : vim 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.0967-1ubuntu6.5?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 2541eefb3c0876e6 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:ecfcbd687a9aa25ef2999a1ec1e7daa01e2c286199ab8253d8f4
│                       │       │                   a6dd51b2dabd 
│                       │       ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0479, a command injection vulnerability exists in
│                       │       │                   tar#Vimuntar() in
│                       │       │                   runtime/autoload/tar.vim when decompressing .tgz archives
│                       │       │                   on Unix-like systems. The function builds :!gunzip and
│                       │       │                   :!gzip -d commands using shellescape(tartail) without the
│                       │       │                   {special} flag, allowing a crafted archive filename to
│                       │       │                   trigger Vim cmdline-special expansion and execute shell
│                       │       │                   commands in the user's context. This vulnerability is fixed
│                       │       │                    in 9.2.0479. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-88 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                  │        │           H/A:H 
│                       │       │                  │        ╰ V3Score : 7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                       │       │                  │      5f1a141b0d67af2aa38a1 
│                       │       │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                       │       │                  │      5f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │       │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │       │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2
│                       │       │                  │      fpv-9ff7-xg5w 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │       ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │       ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ├ [140] ╭ VulnerabilityID : CVE-2026-43961 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.5?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 8a15c1b947cca3b8 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:34021dc0a69a38b35bb7aa691cc8ae14ff6616424d43a2669994
│                       │       │                   0271e0824293 
│                       │       ├ Description     : [Unknown description] 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-6
│                       │                          │      6hr-7p6x-x5j3 
│                       │                          ├ [1]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │                          ├ [2]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                          ╰ [3]: https://www.openwall.com/lists/oss-security/2026/05/1
│                       │                                 4/7 
│                       ├ [141] ╭ VulnerabilityID : CVE-2026-46483 
│                       │       ├ PkgID           : vim-common@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : vim-common 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.0967-1ubuntu6.5?arch=a
│                       │       │                  │       ll&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 8a15c1b947cca3b8 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:f392b82e535e624db99353507f35ccc90dc02e787b9ec7965012
│                       │       │                   b848cc3d0e39 
│                       │       ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0479, a command injection vulnerability exists in
│                       │       │                   tar#Vimuntar() in
│                       │       │                   runtime/autoload/tar.vim when decompressing .tgz archives
│                       │       │                   on Unix-like systems. The function builds :!gunzip and
│                       │       │                   :!gzip -d commands using shellescape(tartail) without the
│                       │       │                   {special} flag, allowing a crafted archive filename to
│                       │       │                   trigger Vim cmdline-special expansion and execute shell
│                       │       │                   commands in the user's context. This vulnerability is fixed
│                       │       │                    in 9.2.0479. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-88 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                  │        │           H/A:H 
│                       │       │                  │        ╰ V3Score : 7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                       │       │                  │      5f1a141b0d67af2aa38a1 
│                       │       │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                       │       │                  │      5f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │       │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │       │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2
│                       │       │                  │      fpv-9ff7-xg5w 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │       ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │       ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ├ [142] ╭ VulnerabilityID : CVE-2026-43961 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.5?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : a4708db604f82859 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:81c327caa8eef6b989bbe78b37c3574ad01a7fe3115af82286cb
│                       │       │                   bbbfb4375eef 
│                       │       ├ Description     : [Unknown description] 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-6
│                       │                          │      6hr-7p6x-x5j3 
│                       │                          ├ [1]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │                          ├ [2]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                          ╰ [3]: https://www.openwall.com/lists/oss-security/2026/05/1
│                       │                                 4/7 
│                       ├ [143] ╭ VulnerabilityID : CVE-2026-46483 
│                       │       ├ PkgID           : vim-runtime@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : vim-runtime 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.0967-1ubuntu6.5?arch=
│                       │       │                  │       all&distro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : a4708db604f82859 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:73a66670e2c55ebcc42d3d4a236a1b4768e7b3379b3119230ab6
│                       │       │                   449720d26aa7 
│                       │       ├ Title           : vim: command injection when decompressing .tgz archives 
│                       │       ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │       │                   9.2.0479, a command injection vulnerability exists in
│                       │       │                   tar#Vimuntar() in
│                       │       │                   runtime/autoload/tar.vim when decompressing .tgz archives
│                       │       │                   on Unix-like systems. The function builds :!gunzip and
│                       │       │                   :!gzip -d commands using shellescape(tartail) without the
│                       │       │                   {special} flag, allowing a crafted archive filename to
│                       │       │                   trigger Vim cmdline-special expansion and execute shell
│                       │       │                   commands in the user's context. This vulnerability is fixed
│                       │       │                    in 9.2.0479. 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ CweIDs           ╭ [0]: CWE-78 
│                       │       │                  ╰ [1]: CWE-88 
│                       │       ├ VendorSeverity   ╭ azure : 1 
│                       │       │                  ├ nvd   : 3 
│                       │       │                  ├ redhat: 2 
│                       │       │                  ╰ ubuntu: 2 
│                       │       ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                  │        │           H/A:H 
│                       │       │                  │        ╰ V3Score : 7 
│                       │       │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                       │       │                           │           H/A:H 
│                       │       │                           ╰ V3Score : 7 
│                       │       ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                       │       │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                       │       │                  │      5f1a141b0d67af2aa38a1 
│                       │       │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                       │       │                  │      5f1a141b0d67af2aa38a1 (v9.2.0479) 
│                       │       │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                       │       │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2
│                       │       │                  │      fpv-9ff7-xg5w 
│                       │       │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                       │       │                  ├ [6]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │       │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                       │       ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                       │       ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
│                       ├ [144] ╭ VulnerabilityID : CVE-2021-31879 
│                       │       ├ PkgID           : wget@1.25.0-2ubuntu3 
│                       │       ├ PkgName         : wget 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu3?arch=amd64&distr
│                       │       │                  │       o=ubuntu-25.10 
│                       │       │                  ╰ UID : 3ae34724b04a04d7 
│                       │       ├ InstalledVersion: 1.25.0-2ubuntu3 
│                       │       ├ Status          : affected 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:994b9c9b43defb849d2cb9d80755f481f1a033b15374af7c9e88
│                       │       │                   3d31cc46ce04 
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
│                       │       ╰ LastModifiedDate: 2024-11-21T06:06:25.02Z 
│                       ├ [145] ╭ VulnerabilityID : CVE-2026-43961 
│                       │       ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.5 
│                       │       ├ PkgName         : xxd 
│                       │       ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.5?arch=amd64&di
│                       │       │                  │       stro=ubuntu-25.10&epoch=2 
│                       │       │                  ╰ UID : 526950e53908bbfb 
│                       │       ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                       │       ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                       │       ├ Status          : fixed 
│                       │       ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                       │       │                  │         e1b66d581b273a93f26dd 
│                       │       │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                       │       │                            8e78ed55fdba5c7f3a301 
│                       │       ├ SeveritySource  : ubuntu 
│                       │       ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-43961 
│                       │       ├ DataSource       ╭ ID  : ubuntu 
│                       │       │                  ├ Name: Ubuntu CVE Tracker 
│                       │       │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │       ├ Fingerprint     : sha256:b599d080a27122e175ec9c47eec4bc3f6e0a218ffd2b7c14137c
│                       │       │                   1b8447b85db1 
│                       │       ├ Description     : [Unknown description] 
│                       │       ├ Severity        : MEDIUM 
│                       │       ├ VendorSeverity   ─ ubuntu: 2 
│                       │       ╰ References       ╭ [0]: https://github.com/vim/vim/security/advisories/GHSA-6
│                       │                          │      6hr-7p6x-x5j3 
│                       │                          ├ [1]: https://ubuntu.com/security/notices/USN-8415-1 
│                       │                          ├ [2]: https://www.cve.org/CVERecord?id=CVE-2026-43961 
│                       │                          ╰ [3]: https://www.openwall.com/lists/oss-security/2026/05/1
│                       │                                 4/7 
│                       ╰ [146] ╭ VulnerabilityID : CVE-2026-46483 
│                               ├ PkgID           : xxd@2:9.1.0967-1ubuntu6.5 
│                               ├ PkgName         : xxd 
│                               ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.0967-1ubuntu6.5?arch=amd64&di
│                               │                  │       stro=ubuntu-25.10&epoch=2 
│                               │                  ╰ UID : 526950e53908bbfb 
│                               ├ InstalledVersion: 2:9.1.0967-1ubuntu6.5 
│                               ├ FixedVersion    : 2:9.1.0967-1ubuntu6.6 
│                               ├ Status          : fixed 
│                               ├ Layer            ╭ Digest: sha256:f4fc0298d5eed4260e6d92dc879ae32c7512a04750f
│                               │                  │         e1b66d581b273a93f26dd 
│                               │                  ╰ DiffID: sha256:0e8797579df3ce309d5303cc6ea9d5a433cd28fdc7b
│                               │                            8e78ed55fdba5c7f3a301 
│                               ├ SeveritySource  : ubuntu 
│                               ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46483 
│                               ├ DataSource       ╭ ID  : ubuntu 
│                               │                  ├ Name: Ubuntu CVE Tracker 
│                               │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                               ├ Fingerprint     : sha256:833d61606d7c50dfbf10bcadbc404c3aeaa19a2153f3d1424453
│                               │                   1d0798f9667e 
│                               ├ Title           : vim: command injection when decompressing .tgz archives 
│                               ├ Description     : Vim is an open source, command line text editor. Prior to
│                               │                   9.2.0479, a command injection vulnerability exists in
│                               │                   tar#Vimuntar() in
│                               │                   runtime/autoload/tar.vim when decompressing .tgz archives
│                               │                   on Unix-like systems. The function builds :!gunzip and
│                               │                   :!gzip -d commands using shellescape(tartail) without the
│                               │                   {special} flag, allowing a crafted archive filename to
│                               │                   trigger Vim cmdline-special expansion and execute shell
│                               │                   commands in the user's context. This vulnerability is fixed
│                               │                    in 9.2.0479. 
│                               ├ Severity        : MEDIUM 
│                               ├ CweIDs           ╭ [0]: CWE-78 
│                               │                  ╰ [1]: CWE-88 
│                               ├ VendorSeverity   ╭ azure : 1 
│                               │                  ├ nvd   : 3 
│                               │                  ├ redhat: 2 
│                               │                  ╰ ubuntu: 2 
│                               ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                               │                  │        │           H/A:H 
│                               │                  │        ╰ V3Score : 7 
│                               │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:
│                               │                           │           H/A:H 
│                               │                           ╰ V3Score : 7 
│                               ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46483 
│                               │                  ├ [1]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                               │                  │      5f1a141b0d67af2aa38a1 
│                               │                  ├ [2]: https://github.com/vim/vim/commit/3fb5e58fbc63d86a3e6
│                               │                  │      5f1a141b0d67af2aa38a1 (v9.2.0479) 
│                               │                  ├ [3]: https://github.com/vim/vim/releases/tag/v9.2.0479 
│                               │                  ├ [4]: https://github.com/vim/vim/security/advisories/GHSA-2
│                               │                  │      fpv-9ff7-xg5w 
│                               │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-46483 
│                               │                  ├ [6]: https://ubuntu.com/security/notices/USN-8415-1 
│                               │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-46483 
│                               ├ PublishedDate   : 2026-05-15T15:16:54.237Z 
│                               ╰ LastModifiedDate: 2026-05-19T12:27:28.72Z 
╰ [1] ╭ Target  : Java 
      ├ Class   : lang-pkgs 
      ├ Type    : jar 
      ╰ Packages 
```
