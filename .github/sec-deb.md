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
│                       │      │                  ╰ UID : f5fbbf9aa30bf0e2 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0c7d5944e0132bfea736e96d1f3bbe41de317e23a3e1f946ab7b8
│                       │      │                   f39143e8a0f 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [1]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : bsdextrautils@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdextrautils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdextrautils@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : f5fbbf9aa30bf0e2 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c163b51e50f13deb972907e342884c25d70cdb879388c960944d4
│                       │      │                   87a7c73cc23 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [2]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 411fc06346b75c80 
│                       │      ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:70233bfe7ef0ef258728ee0487a9406ff9170b474798d77975c6d
│                       │      │                   43d03d44229 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [3]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : bsdutils@1:2.41-4ubuntu4.2 
│                       │      ├ PkgName         : bsdutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/bsdutils@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 411fc06346b75c80 
│                       │      ├ InstalledVersion: 1:2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4efc2791556826666aa05613c8bbd0039fc6459cab98598e8f62b
│                       │      │                   ddd33a48005 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [4]  ╭ VulnerabilityID : CVE-2026-10536 
│                       │      ├ PkgID           : curl@8.14.1-2ubuntu1.4 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.4?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-25.10 
│                       │      │                  ╰ UID : 27d0b7e1b0440923 
│                       │      ├ InstalledVersion: 8.14.1-2ubuntu1.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-10536 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ec09a242048e7d9e4bf10559fe4a03ab575d0c82aad77dbdd2730
│                       │      │                   65bc8527e9d 
│                       │      ├ Title           : libcurl: libcurl: Use-after-free vulnerability leading to
│                       │      │                   Denial of Service 
│                       │      ├ Description     : A use-after-free vulnerability exists in libcurl when an
│                       │      │                   application
│                       │      │                   configures an HTTP/2 stream-dependency tree via
│                       │      │                   `CURLOPT_STREAM_DEPENDS` or
│                       │      │                   `CURLOPT_STREAM_DEPENDS_E`, subsequently invokes
│                       │      │                   `curl_easy_reset()`, and
│                       │      │                   finally terminates the handle with `curl_easy_cleanup()`.
│                       │      │                   During this final
│                       │      │                   cleanup phase, libcurl attempts to access and modify an
│                       │      │                   internal structure
│                       │      │                   that was already freed during the reset operation. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-416 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-10536 
│                       │      │                  ├ [1]: https://curl.se/L7HzKXisfJ/CVE-2026-10536.md 
│                       │      │                  ├ [2]: https://curl.se/docs/CVE-2026-10536.html 
│                       │      │                  ├ [3]: https://curl.se/docs/CVE-2026-10536.json 
│                       │      │                  ├ [4]: https://hackerone.com/reports/3751697 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-10536 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-10536 
│                       │      ├ PublishedDate   : 2026-07-03T07:16:23.563Z 
│                       │      ╰ LastModifiedDate: 2026-07-07T18:02:03.89Z 
│                       ├ [5]  ╭ VulnerabilityID : CVE-2026-12064 
│                       │      ├ PkgID           : curl@8.14.1-2ubuntu1.4 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.14.1-2ubuntu1.4?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-25.10 
│                       │      │                  ╰ UID : 27d0b7e1b0440923 
│                       │      ├ InstalledVersion: 8.14.1-2ubuntu1.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-12064 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d67ab29bffceff4ed18395d492ac30d645f22ba4717c5447a412a
│                       │      │                   55bb880782a 
│                       │      ├ Title           : curl: curl: SSH host verification bypass when using
│                       │      │                   schemeless URLs with SFTP/SCP 
│                       │      ├ Description     : When a user invokes curl using a schemeless URL combined
│                       │      │                   with
│                       │      │                   `--proto-default` sftp (or scp), a disconnect occurs between
│                       │      │                    the tool layer
│                       │      │                   and libcurl. The tool layer incorrectly infers the URL
│                       │      │                   scheme, which
│                       │      │                   erroneously bypasses the initialization of critical SSH
│                       │      │                   security options like
│                       │      │                   CURLOPT_SSH_HOST_PUBLIC_KEY_SHA256 and
│                       │      │                   CURLOPT_SSH_KNOWNHOSTS. Conversely, the
│                       │      │                   libcurl runtime successfully honors CURLOPT_DEFAULT_PROTOCOL
│                       │      │                    and establishes
│                       │      │                   the connection via SFTP/SCP as specified. Because the tool
│                       │      │                   layer skipped the
│                       │      │                   security configuration, these SSH host verification options
│                       │      │                   are silently
│                       │      │                   omitted, causing curl to connect to an unverified SSH remote
│                       │      │                    host without
│                       │      │                   throwing an error. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-295 
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:H
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 7.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-12064 
│                       │      │                  ├ [1]: https://curl.se/L7HzKXisfJ/CVE-2026-12064.md 
│                       │      │                  ├ [2]: https://curl.se/docs/CVE-2026-12064.html 
│                       │      │                  ├ [3]: https://curl.se/docs/CVE-2026-12064.json 
│                       │      │                  ├ [4]: https://hackerone.com/reports/3797526 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-12064 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-12064 
│                       │      ├ PublishedDate   : 2026-07-03T07:16:24.217Z 
│                       │      ╰ LastModifiedDate: 2026-07-07T19:43:11.187Z 
│                       ├ [6]  ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libblkid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : ddaca4141760dfcf 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1b097d15017a22f0a3a04599163bc8ad7e55c9ac9a4a27805bedd
│                       │      │                   0508757f310 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [7]  ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libblkid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libblkid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libblkid1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : ddaca4141760dfcf 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:815657a16aa234896e9cc6cbdb3ad06cbef9e1e3149cd01bd3c9c
│                       │      │                   fe9abe234c9 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [8]  ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:41d3232ef603c13691f92de12de47c68872fb750c845bdf159f79
│                       │      │                   285a64ab06c 
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
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [8] : https://errata.rockylinux.org/RLSA-2026:20594 
│                       │      │                  ├ [9] : https://inbox.sourceware.org/libc-announce/76814edf-c
│                       │      │                  │       f7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │      │                  ├ [10]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │      │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │      │                  ├ [13]: https://packages.fedoraproject.org/pkgs/glibc/glibc-g
│                       │      │                  │       conv-extra/ 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │      │                  ├ [15]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007 
│                       │      │                  ├ [16]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │      │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │      ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:55:54.12Z 
│                       ├ [9]  ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fa944e07486703bb77360a74286fb8b3dfd19e61e9129b2fc4930
│                       │      │                   e4c4dd3aadf 
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
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:19061 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-4437.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │      │                  ├ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │      │                  ╰ [16]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:56:34.227Z 
│                       ├ [10] ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:83192912fdaa153be6e467ccf1abea88d548d261b9088c791e027
│                       │      │                   7966e00b192 
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
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:19061 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-4438.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │      │                  ├ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │      │                  ╰ [16]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:56:34.367Z 
│                       ├ [11] ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cfbe4e782c6cc5c187c9a8813816cc9ab62bb0f3c04e3d02516ac
│                       │      │                   2cf69743a6e 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:59:01.13Z 
│                       ├ [12] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : libc-bin@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.42-0ubuntu3.1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 32f722fad25bcb3d 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fcea715327540f71d36e1d5ad27a8e93d64cc653b2067e95584e4
│                       │      │                   078f7396bc2 
│                       │      ├ Title           : glibc: glibc: Application crash or uninitialized memory read
│                       │      │                    via crafted DNS response 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.0.1 to version 2.43
│                       │      │                    fail to validate the RDATA content against the RDATA length
│                       │      │                    in a DNS response when processing A6, CERT, LOC, TKEY or
│                       │      │                   TSIG records, which may allow an attacker to craft a DNS
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
│                       │      ╰ LastModifiedDate: 2026-06-19T21:17:02.62Z 
│                       ├ [13] ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1730cef5ca45168ee1a788fea8589a4631a460727f3c80ab6ccec
│                       │      │                   3ceedd698bd 
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
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [8] : https://errata.rockylinux.org/RLSA-2026:20594 
│                       │      │                  ├ [9] : https://inbox.sourceware.org/libc-announce/76814edf-c
│                       │      │                  │       f7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │      │                  ├ [10]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │      │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │      │                  ├ [13]: https://packages.fedoraproject.org/pkgs/glibc/glibc-g
│                       │      │                  │       conv-extra/ 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │      │                  ├ [15]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007 
│                       │      │                  ├ [16]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │      │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │      ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:55:54.12Z 
│                       ├ [14] ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f413d54e34ef1df8acc2afd09217608901d426f509ba860ea9c8b
│                       │      │                   2837080a4d7 
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
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:19061 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-4437.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │      │                  ├ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │      │                  ╰ [16]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:56:34.227Z 
│                       ├ [15] ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:826d8acda7bf78480da26b6c0736ad6b1ccd6092311bd3345e50e
│                       │      │                   1f62486f304 
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
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:19061 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-4438.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │      │                  ├ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │      │                  ╰ [16]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:56:34.367Z 
│                       ├ [16] ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0f21172f39d4befedcd6e68f3e1b42f532caaf3c8aafa7e5635a6
│                       │      │                   446aa1f81b8 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:59:01.13Z 
│                       ├ [17] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : libc6@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.42-0ubuntu3.1?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 67fff5c1ddc17a00 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:97ec8e7159672b2ccea1c2375c8b2384d932ca67373bfd10ee616
│                       │      │                   5a8b8c91e9f 
│                       │      ├ Title           : glibc: glibc: Application crash or uninitialized memory read
│                       │      │                    via crafted DNS response 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.0.1 to version 2.43
│                       │      │                    fail to validate the RDATA content against the RDATA length
│                       │      │                    in a DNS response when processing A6, CERT, LOC, TKEY or
│                       │      │                   TSIG records, which may allow an attacker to craft a DNS
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
│                       │      ╰ LastModifiedDate: 2026-06-19T21:17:02.62Z 
│                       ├ [18] ╭ VulnerabilityID : CVE-2026-10536 
│                       │      ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.4 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.4?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 6ab805c4470c83a5 
│                       │      ├ InstalledVersion: 8.14.1-2ubuntu1.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-10536 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8152da2e8e036c0b88f4a42e0456c91730f6df96eb79838207b82
│                       │      │                   8de2b0ee1ae 
│                       │      ├ Title           : libcurl: libcurl: Use-after-free vulnerability leading to
│                       │      │                   Denial of Service 
│                       │      ├ Description     : A use-after-free vulnerability exists in libcurl when an
│                       │      │                   application
│                       │      │                   configures an HTTP/2 stream-dependency tree via
│                       │      │                   `CURLOPT_STREAM_DEPENDS` or
│                       │      │                   `CURLOPT_STREAM_DEPENDS_E`, subsequently invokes
│                       │      │                   `curl_easy_reset()`, and
│                       │      │                   finally terminates the handle with `curl_easy_cleanup()`.
│                       │      │                   During this final
│                       │      │                   cleanup phase, libcurl attempts to access and modify an
│                       │      │                   internal structure
│                       │      │                   that was already freed during the reset operation. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-416 
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 4.7 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-10536 
│                       │      │                  ├ [1]: https://curl.se/L7HzKXisfJ/CVE-2026-10536.md 
│                       │      │                  ├ [2]: https://curl.se/docs/CVE-2026-10536.html 
│                       │      │                  ├ [3]: https://curl.se/docs/CVE-2026-10536.json 
│                       │      │                  ├ [4]: https://hackerone.com/reports/3751697 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-10536 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-10536 
│                       │      ├ PublishedDate   : 2026-07-03T07:16:23.563Z 
│                       │      ╰ LastModifiedDate: 2026-07-07T18:02:03.89Z 
│                       ├ [19] ╭ VulnerabilityID : CVE-2026-12064 
│                       │      ├ PkgID           : libcurl4t64@8.14.1-2ubuntu1.4 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.14.1-2ubuntu1.4?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 6ab805c4470c83a5 
│                       │      ├ InstalledVersion: 8.14.1-2ubuntu1.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-12064 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:924de4d0e9acc7a0523bca9fc1c57661a4dbf644f7885a34b6178
│                       │      │                   4771cd923c9 
│                       │      ├ Title           : curl: curl: SSH host verification bypass when using
│                       │      │                   schemeless URLs with SFTP/SCP 
│                       │      ├ Description     : When a user invokes curl using a schemeless URL combined
│                       │      │                   with
│                       │      │                   `--proto-default` sftp (or scp), a disconnect occurs between
│                       │      │                    the tool layer
│                       │      │                   and libcurl. The tool layer incorrectly infers the URL
│                       │      │                   scheme, which
│                       │      │                   erroneously bypasses the initialization of critical SSH
│                       │      │                   security options like
│                       │      │                   CURLOPT_SSH_HOST_PUBLIC_KEY_SHA256 and
│                       │      │                   CURLOPT_SSH_KNOWNHOSTS. Conversely, the
│                       │      │                   libcurl runtime successfully honors CURLOPT_DEFAULT_PROTOCOL
│                       │      │                    and establishes
│                       │      │                   the connection via SFTP/SCP as specified. Because the tool
│                       │      │                   layer skipped the
│                       │      │                   security configuration, these SSH host verification options
│                       │      │                   are silently
│                       │      │                   omitted, causing curl to connect to an unverified SSH remote
│                       │      │                    host without
│                       │      │                   throwing an error. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs           ─ [0]: CWE-295 
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:H
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 7.5 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-12064 
│                       │      │                  ├ [1]: https://curl.se/L7HzKXisfJ/CVE-2026-12064.md 
│                       │      │                  ├ [2]: https://curl.se/docs/CVE-2026-12064.html 
│                       │      │                  ├ [3]: https://curl.se/docs/CVE-2026-12064.json 
│                       │      │                  ├ [4]: https://hackerone.com/reports/3797526 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-12064 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-12064 
│                       │      ├ PublishedDate   : 2026-07-03T07:16:24.217Z 
│                       │      ╰ LastModifiedDate: 2026-07-07T19:43:11.187Z 
│                       ├ [20] ╭ VulnerabilityID : CVE-2025-66382 
│                       │      ├ PkgID           : libexpat1@2.7.1-2ubuntu0.2 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.1-2ubuntu0.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : bb3ed74d0fd332c6 
│                       │      ├ InstalledVersion: 2.7.1-2ubuntu0.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6e400dbfad3c4d3b39bac61649c9b73a3d3a2c6725b833afcf296
│                       │      │                   325aaf8a858 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T09:56:45.24Z 
│                       ├ [21] ╭ VulnerabilityID : CVE-2024-2236 
│                       │      ├ PkgID           : libgcrypt20@1.11.0-7ubuntu0.1 
│                       │      ├ PkgName         : libgcrypt20 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libgcrypt20@1.11.0-7ubuntu0.1?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 8f3635c00dca0a4f 
│                       │      ├ InstalledVersion: 1.11.0-7ubuntu0.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-2236 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:615a9bc15e4d2676d7318eff948f39cf22a36f69d7dde9157b748
│                       │      │                   006a7377ff1 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T07:24:06.083Z 
│                       ├ [22] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : liblastlog2-2 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 86a2046512fbbaa2 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cd2c39218b3204be6718c9e2c00343b495dcd95f1aa194e4b3e55
│                       │      │                   84be33fdc86 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [23] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : liblastlog2-2@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : liblastlog2-2 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/liblastlog2-2@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 86a2046512fbbaa2 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fcd5d89efee2c65ffad422e5ae3c9a90bccbc84d0a1698c1a0d55
│                       │      │                   68c166f67b7 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [24] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : e278fd35c2ddbe27 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b3a8eda606b737bf0ccda53281dc2dd62d9e3e9d842a5165cbc77
│                       │      │                   d26e708cee2 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [25] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libmount1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libmount1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libmount1@2.41-4ubuntu4.2?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : e278fd35c2ddbe27 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f5ec3cc905cc3e44badc7a3f5b0b6e388db8f7b3e95a4edbb263b
│                       │      │                   73daf4d30ba 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [26] ╭ VulnerabilityID : CVE-2026-13757 
│                       │      ├ PkgID           : libp11-kit0@0.25.5-3ubuntu1 
│                       │      ├ PkgName         : libp11-kit0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libp11-kit0@0.25.5-3ubuntu1?arch=amd64
│                       │      │                  │       &distro=ubuntu-25.10 
│                       │      │                  ╰ UID : d83476d4246a471f 
│                       │      ├ InstalledVersion: 0.25.5-3ubuntu1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-13757 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:90450b41af8e7e2c3b4d877adad5d974dc37210af49b71f1ae49d
│                       │      │                   9702225b349 
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
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.2 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-13757 
│                       │      │                  ├ [1]: https://bugzilla.redhat.com/show_bug.cgi?id=2494556 
│                       │      │                  ├ [2]: https://nvd.nist.gov/vuln/detail/CVE-2026-13757 
│                       │      │                  ╰ [3]: https://www.cve.org/CVERecord?id=CVE-2026-13757 
│                       │      ├ PublishedDate   : 2026-06-29T19:16:40.907Z 
│                       │      ╰ LastModifiedDate: 2026-07-08T03:34:36.15Z 
│                       ├ [27] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13@3.13.7-1ubuntu0.4?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : d39243325c040cfa 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b8a5363e1f6de3a6d000b5de48eb83b3737559b3167b800cb5189
│                       │      │                   16492aa1108 
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
│                       │      │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19064 
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
│                       │      │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-19177.html 
│                       │      │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ├ [51]: https://ubuntu.com/security/notices/USN-8509-1 
│                       │      │                  ╰ [52]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:30:44.59Z 
│                       ├ [28] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13-minimal@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13-minimal 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-minimal@3.13.7-1ubuntu0.
│                       │      │                  │       4?arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 9682446bb647ab44 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a5b5ac099d4edf8c53573f63be97cb8443bc90cd669ee6c687e3a
│                       │      │                   169e653e5e9 
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
│                       │      │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19064 
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
│                       │      │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-19177.html 
│                       │      │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ├ [51]: https://ubuntu.com/security/notices/USN-8509-1 
│                       │      │                  ╰ [52]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:30:44.59Z 
│                       ├ [29] ╭ VulnerabilityID : CVE-2026-2297 
│                       │      ├ PkgID           : libpython3.13-stdlib@3.13.7-1ubuntu0.4 
│                       │      ├ PkgName         : libpython3.13-stdlib 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libpython3.13-stdlib@3.13.7-1ubuntu0.4
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23dd0164f1ee89d8 
│                       │      ├ InstalledVersion: 3.13.7-1ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-2297 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4afd8620de5d173c4d7839a144b532e28edd9d07051f4b9a1fcc5
│                       │      │                   8b89fb6aae0 
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
│                       │      │                  ├ [40]: https://errata.rockylinux.org/RLSA-2026:19064 
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
│                       │      │                  ├ [49]: https://linux.oracle.com/errata/ELSA-2026-19177.html 
│                       │      │                  ├ [50]: https://nvd.nist.gov/vuln/detail/CVE-2026-2297 
│                       │      │                  ├ [51]: https://ubuntu.com/security/notices/USN-8509-1 
│                       │      │                  ╰ [52]: https://www.cve.org/CVERecord?id=CVE-2026-2297 
│                       │      ├ PublishedDate   : 2026-03-04T23:16:10.757Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:30:44.59Z 
│                       ├ [30] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f76c9db1dc5759aeb0a806e0ac154cfa6aed4ae118be69ec7f87e
│                       │      │                   529a91d7f5c 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [31] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libsmartcols1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libsmartcols1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsmartcols1@2.41-4ubuntu4.2?arch=amd
│                       │      │                  │       64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 5caf4ed7c33e8ba9 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a828c90abb3bbe458529de9801726a7d2d6009243452409d913e4
│                       │      │                   4d96e5198fc 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [32] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libsystemd0@257.9-0ubuntu2.5 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@257.9-0ubuntu2.5?arch=amd6
│                       │      │                  │       4&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ec55cdfad517f3cc 
│                       │      ├ InstalledVersion: 257.9-0ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a62836df01f216c0f1a6cb18325d6ebc3d7a279cc211ccbfd552b
│                       │      │                   5ff380820c5 
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
│                       ├ [33] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libudev1@257.9-0ubuntu2.5 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@257.9-0ubuntu2.5?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : f211373f8a95c023 
│                       │      ├ InstalledVersion: 257.9-0ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:775eb0fcd12a58be81241871b6ba45a4a71cc9c05d3bc80556334
│                       │      │                   b4ad6263d70 
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
│                       ├ [34] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23db7c315eddf1f4 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4a62bd1e136d19f985938605c1783b5cfb09ce4f3c14ea30097fd
│                       │      │                   282247fc3e5 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [35] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : libuuid1@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : libuuid1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libuuid1@2.41-4ubuntu4.2?arch=amd64&di
│                       │      │                  │       stro=ubuntu-25.10 
│                       │      │                  ╰ UID : 23db7c315eddf1f4 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2cc85ed8aed39a5a4f88a1ba1fca80cf05c9a7cc7b73041832be4
│                       │      │                   93bff4356b1 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [36] ╭ VulnerabilityID : CVE-2026-4046 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:59a7697ac98be3af7cb721f4785305a2802c7aed313a4a0eed45d
│                       │      │                   486c1e1a3e7 
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
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4046 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2453117 
│                       │      │                  ├ [6] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4046 
│                       │      │                  ├ [7] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [8] : https://errata.rockylinux.org/RLSA-2026:20594 
│                       │      │                  ├ [9] : https://inbox.sourceware.org/libc-announce/76814edf-c
│                       │      │                  │       f7f-47ec-979d-2dce0a2c76bf@gotplt.org/T/#u 
│                       │      │                  ├ [10]: https://linux.oracle.com/cve/CVE-2026-4046.html 
│                       │      │                  ├ [11]: https://linux.oracle.com/errata/ELSA-2026-50291.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2026-4046 
│                       │      │                  ├ [13]: https://packages.fedoraproject.org/pkgs/glibc/glibc-g
│                       │      │                  │       conv-extra/ 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=33980 
│                       │      │                  ├ [15]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007 
│                       │      │                  ├ [16]: https://sourceware.org/git/?p=glibc.git;a=blob_plain;
│                       │      │                  │       f=advisories/GLIBC-SA-2026-0007;hb=HEAD 
│                       │      │                  ╰ [17]: https://www.cve.org/CVERecord?id=CVE-2026-4046 
│                       │      ├ PublishedDate   : 2026-03-30T18:16:19.573Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:55:54.12Z 
│                       ├ [37] ╭ VulnerabilityID : CVE-2026-4437 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4437 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d33680a62362abfb1891d97f31c0d62012830b937bc811d1a534e
│                       │      │                   9bfc4f9e046 
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
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4437 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:19061 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-4437.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-4437 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=34014 
│                       │      │                  ├ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4437 
│                       │      │                  ╰ [16]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.477Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:56:34.227Z 
│                       ├ [38] ╭ VulnerabilityID : CVE-2026-4438 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-4438 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f72424c7a61bb7a2a76ca49737a718b8fb1d26f6d367eec546972
│                       │      │                   3a314a44cd3 
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
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2026:20597 
│                       │      │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2026-4438 
│                       │      │                  ├ [2] : https://bugzilla.redhat.com/2449777 
│                       │      │                  ├ [3] : https://bugzilla.redhat.com/2449783 
│                       │      │                  ├ [4] : https://bugzilla.redhat.com/2453117 
│                       │      │                  ├ [5] : https://bugzilla.redhat.com/show_bug.cgi?id=2449777 
│                       │      │                  ├ [6] : https://bugzilla.redhat.com/show_bug.cgi?id=2449783 
│                       │      │                  ├ [7] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4437 
│                       │      │                  ├ [8] : https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-20
│                       │      │                  │       26-4438 
│                       │      │                  ├ [9] : https://errata.almalinux.org/9/ALSA-2026-20597.html 
│                       │      │                  ├ [10]: https://errata.rockylinux.org/RLSA-2026:19061 
│                       │      │                  ├ [11]: https://linux.oracle.com/cve/CVE-2026-4438.html 
│                       │      │                  ├ [12]: https://linux.oracle.com/errata/ELSA-2026-20597.html 
│                       │      │                  ├ [13]: https://nvd.nist.gov/vuln/detail/CVE-2026-4438 
│                       │      │                  ├ [14]: https://sourceware.org/bugzilla/show_bug.cgi?id=34015 
│                       │      │                  ├ [15]: https://www.cve.org/CVERecord?id=CVE-2026-4438 
│                       │      │                  ╰ [16]: https://www.openwall.com/lists/oss-security/2026/03/2
│                       │      │                          3/2 
│                       │      ├ PublishedDate   : 2026-03-20T20:16:49.623Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:56:34.367Z 
│                       ├ [39] ╭ VulnerabilityID : CVE-2026-5435 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-5435 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d73feae2e27ee51cbaf70a77406067769476ffba6bf62343556f5
│                       │      │                   8068212abd2 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:59:01.13Z 
│                       ├ [40] ╭ VulnerabilityID : CVE-2026-6238 
│                       │      ├ PkgID           : locales@2.42-0ubuntu3.1 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.42-0ubuntu3.1?arch=all&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : 217c1ce65d47a6c2 
│                       │      ├ InstalledVersion: 2.42-0ubuntu3.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-6238 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fd5c7aa8afcaac31ed97248d0a4de75db9ec6f1f764ae003f40e4
│                       │      │                   834e7d42827 
│                       │      ├ Title           : glibc: glibc: Application crash or uninitialized memory read
│                       │      │                    via crafted DNS response 
│                       │      ├ Description     : The deprecated functions ns_printrrf, ns_printrr and
│                       │      │                   fp_nquery in the GNU C Library version 2.0.1 to version 2.43
│                       │      │                    fail to validate the RDATA content against the RDATA length
│                       │      │                    in a DNS response when processing A6, CERT, LOC, TKEY or
│                       │      │                   TSIG records, which may allow an attacker to craft a DNS
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
│                       │      ╰ LastModifiedDate: 2026-06-19T21:17:02.62Z 
│                       ├ [41] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3b09ccc5fd80337859761c93ca816a48967e6339ce0499f6803e6
│                       │      │                   b57db8f8c19 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [42] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : login@1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ PkgName         : login 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login@4.16.0-2%2Breally2.41-4ubuntu4.2
│                       │      │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 7a0cd09a7bc5697e 
│                       │      ├ InstalledVersion: 1:4.16.0-2+really2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b895b8d2a68f699aab89c4e014967bb7bbae0c7249f9d09597c0e
│                       │      │                   336a5077a45 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [43] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : login.defs@1:4.17.4-2ubuntu2 
│                       │      ├ PkgName         : login.defs 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu2?arch=all&di
│                       │      │                  │       stro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 685157e74dbd875c 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:dfb300578acddb407a6589cf48cd6d00b029cb5bce716b75417aa
│                       │      │                   058c97bf657 
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
│                       │      │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20145 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [44] ╭ VulnerabilityID : CVE-2026-10037 
│                       │      ├ PkgID           : mailcap@3.74ubuntu1 
│                       │      ├ PkgName         : mailcap 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mailcap@3.74ubuntu1?arch=all&distro=ub
│                       │      │                  │       untu-25.10 
│                       │      │                  ╰ UID : 2ccd10cbf4e0f3ac 
│                       │      ├ InstalledVersion: 3.74ubuntu1 
│                       │      ├ FixedVersion    : 3.74ubuntu1.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-10037 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d044e9aedb2a751f57efd23562f9a4f85062c4de0d91171fcfbfd
│                       │      │                   2423c68197d 
│                       │      ├ Description     : A sandbox escape vulnerability exists in the OpenJDK
│                       │      │                   packages provided in Ubuntu. The .jar MIME handlers
│                       │      │                   installed by these packages execute files marked as
│                       │      │                   executable when the mailcap package is installed. A
│                       │      │                   compromised or malicious sandboxed application with access
│                       │      │                   to the OpenURI portal via xdg-desktop-portal-gtk can write a
│                       │      │                    malicious .jar file to the host file system, set its
│                       │      │                   executable bit, and trigger the handler to execute arbitrary
│                       │      │                    code outside of the sandbox environment. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-20 
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://bugs.launchpad.net/ubuntu/+source/openjdk-25/+
│                       │      │                  │      bug/2153100 
│                       │      │                  ├ [1]: https://ubuntu.com/security/notices/USN-8518-1 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-10037 
│                       │      ├ PublishedDate   : 2026-07-08T22:17:12.5Z 
│                       │      ╰ LastModifiedDate: 2026-07-08T22:17:12.5Z 
│                       ├ [45] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : f2821a9fde7aa805 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9e61a887390f7ee7bc2ede1f9ccedf6006bb8e61bbc7686a77e60
│                       │      │                   1bdf90a2832 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [46] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : mount@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : mount 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/mount@2.41-4ubuntu4.2?arch=amd64&distr
│                       │      │                  │       o=ubuntu-25.10 
│                       │      │                  ╰ UID : f2821a9fde7aa805 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:de5d8c3ec41b1ac2a46f7212c39aba218e24e9a9d2c195bac9c64
│                       │      │                   579ed0fff20 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [47] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : passwd@1:4.17.4-2ubuntu2 
│                       │      ├ PkgName         : passwd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu2?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-25.10&epoch=1 
│                       │      │                  ╰ UID : 2d87ef360f209a3f 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:006302474c563c60d2eb05ddfa85edcffa51687ffe502194359fd
│                       │      │                   5bd09ed0168 
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
│                       │      │                  ├ [6] : https://errata.rockylinux.org/RLSA-2025:20145 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [48] ╭ VulnerabilityID : CVE-2026-35338 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35338 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:56898554c40768e640fa39847b4636a38703b6a74b9bb7e933b92
│                       │      │                   d4f36175c55 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-4c7q-4928-8445 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35338 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35338 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:35.583Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.177Z 
│                       ├ [49] ╭ VulnerabilityID : CVE-2026-35339 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35339 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e0236da0a15bd4e371759b3c5ea922187d2d25b7c4347661c2baa
│                       │      │                   fa6e513a7a4 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-4x34-chg5-mwjj 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35339 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35339 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:35.767Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.29Z 
│                       ├ [50] ╭ VulnerabilityID : CVE-2026-35340 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35340 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:922ba4afe862bcb3e6cbe782014931a6f69f34187cac1eedc7125
│                       │      │                   3671d3e9e76 
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
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References       ╭ [0]: https://github.com/uutils/coreutils/pull/10035 
│                       │      │                  ├ [1]: https://github.com/uutils/coreutils/releases/tag/0.6.0 
│                       │      │                  ╰ [2]: https://www.cve.org/CVERecord?id=CVE-2026-35340 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:35.923Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.393Z 
│                       ├ [51] ╭ VulnerabilityID : CVE-2026-35341 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3f78b16f130e206e9387ec074f8407e1d9ea71d92ae8992fad202
│                       │      │                   3b2c1a9ae9d 
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
│                       ├ [52] ╭ VulnerabilityID : CVE-2026-35342 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35342 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ff3ef72a1801d2baf5ce783cc4a6727a5925e3041c8d529355554
│                       │      │                   78e232429aa 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-2w8r-9xj7-69j5 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35342 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35342 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.217Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.61Z 
│                       ├ [53] ╭ VulnerabilityID : CVE-2026-35343 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35343 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7905685bf766f9416964998eb367ec95c0aa153f444b74a672bea
│                       │      │                   fd02ca51fdd 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-wv33-5pxh-r7j7 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35343 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35343 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.357Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.723Z 
│                       ├ [54] ╭ VulnerabilityID : CVE-2026-35344 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:331197c026cb8430f089e9406d6fbcf86fb6b88fe007d6d2a4556
│                       │      │                   a552aa98785 
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
│                       ├ [55] ╭ VulnerabilityID : CVE-2026-35345 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:71b0e93e3df66a2da56eb3825515b36ede4dd17330740e28d4365
│                       │      │                   e67ba404de6 
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
│                       ├ [56] ╭ VulnerabilityID : CVE-2026-35346 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35346 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2c234b015285b907e3d116faeb298f932aa2e58a46ea0e13e872a
│                       │      │                   69fd35e2d69 
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
│                       │      │                  ├ [5]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-6gcw-w7cp-94g9 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-35346 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-35346 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.76Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.057Z 
│                       ├ [57] ╭ VulnerabilityID : CVE-2026-35347 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35347 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9b2f16bcca9e1cc96f8d52ba56d0d8177131a3ed361bb80060bef
│                       │      │                   e6fcf52679a 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-3wfc-mgpm-9rq6 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35347 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35347 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.903Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.167Z 
│                       ├ [58] ╭ VulnerabilityID : CVE-2026-35348 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c1aa64ca2b8811091de4334ffd406c44e251fddd2170f2daf76a1
│                       │      │                   784462c6c90 
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
│                       ├ [59] ╭ VulnerabilityID : CVE-2026-35349 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35349 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:32ecabb1e3bffd1464d62805fb3b3e0a05cb632413bf65e4e0a4f
│                       │      │                   8fbb7d225c5 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-7cr3-h577-g38j 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35349 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35349 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.19Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.377Z 
│                       ├ [60] ╭ VulnerabilityID : CVE-2026-35350 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fecabfb26d85703bb466b1009cb09081e938e6064b8918f43c9aa
│                       │      │                   3e0bd57c141 
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
│                       ├ [61] ╭ VulnerabilityID : CVE-2026-35351 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5493ee199f938d12980ace04d680a92359e3664b10ee18a88cf15
│                       │      │                   bcb1a69db58 
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
│                       ├ [62] ╭ VulnerabilityID : CVE-2026-35352 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:60c740ea330a2ced7edeaa7743a50af43af28fbebc71659643f27
│                       │      │                   bc6678eb36f 
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
│                       ├ [63] ╭ VulnerabilityID : CVE-2026-35353 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35353 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9cc53f277d4372ee19f572db351153335d328da6840ef1e84b901
│                       │      │                   0d941d4627a 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-mj6p-44ch-cq69 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35353 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35353 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.723Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.8Z 
│                       ├ [64] ╭ VulnerabilityID : CVE-2026-35354 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6704cac93effc5af3eed5cf275fa16d80147eed416f7352917976
│                       │      │                   ede6d7faa8f 
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
│                       ├ [65] ╭ VulnerabilityID : CVE-2026-35355 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35355 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cc470afff170e0f232aad13b925ace476d92f2a0facecc5e11463
│                       │      │                   237e5bd505a 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-239g-2685-54x3 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35355 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35355 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.993Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.013Z 
│                       ├ [66] ╭ VulnerabilityID : CVE-2026-35356 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35356 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:deedd4829f20d04768a98495dd10335b0eff8cfaad457ef649385
│                       │      │                   4e754de039f 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-gwm6-q8ch-hcfr 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35356 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35356 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.13Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.117Z 
│                       ├ [67] ╭ VulnerabilityID : CVE-2026-35357 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:efca2bc98d62de3bafe9ef1639f03826c03a99b35f4ec88fbc3bc
│                       │      │                   82edb15c84d 
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
│                       ├ [68] ╭ VulnerabilityID : CVE-2026-35358 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35358 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6b3b3adca956119175f75a9bbdcf076d07a38ba4d8ec16d0cefc3
│                       │      │                   48c60926149 
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
│                       │      │                  ├ [5]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-8vrf-r662-2w2v 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-35358 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-35358 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.393Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.33Z 
│                       ├ [69] ╭ VulnerabilityID : CVE-2026-35359 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e9f37fc8dcb21055a7198965226a28b0aeabd9c2306eee750f8ff
│                       │      │                   de9b432c1ac 
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
│                       ├ [70] ╭ VulnerabilityID : CVE-2026-35360 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5e0c6c0da727ec39ad660d2d8efdf15fadd0bbe73d484a8ac3923
│                       │      │                   823711de249 
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
│                       ├ [71] ╭ VulnerabilityID : CVE-2026-35361 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35361 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:71332a2dfad72a9eaede3c6215aa19a49e98f6f37d5244128b5eb
│                       │      │                   922e4e4b8a4 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-r9hw-mj3w-phcq 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35361 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35361 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.827Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.653Z 
│                       ├ [72] ╭ VulnerabilityID : CVE-2026-35362 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35362 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:841246c3e299d43250353078a1b7912bd9a81568d87f4b9a53f6f
│                       │      │                   9e004dff1b5 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-w6xc-g9qj-vp32 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35362 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35362 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.96Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.76Z 
│                       ├ [73] ╭ VulnerabilityID : CVE-2026-35363 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f1f77f24350b43fadd7bfb84cc9b5e13092ae72024a27aa2977b3
│                       │      │                   f6db8a3fcc7 
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
│                       ├ [74] ╭ VulnerabilityID : CVE-2026-35364 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fc0a33392ce5ad79c9f950783668d647e9c8c5e15cfa1e6b53846
│                       │      │                   8888d61d6e1 
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
│                       ├ [75] ╭ VulnerabilityID : CVE-2026-35365 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35365 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d8fcff86e08ccee6bcab27418d16a0d2838d46fba4098f000f7f7
│                       │      │                   db17f68173b 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-h444-6j9x-p8vh 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35365 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35365 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.9Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.08Z 
│                       ├ [76] ╭ VulnerabilityID : CVE-2026-35366 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35366 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4be5dfe6b18f3db421f1c66138576d65f1ab901bdb9594cd6bb98
│                       │      │                   c9c47d9c5b1 
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
│                       │      │                  ├ [5]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-p7h3-7q52-72w8 
│                       │      │                  ├ [6]: https://nvd.nist.gov/vuln/detail/CVE-2026-35366 
│                       │      │                  ╰ [7]: https://www.cve.org/CVERecord?id=CVE-2026-35366 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.167Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.19Z 
│                       ├ [77] ╭ VulnerabilityID : CVE-2026-35367 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5dee0116488e45d736f8189e5588ecfee0e18577e144cb97dee14
│                       │      │                   43b6be67ee8 
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
│                       ├ [78] ╭ VulnerabilityID : CVE-2026-35368 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5f00b3be82ae195f6b8ee0effa5d4c1535028b69a22516e4d65b4
│                       │      │                   3562cbdd816 
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
│                       ├ [79] ╭ VulnerabilityID : CVE-2026-35369 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35369 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:434cc2e869410b3d152ccb03f00a7abc83958925205f277ea736b
│                       │      │                   fd736371ad5 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-p6rv-2qpm-fwvg 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35369 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35369 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.687Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.51Z 
│                       ├ [80] ╭ VulnerabilityID : CVE-2026-35370 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0468ddece38e46854fa0e7faa741708e5eb491c598409ac52c964
│                       │      │                   ce6c075185a 
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
│                       ├ [81] ╭ VulnerabilityID : CVE-2026-35371 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5d28e0005a8152c7b89b0b9cb696765e18ff9149a4976d799aea8
│                       │      │                   f55cb5b8ad2 
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
│                       ├ [82] ╭ VulnerabilityID : CVE-2026-35372 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35372 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b5d4f9187cd1601d378806263f3ef7471c7938292fc7efd68d39e
│                       │      │                   f221c7f3591 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.83Z 
│                       ├ [83] ╭ VulnerabilityID : CVE-2026-35373 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a17f364701f72b23b2b81b971f610ded7f98861e4b4e31ec968d4
│                       │      │                   bee33269562 
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
│                       ├ [84] ╭ VulnerabilityID : CVE-2026-35374 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:99d06bb50a20e9202b6e68c992adbca6d3771fed52254a798a198
│                       │      │                   b859cb1d778 
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
│                       ├ [85] ╭ VulnerabilityID : CVE-2026-35375 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35375 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:236b60f25b354a4f730513aa3b243f4861ac86b98b51da112fe14
│                       │      │                   63d205305dc 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.143Z 
│                       ├ [86] ╭ VulnerabilityID : CVE-2026-35376 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35376 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0fac738b62d29df3295456d74112e7d83973c2d73563bc7b55dea
│                       │      │                   6db3e64c5ee 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.25Z 
│                       ├ [87] ╭ VulnerabilityID : CVE-2026-35377 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d2298e058a0f00927d259a2acbafc13f96e60d21594a61b8e2011
│                       │      │                   5928c597933 
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
│                       ├ [88] ╭ VulnerabilityID : CVE-2026-35378 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35378 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:173ce50006fee8ccb55e1a779f61bba5a671178222e7110534bb6
│                       │      │                   d8ebdb72924 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.463Z 
│                       ├ [89] ╭ VulnerabilityID : CVE-2026-35379 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35379 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e0cf6094a055b9185f18e5b041426e5e3b69dee2565c32a4b46ce
│                       │      │                   da8b38c997d 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.57Z 
│                       ├ [90] ╭ VulnerabilityID : CVE-2026-35380 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35380 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9563caa2588acf5850ac80f94c00bfef2a3fe82cd6e35b755ca89
│                       │      │                   01a26391fcc 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.673Z 
│                       ├ [91] ╭ VulnerabilityID : CVE-2026-35381 
│                       │      ├ PkgID           : rust-coreutils@0.2.2-0ubuntu2.1 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.2.2-0ubuntu2.1?arch=a
│                       │      │                  │       md64&distro=ubuntu-25.10 
│                       │      │                  ╰ UID : ebefeb85901fc403 
│                       │      ├ InstalledVersion: 0.2.2-0ubuntu2.1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35381 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:25c734f9d9ff71fa5c63b2c7cdb3f4c6b6be68106c59de719c2ef
│                       │      │                   b0c4b94b065 
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
│                       │      │                  ├ [4]: https://github.com/uutils/coreutils/security/advisorie
│                       │      │                  │      s/GHSA-pmfc-4wjj-gmhx 
│                       │      │                  ├ [5]: https://nvd.nist.gov/vuln/detail/CVE-2026-35381 
│                       │      │                  ╰ [6]: https://www.cve.org/CVERecord?id=CVE-2026-35381 
│                       │      ├ PublishedDate   : 2026-04-22T17:16:43.2Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.78Z 
│                       ├ [92] ╭ VulnerabilityID : CVE-2025-45582 
│                       │      ├ PkgID           : tar@1.35+dfsg-3.1build1 
│                       │      ├ PkgName         : tar 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-3.1build1?arch=amd64&d
│                       │      │                  │       istro=ubuntu-25.10 
│                       │      │                  ╰ UID : 41081f85f98b9d6a 
│                       │      ├ InstalledVersion: 1.35+dfsg-3.1build1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-45582 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fc7f5143aaf5d6db8e25aae5ac6f934a0b2bbeec4dbd64d462949
│                       │      │                   6d42d6591e3 
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
│                       │      │                  ├ [7] : https://errata.rockylinux.org/RLSA-2026:0002 
│                       │      │                  ├ [8] : https://github.com/i900008/vulndb/blob/main/Gnu_tar_v
│                       │      │                  │       uln.md 
│                       │      │                  ├ [9] : https://linux.oracle.com/cve/CVE-2025-45582.html 
│                       │      │                  ├ [10]: https://linux.oracle.com/errata/ELSA-2026-0067.html 
│                       │      │                  ├ [11]: https://lists.gnu.org/archive/html/bug-tar/2025-08/ms
│                       │      │                  │       g00012.html 
│                       │      │                  ├ [12]: https://nvd.nist.gov/vuln/detail/CVE-2025-45582 
│                       │      │                  ├ [13]: https://ubuntu.com/security/notices/USN-8510-1 
│                       │      │                  ├ [14]: https://www.cve.org/CVERecord?id=CVE-2025-45582 
│                       │      │                  ├ [15]: https://www.gnu.org/software/tar/ 
│                       │      │                  ├ [16]: https://www.gnu.org/software/tar/manual/html_node/Int
│                       │      │                  │       egrity.html 
│                       │      │                  ├ [17]: https://www.gnu.org/software/tar/manual/html_node/Int
│                       │      │                  │       egrity.html#Integrity 
│                       │      │                  ╰ [18]: https://www.gnu.org/software/tar/manual/html_node/Sec
│                       │      │                          urity-rules-of-thumb.html 
│                       │      ├ PublishedDate   : 2025-07-11T17:15:37.183Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T09:25:34.87Z 
│                       ├ [93] ╭ VulnerabilityID : CVE-2026-27456 
│                       │      ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27456 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d3812e45760bb6cd209768d8412769f07652254fc452a5cdc7fe6
│                       │      │                   3cf448cbdee 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:27:11.017Z 
│                       ├ [94] ╭ VulnerabilityID : CVE-2026-3184 
│                       │      ├ PkgID           : util-linux@2.41-4ubuntu4.2 
│                       │      ├ PkgName         : util-linux 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/util-linux@2.41-4ubuntu4.2?arch=amd64&
│                       │      │                  │       distro=ubuntu-25.10 
│                       │      │                  ╰ UID : 4a5ea37c462ea4f5 
│                       │      ├ InstalledVersion: 2.41-4ubuntu4.2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-3184 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:80fecc88d0b6a614c41c7786f11191b629892bcf74ece0d95ce62
│                       │      │                   1390732f0a3 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T10:43:10.203Z 
│                       ├ [95] ╭ VulnerabilityID : CVE-2021-31879 
│                       │      ├ PkgID           : wget@1.25.0-2ubuntu3 
│                       │      ├ PkgName         : wget 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu3?arch=amd64&distro
│                       │      │                  │       =ubuntu-25.10 
│                       │      │                  ╰ UID : 3ae34724b04a04d7 
│                       │      ├ InstalledVersion: 1.25.0-2ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                       │      │                  │         c0d01e33784d64a22814 
│                       │      │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                       │      │                            937fe30eccf2ed4508f9 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:60135fdd320e9102045469f8f5855d9848f84f3e44264848e1c88
│                       │      │                   871c84407f1 
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
│                       │      ╰ LastModifiedDate: 2026-06-17T03:52:23.987Z 
│                       ╰ [96] ╭ VulnerabilityID : CVE-2026-27171 
│                              ├ PkgID           : zlib1g@1:1.3.dfsg+really1.3.1-1ubuntu2 
│                              ├ PkgName         : zlib1g 
│                              ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/zlib1g@1.3.dfsg%2Breally1.3.1-1ubuntu2
│                              │                  │       ?arch=amd64&distro=ubuntu-25.10&epoch=1 
│                              │                  ╰ UID : a2db0415a832ade 
│                              ├ InstalledVersion: 1:1.3.dfsg+really1.3.1-1ubuntu2 
│                              ├ Status          : affected 
│                              ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4b
│                              │                  │         c0d01e33784d64a22814 
│                              │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f
│                              │                            937fe30eccf2ed4508f9 
│                              ├ SeveritySource  : ubuntu 
│                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27171 
│                              ├ DataSource       ╭ ID  : ubuntu 
│                              │                  ├ Name: Ubuntu CVE Tracker 
│                              │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                              ├ Fingerprint     : sha256:f04594c468d60ecfaaa42e1e057906ffb469f194d246485b5e6c9
│                              │                   8d8b6fe60b8 
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
│                              │                  ├ julia      : 1 
│                              │                  ├ nvd        : 2 
│                              │                  ├ photon     : 2 
│                              │                  ├ redhat     : 1 
│                              │                  ╰ ubuntu     : 1 
│                              ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                              │                  │        │           /A:L 
│                              │                  │        ╰ V3Score : 2.9 
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
                        │     ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                        │     │                  │         0d01e33784d64a22814 
                        │     │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                        │     │                            37fe30eccf2ed4508f9 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54512 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:9f16829c21fa858c2d2ff351dd29ccc2f296cd4e4911ce18c952d6
                        │     │                   9a08beee9f 
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
                        │     ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                        │     │                  │         0d01e33784d64a22814 
                        │     │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                        │     │                            37fe30eccf2ed4508f9 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54513 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:20239ae6c67c0b6d0720b5f39ba76ece35293f2a7749a5fcfcc669
                        │     │                   6d6ff1f60c 
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
                        │     ╰ LastModifiedDate: 2026-07-03T13:17:29.627Z 
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
                        │     ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                        │     │                  │         0d01e33784d64a22814 
                        │     │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                        │     │                            37fe30eccf2ed4508f9 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54514 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:756ea0a74d3c6bfb90e1811428bedc6820dc17a74316b4f6d472f5
                        │     │                   79ba6893f1 
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
                        │     ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                        │     │                  │         0d01e33784d64a22814 
                        │     │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                        │     │                            37fe30eccf2ed4508f9 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54515 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:83145790e1767db6b070952f74d05686b95f984f5c876761aae08f
                        │     │                   7d65a1aebf 
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
                        │     ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                        │     │                  │         0d01e33784d64a22814 
                        │     │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                        │     │                            37fe30eccf2ed4508f9 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54516 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:6940dec6973684fd40a004399e7126c99b72b0225880b85f954783
                        │     │                   7632b8a599 
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
                        │     ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                        │     │                  │         0d01e33784d64a22814 
                        │     │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                        │     │                            37fe30eccf2ed4508f9 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54517 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:4368e0668353530f8189186436d06e63ef04352f09b8a8ee6d294b
                        │     │                   16af58a1f0 
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
                              ├ Layer            ╭ Digest: sha256:5d05ebcf9e9e9e48321ca6b8c16b0f51d80f24b59e4bc
                              │                  │         0d01e33784d64a22814 
                              │                  ╰ DiffID: sha256:3abc0486e46222cc5aba63f411fe5b104c2f3d1ea49f9
                              │                            37fe30eccf2ed4508f9 
                              ├ SeveritySource  : ghsa 
                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54518 
                              ├ DataSource       ╭ ID  : ghsa 
                              │                  ├ Name: GitHub Security Advisory Maven 
                              │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                              │                          osystem%3Amaven 
                              ├ Fingerprint     : sha256:4626dd2f9ae135a0a135a00902d259710cc0595b390e14bf8b981d
                              │                   814e2cc68d 
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
