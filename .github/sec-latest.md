```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:latest (alpine 3.24.0) 
│     ├ Class          : os-pkgs 
│     ├ Type           : alpine 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2026-55199 
│                       │     ├ PkgID           : libssh2@1.11.1-r2 
│                       │     ├ PkgName         : libssh2 
│                       │     ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libssh2@1.11.1-r2?arch=x86_64&distro=3.
│                       │     │                  │       24.0 
│                       │     │                  ╰ UID : d263fa2b663bba20 
│                       │     ├ InstalledVersion: 1.11.1-r2 
│                       │     ├ FixedVersion    : 1.11.1-r3 
│                       │     ├ Status          : fixed 
│                       │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
│                       │     │                  │         dd4162d8ce9f14b3f1f 
│                       │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
│                       │     │                            79274f61093c8474205 
│                       │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55199 
│                       │     ├ DataSource       ╭ ID  : alpine 
│                       │     │                  ├ Name: Alpine Secdb 
│                       │     │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │     ├ Fingerprint     : sha256:a58a23231a30a5c3b369ca740f63a4bfa032f3d9cc713a30f67697
│                       │     │                   2e3bc36758 
│                       │     ├ Title           : libssh2 through 1.11.1, fixed in commit 1762685, contains a
│                       │     │                   pre-authen ... 
│                       │     ├ Description     : libssh2 through 1.11.1, fixed in commit 1762685, contains a
│                       │     │                   pre-authentication denial of service vulnerability in the
│                       │     │                   SSH_MSG_EXT_INFO handler in src/packet.c that allows a
│                       │     │                   malicious SSH server to cause a client CPU exhaustion loop by
│                       │     │                    sending a crafted extension count value. A malicious server
│                       │     │                   can set nr_extensions to 0xFFFFFFFF during key exchange,
│                       │     │                   causing the client to spin in a tight CPU loop for over 60
│                       │     │                   seconds because return values from _libssh2_get_string() are
│                       │     │                   unchecked and the session timeout does not apply to CPU-bound
│                       │     │                    loops. 
│                       │     ├ Severity        : UNKNOWN 
│                       │     ├ CweIDs           ─ [0]: CWE-835 
│                       │     ├ References       ╭ [0]: https://github.com/libssh2/libssh2/commit/17626857d20b3
│                       │     │                  │      c9a1addfa45979dadcee1cd84a4 
│                       │     │                  ├ [1]: https://github.com/libssh2/libssh2/pull/1864 
│                       │     │                  ╰ [2]: https://www.vulncheck.com/advisories/libssh2-pre-authen
│                       │     │                         tication-dos-via-ssh-msg-ext-info-handler 
│                       │     ├ PublishedDate   : 2026-06-17T20:17:28.52Z 
│                       │     ╰ LastModifiedDate: 2026-06-22T18:43:49.9Z 
│                       ╰ [1] ╭ VulnerabilityID : CVE-2026-55200 
│                             ├ PkgID           : libssh2@1.11.1-r2 
│                             ├ PkgName         : libssh2 
│                             ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libssh2@1.11.1-r2?arch=x86_64&distro=3.
│                             │                  │       24.0 
│                             │                  ╰ UID : d263fa2b663bba20 
│                             ├ InstalledVersion: 1.11.1-r2 
│                             ├ FixedVersion    : 1.11.1-r3 
│                             ├ Status          : fixed 
│                             ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
│                             │                  │         dd4162d8ce9f14b3f1f 
│                             │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
│                             │                            79274f61093c8474205 
│                             ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55200 
│                             ├ DataSource       ╭ ID  : alpine 
│                             │                  ├ Name: Alpine Secdb 
│                             │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                             ├ Fingerprint     : sha256:c2d27600c0a3649ae40dc80e68bb466537077c8715d95ba32ad74f
│                             │                   17158f5321 
│                             ├ Title           : libssh2 through 1.11.1, fixed in commit 7acf3df contains an
│                             │                   out-of-bou ... 
│                             ├ Description     : libssh2 through 1.11.1, fixed in commit 7acf3df contains an
│                             │                   out-of-bounds write vulnerability in ssh2_transport_read()
│                             │                   that fails to enforce upper bounds on packet_length field.
│                             │                   Remote attackers can send crafted SSH packets with
│                             │                   excessively large packet_length values to corrupt heap memory
│                             │                    and achieve remote code execution. 
│                             ├ Severity        : UNKNOWN 
│                             ├ CweIDs           ─ [0]: CWE-680 
│                             ├ References       ╭ [0]: https://github.com/libssh2/libssh2/commit/97acf3dfda80c
│                             │                  │      91c3a8c9f2372546301d4a1a7a8 
│                             │                  ├ [1]: https://github.com/libssh2/libssh2/pull/2052 
│                             │                  ╰ [2]: https://www.vulncheck.com/advisories/libssh2-out-of-bou
│                             │                         nds-write-via-unchecked-packet-length-in-transport-c 
│                             ├ PublishedDate   : 2026-06-17T20:17:28.667Z 
│                             ╰ LastModifiedDate: 2026-06-22T18:43:49.9Z 
╰ [1] ╭ Target         : Java 
      ├ Class          : lang-pkgs 
      ├ Type           : jar 
      ├ Packages        
      ╰ Vulnerabilities ╭ [0] ╭ VulnerabilityID : CVE-2026-54512 
                        │     ├ VendorIDs        ─ [0]: GHSA-j3rv-43j4-c7qm 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.3 
                        │     │                  ╰ UID : af9e86e80fd64186 
                        │     ├ InstalledVersion: 2.21.3 
                        │     ├ FixedVersion    : 2.18.8, 3.1.4, 2.21.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                        │     │                  │         dd4162d8ce9f14b3f1f 
                        │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                        │     │                            79274f61093c8474205 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54512 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:3c0da12f713c89db11abcca802fa3f70f05dfb9ff4df7ea90d80a0
                        │     │                   03b4591a9a 
                        │     ├ Title           : jackson-databind has a PolymorphicTypeValidator bypass via
                        │     │                   generic type parameters that allows arbitrary class
                        │     │                   instantiation 
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
                        │     ├ VendorSeverity   ─ ghsa: 3 
                        │     ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H 
                        │     │                         ╰ V3Score : 8.1 
                        │     ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/43
                        │     │                  │      4d6c511de7fdd9872f29157aafb6162d12d8d5 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/issues/5988 
                        │     │                  ╰ [3]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                         advisories/GHSA-j3rv-43j4-c7qm 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.203Z 
                        │     ╰ LastModifiedDate: 2026-06-23T21:17:02.203Z 
                        ├ [1] ╭ VulnerabilityID : CVE-2026-54513 
                        │     ├ VendorIDs        ─ [0]: GHSA-rmj7-2vxq-3g9f 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.3 
                        │     │                  ╰ UID : af9e86e80fd64186 
                        │     ├ InstalledVersion: 2.21.3 
                        │     ├ FixedVersion    : 2.18.8, 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                        │     │                  │         dd4162d8ce9f14b3f1f 
                        │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                        │     │                            79274f61093c8474205 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54513 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:26dde57c1f95b4403ef63933018e24f44b3c990ca3b8f5eff224d4
                        │     │                   ffab19ad53 
                        │     ├ Title           : jackson-databind has an array subtype allowlist bypass in
                        │     │                   BasicPolymorphicTypeValidator (allowIfSubTypeIsArray) 
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
                        │     ├ VendorSeverity   ─ ghsa: 3 
                        │     ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H 
                        │     │                         ╰ V3Score : 8.1 
                        │     ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/01
                        │     │                  │      d1692c8d0ed03e51a0e3c4f8a9e6908e4931e5 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/24
                        │     │                  │      529da29fdf46ff94ca38de9ebf31cd188f5e8e 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/issues/5981 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/issues/5983 
                        │     │                  ├ [5]: https://github.com/FasterXML/jackson-databind/pull/5984 
                        │     │                  ╰ [6]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                         advisories/GHSA-rmj7-2vxq-3g9f 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.333Z 
                        │     ╰ LastModifiedDate: 2026-06-23T21:17:02.333Z 
                        ├ [2] ╭ VulnerabilityID : CVE-2026-54514 
                        │     ├ VendorIDs        ─ [0]: GHSA-hgj6-7826-r7m5 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.3 
                        │     │                  ╰ UID : af9e86e80fd64186 
                        │     ├ InstalledVersion: 2.21.3 
                        │     ├ FixedVersion    : 2.18.8, 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                        │     │                  │         dd4162d8ce9f14b3f1f 
                        │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                        │     │                            79274f61093c8474205 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54514 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:d30b1279c3f37e6dfb3dd8f31e71d48ec1f1aeeb845f1a8da2b86b
                        │     │                   157d66f234 
                        │     ├ Title           : jackson-databind: InetSocketAddress deserialization triggers
                        │     │                   eager DNS resolution (SSRF) 
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
                        │     ├ VendorSeverity   ─ ghsa: 2 
                        │     ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/A:N 
                        │     │                         ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/1f
                        │     │                  │      5a1037b1e9e05920e755cb35f198bcd46667e4 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/pull/5951 
                        │     │                  ╰ [3]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                         advisories/GHSA-hgj6-7826-r7m5 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.467Z 
                        │     ╰ LastModifiedDate: 2026-06-23T21:17:02.467Z 
                        ├ [3] ╭ VulnerabilityID : CVE-2026-54515 
                        │     ├ VendorIDs        ─ [0]: GHSA-5jmj-h7xm-6q6v 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.3 
                        │     │                  ╰ UID : af9e86e80fd64186 
                        │     ├ InstalledVersion: 2.21.3 
                        │     ├ FixedVersion    : 3.1.4, 2.18.9, 2.21.5 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                        │     │                  │         dd4162d8ce9f14b3f1f 
                        │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                        │     │                            79274f61093c8474205 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54515 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:7938ad2990bdfbe167af3732426b8a0994f7b40efc71e312e98501
                        │     │                   a1422899c9 
                        │     ├ Title           : jackson-databind has case-insensitive deserialization
                        │     │                   bypasses per-property @JsonIgnoreProperties 
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
                        │     ├ VendorSeverity   ─ ghsa: 2 
                        │     ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/A:N 
                        │     │                         ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/0e
                        │     │                  │      1b0b211f7a53baa62ba2f4c9bd006c7bf4d5fa 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/issues/5962 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/issues/5964 
                        │     │                  ╰ [4]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                         advisories/GHSA-5jmj-h7xm-6q6v 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.597Z 
                        │     ╰ LastModifiedDate: 2026-06-23T21:17:02.597Z 
                        ├ [4] ╭ VulnerabilityID : CVE-2026-54516 
                        │     ├ VendorIDs        ─ [0]: GHSA-9fxm-vc8v-hj55 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.3 
                        │     │                  ╰ UID : af9e86e80fd64186 
                        │     ├ InstalledVersion: 2.21.3 
                        │     ├ FixedVersion    : 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                        │     │                  │         dd4162d8ce9f14b3f1f 
                        │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                        │     │                            79274f61093c8474205 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54516 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:9c1c595e5be7fa623c83e02c9c82800b2c69762e52d235100341d8
                        │     │                   e00b2f7dc9 
                        │     ├ Title           : jackson-databind's renamed @JsonIgnore'd setters can
                        │     │                   deserialize via private fields 
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
                        │     ├ VendorSeverity   ─ ghsa: 2 
                        │     ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/A:N 
                        │     │                         ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/c3
                        │     │                  │      d56dd25d52319828147c5b9aeabf2d485c250a 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/e8
                        │     │                  │      8cb17006b6af4883b973058f0bb6486e5074af 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/pull/5967 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/pull/5968 
                        │     │                  ╰ [5]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                         advisories/GHSA-9fxm-vc8v-hj55 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.723Z 
                        │     ╰ LastModifiedDate: 2026-06-23T21:17:02.723Z 
                        ├ [5] ╭ VulnerabilityID : CVE-2026-54517 
                        │     ├ VendorIDs        ─ [0]: GHSA-5hh8-q8hv-fr38 
                        │     ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                        │     ├ PkgPath         : openaf/openaf.jar 
                        │     ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                        │     │                  │       2.21.3 
                        │     │                  ╰ UID : af9e86e80fd64186 
                        │     ├ InstalledVersion: 2.21.3 
                        │     ├ FixedVersion    : 2.21.4, 3.1.4 
                        │     ├ Status          : fixed 
                        │     ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                        │     │                  │         dd4162d8ce9f14b3f1f 
                        │     │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                        │     │                            79274f61093c8474205 
                        │     ├ SeveritySource  : ghsa 
                        │     ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54517 
                        │     ├ DataSource       ╭ ID  : ghsa 
                        │     │                  ├ Name: GitHub Security Advisory Maven 
                        │     │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                        │     │                          osystem%3Amaven 
                        │     ├ Fingerprint     : sha256:80283557880e3a6f1f426e1dd4defd0df8c15f8f7c689926f6ed7b
                        │     │                   bdc4952204 
                        │     ├ Title           : jackson-databind has @JsonView bypass for setterless creator
                        │     │                   properties 
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
                        │     ├ VendorSeverity   ─ ghsa: 2 
                        │     ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/A:N 
                        │     │                         ╰ V3Score : 5.3 
                        │     ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/5b
                        │     │                  │      f23edb4221f7dd2ec8e71ff6d26c61640f261d 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/94
                        │     │                  │      c5d215b3af1505098c686405d9641f041a9962 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/pull/5969 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/pull/5970 
                        │     │                  ╰ [5]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                         advisories/GHSA-5hh8-q8hv-fr38 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.853Z 
                        │     ╰ LastModifiedDate: 2026-06-23T21:17:02.853Z 
                        ╰ [6] ╭ VulnerabilityID : CVE-2026-54518 
                              ├ VendorIDs        ─ [0]: GHSA-rcqc-6cw3-h962 
                              ├ PkgName         : com.fasterxml.jackson.core:jackson-databind 
                              ├ PkgPath         : openaf/openaf.jar 
                              ├ PkgIdentifier    ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@
                              │                  │       2.21.3 
                              │                  ╰ UID : af9e86e80fd64186 
                              ├ InstalledVersion: 2.21.3 
                              ├ FixedVersion    : 2.21.4 
                              ├ Status          : fixed 
                              ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7bd
                              │                  │         dd4162d8ce9f14b3f1f 
                              │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5b
                              │                            79274f61093c8474205 
                              ├ SeveritySource  : ghsa 
                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-54518 
                              ├ DataSource       ╭ ID  : ghsa 
                              │                  ├ Name: GitHub Security Advisory Maven 
                              │                  ╰ URL : https://github.com/advisories?query=type%3Areviewed+ec
                              │                          osystem%3Amaven 
                              ├ Fingerprint     : sha256:4e83ea88efae00bc4043e83d159f3921b5315e2f2f8f9f0fd1ff7d
                              │                   97996d61cd 
                              ├ Title           : jackson-databind has a @JsonView bypass for unwrapped creator
                              │                    parameters 
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
                              ├ VendorSeverity   ─ ghsa: 2 
                              ├ CVSS             ─ ghsa ╭ V3Vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L/A:N 
                              │                         ╰ V3Score : 6.5 
                              ├ References       ╭ [0]: https://github.com/FasterXML/jackson-databind 
                              │                  ├ [1]: https://github.com/FasterXML/jackson-databind/commit/72
                              │                  │      1fa07ebbd4aab4a659a1a68940878315c3e341 
                              │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/d6
                              │                  │      33bc038f200c1397c07f1a2b46f58e72c91eea 
                              │                  ├ [3]: https://github.com/FasterXML/jackson-databind/pull/5971 
                              │                  ├ [4]: https://github.com/FasterXML/jackson-databind/pull/5973 
                              │                  ╰ [5]: https://github.com/FasterXML/jackson-databind/security/
                              │                         advisories/GHSA-rcqc-6cw3-h962 
                              ├ PublishedDate   : 2026-06-23T22:16:32.073Z 
                              ╰ LastModifiedDate: 2026-06-23T22:16:32.073Z 
```
