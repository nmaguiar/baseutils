````yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:latest (alpine 3.23.0_alpha20250612) 
│     ├ Class          : os-pkgs 
│     ├ Type           : alpine 
│     ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2025-4575 
│                       │     ├ PkgID           : libcrypto3@3.5.0-r0 
│                       │     ├ PkgName         : libcrypto3 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libcrypto3@3.5.0-r0?arch=x86_64&distro=
│                       │     │                  │       3.23.0_alpha20250612 
│                       │     │                  ╰ UID : a4f80010e7087a11 
│                       │     ├ InstalledVersion: 3.5.0-r0 
│                       │     ├ FixedVersion    : 3.5.1-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:6d4311eb70f1e3fcf9763fe1649151b6c37f446618c56
│                       │     │                  │         2a377f16b912b6f3abb 
│                       │     │                  ╰ DiffID: sha256:cf8f4a60b385996e7680949265f582b6aa5dda4d74322
│                       │     │                            41e87c8670a5e404557 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-4575 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : Issue summary: Use of -addreject option with the openssl x509
│                       │     │                    applicat ... 
│                       │     ├ Description     : Issue summary: Use of -addreject option with the openssl x509
│                       │     │                    application adds
│                       │     │                   a trusted use instead of a rejected use for a certificate.
│                       │     │                   
│                       │     │                   Impact summary: If a user intends to make a trusted
│                       │     │                   certificate rejected for
│                       │     │                   a particular use it will be instead marked as trusted for
│                       │     │                   that use.
│                       │     │                   A copy & paste error during minor refactoring of the code
│                       │     │                   introduced this
│                       │     │                   issue in the OpenSSL 3.5 version. If, for example, a trusted
│                       │     │                   CA certificate
│                       │     │                   should be trusted only for the purpose of authenticating TLS
│                       │     │                   servers but not
│                       │     │                   for CMS signature verification and the CMS signature
│                       │     │                   verification is intended
│                       │     │                   to be marked as rejected with the -addreject option, the
│                       │     │                   resulting CA
│                       │     │                   certificate will be trusted for CMS signature verification
│                       │     │                   purpose instead.
│                       │     │                   Only users which use the trusted certificate format who use
│                       │     │                   the openssl x509
│                       │     │                   command line application to add rejected uses are affected by
│                       │     │                    this issue.
│                       │     │                   The issues affecting only the command line application are
│                       │     │                   considered to
│                       │     │                   be Low severity.
│                       │     │                   The FIPS modules in 3.5, 3.4, 3.3, 3.2, 3.1 and 3.0 are not
│                       │     │                   affected by this
│                       │     │                   issue.
│                       │     │                   OpenSSL 3.4, 3.3, 3.2, 3.1, 3.0, 1.1.1 and 1.0.2 are also not
│                       │     │                    affected by this
│                       │     │                   issue. 
│                       │     ├ Severity        : UNKNOWN 
│                       │     ├ CweIDs           ─ [0]: CWE-295 
│                       │     ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2025/05/22/1 
│                       │     │                  ├ [1]: https://github.com/openssl/openssl/commit/e96d22446e633
│                       │     │                  │      d117e6c9904cb15b4693e956eaa 
│                       │     │                  ╰ [2]: https://openssl-library.org/news/secadv/20250522.txt 
│                       │     ├ PublishedDate   : 2025-05-22T14:16:07.63Z 
│                       │     ╰ LastModifiedDate: 2025-05-23T15:55:02.04Z 
│                       ├ [1] ╭ VulnerabilityID : CVE-2025-4575 
│                       │     ├ PkgID           : libssl3@3.5.0-r0 
│                       │     ├ PkgName         : libssl3 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libssl3@3.5.0-r0?arch=x86_64&distro=3.2
│                       │     │                  │       3.0_alpha20250612 
│                       │     │                  ╰ UID : 7a86a4ef5d4ce4a6 
│                       │     ├ InstalledVersion: 3.5.0-r0 
│                       │     ├ FixedVersion    : 3.5.1-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:6d4311eb70f1e3fcf9763fe1649151b6c37f446618c56
│                       │     │                  │         2a377f16b912b6f3abb 
│                       │     │                  ╰ DiffID: sha256:cf8f4a60b385996e7680949265f582b6aa5dda4d74322
│                       │     │                            41e87c8670a5e404557 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-4575 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : Issue summary: Use of -addreject option with the openssl x509
│                       │     │                    applicat ... 
│                       │     ├ Description     : Issue summary: Use of -addreject option with the openssl x509
│                       │     │                    application adds
│                       │     │                   a trusted use instead of a rejected use for a certificate.
│                       │     │                   
│                       │     │                   Impact summary: If a user intends to make a trusted
│                       │     │                   certificate rejected for
│                       │     │                   a particular use it will be instead marked as trusted for
│                       │     │                   that use.
│                       │     │                   A copy & paste error during minor refactoring of the code
│                       │     │                   introduced this
│                       │     │                   issue in the OpenSSL 3.5 version. If, for example, a trusted
│                       │     │                   CA certificate
│                       │     │                   should be trusted only for the purpose of authenticating TLS
│                       │     │                   servers but not
│                       │     │                   for CMS signature verification and the CMS signature
│                       │     │                   verification is intended
│                       │     │                   to be marked as rejected with the -addreject option, the
│                       │     │                   resulting CA
│                       │     │                   certificate will be trusted for CMS signature verification
│                       │     │                   purpose instead.
│                       │     │                   Only users which use the trusted certificate format who use
│                       │     │                   the openssl x509
│                       │     │                   command line application to add rejected uses are affected by
│                       │     │                    this issue.
│                       │     │                   The issues affecting only the command line application are
│                       │     │                   considered to
│                       │     │                   be Low severity.
│                       │     │                   The FIPS modules in 3.5, 3.4, 3.3, 3.2, 3.1 and 3.0 are not
│                       │     │                   affected by this
│                       │     │                   issue.
│                       │     │                   OpenSSL 3.4, 3.3, 3.2, 3.1, 3.0, 1.1.1 and 1.0.2 are also not
│                       │     │                    affected by this
│                       │     │                   issue. 
│                       │     ├ Severity        : UNKNOWN 
│                       │     ├ CweIDs           ─ [0]: CWE-295 
│                       │     ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2025/05/22/1 
│                       │     │                  ├ [1]: https://github.com/openssl/openssl/commit/e96d22446e633
│                       │     │                  │      d117e6c9904cb15b4693e956eaa 
│                       │     │                  ╰ [2]: https://openssl-library.org/news/secadv/20250522.txt 
│                       │     ├ PublishedDate   : 2025-05-22T14:16:07.63Z 
│                       │     ╰ LastModifiedDate: 2025-05-23T15:55:02.04Z 
│                       ├ [2] ╭ VulnerabilityID : CVE-2025-4575 
│                       │     ├ PkgID           : openssl@3.5.0-r0 
│                       │     ├ PkgName         : openssl 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/openssl@3.5.0-r0?arch=x86_64&distro=3.2
│                       │     │                  │       3.0_alpha20250612 
│                       │     │                  ╰ UID : eb8f3721924b72d7 
│                       │     ├ InstalledVersion: 3.5.0-r0 
│                       │     ├ FixedVersion    : 3.5.1-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:6d4311eb70f1e3fcf9763fe1649151b6c37f446618c56
│                       │     │                  │         2a377f16b912b6f3abb 
│                       │     │                  ╰ DiffID: sha256:cf8f4a60b385996e7680949265f582b6aa5dda4d74322
│                       │     │                            41e87c8670a5e404557 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-4575 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : Issue summary: Use of -addreject option with the openssl x509
│                       │     │                    applicat ... 
│                       │     ├ Description     : Issue summary: Use of -addreject option with the openssl x509
│                       │     │                    application adds
│                       │     │                   a trusted use instead of a rejected use for a certificate.
│                       │     │                   
│                       │     │                   Impact summary: If a user intends to make a trusted
│                       │     │                   certificate rejected for
│                       │     │                   a particular use it will be instead marked as trusted for
│                       │     │                   that use.
│                       │     │                   A copy & paste error during minor refactoring of the code
│                       │     │                   introduced this
│                       │     │                   issue in the OpenSSL 3.5 version. If, for example, a trusted
│                       │     │                   CA certificate
│                       │     │                   should be trusted only for the purpose of authenticating TLS
│                       │     │                   servers but not
│                       │     │                   for CMS signature verification and the CMS signature
│                       │     │                   verification is intended
│                       │     │                   to be marked as rejected with the -addreject option, the
│                       │     │                   resulting CA
│                       │     │                   certificate will be trusted for CMS signature verification
│                       │     │                   purpose instead.
│                       │     │                   Only users which use the trusted certificate format who use
│                       │     │                   the openssl x509
│                       │     │                   command line application to add rejected uses are affected by
│                       │     │                    this issue.
│                       │     │                   The issues affecting only the command line application are
│                       │     │                   considered to
│                       │     │                   be Low severity.
│                       │     │                   The FIPS modules in 3.5, 3.4, 3.3, 3.2, 3.1 and 3.0 are not
│                       │     │                   affected by this
│                       │     │                   issue.
│                       │     │                   OpenSSL 3.4, 3.3, 3.2, 3.1, 3.0, 1.1.1 and 1.0.2 are also not
│                       │     │                    affected by this
│                       │     │                   issue. 
│                       │     ├ Severity        : UNKNOWN 
│                       │     ├ CweIDs           ─ [0]: CWE-295 
│                       │     ├ References       ╭ [0]: http://www.openwall.com/lists/oss-security/2025/05/22/1 
│                       │     │                  ├ [1]: https://github.com/openssl/openssl/commit/e96d22446e633
│                       │     │                  │      d117e6c9904cb15b4693e956eaa 
│                       │     │                  ╰ [2]: https://openssl-library.org/news/secadv/20250522.txt 
│                       │     ├ PublishedDate   : 2025-05-22T14:16:07.63Z 
│                       │     ╰ LastModifiedDate: 2025-05-23T15:55:02.04Z 
│                       ├ [3] ╭ VulnerabilityID : CVE-2025-32462 
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
│                       │     ├ VendorSeverity   ╭ alma       : 3 
│                       │     │                  ├ oracle-oval: 3 
│                       │     │                  ├ photon     : 1 
│                       │     │                  ├ redhat     : 3 
│                       │     │                  ╰ ubuntu     : 3 
│                       │     ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/
│                       │     │                           │           A:H 
│                       │     │                           ╰ V3Score : 7 
│                       │     ├ References       ╭ [0] : https://access.redhat.com/errata/RHSA-2025:10110 
│                       │     │                  ├ [1] : https://access.redhat.com/security/cve/CVE-2025-32462 
│                       │     │                  ├ [2] : https://bugzilla.redhat.com/2374692 
│                       │     │                  ├ [3] : https://errata.almalinux.org/8/ALSA-2025-10110.html 
│                       │     │                  ├ [4] : https://linux.oracle.com/cve/CVE-2025-32462.html 
│                       │     │                  ├ [5] : https://linux.oracle.com/errata/ELSA-2025-9978.html 
│                       │     │                  ├ [6] : https://nvd.nist.gov/vuln/detail/CVE-2025-32462 
│                       │     │                  ├ [7] : https://ubuntu.com/security/notices/USN-7604-1 
│                       │     │                  ├ [8] : https://ubuntu.com/security/notices/USN-7604-2 
│                       │     │                  ├ [9] : https://www.cve.org/CVERecord?id=CVE-2025-32462 
│                       │     │                  ├ [10]: https://www.openwall.com/lists/oss-security/2025/06/30/2 
│                       │     │                  ├ [11]: https://www.stratascale.com/vulnerability-alert-CVE-20
│                       │     │                  │       25-32462-sudo-host 
│                       │     │                  ├ [12]: https://www.sudo.ws/releases/changelog/ 
│                       │     │                  ├ [13]: https://www.sudo.ws/security/advisories/ 
│                       │     │                  ╰ [14]: https://www.sudo.ws/security/advisories/host_any/ 
│                       │     ├ PublishedDate   : 2025-06-30T21:15:30.08Z 
│                       │     ╰ LastModifiedDate: 2025-06-30T21:15:30.08Z 
│                       ╰ [4] ╭ VulnerabilityID : CVE-2025-32463 
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
│                             ├ VendorSeverity   ╭ photon: 4 
│                             │                  ├ redhat: 3 
│                             │                  ╰ ubuntu: 3 
│                             ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/
│                             │                           │           A:H 
│                             │                           ╰ V3Score : 7.8 
│                             ├ References       ╭ [0] : https://access.redhat.com/security/cve/CVE-2025-32463 
│                             │                  ├ [1] : https://access.redhat.com/security/cve/cve-2025-32463 
│                             │                  ├ [2] : https://bugs.gentoo.org/show_bug.cgi?id=CVE-2025-32463 
│                             │                  ├ [3] : https://explore.alas.aws.amazon.com/CVE-2025-32463.html 
│                             │                  ├ [4] : https://nvd.nist.gov/vuln/detail/CVE-2025-32463 
│                             │                  ├ [5] : https://security-tracker.debian.org/tracker/CVE-2025-3
│                             │                  │       2463 
│                             │                  ├ [6] : https://ubuntu.com/security/notices/USN-7604-1 
│                             │                  ├ [7] : https://www.cve.org/CVERecord?id=CVE-2025-32463 
│                             │                  ├ [8] : https://www.openwall.com/lists/oss-security/2025/06/30/3 
│                             │                  ├ [9] : https://www.stratascale.com/vulnerability-alert-CVE-20
│                             │                  │       25-32463-sudo-chroot 
│                             │                  ├ [10]: https://www.sudo.ws/releases/changelog/ 
│                             │                  ├ [11]: https://www.sudo.ws/security/advisories/ 
│                             │                  ├ [12]: https://www.sudo.ws/security/advisories/chroot_bug/ 
│                             │                  ├ [13]: https://www.suse.com/security/cve/CVE-2025-32463.html 
│                             │                  ╰ [14]: https://www.suse.com/support/update/announcement/2025/
│                             │                          suse-su-202502177-1/ 
│                             ├ PublishedDate   : 2025-06-30T21:15:30.257Z 
│                             ╰ LastModifiedDate: 2025-07-01T20:15:24.673Z 
╰ [1] ╭ Target: Java 
      ├ Class : lang-pkgs 
      ╰ Type  : jar 
````
