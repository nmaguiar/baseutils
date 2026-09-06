```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:latest (alpine 3.25.0_alpha20260805) 
│     ├ Class          : os-pkgs 
│     ├ Type           : alpine 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2026-78408 
│                       │     ├ PkgID           : libblkid@2.42.3-r0 
│                       │     ├ PkgName         : libblkid 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libblkid@2.42.3-r0?arch=x86_64&distro=3
│                       │     │                  │       .25.0_alpha20260805 
│                       │     │                  ╰ UID : e81c25e07875af4d 
│                       │     ├ InstalledVersion: 2.42.3-r0 
│                       │     ├ FixedVersion    : 2.42.3-r1 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:de0175de2835f5eef8736f54fdca0e3f0f915002e79fa
│                       │     │                  │         5c379ccd864db26f6ba 
│                       │     │                  ╰ DiffID: sha256:d0fafff4a4630986a13b89a6911de421a021a9e0f0d28
│                       │     │                            e8c01ad755e7816e4c6 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-78408 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Fingerprint     : sha256:e08ce9026657bd51713edf19efed5b595440b42189208a5e720925
│                       │     │                   83db4f694d 
│                       │     ├ Title           : util-linux: util-linux: nsenter --join-cgroup leaks root
│                       │     │                   cgroup migration authority 
│                       │     ├ Description     : The nsenter --join-cgroup option opens the target
│                       │     │                   cgroup.procs file as root and leaves that file descriptor
│                       │     │                   open across later namespace and credential changes and across
│                       │     │                    execve(). Because the kernel checks later cgroup migrations
│                       │     │                   using the credentials from the original open, a program run
│                       │     │                   in an attacker-controlled target can inherit root's ability
│                       │     │                   to move host processes between cgroups. After a privileged
│                       │     │                   operator uses --join-cgroup against that target, an
│                       │     │                   unprivileged user can migrate and terminate unrelated root
│                       │     │                   processes. 
│                       │     ├ Severity        : HIGH 
│                       │     ├ CweIDs                  
│                       │     │                  ───────
│                       │     │                  CWE-775
│                       │     │                  
│                       │     ├ VendorSeverity   ─ redhat: 3 
│                       │     ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:N/I:H/
│                       │     │                           │           A:H 
│                       │     │                           ╰ V3Score : 7.9 
│                       │     ├ References                                                                     
│                       │     │                  ──────────────────────────────────────────────────────────────
│                       │     │                  http://www.openwall.com/lists/oss-security/2026/09/05/2       
│                       │     │                  https://access.redhat.com/errata/RHSA-2026:63162              
│                       │     │                  https://access.redhat.com/security/cve/CVE-2026-78408         
│                       │     │                  https://bugzilla.redhat.com/show_bug.cgi?id=2522497           
│                       │     │                  https://github.com/util-linux/util-linux/security/advisories/G
│                       │     │                  HSA-55fx-f4gg-cfhj                                            
│                       │     │                  https://nvd.nist.gov/vuln/detail/CVE-2026-78408               
│                       │     │                                                                                
│                       │     │                  https://www.cve.org/CVERecord?id=CVE-2026-78408               
│                       │     │                                                                                
│                       │     │                  
│                       │     ├ PublishedDate   : 2026-09-02T16:17:23.687Z 
│                       │     ╰ LastModifiedDate: 2026-09-05T14:17:23.727Z 
│                       ├ [1] ╭ VulnerabilityID : CVE-2026-78408 
│                       │     ├ PkgID           : libmount@2.42.3-r0 
│                       │     ├ PkgName         : libmount 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libmount@2.42.3-r0?arch=x86_64&distro=3
│                       │     │                  │       .25.0_alpha20260805 
│                       │     │                  ╰ UID : 7d5232be06c02a1d 
│                       │     ├ InstalledVersion: 2.42.3-r0 
│                       │     ├ FixedVersion    : 2.42.3-r1 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:de0175de2835f5eef8736f54fdca0e3f0f915002e79fa
│                       │     │                  │         5c379ccd864db26f6ba 
│                       │     │                  ╰ DiffID: sha256:d0fafff4a4630986a13b89a6911de421a021a9e0f0d28
│                       │     │                            e8c01ad755e7816e4c6 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-78408 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Fingerprint     : sha256:8eb86efe096f2629ccd15222bcd907d7d7fe21e07fae683266bd5d
│                       │     │                   5e90d64c49 
│                       │     ├ Title           : util-linux: util-linux: nsenter --join-cgroup leaks root
│                       │     │                   cgroup migration authority 
│                       │     ├ Description     : The nsenter --join-cgroup option opens the target
│                       │     │                   cgroup.procs file as root and leaves that file descriptor
│                       │     │                   open across later namespace and credential changes and across
│                       │     │                    execve(). Because the kernel checks later cgroup migrations
│                       │     │                   using the credentials from the original open, a program run
│                       │     │                   in an attacker-controlled target can inherit root's ability
│                       │     │                   to move host processes between cgroups. After a privileged
│                       │     │                   operator uses --join-cgroup against that target, an
│                       │     │                   unprivileged user can migrate and terminate unrelated root
│                       │     │                   processes. 
│                       │     ├ Severity        : HIGH 
│                       │     ├ CweIDs                  
│                       │     │                  ───────
│                       │     │                  CWE-775
│                       │     │                  
│                       │     ├ VendorSeverity   ─ redhat: 3 
│                       │     ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:N/I:H/
│                       │     │                           │           A:H 
│                       │     │                           ╰ V3Score : 7.9 
│                       │     ├ References                                                                     
│                       │     │                  ──────────────────────────────────────────────────────────────
│                       │     │                  http://www.openwall.com/lists/oss-security/2026/09/05/2       
│                       │     │                  https://access.redhat.com/errata/RHSA-2026:63162              
│                       │     │                  https://access.redhat.com/security/cve/CVE-2026-78408         
│                       │     │                  https://bugzilla.redhat.com/show_bug.cgi?id=2522497           
│                       │     │                  https://github.com/util-linux/util-linux/security/advisories/G
│                       │     │                  HSA-55fx-f4gg-cfhj                                            
│                       │     │                  https://nvd.nist.gov/vuln/detail/CVE-2026-78408               
│                       │     │                                                                                
│                       │     │                  https://www.cve.org/CVERecord?id=CVE-2026-78408               
│                       │     │                                                                                
│                       │     │                  
│                       │     ├ PublishedDate   : 2026-09-02T16:17:23.687Z 
│                       │     ╰ LastModifiedDate: 2026-09-05T14:17:23.727Z 
│                       ╰ [2] ╭ VulnerabilityID : CVE-2026-78408 
│                             ├ PkgID           : util-linux-doc@2.42.3-r0 
│                             ├ PkgName         : util-linux-doc 
│                             ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/util-linux-doc@2.42.3-r0?arch=x86_64&di
│                             │                  │       stro=3.25.0_alpha20260805 
│                             │                  ╰ UID : 4c47abb702f47050 
│                             ├ InstalledVersion: 2.42.3-r0 
│                             ├ FixedVersion    : 2.42.3-r1 
│                             ├ Status          : fixed 
│                             ├ Layer            ╭ Digest: sha256:de0175de2835f5eef8736f54fdca0e3f0f915002e79fa
│                             │                  │         5c379ccd864db26f6ba 
│                             │                  ╰ DiffID: sha256:d0fafff4a4630986a13b89a6911de421a021a9e0f0d28
│                             │                            e8c01ad755e7816e4c6 
│                             ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-78408 
│                             ├ DataSource       ╭ ID  : alpine 
│                             │                  ├ Name: Alpine Secdb 
│                             │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                             ├ Fingerprint     : sha256:857c4b492f1ff1bce726714e3a95710424b68972a35d02ef9262c0
│                             │                   03b6d13094 
│                             ├ Title           : util-linux: util-linux: nsenter --join-cgroup leaks root
│                             │                   cgroup migration authority 
│                             ├ Description     : The nsenter --join-cgroup option opens the target
│                             │                   cgroup.procs file as root and leaves that file descriptor
│                             │                   open across later namespace and credential changes and across
│                             │                    execve(). Because the kernel checks later cgroup migrations
│                             │                   using the credentials from the original open, a program run
│                             │                   in an attacker-controlled target can inherit root's ability
│                             │                   to move host processes between cgroups. After a privileged
│                             │                   operator uses --join-cgroup against that target, an
│                             │                   unprivileged user can migrate and terminate unrelated root
│                             │                   processes. 
│                             ├ Severity        : HIGH 
│                             ├ CweIDs                  
│                             │                  ───────
│                             │                  CWE-775
│                             │                  
│                             ├ VendorSeverity   ─ redhat: 3 
│                             ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:C/C:N/I:H/
│                             │                           │           A:H 
│                             │                           ╰ V3Score : 7.9 
│                             ├ References                                                                     
│                             │                  ──────────────────────────────────────────────────────────────
│                             │                  http://www.openwall.com/lists/oss-security/2026/09/05/2       
│                             │                  https://access.redhat.com/errata/RHSA-2026:63162              
│                             │                  https://access.redhat.com/security/cve/CVE-2026-78408         
│                             │                  https://bugzilla.redhat.com/show_bug.cgi?id=2522497           
│                             │                  https://github.com/util-linux/util-linux/security/advisories/G
│                             │                  HSA-55fx-f4gg-cfhj                                            
│                             │                  https://nvd.nist.gov/vuln/detail/CVE-2026-78408               
│                             │                                                                                
│                             │                  https://www.cve.org/CVERecord?id=CVE-2026-78408               
│                             │                                                                                
│                             │                  
│                             ├ PublishedDate   : 2026-09-02T16:17:23.687Z 
│                             ╰ LastModifiedDate: 2026-09-05T14:17:23.727Z 
╰ [1] ╭ Target  : Java 
      ├ Class   : lang-pkgs 
      ├ Type    : jar 
      ╰ Packages 
```
