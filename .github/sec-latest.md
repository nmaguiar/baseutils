````yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:latest (alpine 3.23.0_alpha20250612) 
│     ├ Class          : os-pkgs 
│     ├ Type           : alpine 
│     ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2025-9086 
│                       │     ├ PkgID           : curl@8.15.0-r1 
│                       │     ├ PkgName         : curl 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/curl@8.15.0-r1?arch=x86_64&distro=3.23.
│                       │     │                  │       0_alpha20250612 
│                       │     │                  ╰ UID : 1e4774d17cac5563 
│                       │     ├ InstalledVersion: 8.15.0-r1 
│                       │     ├ FixedVersion    : 8.16.0-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:020ecf237201966036d343785c220f37a1d892635f57b
│                       │     │                  │         a7d021ec11ffb16723c 
│                       │     │                  ╰ DiffID: sha256:aabf480a74f08707188ff364c85e928a76c5172a361c2
│                       │     │                            9dbad8ae4a60c0bd86a 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-9086 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : [Out of bounds read for cookie path] 
│                       │     ├ Description     : Out-of-bounds read when dealing with cookies 
│                       │     ├ Severity        : LOW 
│                       │     ├ VendorSeverity   ─ ubuntu: 1 
│                       │     ╰ References       ╭ [0]: https://curl.se/docs/CVE-2025-9086.html 
│                       │                        ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2025-9086 
│                       ├ [1] ╭ VulnerabilityID : CVE-2025-10148 
│                       │     ├ PkgID           : curl@8.15.0-r1 
│                       │     ├ PkgName         : curl 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/curl@8.15.0-r1?arch=x86_64&distro=3.23.
│                       │     │                  │       0_alpha20250612 
│                       │     │                  ╰ UID : 1e4774d17cac5563 
│                       │     ├ InstalledVersion: 8.15.0-r1 
│                       │     ├ FixedVersion    : 8.16.0-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:020ecf237201966036d343785c220f37a1d892635f57b
│                       │     │                  │         a7d021ec11ffb16723c 
│                       │     │                  ╰ DiffID: sha256:aabf480a74f08707188ff364c85e928a76c5172a361c2
│                       │     │                            9dbad8ae4a60c0bd86a 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-10148 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : [predictable WebSocket mask] 
│                       │     ╰ Severity        : UNKNOWN 
│                       ├ [2] ╭ VulnerabilityID : CVE-2025-9086 
│                       │     ├ PkgID           : libcurl@8.15.0-r1 
│                       │     ├ PkgName         : libcurl 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libcurl@8.15.0-r1?arch=x86_64&distro=3.
│                       │     │                  │       23.0_alpha20250612 
│                       │     │                  ╰ UID : 207617dd56a7519f 
│                       │     ├ InstalledVersion: 8.15.0-r1 
│                       │     ├ FixedVersion    : 8.16.0-r0 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:020ecf237201966036d343785c220f37a1d892635f57b
│                       │     │                  │         a7d021ec11ffb16723c 
│                       │     │                  ╰ DiffID: sha256:aabf480a74f08707188ff364c85e928a76c5172a361c2
│                       │     │                            9dbad8ae4a60c0bd86a 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-9086 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Title           : [Out of bounds read for cookie path] 
│                       │     ├ Description     : Out-of-bounds read when dealing with cookies 
│                       │     ├ Severity        : LOW 
│                       │     ├ VendorSeverity   ─ ubuntu: 1 
│                       │     ╰ References       ╭ [0]: https://curl.se/docs/CVE-2025-9086.html 
│                       │                        ╰ [1]: https://www.cve.org/CVERecord?id=CVE-2025-9086 
│                       ╰ [3] ╭ VulnerabilityID : CVE-2025-10148 
│                             ├ PkgID           : libcurl@8.15.0-r1 
│                             ├ PkgName         : libcurl 
│                             ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libcurl@8.15.0-r1?arch=x86_64&distro=3.
│                             │                  │       23.0_alpha20250612 
│                             │                  ╰ UID : 207617dd56a7519f 
│                             ├ InstalledVersion: 8.15.0-r1 
│                             ├ FixedVersion    : 8.16.0-r0 
│                             ├ Status          : fixed 
│                             ├ Layer            ╭ Digest: sha256:020ecf237201966036d343785c220f37a1d892635f57b
│                             │                  │         a7d021ec11ffb16723c 
│                             │                  ╰ DiffID: sha256:aabf480a74f08707188ff364c85e928a76c5172a361c2
│                             │                            9dbad8ae4a60c0bd86a 
│                             ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-10148 
│                             ├ DataSource       ╭ ID  : alpine 
│                             │                  ├ Name: Alpine Secdb 
│                             │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                             ├ Title           : [predictable WebSocket mask] 
│                             ╰ Severity        : UNKNOWN 
╰ [1] ╭ Target: Java 
      ├ Class : lang-pkgs 
      ╰ Type  : jar 
````
