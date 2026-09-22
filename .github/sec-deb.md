```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:deb (ubuntu 26.04) 
│     ├ Class          : os-pkgs 
│     ├ Type           : ubuntu 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0]  ╭ VulnerabilityID : CVE-2026-13608 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-13608 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:69f8c978629a50a451f4dad0780d4db222c3e36c80ee0e95fad83
│                       │      │                   4a43534c81e 
│                       │      ├ Title           : curl: curl: Authentication bypass in OpenLDAP SASL
│                       │      │                   negotiation via Man-in-the-Middle (MITM) attack 
│                       │      ├ Description     : A flaw in the libcurl SASL negotiation for LDAP
│                       │      │                   authentication allows an
│                       │      │                   incomplete handshake sequence to be misinterpreted as a
│                       │      │                   successful
│                       │      │                   cryptographic verification. An attacker executing a
│                       │      │                   Man-in-the-Middle (MITM)
│                       │      │                   attack can inject a premature or shortcut response that
│                       │      │                   bypasses complete peer
│                       │      │                   validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-923
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-13608        
│                       │      │                  https://curl.se/docs/CVE-2026-13608.html                     
│                       │      │                  https://curl.se/docs/CVE-2026-13608.json                     
│                       │      │                  https://github.com/curl/curl/pull/22213/changes/1a00e2a73675c
│                       │      │                  9521d214aafd6c02b553bfeb022                                  
│                       │      │                  https://hackerone.com/reports/3822248                        
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-13608              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-13608              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:19.81Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:26.353Z 
│                       ├ [1]  ╭ VulnerabilityID : CVE-2026-18924 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18924 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bbc556a2a4570788b4952adedbaf84a3b77880230df5d78df6e9c
│                       │      │                   7c44f47e75b 
│                       │      ├ Title           : curl: libcurl: Use-after-free in HTTP/2 Server Push with
│                       │      │                   shared connections 
│                       │      ├ Description     : A flaw in libcurl's handling of HTTP/2 Server Push streams,
│                       │      │                   when the parent
│                       │      │                   handle is set to share connections with other handles, can
│                       │      │                   lead to
│                       │      │                   use-after-free in the cleanup process. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18924        
│                       │      │                  https://curl.se/docs/CVE-2026-18924.html                     
│                       │      │                  https://curl.se/docs/CVE-2026-18924.json                     
│                       │      │                  https://github.com/curl/curl/commit/90325ff0444cbdff368bda5d2
│                       │      │                  6d6                                                          
│                       │      │                  https://hackerone.com/reports/3916059                        
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18924              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18924              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:20.553Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:27.063Z 
│                       ├ [2]  ╭ VulnerabilityID : CVE-2026-19931 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-19931 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:738dae974451eeedaeb4b779824ecef23630c763a7528426e532d
│                       │      │                   dd7f9da5201 
│                       │      ├ Title           : curl: libcurl: Information disclosure via incorrect
│                       │      │                   connection reuse with Negotiate authentication 
│                       │      ├ Description     : A flaw in libcurl makes it wrongly reuse an HTTP connection
│                       │      │                   setup for a given
│                       │      │                   hostname using Negotiate authentication, when the initial
│                       │      │                   request is done
│                       │      │                   using empty credentials. This can make user B's request get
│                       │      │                   sent over user A's
│                       │      │                   previously authenticated connection. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-488
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                 
│                       │      │                  ──────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-19931     
│                       │      │                  https://curl.se/docs/CVE-2026-19931.html                  
│                       │      │                  https://curl.se/docs/CVE-2026-19931.json                  
│                       │      │                  https://github.com/curl/curl/commit/7103a93b05bc69ea98ed9d
│                       │      │                  https://hackerone.com/reports/3923520                     
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-19931           
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-19931           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:20.733Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:27.29Z 
│                       ├ [3]  ╭ VulnerabilityID : CVE-2026-80229 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-80229 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d77764e597a84c6fe03465303a490f19de580bb904884f71ad26c
│                       │      │                   ccbc8bc4e48 
│                       │      ├ Title           : When performing transfers via libcurl\u2019s multi
│                       │      │                   interface, pooled T ... 
│                       │      ├ Description     : When performing transfers via libcurl’s multi interface,
│                       │      │                   pooled TLS
│                       │      │                   connections can outlive their originating easy handles. In
│                       │      │                   OpenSSL 3 provider
│                       │      │                   configurations, libcurl attaches an allocated library
│                       │      │                   context to the easy
│                       │      │                   handle's state and passes it to OpenSSL without acquiring an
│                       │      │                    ownership
│                       │      │                   reference; destroying the easy handle prematurely frees this
│                       │      │                    context while the
│                       │      │                   active connection retains a dangling pointer, leading to a
│                       │      │                   heap-use-after-free
│                       │      │                   upon subsequent I/O or post-handshake operations. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References                                                                 
│                       │      │                  ──────────────────────────────────────────────────────────
│                       │      │                  https://curl.se/docs/CVE-2026-80229.html                  
│                       │      │                  https://curl.se/docs/CVE-2026-80229.json                  
│                       │      │                  https://github.com/curl/curl/commit/7ea37abc6ac0120ba5f6d9
│                       │      │                  https://hackerone.com/reports/3969255                     
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-80229           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.217Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:30.157Z 
│                       ├ [4]  ╭ VulnerabilityID : CVE-2026-80230 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-80230 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ac90f9e6f4e8cc14656083e4e38bf971b1d05e615dea183466ae2
│                       │      │                   b9fd6704f3f 
│                       │      ├ Title           : When `CURLOPT_PINNEDPUBLICKEY` is configured alongside
│                       │      │                   options that di ... 
│                       │      ├ Description     : When `CURLOPT_PINNEDPUBLICKEY` is configured alongside
│                       │      │                   options that disable
│                       │      │                   standard peer verification (`CURLOPT_SSL_VERIFYPEER = 0`
│                       │      │                   and
│                       │      │                   `CURLOPT_SSL_VERIFYHOST = 0`), libcurl fails to enforce
│                       │      │                   public key pinning on
│                       │      │                   connections established without a presented server
│                       │      │                   certificate. Bypassing the
│                       │      │                   pinning check under these disabled-verification conditions
│                       │      │                   allows
│                       │      │                   unauthenticated connections to succeed when they should be
│                       │      │                   rejected. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-295
│                       │      │                  
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References                                                                
│                       │      │                  ─────────────────────────────────────────────────────────
│                       │      │                  https://curl.se/docs/CVE-2026-80230.html                 
│                       │      │                  https://curl.se/docs/CVE-2026-80230.json                 
│                       │      │                  https://github.com/curl/curl/commit/5267ed859d545534d0c21
│                       │      │                  https://hackerone.com/reports/3969300                    
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-80230          
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.327Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:30.337Z 
│                       ├ [5]  ╭ VulnerabilityID : CVE-2026-80255 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-80255 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8a7b693aae02d19ef5b9f1ba59ec4efa7680b8c01ae703c332d09
│                       │      │                   63947d0cb1f 
│                       │      ├ Title           : A `Set-Cookie:` header using tab (horizontal tab, ASCII code
│                       │      │                    9) instea ... 
│                       │      ├ Description     : A `Set-Cookie:` header using tab (horizontal tab, ASCII code
│                       │      │                    9) instead of
│                       │      │                   space (ascii code 32) immediately before the `Secure`
│                       │      │                   attribute causes curl to
│                       │      │                   store the cookie without its Secure flag. The cookie might
│                       │      │                   then wrongfully be
│                       │      │                   sent over plaintext HTTP on subsequent requests to the same
│                       │      │                   host. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-201
│                       │      │                  
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References                                                                 
│                       │      │                  ──────────────────────────────────────────────────────────
│                       │      │                  https://curl.se/docs/CVE-2026-80255.html                  
│                       │      │                  https://curl.se/docs/CVE-2026-80255.json                  
│                       │      │                  https://github.com/curl/curl/commit/4f6aa41a0145e930e76677
│                       │      │                  https://hackerone.com/reports/3972395                     
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-80255           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.623Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:30.77Z 
│                       ├ [6]  ╭ VulnerabilityID : CVE-2026-82209 
│                       │      ├ PkgID           : curl@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : curl 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/curl@8.18.0-1ubuntu2.5?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : 59f792208966fece 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-82209 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:61a44e4648980a34390edd815a3234f360f01026fdede6fb08731
│                       │      │                   16e5508cdff 
│                       │      ├ Title           : curl: libcurl: Information disclosure via improper Public
│                       │      │                   Suffix List boundary check 
│                       │      ├ Description     : When libpsl support is enabled, libcurl fails to enforce the
│                       │      │                    Public Suffix
│                       │      │                   List boundary check when processing a `Set-Cookie` header
│                       │      │                   where the `Domain`
│                       │      │                   attribute explicitly matches an origin host that is itself a
│                       │      │                    public suffix
│                       │      │                   (e.g., `Domain=co.uk` set by `co.uk`).
│                       │      │                   
│                       │      │                   Instead of coercing it into a strict host-only cookie,
│                       │      │                   libcurl saves the
│                       │      │                   cookie with wildcard domain scope (`.co.uk`). Consequently,
│                       │      │                   the cookie is
│                       │      │                   inappropriately included in subsequent outbound requests or
│                       │      │                   HTTP redirects to
│                       │      │                   arbitrary sibling subdomains under the same public suffix
│                       │      │                   (e.g.,
│                       │      │                   `attacker.co.uk`). 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-201
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.1 
│                       │      ├ References                                                                      
│                       │      │                  ───────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-82209          
│                       │      │                  https://curl.se/docs/CVE-2026-82209.html                       
│                       │      │                  https://curl.se/docs/CVE-2026-82209.json                       
│                       │      │                  https://github.com/curl/curl/commit/95c1e8915dce64606bd753fd47f
│                       │      │                  https://hackerone.com/reports/3972385                          
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-82209                
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-82209                
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.847Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:31.233Z 
│                       ├ [7]  ╭ VulnerabilityID : CVE-2026-18374 
│                       │      ├ PkgID           : libc-bin@2.43-2ubuntu2.4 
│                       │      ├ PkgName         : libc-bin 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-bin@2.43-2ubuntu2.4?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : b964ecf8d3a43faa 
│                       │      ├ InstalledVersion: 2.43-2ubuntu2.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2b7747e3ca1fbac384348b425d54064feb80244d75c898d8dc25e
│                       │      │                   88cbff2b742 
│                       │      ├ Title           : glibc: glibc: Heap buffer overflow via attacker-controlled
│                       │      │                   fopen mode string 
│                       │      ├ Description     : Passing an effectively empty string to the `,ccs=` syntax
│                       │      │                   extension of the mode argument in the `fopen` function in
│                       │      │                   the GNU C Library version 2.45 or earlier may result in a
│                       │      │                   heap buffer overflow when the mode string input to the
│                       │      │                   function is attacker controlled.
│                       │      │                   
│                       │      │                   This usage pattern is not seen in applications in common
│                       │      │                   GNU/Linux distributions and applications that process
│                       │      │                   user-supplied values for `ccs` should not pass them through
│                       │      │                   without validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-787
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/08/27/6      
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18374        
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18374              
│                       │      │                  https://sourceware.org/bugzilla/show_bug.cgi?id=34574        
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/G
│                       │      │                  LIBC-SA-2026-0015                                            
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=adviso
│                       │      │                  ries/GLIBC-SA-2026-0015                                      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18374              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-27T20:17:03.553Z 
│                       │      ╰ LastModifiedDate: 2026-09-03T16:43:15.293Z 
│                       ├ [8]  ╭ VulnerabilityID : CVE-2026-18374 
│                       │      ├ PkgID           : libc-gconv-modules-extra@2.43-2ubuntu2.4 
│                       │      ├ PkgName         : libc-gconv-modules-extra 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc-gconv-modules-extra@2.43-2ubuntu2
│                       │      │                  │       .4?arch=amd64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : bbb7a8f7a59474e8 
│                       │      ├ InstalledVersion: 2.43-2ubuntu2.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f54c444e0c9ebc2d32f63a0af4466c3c6aab45bff8f053b6fb14c
│                       │      │                   f4249388f18 
│                       │      ├ Title           : glibc: glibc: Heap buffer overflow via attacker-controlled
│                       │      │                   fopen mode string 
│                       │      ├ Description     : Passing an effectively empty string to the `,ccs=` syntax
│                       │      │                   extension of the mode argument in the `fopen` function in
│                       │      │                   the GNU C Library version 2.45 or earlier may result in a
│                       │      │                   heap buffer overflow when the mode string input to the
│                       │      │                   function is attacker controlled.
│                       │      │                   
│                       │      │                   This usage pattern is not seen in applications in common
│                       │      │                   GNU/Linux distributions and applications that process
│                       │      │                   user-supplied values for `ccs` should not pass them through
│                       │      │                   without validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-787
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/08/27/6      
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18374        
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18374              
│                       │      │                  https://sourceware.org/bugzilla/show_bug.cgi?id=34574        
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/G
│                       │      │                  LIBC-SA-2026-0015                                            
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=adviso
│                       │      │                  ries/GLIBC-SA-2026-0015                                      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18374              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-27T20:17:03.553Z 
│                       │      ╰ LastModifiedDate: 2026-09-03T16:43:15.293Z 
│                       ├ [9]  ╭ VulnerabilityID : CVE-2026-18374 
│                       │      ├ PkgID           : libc6@2.43-2ubuntu2.4 
│                       │      ├ PkgName         : libc6 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libc6@2.43-2ubuntu2.4?arch=amd64&distr
│                       │      │                  │       o=ubuntu-26.04 
│                       │      │                  ╰ UID : fe574f54c2bc3102 
│                       │      ├ InstalledVersion: 2.43-2ubuntu2.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:05840eb3345f430a3e0eb917241f34c0fd961345c9b7db87e2ee1
│                       │      │                   f9d8f8b04ec 
│                       │      ├ Title           : glibc: glibc: Heap buffer overflow via attacker-controlled
│                       │      │                   fopen mode string 
│                       │      ├ Description     : Passing an effectively empty string to the `,ccs=` syntax
│                       │      │                   extension of the mode argument in the `fopen` function in
│                       │      │                   the GNU C Library version 2.45 or earlier may result in a
│                       │      │                   heap buffer overflow when the mode string input to the
│                       │      │                   function is attacker controlled.
│                       │      │                   
│                       │      │                   This usage pattern is not seen in applications in common
│                       │      │                   GNU/Linux distributions and applications that process
│                       │      │                   user-supplied values for `ccs` should not pass them through
│                       │      │                   without validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-787
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/08/27/6      
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18374        
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18374              
│                       │      │                  https://sourceware.org/bugzilla/show_bug.cgi?id=34574        
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/G
│                       │      │                  LIBC-SA-2026-0015                                            
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=adviso
│                       │      │                  ries/GLIBC-SA-2026-0015                                      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18374              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-27T20:17:03.553Z 
│                       │      ╰ LastModifiedDate: 2026-09-03T16:43:15.293Z 
│                       ├ [10] ╭ VulnerabilityID : CVE-2026-13608 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-13608 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:220480167b3c8302b8f011f335705d17c35f0c378bb563b2399d8
│                       │      │                   8c6326aea30 
│                       │      ├ Title           : curl: curl: Authentication bypass in OpenLDAP SASL
│                       │      │                   negotiation via Man-in-the-Middle (MITM) attack 
│                       │      ├ Description     : A flaw in the libcurl SASL negotiation for LDAP
│                       │      │                   authentication allows an
│                       │      │                   incomplete handshake sequence to be misinterpreted as a
│                       │      │                   successful
│                       │      │                   cryptographic verification. An attacker executing a
│                       │      │                   Man-in-the-Middle (MITM)
│                       │      │                   attack can inject a premature or shortcut response that
│                       │      │                   bypasses complete peer
│                       │      │                   validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-923
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-13608        
│                       │      │                  https://curl.se/docs/CVE-2026-13608.html                     
│                       │      │                  https://curl.se/docs/CVE-2026-13608.json                     
│                       │      │                  https://github.com/curl/curl/pull/22213/changes/1a00e2a73675c
│                       │      │                  9521d214aafd6c02b553bfeb022                                  
│                       │      │                  https://hackerone.com/reports/3822248                        
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-13608              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-13608              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:19.81Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:26.353Z 
│                       ├ [11] ╭ VulnerabilityID : CVE-2026-18924 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18924 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f6b4d72949be898150809f40691e8562b33706aeb8ac710e487d3
│                       │      │                   77b626ba68a 
│                       │      ├ Title           : curl: libcurl: Use-after-free in HTTP/2 Server Push with
│                       │      │                   shared connections 
│                       │      ├ Description     : A flaw in libcurl's handling of HTTP/2 Server Push streams,
│                       │      │                   when the parent
│                       │      │                   handle is set to share connections with other handles, can
│                       │      │                   lead to
│                       │      │                   use-after-free in the cleanup process. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18924        
│                       │      │                  https://curl.se/docs/CVE-2026-18924.html                     
│                       │      │                  https://curl.se/docs/CVE-2026-18924.json                     
│                       │      │                  https://github.com/curl/curl/commit/90325ff0444cbdff368bda5d2
│                       │      │                  6d6                                                          
│                       │      │                  https://hackerone.com/reports/3916059                        
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18924              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18924              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:20.553Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:27.063Z 
│                       ├ [12] ╭ VulnerabilityID : CVE-2026-19931 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-19931 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e360677fb356f4d7ad5a15ed3a8fe88bea3a469375a9dcfb4d715
│                       │      │                   9158b77aa67 
│                       │      ├ Title           : curl: libcurl: Information disclosure via incorrect
│                       │      │                   connection reuse with Negotiate authentication 
│                       │      ├ Description     : A flaw in libcurl makes it wrongly reuse an HTTP connection
│                       │      │                   setup for a given
│                       │      │                   hostname using Negotiate authentication, when the initial
│                       │      │                   request is done
│                       │      │                   using empty credentials. This can make user B's request get
│                       │      │                   sent over user A's
│                       │      │                   previously authenticated connection. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-488
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                 
│                       │      │                  ──────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-19931     
│                       │      │                  https://curl.se/docs/CVE-2026-19931.html                  
│                       │      │                  https://curl.se/docs/CVE-2026-19931.json                  
│                       │      │                  https://github.com/curl/curl/commit/7103a93b05bc69ea98ed9d
│                       │      │                  https://hackerone.com/reports/3923520                     
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-19931           
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-19931           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:20.733Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:27.29Z 
│                       ├ [13] ╭ VulnerabilityID : CVE-2026-80229 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-80229 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a5df85a58253b823ff41b167023c09082952b80137ddc31660b21
│                       │      │                   d3b9a570dcc 
│                       │      ├ Title           : When performing transfers via libcurl\u2019s multi
│                       │      │                   interface, pooled T ... 
│                       │      ├ Description     : When performing transfers via libcurl’s multi interface,
│                       │      │                   pooled TLS
│                       │      │                   connections can outlive their originating easy handles. In
│                       │      │                   OpenSSL 3 provider
│                       │      │                   configurations, libcurl attaches an allocated library
│                       │      │                   context to the easy
│                       │      │                   handle's state and passes it to OpenSSL without acquiring an
│                       │      │                    ownership
│                       │      │                   reference; destroying the easy handle prematurely frees this
│                       │      │                    context while the
│                       │      │                   active connection retains a dangling pointer, leading to a
│                       │      │                   heap-use-after-free
│                       │      │                   upon subsequent I/O or post-handshake operations. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References                                                                 
│                       │      │                  ──────────────────────────────────────────────────────────
│                       │      │                  https://curl.se/docs/CVE-2026-80229.html                  
│                       │      │                  https://curl.se/docs/CVE-2026-80229.json                  
│                       │      │                  https://github.com/curl/curl/commit/7ea37abc6ac0120ba5f6d9
│                       │      │                  https://hackerone.com/reports/3969255                     
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-80229           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.217Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:30.157Z 
│                       ├ [14] ╭ VulnerabilityID : CVE-2026-80230 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-80230 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6129dd91c910f8e534a0b9f263e04269ceb40395e58d066cc25b8
│                       │      │                   25aa4035b31 
│                       │      ├ Title           : When `CURLOPT_PINNEDPUBLICKEY` is configured alongside
│                       │      │                   options that di ... 
│                       │      ├ Description     : When `CURLOPT_PINNEDPUBLICKEY` is configured alongside
│                       │      │                   options that disable
│                       │      │                   standard peer verification (`CURLOPT_SSL_VERIFYPEER = 0`
│                       │      │                   and
│                       │      │                   `CURLOPT_SSL_VERIFYHOST = 0`), libcurl fails to enforce
│                       │      │                   public key pinning on
│                       │      │                   connections established without a presented server
│                       │      │                   certificate. Bypassing the
│                       │      │                   pinning check under these disabled-verification conditions
│                       │      │                   allows
│                       │      │                   unauthenticated connections to succeed when they should be
│                       │      │                   rejected. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-295
│                       │      │                  
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References                                                                
│                       │      │                  ─────────────────────────────────────────────────────────
│                       │      │                  https://curl.se/docs/CVE-2026-80230.html                 
│                       │      │                  https://curl.se/docs/CVE-2026-80230.json                 
│                       │      │                  https://github.com/curl/curl/commit/5267ed859d545534d0c21
│                       │      │                  https://hackerone.com/reports/3969300                    
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-80230          
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.327Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:30.337Z 
│                       ├ [15] ╭ VulnerabilityID : CVE-2026-80255 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-80255 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:48b97bc2051c87f12ad9ab2dedb160eb88e325f4c4177636f0893
│                       │      │                   4e6572d251c 
│                       │      ├ Title           : A `Set-Cookie:` header using tab (horizontal tab, ASCII code
│                       │      │                    9) instea ... 
│                       │      ├ Description     : A `Set-Cookie:` header using tab (horizontal tab, ASCII code
│                       │      │                    9) instead of
│                       │      │                   space (ascii code 32) immediately before the `Secure`
│                       │      │                   attribute causes curl to
│                       │      │                   store the cookie without its Secure flag. The cookie might
│                       │      │                   then wrongfully be
│                       │      │                   sent over plaintext HTTP on subsequent requests to the same
│                       │      │                   host. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-201
│                       │      │                  
│                       │      ├ VendorSeverity   ─ ubuntu: 2 
│                       │      ├ References                                                                 
│                       │      │                  ──────────────────────────────────────────────────────────
│                       │      │                  https://curl.se/docs/CVE-2026-80255.html                  
│                       │      │                  https://curl.se/docs/CVE-2026-80255.json                  
│                       │      │                  https://github.com/curl/curl/commit/4f6aa41a0145e930e76677
│                       │      │                  https://hackerone.com/reports/3972395                     
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-80255           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.623Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:30.77Z 
│                       ├ [16] ╭ VulnerabilityID : CVE-2026-82209 
│                       │      ├ PkgID           : libcurl4t64@8.18.0-1ubuntu2.5 
│                       │      ├ PkgName         : libcurl4t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libcurl4t64@8.18.0-1ubuntu2.5?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8758ff99a6247a97 
│                       │      ├ InstalledVersion: 8.18.0-1ubuntu2.5 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-82209 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:0574d01a0b656bb0d6f910750b6856a6b727a5f844d21d78f4794
│                       │      │                   8c6a3e9f806 
│                       │      ├ Title           : curl: libcurl: Information disclosure via improper Public
│                       │      │                   Suffix List boundary check 
│                       │      ├ Description     : When libpsl support is enabled, libcurl fails to enforce the
│                       │      │                    Public Suffix
│                       │      │                   List boundary check when processing a `Set-Cookie` header
│                       │      │                   where the `Domain`
│                       │      │                   attribute explicitly matches an origin host that is itself a
│                       │      │                    public suffix
│                       │      │                   (e.g., `Domain=co.uk` set by `co.uk`).
│                       │      │                   
│                       │      │                   Instead of coercing it into a strict host-only cookie,
│                       │      │                   libcurl saves the
│                       │      │                   cookie with wildcard domain scope (`.co.uk`). Consequently,
│                       │      │                   the cookie is
│                       │      │                   inappropriately included in subsequent outbound requests or
│                       │      │                   HTTP redirects to
│                       │      │                   arbitrary sibling subdomains under the same public suffix
│                       │      │                   (e.g.,
│                       │      │                   `attacker.co.uk`). 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-201
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:L/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.1 
│                       │      ├ References                                                                      
│                       │      │                  ───────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-82209          
│                       │      │                  https://curl.se/docs/CVE-2026-82209.html                       
│                       │      │                  https://curl.se/docs/CVE-2026-82209.json                       
│                       │      │                  https://github.com/curl/curl/commit/95c1e8915dce64606bd753fd47f
│                       │      │                  https://hackerone.com/reports/3972385                          
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-82209                
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-82209                
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-06T18:17:22.847Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T07:16:31.233Z 
│                       ├ [17] ╭ VulnerabilityID : CVE-2025-66382 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-66382 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4bc17e7e54a4e855bbea7389016bd17bd9e38c58414f156f401d1
│                       │      │                   3910504231c 
│                       │      ├ Title           : libexpat: libexpat: Denial of service via crafted file
│                       │      │                   processing 
│                       │      ├ Description     : In libexpat through 2.7.3, a crafted file with an
│                       │      │                   approximate size of 2 MiB can lead to dozens of seconds of
│                       │      │                   processing time. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-407
│                       │      │                  
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
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2025/12/02/1      
│                       │      │                  https://access.redhat.com/security/cve/CVE-2025-66382        
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-082556.h
│                       │      │                  tml                                                          
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-253495.h
│                       │      │                  tml                                                          
│                       │      │                  https://github.com/libexpat/libexpat/issues/1076             
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2025-66382              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2025-66382              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2025-11-28T07:15:57.9Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T09:56:45.24Z 
│                       ├ [18] ╭ VulnerabilityID : CVE-2026-32776 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-32776 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6ada7f9371fafb81ddd26f7ddfb40b53b1a49676fd731e15bf160
│                       │      │                   d82a8869271 
│                       │      ├ Title           : libexpat: libexpat: Denial of Service due to NULL pointer
│                       │      │                   dereference 
│                       │      ├ Description     : libexpat before 2.7.5 allows a NULL pointer dereference with
│                       │      │                    empty external parameter entity content. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-476
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 2 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.2 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-32776        
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-082556.h
│                       │      │                  tml                                                          
│                       │      │                  https://github.com/libexpat/libexpat/pull/1158               
│                       │      │                                                                               
│                       │      │                  https://github.com/libexpat/libexpat/pull/1159               
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-32776              
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-32776              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-03-16T14:19:44.6Z 
│                       │      ╰ LastModifiedDate: 2026-07-14T13:18:49.53Z 
│                       ├ [19] ╭ VulnerabilityID : CVE-2026-32777 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-32777 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5a0732f81bcd9069d7ff2dab1688dc2f5e97edcc4325c217aafd5
│                       │      │                   14d873f06ff 
│                       │      ├ Title           : libexpat: libexpat: Denial of Service via infinite loop in
│                       │      │                   DTD content parsing 
│                       │      ├ Description     : libexpat before 2.7.5 allows an infinite loop while parsing
│                       │      │                   DTD content. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-835
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 2 
│                       │      │                  ├ azure : 1 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-32777        
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-082556.h
│                       │      │                  tml                                                          
│                       │      │                  https://github.com/libexpat/libexpat/issues/1161             
│                       │      │                                                                               
│                       │      │                  https://github.com/libexpat/libexpat/pull/1159               
│                       │      │                                                                               
│                       │      │                  https://github.com/libexpat/libexpat/pull/1162               
│                       │      │                                                                               
│                       │      │                  https://issues.oss-fuzz.com/issues/486993411                 
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-32777              
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-32777              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-03-16T14:19:44.78Z 
│                       │      ╰ LastModifiedDate: 2026-07-14T13:18:49.687Z 
│                       ├ [20] ╭ VulnerabilityID : CVE-2026-32778 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-32778 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:6a35984357846ec6a46df5809b143e3a6481340a1cc829fbbf428
│                       │      │                   9d5ed9bcb05 
│                       │      ├ Title           : libexpat: libexpat: Denial of Service via NULL pointer
│                       │      │                   dereference after out-of-memory condition 
│                       │      ├ Description     : libexpat before 2.7.5 allows a NULL pointer dereference in
│                       │      │                   the function setContext on retry after an earlier
│                       │      │                   ouf-of-memory condition. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-476
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 2 
│                       │      │                  ├ azure : 1 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ photon: 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 5.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.1 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-32778        
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-082556.h
│                       │      │                  tml                                                          
│                       │      │                  https://github.com/libexpat/libexpat/pull/1159               
│                       │      │                                                                               
│                       │      │                  https://github.com/libexpat/libexpat/pull/1163               
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-32778              
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-32778              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-03-16T14:19:44.97Z 
│                       │      ╰ LastModifiedDate: 2026-07-14T13:18:49.843Z 
│                       ├ [21] ╭ VulnerabilityID : CVE-2026-41080 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-41080 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:1ee470109bb340c4d1dda5f1df5d4a7f648c08d7d40eb5ca03203
│                       │      │                   73d0901fb86 
│                       │      ├ Title           : libexpat: expat: libexpat: Denial of Service via hash
│                       │      │                   flooding with crafted XML 
│                       │      ├ Description     : libexpat before 2.8.0 uses insufficient entropy, and thus
│                       │      │                   hash flooding can occur via a crafted XML document. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-331
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 1 
│                       │      │                  ├ azure : 1 
│                       │      │                  ├ julia : 1 
│                       │      │                  ├ photon: 3 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 2.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 3.7 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/04/26/1      
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-41080        
│                       │      │                  https://blog.hartwork.org/posts/expat-2-8-0-released/        
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-082556.h
│                       │      │                  tml                                                          
│                       │      │                  https://github.com/libexpat/libexpat/issues/47               
│                       │      │                                                                               
│                       │      │                  https://github.com/libexpat/libexpat/pull/1183               
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-41080              
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8520-1               
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-41080              
│                       │      │                                                                               
│                       │      │                  https://www.openwall.com/lists/oss-security/2026/04/26/1     
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-16T17:16:54.917Z 
│                       │      ╰ LastModifiedDate: 2026-07-14T13:18:51.257Z 
│                       ├ [22] ╭ VulnerabilityID : CVE-2026-45186 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-45186 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:db585c496c07126670cb3552499c62d97135e392653a6f37db830
│                       │      │                   c2416b8f3fa 
│                       │      ├ Title           : libexpat: denial of service via crafted XML input 
│                       │      ├ Description     : In libexpat before 2.8.1, the computational complexity of
│                       │      │                   attribute name collision checks allows a denial of service
│                       │      │                   via moderately sized crafted XML input. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-407
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 1 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 3 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/05/11/16     
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:22715             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:22721             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:23230             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:26319             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:27201             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:29197             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-45186        
│                       │      │                  https://bugzilla.redhat.com/2468575                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2468575          
│                       │      │                  https://cert-portal.siemens.com/productcert/html/ssa-082556.h
│                       │      │                  tml                                                          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                                                                               
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-45186
│                       │      │                                                                               
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-22715.html         
│                       │      │                                                                               
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:23230                
│                       │      │                                                                               
│                       │      │                  https://github.com/libexpat/libexpat/pull/1216               
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-45186.html             
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-23230.html         
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-45186              
│                       │      │                                                                               
│                       │      │                  https://security.access.redhat.com/data/csaf/v2/vex/2026/cve-
│                       │      │                  2026-45186.json                                              
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-45186              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-05-10T07:16:07.883Z 
│                       │      ╰ LastModifiedDate: 2026-09-16T13:17:58.967Z 
│                       ├ [23] ╭ VulnerabilityID : CVE-2026-50219 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-50219 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7bf9724611a7cff5a193ef03ed733e6d7716a098ea47ab4ac890d
│                       │      │                   e40c551cc7f 
│                       │      ├ Title           : expat: libexpat: Use-after-free vulnerability due to
│                       │      │                   improper handler call depth tracking 
│                       │      ├ Description     : libexpat before 2.8.2 lacks handler call depth tracking for
│                       │      │                   calls to XML_GetBuffer, XML_Parse, XML_ParseBuffer,
│                       │      │                   XML_ParserFree, or XML_ParserReset from within handlers in
│                       │      │                   cases of a policy violation. Thus, a use-after-free can
│                       │      │                   occur, 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 1 
│                       │      │                  ├ julia      : 2 
│                       │      │                  ├ nvd        : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 5.9 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 5.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64810             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64812             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-50219        
│                       │      │                  https://bugzilla.redhat.com/2484620                          
│                       │      │                  https://bugzilla.redhat.com/2490669                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484620          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2490669          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-50219
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56132
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-64810.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:64812                
│                       │      │                  https://github.com/libexpat/libexpat/pull/1246               
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-50219.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-64812-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-50219              
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-50219              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-04T06:16:25.05Z 
│                       │      ╰ LastModifiedDate: 2026-07-22T20:10:00.127Z 
│                       ├ [24] ╭ VulnerabilityID : CVE-2026-56131 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56131 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:fcbc277ff86d79eae1dd981714bb00b3a6b502185d08142fcceef
│                       │      │                   0ae8ea520a8 
│                       │      ├ Title           : libexpat: libexpat: Use-after-free vulnerability due to
│                       │      │                   insufficient handler call depth tracking 
│                       │      ├ Description     : libexpat before 2.8.2 lacks handler call depth tracking for
│                       │      │                   calls to XML_ResumeParser from within handlers in cases of a
│                       │      │                    policy violation. Thus, a use-after-free can occur (similar
│                       │      │                    to the CVE-2026-50219 situation). 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 4.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.5 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56131
│                       │      │                  https://github.com/libexpat/libexpat/pull/1267       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56131      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56131      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-19T06:17:10.107Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T20:15:48.007Z 
│                       ├ [25] ╭ VulnerabilityID : CVE-2026-56132 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56132 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3007904e54baa91600dfd2abf594977b8ee52f505ed6dda2bf1bc
│                       │      │                   3b178b56524 
│                       │      ├ Title           : expat: libexpat: Arbitrary Code Execution via Heap-based
│                       │      │                   Buffer Overflow 
│                       │      ├ Description     : In libexpat before 2.8.2, there is a heap-based buffer
│                       │      │                   overflow in doProlog in xmlparse.c because scaffold backing
│                       │      │                   array reallocation is mishandled when there is
│                       │      │                   data-structure sharing across parsers. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-821
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 2 
│                       │      │                  ├ nvd        : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64810             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64812             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56132        
│                       │      │                  https://bugzilla.redhat.com/2484620                          
│                       │      │                  https://bugzilla.redhat.com/2490669                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484620          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2490669          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-50219
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56132
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-64810.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:64812                
│                       │      │                  https://github.com/libexpat/libexpat/pull/1272               
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-56132.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-64812-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56132              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56132              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-19T06:17:10.253Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T20:15:26.23Z 
│                       ├ [26] ╭ VulnerabilityID : CVE-2026-56403 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56403 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:85f6277cd8f448ab42f88eba1a22689215e5864c0a57bf1f7f26c
│                       │      │                   b60a538c9ea 
│                       │      ├ Title           : libexpat: libexpat: Arbitrary code execution due to integer
│                       │      │                   overflow in storeAtts 
│                       │      ├ Description     : libexpat before 2.8.2 has an integer overflow in storeAtts. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56403
│                       │      │                  https://github.com/libexpat/libexpat/pull/1232       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56403      
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1       
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56403      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:26.59Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T20:15:16.76Z 
│                       ├ [27] ╭ VulnerabilityID : CVE-2026-56404 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56404 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f1cd5ef1864d0ce0a2c187a3aacf80c72c1d4b8acc350674e4876
│                       │      │                   ac1304a8c88 
│                       │      ├ Title           : libexpat: libexpat: Arbitrary Code Execution via integer
│                       │      │                   overflow in addBinding 
│                       │      ├ Description     : libexpat before 2.8.2 has an integer overflow in addBinding. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56404
│                       │      │                  https://github.com/libexpat/libexpat/pull/1249       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56404      
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1       
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56404      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:27.62Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T20:15:05.85Z 
│                       ├ [28] ╭ VulnerabilityID : CVE-2026-56405 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56405 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f808f1041a9402433df2c806f45b812ddb59e1db3e8a3da9139a5
│                       │      │                   4db5a3d6b93 
│                       │      ├ Title           : libexpat: libexpat: Information disclosure and arbitrary
│                       │      │                   code execution via integer overflow 
│                       │      ├ Description     : libexpat before 2.8.2 has an integer overflow in
│                       │      │                   getAttributeId. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56405
│                       │      │                  https://github.com/libexpat/libexpat/pull/1251       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56405      
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1       
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56405      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:27.74Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T20:14:51.73Z 
│                       ├ [29] ╭ VulnerabilityID : CVE-2026-56406 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56406 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e7dd7dca19f27b4f24cc51da3ca9bc61f3734c5eb81267b06ce89
│                       │      │                   5166130da5f 
│                       │      ├ Title           : libexpat: libexpat: Arbitrary code execution via integer
│                       │      │                   overflow in XML_ParseBuffer 
│                       │      ├ Description     : libexpat before 2.8.2 has an integer overflow in
│                       │      │                   XML_ParseBuffer because it lacked a check that was present
│                       │      │                   in XML_Parse. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56406
│                       │      │                  https://github.com/libexpat/libexpat/pull/1255       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56406      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56406      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:27.87Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T16:29:06.077Z 
│                       ├ [30] ╭ VulnerabilityID : CVE-2026-56407 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56407 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:27bb9b3582f8c141a563f57eb0de00a25c2edf8af91606008331c
│                       │      │                   c3571db2396 
│                       │      ├ Title           : libexpat: libexpat: Arbitrary code execution due to integer
│                       │      │                   overflow 
│                       │      ├ Description     : libexpat before 2.8.2 has an integer overflow in doProlog
│                       │      │                   that is related to storeEntityValue and entity textLen. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56407
│                       │      │                  https://github.com/libexpat/libexpat/pull/1262       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56407      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56407      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:27.987Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T16:28:29.983Z 
│                       ├ [31] ╭ VulnerabilityID : CVE-2026-56408 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56408 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:76f6000f148375ac04e6fc58b10054e6b12dc195ce63f001a9063
│                       │      │                   57e9c36d70e 
│                       │      ├ Title           : libexpat before 2.8.2 has an integer overflow in copyString. 
│                       │      ├ Description     : libexpat before 2.8.2 has an integer overflow in copyString. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ julia ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H/
│                       │      │                          │           A:L 
│                       │      │                          ╰ V3Score : 6.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/libexpat/libexpat/commit/16e2efd867ea8567f
│                       │      │                  fa012210b52ef5918e20817                                      
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56408              
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56408              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:28.11Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T16:27:26.523Z 
│                       ├ [32] ╭ VulnerabilityID : CVE-2026-56409 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56409 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9344e0af79588338206fd2165f04e926178aae5c39d75f6a815ea
│                       │      │                   6b8239090c8 
│                       │      ├ Title           : xmlwf in libexpat before 2.8.2 has an integer overflow for
│                       │      │                   the output  ... 
│                       │      ├ Description     : xmlwf in libexpat before 2.8.2 has an integer overflow for
│                       │      │                   the output filename when -d outputDir is used. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ julia ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H/
│                       │      │                          │           A:L 
│                       │      │                          ╰ V3Score : 6.5 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/libexpat/libexpat/pull/1259 
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56409
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56409
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:28.23Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T16:21:55.607Z 
│                       ├ [33] ╭ VulnerabilityID : CVE-2026-56410 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56410 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e78469f209ceb73f989792a5a71bdb56b29370ab3b2dff0001509
│                       │      │                   3fff386d020 
│                       │      ├ Title           : libexpat: libexpat: Integer overflow in xmlwf can lead to
│                       │      │                   information disclosure and arbitrary code execution. 
│                       │      ├ Description     : xmlwf in libexpat before 2.8.2 has an integer overflow in
│                       │      │                   resolveSystemId. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56410
│                       │      │                  https://github.com/libexpat/libexpat/pull/1252       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56410      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56410      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T16:16:28.36Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T16:18:16.427Z 
│                       ├ [34] ╭ VulnerabilityID : CVE-2026-56411 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56411 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ca767e28a308ddd2a55be51fcd19bc5912d08fdb19ed9c1228d36
│                       │      │                   27c06811454 
│                       │      ├ Title           : expat: libexpat: Integer Overflow Vulnerability Leading to
│                       │      │                   Information Disclosure or Code Execution 
│                       │      ├ Description     : xmlwf in libexpat before 2.8.2 has an integer overflow in
│                       │      │                   endDoctypeDecl via NOTATION declarations. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-190
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 6.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56411
│                       │      │                  https://github.com/libexpat/libexpat/pull/1263       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56411      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56411      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T17:16:44.523Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T16:16:36.417Z 
│                       ├ [35] ╭ VulnerabilityID : CVE-2026-56412 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ FixedVersion    : 2.7.4-1ubuntu0.1 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56412 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:07560c69b9224ad4d2217f3524246829dc5ba218effa7b3ebe15f
│                       │      │                   cc97c28f532 
│                       │      ├ Title           : libexpat: libexpat: Use-after-free vulnerability due to
│                       │      │                   improper handling of XML CDATA sections 
│                       │      ├ Description     : libexpat before 2.8.2 does not consider XML_TOK_DATA_CHARS
│                       │      │                   in doCdataSection and thus lacks handler call depth tracking
│                       │      │                    for various calls from within handlers in cases of a policy
│                       │      │                    violation. Thus, a use-after-free can occur. NOTE: this
│                       │      │                   issue exists because of an incomplete fix for
│                       │      │                   CVE-2026-50219. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ julia : 2 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 5.9 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:L 
│                       │      │                  │        ╰ V3Score : 5.9 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-56412
│                       │      │                  https://github.com/libexpat/libexpat/pull/1278       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56412      
│                       │      │                  https://ubuntu.com/security/notices/USN-8790-1       
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56412      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-21T17:16:44.657Z 
│                       │      ╰ LastModifiedDate: 2026-06-23T15:31:30.853Z 
│                       ├ [36] ╭ VulnerabilityID : CVE-2026-66046 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-66046 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8c698f30840aa62bda33773be9d874f0afc55677f35af1a99025f
│                       │      │                   2671407a9ae 
│                       │      ├ Title           : expat: Expat: Denial of Service via quadratic complexity in
│                       │      │                   attribute processing 
│                       │      ├ Description     : Expat through 2.8.3 contains a denial of service
│                       │      │                   vulnerability caused by quadratic algorithmic complexity in
│                       │      │                   the storeAtts() function in xmlparse.c, where processing N
│                       │      │                   specified attributes with non-normalized values triggers an
│                       │      │                   O(N^2) linear scan of elementType->defaultAtts to determine
│                       │      │                   CDATA status. A remote unauthenticated attacker can supply a
│                       │      │                    single well-formed XML document of a few megabytes to an
│                       │      │                   application parsing untrusted XML to cause excessive CPU
│                       │      │                   consumption, resulting in denial of service without
│                       │      │                   requiring authentication, external entity resolution, or
│                       │      │                   non-default parser options. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-407
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 3 
│                       │      │                  ├ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-66046        
│                       │      │                  https://github.com/libexpat/libexpat/pull/1321               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-66046              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-66046              
│                       │      │                  https://www.vulncheck.com/advisories/expat-denial-of-service-
│                       │      │                  via-storeatts-quadratic-complexity                           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-18T15:16:57Z 
│                       │      ╰ LastModifiedDate: 2026-09-18T15:07:24.37Z 
│                       ├ [37] ╭ VulnerabilityID : CVE-2026-72522 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-72522 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:111247c747c343f3c92937c5725b89bf463186b79e8ba41db78df
│                       │      │                   5707bc36837 
│                       │      ├ Title           : expat: libexpat: Denial of Service due to incorrect Unicode
│                       │      │                   surrogate handling 
│                       │      ├ Description     : libexpat before 2.8.3 has an out-of-bounds read and
│                       │      │                   resultant infinite loop because low surrogates are treated
│                       │      │                   the same as high surrogates during Unicode processing in the
│                       │      │                    *_toUtf16 functions. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-125
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.2 
│                       │      ├ References                                                              
│                       │      │                  ───────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/08/11/5
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-72522  
│                       │      │                  https://bugzilla.mozilla.org/show_bug.cgi?id=2053153   
│                       │      │                  https://github.com/libexpat/libexpat/pull/1296         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-72522        
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-72522        
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-10T04:16:50.91Z 
│                       │      ╰ LastModifiedDate: 2026-08-31T19:33:11.197Z 
│                       ├ [38] ╭ VulnerabilityID : CVE-2026-76641 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-76641 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:92009df27929c84c3aa13042ee5410c65699f8921bd9bf44e324b
│                       │      │                   ce66b9226ca 
│                       │      ├ Title           : CVE-2026-76641 affecting package expat for versions less
│                       │      │                   than 2.8.3-2 
│                       │      ├ Description     : Expat through 2.8.3 contains an out-of-bounds read
│                       │      │                   vulnerability that allows attackers to trigger memory
│                       │      │                   corruption by processing XML with external entity parsers
│                       │      │                   created via XML_ExternalEntityParserCreate. A struct size
│                       │      │                   mismatch between ELEMENT_TYPE members causes storeAtts to
│                       │      │                   read the attIndex member past allocated memory boundaries,
│                       │      │                   resulting in failure to normalize whitespace in non-CDATA
│                       │      │                   attributes or a wild pointer dereference causing a segfault.
│                       │      │                    This vulnerability was introduced by the fix for
│                       │      │                   CVE-2026-66046. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-125
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ azure : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/libexpat/libexpat/commit/98599f6dcc2b46041
│                       │      │                  0881fe420f5f55d6bec63bf                                      
│                       │      │                  https://github.com/libexpat/libexpat/pull/1331               
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-76641              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-76641              
│                       │      │                                                                               
│                       │      │                  https://www.vulncheck.com/advisories/expat-out-of-bounds-read
│                       │      │                  -via-dtdcopy                                                 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-20T18:16:51.887Z 
│                       │      ╰ LastModifiedDate: 2026-08-20T19:17:04.43Z 
│                       ├ [39] ╭ VulnerabilityID : CVE-2026-76957 
│                       │      ├ PkgID           : libexpat1@2.7.4-1 
│                       │      ├ PkgName         : libexpat1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libexpat1@2.7.4-1?arch=amd64&distro=ub
│                       │      │                  │       untu-26.04 
│                       │      │                  ╰ UID : c17b9d4b5a8b1286 
│                       │      ├ InstalledVersion: 2.7.4-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-76957 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:efbe947f03dfb27b969dea76b7fae43e328fca1e9368a681d6ba2
│                       │      │                   967fccca5cc 
│                       │      ├ Title           : libexpat: libexpat: Memory corruption vulnerability allows
│                       │      │                   arbitrary code execution or denial of service 
│                       │      ├ Description     : libexpat before 2.8.4 lacks handler call depth tracking with
│                       │      │                    custom encoding callbacks. Thus, a use-after-free can
│                       │      │                   occur. NOTE: this is similar to CVE-2026-50219,
│                       │      │                   CVE-2026-56131 and CVE-2026-56412. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-416
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ amazon: 3 
│                       │      │                  ├ azure : 2 
│                       │      │                  ├ nvd   : 3 
│                       │      │                  ├ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.8 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-76957
│                       │      │                  https://github.com/libexpat/libexpat/pull/1322       
│                       │      │                  https://github.com/libexpat/libexpat/pull/1329       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-76957      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-76957      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-20T05:16:29.747Z 
│                       │      ╰ LastModifiedDate: 2026-09-08T20:56:31.86Z 
│                       ├ [40] ╭ VulnerabilityID : CVE-2026-15588 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-15588 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cf34d952d5534589a67ed1f20573998c2bc4dbb46cf6c51c391a1
│                       │      │                   24f660c3a90 
│                       │      ├ Title           : GDBusServer: glib2: GDBusServer pre-authentication DoS via
│                       │      │                   unbounded SASL line buffering 
│                       │      ├ Description     : A denial-of-service and resource exhaustion vulnerability
│                       │      │                   exists within the `GDBus` component of GLib. The `gdbusauth`
│                       │      │                    authentication mechanism fails to enforce proper length
│                       │      │                   limitations on data lines read from a client. An
│                       │      │                   unauthenticated local or remote attacker can exploit this
│                       │      │                   lack of input validation by sending excessively long streams
│                       │      │                    of data, causing the application to consume massive amounts
│                       │      │                    of system memory and CPU, potentially leading to a crash or
│                       │      │                    system hang. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-770
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.3 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:39985             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:40485             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42329             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-15588        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3985            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/merge_requests/5240    
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/merge_requests/5241    
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-15588.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-15588              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-15588              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-07-20T12:17:55.22Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:17:56.303Z 
│                       ├ [41] ╭ VulnerabilityID : CVE-2026-16118 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-16118 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e79604c81f4f23da450adf3e2d5be1308b4b35ad0288e6a167f6f
│                       │      │                   43f7a8f01b7 
│                       │      ├ Title           : xdgmime: heap-based buffer overflow in
│                       │      │                   _xdg_mime_magic_parse_magic_line() in xdgmimemagic.c 
│                       │      ├ Description     : A flaw was found in xdgmime. A heap-based buffer overflow
│                       │      │                   can be triggered in _xdg_mime_magic_parse_magic_line() in
│                       │      │                   the xdgmimemagic.c file on little-endian systems when an
│                       │      │                   attacker-controlled MIME magic file in a user-writable XDG
│                       │      │                   data location (e.g., in the $XDG_DATA_HOME/mime/magic path)
│                       │      │                   is parsed by an application performing MIME type detection
│                       │      │                   (e.g., via g_content_type_guess()). When performing
│                       │      │                   byte-swap, incorrect pointer arithmetic on the write side
│                       │      │                   causes an out-of-bounds write of 2 bytes, resulting in an
│                       │      │                   application crash or memory corruption. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-122
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.1 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64799             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64800             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66451             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:67956             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-16118        
│                       │      │                  https://bugzilla.redhat.com/2501732                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2501732          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-16118
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-64799.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:64800                
│                       │      │                  https://gitlab.freedesktop.org/xdg/xdgmime/-/work_items/41   
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/work_items/3992        
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-16118.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-66451-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-16118              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-16118              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-07-17T20:17:16.167Z 
│                       │      ╰ LastModifiedDate: 2026-09-21T12:17:09.173Z 
│                       ├ [42] ╭ VulnerabilityID : CVE-2026-58010 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58010 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f10d7057f8e32759853133a68d89d709c892b8bddc5f2a54a0d49
│                       │      │                   89a85790ce4 
│                       │      ├ Title           : glib: buffer over-read in glib/gvariant-serialiser.c via
│                       │      │                   gvs_tuple_is_normal() 
│                       │      ├ Description     : A flaw was found in GLib. An off-by-one error can occur in
│                       │      │                   the gvs_tuple_is_normal function in the
│                       │      │                   glib/gvariant-serialiser.c file when doing an alignment
│                       │      │                   padding check because the bounds check uses > instead of >=,
│                       │      │                    causing an out-of-bounds read of only 1 byte. This issue
│                       │      │                   can cause a minor information disclosure of 1 byte and a
│                       │      │                   denial of service when the out-of-bounds read crosses a page
│                       │      │                    boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-126
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58010        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-m7rp-473c-296x            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3915            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58010.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58010              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58010              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.067Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:02.7Z 
│                       ├ [43] ╭ VulnerabilityID : CVE-2026-58011 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58011 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:feacd5c9c19e17ef7cdef5013d038247003444db3366acfc3a068
│                       │      │                   d303ead0988 
│                       │      ├ Title           : glib: out-of-bounds read in
│                       │      │                   glib/gdatetime.c:g_date_time_get_ymd via invalid GDateTime[
│                       │      │                   m 
│                       │      ├ Description     : A flaw was found in GLib. An out-of-bounds read of only 2
│                       │      │                   bytes can occur in the g_date_time_get_ymd function in the
│                       │      │                   glib/gdatetime.c file when an invalid GDateTime object
│                       │      │                   produced by the g_date_time_add_full function is processed.
│                       │      │                   This flaw can corrupt the date output and potentially cause
│                       │      │                   logic errors that may lead to a denial of service. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-125
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58011        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-8xmh-8wfg-9f6j            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3917            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/work_items/3917        
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58011.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58011              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58011              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.2Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:03Z 
│                       ├ [44] ╭ VulnerabilityID : CVE-2026-58012 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58012 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d8142bd35c34b7865c5eac5e2d05c8305a12cc82b583a46b10464
│                       │      │                   b92247a697d 
│                       │      ├ Title           : glib: buffer over-read in g_regex_replace() via
│                       │      │                   glib/gregex.c:string_append() and g_utf8_next_char() 
│                       │      ├ Description     : A flaw was found in GLib. A buffer over-read can occur in
│                       │      │                   the g_regex_replace function when used with the
│                       │      │                   `G_REGEX_RAW` compile flag and case-change replacement
│                       │      │                   escapes because the string_append function processes matched
│                       │      │                    substrings using UTF-8 functions that assume valid UTF-8
│                       │      │                   input, even when the string is treated as raw bytes. This
│                       │      │                   vulnerability can cause a minor information disclosure of
│                       │      │                   1-5 bytes and a denial of service when the buffer over-read
│                       │      │                   crosses a page boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-126
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58012        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-vwg8-37h9-g38g            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3918            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58012.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58012              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58012              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.33Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:03.29Z 
│                       ├ [45] ╭ VulnerabilityID : CVE-2026-58013 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58013 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4e666906fa8f55515c1df9a70323976805e5e8e6914f3c5eac319
│                       │      │                   6c810a37aab 
│                       │      ├ Title           : glib: buffer over-read in glib/giochannel.c via
│                       │      │                   "g_io_channel_read_line_backend" 
│                       │      ├ Description     : A flaw was found in GLib. A buffer over-read can occur in
│                       │      │                   g_io_channel_read_line_backend() in the giochannel.c file
│                       │      │                   when a custom line terminator with a length greater than one
│                       │      │                    is set, causing memcmp to read past the GString buffer.
│                       │      │                   This vulnerability can cause a minor information disclosure
│                       │      │                   of 7 bytes or a denial of service when the buffer over-read
│                       │      │                   crosses a page boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-126
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58013        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-4x46-h598-64qr            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3925            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58013.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58013              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58013              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.457Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:03.59Z 
│                       ├ [46] ╭ VulnerabilityID : CVE-2026-58014 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58014 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a97469b9a688153cfb94525114e5ece7abf8f3d968e8d5e62c8f4
│                       │      │                   caedc6a3f16 
│                       │      ├ Title           : glib: off-by-one error in glib/gkeyfile.c via
│                       │      │                   "g_key_file_get_locale_string_list" 
│                       │      ├ Description     : A flaw was found in GLib. An off-by-one error can occur in
│                       │      │                   the g_key_file_get_locale_string_list function in the
│                       │      │                   gkeyfile.c file when loading a key file with an empty value.
│                       │      │                    This flaw can cause an out-of-bounds access of 1 byte or a
│                       │      │                   denial of service when the out-of-bounds access crosses a
│                       │      │                   page boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-193
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 3 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.6 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.6 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 7.3 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66357             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58014        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-h88q-m8mm-7243            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3930            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58014.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58014              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58014              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.58Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T12:17:51.327Z 
│                       ├ [47] ╭ VulnerabilityID : CVE-2026-58015 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58015 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b5fe6a5bd347e6ffcea45455a805f22d2b6fbb34e45b03360689d
│                       │      │                   dc001046186 
│                       │      ├ Title           : glib: path traversal in glib/gio/gdbusauthmechanismsha1.c
│                       │      │                   via keyring_lookup_entry and mechanism_client_data_receive[
│                       │      │                   m 
│                       │      ├ Description     : A flaw was found in GLib. The D-Bus client-side
│                       │      │                   implementation of the DBUS_COOKIE_SHA1 SASL authentication
│                       │      │                   mechanism does not validate the cookie_context parameter
│                       │      │                   received from the server. A malicious D-Bus server can
│                       │      │                   supply a cookie_context containing path traversal sequences,
│                       │      │                    causing the client to read an arbitrary file and exfiltrate
│                       │      │                    sensitive data by verifying guessed file contents against a
│                       │      │                    generated hash. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-22
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66357             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58015        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-hmpf-72wc-2r6x            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3931            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58015.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58015              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58015              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.707Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T12:17:51.643Z 
│                       ├ [48] ╭ VulnerabilityID : CVE-2026-58016 
│                       │      ├ PkgID           : libglib2.0-0t64@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-0t64 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-0t64@2.88.0-1?arch=amd64&di
│                       │      │                  │       stro=ubuntu-26.04 
│                       │      │                  ╰ UID : 92324570e14d5870 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58016 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b2aa47c38e9f24bfb9fa4e661d18a6c67b1b9501e3f667129f642
│                       │      │                   900598a1cb8 
│                       │      ├ Title           : glib: integer underflow in gio/gdbusintrospection.c via
│                       │      │                   "g_dbus_node_info_new_for_xml" 
│                       │      ├ Description     : A flaw was found in GLib. A state confusion issue exists in
│                       │      │                   g_dbus_node_info_new_for_xml() in the
│                       │      │                   gio/gdbusintrospection.c file when processing malformed
│                       │      │                   D-Bus introspection XML, specifically with a `node` element
│                       │      │                   nested within other elements like `method`, `signal`,
│                       │      │                   `property` or `arg`. This issue can cause an unsigned
│                       │      │                   integer overflow and lead to an out-of-bounds read,
│                       │      │                   resulting in a denial of service. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-191
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 4 
│                       │      │                  ├ nvd        : 4 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ photon     : 4 
│                       │      │                  ├ redhat     : 3 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 9.1 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 9.1 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42063             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42089             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42090             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:44481             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:46836             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51175             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51176             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51177             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51181             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51182             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51183             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51184             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51185             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:53371             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58016        
│                       │      │                  https://bugzilla.redhat.com/2492257                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492257          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58016
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-42063.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:42089                
│                       │      │                  https://github.com/advisories/GHSA-8rpw-4xx7-27w7            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3932            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58016.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-51183.html         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58016              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58016              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.84Z 
│                       │      ╰ LastModifiedDate: 2026-08-25T10:18:12.017Z 
│                       ├ [49] ╭ VulnerabilityID : CVE-2026-15588 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-15588 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cf2a24f2573720b0fa95557a559e44bada44e01090771e987c2eb
│                       │      │                   f47c3995f0c 
│                       │      ├ Title           : GDBusServer: glib2: GDBusServer pre-authentication DoS via
│                       │      │                   unbounded SASL line buffering 
│                       │      ├ Description     : A denial-of-service and resource exhaustion vulnerability
│                       │      │                   exists within the `GDBus` component of GLib. The `gdbusauth`
│                       │      │                    authentication mechanism fails to enforce proper length
│                       │      │                   limitations on data lines read from a client. An
│                       │      │                   unauthenticated local or remote attacker can exploit this
│                       │      │                   lack of input validation by sending excessively long streams
│                       │      │                    of data, causing the application to consume massive amounts
│                       │      │                    of system memory and CPU, potentially leading to a crash or
│                       │      │                    system hang. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-770
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 5.3 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:39985             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:40485             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42329             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-15588        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3985            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/merge_requests/5240    
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/merge_requests/5241    
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-15588.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-15588              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-15588              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-07-20T12:17:55.22Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:17:56.303Z 
│                       ├ [50] ╭ VulnerabilityID : CVE-2026-16118 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-16118 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e34966c049fc854c12ef4a8057e6bfbfaa64afd466e43db286b2e
│                       │      │                   085833b4144 
│                       │      ├ Title           : xdgmime: heap-based buffer overflow in
│                       │      │                   _xdg_mime_magic_parse_magic_line() in xdgmimemagic.c 
│                       │      ├ Description     : A flaw was found in xdgmime. A heap-based buffer overflow
│                       │      │                   can be triggered in _xdg_mime_magic_parse_magic_line() in
│                       │      │                   the xdgmimemagic.c file on little-endian systems when an
│                       │      │                   attacker-controlled MIME magic file in a user-writable XDG
│                       │      │                   data location (e.g., in the $XDG_DATA_HOME/mime/magic path)
│                       │      │                   is parsed by an application performing MIME type detection
│                       │      │                   (e.g., via g_content_type_guess()). When performing
│                       │      │                   byte-swap, incorrect pointer arithmetic on the write side
│                       │      │                   causes an out-of-bounds write of 2 bytes, resulting in an
│                       │      │                   application crash or memory corruption. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-122
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:N/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.1 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64799             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64800             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66451             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:67956             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-16118        
│                       │      │                  https://bugzilla.redhat.com/2501732                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2501732          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-16118
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-64799.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:64800                
│                       │      │                  https://gitlab.freedesktop.org/xdg/xdgmime/-/work_items/41   
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/work_items/3992        
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-16118.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-66451-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-16118              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-16118              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-07-17T20:17:16.167Z 
│                       │      ╰ LastModifiedDate: 2026-09-21T12:17:09.173Z 
│                       ├ [51] ╭ VulnerabilityID : CVE-2026-58010 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58010 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:eedea0cdbf75bbc026fcbd4b03167a7018e10ec87edf6d10d2161
│                       │      │                   c49085880d9 
│                       │      ├ Title           : glib: buffer over-read in glib/gvariant-serialiser.c via
│                       │      │                   gvs_tuple_is_normal() 
│                       │      ├ Description     : A flaw was found in GLib. An off-by-one error can occur in
│                       │      │                   the gvs_tuple_is_normal function in the
│                       │      │                   glib/gvariant-serialiser.c file when doing an alignment
│                       │      │                   padding check because the bounds check uses > instead of >=,
│                       │      │                    causing an out-of-bounds read of only 1 byte. This issue
│                       │      │                   can cause a minor information disclosure of 1 byte and a
│                       │      │                   denial of service when the out-of-bounds read crosses a page
│                       │      │                    boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-126
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58010        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-m7rp-473c-296x            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3915            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58010.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58010              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58010              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.067Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:02.7Z 
│                       ├ [52] ╭ VulnerabilityID : CVE-2026-58011 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58011 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5381f16206860a26e27e52b26c5a70228cb80a09faa8dc9a0ee93
│                       │      │                   a56a336c294 
│                       │      ├ Title           : glib: out-of-bounds read in
│                       │      │                   glib/gdatetime.c:g_date_time_get_ymd via invalid GDateTime[
│                       │      │                   m 
│                       │      ├ Description     : A flaw was found in GLib. An out-of-bounds read of only 2
│                       │      │                   bytes can occur in the g_date_time_get_ymd function in the
│                       │      │                   glib/gdatetime.c file when an invalid GDateTime object
│                       │      │                   produced by the g_date_time_add_full function is processed.
│                       │      │                   This flaw can corrupt the date output and potentially cause
│                       │      │                   logic errors that may lead to a denial of service. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-125
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58011        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-8xmh-8wfg-9f6j            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3917            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/work_items/3917        
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58011.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58011              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58011              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.2Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:03Z 
│                       ├ [53] ╭ VulnerabilityID : CVE-2026-58012 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58012 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:187502ce088deab4ee9642d3b832df5252147defe572166a57c30
│                       │      │                   027e3b6e49a 
│                       │      ├ Title           : glib: buffer over-read in g_regex_replace() via
│                       │      │                   glib/gregex.c:string_append() and g_utf8_next_char() 
│                       │      ├ Description     : A flaw was found in GLib. A buffer over-read can occur in
│                       │      │                   the g_regex_replace function when used with the
│                       │      │                   `G_REGEX_RAW` compile flag and case-change replacement
│                       │      │                   escapes because the string_append function processes matched
│                       │      │                    substrings using UTF-8 functions that assume valid UTF-8
│                       │      │                   input, even when the string is treated as raw bytes. This
│                       │      │                   vulnerability can cause a minor information disclosure of
│                       │      │                   1-5 bytes and a denial of service when the buffer over-read
│                       │      │                   crosses a page boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-126
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58012        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-vwg8-37h9-g38g            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3918            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58012.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58012              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58012              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.33Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:03.29Z 
│                       ├ [54] ╭ VulnerabilityID : CVE-2026-58013 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58013 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7c2513fbd39d74095fd3aa7247e9805045db625cc4eb8d6490543
│                       │      │                   231996a4c78 
│                       │      ├ Title           : glib: buffer over-read in glib/giochannel.c via
│                       │      │                   "g_io_channel_read_line_backend" 
│                       │      ├ Description     : A flaw was found in GLib. A buffer over-read can occur in
│                       │      │                   g_io_channel_read_line_backend() in the giochannel.c file
│                       │      │                   when a custom line terminator with a length greater than one
│                       │      │                    is set, causing memcmp to read past the GString buffer.
│                       │      │                   This vulnerability can cause a minor information disclosure
│                       │      │                   of 7 bytes or a denial of service when the buffer over-read
│                       │      │                   crosses a page boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-126
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.2 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 6.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58013        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-4x46-h598-64qr            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3925            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58013.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58013              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58013              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.457Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:18:03.59Z 
│                       ├ [55] ╭ VulnerabilityID : CVE-2026-58014 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58014 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:848cd533b9f6cb5e3f469c57a8ebbe836530d3f673575bb6be9e1
│                       │      │                   85d00626abb 
│                       │      ├ Title           : glib: off-by-one error in glib/gkeyfile.c via
│                       │      │                   "g_key_file_get_locale_string_list" 
│                       │      ├ Description     : A flaw was found in GLib. An off-by-one error can occur in
│                       │      │                   the g_key_file_get_locale_string_list function in the
│                       │      │                   gkeyfile.c file when loading a key file with an empty value.
│                       │      │                    This flaw can cause an out-of-bounds access of 1 byte or a
│                       │      │                   denial of service when the out-of-bounds access crosses a
│                       │      │                   page boundary. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-193
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 3 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.6 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 8.6 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 7.3 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66357             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58014        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-h88q-m8mm-7243            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3930            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58014.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58014              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58014              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.58Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T12:17:51.327Z 
│                       ├ [56] ╭ VulnerabilityID : CVE-2026-58015 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58015 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:58dd1d5ba0ada8e7d2e5911e1a682d7e029883594a1628dec1c05
│                       │      │                   d165a74bc99 
│                       │      ├ Title           : glib: path traversal in glib/gio/gdbusauthmechanismsha1.c
│                       │      │                   via keyring_lookup_entry and mechanism_client_data_receive[
│                       │      │                   m 
│                       │      ├ Description     : A flaw was found in GLib. The D-Bus client-side
│                       │      │                   implementation of the DBUS_COOKIE_SHA1 SASL authentication
│                       │      │                   mechanism does not validate the cookie_context parameter
│                       │      │                   received from the server. A malicious D-Bus server can
│                       │      │                   supply a cookie_context containing path traversal sequences,
│                       │      │                    causing the client to read an arbitrary file and exfiltrate
│                       │      │                    sensitive data by verifying guessed file contents against a
│                       │      │                    generated hash. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-22
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 3 
│                       │      │                  ├ nvd        : 3 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ photon     : 3 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 7.5 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:55440             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:57015             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61766             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63135             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63138             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:63140             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65762             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65763             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65767             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65768             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65769             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65770             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65771             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:65773             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66357             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58015        
│                       │      │                  https://bugzilla.redhat.com/2492243                          
│                       │      │                  https://bugzilla.redhat.com/2492245                          
│                       │      │                  https://bugzilla.redhat.com/2492247                          
│                       │      │                  https://bugzilla.redhat.com/2492248                          
│                       │      │                  https://bugzilla.redhat.com/2492255                          
│                       │      │                  https://bugzilla.redhat.com/2492256                          
│                       │      │                  https://bugzilla.redhat.com/2499675                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492243          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492245          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492247          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492248          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492255          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492256          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2499675          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-15588
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58010
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58011
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58012
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58013
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58014
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58015
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-57015.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:55440                
│                       │      │                  https://github.com/advisories/GHSA-hmpf-72wc-2r6x            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3931            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58015.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61766-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58015              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58015              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.707Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T12:17:51.643Z 
│                       ├ [57] ╭ VulnerabilityID : CVE-2026-58016 
│                       │      ├ PkgID           : libglib2.0-data@2.88.0-1 
│                       │      ├ PkgName         : libglib2.0-data 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libglib2.0-data@2.88.0-1?arch=all&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : ef55ca0cc473e830 
│                       │      ├ InstalledVersion: 2.88.0-1 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-58016 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:56795cc3f6638295efe3f2aceb9c95e09cf285e3c3a237e3da5d1
│                       │      │                   fe3be86aedb 
│                       │      ├ Title           : glib: integer underflow in gio/gdbusintrospection.c via
│                       │      │                   "g_dbus_node_info_new_for_xml" 
│                       │      ├ Description     : A flaw was found in GLib. A state confusion issue exists in
│                       │      │                   g_dbus_node_info_new_for_xml() in the
│                       │      │                   gio/gdbusintrospection.c file when processing malformed
│                       │      │                   D-Bus introspection XML, specifically with a `node` element
│                       │      │                   nested within other elements like `method`, `signal`,
│                       │      │                   `property` or `arg`. This issue can cause an unsigned
│                       │      │                   integer overflow and lead to an out-of-bounds read,
│                       │      │                   resulting in a denial of service. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-191
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ amazon     : 3 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ julia      : 4 
│                       │      │                  ├ nvd        : 4 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ photon     : 4 
│                       │      │                  ├ redhat     : 3 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 9.1 
│                       │      │                  ├ nvd    ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 9.1 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42063             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42089             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:42090             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:44481             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:46836             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49512             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51175             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51176             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51177             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51181             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51182             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51183             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51184             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:51185             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:53371             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-58016        
│                       │      │                  https://bugzilla.redhat.com/2492257                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2492257          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-58016
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-42063.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:42089                
│                       │      │                  https://github.com/advisories/GHSA-8rpw-4xx7-27w7            
│                       │      │                  https://gitlab.gnome.org/GNOME/glib/-/issues/3932            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-58016.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-51183.html         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-58016              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-58016              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-30T13:19:17.84Z 
│                       │      ╰ LastModifiedDate: 2026-08-25T10:18:12.017Z 
│                       ├ [58] ╭ VulnerabilityID : CVE-2026-13757 
│                       │      ├ PkgID           : libp11-kit0@0.26.2-2 
│                       │      ├ PkgName         : libp11-kit0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libp11-kit0@0.26.2-2?arch=amd64&distro
│                       │      │                  │       =ubuntu-26.04 
│                       │      │                  ╰ UID : 39936f33632ab742 
│                       │      ├ InstalledVersion: 0.26.2-2 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-13757 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:81b38f45c9a6613a1d89acce8b6aa6e41f97c839f701c59218bbd
│                       │      │                   fd7641ed31d 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-674
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ azure      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 6.2 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:37469             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:38342             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49667             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49668             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:53371             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:54387             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:54760             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:58981             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-13757        
│                       │      │                  https://bugzilla.redhat.com/2494556                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2494556          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-13757
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-49668.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:49667                
│                       │      │                  https://github.com/advisories/GHSA-p2wm-69qx-x25w            
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-13757.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-49668.html         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-13757              
│                       │      │                  https://ubuntu.com/security/notices/USN-8687-1               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-13757              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-06-29T19:16:40.907Z 
│                       │      ╰ LastModifiedDate: 2026-09-01T13:18:10.253Z 
│                       ├ [59] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libsystemd0@259.5-0ubuntu3.4 
│                       │      ├ PkgName         : libsystemd0 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libsystemd0@259.5-0ubuntu3.4?arch=amd6
│                       │      │                  │       4&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 8e41c7d584057e32 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9f29b8b059852e15097dbb393cce0d09d258f4cb35d50be4365ec
│                       │      │                   5e73039f1d4 
│                       │      ├ Title           : systemd: systemd-journald: Unintended output to user
│                       │      │                   terminals via logger command 
│                       │      ├ Description     : In systemd 259, systemd-journald can send ANSI escape
│                       │      │                   sequences to the terminals of arbitrary users when a "logger
│                       │      │                    -p emerg" command is executed, if ForwardToWall=yes is
│                       │      │                   set. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-669
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ nvd   : 1 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 3.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 2.9 
│                       │      ├ References                                                               
│                       │      │                  ────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/05/05/1 
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-40228   
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-40228         
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-40228         
│                       │      │                  https://www.openwall.com/lists/oss-security/2026/04/08/1
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-10T16:16:33.753Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:44:53.31Z 
│                       ├ [60] ╭ VulnerabilityID : CVE-2026-40228 
│                       │      ├ PkgID           : libudev1@259.5-0ubuntu3.4 
│                       │      ├ PkgName         : libudev1 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libudev1@259.5-0ubuntu3.4?arch=amd64&d
│                       │      │                  │       istro=ubuntu-26.04 
│                       │      │                  ╰ UID : db6ded6155f534fe 
│                       │      ├ InstalledVersion: 259.5-0ubuntu3.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-40228 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5d366f457cc8855c585b32ed7f0a060fbdff5f8d4330a1502882d
│                       │      │                   9eb9fc3a8ef 
│                       │      ├ Title           : systemd: systemd-journald: Unintended output to user
│                       │      │                   terminals via logger command 
│                       │      ├ Description     : In systemd 259, systemd-journald can send ANSI escape
│                       │      │                   sequences to the terminals of arbitrary users when a "logger
│                       │      │                    -p emerg" command is executed, if ForwardToWall=yes is
│                       │      │                   set. 
│                       │      ├ Severity        : LOW 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-669
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ nvd   : 1 
│                       │      │                  ├ redhat: 1 
│                       │      │                  ╰ ubuntu: 1 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 3.3 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:N/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 2.9 
│                       │      ├ References                                                               
│                       │      │                  ────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/05/05/1 
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-40228   
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-40228         
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-40228         
│                       │      │                  https://www.openwall.com/lists/oss-security/2026/04/08/1
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-10T16:16:33.753Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:44:53.31Z 
│                       ├ [61] ╭ VulnerabilityID : CVE-2026-74860 
│                       │      ├ PkgID           : libxml2-16@2.15.2+dfsg-0.1ubuntu0.1 
│                       │      ├ PkgName         : libxml2-16 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libxml2-16@2.15.2%2Bdfsg-0.1ubuntu0.1?
│                       │      │                  │       arch=amd64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : db080d50b6a8f0f0 
│                       │      ├ InstalledVersion: 2.15.2+dfsg-0.1ubuntu0.1 
│                       │      ├ FixedVersion    : 2.15.2+dfsg-0.1ubuntu0.2 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-74860 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:5c8b5f3ae67fb194a1254487745587f05feef92fd1b8affb99bf8
│                       │      │                   36355cfc075 
│                       │      ├ Title           : libxml2: double-free/UAF in libxml2 Python bindings 
│                       │      ├ Description     : A flaw was found in libxml2 with Python bindings enabled. A
│                       │      │                   remote attacker could exploit this vulnerability by
│                       │      │                   providing a specially crafted XML document containing a
│                       │      │                   Document Type Definition (DTD) with enumerated attribute
│                       │      │                   values. This triggers a double-free error in the SAX
│                       │      │                   attributeDecl callback handler, where a string is freed
│                       │      │                   twice. This flaw can lead to a denial of service (DoS) due
│                       │      │                   to a reproducible crash in Python applications using the
│                       │      │                   libxml2 SAX bindings. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-763
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ azure : 3 
│                       │      │                  ├ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:L/UI:N/S:C/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 8.5 
│                       │      ├ References                                                            
│                       │      │                  ─────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:64463     
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-74860
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2529697  
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-74860      
│                       │      │                  https://ubuntu.com/security/notices/USN-8787-1       
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-74860      
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-08T12:16:58.083Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T20:17:28.66Z 
│                       ├ [62] ╭ VulnerabilityID : CVE-2026-86140 
│                       │      ├ PkgID           : libxml2-16@2.15.2+dfsg-0.1ubuntu0.1 
│                       │      ├ PkgName         : libxml2-16 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/libxml2-16@2.15.2%2Bdfsg-0.1ubuntu0.1?
│                       │      │                  │       arch=amd64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : db080d50b6a8f0f0 
│                       │      ├ InstalledVersion: 2.15.2+dfsg-0.1ubuntu0.1 
│                       │      ├ FixedVersion    : 2.15.2+dfsg-0.1ubuntu0.2 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-86140 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:93325a0a8d7d3f4485df3033f7bdb2cdb5d2dbfbc6812b447876e
│                       │      │                   dd45f3ea4fd 
│                       │      ├ Title           : libxml2: libxml2: Arbitrary code execution via stack-based
│                       │      │                   buffer overflow in xmlSnprintfElements 
│                       │      ├ Description     : In libxml2 before 2.15.4, xmlSnprintfElements in valid.c has
│                       │      │                    a strcat stack-based buffer overflow. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-121
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ azure : 3 
│                       │      │                  ├ nvd   : 3 
│                       │      │                  ├ photon: 4 
│                       │      │                  ├ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ nvd    ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                  │        │           /A:H 
│                       │      │                  │        ╰ V3Score : 7.8 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.4 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-86140        
│                       │      │                  https://github.com/GNOME/libxml2/commit/d1686f91dbda141a75220
│                       │      │                  0419d35639fd6b38340                                          
│                       │      │                  https://github.com/GNOME/libxml2/compare/v2.15.3...v2.15.4   
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-86140              
│                       │      │                                                                               
│                       │      │                  https://ubuntu.com/security/notices/USN-8787-1               
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-86140              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-09-05T05:17:12.877Z 
│                       │      ╰ LastModifiedDate: 2026-09-15T19:39:17.01Z 
│                       ├ [63] ╭ VulnerabilityID : CVE-2026-18374 
│                       │      ├ PkgID           : locales@2.43-2ubuntu2.4 
│                       │      ├ PkgName         : locales 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/locales@2.43-2ubuntu2.4?arch=all&distr
│                       │      │                  │       o=ubuntu-26.04 
│                       │      │                  ╰ UID : 99ee62f19d60b18d 
│                       │      ├ InstalledVersion: 2.43-2ubuntu2.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ef9f22a518b5c6eeaf790d4fa3b47ad82871cb1e2ba2a5c780950
│                       │      │                   a9974ad124d 
│                       │      ├ Title           : glibc: glibc: Heap buffer overflow via attacker-controlled
│                       │      │                   fopen mode string 
│                       │      ├ Description     : Passing an effectively empty string to the `,ccs=` syntax
│                       │      │                   extension of the mode argument in the `fopen` function in
│                       │      │                   the GNU C Library version 2.45 or earlier may result in a
│                       │      │                   heap buffer overflow when the mode string input to the
│                       │      │                   function is attacker controlled.
│                       │      │                   
│                       │      │                   This usage pattern is not seen in applications in common
│                       │      │                   GNU/Linux distributions and applications that process
│                       │      │                   user-supplied values for `ccs` should not pass them through
│                       │      │                   without validation. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-787
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:N/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:L 
│                       │      │                           ╰ V3Score : 4.9 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/08/27/6      
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18374        
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18374              
│                       │      │                  https://sourceware.org/bugzilla/show_bug.cgi?id=34574        
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/G
│                       │      │                  LIBC-SA-2026-0015                                            
│                       │      │                  https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=adviso
│                       │      │                  ries/GLIBC-SA-2026-0015                                      
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18374              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-27T20:17:03.553Z 
│                       │      ╰ LastModifiedDate: 2026-09-03T16:43:15.293Z 
│                       ├ [64] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : login.defs@1:4.17.4-2ubuntu3 
│                       │      ├ PkgName         : login.defs 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/login.defs@4.17.4-2ubuntu3?arch=all&di
│                       │      │                  │       stro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : eaf648d5e4e975f7 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:27bf82f3b154c6fafda735335237c1627816d8d96d030fc05eaa8
│                       │      │                   e3b3f16b748 
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
│                       │      ├ CweIDs                   
│                       │      │                  ────────
│                       │      │                  CWE-1188
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 1 
│                       │      │                  ├ azure      : 1 
│                       │      │                  ├ oracle-oval: 1 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 1 
│                       │      │                  ╰ ubuntu     : 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.6 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2025:20559             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2024-56433        
│                       │      │                  https://bugzilla.redhat.com/2334165                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2334165          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-56433
│                       │      │                  https://errata.almalinux.org/9/ALSA-2025-20559.html          
│                       │      │                  https://errata.rockylinux.org/RLSA-2025:20559                
│                       │      │                  https://github.com/shadow-maint/shadow/blob/e2512d5741d4a44bd
│                       │      │                  d81a8c2d0029b6222728cf0/etc/login.defs#L238-L241             
│                       │      │                  https://github.com/shadow-maint/shadow/issues/1157           
│                       │      │                                                                               
│                       │      │                  https://github.com/shadow-maint/shadow/releases/tag/4.4      
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/cve/CVE-2024-56433.html             
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/errata/ELSA-2025-20559-0.html       
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2024-56433              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2024-56433              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [65] ╭ VulnerabilityID : CVE-2024-56433 
│                       │      ├ PkgID           : passwd@1:4.17.4-2ubuntu3 
│                       │      ├ PkgName         : passwd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/passwd@4.17.4-2ubuntu3?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04&epoch=1 
│                       │      │                  ╰ UID : 12ffbe3e135ac553 
│                       │      ├ InstalledVersion: 1:4.17.4-2ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2024-56433 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f1d12c7da8e83e45bb4abf5645259b2fe2820d7f675d96e5b77f2
│                       │      │                   f6698732b92 
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
│                       │      ├ CweIDs                   
│                       │      │                  ────────
│                       │      │                  CWE-1188
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 1 
│                       │      │                  ├ azure      : 1 
│                       │      │                  ├ oracle-oval: 1 
│                       │      │                  ├ redhat     : 1 
│                       │      │                  ├ rocky      : 1 
│                       │      │                  ╰ ubuntu     : 1 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 3.6 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2025:20559             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2024-56433        
│                       │      │                  https://bugzilla.redhat.com/2334165                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2334165          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-56433
│                       │      │                  https://errata.almalinux.org/9/ALSA-2025-20559.html          
│                       │      │                  https://errata.rockylinux.org/RLSA-2025:20559                
│                       │      │                  https://github.com/shadow-maint/shadow/blob/e2512d5741d4a44bd
│                       │      │                  d81a8c2d0029b6222728cf0/etc/login.defs#L238-L241             
│                       │      │                  https://github.com/shadow-maint/shadow/issues/1157           
│                       │      │                                                                               
│                       │      │                  https://github.com/shadow-maint/shadow/releases/tag/4.4      
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/cve/CVE-2024-56433.html             
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/errata/ELSA-2025-20559-0.html       
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2024-56433              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2024-56433              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2024-12-26T09:15:07.267Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T08:12:10.903Z 
│                       ├ [66] ╭ VulnerabilityID : CVE-2026-35341 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35341 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a313fd64d5e739e8dba1b59566b9f4bb3ec13585eb6623c8c9f1f
│                       │      │                   c86e2eeefc9 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-732
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:N 
│                       │      │                         ╰ V3Score : 7.1 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils                          
│                       │      │                  https://github.com/uutils/coreutils/issues/10020             
│                       │      │                  https://github.com/uutils/coreutils/pull/10376               
│                       │      │                  https://github.com/uutils/coreutils/security/advisories/GHSA-
│                       │      │                  pmf6-rcx4-v53v                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35341              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35341              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.06Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.5Z 
│                       ├ [67] ╭ VulnerabilityID : CVE-2026-35344 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35344 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4a79188523f5f42603837a22484e2f96a87400b891a4a40ad89a7
│                       │      │                   c614040e16b 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-252
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils            
│                       │      │                  https://github.com/uutils/coreutils/issues/9745
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35344
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35344
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.49Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.833Z 
│                       ├ [68] ╭ VulnerabilityID : CVE-2026-35345 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35345 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ffdd3256a238e667024767ed4106e26fd492eb7de00aa00943df9
│                       │      │                   367e7a94318 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-59 
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:L/A:N 
│                       │      │                         ╰ V3Score : 5.3 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10328
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35345 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35345 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:36.627Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:25.943Z 
│                       ├ [69] ╭ VulnerabilityID : CVE-2026-35348 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35348 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:2dfc732b5285a15dd9dfe19f8ef6d9e974b34d4429c9f6595d97b
│                       │      │                   c2ddf79180a 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-248
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:H 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils            
│                       │      │                  https://github.com/uutils/coreutils/issues/9696
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35348
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35348
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.04Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.27Z 
│                       ├ [70] ╭ VulnerabilityID : CVE-2026-35350 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35350 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cda50f251eceaf52b8bfb4aced2bce42043e9576302eceb6f8e86
│                       │      │                   c1fe6ee1667 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-281
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:H/A:L 
│                       │      │                         ╰ V3Score : 6.6 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils            
│                       │      │                  https://github.com/uutils/coreutils/issues/9750
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35350
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35350
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.327Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.48Z 
│                       ├ [71] ╭ VulnerabilityID : CVE-2026-35351 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35351 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7dd09a7e76eab4eff3aa11d1abd67e2c077428118bdf61926137b
│                       │      │                   39ad544027e 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-281
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:H/UI:N/S:U/C:L/I:L/A:L 
│                       │      │                         ╰ V3Score : 4.2 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils            
│                       │      │                  https://github.com/uutils/coreutils/issues/9714
│                       │      │                  https://github.com/uutils/coreutils/pull/11706 
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35351
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35351
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.457Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.587Z 
│                       ├ [72] ╭ VulnerabilityID : CVE-2026-35352 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35352 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:a4c9428c5d612c2a27d6a591a99ff0a0a104740ada2ae489b175d
│                       │      │                   ce29f57939f 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H 
│                       │      │                         ╰ V3Score : 7 
│                       │      ├ References                                                              
│                       │      │                  ───────────────────────────────────────────────────────
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/05/04/4
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/05/04/5
│                       │      │                  http://www.openwall.com/lists/oss-security/2026/05/04/6
│                       │      │                  https://github.com/uutils/coreutils                    
│                       │      │                  https://github.com/uutils/coreutils/issues/10020       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35352        
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35352        
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.597Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.69Z 
│                       ├ [73] ╭ VulnerabilityID : CVE-2026-35354 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35354 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ff8f6eece56af422bfc8d68a49f07fe160b0b57505b2832b01ca9
│                       │      │                   5b24edbee2c 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:N 
│                       │      │                         ╰ V3Score : 4.7 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10014
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35354 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35354 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:37.867Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:26.907Z 
│                       ├ [74] ╭ VulnerabilityID : CVE-2026-35357 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35357 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:8394287f48051c612edfb85c2a0cee17d8378adff297b04f087fc
│                       │      │                   0d7cb60e34c 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N/A:N 
│                       │      │                         ╰ V3Score : 4.7 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10011
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35357 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35357 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.267Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.223Z 
│                       ├ [75] ╭ VulnerabilityID : CVE-2026-35359 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35359 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:858003a450a8cc2669df85e8b795f501703643d58fed4b7aa941d
│                       │      │                   65c91b30aad 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-59 
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:N/A:N 
│                       │      │                         ╰ V3Score : 4.7 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10017
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35359 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35359 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.537Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.437Z 
│                       ├ [76] ╭ VulnerabilityID : CVE-2026-35360 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35360 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bc8465111f6d09cda965d2f9b1a57a2f7c3a8b749e1470990a0ec
│                       │      │                   8184c571c69 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10019
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35360 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35360 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:38.673Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.543Z 
│                       ├ [77] ╭ VulnerabilityID : CVE-2026-35363 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35363 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:9131e5469bee59343cd06dcaf7a14769a71c3b2335361302009ab
│                       │      │                   08ee35eeeda 
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
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-22
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:R/S:U/C:N/I:H/A:L 
│                       │      │                         ╰ V3Score : 5.6 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils                          
│                       │      │                  https://github.com/uutils/coreutils/issues/9749              
│                       │      │                  https://github.com/uutils/coreutils/security/advisories/GHSA-
│                       │      │                  89p7-7cq3-hhr2                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35363              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35363              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.12Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.867Z 
│                       ├ [78] ╭ VulnerabilityID : CVE-2026-35364 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35364 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:df9d85c15cbd46161b35e7614feee3fce44901d891c248a1b3ae3
│                       │      │                   383bb899935 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10015
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35364 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35364 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:39.737Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:27.97Z 
│                       ├ [79] ╭ VulnerabilityID : CVE-2026-35367 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35367 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:b504eded7eacbd2a02ba36a29d07406437b185dae86ff5ed90811
│                       │      │                   bf79e80bbed 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-732
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10021
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35367 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35367 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.423Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.297Z 
│                       ├ [80] ╭ VulnerabilityID : CVE-2026-35368 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35368 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:e482ca43044f435446bf012b3f55c9d4012d13c59a4ec95ca1237
│                       │      │                   39b0f4d567b 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-426
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:C/C:H/I:H/A:H 
│                       │      │                         ╰ V3Score : 7.9 
│                       │      ├ References                                                       
│                       │      │                  ────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils             
│                       │      │                  https://github.com/uutils/coreutils/issues/10327
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35368 
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35368 
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.56Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.4Z 
│                       ├ [81] ╭ VulnerabilityID : CVE-2026-35370 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35370 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:994fa83413d58b21654108240b40dd8686c67801df8668b678dfe
│                       │      │                   857b6f7b415 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-863
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N 
│                       │      │                         ╰ V3Score : 4.4 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils                          
│                       │      │                  https://github.com/uutils/coreutils/issues/10006             
│                       │      │                  https://github.com/uutils/coreutils/security/advisories/GHSA-
│                       │      │                  47c7-qrm7-mqw7                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35370              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35370              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.833Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.613Z 
│                       ├ [82] ╭ VulnerabilityID : CVE-2026-35371 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35371 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:d1b0208205645c0653af8e6df7c9d2deea1a025b4e8b91494a30c
│                       │      │                   185f4f1405a 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-451
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils                          
│                       │      │                  https://github.com/uutils/coreutils/issues/10006             
│                       │      │                  https://github.com/uutils/coreutils/security/advisories/GHSA-
│                       │      │                  xv5w-cw7x-72gj                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35371              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35371              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:40.987Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.723Z 
│                       ├ [83] ╭ VulnerabilityID : CVE-2026-35373 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35373 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:cdbd8e7dcf2973698f0981916cbc08c3eb9845763aa41a74a87c3
│                       │      │                   92b3e60e4de 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-176
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ├ nvd   : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ╭ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:L 
│                       │      │                  │      ╰ V3Score : 3.3 
│                       │      │                  ╰ nvd  ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:H 
│                       │      │                         ╰ V3Score : 5.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils                          
│                       │      │                  https://github.com/uutils/coreutils/pull/11403               
│                       │      │                  https://github.com/uutils/coreutils/security/advisories/GHSA-
│                       │      │                  jcjr-rh8q-7xqf                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35373              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35373              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:41.997Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:28.933Z 
│                       ├ [84] ╭ VulnerabilityID : CVE-2026-35374 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35374 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:ea45889b4526ab9e11bfca4e843ee03274b5c0c434592abe86e46
│                       │      │                   1e99e91a1d0 
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
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:N/S:U/C:N/I:H/A:H 
│                       │      │                         ╰ V3Score : 6.3 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils            
│                       │      │                  https://github.com/uutils/coreutils/pull/11401 
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35374
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35374
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.127Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.04Z 
│                       ├ [85] ╭ VulnerabilityID : CVE-2026-35377 
│                       │      ├ PkgID           : rust-coreutils@0.8.0-0ubuntu3 
│                       │      ├ PkgName         : rust-coreutils 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/rust-coreutils@0.8.0-0ubuntu3?arch=amd
│                       │      │                  │       64&distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 2129e05d8c2e5188 
│                       │      ├ InstalledVersion: 0.8.0-0ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-35377 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:21d9f45785db7af2b88dbbd6ba02a0ef4a84714df4adae3ce9e76
│                       │      │                   010e59e5b31 
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
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-20
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ ghsa  : 1 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N/A:L 
│                       │      │                         ╰ V3Score : 3.3 
│                       │      ├ References                                                      
│                       │      │                  ───────────────────────────────────────────────
│                       │      │                  https://github.com/uutils/coreutils            
│                       │      │                  https://github.com/uutils/coreutils/pull/11512 
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-35377
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-35377
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-04-22T17:16:42.577Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T10:40:29.357Z 
│                       ├ [86] ╭ VulnerabilityID : CVE-2026-82474 
│                       │      ├ PkgID           : sudo@1.9.17p2-1ubuntu3 
│                       │      ├ PkgName         : sudo 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/sudo@1.9.17p2-1ubuntu3?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : b26025a68a135817 
│                       │      ├ InstalledVersion: 1.9.17p2-1ubuntu3 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-82474 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:72ba1140cae52ef46ebce09f7d65135903e0af79eac9a3f9f7b8b
│                       │      │                   b35cd43f410 
│                       │      ├ Title           : sudo: Sudo: Policy bypass allows unauthorized program
│                       │      │                   execution via execveat 
│                       │      ├ Description     : Sudo through 1.9.17p2 fails to apply intercept policy checks
│                       │      │                    to the execveat system call in ptrace-based intercept mode.
│                       │      │                    Users permitted to run specific commands can execute denied
│                       │      │                    programs by calling execveat directly or through fexecve,
│                       │      │                   bypassing policy enforcement and logging. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-693
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 3 
│                       │      │                  ├ azure      : 3 
│                       │      │                  ├ oracle-oval: 3 
│                       │      │                  ├ redhat     : 3 
│                       │      │                  ├ rocky      : 3 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:68692             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-82474        
│                       │      │                  https://bugzilla.redhat.com/2525889                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2525889          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-82474
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-68692.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:68692                
│                       │      │                  https://github.com/sudo-project/sudo                         
│                       │      │                  https://github.com/sudo-project/sudo/blob/v1.9.17p2/src/exec_
│                       │      │                  ptrace.c                                                     
│                       │      │                  https://github.com/sudo-project/sudo/commit/71fbe42dcd5a1c8f7
│                       │      │                  99540583a2dfb2ae6221edf                                      
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-82474.html             
│                       │      │                                                                               
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-68692.html         
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-82474              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-82474              
│                       │      │                                                                               
│                       │      │                  https://www.vulncheck.com/advisories/sudo-through-1.9-17p2-in
│                       │      │                  tercept-policy-bypass-via-execveat                           
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-29T17:17:59.91Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T19:54:25.81Z 
│                       ├ [87] ╭ VulnerabilityID : CVE-2026-18477 
│                       │      ├ PkgID           : tar@1.35+dfsg-4ubuntu0.4 
│                       │      ├ PkgName         : tar 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-4ubuntu0.4?arch=amd64&
│                       │      │                  │       distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 5867f93e7d45b368 
│                       │      ├ InstalledVersion: 1.35+dfsg-4ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18477 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:f37160efa54a138334b90ed6776eb3ad6e40b5960b7e80dbb790c
│                       │      │                   2c02a497c0c 
│                       │      ├ Title           : tar: tar: TOCTOU in incremental dumpdir 'X' rename handling
│                       │      │                   allows restore path escape 
│                       │      ├ Description     : A TOCTOU (Time-of-Check Time-of-Use) vulnerability in GNU
│                       │      │                   tar's incremental dumpdir 'X' rename handling allows a local
│                       │      │                    attacker with write access to a directory being backed up
│                       │      │                   to influence the restore process if the attacker has access
│                       │      │                   to the system where the restore is being performed. During
│                       │      │                   restoration, files or directories may be created, renamed or
│                       │      │                    overwritten outside the intended extraction directory. This
│                       │      │                    could lead to unauthorized file modification or, in some
│                       │      │                   cases, privilege escalation. Exploitation does not require
│                       │      │                   the attacker to modify or craft the archive, and standard
│                       │      │                   backup and restore workflows—including extracting into a
│                       │      │                   newly created directory without using the -P option do not
│                       │      │                   mitigate the issue. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-367
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ julia      : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ╭ julia  ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:R/S:U/C:N/I:H
│                       │      │                  │        │           /A:N 
│                       │      │                  │        ╰ V3Score : 4.4 
│                       │      │                  ╰ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:H/PR:L/UI:R/S:U/C:N/I:H
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.4 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:49361             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61581             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61586             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18477        
│                       │      │                  https://bugzilla.redhat.com/2455360                          
│                       │      │                  https://bugzilla.redhat.com/2509735                          
│                       │      │                  https://bugzilla.redhat.com/2509843                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2455360          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2509735          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2509843          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-18477
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-18508
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-5704 
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-61586.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:61581                
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-18477.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61586-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18477              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18477              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-03T17:16:33.897Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:17:56.97Z 
│                       ├ [88] ╭ VulnerabilityID : CVE-2026-18508 
│                       │      ├ PkgID           : tar@1.35+dfsg-4ubuntu0.4 
│                       │      ├ PkgName         : tar 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/tar@1.35%2Bdfsg-4ubuntu0.4?arch=amd64&
│                       │      │                  │       distro=ubuntu-26.04 
│                       │      │                  ╰ UID : 5867f93e7d45b368 
│                       │      ├ InstalledVersion: 1.35+dfsg-4ubuntu0.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-18508 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c22ae967caf9ec1a5fbf85216f76f9fdaab857340ffa4a4b8194a
│                       │      │                   27a96f6c9a0 
│                       │      ├ Title           : tar: tar: --one-top-level hardlink targets not confined to
│                       │      │                   top-level directory enabling arbitrary file overwrite 
│                       │      ├ Description     : A flaw was found in GNU tar. When extracting an archive with
│                       │      │                    the --one-top-level option, hardlink targets are not
│                       │      │                   confined to the designated top-level directory and may
│                       │      │                   resolve relative to the extraction working directory. A
│                       │      │                   crafted archive can create hardlinks that escape the
│                       │      │                   intended boundary and, when combined with a preexisting
│                       │      │                   symbolic link under the working directory, may allow writing
│                       │      │                    outside that boundary during a single extraction. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-59
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ alma       : 2 
│                       │      │                  ├ oracle-oval: 2 
│                       │      │                  ├ redhat     : 2 
│                       │      │                  ├ rocky      : 2 
│                       │      │                  ╰ ubuntu     : 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:L/I:L
│                       │      │                           │           /A:N 
│                       │      │                           ╰ V3Score : 4.4 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:50807             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61581             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61586             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:61783             
│                       │      │                  https://access.redhat.com/errata/RHSA-2026:66018             
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-18508        
│                       │      │                  https://bugzilla.redhat.com/2455360                          
│                       │      │                  https://bugzilla.redhat.com/2509735                          
│                       │      │                  https://bugzilla.redhat.com/2509843                          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2455360          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2509735          
│                       │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2509843          
│                       │      │                  https://creativecommons.org/licenses/by/4.0/                 
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-18477
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-18508
│                       │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-5704 
│                       │      │                  https://errata.almalinux.org/10/ALSA-2026-61586.html         
│                       │      │                  https://errata.rockylinux.org/RLSA-2026:61581                
│                       │      │                  https://linux.oracle.com/cve/CVE-2026-18508.html             
│                       │      │                  https://linux.oracle.com/errata/ELSA-2026-61586-0.html       
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-18508              
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-18508              
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-03T16:16:28.387Z 
│                       │      ╰ LastModifiedDate: 2026-09-10T18:17:57.193Z 
│                       ├ [89] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : vim@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.2141-1ubuntu4.9?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 6e374df7a1985f8 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:87b75c507a56b33c1173e7d6a66a1828908c62ea301537ff78f96
│                       │      │                   65e0ed6b431 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-401
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51400        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:38:03.09Z 
│                       ├ [90] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : vim@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim@9.1.2141-1ubuntu4.9?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 6e374df7a1985f8 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:97aebb9279f018c7072180d3b0cd57806633b9cf5e6b0714dd673
│                       │      │                   032778df98a 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-94
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51401        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://github.com/vim/vim                                   
│                       │      │                                                                               
│                       │      │                  https://github.com/vim/vim/blob/master/src/os_vms.c          
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:33:02.03Z 
│                       ├ [91] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : vim-common@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.2141-1ubuntu4.9?arch=al
│                       │      │                  │       l&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 4cd34c507280bdb3 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:7bb1145162dd813fdb3d43217d7ee2d57c85ee938d003747bb3c3
│                       │      │                   dcf52a02005 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-401
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51400        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:38:03.09Z 
│                       ├ [92] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : vim-common@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-common@9.1.2141-1ubuntu4.9?arch=al
│                       │      │                  │       l&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 4cd34c507280bdb3 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:bf81c5b34503bcb5493f1431f300f25993676027cc44ec0cf84c4
│                       │      │                   3e39980b6e3 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-94
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51401        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://github.com/vim/vim                                   
│                       │      │                                                                               
│                       │      │                  https://github.com/vim/vim/blob/master/src/os_vms.c          
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:33:02.03Z 
│                       ├ [93] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : vim-runtime@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : vim-runtime 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.2141-1ubuntu4.9?arch=a
│                       │      │                  │       ll&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 7b05671a44d4cf47 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:c92f62f90600dd34986c0092520f3a22b6463d4fe8a60becfdf11
│                       │      │                   52e0a5a4750 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-401
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51400        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:38:03.09Z 
│                       ├ [94] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : vim-runtime@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : vim-runtime 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/vim-runtime@9.1.2141-1ubuntu4.9?arch=a
│                       │      │                  │       ll&distro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : 7b05671a44d4cf47 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:42a5d7e538a04e43a08a2ed55457ce42e024c30418c74e427b6f3
│                       │      │                   0302c800ecc 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-94
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51401        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://github.com/vim/vim                                   
│                       │      │                                                                               
│                       │      │                  https://github.com/vim/vim/blob/master/src/os_vms.c          
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:33:02.03Z 
│                       ├ [95] ╭ VulnerabilityID : CVE-2021-31879 
│                       │      ├ PkgID           : wget@1.25.0-2ubuntu4.4 
│                       │      ├ PkgName         : wget 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/wget@1.25.0-2ubuntu4.4?arch=amd64&dist
│                       │      │                  │       ro=ubuntu-26.04 
│                       │      │                  ╰ UID : af1ec1b586d3a1cd 
│                       │      ├ InstalledVersion: 1.25.0-2ubuntu4.4 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2021-31879 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:4aa9685e43b75f9cc25121357a6ad709956733895fbddcd6f9ce4
│                       │      │                   08aeb24c2e4 
│                       │      ├ Title           : wget: authorization header disclosure on redirect 
│                       │      ├ Description     : GNU Wget through 1.21.1 does not omit the Authorization
│                       │      │                   header upon a redirect to a different origin, a related
│                       │      │                   issue to CVE-2018-1000007. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-601
│                       │      │                  
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
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2021-31879        
│                       │      │                  https://mail.gnu.org/archive/html/bug-wget/2021-02/msg00002.h
│                       │      │                  tml                                                          
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2021-31879              
│                       │      │                                                                               
│                       │      │                  https://savannah.gnu.org/bugs/?56909                         
│                       │      │                                                                               
│                       │      │                  https://security.netapp.com/advisory/ntap-20210618-0002/     
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2021-31879              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2021-04-29T05:15:08.707Z 
│                       │      ╰ LastModifiedDate: 2026-06-17T03:52:23.987Z 
│                       ├ [96] ╭ VulnerabilityID : CVE-2026-51400 
│                       │      ├ PkgID           : xxd@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.2141-1ubuntu4.9?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : c2c7a877f47b35cf 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51400 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:84b78efcb2a40582898a30696dd6fa0e2b36608f7b4a8da143abd
│                       │      │                   987777c1a03 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                  
│                       │      │                  ───────
│                       │      │                  CWE-401
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 2 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.5 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51400        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51400              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.433Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:38:03.09Z 
│                       ├ [97] ╭ VulnerabilityID : CVE-2026-51401 
│                       │      ├ PkgID           : xxd@2:9.1.2141-1ubuntu4.9 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/xxd@9.1.2141-1ubuntu4.9?arch=amd64&dis
│                       │      │                  │       tro=ubuntu-26.04&epoch=2 
│                       │      │                  ╰ UID : c2c7a877f47b35cf 
│                       │      ├ InstalledVersion: 2:9.1.2141-1ubuntu4.9 
│                       │      ├ Status          : affected 
│                       │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                       │      │                  │         bb22a540f6cb4c5edad4 
│                       │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                       │      │                            a394f2090d37bfc108d4 
│                       │      ├ SeveritySource  : ubuntu 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-51401 
│                       │      ├ DataSource       ╭ ID  : ubuntu 
│                       │      │                  ├ Name: Ubuntu CVE Tracker 
│                       │      │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                       │      ├ Fingerprint     : sha256:3e3d1e40b5106b0ad3da1607c8a39eb666f8da8b66b6e61a62a32
│                       │      │                   4fa1985a97c 
│                       │      ├ Title           : vim: Vim: Arbitrary code execution via vms_fixfilename()
│                       │      │                   function 
│                       │      ├ Description     : An issue in Vim Project v9.2.0389 and earlier allows a local
│                       │      │                    attacker to execute arbitrary code via the
│                       │      │                   vms_fixfilename() function within file vim/src/os_vms.c 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs                 
│                       │      │                  ──────
│                       │      │                  CWE-94
│                       │      │                  
│                       │      ├ VendorSeverity   ╭ redhat: 3 
│                       │      │                  ╰ ubuntu: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 7.8 
│                       │      ├ References                                                                    
│                       │      │                  ─────────────────────────────────────────────────────────────
│                       │      │                  https://access.redhat.com/security/cve/CVE-2026-51401        
│                       │      │                  https://gist.github.com/jiejiaodedengdai/ff5d34a523167e09b7d8
│                       │      │                  330cc9f5d4e5#file-vim-os_vms-cves-md                         
│                       │      │                  https://github.com/vim/vim                                   
│                       │      │                                                                               
│                       │      │                  https://github.com/vim/vim/blob/master/src/os_vms.c          
│                       │      │                                                                               
│                       │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  https://www.cve.org/CVERecord?id=CVE-2026-51401              
│                       │      │                                                                               
│                       │      │                  
│                       │      ├ PublishedDate   : 2026-08-04T21:16:36.567Z 
│                       │      ╰ LastModifiedDate: 2026-09-04T13:33:02.03Z 
│                       ╰ [98] ╭ VulnerabilityID : CVE-2026-85091 
│                              ├ PkgID           : zlib1g@1:1.3.dfsg+really1.3.1-1ubuntu3.1 
│                              ├ PkgName         : zlib1g 
│                              ├ PkgIdentifier    ╭ PURL: pkg:deb/ubuntu/zlib1g@1.3.dfsg%2Breally1.3.1-1ubuntu3
│                              │                  │       .1?arch=amd64&distro=ubuntu-26.04&epoch=1 
│                              │                  ╰ UID : a4f0bcc5ee12eaad 
│                              ├ InstalledVersion: 1:1.3.dfsg+really1.3.1-1ubuntu3.1 
│                              ├ Status          : affected 
│                              ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
│                              │                  │         bb22a540f6cb4c5edad4 
│                              │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
│                              │                            a394f2090d37bfc108d4 
│                              ├ SeveritySource  : ubuntu 
│                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-85091 
│                              ├ DataSource       ╭ ID  : ubuntu 
│                              │                  ├ Name: Ubuntu CVE Tracker 
│                              │                  ╰ URL : https://git.launchpad.net/ubuntu-cve-tracker 
│                              ├ Fingerprint     : sha256:610cbe2bfe060d0a105f27078dc25ec7c0855c8be71c6ecd7ba2f
│                              │                   b73de739447 
│                              ├ Title           : zlib versions 1.3.1.2 through 1.3.2 contain a heap buffer
│                              │                   overflow vul ... 
│                              ├ Description     : zlib versions 1.3.1.2 through 1.3.2 contain a heap buffer
│                              │                   overflow vulnerability in the gz_vacate() function when
│                              │                   processing non-blocking gzwrite() operations with stale
│                              │                   external buffer pointers. Attackers can trigger the overflow
│                              │                    by calling gzprintf() or gzvprintf() after a write stall,
│                              │                   causing an unchecked memmove() to write beyond the internal
│                              │                   input buffer boundary. 
│                              ├ Severity        : MEDIUM 
│                              ├ CweIDs                  
│                              │                  ───────
│                              │                  CWE-787
│                              │                  
│                              ├ VendorSeverity   ─ ubuntu: 2 
│                              ├ References                                                                    
│                              │                  ─────────────────────────────────────────────────────────────
│                              │                  https://gist.github.com/thesmartshadow/e0b9481792afb7c31e86fe
│                              │                  e1ff084490                                                   
│                              │                  https://github.com/madler/zlib                               
│                              │                                                                               
│                              │                  https://github.com/madler/zlib/blob/v1.3.2/gzwrite.c#L393    
│                              │                                                                               
│                              │                  https://www.cve.org/CVERecord?id=CVE-2026-85091              
│                              │                                                                               
│                              │                  https://www.vulncheck.com/advisories/zlib-1.3.1.2-through-1.3
│                              │                  .2-heap-buffer-overflow-via-gz-vacate                        
│                              │                  
│                              ├ PublishedDate   : 2026-09-03T13:06:20.573Z 
│                              ╰ LastModifiedDate: 2026-09-09T20:41:07.123Z 
├ [1] ╭ Target  : Java 
│     ├ Class   : lang-pkgs 
│     ├ Type    : jar 
│     ╰ Packages 
╰ [2] ╭ Target         : usr/bin/pebble 
      ├ Class          : lang-pkgs 
      ├ Type           : gobinary 
      ├ Packages        
      ╰ Vulnerabilities ╭ [0]  ╭ VulnerabilityID : GHSA-w67g-5rqw-f597 
                        │      ├ PkgID           : github.com/gorilla/websocket@v1.5.1 
                        │      ├ PkgName         : github.com/gorilla/websocket 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/github.com/gorilla/websocket@v1.5.1 
                        │      │                  ╰ UID : 13db0ba03ae70421 
                        │      ├ InstalledVersion: v1.5.1 
                        │      ├ FixedVersion    : 1.5.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ SeveritySource  : ghsa 
                        │      ├ PrimaryURL      : https://github.com/advisories/GHSA-w67g-5rqw-f597 
                        │      ├ DataSource       ╭ ID  : ghsa 
                        │      │                  ├ Name: GitHub Security Advisory Go 
                        │      │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+e
                        │      │                          cosystem%3Ago 
                        │      ├ Fingerprint     : sha256:5721a2fdf0566bb0205380b72035f9257c4bfcf849a226e8e3fe4
                        │      │                   da74151b5b8 
                        │      ├ Title           : Gorilla WebSocket Uses Cryptographically Weak PRNG for
                        │      │                   WebSocket Mask Key 
                        │      ├ Description     : gorilla/websocket used `math/rand` (cryptographically weak
                        │      │                   pseudo-random number generator) to generate WebSocket frame
                        │      │                   mask keys prior to commit d67f4185. WebSocket masking keys
                        │      │                   MUST be unpredictable to prevent frame content injection
                        │      │                   attacks. math/rand produces deterministic output when seeded
                        │      │                    with a known value, enabling an attacker to predict or
                        │      │                   recover mask keys and inject content into WebSocket
                        │      │                   connections.
                        │      │                   
                        │      │                   **Type:** Use of Cryptographically Weak Pseudo-Random Number
                        │      │                    Generator
                        │      │                   **Fix:** Replaced math/rand with crypto/rand (commit
                        │      │                   d67f4185, released in v1.5.3)
                        │      │                   **Credit:** bounty-hunter v6.0 silent-fix detection 
                        │      ├ Severity        : MEDIUM 
                        │      ├ VendorSeverity   ─ ghsa: 2 
                        │      ├ CVSS             ─ ghsa ╭ V40Vector: CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:L/VI
                        │      │                         │            :L/VA:N/SC:N/SI:N/SA:N 
                        │      │                         ╰ V40Score : 6.9 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://github.com/canolgun-commits/websocket                
                        │      │                  https://github.com/canolgun-commits/websocket/security/adviso
                        │      │                  ries/GHSA-w67g-5rqw-f597                                     
                        │      │                  https://github.com/gorilla/websocket/commit/d67f41855da42d7bc
                        │      │                  cd9ef050c49f7e54e783b95                                      
                        │      │                  https://github.com/gorilla/websocket/releases/tag/v1.5.3     
                        │      │                                                                               
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-24T21:00:54Z 
                        │      ╰ LastModifiedDate: 2026-08-24T21:00:54Z 
                        ├ [1]  ╭ VulnerabilityID : CVE-2026-25681 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5029
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-25681 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:427a09c42cfab641aee7db1967a2810a7bd02291a2c45741c8513
                        │      │                   faa58ef28c5 
                        │      ├ Title           : golang.org/x/net/html: golang.org/x/net/html: Arbitrary code
                        │      │                    execution via Cross-Site Scripting 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                   
                        │      │                  ────────
                        │      │                  CWE-1021
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 8.1 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34357             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67138             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-25681        
                        │      │                  https://bugzilla.redhat.com/2466505                          
                        │      │                  https://bugzilla.redhat.com/2466507                          
                        │      │                  https://bugzilla.redhat.com/2467822                          
                        │      │                  https://bugzilla.redhat.com/2480756                          
                        │      │                  https://bugzilla.redhat.com/2480761                          
                        │      │                  https://bugzilla.redhat.com/2484207                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480757          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480761          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480762          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484830          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-25681
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-27136
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-41178
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42502
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-34357.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:67138                
                        │      │                  https://go.dev/cl/781703                                     
                        │      │                  https://go.dev/issue/79574                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-25681.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-67139-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-25681              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5029                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-25681              
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:19.863Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [2]  ╭ VulnerabilityID : CVE-2026-27136 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5030
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-27136 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:9e06dae0b31c6511a6f532f6676f2a03aed57be7de4986fb0889c
                        │      │                   e73c7b33883 
                        │      ├ Title           : golang.org/x/net/html: golang: golang.org/x/net/html:
                        │      │                   Cross-Site Scripting via HTML parsing bypass 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                   
                        │      │                  ────────
                        │      │                  CWE-1021
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 8.1 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37123             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67138             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-27136        
                        │      │                  https://bugzilla.redhat.com/2480680                          
                        │      │                  https://bugzilla.redhat.com/2480681                          
                        │      │                  https://bugzilla.redhat.com/2480685                          
                        │      │                  https://bugzilla.redhat.com/2480688                          
                        │      │                  https://bugzilla.redhat.com/2480757                          
                        │      │                  https://bugzilla.redhat.com/2480761                          
                        │      │                  https://bugzilla.redhat.com/2493620                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480757          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480761          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480762          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484830          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-25681
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-27136
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-41178
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42502
                        │      │                  https://errata.almalinux.org/9/ALSA-2026-37123.html          
                        │      │                  https://errata.rockylinux.org/RLSA-2026:67138                
                        │      │                  https://go.dev/cl/781685                                     
                        │      │                  https://go.dev/issue/79575                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-27136.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-67139-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-27136              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5030                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-27136              
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.087Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [3]  ╭ VulnerabilityID : CVE-2026-33814 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-4918
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.53.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ SeveritySource  : nvd 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-33814 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:dc20e0179ff0814a11d9d565882fcebc29eccfd6658e8bfd76238
                        │      │                   5e419682bb2 
                        │      ├ Title           : net/http/internal/http2: golang: golang.org/x/net: Go
                        │      │                   HTTP/2: Denial of Service via malformed
                        │      │                   SETTINGS_MAX_FRAME_SIZE frame 
                        │      ├ Description     : When processing HTTP/2 SETTINGS frames, transport will enter
                        │      │                    an infinite loop of writing CONTINUATION frames if it
                        │      │                   receives a SETTINGS_MAX_FRAME_SIZE with a value of 0. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-835
                        │      │                  CWE-606
                        │      │                  
                        │      ├ VendorSeverity   ╭ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ nvd        : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ├ rocky      : 3 
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
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:22112             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:22120             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:22121             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:23262             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:23264             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33120             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33123             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33142             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33150             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34342             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37387             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42644             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43692             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:49702             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:49712             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:50205             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54274             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54283             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54284             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54285             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54286             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54287             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56854             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56912             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57191             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57194             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57365             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57367             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57408             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57545             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57649             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57845             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59833             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60023             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60025             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60441             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60442             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60446             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60447             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60454             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60477             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60478             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60520             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60668             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:61253             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:62410             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:62550             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:62551             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63046             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63047             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63048             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63050             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63091             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63096             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63097             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63103             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63104             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63636             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63637             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63639             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65126             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66350             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-33814        
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467809          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467810          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467811          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467813          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467822          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467823          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467825          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467826          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467827          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33811
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33814
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39817
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39819
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39820
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39823
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39825
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39826
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39836
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42499
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42501
                        │      │                  https://errata.rockylinux.org/RLSA-2026:22121                
                        │      │                  https://github.com/golang/go/issues/78476                    
                        │      │                  https://go-review.googlesource.com/c/go/+/761581             
                        │      │                  https://go-review.googlesource.com/c/net/+/761640            
                        │      │                  https://go.dev/cl/761581                                     
                        │      │                  https://go.dev/cl/761640                                     
                        │      │                  https://go.dev/issue/78476                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/qcCIEXso47M    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-33814.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-22121.html         
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-33814              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-4918                         
                        │      │                  https://security.access.redhat.com/data/csaf/v2/vex/2026/cve-
                        │      │                  2026-33814.json                                              
                        │      │                  https://ubuntu.com/security/notices/USN-8430-1               
                        │      │                                                                               
                        │      │                  https://ubuntu.com/security/notices/USN-8471-1               
                        │      │                                                                               
                        │      │                  https://ubuntu.com/security/notices/USN-8472-1               
                        │      │                                                                               
                        │      │                  https://ubuntu.com/security/notices/USN-8473-1               
                        │      │                                                                               
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-33814              
                        │      │                                                                               
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-07T20:16:42.88Z 
                        │      ╰ LastModifiedDate: 2026-09-18T13:17:59.293Z 
                        ├ [4]  ╭ VulnerabilityID : CVE-2026-39821 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5026
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39821 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:1115b4cc9942b520882f71d4419f4e711ebfa2f457f16c09251e4
                        │      │                   e5fae355b1c 
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
                        │      ├ CweIDs                   
                        │      │                  ────────
                        │      │                  CWE-1289
                        │      │                  
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
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:23262             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:23264             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:26546             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:26547             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30650             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30651             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30853             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30854             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30855             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33155             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33160             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33163             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33173             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33183             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33524             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33531             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34342             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34357             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34359             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34364             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34789             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35826             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35827             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35828             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35829             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35830             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35831             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35993             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35994             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36105             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36167             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36207             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36648             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36651             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36796             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36797             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36808             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36820             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36883             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37387             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37435             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37436             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:38995             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:39005             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:39573             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:39879             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:40118             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:40262             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:40945             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41019             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41030             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41031             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41036             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41055             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41066             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41928             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41930             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42043             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42047             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42048             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42049             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42050             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42051             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42078             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42079             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42080             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42082             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42132             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42142             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42146             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42150             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42151             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42240             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42644             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42796             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42852             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43038             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43052             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43692             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:44622             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:44624             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:46395             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47149             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47735             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47737             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47952             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:49702             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:49712             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:50300             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:50843             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51033             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51112             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51187             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51194             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51341             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:52826             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53374             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53412             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53413             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53415             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53530             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54191             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54274             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54283             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54284             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54285             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54286             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54287             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54395             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54401             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54435             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54441             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54531             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54580             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54757             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56143             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56223             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56340             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56431             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57194             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57541             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57649             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57845             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59546             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59549             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59562             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60315             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60354             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60387             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60520             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:61245             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:61253             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:62549             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63134             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65126             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65153             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65359             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65534             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65851             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65886             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66016             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66022             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66350             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66432             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67149             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67159             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67160             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67287             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67319             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67517             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:68504             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-39821        
                        │      │                  https://bugzilla.redhat.com/2480756                          
                        │      │                  https://bugzilla.redhat.com/2484207                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456333          
                        │      │                  CWE-787                                                      
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467809          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467822          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480756          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484204          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515827          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515838          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515840          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32280
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32281
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33811
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39820
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39821
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42499
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42504
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56853
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56858
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56859
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-46395.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:65886                
                        │      │                  https://github.com/golang/go/issues/78760                    
                        │      │                  https://go.dev/cl/767220                                     
                        │      │                  https://go.dev/issue/78760                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-39821.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-66432-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-39821              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5026                         
                        │      │                  https://security.access.redhat.com/data/csaf/v2/vex/2026/cve-
                        │      │                  2026-39821.json                                              
                        │      │                  https://ubuntu.com/security/notices/USN-8416-1               
                        │      │                                                                               
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-39821              
                        │      │                                                                               
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.41Z 
                        │      ╰ LastModifiedDate: 2026-09-17T12:18:05.767Z 
                        ├ [5]  ╭ VulnerabilityID : CVE-2026-46600 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5942
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.56.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46600 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:1335a8b925bf073fe3a33ea9cddbce2e46eb3e409cdfebb15e6f4
                        │      │                   12a0e5c4620 
                        │      ├ Title           : golang.org/x/net/dns/dnsmessage:
                        │      │                   golang.org/x/net/dns/dnsmessage: Denial of Service via
                        │      │                   invalid DNS record parsing 
                        │      ├ Description     : Parsing an invalid SVCB or HTTPS RR can panic when the size
                        │      │                   of a parameter value overflows the message buffer. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-125
                        │      │                  
                        │      ├ VendorSeverity   ╭ azure  : 2 
                        │      │                  ├ bitnami: 3 
                        │      │                  ╰ redhat : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-46600    
                        │      │                  https://go.dev/cl/786345                                 
                        │      │                  https://go.dev/issue/79795                               
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-46600          
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5942                     
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-46600          
                        │      │                  
                        │      ├ PublishedDate   : 2026-07-21T20:17:01.213Z 
                        │      ╰ LastModifiedDate: 2026-08-14T16:16:55.673Z 
                        ├ [6]  ╭ VulnerabilityID : CVE-2025-47911 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-4440
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.45.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ SeveritySource  : nvd 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-47911 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:f2ccad2d131f351feef494ea80e85f8a8acb0141e8940c0068d67
                        │      │                   2b8a9208cce 
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
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/security/cve/CVE-2025-47911    
                        │      │                  https://github.com/golang/go/issues/75682                
                        │      │                  https://github.com/golang/vulndb/issues/4440             
                        │      │                  https://go.dev/cl/709876                                 
                        │      │                  https://groups.google.com/g/golang-announce/c/jnQcOYpiR2c
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2025-47911          
                        │      │                  https://pkg.go.dev/vuln/GO-2026-4440                     
                        │      │                  https://ubuntu.com/security/notices/USN-8089-1           
                        │      │                  https://ubuntu.com/security/notices/USN-8089-2           
                        │      │                  https://ubuntu.com/security/notices/USN-8089-3           
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2025-47911          
                        │      │                  
                        │      ├ PublishedDate   : 2026-02-05T18:16:09.893Z 
                        │      ╰ LastModifiedDate: 2026-06-17T09:28:50.07Z 
                        ├ [7]  ╭ VulnerabilityID : CVE-2025-58190 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-4441
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.45.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ SeveritySource  : nvd 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2025-58190 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:401396ee72e82b8e961aa8c2ed927e63725a56bf98bf82e28e65e
                        │      │                   cf3d349e909 
                        │      ├ Title           : golang.org/x/net/html: Infinite parsing loop in
                        │      │                   golang.org/x/net 
                        │      ├ Description     : The html.Parse function in golang.org/x/net/html has an
                        │      │                   infinite parsing loop when processing certain inputs, which
                        │      │                   can lead to denial of service (DoS) if an attacker provides
                        │      │                   specially crafted HTML content. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-835
                        │      │                  
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
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/security/cve/CVE-2025-58190    
                        │      │                  https://github.com/golang/go/issues/70179                
                        │      │                  https://github.com/golang/vulndb/issues/4441             
                        │      │                  https://go.dev/cl/709875                                 
                        │      │                  https://groups.google.com/g/golang-announce/c/jnQcOYpiR2c
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2025-58190          
                        │      │                  https://pkg.go.dev/vuln/GO-2026-4441                     
                        │      │                  https://ubuntu.com/security/notices/USN-8089-1           
                        │      │                  https://ubuntu.com/security/notices/USN-8089-2           
                        │      │                  https://ubuntu.com/security/notices/USN-8089-3           
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2025-58190          
                        │      │                  
                        │      ├ PublishedDate   : 2026-02-05T18:16:10.027Z 
                        │      ╰ LastModifiedDate: 2026-06-17T09:44:02.557Z 
                        ├ [8]  ╭ VulnerabilityID : CVE-2026-25680 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5028
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-25680 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:9c266855a421d850cbfeab3e56d8a69636cb2a335c62c1bed3dba
                        │      │                   4d6f23d01f1 
                        │      ├ Title           : golang.org/x/net/html: golang.org/x/net/html: Denial of
                        │      │                   Service due to excessive HTML parsing 
                        │      ├ Description     : Parsing arbitrary HTML can consume excessive CPU time,
                        │      │                   possibly leading to denial of service. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-400
                        │      │                  
                        │      ├ VendorSeverity   ╭ amazon: 3 
                        │      │                  ├ azure : 2 
                        │      │                  ╰ redhat: 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:N/I:N
                        │      │                           │           /A:H 
                        │      │                           ╰ V3Score : 6.5 
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-25680    
                        │      │                  https://go.dev/cl/781702                                 
                        │      │                  https://go.dev/issue/79573                               
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-25680          
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5028                     
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-25680          
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:19.753Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [9]  ╭ VulnerabilityID : CVE-2026-42502 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5027
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42502 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:0a5e66257f3f025bf87aa15bc50e39699820522da39c97d1d0ee3
                        │      │                   dc224dfad85 
                        │      ├ Title           : golang.org/x/net/html: golang: golang.org/x/net/html:
                        │      │                   Cross-Site Scripting via unexpected HTML tree rendering 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs                   
                        │      │                  ────────
                        │      │                  CWE-1021
                        │      │                  
                        │      ├ VendorSeverity   ╭ amazon     : 3 
                        │      │                  ├ azure      : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ redhat     : 2 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 6.1 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67138             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-42502        
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480757          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480761          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480762          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484830          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-25681
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-27136
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-41178
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42502
                        │      │                  https://errata.rockylinux.org/RLSA-2026:67138                
                        │      │                  https://go.dev/cl/781701                                     
                        │      │                  https://go.dev/issue/79572                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-42502.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-67139-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-42502              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5027                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-42502              
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.587Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [10] ╭ VulnerabilityID : CVE-2026-42506 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5025
                        │      │                  
                        │      ├ PkgID           : golang.org/x/net@v0.40.0 
                        │      ├ PkgName         : golang.org/x/net 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/net@v0.40.0 
                        │      │                  ╰ UID : b8870a94f706b324 
                        │      ├ InstalledVersion: v0.40.0 
                        │      ├ FixedVersion    : 0.55.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42506 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:e7dd115fce4978ed2069555f43ad43c450476d55cc4309cb076ff
                        │      │                   2dd4a12c1b4 
                        │      ├ Title           : golang.org/x/net/html: golang.org/x/net/html: Cross-Site
                        │      │                   Scripting (XSS) via arbitrary HTML parsing 
                        │      ├ Description     : Parsing arbitrary HTML which is then rendered using Render
                        │      │                   can result in an unexpected HTML tree. This can be leveraged
                        │      │                    to execute XSS attacks in applications that attempt to
                        │      │                   sanitize input HTML before rendering. 
                        │      ├ Severity        : MEDIUM 
                        │      ├ CweIDs                 
                        │      │                  ──────
                        │      │                  CWE-79
                        │      │                  
                        │      ├ VendorSeverity   ╭ amazon: 3 
                        │      │                  ├ azure : 2 
                        │      │                  ╰ redhat: 2 
                        │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:L/I:L
                        │      │                           │           /A:N 
                        │      │                           ╰ V3Score : 5.4 
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-42506    
                        │      │                  https://go.dev/cl/781700                                 
                        │      │                  https://go.dev/issue/79571                               
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-42506          
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5025                     
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-42506          
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.803Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [11] ╭ VulnerabilityID : CVE-2026-39824 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5024
                        │      │                  
                        │      ├ PkgID           : golang.org/x/sys@v0.33.0 
                        │      ├ PkgName         : golang.org/x/sys 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/golang.org/x/sys@v0.33.0 
                        │      │                  ╰ UID : a350d4cc028089d4 
                        │      ├ InstalledVersion: v0.33.0 
                        │      ├ FixedVersion    : 0.44.0 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39824 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:e3739dfee74f29a700362f336d8fe728fa833509a7e77ce57e0fc
                        │      │                   0b55d6771d3 
                        │      ├ Title           : Invoking integer overflow in NewNTUnicodeString in
                        │      │                   golang.org/x/sys/windows 
                        │      ├ Description     : NewNTUnicodeString does not check for string length
                        │      │                   overflow. When provided with a string that overflows the
                        │      │                   maximum size of a NTUnicodeString (a 16-bit number of
                        │      │                   bytes), it returns a truncated string rather than an
                        │      │                   error. 
                        │      ├ Severity        : UNKNOWN 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-190
                        │      │                  
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://go.dev/cl/770080                                 
                        │      │                  https://go.dev/issue/78916                               
                        │      │                  https://groups.google.com/g/golang-announce/c/6MMI8Lj-Atg
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5024                     
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T20:16:33.057Z 
                        │      ╰ LastModifiedDate: 2026-07-23T16:10:00.137Z 
                        ├ [12] ╭ VulnerabilityID : CVE-2026-33818 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5972
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-33818 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:c23662312fc334c38d248dd060b4ca6723948c0f0c2f16106bde2
                        │      │                   45941503889 
                        │      ├ Title           : encoding/asn1: golang: Go encoding/asn1: Denial of Service
                        │      │                   via excessive recursion in Unmarshal 
                        │      ├ Description     : Enforce a recursion limit in Unmarshal to prevent stack
                        │      │                   exhaustion when parsing deeply-nested, recursive
                        │      │                   structures. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-400
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65116             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66364             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-33818        
                        │      │                  https://bugzilla.redhat.com/2467809                          
                        │      │                  https://bugzilla.redhat.com/2467820                          
                        │      │                  https://bugzilla.redhat.com/2484204                          
                        │      │                  https://bugzilla.redhat.com/2484830                          
                        │      │                  https://bugzilla.redhat.com/2515815                          
                        │      │                  https://bugzilla.redhat.com/2515820                          
                        │      │                  https://bugzilla.redhat.com/2515827                          
                        │      │                  https://bugzilla.redhat.com/2515838                          
                        │      │                  https://bugzilla.redhat.com/2515839                          
                        │      │                  https://bugzilla.redhat.com/2515840                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-65116.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:66364                
                        │      │                  https://go.dev/cl/814980                                     
                        │      │                  https://go.dev/issue/80405                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-33818.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-67161-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-33818              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5972                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-33818              
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-13T22:17:19.84Z 
                        │      ╰ LastModifiedDate: 2026-09-03T16:37:52.17Z 
                        ├ [13] ╭ VulnerabilityID : CVE-2026-39821 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5026
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39821 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:b4b60ab0709b756a753c8e75c36cd53eaf33234eda8369cf081ac
                        │      │                   0cc5770da72 
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
                        │      ├ CweIDs                   
                        │      │                  ────────
                        │      │                  CWE-1289
                        │      │                  
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
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:23262             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:23264             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:26546             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:26547             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30650             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30651             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30853             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30854             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:30855             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33155             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33160             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33163             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33173             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33183             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33524             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:33531             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34342             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34357             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34359             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34364             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:34789             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35826             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35827             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35828             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35829             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35830             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35831             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35993             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:35994             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36105             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36167             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36207             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36648             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36651             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36796             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36797             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36808             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36820             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:36883             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37387             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37435             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:37436             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:38995             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:39005             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:39573             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:39879             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:40118             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:40262             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:40945             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41019             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41030             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41031             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41036             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41055             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41066             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41928             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:41930             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42043             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42047             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42048             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42049             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42050             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42051             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42078             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42079             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42080             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42082             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42132             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42142             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42146             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42150             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42151             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42240             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42644             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42796             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:42852             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43038             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43052             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:43692             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:44622             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:44624             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:46395             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47149             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47735             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47737             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:47952             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:49702             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:49712             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:50300             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:50843             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51033             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51112             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51187             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51194             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:51341             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:52826             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53374             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53412             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53413             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53415             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:53530             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54191             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54274             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54283             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54284             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54285             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54286             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54287             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54395             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54401             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54435             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54441             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54531             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54580             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:54757             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56143             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56223             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56340             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:56431             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57194             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57541             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57649             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:57845             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59546             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59549             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:59562             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60315             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60354             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60387             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:60520             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:61245             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:61253             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:62549             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:63134             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65126             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65153             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65359             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65534             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65851             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65886             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66016             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66022             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66350             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66432             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67149             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67159             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67160             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67287             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67319             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:67517             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:68504             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-39821        
                        │      │                  https://bugzilla.redhat.com/2480756                          
                        │      │                  https://bugzilla.redhat.com/2484207                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456333          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456339          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467809          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467822          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480756          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484204          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515827          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515838          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515840          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32280
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32281
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33811
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39820
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39821
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42499
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42504
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56853
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56858
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56859
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-46395.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:65886                
                        │      │                  https://github.com/golang/go/issues/78760                    
                        │      │                  https://go.dev/cl/767220                                     
                        │      │                  https://go.dev/issue/78760                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://groups.google.com/g/golang-announce/c/iI-mYSI0lu8    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-39821.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-66432-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-39821              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5026                         
                        │      │                  https://security.access.redhat.com/data/csaf/v2/vex/2026/cve-
                        │      │                  2026-39821.json                                              
                        │      │                  https://ubuntu.com/security/notices/USN-8416-1               
                        │      │                                                                               
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-39821              
                        │      │                                                                               
                        │      │                  
                        │      ├ PublishedDate   : 2026-05-22T16:16:20.41Z 
                        │      ╰ LastModifiedDate: 2026-09-17T12:18:05.767Z 
                        ├ [14] ╭ VulnerabilityID : CVE-2026-39822 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-4970
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.12, 1.26.5, 1.27.0-rc.2 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-39822 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:e025b26a22e012efad18c98245276c64c51f725b3558115fa4a3f
                        │      │                   9f3a615058d 
                        │      ├ Title           : golang: Go os.Root: Symlink following vulnerability allows
                        │      │                   directory traversal 
                        │      ├ Description     : On Unix systems, opening a file in an os.Root improperly
                        │      │                   follows symlinks to locations outside of the Root when the
                        │      │                   final path component of the a path is a symbolic link and
                        │      │                   the path ends in /. For example, 'root.Open("symlink/")'
                        │      │                   will open "symlink" even when "symlink" is a symbolic link
                        │      │                   pointing outside of the root. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                 
                        │      │                  ──────
                        │      │                  CWE-61
                        │      │                  
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
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:38495             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:38878             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-39822        
                        │      │                  https://bugzilla.redhat.com/2498152                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2498152          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39822
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-38495.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:38878                
                        │      │                  https://go.dev/cl/797880                                     
                        │      │                  https://go.dev/issue/79005                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/OrmQE_Yp5Sc    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-39822.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-38995.html         
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-39822              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-4970                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-39822              
                        │      │                  
                        │      ├ PublishedDate   : 2026-07-08T17:17:21.31Z 
                        │      ╰ LastModifiedDate: 2026-09-17T17:10:20.047Z 
                        ├ [15] ╭ VulnerabilityID : CVE-2026-46600 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-5942
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-46600 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:f8f6fda3c1ff2a3329142039355b37780f9e215d7365a0521ea54
                        │      │                   1f5c5514dd9 
                        │      ├ Title           : golang.org/x/net/dns/dnsmessage:
                        │      │                   golang.org/x/net/dns/dnsmessage: Denial of Service via
                        │      │                   invalid DNS record parsing 
                        │      ├ Description     : Parsing an invalid SVCB or HTTPS RR can panic when the size
                        │      │                   of a parameter value overflows the message buffer. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-125
                        │      │                  
                        │      ├ VendorSeverity   ╭ azure  : 2 
                        │      │                  ├ bitnami: 3 
                        │      │                  ╰ redhat : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                
                        │      │                  ─────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-46600    
                        │      │                  https://go.dev/cl/786345                                 
                        │      │                  https://go.dev/issue/79795                               
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-46600          
                        │      │                  https://pkg.go.dev/vuln/GO-2026-5942                     
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-46600          
                        │      │                  
                        │      ├ PublishedDate   : 2026-07-21T20:17:01.213Z 
                        │      ╰ LastModifiedDate: 2026-08-14T16:16:55.673Z 
                        ├ [16] ╭ VulnerabilityID : CVE-2026-56853 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-6089
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56853 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:6a65d67cc2340f0554d47f6911f285f4bcad036af5bcc9c1dd1c0
                        │      │                   75a45826b23 
                        │      ├ Title           : net/http: golang: Go net/http: Unencrypted HTTP/2
                        │      │                   connections vulnerable to Denial of Service 
                        │      ├ Description     : When a server is configured to support unencrypted HTTP/2,
                        │      │                   it reads a few bytes from each new connection to see if they
                        │      │                    contain the HTTP/2 client preface. ReadHeaderTimeout is
                        │      │                   unexpectedly not being applied when doing this. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-770
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65116             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65886             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-56853        
                        │      │                  https://bugzilla.redhat.com/2467809                          
                        │      │                  https://bugzilla.redhat.com/2467820                          
                        │      │                  https://bugzilla.redhat.com/2484204                          
                        │      │                  https://bugzilla.redhat.com/2484830                          
                        │      │                  https://bugzilla.redhat.com/2515815                          
                        │      │                  https://bugzilla.redhat.com/2515820                          
                        │      │                  https://bugzilla.redhat.com/2515827                          
                        │      │                  https://bugzilla.redhat.com/2515838                          
                        │      │                  https://bugzilla.redhat.com/2515839                          
                        │      │                  https://bugzilla.redhat.com/2515840                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456333          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456339          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467809          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467822          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480756          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484204          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515827          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515838          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515840          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32280
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32281
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33811
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39820
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39821
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42499
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42504
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56853
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56858
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56859
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-65116.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:65886                
                        │      │                  https://go.dev/cl/795540                                     
                        │      │                  https://go.dev/issue/80205                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-56853.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-65895-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56853              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-6089                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56853              
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.093Z 
                        │      ╰ LastModifiedDate: 2026-09-03T16:37:52.17Z 
                        ├ [17] ╭ VulnerabilityID : CVE-2026-56858 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-6091
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56858 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:097acfba5ff49a764a2852ffd7402faad786b7d5c8981c5d58963
                        │      │                   99d3d474798 
                        │      ├ Title           : html/template: golang: Go html/template: Cross-Site
                        │      │                   Scripting via pathological input 
                        │      ├ Description     : Previously, pathological inputs could close an unescaped '/'
                        │      │                    early, allowing for attack-controlled data to inject
                        │      │                   arbitrary content, potentially leading to XSS. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                 
                        │      │                  ──────
                        │      │                  CWE-79
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ bitnami    : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 2 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:
                        │      │                  │         │           L/A:N 
                        │      │                  │         ╰ V3Score : 6.1 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:
                        │      │                            │           H/A:N 
                        │      │                            ╰ V3Score : 8.1 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65116             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65886             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-56858        
                        │      │                  https://bugzilla.redhat.com/2467809                          
                        │      │                  https://bugzilla.redhat.com/2467820                          
                        │      │                  https://bugzilla.redhat.com/2484204                          
                        │      │                  https://bugzilla.redhat.com/2484830                          
                        │      │                  https://bugzilla.redhat.com/2515815                          
                        │      │                  https://bugzilla.redhat.com/2515820                          
                        │      │                  https://bugzilla.redhat.com/2515827                          
                        │      │                  https://bugzilla.redhat.com/2515838                          
                        │      │                  https://bugzilla.redhat.com/2515839                          
                        │      │                  https://bugzilla.redhat.com/2515840                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456333          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456339          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467809          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467822          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480756          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484204          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515827          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515838          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515840          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32280
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32281
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33811
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39820
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39821
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42499
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42504
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56853
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56858
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56859
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-65116.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:65886                
                        │      │                  https://go.dev/cl/807100                                     
                        │      │                  https://go.dev/issue/80435                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-56858.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-65895-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56858              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-6091                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56858              
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.207Z 
                        │      ╰ LastModifiedDate: 2026-09-03T16:37:52.17Z 
                        ├ [18] ╭ VulnerabilityID : CVE-2026-56859 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-6088
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56859 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:854b10dad8708725049a756482fae867164e826f19ee497f19857
                        │      │                   a6b52c98127 
                        │      ├ Title           : encoding/xml: golang: Go: Denial of Service via XML decoding
                        │      │                    recursion depth issue 
                        │      ├ Description     : Previously, DecodeElement would reset the depth counter
                        │      │                   causing it to never fire; this could lead to stack
                        │      │                   exhaustion. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-770
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65116             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65886             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-56859        
                        │      │                  https://bugzilla.redhat.com/2467809                          
                        │      │                  https://bugzilla.redhat.com/2467820                          
                        │      │                  https://bugzilla.redhat.com/2484204                          
                        │      │                  https://bugzilla.redhat.com/2484830                          
                        │      │                  https://bugzilla.redhat.com/2515815                          
                        │      │                  https://bugzilla.redhat.com/2515820                          
                        │      │                  https://bugzilla.redhat.com/2515827                          
                        │      │                  https://bugzilla.redhat.com/2515838                          
                        │      │                  https://bugzilla.redhat.com/2515839                          
                        │      │                  https://bugzilla.redhat.com/2515840                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456333          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2456339          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467809          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2467822          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2480756          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2484204          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515827          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515838          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515840          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32280
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-32281
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33811
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39820
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-39821
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42499
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42504
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56853
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56858
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56859
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-65116.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:65886                
                        │      │                  https://go.dev/cl/803320                                     
                        │      │                  https://go.dev/issue/80481                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-56859.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-69099.html         
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56859              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-6088                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56859              
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.32Z 
                        │      ╰ LastModifiedDate: 2026-09-03T16:37:52.17Z 
                        ├ [19] ╭ VulnerabilityID : CVE-2026-56860 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-6218
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56860 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:b4702bb8ba17dd5d38286ef468cbbf3123c9199fab171da767e39
                        │      │                   258dc937d6e 
                        │      ├ Title           : net/url: golang: golang net/url: Denial of Service from
                        │      │                   quadratic complexity in path resolution 
                        │      ├ Description     : Previously, resolving relative paths containing parent
                        │      │                   directory ('..') segments performed string conversions and
                        │      │                   buffer rewrites on each step, resulting in quadratic time
                        │      │                   complexity and high memory allocation overhead. Now, path
                        │      │                   resolution operates on a byte buffer using index-based
                        │      │                   backtracking for '..' segments, eliminating the quadratic
                        │      │                   time complexity and significantly reducing memory
                        │      │                   allocations. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-407
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ bitnami    : 2 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 2 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 5.9 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65116             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66364             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-56860        
                        │      │                  https://bugzilla.redhat.com/2467809                          
                        │      │                  https://bugzilla.redhat.com/2467820                          
                        │      │                  https://bugzilla.redhat.com/2484204                          
                        │      │                  https://bugzilla.redhat.com/2484830                          
                        │      │                  https://bugzilla.redhat.com/2515815                          
                        │      │                  https://bugzilla.redhat.com/2515820                          
                        │      │                  https://bugzilla.redhat.com/2515827                          
                        │      │                  https://bugzilla.redhat.com/2515838                          
                        │      │                  https://bugzilla.redhat.com/2515839                          
                        │      │                  https://bugzilla.redhat.com/2515840                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-65116.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:66364                
                        │      │                  https://go.dev/cl/803681                                     
                        │      │                  https://go.dev/issue/80494                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-56860.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-69099.html         
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56860              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-6218                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56860              
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.44Z 
                        │      ╰ LastModifiedDate: 2026-09-03T16:37:52.17Z 
                        ├ [20] ╭ VulnerabilityID : CVE-2026-56862 
                        │      ├ VendorIDs                    
                        │      │                  ────────────
                        │      │                  GO-2026-6090
                        │      │                  
                        │      ├ PkgID           : stdlib@v1.26.4 
                        │      ├ PkgName         : stdlib 
                        │      ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                        │      │                  ╰ UID : 364846ec8fe81bdc 
                        │      ├ InstalledVersion: v1.26.4 
                        │      ├ FixedVersion    : 1.25.13, 1.26.6, 1.27.0-rc.3 
                        │      ├ Status          : fixed 
                        │      ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                        │      │                  │         bb22a540f6cb4c5edad4 
                        │      │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                        │      │                            a394f2090d37bfc108d4 
                        │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-56862 
                        │      ├ DataSource       ╭ ID  : govulndb 
                        │      │                  ├ Name: The Go Vulnerability Database 
                        │      │                  ╰ URL : https://pkg.go.dev/vuln/ 
                        │      ├ Fingerprint     : sha256:7d95f652d9a1732aa32b627497b576b1c8c10bb65978699fc0863
                        │      │                   99714796e39 
                        │      ├ Title           : crypto/tls: golang: Golang crypto/tls: Denial of Service via
                        │      │                    indefinite KeyUpdate messages 
                        │      ├ Description     : Handshake messages, such as KeyUpdate, are always considered
                        │      │                    as state-advancing, regardless of whether a handshake has
                        │      │                   been completed or not. As a result, a malicious client can
                        │      │                   keep sending KeyUpdate messages to force the server to keep
                        │      │                   performing key derivation operations indefinitely. 
                        │      ├ Severity        : HIGH 
                        │      ├ CweIDs                  
                        │      │                  ───────
                        │      │                  CWE-770
                        │      │                  
                        │      ├ VendorSeverity   ╭ alma       : 3 
                        │      │                  ├ amazon     : 3 
                        │      │                  ├ bitnami    : 3 
                        │      │                  ├ oracle-oval: 3 
                        │      │                  ├ photon     : 3 
                        │      │                  ├ redhat     : 3 
                        │      │                  ╰ rocky      : 3 
                        │      ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                  │         │           N/A:H 
                        │      │                  │         ╰ V3Score : 7.5 
                        │      │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:
                        │      │                            │           N/A:H 
                        │      │                            ╰ V3Score : 7.5 
                        │      ├ References                                                                    
                        │      │                  ─────────────────────────────────────────────────────────────
                        │      │                  https://access.redhat.com/errata/RHSA-2026:65116             
                        │      │                  https://access.redhat.com/errata/RHSA-2026:66364             
                        │      │                  https://access.redhat.com/security/cve/CVE-2026-56862        
                        │      │                  https://bugzilla.redhat.com/2467809                          
                        │      │                  https://bugzilla.redhat.com/2467820                          
                        │      │                  https://bugzilla.redhat.com/2484204                          
                        │      │                  https://bugzilla.redhat.com/2484830                          
                        │      │                  https://bugzilla.redhat.com/2515815                          
                        │      │                  https://bugzilla.redhat.com/2515820                          
                        │      │                  https://bugzilla.redhat.com/2515827                          
                        │      │                  https://bugzilla.redhat.com/2515838                          
                        │      │                  https://bugzilla.redhat.com/2515839                          
                        │      │                  https://bugzilla.redhat.com/2515840                          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515815          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515820          
                        │      │                  https://bugzilla.redhat.com/show_bug.cgi?id=2515839          
                        │      │                  https://creativecommons.org/licenses/by/4.0/                 
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-33818
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56860
                        │      │                  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-56862
                        │      │                  https://errata.almalinux.org/10/ALSA-2026-65116.html         
                        │      │                  https://errata.rockylinux.org/RLSA-2026:66364                
                        │      │                  https://go.dev/cl/804261                                     
                        │      │                  https://go.dev/issue/80528                                   
                        │      │                  https://groups.google.com/g/golang-announce/c/94pEornpRlI    
                        │      │                  https://linux.oracle.com/cve/CVE-2026-56862.html             
                        │      │                  https://linux.oracle.com/errata/ELSA-2026-67161-0.html       
                        │      │                  https://nvd.nist.gov/vuln/detail/CVE-2026-56862              
                        │      │                  https://pkg.go.dev/vuln/GO-2026-6090                         
                        │      │                  https://www.cve.org/CVERecord?id=CVE-2026-56862              
                        │      │                  
                        │      ├ PublishedDate   : 2026-08-13T22:17:22.55Z 
                        │      ╰ LastModifiedDate: 2026-09-03T16:37:52.17Z 
                        ╰ [21] ╭ VulnerabilityID : CVE-2026-42505 
                               ├ VendorIDs                    
                               │                  ────────────
                               │                  GO-2026-5856
                               │                  
                               ├ PkgID           : stdlib@v1.26.4 
                               ├ PkgName         : stdlib 
                               ├ PkgIdentifier    ╭ PURL: pkg:golang/stdlib@v1.26.4 
                               │                  ╰ UID : 364846ec8fe81bdc 
                               ├ InstalledVersion: v1.26.4 
                               ├ FixedVersion    : 1.25.12, 1.26.5, 1.27.0-rc.2 
                               ├ Status          : fixed 
                               ├ Layer            ╭ Digest: sha256:0e4a9532af5c244a37ca106585e08e1965bfad2afec6
                               │                  │         bb22a540f6cb4c5edad4 
                               │                  ╰ DiffID: sha256:f453f7b1534697e7876d535ae3f5ec29d0c8f83c1b62
                               │                            a394f2090d37bfc108d4 
                               ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-42505 
                               ├ DataSource       ╭ ID  : govulndb 
                               │                  ├ Name: The Go Vulnerability Database 
                               │                  ╰ URL : https://pkg.go.dev/vuln/ 
                               ├ Fingerprint     : sha256:1b7c60a419b50c92e5cdd555146ce7677556cfaf6b838d639d3b8
                               │                   c622ead07e6 
                               ├ Title           : crypto/tls: golang: Go crypto/tls: Information disclosure in
                               │                    Encrypted Client Hello 
                               ├ Description     : Handshakes which used Encrypted Client Hello could be
                               │                   de-anonymized by a passive network observer due to a
                               │                   disclosure of pre-shared key identities in the unencrypted
                               │                   client hello. 
                               ├ Severity        : MEDIUM 
                               ├ CweIDs                  
                               │                  ───────
                               │                  CWE-201
                               │                  
                               ├ VendorSeverity   ╭ alma   : 3 
                               │                  ├ amazon : 2 
                               │                  ├ azure  : 2 
                               │                  ├ bitnami: 2 
                               │                  ├ photon : 2 
                               │                  ╰ redhat : 2 
                               ├ CVSS             ╭ bitnami ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:
                               │                  │         │           N/A:N 
                               │                  │         ╰ V3Score : 5.3 
                               │                  ╰ redhat  ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:
                               │                            │           N/A:N 
                               │                            ╰ V3Score : 5.3 
                               ├ References                                                                
                               │                  ─────────────────────────────────────────────────────────
                               │                  https://access.redhat.com/errata/RHSA-2026:37436         
                               │                  https://access.redhat.com/security/cve/CVE-2026-42505    
                               │                  https://bugzilla.redhat.com/2480756                      
                               │                  https://errata.almalinux.org/10/ALSA-2026-37436.html     
                               │                  https://go.dev/cl/775960                                 
                               │                  https://go.dev/issue/79282                               
                               │                  https://groups.google.com/g/golang-announce/c/OrmQE_Yp5Sc
                               │                  https://nvd.nist.gov/vuln/detail/CVE-2026-42505          
                               │                  https://pkg.go.dev/vuln/GO-2026-5856                     
                               │                  https://www.cve.org/CVERecord?id=CVE-2026-42505          
                               │                  
                               ├ PublishedDate   : 2026-07-08T17:17:21.497Z 
                               ╰ LastModifiedDate: 2026-09-16T20:14:44.473Z 
```
