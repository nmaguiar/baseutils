```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:deb (ubuntu 26.04) 
│     ├ Class          : os-pkgs 
│     ├ Type           : ubuntu 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : bsdextrautils@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : bsdextrautils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41.3-3ubuntu2?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 3e7202472804e710 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b0c6ce1c3fc12fad8f32e0db0d1d9f66babc951da9305f2da79f0
│                       │      │                   671dd3e23b9 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [1]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : bsdextrautils@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : bsdextrautils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41.3-3ubuntu2?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 3e7202472804e710 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9f863991bb393db5b3200ed60744811f5fff6437ecf9e149eb357
│                       │      │                   a7dd49d5962 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [2]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : bsdutils@1:2.41.3-3ubuntu2 
│                       │      ├ PkgName         : bsdutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41.3-3ubuntu2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : d513a572db034d99 
│                       │      ├ InstalledVersion: 1:2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:644132a179ae64a7b93eb6e5141aabb053955b801b9ed561953b6
│                       │      │                   8788714c184 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [3]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : bsdutils@1:2.41.3-3ubuntu2 
│                       │      ├ PkgName         : bsdutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41.3-3ubuntu2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : d513a572db034d99 
│                       │      ├ InstalledVersion: 1:2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6d9391bda02e46ace11c282f5abea8babe2cf584f8befd8cb6776
│                       │      │                   c01849c67fc 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [4]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libblkid1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libblkid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41.3-3ubuntu2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : cfada1ce2d53117c 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f07aa3eb2f87d70958a7b5f7c951bc1d319d3d191b11e3a224eb5
│                       │      │                   e0f293392a4 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [5]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libblkid1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libblkid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41.3-3ubuntu2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : cfada1ce2d53117c 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2f05edb2c830b9381cbacc7c8541fd80aeb4310150500c08b7df9
│                       │      │                   db07f479f74 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [6]  ╭ VulnerabilityID : CVE-2025-66382 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:500040264c5f29cd43262fd9f5c2710dbcc1f17c2a6c94b7a77c2
│                       │      │                   1f023ea8b06 
│                       │      ├ Title           : libexpat: libexpat: Denial of service via crafted file
│                       │      │                   processing 
│                       │      ├ Description     : In libexpat through 2.7.3, a crafted file with an
│                       │      │                   approximate size of 2 MiB can lead to dozens of seconds of
│                       │      │                   processing time. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-407 
│                       │      ├ VendorSeverity   ╭ azure : 1 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:N
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
│                       │      ╰ LastModifiedDate: 2026-06-17T09:56:45.24Z 
│                       ├ [7]  ╭ VulnerabilityID : CVE-2024-2236 
│                       │      ├ PkgID           : libgcrypt20@1.12.0-2ubuntu1 
│                       │      ├ PkgName         : libgcrypt20 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libgcrypt20@1.12.0-2ubuntu1?arch=amd64
│                       │      │                  │       &distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 45e5e1ad6adb0acd 
│                       │      ├ InstalledVersion: 1.12.0-2ubuntu1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-2236 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d03edf4cbd843a2efb0b7bf8ec391240fc23d3f80afe54910e8ba
│                       │      │                   390bf884921 
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
│                       │      │                  ├ [7] : https://creativecommons.org/licenses/by/4.0/ 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       24-2236 
│                       │      │                  ├ [9] : https://dev.gnupg.org/T7136 
│                       │      │                  ├ [10]: https://errata.almalinux.org/9/ALSA-2024-9404.html 
│                       │      │                  ├ [11]: https://errata.rockylinux.org/RLSA-2024:9404 
│                       │      │                  ├ [12]: https://github.com/tomato42/marvin-toolkit/tree/maste
│                       │      │                  │       r/example/libgcrypt 
│                       │      │                  ├ [13]: https://gitlab.com/redhat-crypto/libgcrypt/libgcrypt-
│                       │      │                  │       mirror/-/merge_requests/17 
│                       │      │                  ├ [14]: https://linux.oracle.com/cve/CVE-2024-2236.html 
│                       │      │                  ├ [15]: https://linux.oracle.com/errata/ELSA-2024-9404.html 
│                       │      │                  ├ [16]: https://lists.gnupg.org/pipermail/gcrypt-devel/2024-M
│                       │      │                  │       arch/005607.html 
│                       │      │                  ├ [17]: https://nvd.nist.gov/vuln/detail/CVE-2024-2236 
│                       │      │                  ╰ [18]: https://www.cve.org/CVERecord?id=CVE-2024-2236 
│                       │      ├ PublishedDate   : 2024-03-06T22:15:57.977Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T07:24:06.083Z 
│                       ├ [8]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libmount1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41.3-3ubuntu2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : ec572950b070797 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:da25924ee97d0b697bd9dfa8b5c255515adda6f8c3dfbe3a52933
│                       │      │                   2fbde1d8bab 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [9]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libmount1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41.3-3ubuntu2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : ec572950b070797 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1474c256ad158711576f677265e5436d98e4fe197b895e441c1c6
│                       │      │                   52aefaa7243 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [10] ╭ VulnerabilityID : CVE-2026-13757 
│                       │      ├ PkgID           : libp11-kit0@0.26.2-2 
│                       │      ├ PkgName         : libp11-kit0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libp11-kit0@0.26.2-2?arch=amd64&distro
│                       │      │                  │       =ubuntu-26.04 
│                       │      │                  ╰ UID : 38d0559292d79a63 
│                       │      ├ InstalledVersion: 0.26.2-2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-13757 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:674ba2243e39cbb0f4e4b7253bdbd1102518efc998e6b5d1b7da6
│                       │      │                   c4f528ca28e 
│                       │      ├ Title           : p11-kit: Stack exhaustion via unbounded recursion in RPC
│                       │      │                   attribute parsing 
│                       │      ├ Description     : A flaw was found in p11-kit. The RPC message attribute
│                       │      │                   parsing functions p11_rpc_message_get_attribute() and
│                       │      │                   p11_rpc_message_get_attribute_array_value() form a
│                       │      │                   mutually-recursive call chain with no recursion depth limit
│                       │      │                   when processing nested CKA_WRAP_TEMPLATE,
│                       │      │                   CKA_UNWRAP_TEMPLATE, and CKA_DERIVE_TEMPLATE attributes. An
│                       │      │                   unauthenticated attacker with local access to the p11-kit
│                       │      │                   RPC Unix domain socket can send a specially crafted request
│                       │      │                   with deeply nested template attributes, causing stack
│                       │      │                   exhaustion and crashing the p11-kit server process and its
│                       │      │                   dependent services. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-674 
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.2 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:37469 
│                       │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:38342 
│                       │      │                  ├ [2] : https://access.redhat.com/errata/RHSA-2026:49667 
│                       │      │                  ├ [3] : https://access.redhat.com/errata/RHSA-2026:49668 
│                       │      │                  ├ [4] : https://access.redhat.com/errata/RHSA-2026:53371 
│                       │      │                  ├ [5] : https://access.redhat.com/errata/RHSA-2026:54387 
│                       │      │                  ├ [6] : https://access.redhat.com/errata/RHSA-2026:54760 
│                       │      │                  ├ [7] : https://access.redhat.com/security/cve/CVE-2026-13757 
│                       │      │                  ├ [8] : https://bugzilla.redhat.com/2494556 
│                       │      │                  ├ [9] : https://bugzilla.redhat.com/show_bug.cgi?id=2494556 
│                       │      │                  ├ [10]: https://creativecommons.org/licenses/by/4.0/ 
│                       │      │                  ├ [11]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-13757 
│                       │      │                  ├ [12]: https://errata.almalinux.org/9/ALSA-2026-49667.html 
│                       │      │                  ├ [13]: https://errata.rockylinux.org/RLSA-2026:49667 
│                       │      │                  ├ [14]: https://github.com/advisories/GHSA-p2wm-69qx-x25w 
│                       │      │                  ├ [15]: https://linux.oracle.com/cve/CVE-2026-13757.html 
│                       │      │                  ├ [16]: https://linux.oracle.com/errata/ELSA-2026-49668.html 
│                       │      │                  ├ [17]: https://nvd.nist.gov/vuln/detail/CVE-2026-13757 
│                       │      │                  ╰ [18]: https://www.cve.org/CVERecord?id=CVE-2026-13757 
│                       │      ├ PublishedDate   : 2026-06-29T19:16:40.907Z 
│                       │      ╰ LastModifiedDate: 2026-08-13T21:17:40.737Z 
│                       ├ [11] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libsmartcols1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41.3-3ubuntu2?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : eb8f24163bcc7b6b 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2ad3014c4e03e27a90ac5ac5280c1c34fe448e19e777449394fe3
│                       │      │                   4f2e2e9e1fe 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [12] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libsmartcols1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41.3-3ubuntu2?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : eb8f24163bcc7b6b 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9c8732698083bfeecfd5f2036038830092c01acdc49fc67eea83d
│                       │      │                   1de2a93fb1d 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [13] ╭ VulnerabilityID : CVE-2026-15059 
│                       │      ├ PkgID           : libsystemd0@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@259.5-0ubuntu3.3?arch=amd6
│                       │      │                  │       4&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : fcc1e0814fd72e7d 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ FixedVersion    : 259.5-0ubuntu3.4 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-15059 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f546396b9a03bb5df17a4d057fe05b21cac3f32148e5765c1f448
│                       │      │                   c6228cf348f 
│                       │      ├ Title           : Local unprivileged users can terminate arbitrary local
│                       │      │                   processes  ... 
│                       │      ├ Description     : Local unprivileged users can terminate arbitrary local
│                       │      │                   processes via a systemd-oomd IPC API due to a missing path
│                       │      │                   traversal validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-22 
│                       │      │                  ╰ [1]: CWE-59 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/systemd/systemd/security/advisories
│                       │      │                  │      /GHSA-652q-wxr6-h5j6 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8626-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-15059 
│                       │      ├ PublishedDate   : 2026-08-10T14:17:20.76Z 
│                       │      ╰ LastModifiedDate: 2026-08-10T18:17:40.983Z 
│                       ├ [14] ╭ VulnerabilityID : CVE-2026-15060 
│                       │      ├ PkgID           : libsystemd0@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@259.5-0ubuntu3.3?arch=amd6
│                       │      │                  │       4&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : fcc1e0814fd72e7d 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ FixedVersion    : 259.5-0ubuntu3.4 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-15060 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:eff305596d2bebf635d0d53e53cebf7105845eb7953f228470163
│                       │      │                   c713736910b 
│                       │      ├ Title           : When systemd-machined >= v259 (or v258 with a custom
│                       │      │                   `polkit` pol ... 
│                       │      ├ Description     : When systemd-machined >= v259 (or v258 with a custom
│                       │      │                   `polkit` policy that allows `register-machine` access) is
│                       │      │                   running on a desktop system, an unprivileged user logged in
│                       │      │                   a desktop graphical session can kill arbitrary processes,
│                       │      │                   even privileged ones.
│                       │      │                   
│                       │      │                   - versions older than v259 are not affected, unless
│                       │      │                   unprivileged access is granted for the `register-machine`
│                       │      │                   polkit action via a local, custom policy config file
│                       │      │                   - versions older than v258 are not affected
│                       │      │                   - unrelated to the systemd service manager (pid 1 or user
│                       │      │                   session managers)
│                       │      │                   - systemd-machined is not typically installed by default,
│                       │      │                   and is typically in an optional, separate package (e.g.:
│                       │      │                   systemd-container)
│                       │      │                   - terminal-only or remote sessions (e.g.: ssh) are not
│                       │      │                   affected 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-284 
│                       │      │                  ╰ [1]: CWE-862 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/systemd/systemd/security/advisories
│                       │      │                  │      /GHSA-qwv4-3gwc-w5g8 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8626-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-15060 
│                       │      ├ PublishedDate   : 2026-08-10T14:17:21.13Z 
│                       │      ╰ LastModifiedDate: 2026-08-10T18:17:41.087Z 
│                       ├ [15] ╭ VulnerabilityID : CVE-2026-16742 
│                       │      ├ PkgID           : libsystemd0@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@259.5-0ubuntu3.3?arch=amd6
│                       │      │                  │       4&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : fcc1e0814fd72e7d 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ FixedVersion    : 259.5-0ubuntu3.4 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-16742 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8e46ec025805a5a3fcd00c3d6cce4a71625ad7f55a012d3737a86
│                       │      │                   63caa92f6e6 
│                       │      ├ Title           : systemd-homed contains a local privilege escalation bug via
│                       │      │                   arbit ... 
│                       │      ├ Description     : systemd-homed contains a local privilege escalation bug via
│                       │      │                   arbitrary system group addition to a local, logged in,
│                       │      │                   homed-managed user 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-269 
│                       │      │                  ╰ [1]: CWE-347 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/systemd/systemd/security/advisories
│                       │      │                  │      /GHSA-jm29-p7hh-vjhv 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8626-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-16742 
│                       │      ├ PublishedDate   : 2026-08-10T14:17:21.277Z 
│                       │      ╰ LastModifiedDate: 2026-08-10T16:19:29.157Z 
│                       ├ [16] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libsystemd0@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@259.5-0ubuntu3.3?arch=amd6
│                       │      │                  │       4&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : fcc1e0814fd72e7d 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ae6835da2a9071436ceddfc94f62a01b5d1772313b0c32bccadd8
│                       │      │                   2191baefee6 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:44:53.31Z 
│                       ├ [17] ╭ VulnerabilityID : CVE-2026-15059 
│                       │      ├ PkgID           : libudev1@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@259.5-0ubuntu3.3?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : df574d4e09e87346 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ FixedVersion    : 259.5-0ubuntu3.4 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-15059 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3ca7a3d9e5f30f5eef5da3115555a1d9d55bfd27c85e6e60f4b24
│                       │      │                   6a3bff2655d 
│                       │      ├ Title           : Local unprivileged users can terminate arbitrary local
│                       │      │                   processes  ... 
│                       │      ├ Description     : Local unprivileged users can terminate arbitrary local
│                       │      │                   processes via a systemd-oomd IPC API due to a missing path
│                       │      │                   traversal validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-22 
│                       │      │                  ╰ [1]: CWE-59 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/systemd/systemd/security/advisories
│                       │      │                  │      /GHSA-652q-wxr6-h5j6 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8626-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-15059 
│                       │      ├ PublishedDate   : 2026-08-10T14:17:20.76Z 
│                       │      ╰ LastModifiedDate: 2026-08-10T18:17:40.983Z 
│                       ├ [18] ╭ VulnerabilityID : CVE-2026-15060 
│                       │      ├ PkgID           : libudev1@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@259.5-0ubuntu3.3?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : df574d4e09e87346 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ FixedVersion    : 259.5-0ubuntu3.4 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-15060 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0a45dc0957dd53b4deb5f8858ef61374ef4c349898de1830db739
│                       │      │                   c5823a9dbdf 
│                       │      ├ Title           : When systemd-machined >= v259 (or v258 with a custom
│                       │      │                   `polkit` pol ... 
│                       │      ├ Description     : When systemd-machined >= v259 (or v258 with a custom
│                       │      │                   `polkit` policy that allows `register-machine` access) is
│                       │      │                   running on a desktop system, an unprivileged user logged in
│                       │      │                   a desktop graphical session can kill arbitrary processes,
│                       │      │                   even privileged ones.
│                       │      │                   
│                       │      │                   - versions older than v259 are not affected, unless
│                       │      │                   unprivileged access is granted for the `register-machine`
│                       │      │                   polkit action via a local, custom policy config file
│                       │      │                   - versions older than v258 are not affected
│                       │      │                   - unrelated to the systemd service manager (pid 1 or user
│                       │      │                   session managers)
│                       │      │                   - systemd-machined is not typically installed by default,
│                       │      │                   and is typically in an optional, separate package (e.g.:
│                       │      │                   systemd-container)
│                       │      │                   - terminal-only or remote sessions (e.g.: ssh) are not
│                       │      │                   affected 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-284 
│                       │      │                  ╰ [1]: CWE-862 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/systemd/systemd/security/advisories
│                       │      │                  │      /GHSA-qwv4-3gwc-w5g8 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8626-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-15060 
│                       │      ├ PublishedDate   : 2026-08-10T14:17:21.13Z 
│                       │      ╰ LastModifiedDate: 2026-08-10T18:17:41.087Z 
│                       ├ [19] ╭ VulnerabilityID : CVE-2026-16742 
│                       │      ├ PkgID           : libudev1@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@259.5-0ubuntu3.3?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : df574d4e09e87346 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ FixedVersion    : 259.5-0ubuntu3.4 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-16742 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6f0b60df01c1ccd9dc009d9b808035ee5e094fedd0ac366c03230
│                       │      │                   dc2a20cfb65 
│                       │      ├ Title           : systemd-homed contains a local privilege escalation bug via
│                       │      │                   arbit ... 
│                       │      ├ Description     : systemd-homed contains a local privilege escalation bug via
│                       │      │                   arbitrary system group addition to a local, logged in,
│                       │      │                   homed-managed user 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ╭ [0]: CWE-269 
│                       │      │                  ╰ [1]: CWE-347 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/systemd/systemd/security/advisories
│                       │      │                  │      /GHSA-jm29-p7hh-vjhv 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8626-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-16742 
│                       │      ├ PublishedDate   : 2026-08-10T14:17:21.277Z 
│                       │      ╰ LastModifiedDate: 2026-08-10T16:19:29.157Z 
│                       ├ [20] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libudev1@259.5-0ubuntu3.3 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@259.5-0ubuntu3.3?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : df574d4e09e87346 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c473c18d8d9a64d837ea1a2b49a32e3265d2c7ded4259e0acbbe7
│                       │      │                   f8ed7be4c42 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:44:53.31Z 
│                       ├ [21] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libuuid1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41.3-3ubuntu2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 927585f152fe989a 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:55f7787e281fc21dfa2fe61305b9354abd15f71524c29eca43b70
│                       │      │                   023d88ceaf8 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [22] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libuuid1@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41.3-3ubuntu2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 927585f152fe989a 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:143cca8359a0d3a32dacfbab6ef98eca293f9edff42adeda3debe
│                       │      │                   b191bb34830 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [23] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41.3-3ubuntu2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41.3-3ubuntu2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : 591feb53ee99f4f9 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d9ca07d42bc9feef59970d5975854c83a4f3c85726807812926c8
│                       │      │                   aab84dc687b 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [24] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41.3-3ubuntu2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41.3-3ubuntu2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : 591feb53ee99f4f9 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:333d19511b7a648fadd8fe9e4db458936f440cb2c3ff6165aab9d
│                       │      │                   0cb024f3d80 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [25] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : login.defs@1:4.17.4-2ubuntu3 
│                       │      ├ PkgName         : login.defs 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu3?arch=all&di
│                       │      │                  │       stro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : eaf648d5e4e975f7 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:74f020a856d9c5fc93f48ce9ae4d36d34184588a951732d783333
│                       │      │                   7492a4ed35b 
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
│                       │      │                  ├ [4] : https://creativecommons.org/licenses/by/4.0/ 
│                       │      │                  ├ [5] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       24-56433 
│                       │      │                  ├ [6] : https://errata.almalinux.org/9/ALSA-2025-20559.html 
│                       │      │                  ├ [7] : https://errata.rockylinux.org/RLSA-2025:20559 
│                       │      │                  ├ [8] : https://github.com/shadow-maint/shadow/blob/e2512d574
│                       │      │                  │       1d4a44bdd81a8c2d0029b6222728cf0/etc/login.defs#L238-L
│                       │      │                  │       241 
│                       │      │                  ├ [9] : https://github.com/shadow-maint/shadow/issues/1157 
│                       │      │                  ├ [10]: https://github.com/shadow-maint/shadow/releases/tag/4.4 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2024-56433.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2025-20559-0.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2024-56433 
│                       │      │                  ╰ [14]: https://www.cve.org/CVERecord?id=CVE-2024-56433 
│                       │      ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [26] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : mount@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41.3-3ubuntu2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-26.04 
│                       │      │                  ╰ UID : 98c6a5d7e9e110eb 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9f235338409c55bdf8b08f3193596d38e64d4ac2bb5c3512c496f
│                       │      │                   13feffbf26a 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [27] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : mount@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41.3-3ubuntu2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-26.04 
│                       │      │                  ╰ UID : 98c6a5d7e9e110eb 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:621edb9bf5d9e34aaaf130855307c0df42677bfe5611afb78e112
│                       │      │                   d35d6cb908c 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [28] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : passwd@1:4.17.4-2ubuntu3 
│                       │      ├ PkgName         : passwd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu3?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : 6f8f43a2d44eb6a2 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0e565f21ea2279efe69c74be62935ee3ee037cafe1c4b8cc31f5c
│                       │      │                   b9d779d4ebf 
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
│                       │      │                  ├ [4] : https://creativecommons.org/licenses/by/4.0/ 
│                       │      │                  ├ [5] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       24-56433 
│                       │      │                  ├ [6] : https://errata.almalinux.org/9/ALSA-2025-20559.html 
│                       │      │                  ├ [7] : https://errata.rockylinux.org/RLSA-2025:20559 
│                       │      │                  ├ [8] : https://github.com/shadow-maint/shadow/blob/e2512d574
│                       │      │                  │       1d4a44bdd81a8c2d0029b6222728cf0/etc/login.defs#L238-L
│                       │      │                  │       241 
│                       │      │                  ├ [9] : https://github.com/shadow-maint/shadow/issues/1157 
│                       │      │                  ├ [10]: https://github.com/shadow-maint/shadow/releases/tag/4.4 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2024-56433.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2025-20559-0.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2024-56433 
│                       │      │                  ╰ [14]: https://www.cve.org/CVERecord?id=CVE-2024-56433 
│                       │      ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [29] ╭ VulnerabilityID : CVE-2026-35341 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:591ef7aa83f22340491efbaa06b28789555825884b29fa2894486
│                       │      │                   aa2b2ea5cd3 
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
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/pull/10376 
│                       │      │                  ├ [3]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-pmf6-rcx4-v53v 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-35341 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-35341 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.06Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.5Z 
│                       ├ [30] ╭ VulnerabilityID : CVE-2026-35344 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:22429f9e5613209e7170158627e296e438dc5819c4b1aa5c4b84a
│                       │      │                   2b977744911 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.833Z 
│                       ├ [31] ╭ VulnerabilityID : CVE-2026-35345 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:058d3126e3d16c39e9a4c1d6023f27918d17e5c556f38d62721ea
│                       │      │                   ce036dae6a1 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.943Z 
│                       ├ [32] ╭ VulnerabilityID : CVE-2026-35348 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:291a5e5eb68590ea0b048c4af2508f14bf1671fb684648397c644
│                       │      │                   e1b371da80d 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.27Z 
│                       ├ [33] ╭ VulnerabilityID : CVE-2026-35350 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:175bf5fe055976f1cfdb07b998a0474f89c96b1f21dea5f6533b7
│                       │      │                   8e3863cb8a5 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.48Z 
│                       ├ [34] ╭ VulnerabilityID : CVE-2026-35351 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2966fe752f032ba8f047262902d87cc8cdf140d79712af85a4f85
│                       │      │                   4f405d410ab 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.587Z 
│                       ├ [35] ╭ VulnerabilityID : CVE-2026-35352 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fe883e3dad8900d41b7242aa16d915e59702cc921d0d32df2ce17
│                       │      │                   53df2f4e0f8 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.69Z 
│                       ├ [36] ╭ VulnerabilityID : CVE-2026-35354 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6bdb8331803d10386f438d848bae4d590c732254cbcee0a5ebb5a
│                       │      │                   3cc4f98d231 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.907Z 
│                       ├ [37] ╭ VulnerabilityID : CVE-2026-35357 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:910811dc35b68ea93df529d60c41239d50ac02cb34dec1f58c0a5
│                       │      │                   0c42eeab3cd 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.223Z 
│                       ├ [38] ╭ VulnerabilityID : CVE-2026-35359 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:99b477cf982a20c27a15eaadda06727269668ec713f9b2f9df82e
│                       │      │                   2fdcbef4ef5 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.437Z 
│                       ├ [39] ╭ VulnerabilityID : CVE-2026-35360 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:033610490c8d7a02c77b89e95ed86d8558906fe2e0e7c7831a0ba
│                       │      │                   a5c87936900 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.543Z 
│                       ├ [40] ╭ VulnerabilityID : CVE-2026-35363 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:271bc735165c338511ac2822b576e7117c9eb4a4d60639e55e95a
│                       │      │                   ab221999a60 
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
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-89p7-7cq3-hhr2 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35363 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35363 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.12Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.867Z 
│                       ├ [41] ╭ VulnerabilityID : CVE-2026-35364 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:05f189cfc2681177760d1ab2234f6a2e3d44b993b256aee829598
│                       │      │                   59c47d64f17 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.97Z 
│                       ├ [42] ╭ VulnerabilityID : CVE-2026-35367 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:256d275e8664c30b9964f4b1be4c2958d65dc1a22c5db2b6e00da
│                       │      │                   e81bd47c2de 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.297Z 
│                       ├ [43] ╭ VulnerabilityID : CVE-2026-35368 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:66124f95569671d0cbfce6ecfc3ff763f1ebac1bc6e2af205b111
│                       │      │                   88d80f9f7bb 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.4Z 
│                       ├ [44] ╭ VulnerabilityID : CVE-2026-35370 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:17949b2c84a1d3ec9e3126257f08b40c29f4f38b79636416725ea
│                       │      │                   646186c6fd1 
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
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-47c7-qrm7-mqw7 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35370 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35370 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.833Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.613Z 
│                       ├ [45] ╭ VulnerabilityID : CVE-2026-35371 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:be631f5e18bd18300990614bdf47a25a88e3facfc2f170282580b
│                       │      │                   4c9ea8d9be7 
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
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-xv5w-cw7x-72gj 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35371 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35371 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.987Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.723Z 
│                       ├ [46] ╭ VulnerabilityID : CVE-2026-35373 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:707848adff028da54903059cd1f36093d8030af3a97a6ab6a791c
│                       │      │                   b8581e5deda 
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
│                       │      │                  ├ [2]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-jcjr-rh8q-7xqf 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-35373 
│                       │      │                  ╰ [4]: https://www.cve.org/CVERecord?id=CVE-2026-35373 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:41.997Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.933Z 
│                       ├ [47] ╭ VulnerabilityID : CVE-2026-35374 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0f2d6e24da8c4be626541463c36903bd4583f5f41273465b61883
│                       │      │                   bfcb90bbf62 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.04Z 
│                       ├ [48] ╭ VulnerabilityID : CVE-2026-35377 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 15e3b6ce4401d8b0 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:12ae0197da07dbdede1e6ef0f9ba01339c9c1b54a1f6c85fc9b57
│                       │      │                   df7228a38e6 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.357Z 
│                       ├ [49] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : util-linux@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41.3-3ubuntu2?arch=amd64&
│                       │      │                  │       distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 34e9503915630576 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b0d14c45c081e3ca5258786095a129b732aa26d290a86bcb889b2
│                       │      │                   f067efbb82c 
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
│                       │      ├ VendorSeverity   ╭ azure       : 2 
│                       │      │                  ├ bottlerocket: 2 
│                       │      │                  ├ julia       : 2 
│                       │      │                  ├ redhat      : 2 
│                       │      │                  ╰ ubuntu      : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.7 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026
│                       │      │                  │      -27456 
│                       │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-27456 
│                       │      │                  ├ [2]: https://github.com/bottlerocket-os/bottlerocket-core-k
│                       │      │                  │      it/blob/develop/advisories/14.5.0/BRSA-jgcxwcxt3sxd.to
│                       │      │                  │      ml 
│                       │      │                  ├ [3]: https://github.com/util-linux/util-linux/commit/5e3904
│                       │      │                  │      67b26a3cf3fecc04e1a0d482dff3162fc4 
│                       │      │                  ├ [4]: https://github.com/util-linux/util-linux/releases/tag/
│                       │      │                  │      v2.41.4 
│                       │      │                  ├ [5]: https://github.com/util-linux/util-linux/security/advi
│                       │      │                  │      sories/GHSA-qq4x-vfq4-9h9g 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-27456 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-27456 
│                       │      ├ PublishedDate   : 2026-04-03T22:16:25.4Z 
│                       │      ╰ LastModifiedDate: 2026-07-24T22:10:00.14Z 
│                       ├ [50] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : util-linux@2.41.3-3ubuntu2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41.3-3ubuntu2?arch=amd64&
│                       │      │                  │       distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 34e9503915630576 
│                       │      ├ InstalledVersion: 2.41.3-3ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9b78f77f8f520bd9c034780e1656e68dedf66c8a75e1a56dab284
│                       │      │                   1b526bf651b 
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
│                       │      ╰ LastModifiedDate: 2026-07-21T19:10:00.107Z 
│                       ├ [51] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : vim@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.2141-1ubuntu4.7?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 81174070196e01a7 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1e5c76979d0aea17b670e1c5464e03530bc2aa717776363a7f2a7
│                       │      │                   5f37e23be78 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-401 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51400 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-51400 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-51400 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T18:17:11.477Z 
│                       ├ [52] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : vim@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.2141-1ubuntu4.7?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 81174070196e01a7 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bbe80f7bbca920eed491f38f4c6d46ac2d991b1cd7e8c7c7f3fa3
│                       │      │                   a19a9bafdd2 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-94 
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51401 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://github.com/vim/vim 
│                       │      │                  ├ [3]: https://github.com/vim/vim/blob/master/src/os_vms.c 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-51401 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-51401 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T20:17:09.31Z 
│                       ├ [53] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : vim-common@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.2141-1ubuntu4.7?arch=al
│                       │      │                  │       l&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : e4335c61f6d20a99 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ad50ab87671ca29efe858c9e49ccdcdfbf54b878241c314598dca
│                       │      │                   ab386b1831d 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-401 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51400 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-51400 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-51400 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T18:17:11.477Z 
│                       ├ [54] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : vim-common@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.2141-1ubuntu4.7?arch=al
│                       │      │                  │       l&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : e4335c61f6d20a99 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9b8cee699391587fbecd24fb0e905ffd3f15e24caa062648d8297
│                       │      │                   c6d530e3010 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-94 
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51401 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://github.com/vim/vim 
│                       │      │                  ├ [3]: https://github.com/vim/vim/blob/master/src/os_vms.c 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-51401 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-51401 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T20:17:09.31Z 
│                       ├ [55] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : vim-runtime@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : vim-runtime 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.2141-1ubuntu4.7?arch=a
│                       │      │                  │       ll&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : b876d7ab71a834bc 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6763824bdf0307b6b14a9ed792e5439c4057b3ab6916de85b5c67
│                       │      │                   928b68c242d 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-401 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51400 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-51400 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-51400 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T18:17:11.477Z 
│                       ├ [56] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : vim-runtime@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : vim-runtime 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.2141-1ubuntu4.7?arch=a
│                       │      │                  │       ll&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : b876d7ab71a834bc 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:86854707e16004ea77f0c6b7f2fad1c0ffc0b897f683d703ddbe3
│                       │      │                   8048af2cd62 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-94 
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51401 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://github.com/vim/vim 
│                       │      │                  ├ [3]: https://github.com/vim/vim/blob/master/src/os_vms.c 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-51401 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-51401 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T20:17:09.31Z 
│                       ├ [57] ╭ VulnerabilityID : CVE-2021-31879 
│                       │      ├ PkgID           : wget@1.25.0-2ubuntu4.3 
│                       │      ├ PkgName         : wget 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu4.3?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : a7a564ca8877281a 
│                       │      ├ InstalledVersion: 1.25.0-2ubuntu4.3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bd377b62721ed9af997c8dfb6f290f8d0cd6eacdc12cddfe498f5
│                       │      │                   3a4bd3f8b2c 
│                       │      ├ Title           : wget: authorization header disclosure on redirect 
│                       │      ├ Description     : GNU Wget through 1.21.1 does not omit the Authorization
│                       │      │                   header upon a redirect to a different origin, a related
│                       │      │                   issue to CVE-2018-1000007. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-601 
│                       │      ├ VendorSeverity   ╭ amazon     : 2 
│                       │      │                  ├ cbl-mariner: 2 
│                       │      │                  ├ julia      : 2 
│                       │      │                  ├ nvd        : 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 6.1 
│                       │      │                  ├ nvd    ╭ V2Vector: AV:N/AC:M/Au:N/C:P/I:P/A:N 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T03:52:23.987Z 
│                       ├ [58] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : xxd@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.2141-1ubuntu4.7?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 2c613ff4ce2c8406 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ef510a2d8f70dcad2834c0e17b39982fe14d7855f2508cc97063c
│                       │      │                   b213819c930 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-401 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51400 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-51400 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-51400 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T18:17:11.477Z 
│                       ├ [59] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : xxd@2:9.1.2141-1ubuntu4.7 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.2141-1ubuntu4.7?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 2c613ff4ce2c8406 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.7 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                       │      │                  │         4724a45c03fe2abddba1 
│                       │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                       │      │                            28c664cc70b025656e08 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:326fd24ef59bdf11ab7786cde3be50b33c9e09aeb77676b74ca8c
│                       │      │                   3d42a5a87b3 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-94 
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-51401 
│                       │      │                  ├ [1]: https://gist.github.com/jiejiaodedengdai/ff5d34a523167
│                       │      │                  │      e09b7d8330cc9f5d4e5#file-vim-os_vms-cves-md 
│                       │      │                  ├ [2]: https://github.com/vim/vim 
│                       │      │                  ├ [3]: https://github.com/vim/vim/blob/master/src/os_vms.c 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-51401 
│                       │      │                  ╰ [5]: https://www.cve.org/CVERecord?id=CVE-2026-51401 
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-08-05T20:17:09.31Z 
│                       ╰ [60] ╭ VulnerabilityID : CVE-2026-27171 
│                              ├ PkgID           : zlib1g@1:1.3.dfsg+really1.3.1-1ubuntu3 
│                              ├ PkgName         : zlib1g 
│                              ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/zlib1g@1.3.dfsg%2Breally1.3.1-1ubuntu3
│                              │                  │       ?arch=amd64&distro=ubuntu-26.04&epoch=1 
│                              │                  ╰ UID : e6f2cecd2b667912 
│                              ├ InstalledVersion: 1:1.3.dfsg+really1.3.1-1ubuntu3 
│                              ├ Status          : affected 
│                              ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
│                              │                  │         4724a45c03fe2abddba1 
│                              │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
│                              │                            28c664cc70b025656e08 
│                              ├ SeveritySource  : ubuntu 
│                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27171 
│                              ├ DataSource       ╭ ID  : ubuntu 
│                              │                  ├ Name: Ubuntu CVE Tracker 
│                              │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                              ├ Fingerprint     : sha256:d733f3db7e93c6b9fe5942ffb04a42b6202c092752639067d7ffc
│                              │                   37109a0ef05 
│                              ├ Title           : zlib: zlib: Denial of Service via infinite loop in CRC32
│                              │                   combine functions 
│                              ├ Description     : zlib before 1.3.2 allows CPU consumption via crc32_combine64
│                              │                    and crc32_combine_gen64 because x2nmodp can do right shifts
│                              │                    within a loop that has no termination condition. 
│                              ├ Severity        : LOW 
│                              ├ CweIDs           ─ [0]: CWE-1284 
│                              ├ VendorSeverity   ╭ amazon     : 1 
│                              │                  ├ azure      : 1 
│                              │                  ├ cbl-mariner: 1 
│                              │                  ├ julia      : 2 
│                              │                  ├ nvd        : 2 
│                              │                  ├ photon     : 2 
│                              │                  ├ redhat     : 1 
│                              │                  ╰ ubuntu     : 1 
│                              ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                              │                  │        │           /A:H 
│                              │                  │        ╰ V3Score : 5.5 
│                              │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                              │                  │        │           /A:H 
│                              │                  │        ╰ V3Score : 5.5 
│                              │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                              │                           │           /A:L 
│                              │                           ╰ V3Score : 3.3 
│                              ├ References       ╭ [0] : https://7asecurity.com/blog/2026/02/zlib-7asecurity-a
│                              │                  │       udit 
│                              │                  ├ [1] : https://7asecurity.com/blog/2026/02/zlib-7asecurity-a
│                              │                  │       udit/ 
│                              │                  ├ [2] : https://7asecurity.com/reports/pentest-report-zlib-RC
│                              │                  │       1.1.pdf 
│                              │                  ├ [3] : https://access.redhat.com/security/cve/CVE-2026-27171 
│                              │                  ├ [4] : https://github.com/advisories/GHSA-h858-mf2m-8jf4 
│                              │                  ├ [5] : https://github.com/madler/zlib/issues/904 
│                              │                  ├ [6] : https://github.com/madler/zlib/releases/tag/v1.3.2 
│                              │                  ├ [7] : https://nvd.nist.gov/vuln/detail/CVE-2026-27171 
│                              │                  ├ [8] : https://ostif.org/zlib-audit-complete 
│                              │                  ├ [9] : https://ostif.org/zlib-audit-complete/ 
│                              │                  ╰ [10]: https://www.cve.org/CVERecord?id=CVE-2026-27171 
│                              ├ PublishedDate   : 2026-02-18T04:16:01.263Z 
│                              ╰ LastModifiedDate: 2026-06-17T10:26:47.357Z 
├ [1] ╭ Target  : Java 
│     ├ Class   : lang-pkgs 
│     ├ Type    : jar 
│     ╰ Packages 
╰ [2] ╭ Target         : usr/bin/pebble 
      ├ Class          : lang-pkgs 
      ├ Type           : gobinary 
      ├ Packages        
      ╰ Vulnerabilities ╭ [0]  ╭ VulnerabilityID : CVE-2026-25681 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5029 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-25681 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:ad413bdde44e4be7ce7f46736ec23d7c5d7bb69169045718e79fe
                        │      │                   8c4e8efb498 
                        │      ├ Title           : golang.org/x/net/html: golang.org/x/net/html: Arbitrary code
                        │      │                    execution via Cross-Site Scripting 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-1021 
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 8.1 
                        │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:37123 
                        │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-25681 
                        │      │                  ├ [2] : https://bugzilla.redhat.com/2480680 
                        │      │                  ├ [3] : https://bugzilla.redhat.com/2480681 
                        │      │                  ├ [4] : https://bugzilla.redhat.com/2480685 
                        │      │                  ├ [5] : https://bugzilla.redhat.com/2480688 
                        │      │                  ├ [6] : https://bugzilla.redhat.com/2480757 
                        │      │                  ├ [7] : https://bugzilla.redhat.com/2480761 
                        │      │                  ├ [8] : https://bugzilla.redhat.com/2493620 
                        │      │                  ├ [9] : https://bugzilla.redhat.com/show_bug.cgi?id=2480680 
                        │      │                  ├ [10]: https://bugzilla.redhat.com/show_bug.cgi?id=2480681 
                        │      │                  ├ [11]: https://bugzilla.redhat.com/show_bug.cgi?id=2480685 
                        │      │                  ├ [12]: https://bugzilla.redhat.com/show_bug.cgi?id=2480688 
                        │      │                  ├ [13]: https://bugzilla.redhat.com/show_bug.cgi?id=2480757 
                        │      │                  ├ [14]: https://bugzilla.redhat.com/show_bug.cgi?id=2480761 
                        │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2493620 
                        │      │                  ├ [16]: https://creativecommons.org/licenses/by/4.0/ 
                        │      │                  ├ [17]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-25681 
                        │      │                  ├ [18]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-27136 
                        │      │                  ├ [19]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39829 
                        │      │                  ├ [20]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39832 
                        │      │                  ├ [21]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39835 
                        │      │                  ├ [22]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-42508 
                        │      │                  ├ [23]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-57231 
                        │      │                  ├ [24]: https://errata.almalinux.org/9/ALSA-2026-37123.html 
                        │      │                  ├ [25]: https://errata.rockylinux.org/RLSA-2026:37123 
                        │      │                  ├ [26]: https://go.dev/cl/781703 
                        │      │                  ├ [27]: https://go.dev/issue/79574 
                        │      │                  ├ [28]: https://groups.google.com/g/golang-announce/c/iI-mYSI
                        │      │                  │       0lu8 
                        │      │                  ├ [29]: https://linux.oracle.com/cve/CVE-2026-25681.html 
                        │      │                  ├ [30]: https://linux.oracle.com/errata/ELSA-2026-37123.html 
                        │      │                  ├ [31]: https://nvd.nist.gov/vuln/detail/CVE-2026-25681 
                        │      │                  ├ [32]: https://pkg.go.dev/vuln/GO-2026-5029 
                        │      │                  ╰ [33]: https://www.cve.org/CVERecord?id=CVE-2026-25681 
                        │      ├ PublishedDate   : 2026-05-22T16:16:19.863Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [1]  ╭ VulnerabilityID : CVE-2026-27136 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5030 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27136 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:a99d57d340b67993dd97b3fbd49729334d0014422699d14ed8de4
                        │      │                   9ba554f2967 
                        │      ├ Title           : golang.org/x/net/html: golang: golang.org/x/net/html:
                        │      │                   Cross-Site Scripting via HTML parsing bypass 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-1021 
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 8.1 
                        │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:37123 
                        │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-27136 
                        │      │                  ├ [2] : https://bugzilla.redhat.com/2480680 
                        │      │                  ├ [3] : https://bugzilla.redhat.com/2480681 
                        │      │                  ├ [4] : https://bugzilla.redhat.com/2480685 
                        │      │                  ├ [5] : https://bugzilla.redhat.com/2480688 
                        │      │                  ├ [6] : https://bugzilla.redhat.com/2480757 
                        │      │                  ├ [7] : https://bugzilla.redhat.com/2480761 
                        │      │                  ├ [8] : https://bugzilla.redhat.com/2493620 
                        │      │                  ├ [9] : https://bugzilla.redhat.com/show_bug.cgi?id=2480680 
                        │      │                  ├ [10]: https://bugzilla.redhat.com/show_bug.cgi?id=2480681 
                        │      │                  ├ [11]: https://bugzilla.redhat.com/show_bug.cgi?id=2480685 
                        │      │                  ├ [12]: https://bugzilla.redhat.com/show_bug.cgi?id=2480688 
                        │      │                  ├ [13]: https://bugzilla.redhat.com/show_bug.cgi?id=2480757 
                        │      │                  ├ [14]: https://bugzilla.redhat.com/show_bug.cgi?id=2480761 
                        │      │                  ├ [15]: https://bugzilla.redhat.com/show_bug.cgi?id=2493620 
                        │      │                  ├ [16]: https://creativecommons.org/licenses/by/4.0/ 
                        │      │                  ├ [17]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-25681 
                        │      │                  ├ [18]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-27136 
                        │      │                  ├ [19]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39829 
                        │      │                  ├ [20]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39832 
                        │      │                  ├ [21]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39835 
                        │      │                  ├ [22]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-42508 
                        │      │                  ├ [23]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-57231 
                        │      │                  ├ [24]: https://errata.almalinux.org/9/ALSA-2026-37123.html 
                        │      │                  ├ [25]: https://errata.rockylinux.org/RLSA-2026:37123 
                        │      │                  ├ [26]: https://go.dev/cl/781685 
                        │      │                  ├ [27]: https://go.dev/issue/79575 
                        │      │                  ├ [28]: https://groups.google.com/g/golang-announce/c/iI-mYSI
                        │      │                  │       0lu8 
                        │      │                  ├ [29]: https://linux.oracle.com/cve/CVE-2026-27136.html 
                        │      │                  ├ [30]: https://linux.oracle.com/errata/ELSA-2026-37123.html 
                        │      │                  ├ [31]: https://nvd.nist.gov/vuln/detail/CVE-2026-27136 
                        │      │                  ├ [32]: https://pkg.go.dev/vuln/GO-2026-5030 
                        │      │                  ╰ [33]: https://www.cve.org/CVERecord?id=CVE-2026-27136 
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.087Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [2]  ╭ VulnerabilityID : CVE-2026-33814 
                        │      ├ VendorIDs        ─ [0]: GO-2026-4918 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.53.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ SeveritySource  : nvd 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-33814 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:0cec0d4728c7d71f03859b60e68b3c55a8239a2c6333beea50aef
                        │      │                   832f29c4e30 
                        │      ├ Title           : net/http/internal/http2: golang: golang.org/x/net: Go
                        │      │                   HTTP/2: Denial of Service via malformed
                        │      │                   SETTINGS_MAX_FRAME_SIZE frame 
                        │      ├ Description     : When processing HTTP/2 SETTINGS frames, transport will enter
                        │      │                    an infinite loop of writing CONTINUATION frames if it
                        │      │                   receives a SETTINGS_MAX_FRAME_SIZE with a value of 0. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ╭ [0]: CWE-835 
                        │      │                  ╰ [1]: CWE-606 
                        │      ├ VendorSeverity   ╭ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ nvd        : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ ubuntu     : 2 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ├ nvd     ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:23262 
                        │      │                  ├ [1] : https://access.redhat.com/errata/RHSA-2026:23264 
                        │      │                  ├ [2] : https://access.redhat.com/errata/RHSA-2026:33120 
                        │      │                  ├ [3] : https://access.redhat.com/errata/RHSA-2026:33123 
                        │      │                  ├ [4] : https://access.redhat.com/errata/RHSA-2026:33142 
                        │      │                  ├ [5] : https://access.redhat.com/errata/RHSA-2026:33150 
                        │      │                  ├ [6] : https://access.redhat.com/errata/RHSA-2026:34342 
                        │      │                  ├ [7] : https://access.redhat.com/errata/RHSA-2026:37387 
                        │      │                  ├ [8] : https://access.redhat.com/errata/RHSA-2026:42644 
                        │      │                  ├ [9] : https://access.redhat.com/errata/RHSA-2026:43692 
                        │      │                  ├ [10]: https://access.redhat.com/errata/RHSA-2026:50205 
                        │      │                  ├ [11]: https://access.redhat.com/errata/RHSA-2026:54274 
                        │      │                  ├ [12]: https://access.redhat.com/errata/RHSA-2026:54283 
                        │      │                  ├ [13]: https://access.redhat.com/errata/RHSA-2026:54284 
                        │      │                  ├ [14]: https://access.redhat.com/errata/RHSA-2026:54285 
                        │      │                  ├ [15]: https://access.redhat.com/errata/RHSA-2026:54286 
                        │      │                  ├ [16]: https://access.redhat.com/errata/RHSA-2026:54287 
                        │      │                  ├ [17]: https://access.redhat.com/security/cve/CVE-2026-33814 
                        │      │                  ├ [18]: https://bugzilla.redhat.com/show_bug.cgi?id=2467815 
                        │      │                  ├ [19]: https://github.com/golang/go/issues/78476 
                        │      │                  ├ [20]: https://go-review.googlesource.com/c/go/+/761581 
                        │      │                  ├ [21]: https://go-review.googlesource.com/c/net/+/761640 
                        │      │                  ├ [22]: https://go.dev/cl/761581 
                        │      │                  ├ [23]: https://go.dev/cl/761640 
                        │      │                  ├ [24]: https://go.dev/issue/78476 
                        │      │                  ├ [25]: https://groups.google.com/g/golang-announce/c/qcCIEXs
                        │      │                  │       o47M 
                        │      │                  ├ [26]: https://linux.oracle.com/cve/CVE-2026-33814.html 
                        │      │                  ├ [27]: https://linux.oracle.com/errata/ELSA-2026-22121.html 
                        │      │                  ├ [28]: https://nvd.nist.gov/vuln/detail/CVE-2026-33814 
                        │      │                  ├ [29]: https://pkg.go.dev/vuln/GO-2026-4918 
                        │      │                  ├ [30]: https://security.access.redhat.com/data/csaf/v2/vex/2
                        │      │                  │       026/cve-2026-33814.json 
                        │      │                  ├ [31]: https://ubuntu.com/security/notices/USN-8430-1 
                        │      │                  ├ [32]: https://ubuntu.com/security/notices/USN-8471-1 
                        │      │                  ├ [33]: https://ubuntu.com/security/notices/USN-8472-1 
                        │      │                  ├ [34]: https://ubuntu.com/security/notices/USN-8473-1 
                        │      │                  ╰ [35]: https://www.cve.org/CVERecord?id=CVE-2026-33814 
                        │      ├ PublishedDate   : 2026-05-07T20:16:42.88Z 
                        │      ╰ LastModifiedDate: 2026-08-13T13:18:25.52Z 
                        ├ [3]  ╭ VulnerabilityID : CVE-2026-39821 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5026 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39821 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:718be6aa3abb1a09713545f4e7de52424c77b1b47ca00f0b16074
                        │      │                   a28ca97b58c 
                        │      ├ Title           : golang.org/x/net/idna: golang: net/http:
                        │      │                   golang.org/x/net/idna: Privilege escalation via incorrect
                        │      │                   Punycode label processing 
                        │      ├ Description     : The ToASCII and ToUnicode functions incorrectly accept
                        │      │                   Punycode-encoded labels that decode to an ASCII-only label.
                        │      │                   For example, ToUnicode("xn--example-.com") incorrectly
                        │      │                   returns the name "example.com" rather than an error. This
                        │      │                   behavior can lead to privilege escalation in programs using
                        │      │                   the idna package. For example, a program which performs
                        │      │                   privilege checks on the ASCII hostname may reject
                        │      │                   "example.com" but permit "xn--example-.com". If that program
                        │      │                    subsequently converts the ASCII hostname to Unicode, it
                        │      │                   will inadvertently permits access to the Unicode name
                        │      │                   "example.com". 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-1289 
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ azure      : 4 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ├ rocky      : 3 
                        │      │                  ╰ ubuntu     : 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:L/UI:N/S:C/C:H/I:H
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 8.2 
                        │      ├ References       ╭ [0]  : https://access.redhat.com/errata/RHSA-2026:23262 
                        │      │                  ├ [1]  : https://access.redhat.com/errata/RHSA-2026:23264 
                        │      │                  ├ [2]  : https://access.redhat.com/errata/RHSA-2026:26546 
                        │      │                  ├ [3]  : https://access.redhat.com/errata/RHSA-2026:26547 
                        │      │                  ├ [4]  : https://access.redhat.com/errata/RHSA-2026:30650 
                        │      │                  ├ [5]  : https://access.redhat.com/errata/RHSA-2026:30651 
                        │      │                  ├ [6]  : https://access.redhat.com/errata/RHSA-2026:30853 
                        │      │                  ├ [7]  : https://access.redhat.com/errata/RHSA-2026:30854 
                        │      │                  ├ [8]  : https://access.redhat.com/errata/RHSA-2026:30855 
                        │      │                  ├ [9]  : https://access.redhat.com/errata/RHSA-2026:33155 
                        │      │                  ├ [10] : https://access.redhat.com/errata/RHSA-2026:33160 
                        │      │                  ├ [11] : https://access.redhat.com/errata/RHSA-2026:33163 
                        │      │                  ├ [12] : https://access.redhat.com/errata/RHSA-2026:33173 
                        │      │                  ├ [13] : https://access.redhat.com/errata/RHSA-2026:33183 
                        │      │                  ├ [14] : https://access.redhat.com/errata/RHSA-2026:33524 
                        │      │                  ├ [15] : https://access.redhat.com/errata/RHSA-2026:33531 
                        │      │                  ├ [16] : https://access.redhat.com/errata/RHSA-2026:34342 
                        │      │                  ├ [17] : https://access.redhat.com/errata/RHSA-2026:34357 
                        │      │                  ├ [18] : https://access.redhat.com/errata/RHSA-2026:34359 
                        │      │                  ├ [19] : https://access.redhat.com/errata/RHSA-2026:34364 
                        │      │                  ├ [20] : https://access.redhat.com/errata/RHSA-2026:34789 
                        │      │                  ├ [21] : https://access.redhat.com/errata/RHSA-2026:35826 
                        │      │                  ├ [22] : https://access.redhat.com/errata/RHSA-2026:35827 
                        │      │                  ├ [23] : https://access.redhat.com/errata/RHSA-2026:35828 
                        │      │                  ├ [24] : https://access.redhat.com/errata/RHSA-2026:35829 
                        │      │                  ├ [25] : https://access.redhat.com/errata/RHSA-2026:35830 
                        │      │                  ├ [26] : https://access.redhat.com/errata/RHSA-2026:35831 
                        │      │                  ├ [27] : https://access.redhat.com/errata/RHSA-2026:35993 
                        │      │                  ├ [28] : https://access.redhat.com/errata/RHSA-2026:35994 
                        │      │                  ├ [29] : https://access.redhat.com/errata/RHSA-2026:36105 
                        │      │                  ├ [30] : https://access.redhat.com/errata/RHSA-2026:36167 
                        │      │                  ├ [31] : https://access.redhat.com/errata/RHSA-2026:36207 
                        │      │                  ├ [32] : https://access.redhat.com/errata/RHSA-2026:36648 
                        │      │                  ├ [33] : https://access.redhat.com/errata/RHSA-2026:36651 
                        │      │                  ├ [34] : https://access.redhat.com/errata/RHSA-2026:36796 
                        │      │                  ├ [35] : https://access.redhat.com/errata/RHSA-2026:36797 
                        │      │                  ├ [36] : https://access.redhat.com/errata/RHSA-2026:36808 
                        │      │                  ├ [37] : https://access.redhat.com/errata/RHSA-2026:36820 
                        │      │                  ├ [38] : https://access.redhat.com/errata/RHSA-2026:36883 
                        │      │                  ├ [39] : https://access.redhat.com/errata/RHSA-2026:37387 
                        │      │                  ├ [40] : https://access.redhat.com/errata/RHSA-2026:37435 
                        │      │                  ├ [41] : https://access.redhat.com/errata/RHSA-2026:37436 
                        │      │                  ├ [42] : https://access.redhat.com/errata/RHSA-2026:38995 
                        │      │                  ├ [43] : https://access.redhat.com/errata/RHSA-2026:39005 
                        │      │                  ├ [44] : https://access.redhat.com/errata/RHSA-2026:39573 
                        │      │                  ├ [45] : https://access.redhat.com/errata/RHSA-2026:39879 
                        │      │                  ├ [46] : https://access.redhat.com/errata/RHSA-2026:40118 
                        │      │                  ├ [47] : https://access.redhat.com/errata/RHSA-2026:40262 
                        │      │                  ├ [48] : https://access.redhat.com/errata/RHSA-2026:40945 
                        │      │                  ├ [49] : https://access.redhat.com/errata/RHSA-2026:41019 
                        │      │                  ├ [50] : https://access.redhat.com/errata/RHSA-2026:41030 
                        │      │                  ├ [51] : https://access.redhat.com/errata/RHSA-2026:41031 
                        │      │                  ├ [52] : https://access.redhat.com/errata/RHSA-2026:41036 
                        │      │                  ├ [53] : https://access.redhat.com/errata/RHSA-2026:41055 
                        │      │                  ├ [54] : https://access.redhat.com/errata/RHSA-2026:41066 
                        │      │                  ├ [55] : https://access.redhat.com/errata/RHSA-2026:41928 
                        │      │                  ├ [56] : https://access.redhat.com/errata/RHSA-2026:41930 
                        │      │                  ├ [57] : https://access.redhat.com/errata/RHSA-2026:42043 
                        │      │                  ├ [58] : https://access.redhat.com/errata/RHSA-2026:42047 
                        │      │                  ├ [59] : https://access.redhat.com/errata/RHSA-2026:42048 
                        │      │                  ├ [60] : https://access.redhat.com/errata/RHSA-2026:42049 
                        │      │                  ├ [61] : https://access.redhat.com/errata/RHSA-2026:42050 
                        │      │                  ├ [62] : https://access.redhat.com/errata/RHSA-2026:42051 
                        │      │                  ├ [63] : https://access.redhat.com/errata/RHSA-2026:42078 
                        │      │                  ├ [64] : https://access.redhat.com/errata/RHSA-2026:42079 
                        │      │                  ├ [65] : https://access.redhat.com/errata/RHSA-2026:42080 
                        │      │                  ├ [66] : https://access.redhat.com/errata/RHSA-2026:42082 
                        │      │                  ├ [67] : https://access.redhat.com/errata/RHSA-2026:42132 
                        │      │                  ├ [68] : https://access.redhat.com/errata/RHSA-2026:42142 
                        │      │                  ├ [69] : https://access.redhat.com/errata/RHSA-2026:42146 
                        │      │                  ├ [70] : https://access.redhat.com/errata/RHSA-2026:42150 
                        │      │                  ├ [71] : https://access.redhat.com/errata/RHSA-2026:42151 
                        │      │                  ├ [72] : https://access.redhat.com/errata/RHSA-2026:42240 
                        │      │                  ├ [73] : https://access.redhat.com/errata/RHSA-2026:42644 
                        │      │                  ├ [74] : https://access.redhat.com/errata/RHSA-2026:42796 
                        │      │                  ├ [75] : https://access.redhat.com/errata/RHSA-2026:42852 
                        │      │                  ├ [76] : https://access.redhat.com/errata/RHSA-2026:43038 
                        │      │                  ├ [77] : https://access.redhat.com/errata/RHSA-2026:43052 
                        │      │                  ├ [78] : https://access.redhat.com/errata/RHSA-2026:43692 
                        │      │                  ├ [79] : https://access.redhat.com/errata/RHSA-2026:44622 
                        │      │                  ├ [80] : https://access.redhat.com/errata/RHSA-2026:44624 
                        │      │                  ├ [81] : https://access.redhat.com/errata/RHSA-2026:46395 
                        │      │                  ├ [82] : https://access.redhat.com/errata/RHSA-2026:47149 
                        │      │                  ├ [83] : https://access.redhat.com/errata/RHSA-2026:47735 
                        │      │                  ├ [84] : https://access.redhat.com/errata/RHSA-2026:47737 
                        │      │                  ├ [85] : https://access.redhat.com/errata/RHSA-2026:47952 
                        │      │                  ├ [86] : https://access.redhat.com/errata/RHSA-2026:50300 
                        │      │                  ├ [87] : https://access.redhat.com/errata/RHSA-2026:50843 
                        │      │                  ├ [88] : https://access.redhat.com/errata/RHSA-2026:51033 
                        │      │                  ├ [89] : https://access.redhat.com/errata/RHSA-2026:51112 
                        │      │                  ├ [90] : https://access.redhat.com/errata/RHSA-2026:51187 
                        │      │                  ├ [91] : https://access.redhat.com/errata/RHSA-2026:51194 
                        │      │                  ├ [92] : https://access.redhat.com/errata/RHSA-2026:51341 
                        │      │                  ├ [93] : https://access.redhat.com/errata/RHSA-2026:52826 
                        │      │                  ├ [94] : https://access.redhat.com/errata/RHSA-2026:53374 
                        │      │                  ├ [95] : https://access.redhat.com/errata/RHSA-2026:53412 
                        │      │                  ├ [96] : https://access.redhat.com/errata/RHSA-2026:53413 
                        │      │                  ├ [97] : https://access.redhat.com/errata/RHSA-2026:53415 
                        │      │                  ├ [98] : https://access.redhat.com/errata/RHSA-2026:53530 
                        │      │                  ├ [99] : https://access.redhat.com/errata/RHSA-2026:54191 
                        │      │                  ├ [100]: https://access.redhat.com/errata/RHSA-2026:54274 
                        │      │                  ├ [101]: https://access.redhat.com/errata/RHSA-2026:54283 
                        │      │                  ├ [102]: https://access.redhat.com/errata/RHSA-2026:54284 
                        │      │                  ├ [103]: https://access.redhat.com/errata/RHSA-2026:54285 
                        │      │                  ├ [104]: https://access.redhat.com/errata/RHSA-2026:54286 
                        │      │                  ├ [105]: https://access.redhat.com/errata/RHSA-2026:54287 
                        │      │                  ├ [106]: https://access.redhat.com/errata/RHSA-2026:54395 
                        │      │                  ├ [107]: https://access.redhat.com/errata/RHSA-2026:54401 
                        │      │                  ├ [108]: https://access.redhat.com/errata/RHSA-2026:54435 
                        │      │                  ├ [109]: https://access.redhat.com/errata/RHSA-2026:54441 
                        │      │                  ├ [110]: https://access.redhat.com/security/cve/CVE-2026-39821 
                        │      │                  ├ [111]: https://bugzilla.redhat.com/2480756 
                        │      │                  ├ [112]: https://bugzilla.redhat.com/show_bug.cgi?id=2480756 
                        │      │                  ├ [113]: https://bugzilla.redhat.com/show_bug.cgi?id=2498152 
                        │      │                  ├ [114]: https://creativecommons.org/licenses/by/4.0/ 
                        │      │                  ├ [115]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
                        │      │                  │        026-39821 
                        │      │                  ├ [116]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
                        │      │                  │        026-39822 
                        │      │                  ├ [117]: https://errata.almalinux.org/9/ALSA-2026-37435.html 
                        │      │                  ├ [118]: https://errata.rockylinux.org/RLSA-2026:37435 
                        │      │                  ├ [119]: https://github.com/golang/go/issues/78760 
                        │      │                  ├ [120]: https://go.dev/cl/767220 
                        │      │                  ├ [121]: https://go.dev/issue/78760 
                        │      │                  ├ [122]: https://groups.google.com/g/golang-announce/c/94pEor
                        │      │                  │        npRlI 
                        │      │                  ├ [123]: https://groups.google.com/g/golang-announce/c/iI-mYS
                        │      │                  │        I0lu8 
                        │      │                  ├ [124]: https://linux.oracle.com/cve/CVE-2026-39821.html 
                        │      │                  ├ [125]: https://linux.oracle.com/errata/ELSA-2026-46395.html 
                        │      │                  ├ [126]: https://nvd.nist.gov/vuln/detail/CVE-2026-39821 
                        │      │                  ├ [127]: https://pkg.go.dev/vuln/GO-2026-5026 
                        │      │                  ├ [128]: https://security.access.redhat.com/data/csaf/v2/vex/
                        │      │                  │        2026/cve-2026-39821.json 
                        │      │                  ├ [129]: https://ubuntu.com/security/notices/USN-8416-1 
                        │      │                  ╰ [130]: https://www.cve.org/CVERecord?id=CVE-2026-39821 
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.41Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:19.973Z 
                        ├ [4]  ╭ VulnerabilityID : CVE-2026-46600 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5942 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.56.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46600 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:93e768e34dbe2d91836eca6dc1a4916d74e3d68161b9265a5a021
                        │      │                   ca944d7fcbb 
                        │      ├ Title           : golang.org/x/net/dns/dnsmessage:
                        │      │                   golang.org/x/net/dns/dnsmessage: Denial of Service via
                        │      │                   invalid DNS record parsing 
                        │      ├ Description     : Parsing an invalid SVCB or HTTPS RR can panic when the size
                        │      │                   of a parameter value overflows the message buffer. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-125 
                        │      ├ VendorSeverity   ─ redhat: 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
                        │      │                           │           /A:H 
                        │      │                           ╰ V3Score : 7.5 
                        │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46600 
                        │      │                  ├ [1]: https://go.dev/cl/786345 
                        │      │                  ├ [2]: https://go.dev/issue/79795 
                        │      │                  ├ [3]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-46600 
                        │      │                  ├ [5]: https://pkg.go.dev/vuln/GO-2026-5942 
                        │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-46600 
                        │      ├ PublishedDate   : 2026-07-21T20:17:01.213Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:21.913Z 
                        ├ [5]  ╭ VulnerabilityID : CVE-2025-47911 
                        │      ├ VendorIDs        ─ [0]: GO-2026-4440 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.45.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ SeveritySource  : nvd 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-47911 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:9eb5b9d62ffa350a33b5141113bd296a44c642266b16b7019cb7f
                        │      │                   1ccc0228f31 
                        │      ├ Title           : golang.org/x/net/html: Quadratic parsing complexity in
                        │      │                   golang.org/x/net/html 
                        │      ├ Description     : The html.Parse function in golang.org/x/net/html has
                        │      │                   quadratic parsing complexity when processing certain inputs,
                        │      │                    which can lead to denial of service (DoS) if an attacker
                        │      │                   provides specially crafted HTML content. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ VendorSeverity   ╭ amazon     : 2 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ cbl-mariner: 2 
                        │      │                  ├ nvd        : 2 
                        │      │                  ├ redhat     : 2 
                        │      │                  ╰ ubuntu     : 2 
                        │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
                        │      │                  │        │           /A:L 
                        │      │                  │        ╰ V3Score : 5.3 
                        │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
                        │      │                           │           /A:L 
                        │      │                           ╰ V3Score : 5.3 
                        │      ├ References       ╭ [0] : https://access.redhat.com/security/cve/CVE-2025-47911 
                        │      │                  ├ [1] : https://github.com/golang/go/issues/75682 
                        │      │                  ├ [2] : https://github.com/golang/vulndb/issues/4440 
                        │      │                  ├ [3] : https://go.dev/cl/709876 
                        │      │                  ├ [4] : https://groups.google.com/g/golang-announce/c/jnQcOYp
                        │      │                  │       iR2c 
                        │      │                  ├ [5] : https://nvd.nist.gov/vuln/detail/CVE-2025-47911 
                        │      │                  ├ [6] : https://pkg.go.dev/vuln/GO-2026-4440 
                        │      │                  ├ [7] : https://ubuntu.com/security/notices/USN-8089-1 
                        │      │                  ├ [8] : https://ubuntu.com/security/notices/USN-8089-2 
                        │      │                  ├ [9] : https://ubuntu.com/security/notices/USN-8089-3 
                        │      │                  ╰ [10]: https://www.cve.org/CVERecord?id=CVE-2025-47911 
                        │      ├ PublishedDate   : 2026-02-05T18:16:09.893Z 
                        │      ╰ LastModifiedDate: 2026-06-17T09:28:50.07Z 
                        ├ [6]  ╭ VulnerabilityID : CVE-2025-58190 
                        │      ├ VendorIDs        ─ [0]: GO-2026-4441 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.45.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ SeveritySource  : nvd 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-58190 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:bba9a2474962ccceafb1ab176b047e25c61f65fd656e6dad5a599
                        │      │                   0deda8ceb38 
                        │      ├ Title           : golang.org/x/net/html: Infinite parsing loop in
                        │      │                   golang.org/x/net 
                        │      ├ Description     : The html.Parse function in golang.org/x/net/html has an
                        │      │                   infinite parsing loop when processing certain inputs, which
                        │      │                   can lead to denial of service (DoS) if an attacker provides
                        │      │                   specially crafted HTML content. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs           ─ [0]: CWE-835 
                        │      ├ VendorSeverity   ╭ amazon     : 2 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ cbl-mariner: 2 
                        │      │                  ├ nvd        : 2 
                        │      │                  ├ redhat     : 2 
                        │      │                  ╰ ubuntu     : 2 
                        │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
                        │      │                  │        │           /A:L 
                        │      │                  │        ╰ V3Score : 5.3 
                        │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:N/I:N
                        │      │                           │           /A:L 
                        │      │                           ╰ V3Score : 4.3 
                        │      ├ References       ╭ [0] : https://access.redhat.com/security/cve/CVE-2025-58190 
                        │      │                  ├ [1] : https://github.com/golang/go/issues/70179 
                        │      │                  ├ [2] : https://github.com/golang/vulndb/issues/4441 
                        │      │                  ├ [3] : https://go.dev/cl/709875 
                        │      │                  ├ [4] : https://groups.google.com/g/golang-announce/c/jnQcOYp
                        │      │                  │       iR2c 
                        │      │                  ├ [5] : https://nvd.nist.gov/vuln/detail/CVE-2025-58190 
                        │      │                  ├ [6] : https://pkg.go.dev/vuln/GO-2026-4441 
                        │      │                  ├ [7] : https://ubuntu.com/security/notices/USN-8089-1 
                        │      │                  ├ [8] : https://ubuntu.com/security/notices/USN-8089-2 
                        │      │                  ├ [9] : https://ubuntu.com/security/notices/USN-8089-3 
                        │      │                  ╰ [10]: https://www.cve.org/CVERecord?id=CVE-2025-58190 
                        │      ├ PublishedDate   : 2026-02-05T18:16:10.027Z 
                        │      ╰ LastModifiedDate: 2026-06-17T09:44:02.557Z 
                        ├ [7]  ╭ VulnerabilityID : CVE-2026-25680 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5028 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-25680 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:90af48528ec6a741fc47b027153b8e5d7a96358bf0ddf14ee875e
                        │      │                   9eb12ef3715 
                        │      ├ Title           : golang.org/x/net/html: golang.org/x/net/html: Denial of
                        │      │                   Service due to excessive HTML parsing 
                        │      ├ Description     : Parsing arbitrary HTML can consume excessive CPU time,
                        │      │                   possibly leading to denial of service. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs           ─ [0]: CWE-400 
                        │      ├ VendorSeverity   ╭ amazon: 3 
                        │      │                  ├ azure : 2 
                        │      │                  ╰ redhat: 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:N/I:N
                        │      │                           │           /A:H 
                        │      │                           ╰ V3Score : 6.5 
                        │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-25680 
                        │      │                  ├ [1]: https://go.dev/cl/781702 
                        │      │                  ├ [2]: https://go.dev/issue/79573 
                        │      │                  ├ [3]: https://groups.google.com/g/golang-announce/c/iI-mYSI0
                        │      │                  │      lu8 
                        │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-25680 
                        │      │                  ├ [5]: https://pkg.go.dev/vuln/GO-2026-5028 
                        │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-25680 
                        │      ├ PublishedDate   : 2026-05-22T16:16:19.753Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [8]  ╭ VulnerabilityID : CVE-2026-42502 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5027 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42502 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:5a6ca02de031aaf3f026fce2936f6bbc66ceac63fd71c7a62c78f
                        │      │                   96bc22e1fb6 
                        │      ├ Title           : golang.org/x/net/html: golang: golang.org/x/net/html:
                        │      │                   Cross-Site Scripting via unexpected HTML tree rendering 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs           ─ [0]: CWE-1021 
                        │      ├ VendorSeverity   ╭ amazon: 3 
                        │      │                  ├ azure : 2 
                        │      │                  ╰ redhat: 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 6.1 
                        │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-42502 
                        │      │                  ├ [1]: https://go.dev/cl/781701 
                        │      │                  ├ [2]: https://go.dev/issue/79572 
                        │      │                  ├ [3]: https://groups.google.com/g/golang-announce/c/iI-mYSI0
                        │      │                  │      lu8 
                        │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-42502 
                        │      │                  ├ [5]: https://pkg.go.dev/vuln/GO-2026-5027 
                        │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42502 
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.587Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [9]  ╭ VulnerabilityID : CVE-2026-42506 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5025 
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42506 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:30bcabdbd4bac55e1872e405d1079b1e6512fae7f7fa36622c569
                        │      │                   b97957ed680 
                        │      ├ Title           : golang.org/x/net/html: golang.org/x/net/html: Cross-Site
                        │      │                   Scripting (XSS) via arbitrary HTML parsing 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs           ─ [0]: CWE-79 
                        │      ├ VendorSeverity   ╭ amazon: 3 
                        │      │                  ├ azure : 2 
                        │      │                  ╰ redhat: 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:L/I:L
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 5.4 
                        │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-42506 
                        │      │                  ├ [1]: https://go.dev/cl/781700 
                        │      │                  ├ [2]: https://go.dev/issue/79571 
                        │      │                  ├ [3]: https://groups.google.com/g/golang-announce/c/iI-mYSI0
                        │      │                  │      lu8 
                        │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-42506 
                        │      │                  ├ [5]: https://pkg.go.dev/vuln/GO-2026-5025 
                        │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-42506 
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.803Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [10] ╭ VulnerabilityID : CVE-2026-39824 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5024 
                        │      ├ PkgID           : golang.org/x/sys@v0.33.0 
                        │      ├ PkgName         : golang.org/x/sys 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/sys@v0.33.0 
                        │      │                  ╰ UID : a350d4cc028089d4 
                        │      ├ InstalledVersion: v0.33.0 
                        │      ├ FixedVersion    : 0.44.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39824 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:3c72995312b859071cbc31b7f8fb938364b77d609c1c8ab3d8054
                        │      │                   1e583dae83a 
                        │      ├ Title           : Invoking integer overflow in NewNTUnicodeString in
                        │      │                   golang.org/x/sys/windows 
                        │      ├ Description     : NewNTUnicodeString does not check for string length
                        │      │                   overflow. When provided with a string that overflows the
                        │      │                   maximum size of a NTUnicodeString (a 16-bit number of
                        │      │                   bytes), it returns a truncated string rather than an
                        │      │                   error. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ CweIDs           ─ [0]: CWE-190 
                        │      ├ References       ╭ [0]: https://go.dev/cl/770080 
                        │      │                  ├ [1]: https://go.dev/issue/78916 
                        │      │                  ├ [2]: https://groups.google.com/g/golang-announce/c/6MMI8Lj-
                        │      │                  │      Atg 
                        │      │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-5024 
                        │      ├ PublishedDate   : 2026-05-22T20:16:33.057Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [11] ╭ VulnerabilityID : CVE-2026-39821 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5026 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39821 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:5615160c33be3de320f8a6a2d3e3b58b516b0d31238edc0d86be5
                        │      │                   4b1903ffe0c 
                        │      ├ Title           : golang.org/x/net/idna: golang: net/http:
                        │      │                   golang.org/x/net/idna: Privilege escalation via incorrect
                        │      │                   Punycode label processing 
                        │      ├ Description     : The ToASCII and ToUnicode functions incorrectly accept
                        │      │                   Punycode-encoded labels that decode to an ASCII-only label.
                        │      │                   For example, ToUnicode("xn--example-.com") incorrectly
                        │      │                   returns the name "example.com" rather than an error. This
                        │      │                   behavior can lead to privilege escalation in programs using
                        │      │                   the idna package. For example, a program which performs
                        │      │                   privilege checks on the ASCII hostname may reject
                        │      │                   "example.com" but permit "xn--example-.com". If that program
                        │      │                    subsequently converts the ASCII hostname to Unicode, it
                        │      │                   will inadvertently permits access to the Unicode name
                        │      │                   "example.com". 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-1289 
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ azure      : 4 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ├ rocky      : 3 
                        │      │                  ╰ ubuntu     : 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:L/UI:N/S:C/C:H/I:H
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 8.2 
                        │      ├ References       ╭ [0]  : https://access.redhat.com/errata/RHSA-2026:23262 
                        │      │                  ├ [1]  : https://access.redhat.com/errata/RHSA-2026:23264 
                        │      │                  ├ [2]  : https://access.redhat.com/errata/RHSA-2026:26546 
                        │      │                  ├ [3]  : https://access.redhat.com/errata/RHSA-2026:26547 
                        │      │                  ├ [4]  : https://access.redhat.com/errata/RHSA-2026:30650 
                        │      │                  ├ [5]  : https://access.redhat.com/errata/RHSA-2026:30651 
                        │      │                  ├ [6]  : https://access.redhat.com/errata/RHSA-2026:30853 
                        │      │                  ├ [7]  : https://access.redhat.com/errata/RHSA-2026:30854 
                        │      │                  ├ [8]  : https://access.redhat.com/errata/RHSA-2026:30855 
                        │      │                  ├ [9]  : https://access.redhat.com/errata/RHSA-2026:33155 
                        │      │                  ├ [10] : https://access.redhat.com/errata/RHSA-2026:33160 
                        │      │                  ├ [11] : https://access.redhat.com/errata/RHSA-2026:33163 
                        │      │                  ├ [12] : https://access.redhat.com/errata/RHSA-2026:33173 
                        │      │                  ├ [13] : https://access.redhat.com/errata/RHSA-2026:33183 
                        │      │                  ├ [14] : https://access.redhat.com/errata/RHSA-2026:33524 
                        │      │                  ├ [15] : https://access.redhat.com/errata/RHSA-2026:33531 
                        │      │                  ├ [16] : https://access.redhat.com/errata/RHSA-2026:34342 
                        │      │                  ├ [17] : https://access.redhat.com/errata/RHSA-2026:34357 
                        │      │                  ├ [18] : https://access.redhat.com/errata/RHSA-2026:34359 
                        │      │                  ├ [19] : https://access.redhat.com/errata/RHSA-2026:34364 
                        │      │                  ├ [20] : https://access.redhat.com/errata/RHSA-2026:34789 
                        │      │                  ├ [21] : https://access.redhat.com/errata/RHSA-2026:35826 
                        │      │                  ├ [22] : https://access.redhat.com/errata/RHSA-2026:35827 
                        │      │                  ├ [23] : https://access.redhat.com/errata/RHSA-2026:35828 
                        │      │                  ├ [24] : https://access.redhat.com/errata/RHSA-2026:35829 
                        │      │                  ├ [25] : https://access.redhat.com/errata/RHSA-2026:35830 
                        │      │                  ├ [26] : https://access.redhat.com/errata/RHSA-2026:35831 
                        │      │                  ├ [27] : https://access.redhat.com/errata/RHSA-2026:35993 
                        │      │                  ├ [28] : https://access.redhat.com/errata/RHSA-2026:35994 
                        │      │                  ├ [29] : https://access.redhat.com/errata/RHSA-2026:36105 
                        │      │                  ├ [30] : https://access.redhat.com/errata/RHSA-2026:36167 
                        │      │                  ├ [31] : https://access.redhat.com/errata/RHSA-2026:36207 
                        │      │                  ├ [32] : https://access.redhat.com/errata/RHSA-2026:36648 
                        │      │                  ├ [33] : https://access.redhat.com/errata/RHSA-2026:36651 
                        │      │                  ├ [34] : https://access.redhat.com/errata/RHSA-2026:36796 
                        │      │                  ├ [35] : https://access.redhat.com/errata/RHSA-2026:36797 
                        │      │                  ├ [36] : https://access.redhat.com/errata/RHSA-2026:36808 
                        │      │                  ├ [37] : https://access.redhat.com/errata/RHSA-2026:36820 
                        │      │                  ├ [38] : https://access.redhat.com/errata/RHSA-2026:36883 
                        │      │                  ├ [39] : https://access.redhat.com/errata/RHSA-2026:37387 
                        │      │                  ├ [40] : https://access.redhat.com/errata/RHSA-2026:37435 
                        │      │                  ├ [41] : https://access.redhat.com/errata/RHSA-2026:37436 
                        │      │                  ├ [42] : https://access.redhat.com/errata/RHSA-2026:38995 
                        │      │                  ├ [43] : https://access.redhat.com/errata/RHSA-2026:39005 
                        │      │                  ├ [44] : https://access.redhat.com/errata/RHSA-2026:39573 
                        │      │                  ├ [45] : https://access.redhat.com/errata/RHSA-2026:39879 
                        │      │                  ├ [46] : https://access.redhat.com/errata/RHSA-2026:40118 
                        │      │                  ├ [47] : https://access.redhat.com/errata/RHSA-2026:40262 
                        │      │                  ├ [48] : https://access.redhat.com/errata/RHSA-2026:40945 
                        │      │                  ├ [49] : https://access.redhat.com/errata/RHSA-2026:41019 
                        │      │                  ├ [50] : https://access.redhat.com/errata/RHSA-2026:41030 
                        │      │                  ├ [51] : https://access.redhat.com/errata/RHSA-2026:41031 
                        │      │                  ├ [52] : https://access.redhat.com/errata/RHSA-2026:41036 
                        │      │                  ├ [53] : https://access.redhat.com/errata/RHSA-2026:41055 
                        │      │                  ├ [54] : https://access.redhat.com/errata/RHSA-2026:41066 
                        │      │                  ├ [55] : https://access.redhat.com/errata/RHSA-2026:41928 
                        │      │                  ├ [56] : https://access.redhat.com/errata/RHSA-2026:41930 
                        │      │                  ├ [57] : https://access.redhat.com/errata/RHSA-2026:42043 
                        │      │                  ├ [58] : https://access.redhat.com/errata/RHSA-2026:42047 
                        │      │                  ├ [59] : https://access.redhat.com/errata/RHSA-2026:42048 
                        │      │                  ├ [60] : https://access.redhat.com/errata/RHSA-2026:42049 
                        │      │                  ├ [61] : https://access.redhat.com/errata/RHSA-2026:42050 
                        │      │                  ├ [62] : https://access.redhat.com/errata/RHSA-2026:42051 
                        │      │                  ├ [63] : https://access.redhat.com/errata/RHSA-2026:42078 
                        │      │                  ├ [64] : https://access.redhat.com/errata/RHSA-2026:42079 
                        │      │                  ├ [65] : https://access.redhat.com/errata/RHSA-2026:42080 
                        │      │                  ├ [66] : https://access.redhat.com/errata/RHSA-2026:42082 
                        │      │                  ├ [67] : https://access.redhat.com/errata/RHSA-2026:42132 
                        │      │                  ├ [68] : https://access.redhat.com/errata/RHSA-2026:42142 
                        │      │                  ├ [69] : https://access.redhat.com/errata/RHSA-2026:42146 
                        │      │                  ├ [70] : https://access.redhat.com/errata/RHSA-2026:42150 
                        │      │                  ├ [71] : https://access.redhat.com/errata/RHSA-2026:42151 
                        │      │                  ├ [72] : https://access.redhat.com/errata/RHSA-2026:42240 
                        │      │                  ├ [73] : https://access.redhat.com/errata/RHSA-2026:42644 
                        │      │                  ├ [74] : https://access.redhat.com/errata/RHSA-2026:42796 
                        │      │                  ├ [75] : https://access.redhat.com/errata/RHSA-2026:42852 
                        │      │                  ├ [76] : https://access.redhat.com/errata/RHSA-2026:43038 
                        │      │                  ├ [77] : https://access.redhat.com/errata/RHSA-2026:43052 
                        │      │                  ├ [78] : https://access.redhat.com/errata/RHSA-2026:43692 
                        │      │                  ├ [79] : https://access.redhat.com/errata/RHSA-2026:44622 
                        │      │                  ├ [80] : https://access.redhat.com/errata/RHSA-2026:44624 
                        │      │                  ├ [81] : https://access.redhat.com/errata/RHSA-2026:46395 
                        │      │                  ├ [82] : https://access.redhat.com/errata/RHSA-2026:47149 
                        │      │                  ├ [83] : https://access.redhat.com/errata/RHSA-2026:47735 
                        │      │                  ├ [84] : https://access.redhat.com/errata/RHSA-2026:47737 
                        │      │                  ├ [85] : https://access.redhat.com/errata/RHSA-2026:47952 
                        │      │                  ├ [86] : https://access.redhat.com/errata/RHSA-2026:50300 
                        │      │                  ├ [87] : https://access.redhat.com/errata/RHSA-2026:50843 
                        │      │                  ├ [88] : https://access.redhat.com/errata/RHSA-2026:51033 
                        │      │                  ├ [89] : https://access.redhat.com/errata/RHSA-2026:51112 
                        │      │                  ├ [90] : https://access.redhat.com/errata/RHSA-2026:51187 
                        │      │                  ├ [91] : https://access.redhat.com/errata/RHSA-2026:51194 
                        │      │                  ├ [92] : https://access.redhat.com/errata/RHSA-2026:51341 
                        │      │                  ├ [93] : https://access.redhat.com/errata/RHSA-2026:52826 
                        │      │                  ├ [94] : https://access.redhat.com/errata/RHSA-2026:53374 
                        │      │                  ├ [95] : https://access.redhat.com/errata/RHSA-2026:53412 
                        │      │                  ├ [96] : https://access.redhat.com/errata/RHSA-2026:53413 
                        │      │                  ├ [97] : https://access.redhat.com/errata/RHSA-2026:53415 
                        │      │                  ├ [98] : https://access.redhat.com/errata/RHSA-2026:53530 
                        │      │                  ├ [99] : https://access.redhat.com/errata/RHSA-2026:54191 
                        │      │                  ├ [100]: https://access.redhat.com/errata/RHSA-2026:54274 
                        │      │                  ├ [101]: https://access.redhat.com/errata/RHSA-2026:54283 
                        │      │                  ├ [102]: https://access.redhat.com/errata/RHSA-2026:54284 
                        │      │                  ├ [103]: https://access.redhat.com/errata/RHSA-2026:54285 
                        │      │                  ├ [104]: https://access.redhat.com/errata/RHSA-2026:54286 
                        │      │                  ├ [105]: https://access.redhat.com/errata/RHSA-2026:54287 
                        │      │                  ├ [106]: https://access.redhat.com/errata/RHSA-2026:54395 
                        │      │                  ├ [107]: https://access.redhat.com/errata/RHSA-2026:54401 
                        │      │                  ├ [108]: https://access.redhat.com/errata/RHSA-2026:54435 
                        │      │                  ├ [109]: https://access.redhat.com/errata/RHSA-2026:54441 
                        │      │                  ├ [110]: https://access.redhat.com/security/cve/CVE-2026-39821 
                        │      │                  ├ [111]: https://bugzilla.redhat.com/2480756 
                        │      │                  ├ [112]: https://bugzilla.redhat.com/show_bug.cgi?id=2480756 
                        │      │                  ├ [113]: https://bugzilla.redhat.com/show_bug.cgi?id=2498152 
                        │      │                  ├ [114]: https://creativecommons.org/licenses/by/4.0/ 
                        │      │                  ├ [115]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
                        │      │                  │        026-39821 
                        │      │                  ├ [116]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2
                        │      │                  │        026-39822 
                        │      │                  ├ [117]: https://errata.almalinux.org/9/ALSA-2026-37435.html 
                        │      │                  ├ [118]: https://errata.rockylinux.org/RLSA-2026:37435 
                        │      │                  ├ [119]: https://github.com/golang/go/issues/78760 
                        │      │                  ├ [120]: https://go.dev/cl/767220 
                        │      │                  ├ [121]: https://go.dev/issue/78760 
                        │      │                  ├ [122]: https://groups.google.com/g/golang-announce/c/94pEor
                        │      │                  │        npRlI 
                        │      │                  ├ [123]: https://groups.google.com/g/golang-announce/c/iI-mYS
                        │      │                  │        I0lu8 
                        │      │                  ├ [124]: https://linux.oracle.com/cve/CVE-2026-39821.html 
                        │      │                  ├ [125]: https://linux.oracle.com/errata/ELSA-2026-46395.html 
                        │      │                  ├ [126]: https://nvd.nist.gov/vuln/detail/CVE-2026-39821 
                        │      │                  ├ [127]: https://pkg.go.dev/vuln/GO-2026-5026 
                        │      │                  ├ [128]: https://security.access.redhat.com/data/csaf/v2/vex/
                        │      │                  │        2026/cve-2026-39821.json 
                        │      │                  ├ [129]: https://ubuntu.com/security/notices/USN-8416-1 
                        │      │                  ╰ [130]: https://www.cve.org/CVERecord?id=CVE-2026-39821 
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.41Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:19.973Z 
                        ├ [12] ╭ VulnerabilityID : CVE-2026-39822 
                        │      ├ VendorIDs        ─ [0]: GO-2026-4970 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.12, 1.26.5, 1.27.0-rc.2 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39822 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:5f17df9ccd78b19e87f53f3718a0586e1c6b9384126dc4adc3ab9
                        │      │                   b8b0cd3dec0 
                        │      ├ Title           : golang: Go os.Root: Symlink following vulnerability allows
                        │      │                   directory traversal 
                        │      ├ Description     : On Unix systems, opening a file in an os.Root improperly
                        │      │                   follows symlinks to locations outside of the Root when the
                        │      │                   final path component of the a path is a symbolic link and
                        │      │                   the path ends in /. For example, 'root.Open("symlink/")'
                        │      │                   will open "symlink" even when "symlink" is a symbolic link
                        │      │                   pointing outside of the root. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-61 
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 2 
                        │      │                  ├ azure      : 3 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:
                        │      │                  │         │           H/A:H 
                        │      │                  │         ╰ V3Score : 7.8 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:
                        │      │                            │           H/A:H 
                        │      │                            ╰ V3Score : 7.8 
                        │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:38878 
                        │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-39822 
                        │      │                  ├ [2] : https://bugzilla.redhat.com/2498152 
                        │      │                  ├ [3] : https://bugzilla.redhat.com/show_bug.cgi?id=2498152 
                        │      │                  ├ [4] : https://creativecommons.org/licenses/by/4.0/ 
                        │      │                  ├ [5] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
                        │      │                  │       26-39822 
                        │      │                  ├ [6] : https://errata.almalinux.org/9/ALSA-2026-38878.html 
                        │      │                  ├ [7] : https://errata.rockylinux.org/RLSA-2026:38878 
                        │      │                  ├ [8] : https://go.dev/cl/797880 
                        │      │                  ├ [9] : https://go.dev/issue/79005 
                        │      │                  ├ [10]: https://groups.google.com/g/golang-announce/c/OrmQE_Y
                        │      │                  │       p5Sc 
                        │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-39822.html 
                        │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-38995.html 
                        │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-39822 
                        │      │                  ├ [14]: https://pkg.go.dev/vuln/GO-2026-4970 
                        │      │                  ╰ [15]: https://www.cve.org/CVERecord?id=CVE-2026-39822 
                        │      ├ PublishedDate   : 2026-07-08T17:17:21.31Z 
                        │      ╰ LastModifiedDate: 2026-07-13T14:54:26.317Z 
                        ├ [13] ╭ VulnerabilityID : CVE-2026-46600 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5942 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46600 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:d7062c7574aecd15ebe393d02932e3f6af47f392b8584e5828e62
                        │      │                   ea75928cf74 
                        │      ├ Title           : golang.org/x/net/dns/dnsmessage:
                        │      │                   golang.org/x/net/dns/dnsmessage: Denial of Service via
                        │      │                   invalid DNS record parsing 
                        │      ├ Description     : Parsing an invalid SVCB or HTTPS RR can panic when the size
                        │      │                   of a parameter value overflows the message buffer. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs           ─ [0]: CWE-125 
                        │      ├ VendorSeverity   ─ redhat: 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
                        │      │                           │           /A:H 
                        │      │                           ╰ V3Score : 7.5 
                        │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-46600 
                        │      │                  ├ [1]: https://go.dev/cl/786345 
                        │      │                  ├ [2]: https://go.dev/issue/79795 
                        │      │                  ├ [3]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-46600 
                        │      │                  ├ [5]: https://pkg.go.dev/vuln/GO-2026-5942 
                        │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-46600 
                        │      ├ PublishedDate   : 2026-07-21T20:17:01.213Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:21.913Z 
                        ├ [14] ╭ VulnerabilityID : CVE-2026-42505 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5856 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.12, 1.26.5, 1.27.0-rc.2 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42505 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:2bc8b95ffe8d7b3e8018edbe5e271dca1c30daffb986437ddb5a7
                        │      │                   1b51b682e7a 
                        │      ├ Title           : crypto/tls: golang: Go crypto/tls: Information disclosure in
                        │      │                    Encrypted Client Hello 
                        │      ├ Description     : Handshakes which used Encrypted Client Hello could be
                        │      │                   de-anonymized by a passive network observer due to a
                        │      │                   disclosure of pre-shared key identities in the unencrypted
                        │      │                   client hello. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs           ─ [0]: CWE-201 
                        │      ├ VendorSeverity   ╭ alma   : 3 
                        │      │                  ├ amazon : 2 
                        │      │                  ├ azure  : 2 
                        │      │                  ├ bitnami: 2 
                        │      │                  ├ photon : 2 
                        │      │                  ╰ redhat : 2 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:
                        │      │                  │         │           N/A:N 
                        │      │                  │         ╰ V3Score : 5.3 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:
                        │      │                            │           N/A:N 
                        │      │                            ╰ V3Score : 5.3 
                        │      ├ References       ╭ [0]: https://access.redhat.com/errata/RHSA-2026:37435 
                        │      │                  ├ [1]: https://access.redhat.com/security/cve/CVE-2026-42505 
                        │      │                  ├ [2]: https://bugzilla.redhat.com/2480756 
                        │      │                  ├ [3]: https://errata.almalinux.org/9/ALSA-2026-37435.html 
                        │      │                  ├ [4]: https://go.dev/cl/775960 
                        │      │                  ├ [5]: https://go.dev/issue/79282 
                        │      │                  ├ [6]: https://groups.google.com/g/golang-announce/c/OrmQE_Yp
                        │      │                  │      5Sc 
                        │      │                  ├ [7]: https://nvd.nist.gov/vuln/detail/CVE-2026-42505 
                        │      │                  ├ [8]: https://pkg.go.dev/vuln/GO-2026-5856 
                        │      │                  ╰ [9]: https://www.cve.org/CVERecord?id=CVE-2026-42505 
                        │      ├ PublishedDate   : 2026-07-08T17:17:21.497Z 
                        │      ╰ LastModifiedDate: 2026-07-13T17:05:36.303Z 
                        ├ [15] ╭ VulnerabilityID : CVE-2026-33818 
                        │      ├ VendorIDs        ─ [0]: GO-2026-5972 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-33818 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:6302de3f16967e3da2d833d09af8345bc279c9ce99ecda51dd99f
                        │      │                   e07a2dc345a 
                        │      ├ Title           : Enforce maximum recursion depth in encoding/asn1 
                        │      ├ Description     : Enforce a recursion limit in Unmarshal to prevent stack
                        │      │                   exhaustion when parsing deeply-nested, recursive
                        │      │                   structures. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ References       ╭ [0]: https://go.dev/cl/814980 
                        │      │                  ├ [1]: https://go.dev/issue/80405 
                        │      │                  ├ [2]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-5972 
                        │      ├ PublishedDate   : 2026-08-13T22:17:19.84Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:19.84Z 
                        ├ [16] ╭ VulnerabilityID : CVE-2026-56853 
                        │      ├ VendorIDs        ─ [0]: GO-2026-6089 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56853 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:c06e2365471169556bb82cf40dfae0dabc8883eeeb70caa13929c
                        │      │                   5b67c4b07b6 
                        │      ├ Title           : Apply ReadHeaderTimeout when doing unencrypted HTTP/2 check
                        │      │                   in net/http 
                        │      ├ Description     : When a server is configured to support unencrypted HTTP/2,
                        │      │                   it reads a few bytes from each new connection to see if they
                        │      │                    contain the HTTP/2 client preface. ReadHeaderTimeout is
                        │      │                   unexpectedly not being applied when doing this. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ References       ╭ [0]: https://go.dev/cl/795540 
                        │      │                  ├ [1]: https://go.dev/issue/80205 
                        │      │                  ├ [2]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-6089 
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.093Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:22.093Z 
                        ├ [17] ╭ VulnerabilityID : CVE-2026-56858 
                        │      ├ VendorIDs        ─ [0]: GO-2026-6091 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56858 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:88b074adcd213e1a241fde9901be22b2a12b6669716d8b221ee32
                        │      │                   269c5704929 
                        │      ├ Title           : Fix Javascript regexp context tracking in html/template 
                        │      ├ Description     : Previously, pathological inputs could close an unescaped '/'
                        │      │                    early, allowing for attack-controlled data to inject
                        │      │                   arbitrary content, potentially leading to XSS. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ References       ╭ [0]: https://go.dev/cl/807100 
                        │      │                  ├ [1]: https://go.dev/issue/80435 
                        │      │                  ├ [2]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-6091 
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.207Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:22.207Z 
                        ├ [18] ╭ VulnerabilityID : CVE-2026-56859 
                        │      ├ VendorIDs        ─ [0]: GO-2026-6088 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56859 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:74dbb9268b1f65e0a7e1bf36f6ef5e8dce7d3376d41827a2e59d0
                        │      │                   04a1cef231a 
                        │      ├ Title           : Add recursion depth guard during decode in encoding/xml 
                        │      ├ Description     : Previously, DecodeElement would reset the depth counter
                        │      │                   causing it to never fire; this could lead to stack
                        │      │                   exhaustion. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ References       ╭ [0]: https://go.dev/cl/803320 
                        │      │                  ├ [1]: https://go.dev/issue/80481 
                        │      │                  ├ [2]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-6088 
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.32Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:22.32Z 
                        ├ [19] ╭ VulnerabilityID : CVE-2026-56860 
                        │      ├ VendorIDs        ─ [0]: GO-2026-6218 
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                        │      │                  │         4724a45c03fe2abddba1 
                        │      │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                        │      │                            28c664cc70b025656e08 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56860 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:50333fdd85518ea3d845b9fb7475122cd761daafadcd6cf82f475
                        │      │                   30853cf60da 
                        │      ├ Title           : Avoid quadratic complexity in resolvePath in net/url 
                        │      ├ Description     : Previously, resolving relative paths containing parent
                        │      │                   directory ('..') segments performed string conversions and
                        │      │                   buffer rewrites on each step, resulting in quadratic time
                        │      │                   complexity and high memory allocation overhead. Now, path
                        │      │                   resolution operates on a byte buffer using index-based
                        │      │                   backtracking for '..' segments, eliminating the quadratic
                        │      │                   time complexity and significantly reducing memory
                        │      │                   allocations. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ References       ╭ [0]: https://go.dev/cl/803681 
                        │      │                  ├ [1]: https://go.dev/issue/80494 
                        │      │                  ├ [2]: https://groups.google.com/g/golang-announce/c/94pEornp
                        │      │                  │      RlI 
                        │      │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-6218 
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.44Z 
                        │      ╰ LastModifiedDate: 2026-08-13T22:17:22.44Z 
                        ╰ [20] ╭ VulnerabilityID : CVE-2026-56862 
                               ├ VendorIDs        ─ [0]: GO-2026-6090 
                               ├ PkgID           : stdlib@v1.26.4 
                               ├ PkgName         : stdlib 
                               ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                               │                  ╰ UID : 364846ec8fe81bdc 
                               ├ InstalledVersion: v1.26.4 
                               ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                               ├ Status          : fixed 
                               ├ Layer            ╭ Digest: sha256:944565cd442ad5f7b393fe914cfa56b8dc12f93cae1c
                               │                  │         4724a45c03fe2abddba1 
                               │                  ╰ DiffID: sha256:f17a4797abfce19f194fa71560706d6600db54ac9610
                               │                            28c664cc70b025656e08 
                               ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56862 
                               ├ DataSource       ╭ ID  : govulndb 
                               │                  ├ Name: The Go Vulnerability Database 
                               │                  ╰ URL : https://pkg.go.dev/vuln/ 
                               ├ Fingerprint     : sha256:6d4c1d69cfec4e7b95d39b76e365c609c70836baa788551c955db
                               │                   7daff0b6782 
                               ├ Title           : Limit handshake messages we are willing to accept
                               │                   post-handshake in crypto/tls 
                               ├ Description     : Handshake messages, such as KeyUpdate, are always considered
                               │                    as state-advancing, regardless of whether a handshake has
                               │                   been completed or not. As a result, a malicious client can
                               │                   keep sending KeyUpdate messages to force the server to keep
                               │                   performing key derivation operations indefinitely. 
                               ├ Severity        : UNKNOWN 
                               ├ References       ╭ [0]: https://go.dev/cl/804261 
                               │                  ├ [1]: https://go.dev/issue/80528 
                               │                  ├ [2]: https://groups.google.com/g/golang-announce/c/94pEornp
                               │                  │      RlI 
                               │                  ╰ [3]: https://pkg.go.dev/vuln/GO-2026-6090 
                               ├ PublishedDate   : 2026-08-13T22:17:22.55Z 
                               ╰ LastModifiedDate: 2026-08-13T22:17:22.55Z 
```
