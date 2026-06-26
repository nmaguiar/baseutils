```yaml
╭ [0] ╭ Target         : nmaguiar/baseutils:latest (alpine 3.24.0) 
│     ├ Class          : os-pkgs 
│     ├ Type           : alpine 
│     ├ Packages        
│     ╰ Vulnerabilities ╭ [0]  ╭ VulnerabilityID : CVE-2026-55200 
│                       │      ├ PkgID           : libssh2@1.11.1-r2 
│                       │      ├ PkgName         : libssh2 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libssh2@1.11.1-r2?arch=x86_64&distro=3
│                       │      │                  │       .24.0 
│                       │      │                  ╰ UID : d263fa2b663bba20 
│                       │      ├ InstalledVersion: 1.11.1-r2 
│                       │      ├ FixedVersion    : 1.11.1-r3 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55200 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:c2d27600c0a3649ae40dc80e68bb466537077c8715d95ba32ad74
│                       │      │                   f17158f5321 
│                       │      ├ Title           : libssh2: libssh2 - Out-of-Bounds Write via Unchecked
│                       │      │                   packet_length in transport.c 
│                       │      ├ Description     : libssh2 through 1.11.1, fixed in commit 7acf3df contains an
│                       │      │                   out-of-bounds write vulnerability in ssh2_transport_read()
│                       │      │                   that fails to enforce upper bounds on packet_length field.
│                       │      │                   Remote attackers can send crafted SSH packets with
│                       │      │                   excessively large packet_length values to corrupt heap
│                       │      │                   memory and achieve remote code execution. 
│                       │      ├ Severity        : HIGH 
│                       │      ├ CweIDs           ─ [0]: CWE-680 
│                       │      ├ VendorSeverity   ─ redhat: 3 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 8.1 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55200 
│                       │      │                  ├ [1]: https://github.com/bikini/exploitarium/tree/main/libss
│                       │      │                  │      h2-cve-2026-55200-poc 
│                       │      │                  ├ [2]: https://github.com/libssh2/libssh2/commit/97acf3dfda80
│                       │      │                  │      c91c3a8c9f2372546301d4a1a7a8 
│                       │      │                  ├ [3]: https://github.com/libssh2/libssh2/pull/2052 
│                       │      │                  ├ [4]: https://nvd.nist.gov/vuln/detail/CVE-2026-55200 
│                       │      │                  ├ [5]: https://www.cve.org/CVERecord?id=CVE-2026-55200 
│                       │      │                  ╰ [6]: https://www.vulncheck.com/advisories/libssh2-out-of-bo
│                       │      │                         unds-write-via-unchecked-packet-length-in-transport-c
│                       │      │                         [m 
│                       │      ├ PublishedDate   : 2026-06-17T20:17:28.667Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T05:16:54.883Z 
│                       ├ [1]  ╭ VulnerabilityID : CVE-2026-55199 
│                       │      ├ PkgID           : libssh2@1.11.1-r2 
│                       │      ├ PkgName         : libssh2 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/libssh2@1.11.1-r2?arch=x86_64&distro=3
│                       │      │                  │       .24.0 
│                       │      │                  ╰ UID : d263fa2b663bba20 
│                       │      ├ InstalledVersion: 1.11.1-r2 
│                       │      ├ FixedVersion    : 1.11.1-r3 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-55199 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:a58a23231a30a5c3b369ca740f63a4bfa032f3d9cc713a30f6769
│                       │      │                   72e3bc36758 
│                       │      ├ Title           : libssh2: libssh2: Denial of Service via crafted
│                       │      │                   SSH_MSG_EXT_INFO message 
│                       │      ├ Description     : libssh2 through 1.11.1, fixed in commit 1762685, contains a
│                       │      │                   pre-authentication denial of service vulnerability in the
│                       │      │                   SSH_MSG_EXT_INFO handler in src/packet.c that allows a
│                       │      │                   malicious SSH server to cause a client CPU exhaustion loop
│                       │      │                   by sending a crafted extension count value. A malicious
│                       │      │                   server can set nr_extensions to 0xFFFFFFFF during key
│                       │      │                   exchange, causing the client to spin in a tight CPU loop for
│                       │      │                    over 60 seconds because return values from
│                       │      │                   _libssh2_get_string() are unchecked and the session timeout
│                       │      │                   does not apply to CPU-bound loops. 
│                       │      ├ Severity        : MEDIUM 
│                       │      ├ CweIDs           ─ [0]: CWE-835 
│                       │      ├ VendorSeverity   ─ redhat: 2 
│                       │      ├ CVSS             ─ redhat ╭ V3Vector: CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N
│                       │      │                           │           /A:H 
│                       │      │                           ╰ V3Score : 5.9 
│                       │      ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-55199 
│                       │      │                  ├ [1]: https://github.com/libssh2/libssh2/commit/17626857d20b
│                       │      │                  │      3c9a1addfa45979dadcee1cd84a4 
│                       │      │                  ├ [2]: https://github.com/libssh2/libssh2/pull/1864 
│                       │      │                  ├ [3]: https://nvd.nist.gov/vuln/detail/CVE-2026-55199 
│                       │      │                  ├ [4]: https://www.cve.org/CVERecord?id=CVE-2026-55199 
│                       │      │                  ╰ [5]: https://www.vulncheck.com/advisories/libssh2-pre-authe
│                       │      │                         ntication-dos-via-ssh-msg-ext-info-handler 
│                       │      ├ PublishedDate   : 2026-06-17T20:17:28.52Z 
│                       │      ╰ LastModifiedDate: 2026-06-22T18:43:49.9Z 
│                       ├ [2]  ╭ VulnerabilityID : CVE-2026-57453 
│                       │      ├ PkgID           : vim@9.2.0677-r0 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : eb929552ddbcf07b 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0680-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57453 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:c8c9e150418a48163c9e63ab2bd3c602b64d4d7a24268e60b486d
│                       │      │                   9af4cda5c45 
│                       │      ├ Title           : Vim is an open source, command line text editor. From
│                       │      │                   9.1.1784 until 9 ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. From
│                       │      │                   9.1.1784 until 9.2.0678, when the bundled zip plugin
│                       │      │                   autoload/zip.vim falls back to PowerShell to browse, read,
│                       │      │                   extract, update or delete entries in a zip archive, it
│                       │      │                   builds the PowerShell command by inserting archive entry
│                       │      │                   names that are quoted only for the shell, not for
│                       │      │                   PowerShell. A crafted entry name can break out of the
│                       │      │                   intended string context and cause PowerShell to execute
│                       │      │                   arbitrary commands with the privileges of the user running
│                       │      │                   Vim, triggered by opening, viewing or extracting the
│                       │      │                   archive. This vulnerability is fixed in 9.2.0678. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-77 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/b2cc9be119d51212bf0d
│                       │      │                  │      3f2a99 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0678 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-x5
│                       │      │                         fg-h5w9-9frf 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.52Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T16:27:02.61Z 
│                       ├ [3]  ╭ VulnerabilityID : CVE-2026-57454 
│                       │      ├ PkgID           : vim@9.2.0677-r0 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : eb929552ddbcf07b 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0680-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57454 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:bf110146c193170c7c0d46f2d7cf45db1115745376fa0b4225d55
│                       │      │                   78565002dc2 
│                       │      ├ Title           : Vim is an open source, command line text editor. From
│                       │      │                   9.2.0320 until 9 ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. From
│                       │      │                   9.2.0320 until 9.2.0679, a crafted undo or swap file can
│                       │      │                   store a virtual-text property whose offset and length point
│                       │      │                   outside the line's property data. When Vim restores or
│                       │      │                   displays such a line it converts the offset into a pointer
│                       │      │                   and reads the virtual text without bounds checking, causing
│                       │      │                   an out-of-bounds read that can crash Vim or disclose
│                       │      │                   adjacent heap memory. This vulnerability is fixed in
│                       │      │                   9.2.0679. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-125 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/b3faeecc976d3031d7c0
│                       │      │                  │      675623516ec60c30f949 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0679 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-ww
│                       │      │                         8h-47xp-hp4w 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.647Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T16:27:02.61Z 
│                       ├ [4]  ╭ VulnerabilityID : CVE-2026-57455 
│                       │      ├ PkgID           : vim@9.2.0677-r0 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : eb929552ddbcf07b 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0699-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:ea69e8b192f5f361ab360f4c552a53cf95c19e3e8536ca5de9592
│                       │      │                   7a6f277ace8 
│                       │      ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0698, th ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │      │                   in src/spell.c translates a word through a spell file's SOFO
│                       │      │                    (sound-folding) byte map into a caller-owned result buffer.
│                       │      │                    Its copy loop advances the output index ri with no upper
│                       │      │                   bound and terminates only on the input NUL, writing one byte
│                       │      │                    per input byte into the MAXWLEN-element stack buffer the
│                       │      │                   caller provides. A word longer than MAXWLEN, passed to
│                       │      │                   soundfold() (or reached via sound-based spell suggestion)
│                       │      │                   while a SOFO-based spell language is active, therefore
│                       │      │                   writes past the end of that buffer. This is a stack
│                       │      │                   out-of-bounds write that corrupts the call frame and crashes
│                       │      │                    the editor. This vulnerability is fixed in 9.2.0698. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-787 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7f
│                       │      │                  │      69588dd249e8ccfed41b 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-q8
│                       │      │                         mh-6qm3-25g4 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │      ╰ LastModifiedDate: 2026-06-26T00:16:54.907Z 
│                       ├ [5]  ╭ VulnerabilityID : CVE-2026-57456 
│                       │      ├ PkgID           : vim@9.2.0677-r0 
│                       │      ├ PkgName         : vim 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : eb929552ddbcf07b 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0699-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:b9c061e9f4be36306bb06e4008dca748db3977e3b9da391c9783b
│                       │      │                   b5d56574cac 
│                       │      ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0699, Vi ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0699, Vim's Python omni-completion
│                       │      │                   (runtime/autoload/python3complete.vim and the legacy
│                       │      │                   pythoncomplete.vim) executes reconstructed function and
│                       │      │                   class definitions from the current buffer with exec() as
│                       │      │                   part of populating the completion dictionary. When
│                       │      │                   reconstructing that source, each scope's docstring is
│                       │      │                   inserted verbatim between triple quotes with no escaping, so
│                       │      │                    a hostile buffer can break out of the triple-quoted literal
│                       │      │                    and execute attacker-controlled Python during
│                       │      │                   omni-completion. This vulnerability is fixed in 9.2.0699. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-94 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd84
│                       │      │                  │      86ae04e21c2a81016ba8 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-pp
│                       │      │                         j8-wqjf-6fp3 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T19:16:45.803Z 
│                       ├ [6]  ╭ VulnerabilityID : CVE-2026-57453 
│                       │      ├ PkgID           : vim-common@9.2.0677-r0 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim-common@9.2.0677-r0?arch=x86_64&dis
│                       │      │                  │       tro=3.24.0 
│                       │      │                  ╰ UID : bdf02e7de1497012 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0680-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57453 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:7fd381de3a540326d797f6dd83fd44ccc69513e71e6891d8bd675
│                       │      │                   5da8d07d940 
│                       │      ├ Title           : Vim is an open source, command line text editor. From
│                       │      │                   9.1.1784 until 9 ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. From
│                       │      │                   9.1.1784 until 9.2.0678, when the bundled zip plugin
│                       │      │                   autoload/zip.vim falls back to PowerShell to browse, read,
│                       │      │                   extract, update or delete entries in a zip archive, it
│                       │      │                   builds the PowerShell command by inserting archive entry
│                       │      │                   names that are quoted only for the shell, not for
│                       │      │                   PowerShell. A crafted entry name can break out of the
│                       │      │                   intended string context and cause PowerShell to execute
│                       │      │                   arbitrary commands with the privileges of the user running
│                       │      │                   Vim, triggered by opening, viewing or extracting the
│                       │      │                   archive. This vulnerability is fixed in 9.2.0678. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-77 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/b2cc9be119d51212bf0d
│                       │      │                  │      3f2a99 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0678 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-x5
│                       │      │                         fg-h5w9-9frf 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.52Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T16:27:02.61Z 
│                       ├ [7]  ╭ VulnerabilityID : CVE-2026-57454 
│                       │      ├ PkgID           : vim-common@9.2.0677-r0 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim-common@9.2.0677-r0?arch=x86_64&dis
│                       │      │                  │       tro=3.24.0 
│                       │      │                  ╰ UID : bdf02e7de1497012 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0680-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57454 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:ee654e4798ff8cbdf239f3aef5b75f39290637ca35c363f449eed
│                       │      │                   cde55ff7366 
│                       │      ├ Title           : Vim is an open source, command line text editor. From
│                       │      │                   9.2.0320 until 9 ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. From
│                       │      │                   9.2.0320 until 9.2.0679, a crafted undo or swap file can
│                       │      │                   store a virtual-text property whose offset and length point
│                       │      │                   outside the line's property data. When Vim restores or
│                       │      │                   displays such a line it converts the offset into a pointer
│                       │      │                   and reads the virtual text without bounds checking, causing
│                       │      │                   an out-of-bounds read that can crash Vim or disclose
│                       │      │                   adjacent heap memory. This vulnerability is fixed in
│                       │      │                   9.2.0679. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-125 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/b3faeecc976d3031d7c0
│                       │      │                  │      675623516ec60c30f949 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0679 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-ww
│                       │      │                         8h-47xp-hp4w 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.647Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T16:27:02.61Z 
│                       ├ [8]  ╭ VulnerabilityID : CVE-2026-57455 
│                       │      ├ PkgID           : vim-common@9.2.0677-r0 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim-common@9.2.0677-r0?arch=x86_64&dis
│                       │      │                  │       tro=3.24.0 
│                       │      │                  ╰ UID : bdf02e7de1497012 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0699-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:53d713b667dd6e91a05bd4c3da7b8499da406a519889875a025c6
│                       │      │                   0504e9fc9a5 
│                       │      ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0698, th ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │      │                   in src/spell.c translates a word through a spell file's SOFO
│                       │      │                    (sound-folding) byte map into a caller-owned result buffer.
│                       │      │                    Its copy loop advances the output index ri with no upper
│                       │      │                   bound and terminates only on the input NUL, writing one byte
│                       │      │                    per input byte into the MAXWLEN-element stack buffer the
│                       │      │                   caller provides. A word longer than MAXWLEN, passed to
│                       │      │                   soundfold() (or reached via sound-based spell suggestion)
│                       │      │                   while a SOFO-based spell language is active, therefore
│                       │      │                   writes past the end of that buffer. This is a stack
│                       │      │                   out-of-bounds write that corrupts the call frame and crashes
│                       │      │                    the editor. This vulnerability is fixed in 9.2.0698. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-787 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7f
│                       │      │                  │      69588dd249e8ccfed41b 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-q8
│                       │      │                         mh-6qm3-25g4 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │      ╰ LastModifiedDate: 2026-06-26T00:16:54.907Z 
│                       ├ [9]  ╭ VulnerabilityID : CVE-2026-57456 
│                       │      ├ PkgID           : vim-common@9.2.0677-r0 
│                       │      ├ PkgName         : vim-common 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/vim-common@9.2.0677-r0?arch=x86_64&dis
│                       │      │                  │       tro=3.24.0 
│                       │      │                  ╰ UID : bdf02e7de1497012 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0699-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:57ad0bd3303104ff695fe6848a001a6c4ec4dab3cd5191346c7b1
│                       │      │                   b4be1f66b05 
│                       │      ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0699, Vi ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0699, Vim's Python omni-completion
│                       │      │                   (runtime/autoload/python3complete.vim and the legacy
│                       │      │                   pythoncomplete.vim) executes reconstructed function and
│                       │      │                   class definitions from the current buffer with exec() as
│                       │      │                   part of populating the completion dictionary. When
│                       │      │                   reconstructing that source, each scope's docstring is
│                       │      │                   inserted verbatim between triple quotes with no escaping, so
│                       │      │                    a hostile buffer can break out of the triple-quoted literal
│                       │      │                    and execute attacker-controlled Python during
│                       │      │                   omni-completion. This vulnerability is fixed in 9.2.0699. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-94 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd84
│                       │      │                  │      86ae04e21c2a81016ba8 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-pp
│                       │      │                         j8-wqjf-6fp3 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T19:16:45.803Z 
│                       ├ [10] ╭ VulnerabilityID : CVE-2026-57453 
│                       │      ├ PkgID           : xxd@9.2.0677-r0 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/xxd@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : e656a82afe3881e6 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0680-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57453 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:600b2b0391022f1c8ead1f8734b709ff5a9dcde8dc85d6ade3348
│                       │      │                   e9021d35e2f 
│                       │      ├ Title           : Vim is an open source, command line text editor. From
│                       │      │                   9.1.1784 until 9 ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. From
│                       │      │                   9.1.1784 until 9.2.0678, when the bundled zip plugin
│                       │      │                   autoload/zip.vim falls back to PowerShell to browse, read,
│                       │      │                   extract, update or delete entries in a zip archive, it
│                       │      │                   builds the PowerShell command by inserting archive entry
│                       │      │                   names that are quoted only for the shell, not for
│                       │      │                   PowerShell. A crafted entry name can break out of the
│                       │      │                   intended string context and cause PowerShell to execute
│                       │      │                   arbitrary commands with the privileges of the user running
│                       │      │                   Vim, triggered by opening, viewing or extracting the
│                       │      │                   archive. This vulnerability is fixed in 9.2.0678. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-77 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/b2cc9be119d51212bf0d
│                       │      │                  │      3f2a99 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0678 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-x5
│                       │      │                         fg-h5w9-9frf 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.52Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T16:27:02.61Z 
│                       ├ [11] ╭ VulnerabilityID : CVE-2026-57454 
│                       │      ├ PkgID           : xxd@9.2.0677-r0 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/xxd@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : e656a82afe3881e6 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0680-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57454 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:2f8dc408f40b82f9653ebd4aac6387717df2c48f0b05076d28e0c
│                       │      │                   62bb1419b29 
│                       │      ├ Title           : Vim is an open source, command line text editor. From
│                       │      │                   9.2.0320 until 9 ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. From
│                       │      │                   9.2.0320 until 9.2.0679, a crafted undo or swap file can
│                       │      │                   store a virtual-text property whose offset and length point
│                       │      │                   outside the line's property data. When Vim restores or
│                       │      │                   displays such a line it converts the offset into a pointer
│                       │      │                   and reads the virtual text without bounds checking, causing
│                       │      │                   an out-of-bounds read that can crash Vim or disclose
│                       │      │                   adjacent heap memory. This vulnerability is fixed in
│                       │      │                   9.2.0679. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-125 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/b3faeecc976d3031d7c0
│                       │      │                  │      675623516ec60c30f949 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0679 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-ww
│                       │      │                         8h-47xp-hp4w 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.647Z 
│                       │      ╰ LastModifiedDate: 2026-06-25T16:27:02.61Z 
│                       ├ [12] ╭ VulnerabilityID : CVE-2026-57455 
│                       │      ├ PkgID           : xxd@9.2.0677-r0 
│                       │      ├ PkgName         : xxd 
│                       │      ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/xxd@9.2.0677-r0?arch=x86_64&distro=3.2
│                       │      │                  │       4.0 
│                       │      │                  ╰ UID : e656a82afe3881e6 
│                       │      ├ InstalledVersion: 9.2.0677-r0 
│                       │      ├ FixedVersion    : 9.2.0699-r0 
│                       │      ├ Status          : fixed 
│                       │      ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                       │      │                  │         ddd4162d8ce9f14b3f1f 
│                       │      │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                       │      │                            b79274f61093c8474205 
│                       │      ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57455 
│                       │      ├ DataSource       ╭ ID  : alpine 
│                       │      │                  ├ Name: Alpine Secdb 
│                       │      │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                       │      ├ Fingerprint     : sha256:b356c38d5ade09c1ae0c069102acea19de2a09ebccc4559c9d5bb
│                       │      │                   dca20a74ab4 
│                       │      ├ Title           : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0698, th ... 
│                       │      ├ Description     : Vim is an open source, command line text editor. Prior to
│                       │      │                   9.2.0698, the single-byte branch of spell_soundfold_sofo()
│                       │      │                   in src/spell.c translates a word through a spell file's SOFO
│                       │      │                    (sound-folding) byte map into a caller-owned result buffer.
│                       │      │                    Its copy loop advances the output index ri with no upper
│                       │      │                   bound and terminates only on the input NUL, writing one byte
│                       │      │                    per input byte into the MAXWLEN-element stack buffer the
│                       │      │                   caller provides. A word longer than MAXWLEN, passed to
│                       │      │                   soundfold() (or reached via sound-based spell suggestion)
│                       │      │                   while a SOFO-based spell language is active, therefore
│                       │      │                   writes past the end of that buffer. This is a stack
│                       │      │                   out-of-bounds write that corrupts the call frame and crashes
│                       │      │                    the editor. This vulnerability is fixed in 9.2.0698. 
│                       │      ├ Severity        : UNKNOWN 
│                       │      ├ CweIDs           ─ [0]: CWE-787 
│                       │      ├ References       ╭ [0]: https://github.com/vim/vim/commit/497f931f85339d175d7f
│                       │      │                  │      69588dd249e8ccfed41b 
│                       │      │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0698 
│                       │      │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-q8
│                       │      │                         mh-6qm3-25g4 
│                       │      ├ PublishedDate   : 2026-06-25T16:16:42.773Z 
│                       │      ╰ LastModifiedDate: 2026-06-26T00:16:54.907Z 
│                       ╰ [13] ╭ VulnerabilityID : CVE-2026-57456 
│                              ├ PkgID           : xxd@9.2.0677-r0 
│                              ├ PkgName         : xxd 
│                              ├ PkgIdentifier    ╭ PURL: pkg:apk/alpine/xxd@9.2.0677-r0?arch=x86_64&distro=3.2
│                              │                  │       4.0 
│                              │                  ╰ UID : e656a82afe3881e6 
│                              ├ InstalledVersion: 9.2.0677-r0 
│                              ├ FixedVersion    : 9.2.0699-r0 
│                              ├ Status          : fixed 
│                              ├ Layer            ╭ Digest: sha256:fae458aefeb60b1e2ebe5f520fb53d91aebd468abb7b
│                              │                  │         ddd4162d8ce9f14b3f1f 
│                              │                  ╰ DiffID: sha256:77f9cffd1d862a171f87e0c5347e8e6ac9b2b6f32ab5
│                              │                            b79274f61093c8474205 
│                              ├ PrimaryURL      : https://avd.aquasec.com/nvd/cve-2026-57456 
│                              ├ DataSource       ╭ ID  : alpine 
│                              │                  ├ Name: Alpine Secdb 
│                              │                  ╰ URL : https://secdb.alpinelinux.org/ 
│                              ├ Fingerprint     : sha256:f29dda9fc358d63100227861f6b918dff22a83be1f732dc177bbb
│                              │                   caaa70d8a28 
│                              ├ Title           : Vim is an open source, command line text editor. Prior to
│                              │                   9.2.0699, Vi ... 
│                              ├ Description     : Vim is an open source, command line text editor. Prior to
│                              │                   9.2.0699, Vim's Python omni-completion
│                              │                   (runtime/autoload/python3complete.vim and the legacy
│                              │                   pythoncomplete.vim) executes reconstructed function and
│                              │                   class definitions from the current buffer with exec() as
│                              │                   part of populating the completion dictionary. When
│                              │                   reconstructing that source, each scope's docstring is
│                              │                   inserted verbatim between triple quotes with no escaping, so
│                              │                    a hostile buffer can break out of the triple-quoted literal
│                              │                    and execute attacker-controlled Python during
│                              │                   omni-completion. This vulnerability is fixed in 9.2.0699. 
│                              ├ Severity        : UNKNOWN 
│                              ├ CweIDs           ─ [0]: CWE-94 
│                              ├ References       ╭ [0]: https://github.com/vim/vim/commit/cce141c42740f122dd84
│                              │                  │      86ae04e21c2a81016ba8 
│                              │                  ├ [1]: https://github.com/vim/vim/releases/tag/v9.2.0699 
│                              │                  ╰ [2]: https://github.com/vim/vim/security/advisories/GHSA-pp
│                              │                         j8-wqjf-6fp3 
│                              ├ PublishedDate   : 2026-06-25T16:16:42.9Z 
│                              ╰ LastModifiedDate: 2026-06-25T19:16:45.803Z 
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
                        │     ├ Title           : jackson-databind contains the general-purpose data-binding
                        │     │                   functionali ... 
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
                        │     ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
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
                        │     ├ References       ╭ [0]: https://access.redhat.com/security/cve/CVE-2026-54513 
                        │     │                  ├ [1]: https://github.com/FasterXML/jackson-databind 
                        │     │                  ├ [2]: https://github.com/FasterXML/jackson-databind/commit/01
                        │     │                  │      d1692c8d0ed03e51a0e3c4f8a9e6908e4931e5 
                        │     │                  ├ [3]: https://github.com/FasterXML/jackson-databind/commit/24
                        │     │                  │      529da29fdf46ff94ca38de9ebf31cd188f5e8e 
                        │     │                  ├ [4]: https://github.com/FasterXML/jackson-databind/issues/5981 
                        │     │                  ├ [5]: https://github.com/FasterXML/jackson-databind/issues/5983 
                        │     │                  ├ [6]: https://github.com/FasterXML/jackson-databind/pull/5984 
                        │     │                  ├ [7]: https://github.com/FasterXML/jackson-databind/security/
                        │     │                  │      advisories/GHSA-rmj7-2vxq-3g9f 
                        │     │                  ├ [8]: https://nvd.nist.gov/vuln/detail/CVE-2026-54513 
                        │     │                  ╰ [9]: https://www.cve.org/CVERecord?id=CVE-2026-54513 
                        │     ├ PublishedDate   : 2026-06-23T21:17:02.333Z 
                        │     ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
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
                        │     ├ Title           : jackson-databind contains the general-purpose data-binding
                        │     │                   functionali ... 
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
                        │     ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
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
                        │     ├ Title           : jackson-databind contains the general-purpose data-binding
                        │     │                   functionali ... 
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
                        │     ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
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
                        │     ├ Title           : jackson-databind contains the general-purpose data-binding
                        │     │                   functionali ... 
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
                        │     ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
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
                        │     ├ Title           : jackson-databind contains the general-purpose data-binding
                        │     │                   functionali ... 
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
                        │     ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
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
                              ├ Title           : jackson-databind contains the general-purpose data-binding
                              │                   functionali ... 
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
                              ╰ LastModifiedDate: 2026-06-25T16:14:14.483Z 
```
