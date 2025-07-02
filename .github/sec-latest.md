````yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:latest (alpine 3.23.0_alpha20250612) 
│     ├ Class          : os-pkgs 
│     ├ Type           : alpine 
│     ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2025-32462 
│                       │     ├ PkgID           : sudo@1.9.17-r0 
│                       │     ├ PkgName         : sudo 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/sudo@1.9.17-r0?arch=x86_64&distro=3.23.
│                       │     │                  │       0_alpha20250612 
│                       │     │                  ╰ UID : f452168152faeaa2 
│                       │     ├ InstalledVersion: 1.9.17-r0 
│                       │     ├ FixedVersion    : 1.9.17_p1-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:6d4311eb70f1e3fcf9763fe1649151b6c37f446618c56
│                       │     │                  │         2a377f16b912b6f3abb 
│                       │     │                  ╰ DiffID: sha256:cf8f4a60b385996e7680949265f582b6aa5dda4d74322
│                       │     │                            41e87c8670a5e404557 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-32462 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : sudo: LPE via host option 
│                       │     ├ Description     : Sudo before 1.9.17p1, when used with a sudoers file that
│                       │     │                   specifies a host that is neither the current host nor ALL,
│                       │     │                   allows listed users to execute commands on unintended
│                       │     │                   machines. 
│                       │     ├ Severity        : HIGH 
│                       │     ├ CweIDs           ─ [0]: CWE-863 
│                       │     ├ VendorSeverity   ╭ oracle-oval: 3 
│                       │     │                  ├ redhat     : 3 
│                       │     │                  ╰ ubuntu     : 3 
│                       │     ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/
│                       │     │                           │           A:H 
│                       │     │                           ╰ V3Score : 7 
│                       │     ├ References       ╭ [0] : https://access.redhat.com/security/cve/CVE-2025-32462 
│                       │     │                  ├ [1] : https://linux.oracle.com/cve/CVE-2025-32462.html 
│                       │     │                  ├ [2] : https://linux.oracle.com/errata/ELSA-2025-9978.html 
│                       │     │                  ├ [3] : https://nvd.nist.gov/vuln/detail/CVE-2025-32462 
│                       │     │                  ├ [4] : https://ubuntu.com/security/notices/USN-7604-1 
│                       │     │                  ├ [5] : https://ubuntu.com/security/notices/USN-7604-2 
│                       │     │                  ├ [6] : https://www.cve.org/CVERecord?id=CVE-2025-32462 
│                       │     │                  ├ [7] : https://www.openwall.com/lists/oss-security/2025/06/30/2 
│                       │     │                  ├ [8] : https://www.stratascale.com/vulnerability-alert-CVE-20
│                       │     │                  │       25-32462-sudo-host 
│                       │     │                  ├ [9] : https://www.sudo.ws/releases/changelog/ 
│                       │     │                  ├ [10]: https://www.sudo.ws/security/advisories/ 
│                       │     │                  ╰ [11]: https://www.sudo.ws/security/advisories/host_any/ 
│                       │     ├ PublishedDate   : 2025-06-30T21:15:30.08Z 
│                       │     ╰ LastModifiedDate: 2025-06-30T21:15:30.08Z 
│                       ╰ [1] ╭ VulnerabilityID : CVE-2025-32463 
│                             ├ PkgID           : sudo@1.9.17-r0 
│                             ├ PkgName         : sudo 
│                             ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/sudo@1.9.17-r0?arch=x86_64&distro=3.23.
│                             │                  │       0_alpha20250612 
│                             │                  ╰ UID : f452168152faeaa2 
│                             ├ InstalledVersion: 1.9.17-r0 
│                             ├ FixedVersion    : 1.9.17_p1-r0 
│                             ├ Status          : fixed 
│                             ├ Layer            ╭ Digest: sha256:6d4311eb70f1e3fcf9763fe1649151b6c37f446618c56
│                             │                  │         2a377f16b912b6f3abb 
│                             │                  ╰ DiffID: sha256:cf8f4a60b385996e7680949265f582b6aa5dda4d74322
│                             │                            41e87c8670a5e404557 
│                             ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-32463 
│                             ├ DataSource       ╭ ID  : alpine 
│                             │                  ├ Name: Alpine Secdb 
│                             │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                             ├ Title           : sudo: LPE via chroot option 
│                             ├ Description     : Sudo before 1.9.17p1 allows local users to obtain root access
│                             │                    because /etc/nsswitch.conf from a user-controlled directory
│                             │                   is used with the --chroot option. 
│                             ├ Severity        : HIGH 
│                             ├ CweIDs           ─ [0]: CWE-829 
│                             ├ VendorSeverity   ╭ redhat: 3 
│                             │                  ╰ ubuntu: 3 
│                             ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/
│                             │                           │           A:H 
│                             │                           ╰ V3Score : 7.8 
│                             ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2025-32463 
│                             │                  ├ [1]: https://nvd.nist.gov/vuln/detail/CVE-2025-32463 
│                             │                  ├ [2]: https://ubuntu.com/security/notices/USN-7604-1 
│                             │                  ├ [3]: https://www.cve.org/CVERecord?id=CVE-2025-32463 
│                             │                  ├ [4]: https://www.openwall.com/lists/oss-security/2025/06/30/3 
│                             │                  ├ [5]: https://www.stratascale.com/vulnerability-alert-CVE-202
│                             │                  │      5-32463-sudo-chroot 
│                             │                  ├ [6]: https://www.sudo.ws/releases/changelog/ 
│                             │                  ├ [7]: https://www.sudo.ws/security/advisories/ 
│                             │                  ╰ [8]: https://www.sudo.ws/security/advisories/chroot_bug/ 
│                             ├ PublishedDate   : 2025-06-30T21:15:30.257Z 
│                             ╰ LastModifiedDate: 2025-06-30T21:15:30.257Z 
╰ [1] ╭ Target: Java 
      ├ Class : lang-pkgs 
      ╰ Type  : jar 
````
