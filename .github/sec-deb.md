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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b489f06327943d9fbf020f8ab76f19a036715c38b6c2a5818a1ca
│                       │      │                   efdfdadb527 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:665f5122e993502efb9cd4ebe84a90e8c2c4f551d3f64c4a17446
│                       │      │                   b2ca5105ad6 
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
│                       │      │                  ├ photon: 2 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d816b5c5f98d6a6dfa166a6e58c8605fb9bc81b5dc716f8f00c4b
│                       │      │                   1498b5322e8 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5cb47cf52d270e8422a925e7a15bfc6b7f2cec3c49bd0f370c506
│                       │      │                   7c41b09ff53 
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
│                       │      │                  ├ photon: 2 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b59451970adf8a1581b35df9d6305bd413ebb33c802785452d5c5
│                       │      │                   6eb713d9a6a 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fd4b390d711570260108076df8a571a9536316a9afcdc1634f12d
│                       │      │                   1032ccec227 
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
│                       │      │                  ├ photon: 2 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b4d927ed8384a7560ea3a2905b64fadb31313cfad5ad839e68d0f
│                       │      │                   1516bff54ce 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e24f94fb69a99080cf2177cb73a4a9103879776ab2a9a66dc1782
│                       │      │                   f9f6b00c6db 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4787fdbda97459e324f39ffced5d926df45951f875b06d60446b1
│                       │      │                   6440da2efbd 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:840ada88b879e86f202c4724dc8b952a9c469bb429490bc8a0115
│                       │      │                   12c8497529b 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:14ddcfe4e88ba1e99c88b19fa5691c9db9126c4dfb09f98084643
│                       │      │                   08711679737 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:10d233c73beef9080b28320e0de8d9260d59b8e47dfddf7fc435c
│                       │      │                   293743090a1 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:58823497a5ee06f2a8b201d6fbc1213c6c1e96f840fe19e54b800
│                       │      │                   076352e25ed 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:82cc104ddbdbecb867608015e65c06b849e4fd52790e26938daea
│                       │      │                   c33f8e15274 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0ce07dfcf36f9b0c053428d3b9b3ccbc825af70dd61e45474defd
│                       │      │                   a5a21295796 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e9f7f7a994f6468533a128dc431b3762efc99dd03d9866e8ae232
│                       │      │                   b9f4a88c458 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bf768009a6309fa9d828ae08e9db3b9daeec81878ea42417f496b
│                       │      │                   232477a7151 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-2236 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:74be1c7f7a375f05afaf282f53f8719054c84af7843c6a7e251ad
│                       │      │                   5ec7612a220 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:73080cc628d0a6f138552594964c5c2a1295b3f995abee94490dd
│                       │      │                   667e338e060 
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
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d3c9c08af4f597e0c80655201af825bce168f141b1f3cfb48ba74
│                       │      │                   6f634705fb1 
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
│                       │      │                  ├ photon: 2 
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
│                       ├ [20] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : e278fd35c2ddbe27 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4fb681293ea9256f186188ad8cd4a90058e6fe6a4babf70db7980
│                       │      │                   e89ad1df6e7 
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
│                       ├ [21] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : e278fd35c2ddbe27 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f03379f5faf2765d2831162b7fdcd34654fabf8a7bd6a4945ce59
│                       │      │                   b823724be92 
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
│                       │      │                  ├ photon: 2 
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
│                       ├ [22] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13@3.13.7-1ubuntu0.4?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : d39243325c040cfa 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:77bbe9d5057ab7285312fb666791266622d8dd06b8a1d3946d152
│                       │      │                   139a313b950 
│                       │      ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │      ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │      │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │      │                   (a base class) and so does not use io.open_code() to read
│                       │      │                   the .pyc files. sys.audit handlers for this audit event
│                       │      │                   therefore do not fire. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-668 
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 2 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/05/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:10950 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │      │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │      │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │      │                  ├ [11]: https://bugzilla.redhat.com/2457409 
│                       │      │                  ├ [12]: https://bugzilla.redhat.com/2457932 
│                       │      │                  ├ [13]: https://bugzilla.redhat.com/2458049 
│                       │      │                  ├ [14]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │      │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │      │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │      │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │      │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │      │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │      │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │      │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │      │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │      │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │      │                  ├ [26]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-13837 
│                       │      │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-15282 
│                       │      │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-59375 
│                       │      │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-6075 
│                       │      │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-0672 
│                       │      │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-1502 
│                       │      │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-2297 
│                       │      │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-3644 
│                       │      │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4224 
│                       │      │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4519 
│                       │      │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4786 
│                       │      │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-6100 
│                       │      │                  ├ [38]: https://errata.almalinux.org/8/ALSA-2026-10950.html 
│                       │      │                  ├ [39]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │      │                  ├ [40]: https://github.com/python/cpython/commit/482d6f8bdba9
│                       │      │                  │       da3725d272e8bb4a2d25fb6a603e 
│                       │      │                  ├ [41]: https://github.com/python/cpython/commit/69ddd9bb2cc4
│                       │      │                  │       bd69b1565647c18659c6a789ccd9 
│                       │      │                  ├ [42]: https://github.com/python/cpython/commit/876858c9f65d
│                       │      │                  │       9ab656c7fa639f268ce7856d89dd 
│                       │      │                  ├ [43]: https://github.com/python/cpython/commit/a51b1b512de1
│                       │      │                  │       d56b3714b65628a2eae2b07e535e 
│                       │      │                  ├ [44]: https://github.com/python/cpython/commit/e58e9802b9be
│                       │      │                  │       c5cdbf48fc9bf1da5f4fda482e86 
│                       │      │                  ├ [45]: https://github.com/python/cpython/issues/145506 
│                       │      │                  ├ [46]: https://github.com/python/cpython/pull/145507 
│                       │      │                  ├ [47]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │      │                  ├ [48]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │      │                  ├ [49]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ╰ [50]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [23] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13-minimal@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13-minimal 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-minimal@3.13.7-1ubuntu0.
│                       │      │                  │       4?arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 9682446bb647ab44 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2c31b0120e86f1712cea75aa0c9543b9fd74f6f5adcb626c6ae7d
│                       │      │                   5553b55e75c 
│                       │      ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │      ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │      │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │      │                   (a base class) and so does not use io.open_code() to read
│                       │      │                   the .pyc files. sys.audit handlers for this audit event
│                       │      │                   therefore do not fire. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-668 
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 2 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/05/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:10950 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │      │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │      │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │      │                  ├ [11]: https://bugzilla.redhat.com/2457409 
│                       │      │                  ├ [12]: https://bugzilla.redhat.com/2457932 
│                       │      │                  ├ [13]: https://bugzilla.redhat.com/2458049 
│                       │      │                  ├ [14]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │      │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │      │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │      │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │      │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │      │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │      │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │      │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │      │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │      │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │      │                  ├ [26]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-13837 
│                       │      │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-15282 
│                       │      │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-59375 
│                       │      │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-6075 
│                       │      │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-0672 
│                       │      │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-1502 
│                       │      │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-2297 
│                       │      │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-3644 
│                       │      │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4224 
│                       │      │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4519 
│                       │      │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4786 
│                       │      │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-6100 
│                       │      │                  ├ [38]: https://errata.almalinux.org/8/ALSA-2026-10950.html 
│                       │      │                  ├ [39]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │      │                  ├ [40]: https://github.com/python/cpython/commit/482d6f8bdba9
│                       │      │                  │       da3725d272e8bb4a2d25fb6a603e 
│                       │      │                  ├ [41]: https://github.com/python/cpython/commit/69ddd9bb2cc4
│                       │      │                  │       bd69b1565647c18659c6a789ccd9 
│                       │      │                  ├ [42]: https://github.com/python/cpython/commit/876858c9f65d
│                       │      │                  │       9ab656c7fa639f268ce7856d89dd 
│                       │      │                  ├ [43]: https://github.com/python/cpython/commit/a51b1b512de1
│                       │      │                  │       d56b3714b65628a2eae2b07e535e 
│                       │      │                  ├ [44]: https://github.com/python/cpython/commit/e58e9802b9be
│                       │      │                  │       c5cdbf48fc9bf1da5f4fda482e86 
│                       │      │                  ├ [45]: https://github.com/python/cpython/issues/145506 
│                       │      │                  ├ [46]: https://github.com/python/cpython/pull/145507 
│                       │      │                  ├ [47]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │      │                  ├ [48]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │      │                  ├ [49]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ╰ [50]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [24] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13-stdlib@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13-stdlib 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-stdlib@3.13.7-1ubuntu0.4
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 80f30a21647be5ac 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:730758242bdbca1512b6d2da16a4e514cbcc751dbb9a9173ea149
│                       │      │                   a182b7824be 
│                       │      ├ Title           : cpython: CPython: Logging Bypass in Legacy .pyc File Handling 
│                       │      ├ Description     : The import hook in CPython that handles legacy *.pyc files
│                       │      │                   (SourcelessFileLoader) is incorrectly handled in FileLoader
│                       │      │                   (a base class) and so does not use io.open_code() to read
│                       │      │                   the .pyc files. sys.audit handlers for this audit event
│                       │      │                   therefore do not fire. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-668 
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 2 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.3 
│                       │      ├ References       ╭ [0] : http://www.openwall.com/lists/oss-security/2026/03/05/6 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:10950 
│                       │      │                  ├ [2] : https://access.redhat.com/security/cve/CVE-2026-2297 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2395108 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2408891 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/2418084 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/2431366 
│                       │      │                  ├ [7] : https://bugzilla.redhat.com/2431374 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2444691 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/2448168 
│                       │      │                  ├ [10]: https://bugzilla.redhat.com/2448181 
│                       │      │                  ├ [11]: https://bugzilla.redhat.com/2457409 
│                       │      │                  ├ [12]: https://bugzilla.redhat.com/2457932 
│                       │      │                  ├ [13]: https://bugzilla.redhat.com/2458049 
│                       │      │                  ├ [14]: https://bugzilla.redhat.com/show_bug.cgi?id=2395108 
│                       │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2408891 
│                       │      │                  ├ [16]: https://bugzilla.redhat.com/show_bug.cgi?id=2418084 
│                       │      │                  ├ [17]: https://bugzilla.redhat.com/show_bug.cgi?id=2431366 
│                       │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2431374 
│                       │      │                  ├ [19]: https://bugzilla.redhat.com/show_bug.cgi?id=2444691 
│                       │      │                  ├ [20]: https://bugzilla.redhat.com/show_bug.cgi?id=2448168 
│                       │      │                  ├ [21]: https://bugzilla.redhat.com/show_bug.cgi?id=2448181 
│                       │      │                  ├ [22]: https://bugzilla.redhat.com/show_bug.cgi?id=2449649 
│                       │      │                  ├ [23]: https://bugzilla.redhat.com/show_bug.cgi?id=2457409 
│                       │      │                  ├ [24]: https://bugzilla.redhat.com/show_bug.cgi?id=2457932 
│                       │      │                  ├ [25]: https://bugzilla.redhat.com/show_bug.cgi?id=2458049 
│                       │      │                  ├ [26]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-13837 
│                       │      │                  ├ [27]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-15282 
│                       │      │                  ├ [28]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-59375 
│                       │      │                  ├ [29]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       25-6075 
│                       │      │                  ├ [30]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-0672 
│                       │      │                  ├ [31]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-1502 
│                       │      │                  ├ [32]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-2297 
│                       │      │                  ├ [33]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-3644 
│                       │      │                  ├ [34]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4224 
│                       │      │                  ├ [35]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4519 
│                       │      │                  ├ [36]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4786 
│                       │      │                  ├ [37]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-6100 
│                       │      │                  ├ [38]: https://errata.almalinux.org/8/ALSA-2026-10950.html 
│                       │      │                  ├ [39]: https://errata.rockylinux.org/RLSA-2026:19177 
│                       │      │                  ├ [40]: https://github.com/python/cpython/commit/482d6f8bdba9
│                       │      │                  │       da3725d272e8bb4a2d25fb6a603e 
│                       │      │                  ├ [41]: https://github.com/python/cpython/commit/69ddd9bb2cc4
│                       │      │                  │       bd69b1565647c18659c6a789ccd9 
│                       │      │                  ├ [42]: https://github.com/python/cpython/commit/876858c9f65d
│                       │      │                  │       9ab656c7fa639f268ce7856d89dd 
│                       │      │                  ├ [43]: https://github.com/python/cpython/commit/a51b1b512de1
│                       │      │                  │       d56b3714b65628a2eae2b07e535e 
│                       │      │                  ├ [44]: https://github.com/python/cpython/commit/e58e9802b9be
│                       │      │                  │       c5cdbf48fc9bf1da5f4fda482e86 
│                       │      │                  ├ [45]: https://github.com/python/cpython/issues/145506 
│                       │      │                  ├ [46]: https://github.com/python/cpython/pull/145507 
│                       │      │                  ├ [47]: https://linux.oracle.com/cve/CVE-2026-2297.html 
│                       │      │                  ├ [48]: https://linux.oracle.com/errata/ELSA-2026-10950.html 
│                       │      │                  ├ [49]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ╰ [50]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-05-01T16:16:30.11Z 
│                       ├ [25] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5ded7bb8194896b780c5d40b9ec0eccf3b9b27f49997aade983b9
│                       │      │                   1ea1841da6c 
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
│                       ├ [26] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:42e7547ddf5744686fdc24c12d0593661ce507ce82eb66e4e5758
│                       │      │                   f42796c7684 
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
│                       │      │                  ├ photon: 2 
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
│                       ├ [27] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libsystemd0@257.9-0ubuntu2.5 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@257.9-0ubuntu2.5?arch=amd6
│                       │      │                  │       4&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ec55cdfad517f3cc 
│                       │      ├ InstalledVersion: 257.9-0ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ea90c0cc38ffb9aa798850c954741b666547c1e3fe0ba0471e164
│                       │      │                   6a1e1e46b66 
│                       │      ├ Title           : systemd: systemd-journald: Unintended output to user
│                       │      │                   terminals via logger command 
│                       │      ├ Description     : In systemd 259, systemd-journald can send ANSI escape
│                       │      │                   sequences to the terminals of arbitrary users when a "logger
│                       │      │                    -p emerg" command is executed, if ForwardToWall=yes is
│                       │      │                   set. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-669 
│                       │      ├ VendorSeverity   ╭ nvd   : 1 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 3.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 2.9 
│                       │      ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/05/1 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-40228 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-40228 
│                       │      │                  ├ [3]: https://www.cve.org/CVERecord?id=CVE-2026-40228 
│                       │      │                  ╰ [4]: https://www.openwall.com/lists/oss-security/2026/04/08/1 
│                       │      ├ PublishedDate   : 2026-04-10T16:16:33.753Z 
│                       │      ╰ LastModifiedDate: 2026-05-05T02:16:04.82Z 
│                       ├ [28] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libudev1@257.9-0ubuntu2.5 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@257.9-0ubuntu2.5?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : f211373f8a95c023 
│                       │      ├ InstalledVersion: 257.9-0ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ed45628fe85a992de0219b251c39a87fcc03937a2aaaba84edc9d
│                       │      │                   6e0d78302d5 
│                       │      ├ Title           : systemd: systemd-journald: Unintended output to user
│                       │      │                   terminals via logger command 
│                       │      ├ Description     : In systemd 259, systemd-journald can send ANSI escape
│                       │      │                   sequences to the terminals of arbitrary users when a "logger
│                       │      │                    -p emerg" command is executed, if ForwardToWall=yes is
│                       │      │                   set. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-669 
│                       │      ├ VendorSeverity   ╭ nvd   : 1 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 3.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 2.9 
│                       │      ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2026/05/05/1 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-40228 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-40228 
│                       │      │                  ├ [3]: https://www.cve.org/CVERecord?id=CVE-2026-40228 
│                       │      │                  ╰ [4]: https://www.openwall.com/lists/oss-security/2026/04/08/1 
│                       │      ├ PublishedDate   : 2026-04-10T16:16:33.753Z 
│                       │      ╰ LastModifiedDate: 2026-05-05T02:16:04.82Z 
│                       ├ [29] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23db7c315eddf1f4 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:40f4f094ef61b2357bdc64299d1ca1b5f8752f31375f23e53ba75
│                       │      │                   49642f6673b 
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
│                       ├ [30] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23db7c315eddf1f4 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b08244ad0c597ac7febfcf0bfc04b6ca16c5370f399cff33b49ae
│                       │      │                   b56110fa775 
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
│                       │      │                  ├ photon: 2 
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
│                       ├ [31] ╭ VulnerabilityID : CVE-2026-6732 
│                       │      ├ PkgID           : libxml2-16@2.14.5+dfsg-0.2ubuntu0.1 
│                       │      ├ PkgName         : libxml2-16 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libxml2-16@2.14.5%2Bdfsg-0.2ubuntu0.1?
│                       │      │                  │       arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 31495ca6a00051cd 
│                       │      ├ InstalledVersion: 2.14.5+dfsg-0.2ubuntu0.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6732 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3e7276345db10161d32e8221ae341f984b56e747bde382419266a
│                       │      │                   ea7ffb76845 
│                       │      ├ Title           : libxml2: libxml2: Denial of Service via crafted
│                       │      │                   XSD-validated document 
│                       │      ├ Description     : A flaw was found in libxml2. This vulnerability occurs when
│                       │      │                   the library processes a specially crafted XML Schema
│                       │      │                   Definition (XSD) validated document that includes an
│                       │      │                   internal entity reference. An attacker could exploit this by
│                       │      │                    providing a malicious document, leading to a type confusion
│                       │      │                    error that causes the application to crash. This results in
│                       │      │                    a denial of service (DoS), making the affected system or
│                       │      │                   application unavailable. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-843 
│                       │      ├ VendorSeverity   ╭ nvd   : 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:A/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:11503 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-6732 
│                       │      │                  ├ [2]: https://bugzilla.redhat.com/show_bug.cgi?id=2461300 
│                       │      │                  ├ [3]: https://gitlab.gnome.org/GNOME/libxml2/-/issues/1097 
│                       │      │                  ├ [4]: https://gitlab.gnome.org/GNOME/libxml2/-/merge_request
│                       │      │                  │      s/411 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-6732 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-6732 
│                       │      ├ PublishedDate   : 2026-04-23T23:16:16.443Z 
│                       │      ╰ LastModifiedDate: 2026-05-15T14:36:35.823Z 
│                       ├ [32] ╭ VulnerabilityID : CVE-2026-1757 
│                       │      ├ PkgID           : libxml2-16@2.14.5+dfsg-0.2ubuntu0.1 
│                       │      ├ PkgName         : libxml2-16 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libxml2-16@2.14.5%2Bdfsg-0.2ubuntu0.1?
│                       │      │                  │       arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 31495ca6a00051cd 
│                       │      ├ InstalledVersion: 2.14.5+dfsg-0.2ubuntu0.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-1757 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:003b4a9e9030ea7f4da299d1726364a064ff1d3d37591cc1f6494
│                       │      │                   36a738fe4ab 
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
│                       ├ [33] ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:efd52c91a0e82babc47e0ea56578a489eac8040e2c3e1c41ae662
│                       │      │                   c7fb4d3b336 
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
│                       ├ [34] ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ebf07f4e551bc80e732462d27906fc220f1654b47ab77a3920c45
│                       │      │                   97898249d68 
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
│                       ├ [35] ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ceed6421891f3817d8515fd8094439ae1d5ae750e3e67c6731ea9
│                       │      │                   1eb4782f3cf 
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
│                       ├ [36] ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2c05cd9b53ef8d3ab7cb2e0941ed7150a1545a2ccd3cca631fc9d
│                       │      │                   15a862a444e 
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
│                       ├ [37] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9cd81a8f4957a400550a999b0d032c4668cc3164d53e997399981
│                       │      │                   bfd46c2f6e3 
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
│                       ├ [38] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f9aa1d72f03a7a510ce336d79747f8abd6d756cff3bb9eb13e937
│                       │      │                   3e8fcb528e2 
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
│                       ├ [39] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:21277f0812dab6c8393229411ba24bec4a0fcc63b44c7737c36d1
│                       │      │                   c3877a28cef 
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
│                       │      │                  ├ photon: 2 
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
│                       ├ [40] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : login.defs@1:4.17.4-2ubuntu2 
│                       │      ├ PkgName         : login.defs 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu2?arch=all&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 685157e74dbd875c 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:48127ddcfa8265b972861e1c9f1be4284eb521510e20955046883
│                       │      │                   5460561224b 
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
│                       ├ [41] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : f2821a9fde7aa805 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0ae527d54dd6c0423a3fcda30ce0d4bd310b071db4573990b9c40
│                       │      │                   390a4365af7 
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
│                       ├ [42] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : f2821a9fde7aa805 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:00b179bd0f989e1cc7800e51d8077844865fece64faf4615439a7
│                       │      │                   72948812054 
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
│                       │      │                  ├ photon: 2 
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
│                       ├ [43] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : passwd@1:4.17.4-2ubuntu2 
│                       │      ├ PkgName         : passwd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu2?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 2d87ef360f209a3f 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:68bafbc24cc4c3dc2cf5fa5a2e1ee078950776feb9441616d1541
│                       │      │                   2728f686ef8 
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
│                       ├ [44] ╭ VulnerabilityID : CVE-2026-35338 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35338 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3a4fd7bb57b952dd49ba9ff5382fb651f6bf4e849949986fdd811
│                       │      │                   10ae3d5918a 
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
│                       ├ [45] ╭ VulnerabilityID : CVE-2026-35339 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35339 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b5d2dc77b84414d93311c87abf002e97dde03755a4580c0fa8994
│                       │      │                   baa6e58202f 
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
│                       ├ [46] ╭ VulnerabilityID : CVE-2026-35340 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35340 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a69738beb72636cfb946a138fa76260674b6360923e3a9cb53662
│                       │      │                   8be26466b7c 
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
│                       ├ [47] ╭ VulnerabilityID : CVE-2026-35341 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5cd8adbbfb81a5033f4f3ab9130e4d875103e1072fc118a516e33
│                       │      │                   d5ccbf8432e 
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
│                       ├ [48] ╭ VulnerabilityID : CVE-2026-35342 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35342 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b7e3313af7cd33915ea94a5b8a59f13dd42b9002fcd279c1fb24c
│                       │      │                   f53f1842f57 
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
│                       ├ [49] ╭ VulnerabilityID : CVE-2026-35343 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35343 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e1d4949d5e96ae4e51320f0221479ef58d238751f168846116d7e
│                       │      │                   90650ddebd0 
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
│                       ├ [50] ╭ VulnerabilityID : CVE-2026-35344 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:799bc553bf5de81d4da184d6a97596bff04af347f11f1d875001a
│                       │      │                   3ad47c30636 
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
│                       ├ [51] ╭ VulnerabilityID : CVE-2026-35345 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1d65ab4b281954739d082fe03ddb4f27728a1dff6b1c35228f209
│                       │      │                   412d0dff1f5 
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
│                       ├ [52] ╭ VulnerabilityID : CVE-2026-35346 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35346 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9ad53fb0a101870415313e68785c4b5743775ab4fc2765c627d26
│                       │      │                   cbc68d817fb 
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
│                       ├ [53] ╭ VulnerabilityID : CVE-2026-35347 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35347 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7ff69f69187e0a8e5b63e8c1508991142ecf660fd511bca64a3c7
│                       │      │                   aac765b8613 
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
│                       ├ [54] ╭ VulnerabilityID : CVE-2026-35348 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f4e2919325d07bc7fd179ef4b6762fffe31c347fa15e022374c2d
│                       │      │                   048d50f9ce3 
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
│                       ├ [55] ╭ VulnerabilityID : CVE-2026-35349 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35349 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:251ab02c4b6021e631ac14e7e28c8bb47c9afd42559baa898c4a5
│                       │      │                   11b00c9278b 
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
│                       ├ [56] ╭ VulnerabilityID : CVE-2026-35350 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:094a4a60d675a15d8f913c16ea98ea5d07e458ef78c6605708157
│                       │      │                   4671dbd9f4a 
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
│                       ├ [57] ╭ VulnerabilityID : CVE-2026-35351 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:361e1e51c0c4da02691ffbefd670e6e79d549714b83c845474884
│                       │      │                   3df40ec53b7 
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
│                       ├ [58] ╭ VulnerabilityID : CVE-2026-35352 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:445420477ad1cb55cece1caac33fc00d6136d8c9dc0b0c9b49047
│                       │      │                   971458e61b3 
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
│                       ├ [59] ╭ VulnerabilityID : CVE-2026-35353 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35353 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6557147b3f22c24e0eab9bff1ae94313f3ea0fbaaf3538f5df6de
│                       │      │                   92f5f15dfe0 
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
│                       ├ [60] ╭ VulnerabilityID : CVE-2026-35354 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:551decc137549c9f5b1f302d7c66c077120c16cf15c3384d27d73
│                       │      │                   1a641214355 
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
│                       ├ [61] ╭ VulnerabilityID : CVE-2026-35355 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35355 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bcda7ebeacf9c5a85adeea78e40e9e273c327a1e7fe7a5c2f84f7
│                       │      │                   e9354890ee3 
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
│                       ├ [62] ╭ VulnerabilityID : CVE-2026-35356 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35356 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8829b8e12ff91620dd96e1d6c4543000a84687c4c0fc2a51e3fb7
│                       │      │                   330cd7cea92 
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
│                       ├ [63] ╭ VulnerabilityID : CVE-2026-35357 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d14bafddd98626023173ae3a5a023712eb0562174522b7ba2d248
│                       │      │                   289991d5f9e 
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
│                       ├ [64] ╭ VulnerabilityID : CVE-2026-35358 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35358 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:47fd6cfe39342019acc9805b1a98a71567c86748116ad6b3488f8
│                       │      │                   5b8cf1c6dd5 
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
│                       ├ [65] ╭ VulnerabilityID : CVE-2026-35359 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:272aacbeb2ad9eb1d94d71a0fb29a58c3897b05a3f2d8e6d7078a
│                       │      │                   8a8ae432bf0 
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
│                       ├ [66] ╭ VulnerabilityID : CVE-2026-35360 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d855d5b7e9c2c2ca714b77b907941f91075393d3eece9fd03053e
│                       │      │                   24d64e615a4 
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
│                       ├ [67] ╭ VulnerabilityID : CVE-2026-35361 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35361 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5f58c9cc572e32849820a6b75ccb54d237e712aa6e1bcc2825a24
│                       │      │                   24075d1cea9 
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
│                       ├ [68] ╭ VulnerabilityID : CVE-2026-35362 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35362 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2046834d104ddf9fd1b665ff67290719133553c4f65241896ff85
│                       │      │                   a4092430654 
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
│                       ├ [69] ╭ VulnerabilityID : CVE-2026-35363 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1339906f58f1018d03ebde34c1260f9ebae43fc788fb5d95da554
│                       │      │                   cb2755d2067 
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
│                       ├ [70] ╭ VulnerabilityID : CVE-2026-35364 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ae40fa1d17d4decc4f4cd2d2a6d0a853b68ed20689a5e3f8439b0
│                       │      │                   4e1082e6480 
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
│                       ├ [71] ╭ VulnerabilityID : CVE-2026-35365 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35365 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a4a71c68ad3470e91f3ce2a8a4c2b0b422d4827ebdc7f051100e1
│                       │      │                   cedfdcf3e6c 
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
│                       ├ [72] ╭ VulnerabilityID : CVE-2026-35366 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35366 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:235bb52fd674b51788c10c7429b699e8d3cec91ed96348be7b162
│                       │      │                   e3d73230aaa 
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
│                       ├ [73] ╭ VulnerabilityID : CVE-2026-35367 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:26a8d1694bc17041b9b0c8abdfd3fe7c95ff44dea2548ad66491e
│                       │      │                   10b7afb043b 
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
│                       ├ [74] ╭ VulnerabilityID : CVE-2026-35368 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:25fcdb82d84bc26355e4c8e964e482263cb3393d80eeeb3b7bfa9
│                       │      │                   e74ad67dfc1 
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
│                       ├ [75] ╭ VulnerabilityID : CVE-2026-35369 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35369 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bd40a6e1f25902333f61a5ec4812e894d412c36776cbda93f3a49
│                       │      │                   533dd23e6f5 
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
│                       ├ [76] ╭ VulnerabilityID : CVE-2026-35370 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b8bd45b36ec8e96d408967c17d9d278e33dd3294c616ce65a7727
│                       │      │                   10f9997ceab 
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
│                       ├ [77] ╭ VulnerabilityID : CVE-2026-35371 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fa7e2dee0c517cbd4bce4e7a9b8897ad0d707ee2cfab215093f66
│                       │      │                   743bcb332ee 
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
│                       ├ [78] ╭ VulnerabilityID : CVE-2026-35372 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35372 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:67f3fa9fd97526f7bc024880143a676f9100489c1cf1149e1824b
│                       │      │                   3bd6ea9f066 
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
│                       ├ [79] ╭ VulnerabilityID : CVE-2026-35373 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:866b33c1aed9c86ed0f8fe2cbeb603bf344e271b6383297d90c57
│                       │      │                   1a9597bd7f0 
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
│                       ├ [80] ╭ VulnerabilityID : CVE-2026-35374 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:03243cc4278a4250bf8dabafdf0eb5b2c0c3e243cf16d785aca5a
│                       │      │                   0f42380e7ed 
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
│                       ├ [81] ╭ VulnerabilityID : CVE-2026-35375 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35375 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e1d471303bea8535afaf561b493600b53f27d77b3ffb25fcd202d
│                       │      │                   a90dac6474c 
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
│                       ├ [82] ╭ VulnerabilityID : CVE-2026-35376 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35376 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1c1b6d574fbccbb89cd8b53152ad98632c858d28dba659425380c
│                       │      │                   8273a3a1f97 
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
│                       ├ [83] ╭ VulnerabilityID : CVE-2026-35377 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9456d71833979cfc2916247d2805d757c6b413268018a1dc58a76
│                       │      │                   d80515e1fe1 
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
│                       ├ [84] ╭ VulnerabilityID : CVE-2026-35378 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35378 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c5f85e670d71352434b63c165da9b26f0627879ea09e65ae6ebb5
│                       │      │                   66a38bb7f89 
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
│                       ├ [85] ╭ VulnerabilityID : CVE-2026-35379 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35379 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ce0663a108a9aa40d743d67bfa5f1221a1878a4f8c6271805b86f
│                       │      │                   eb1b5413d25 
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
│                       ├ [86] ╭ VulnerabilityID : CVE-2026-35380 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35380 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:47e0944a9082e579e39d8c37229f50700de42402319200f18ae55
│                       │      │                   3f8159be997 
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
│                       ├ [87] ╭ VulnerabilityID : CVE-2026-35381 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35381 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7a9e0e77d45895eee7545340ca5862d4d6685ef70540b25bdda32
│                       │      │                   c3b5d6ae78f 
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
│                       ├ [88] ╭ VulnerabilityID : CVE-2025-45582 
│                       │      ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │      ├ PkgName         : tar 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : 41081f85f98b9d6a 
│                       │      ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-45582 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3f589b0856606616db7fc8ab7983a9a734afd851a3424a8de5bef
│                       │      │                   13fc4c44b50 
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
│                       ├ [89] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:24a3c261d7140e361fb3b879d2de31bf26d3a79f76db7c3ed161b
│                       │      │                   f308ba85447 
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
│                       ├ [90] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                       │      │                  │         aaa48bc3384712fcfad1 
│                       │      │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                       │      │                            b3d9f0e27bac7a7bd357 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:36852d7a53fa771a5a1c2c224537e6b68b45e3cb9b1c52ca17aa0
│                       │      │                   08897432721 
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
│                       │      │                  ├ photon: 2 
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
│                       ╰ [91] ╭ VulnerabilityID : CVE-2021-31879 
│                              ├ PkgID           : wget@1.25.0-2ubuntu3 
│                              ├ PkgName         : wget 
│                              ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu3?arch=amd64&distro
│                              │                  │       =ubuntu-25.10 
│                              │                  ╰ UID : 3ae34724b04a04d7 
│                              ├ InstalledVersion: 1.25.0-2ubuntu3 
│                              ├ Status          : affected 
│                              ├ Layer            ╭ Digest: sha256:229d52ccbca3b10e8d42e9be25116611892ec3ad286d
│                              │                  │         aaa48bc3384712fcfad1 
│                              │                  ╰ DiffID: sha256:abd32a897edf16eb45f57555e69ee2bc921a6030f786
│                              │                            b3d9f0e27bac7a7bd357 
│                              ├ SeveritySource  : ubuntu 
│                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                              ├ DataSource       ╭ ID  : ubuntu 
│                              │                  ├ Name: Ubuntu CVE Tracker 
│                              │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                              ├ Fingerprint     : sha256:10cf43b5d216a1b431f1cc5dd9498ea204c1f110a785326e3ebbf
│                              │                   fa8ad38a207 
│                              ├ Title           : wget: authorization header disclosure on redirect 
│                              ├ Description     : GNU Wget through 1.21.1 does not omit the Authorization
│                              │                   header upon a redirect to a different origin, a related
│                              │                   issue to CVE-2018-1000007. 
│                              ├ Severity        : MEDIUM 
│                              ├ CweIDs           ─ [0]: CWE-601 
│                              ├ VendorSeverity   ╭ amazon     : 2 
│                              │                  ├ cbl-mariner: 2 
│                              │                  ├ nvd        : 2 
│                              │                  ├ photon     : 2 
│                              │                  ├ redhat     : 2 
│                              │                  ╰ ubuntu     : 2 
│                              ├ CVSS             ╭ nvd    ╭ V2Vector: AV:N/AC:M/Au:N/C:P/I:P/A:N 
│                              │                  │        ├ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L
│                              │                  │        │           /A:N 
│                              │                  │        ├ V2Score : 5.8 
│                              │                  │        ╰ V3Score : 6.1 
│                              │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:N
│                              │                           │           /A:N 
│                              │                           ╰ V3Score : 6.5 
│                              ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2021-31879 
│                              │                  ├ [1]: https://mail.gnu.org/archive/html/bug-wget/2021-02/msg
│                              │                  │      00002.html 
│                              │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2021-31879 
│                              │                  ├ [3]: https://savannah.gnu.org/bugs/?56909 
│                              │                  ├ [4]: https://security.netapp.com/advisory/ntap-20210618-0002/ 
│                              │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2021-31879 
│                              ├ PublishedDate   : 2021-04-29T05:15:08.707Z 
│                              ╰ LastModifiedDate: 2024-11-21T06:06:25.02Z 
╰ [1] ╭ Target  : Java 
      ├ Class   : lang-pkgs 
      ├ Type    : jar 
      ╰ Packages 
```
