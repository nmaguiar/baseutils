````yaml
╭ [0] ╭ Target  : nmaguiar/baseutils:latest (alpine 3.23.0) 
│     ├ Class   : os-pkgs 
│     ├ Type    : alpine 
│     ╰ Packages ╭ [0]  ╭ ID            : acl-libs@2.3.2-r1 
│                │      ├ Name          : acl-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/acl-libs@2.3.2-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : fac91dd8857e5e44 
│                │      ├ Version       : 2.3.2-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : acl 
│                │      ├ SrcVersion    : 2.3.2-r1 
│                │      ├ Licenses       ╭ [0]: LGPL-2.1-or-later 
│                │      │                ╰ [1]: GPL-2.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:1692d70717669c753f52909bc16fa87b66cdb617 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libacl.so.1 
│                │                       ╰ [1]: usr/lib/libacl.so.1.1.2302 
│                ├ [1]  ╭ ID            : alpine-baselayout@3.7.1-r8 
│                │      ├ Name          : alpine-baselayout 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/alpine-baselayout@3.7.1-r8?arch=x86_64&distro=3
│                │      │                │       .23.0 
│                │      │                ╰ UID : bb9de5e77801798d 
│                │      ├ Version       : 3.7.1-r8 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : alpine-baselayout 
│                │      ├ SrcVersion    : 3.7.1-r8 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: alpine-baselayout-data@3.7.1-r8 
│                │      │                ╰ [1]: busybox-binsh@1.37.0-r29 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:9a137c3c8e738bcabac13326c9fc5472fa58aaf4 
│                │      ╰ InstalledFiles ╭ [0] : etc/motd 
│                │                       ├ [1] : etc/crontabs/root 
│                │                       ├ [2] : etc/modprobe.d/aliases.conf 
│                │                       ├ [3] : etc/modprobe.d/blacklist.conf 
│                │                       ├ [4] : etc/modprobe.d/i386.conf 
│                │                       ├ [5] : etc/profile.d/20locale.sh 
│                │                       ├ [6] : etc/profile.d/README 
│                │                       ├ [7] : etc/profile.d/color_prompt.sh.disabled 
│                │                       ├ [8] : usr/lib/sysctl.d/00-alpine.conf 
│                │                       ├ [9] : var/lock 
│                │                       ├ [10]: var/run 
│                │                       ├ [11]: var/spool/mail 
│                │                       ╰ [12]: var/spool/cron/crontabs 
│                ├ [2]  ╭ ID            : alpine-baselayout-data@3.7.1-r8 
│                │      ├ Name          : alpine-baselayout-data 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/alpine-baselayout-data@3.7.1-r8?arch=x86_64&dis
│                │      │                │       tro=3.23.0 
│                │      │                ╰ UID : aaf48747bbe2abe1 
│                │      ├ Version       : 3.7.1-r8 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : alpine-baselayout 
│                │      ├ SrcVersion    : 3.7.1-r8 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:9a60b0edb4559ab279cf004b7e685cfd78dd0c15 
│                │      ╰ InstalledFiles ╭ [0] : etc/fstab 
│                │                       ├ [1] : etc/group 
│                │                       ├ [2] : etc/hostname 
│                │                       ├ [3] : etc/hosts 
│                │                       ├ [4] : etc/inittab 
│                │                       ├ [5] : etc/modules 
│                │                       ├ [6] : etc/mtab 
│                │                       ├ [7] : etc/nsswitch.conf 
│                │                       ├ [8] : etc/passwd 
│                │                       ├ [9] : etc/profile 
│                │                       ├ [10]: etc/protocols 
│                │                       ├ [11]: etc/services 
│                │                       ├ [12]: etc/shadow 
│                │                       ├ [13]: etc/shells 
│                │                       ╰ [14]: etc/sysctl.conf 
│                ├ [3]  ╭ ID            : alpine-keys@2.6-r0 
│                │      ├ Name          : alpine-keys 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/alpine-keys@2.6-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 842a0d8aceb5c4a9 
│                │      ├ Version       : 2.6-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : alpine-keys 
│                │      ├ SrcVersion    : 2.6-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:e2b0ee196494dc3874f853370dff9451e3bd91d7 
│                │      ╰ InstalledFiles ╭ [0] : etc/apk/keys/alpine-devel@lists.alpinelinux.org-4a6a0840.rsa.pub 
│                │                       ├ [1] : etc/apk/keys/alpine-devel@lists.alpinelinux.org-5261cecb.rsa.pub 
│                │                       ├ [2] : etc/apk/keys/alpine-devel@lists.alpinelinux.org-6165ee59.rsa.pub 
│                │                       ├ [3] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-4a6a0840
│                │                       │       .rsa.pub 
│                │                       ├ [4] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-5243ef4b
│                │                       │       .rsa.pub 
│                │                       ├ [5] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-524d27bb
│                │                       │       .rsa.pub 
│                │                       ├ [6] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-5261cecb
│                │                       │       .rsa.pub 
│                │                       ├ [7] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-58199dcc
│                │                       │       .rsa.pub 
│                │                       ├ [8] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-58cbb476
│                │                       │       .rsa.pub 
│                │                       ├ [9] : usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-58e4f17d
│                │                       │       .rsa.pub 
│                │                       ├ [10]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-5e69ca50
│                │                       │       .rsa.pub 
│                │                       ├ [11]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-60ac2099
│                │                       │       .rsa.pub 
│                │                       ├ [12]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-6165ee59
│                │                       │       .rsa.pub 
│                │                       ├ [13]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-61666e3f
│                │                       │       .rsa.pub 
│                │                       ├ [14]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-616a9724
│                │                       │       .rsa.pub 
│                │                       ├ [15]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-616abc23
│                │                       │       .rsa.pub 
│                │                       ├ [16]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-616ac3bc
│                │                       │       .rsa.pub 
│                │                       ├ [17]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-616adfeb
│                │                       │       .rsa.pub 
│                │                       ├ [18]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-616ae350
│                │                       │       .rsa.pub 
│                │                       ├ [19]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-616db30d
│                │                       │       .rsa.pub 
│                │                       ├ [20]: usr/share/apk/keys/alpine-devel@lists.alpinelinux.org-66ba20fe
│                │                       │       .rsa.pub 
│                │                       ├ [21]: usr/share/apk/keys/aarch64/alpine-devel@lists.alpinelinux.org-
│                │                       │       58199dcc.rsa.pub 
│                │                       ├ [22]: usr/share/apk/keys/aarch64/alpine-devel@lists.alpinelinux.org-
│                │                       │       616ae350.rsa.pub 
│                │                       ├ [23]: usr/share/apk/keys/armhf/alpine-devel@lists.alpinelinux.org-52
│                │                       │       4d27bb.rsa.pub 
│                │                       ├ [24]: usr/share/apk/keys/armhf/alpine-devel@lists.alpinelinux.org-61
│                │                       │       6a9724.rsa.pub 
│                │                       ├ [25]: usr/share/apk/keys/armv7/alpine-devel@lists.alpinelinux.org-52
│                │                       │       4d27bb.rsa.pub 
│                │                       ├ [26]: usr/share/apk/keys/armv7/alpine-devel@lists.alpinelinux.org-61
│                │                       │       6adfeb.rsa.pub 
│                │                       ├ [27]: usr/share/apk/keys/loongarch64/alpine-devel@lists.alpinelinux.
│                │                       │       org-66ba20fe.rsa.pub 
│                │                       ├ [28]: usr/share/apk/keys/mips64/alpine-devel@lists.alpinelinux.org-5
│                │                       │       e69ca50.rsa.pub 
│                │                       ├ [29]: usr/share/apk/keys/ppc64le/alpine-devel@lists.alpinelinux.org-
│                │                       │       58cbb476.rsa.pub 
│                │                       ├ [30]: usr/share/apk/keys/ppc64le/alpine-devel@lists.alpinelinux.org-
│                │                       │       616abc23.rsa.pub 
│                │                       ├ [31]: usr/share/apk/keys/riscv64/alpine-devel@lists.alpinelinux.org-
│                │                       │       60ac2099.rsa.pub 
│                │                       ├ [32]: usr/share/apk/keys/riscv64/alpine-devel@lists.alpinelinux.org-
│                │                       │       616db30d.rsa.pub 
│                │                       ├ [33]: usr/share/apk/keys/s390x/alpine-devel@lists.alpinelinux.org-58
│                │                       │       e4f17d.rsa.pub 
│                │                       ├ [34]: usr/share/apk/keys/s390x/alpine-devel@lists.alpinelinux.org-61
│                │                       │       6ac3bc.rsa.pub 
│                │                       ├ [35]: usr/share/apk/keys/x86/alpine-devel@lists.alpinelinux.org-4a6a
│                │                       │       0840.rsa.pub 
│                │                       ├ [36]: usr/share/apk/keys/x86/alpine-devel@lists.alpinelinux.org-5243
│                │                       │       ef4b.rsa.pub 
│                │                       ├ [37]: usr/share/apk/keys/x86/alpine-devel@lists.alpinelinux.org-6166
│                │                       │       6e3f.rsa.pub 
│                │                       ├ [38]: usr/share/apk/keys/x86_64/alpine-devel@lists.alpinelinux.org-4
│                │                       │       a6a0840.rsa.pub 
│                │                       ├ [39]: usr/share/apk/keys/x86_64/alpine-devel@lists.alpinelinux.org-5
│                │                       │       261cecb.rsa.pub 
│                │                       ╰ [40]: usr/share/apk/keys/x86_64/alpine-devel@lists.alpinelinux.org-6
│                │                               165ee59.rsa.pub 
│                ├ [4]  ╭ ID            : alpine-release@3.23.0-r0 
│                │      ├ Name          : alpine-release 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/alpine-release@3.23.0-r0?arch=x86_64&distro=3.2
│                │      │                │       3.0 
│                │      │                ╰ UID : 57699070d22647ef 
│                │      ├ Version       : 3.23.0-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : alpine-base 
│                │      ├ SrcVersion    : 3.23.0-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: alpine-keys@2.6-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:d85ddacf795775c3637989a1a5e3332e1add193a 
│                │      ╰ InstalledFiles ╭ [0]: etc/alpine-release 
│                │                       ├ [1]: etc/issue 
│                │                       ├ [2]: etc/os-release 
│                │                       ├ [3]: etc/secfixes.d/alpine 
│                │                       ╰ [4]: usr/lib/os-release 
│                ├ [5]  ╭ ID            : apk-tools@3.0.1-r1 
│                │      ├ Name          : apk-tools 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/apk-tools@3.0.1-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : e4ee4f877446f21a 
│                │      ├ Version       : 3.0.1-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : apk-tools 
│                │      ├ SrcVersion    : 3.0.1-r1 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: ca-certificates-bundle@20251003-r0 
│                │      │                ├ [1]: libapk@3.0.1-r1 
│                │      │                ├ [2]: libcrypto3@3.5.4-r0 
│                │      │                ├ [3]: musl@1.2.5-r21 
│                │      │                ╰ [4]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:293b66be72bc80bee333375de1ef4ae6d0504056 
│                │      ╰ InstalledFiles ─ [0]: sbin/apk 
│                ├ [6]  ╭ ID            : apk-tools-bash-completion@3.0.1-r1 
│                │      ├ Name          : apk-tools-bash-completion 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/apk-tools-bash-completion@3.0.1-r1?arch=x86_64&
│                │      │                │       distro=3.23.0 
│                │      │                ╰ UID : 4e10e06fb4bd74dc 
│                │      ├ Version       : 3.0.1-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : apk-tools 
│                │      ├ SrcVersion    : 3.0.1-r1 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4571631abf06a754658f635f37244e5492ab9b97 
│                │      ╰ InstalledFiles ─ [0]: usr/share/bash-completion/completions/_apk 
│                ├ [7]  ╭ ID            : bash@5.3.3-r1 
│                │      ├ Name          : bash 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/bash@5.3.3-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 8d0b81bfa9e81d2d 
│                │      ├ Version       : 5.3.3-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : bash 
│                │      ├ SrcVersion    : 5.3.3-r1 
│                │      ├ Licenses       ─ [0]: GPL-3.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: busybox-binsh@1.37.0-r29 
│                │      │                ├ [1]: musl@1.2.5-r21 
│                │      │                ╰ [2]: readline@8.3.1-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:b0799b34b5652e00443d5be75f01263c575104f2 
│                │      ╰ InstalledFiles ╭ [0] : bin/bash 
│                │                       ├ [1] : etc/bash/bashrc 
│                │                       ├ [2] : etc/profile.d/00-bashrc.sh 
│                │                       ├ [3] : usr/lib/bash/accept 
│                │                       ├ [4] : usr/lib/bash/basename 
│                │                       ├ [5] : usr/lib/bash/chmod 
│                │                       ├ [6] : usr/lib/bash/csv 
│                │                       ├ [7] : usr/lib/bash/cut 
│                │                       ├ [8] : usr/lib/bash/dirname 
│                │                       ├ [9] : usr/lib/bash/dsv 
│                │                       ├ [10]: usr/lib/bash/fdflags 
│                │                       ├ [11]: usr/lib/bash/finfo 
│                │                       ├ [12]: usr/lib/bash/fltexpr 
│                │                       ├ [13]: usr/lib/bash/getconf 
│                │                       ├ [14]: usr/lib/bash/head 
│                │                       ├ [15]: usr/lib/bash/id 
│                │                       ├ [16]: usr/lib/bash/kv 
│                │                       ├ [17]: usr/lib/bash/ln 
│                │                       ├ [18]: usr/lib/bash/logname 
│                │                       ├ [19]: usr/lib/bash/mkdir 
│                │                       ├ [20]: usr/lib/bash/mkfifo 
│                │                       ├ [21]: usr/lib/bash/mktemp 
│                │                       ├ [22]: usr/lib/bash/mypid 
│                │                       ├ [23]: usr/lib/bash/pathchk 
│                │                       ├ [24]: usr/lib/bash/print 
│                │                       ├ [25]: usr/lib/bash/printenv 
│                │                       ├ [26]: usr/lib/bash/push 
│                │                       ├ [27]: usr/lib/bash/realpath 
│                │                       ├ [28]: usr/lib/bash/rm 
│                │                       ├ [29]: usr/lib/bash/rmdir 
│                │                       ├ [30]: usr/lib/bash/seq 
│                │                       ├ [31]: usr/lib/bash/setpgid 
│                │                       ├ [32]: usr/lib/bash/sleep 
│                │                       ├ [33]: usr/lib/bash/stat 
│                │                       ├ [34]: usr/lib/bash/strftime 
│                │                       ├ [35]: usr/lib/bash/strptime 
│                │                       ├ [36]: usr/lib/bash/sync 
│                │                       ├ [37]: usr/lib/bash/tee 
│                │                       ├ [38]: usr/lib/bash/truefalse 
│                │                       ├ [39]: usr/lib/bash/tty 
│                │                       ├ [40]: usr/lib/bash/uname 
│                │                       ├ [41]: usr/lib/bash/unlink 
│                │                       ╰ [42]: usr/lib/bash/whoami 
│                ├ [8]  ╭ ID            : bash-completion@2.17.0-r0 
│                │      ├ Name          : bash-completion 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/bash-completion@2.17.0-r0?arch=x86_64&distro=3.
│                │      │                │       23.0 
│                │      │                ╰ UID : b7ca1d45213563f9 
│                │      ├ Version       : 2.17.0-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : bash-completion 
│                │      ├ SrcVersion    : 2.17.0-r0 
│                │      ├ Licenses       ─ [0]: GPL-2.0-or-later 
│                │      ├ Maintainer    : Achill Gilgenast <achill@achill.org> 
│                │      ├ DependsOn      ─ [0]: bash@5.3.3-r1 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:ee60c781d46581d25847465f2c996acaaf3a277e 
│                │      ╰ InstalledFiles ╭ [0]   : etc/bash/bash_completion.sh 
│                │                       ├ [1]   : etc/bash_completion.d/000_bash_completion_compat.bash 
│                │                       ├ [2]   : usr/share/bash-completion/bash_completion 
│                │                       ├ [3]   : usr/share/bash-completion/completions/2to3 
│                │                       ├ [4]   : usr/share/bash-completion/completions/7z 
│                │                       ├ [5]   : usr/share/bash-completion/completions/7za 
│                │                       ├ [6]   : usr/share/bash-completion/completions/7zr 
│                │                       ├ [7]   : usr/share/bash-completion/completions/7zz 
│                │                       ├ [8]   : usr/share/bash-completion/completions/7zzs 
│                │                       ├ [9]   : usr/share/bash-completion/completions/_airflow 
│                │                       ├ [10]  : usr/share/bash-completion/completions/_allero 
│                │                       ├ [11]  : usr/share/bash-completion/completions/_alp 
│                │                       ├ [12]  : usr/share/bash-completion/completions/_ansible 
│                │                       ├ [13]  : usr/share/bash-completion/completions/_ansible-config 
│                │                       ├ [14]  : usr/share/bash-completion/completions/_ansible-console 
│                │                       ├ [15]  : usr/share/bash-completion/completions/_ansible-doc 
│                │                       ├ [16]  : usr/share/bash-completion/completions/_ansible-galaxy 
│                │                       ├ [17]  : usr/share/bash-completion/completions/_ansible-inventory 
│                │                       ├ [18]  : usr/share/bash-completion/completions/_ansible-playbook 
│                │                       ├ [19]  : usr/share/bash-completion/completions/_ansible-pull 
│                │                       ├ [20]  : usr/share/bash-completion/completions/_ansible-vault 
│                │                       ├ [21]  : usr/share/bash-completion/completions/_apko 
│                │                       ├ [22]  : usr/share/bash-completion/completions/_aqua 
│                │                       ├ [23]  : usr/share/bash-completion/completions/_arduino-cli 
│                │                       ├ [24]  : usr/share/bash-completion/completions/_argc 
│                │                       ├ [25]  : usr/share/bash-completion/completions/_argo 
│                │                       ├ [26]  : usr/share/bash-completion/completions/_asdf 
│                │                       ├ [27]  : usr/share/bash-completion/completions/_atlas 
│                │                       ├ [28]  : usr/share/bash-completion/completions/_atmos 
│                │                       ├ [29]  : usr/share/bash-completion/completions/_bao 
│                │                       ├ [30]  : usr/share/bash-completion/completions/_bashbot 
│                │                       ├ [31]  : usr/share/bash-completion/completions/_black 
│                │                       ├ [32]  : usr/share/bash-completion/completions/_blackd 
│                │                       ├ [33]  : usr/share/bash-completion/completions/_bombadil 
│                │                       ├ [34]  : usr/share/bash-completion/completions/_bosh 
│                │                       ├ [35]  : usr/share/bash-completion/completions/_buf 
│                │                       ├ [36]  : usr/share/bash-completion/completions/_caddy 
│                │                       ├ [37]  : usr/share/bash-completion/completions/_cal 
│                │                       ├ [38]  : usr/share/bash-completion/completions/_cargo 
│                │                       ├ [39]  : usr/share/bash-completion/completions/_chamber 
│                │                       ├ [40]  : usr/share/bash-completion/completions/_changie 
│                │                       ├ [41]  : usr/share/bash-completion/completions/_chezmoi 
│                │                       ├ [42]  : usr/share/bash-completion/completions/_chfn 
│                │                       ├ [43]  : usr/share/bash-completion/completions/_chsh 
│                │                       ├ [44]  : usr/share/bash-completion/completions/_cilium 
│                │                       ├ [45]  : usr/share/bash-completion/completions/_cloudquery 
│                │                       ├ [46]  : usr/share/bash-completion/completions/_clusterctl 
│                │                       ├ [47]  : usr/share/bash-completion/completions/_cmctl 
│                │                       ├ [48]  : usr/share/bash-completion/completions/_coder 
│                │                       ├ [49]  : usr/share/bash-completion/completions/_colima 
│                │                       ├ [50]  : usr/share/bash-completion/completions/_conda 
│                │                       ├ [51]  : usr/share/bash-completion/completions/_conform 
│                │                       ├ [52]  : usr/share/bash-completion/completions/_conftest 
│                │                       ├ [53]  : usr/share/bash-completion/completions/_constellation 
│                │                       ├ [54]  : usr/share/bash-completion/completions/_consul 
│                │                       ├ [55]  : usr/share/bash-completion/completions/_container-structure-t
│                │                       │         est 
│                │                       ├ [56]  : usr/share/bash-completion/completions/_cosign 
│                │                       ├ [57]  : usr/share/bash-completion/completions/_crane 
│                │                       ├ [58]  : usr/share/bash-completion/completions/_crc 
│                │                       ├ [59]  : usr/share/bash-completion/completions/_crictl 
│                │                       ├ [60]  : usr/share/bash-completion/completions/_ctlptl 
│                │                       ├ [61]  : usr/share/bash-completion/completions/_cue 
│                │                       ├ [62]  : usr/share/bash-completion/completions/_cz 
│                │                       ├ [63]  : usr/share/bash-completion/completions/_dagger 
│                │                       ├ [64]  : usr/share/bash-completion/completions/_dapr 
│                │                       ├ [65]  : usr/share/bash-completion/completions/_dasel 
│                │                       ├ [66]  : usr/share/bash-completion/completions/_datree 
│                │                       ├ [67]  : usr/share/bash-completion/completions/_deck 
│                │                       ├ [68]  : usr/share/bash-completion/completions/_delta 
│                │                       ├ [69]  : usr/share/bash-completion/completions/_deno 
│                │                       ├ [70]  : usr/share/bash-completion/completions/_depot 
│                │                       ├ [71]  : usr/share/bash-completion/completions/_devspace 
│                │                       ├ [72]  : usr/share/bash-completion/completions/_diesel 
│                │                       ├ [73]  : usr/share/bash-completion/completions/_diffoci 
│                │                       ├ [74]  : usr/share/bash-completion/completions/_dlv 
│                │                       ├ [75]  : usr/share/bash-completion/completions/_dmesg 
│                │                       ├ [76]  : usr/share/bash-completion/completions/_docker 
│                │                       ├ [77]  : usr/share/bash-completion/completions/_dprint 
│                │                       ├ [78]  : usr/share/bash-completion/completions/_driftctl 
│                │                       ├ [79]  : usr/share/bash-completion/completions/_dyff 
│                │                       ├ [80]  : usr/share/bash-completion/completions/_eject 
│                │                       ├ [81]  : usr/share/bash-completion/completions/_esc 
│                │                       ├ [82]  : usr/share/bash-completion/completions/_flamegraph 
│                │                       ├ [83]  : usr/share/bash-completion/completions/_flask 
│                │                       ├ [84]  : usr/share/bash-completion/completions/_flux 
│                │                       ├ [85]  : usr/share/bash-completion/completions/_furyctl 
│                │                       ├ [86]  : usr/share/bash-completion/completions/_fx 
│                │                       ├ [87]  : usr/share/bash-completion/completions/_gaiacli 
│                │                       ├ [88]  : usr/share/bash-completion/completions/_gaiad 
│                │                       ├ [89]  : usr/share/bash-completion/completions/_gardenctl 
│                │                       ├ [90]  : usr/share/bash-completion/completions/_gcrane 
│                │                       ├ [91]  : usr/share/bash-completion/completions/_gh 
│                │                       ├ [92]  : usr/share/bash-completion/completions/_gh-label 
│                │                       ├ [93]  : usr/share/bash-completion/completions/_ghorg 
│                │                       ├ [94]  : usr/share/bash-completion/completions/_git-bump 
│                │                       ├ [95]  : usr/share/bash-completion/completions/_gitconfig 
│                │                       ├ [96]  : usr/share/bash-completion/completions/_gitleaks 
│                │                       ├ [97]  : usr/share/bash-completion/completions/_gitsign 
│                │                       ├ [98]  : usr/share/bash-completion/completions/_glab 
│                │                       ├ [99]  : usr/share/bash-completion/completions/_glances 
│                │                       ├ [100] : usr/share/bash-completion/completions/_glen 
│                │                       ├ [101] : usr/share/bash-completion/completions/_glow 
│                │                       ├ [102] : usr/share/bash-completion/completions/_go-licenses 
│                │                       ├ [103] : usr/share/bash-completion/completions/_golangci-lint 
│                │                       ├ [104] : usr/share/bash-completion/completions/_gomarklint 
│                │                       ├ [105] : usr/share/bash-completion/completions/_gopass 
│                │                       ├ [106] : usr/share/bash-completion/completions/_gopherjs 
│                │                       ├ [107] : usr/share/bash-completion/completions/_goreleaser 
│                │                       ├ [108] : usr/share/bash-completion/completions/_grype 
│                │                       ├ [109] : usr/share/bash-completion/completions/_gsctl 
│                │                       ├ [110] : usr/share/bash-completion/completions/_gup 
│                │                       ├ [111] : usr/share/bash-completion/completions/_helm 
│                │                       ├ [112] : usr/share/bash-completion/completions/_helmfile 
│                │                       ├ [113] : usr/share/bash-completion/completions/_hexdump 
│                │                       ├ [114] : usr/share/bash-completion/completions/_hostctl 
│                │                       ├ [115] : usr/share/bash-completion/completions/_httpx 
│                │                       ├ [116] : usr/share/bash-completion/completions/_hugo 
│                │                       ├ [117] : usr/share/bash-completion/completions/_hwclock 
│                │                       ├ [118] : usr/share/bash-completion/completions/_ignite 
│                │                       ├ [119] : usr/share/bash-completion/completions/_imgpkg 
│                │                       ├ [120] : usr/share/bash-completion/completions/_incus 
│                │                       ├ [121] : usr/share/bash-completion/completions/_infracost 
│                │                       ├ [122] : usr/share/bash-completion/completions/_insmod 
│                │                       ├ [123] : usr/share/bash-completion/completions/_insmod.static 
│                │                       ├ [124] : usr/share/bash-completion/completions/_ionice 
│                │                       ├ [125] : usr/share/bash-completion/completions/_istioctl 
│                │                       ├ [126] : usr/share/bash-completion/completions/_jj 
│                │                       ├ [127] : usr/share/bash-completion/completions/_jungle 
│                │                       ├ [128] : usr/share/bash-completion/completions/_just 
│                │                       ├ [129] : usr/share/bash-completion/completions/_jwt 
│                │                       ├ [130] : usr/share/bash-completion/completions/_k0sctl 
│                │                       ├ [131] : usr/share/bash-completion/completions/_k3d 
│                │                       ├ [132] : usr/share/bash-completion/completions/_k3s 
│                │                       ├ [133] : usr/share/bash-completion/completions/_k3sup 
│                │                       ├ [134] : usr/share/bash-completion/completions/_k6 
│                │                       ├ [135] : usr/share/bash-completion/completions/_k9s 
│                │                       ├ [136] : usr/share/bash-completion/completions/_kafkactl 
│                │                       ├ [137] : usr/share/bash-completion/completions/_kapp 
│                │                       ├ [138] : usr/share/bash-completion/completions/_kata-runtime 
│                │                       ├ [139] : usr/share/bash-completion/completions/_kconf 
│                │                       ├ [140] : usr/share/bash-completion/completions/_keyring 
│                │                       ├ [141] : usr/share/bash-completion/completions/_kind 
│                │                       ├ [142] : usr/share/bash-completion/completions/_kn 
│                │                       ├ [143] : usr/share/bash-completion/completions/_ko 
│                │                       ├ [144] : usr/share/bash-completion/completions/_kompose 
│                │                       ├ [145] : usr/share/bash-completion/completions/_kontena 
│                │                       ├ [146] : usr/share/bash-completion/completions/_kool 
│                │                       ├ [147] : usr/share/bash-completion/completions/_kops 
│                │                       ├ [148] : usr/share/bash-completion/completions/_krane 
│                │                       ├ [149] : usr/share/bash-completion/completions/_kratos 
│                │                       ├ [150] : usr/share/bash-completion/completions/_kube-capacity 
│                │                       ├ [151] : usr/share/bash-completion/completions/_kube-linter 
│                │                       ├ [152] : usr/share/bash-completion/completions/_kubeadm 
│                │                       ├ [153] : usr/share/bash-completion/completions/_kubebuilder 
│                │                       ├ [154] : usr/share/bash-completion/completions/_kubecm 
│                │                       ├ [155] : usr/share/bash-completion/completions/_kubectl 
│                │                       ├ [156] : usr/share/bash-completion/completions/_kubectl-argo-rollouts 
│                │                       ├ [157] : usr/share/bash-completion/completions/_kubectl-kuttl 
│                │                       ├ [158] : usr/share/bash-completion/completions/_kubelogin 
│                │                       ├ [159] : usr/share/bash-completion/completions/_kubemqctl 
│                │                       ├ [160] : usr/share/bash-completion/completions/_kubescape 
│                │                       ├ [161] : usr/share/bash-completion/completions/_kubesec 
│                │                       ├ [162] : usr/share/bash-completion/completions/_kubeshark 
│                │                       ├ [163] : usr/share/bash-completion/completions/_kubespy 
│                │                       ├ [164] : usr/share/bash-completion/completions/_kustomize 
│                │                       ├ [165] : usr/share/bash-completion/completions/_kyverno 
│                │                       ├ [166] : usr/share/bash-completion/completions/_lefthook 
│                │                       ├ [167] : usr/share/bash-completion/completions/_limactl 
│                │                       ├ [168] : usr/share/bash-completion/completions/_linkerd 
│                │                       ├ [169] : usr/share/bash-completion/completions/_look 
│                │                       ├ [170] : usr/share/bash-completion/completions/_mado 
│                │                       ├ [171] : usr/share/bash-completion/completions/_mattermost 
│                │                       ├ [172] : usr/share/bash-completion/completions/_mdbook 
│                │                       ├ [173] : usr/share/bash-completion/completions/_melange 
│                │                       ├ [174] : usr/share/bash-completion/completions/_metalctl 
│                │                       ├ [175] : usr/share/bash-completion/completions/_minikube 
│                │                       ├ [176] : usr/share/bash-completion/completions/_minishift 
│                │                       ├ [177] : usr/share/bash-completion/completions/_mise 
│                │                       ├ [178] : usr/share/bash-completion/completions/_mmctl 
│                │                       ├ [179] : usr/share/bash-completion/completions/_mock 
│                │                       ├ [180] : usr/share/bash-completion/completions/_mockery 
│                │                       ├ [181] : usr/share/bash-completion/completions/_modinfo 
│                │                       ├ [182] : usr/share/bash-completion/completions/_modprobe 
│                │                       ├ [183] : usr/share/bash-completion/completions/_modules 
│                │                       ├ [184] : usr/share/bash-completion/completions/_moldy 
│                │                       ├ [185] : usr/share/bash-completion/completions/_mount 
│                │                       ├ [186] : usr/share/bash-completion/completions/_mount.linux 
│                │                       ├ [187] : usr/share/bash-completion/completions/_mtr 
│                │                       ├ [188] : usr/share/bash-completion/completions/_multi-gitter 
│                │                       ├ [189] : usr/share/bash-completion/completions/_nerdctl 
│                │                       ├ [190] : usr/share/bash-completion/completions/_newgrp 
│                │                       ├ [191] : usr/share/bash-completion/completions/_nfpm 
│                │                       ├ [192] : usr/share/bash-completion/completions/_ngrok 
│                │                       ├ [193] : usr/share/bash-completion/completions/_nmcli 
│                │                       ├ [194] : usr/share/bash-completion/completions/_nomad 
│                │                       ├ [195] : usr/share/bash-completion/completions/_notation 
│                │                       ├ [196] : usr/share/bash-completion/completions/_nova 
│                │                       ├ [197] : usr/share/bash-completion/completions/_nox 
│                │                       ├ [198] : usr/share/bash-completion/completions/_npm 
│                │                       ├ [199] : usr/share/bash-completion/completions/_nvm 
│                │                       ├ [200] : usr/share/bash-completion/completions/_oc 
│                │                       ├ [201] : usr/share/bash-completion/completions/_odo 
│                │                       ├ [202] : usr/share/bash-completion/completions/_okteto 
│                │                       ├ [203] : usr/share/bash-completion/completions/_op 
│                │                       ├ [204] : usr/share/bash-completion/completions/_opa 
│                │                       ├ [205] : usr/share/bash-completion/completions/_oras 
│                │                       ├ [206] : usr/share/bash-completion/completions/_ory 
│                │                       ├ [207] : usr/share/bash-completion/completions/_packer 
│                │                       ├ [208] : usr/share/bash-completion/completions/_pip 
│                │                       ├ [209] : usr/share/bash-completion/completions/_pip3 
│                │                       ├ [210] : usr/share/bash-completion/completions/_pipenv 
│                │                       ├ [211] : usr/share/bash-completion/completions/_pitchfork 
│                │                       ├ [212] : usr/share/bash-completion/completions/_pluto 
│                │                       ├ [213] : usr/share/bash-completion/completions/_polygon-edge 
│                │                       ├ [214] : usr/share/bash-completion/completions/_popeye 
│                │                       ├ [215] : usr/share/bash-completion/completions/_pulumi 
│                │                       ├ [216] : usr/share/bash-completion/completions/_px 
│                │                       ├ [217] : usr/share/bash-completion/completions/_qrpc 
│                │                       ├ [218] : usr/share/bash-completion/completions/_random 
│                │                       ├ [219] : usr/share/bash-completion/completions/_rclone 
│                │                       ├ [220] : usr/share/bash-completion/completions/_regal 
│                │                       ├ [221] : usr/share/bash-completion/completions/_regctl 
│                │                       ├ [222] : usr/share/bash-completion/completions/_renice 
│                │                       ├ [223] : usr/share/bash-completion/completions/_repomanage 
│                │                       ├ [224] : usr/share/bash-completion/completions/_reptyr 
│                │                       ├ [225] : usr/share/bash-completion/completions/_rfkill 
│                │                       ├ [226] : usr/share/bash-completion/completions/_rg 
│                │                       ├ [227] : usr/share/bash-completion/completions/_rmmod 
│                │                       ├ [228] : usr/share/bash-completion/completions/_rtcwake 
│                │                       ├ [229] : usr/share/bash-completion/completions/_ruff 
│                │                       ├ [230] : usr/share/bash-completion/completions/_runuser 
│                │                       ├ [231] : usr/share/bash-completion/completions/_rustic 
│                │                       ├ [232] : usr/share/bash-completion/completions/_rustup 
│                │                       ├ [233] : usr/share/bash-completion/completions/_secret-tool 
│                │                       ├ [234] : usr/share/bash-completion/completions/_sentry-cli 
│                │                       ├ [235] : usr/share/bash-completion/completions/_shtab 
│                │                       ├ [236] : usr/share/bash-completion/completions/_sinker 
│                │                       ├ [237] : usr/share/bash-completion/completions/_skaffold 
│                │                       ├ [238] : usr/share/bash-completion/completions/_slackpkg 
│                │                       ├ [239] : usr/share/bash-completion/completions/_slsa-verifier 
│                │                       ├ [240] : usr/share/bash-completion/completions/_sops 
│                │                       ├ [241] : usr/share/bash-completion/completions/_sopstool 
│                │                       ├ [242] : usr/share/bash-completion/completions/_spacectl 
│                │                       ├ [243] : usr/share/bash-completion/completions/_ssh-inscribe 
│                │                       ├ [244] : usr/share/bash-completion/completions/_sshi 
│                │                       ├ [245] : usr/share/bash-completion/completions/_starship 
│                │                       ├ [246] : usr/share/bash-completion/completions/_steampipe 
│                │                       ├ [247] : usr/share/bash-completion/completions/_stern 
│                │                       ├ [248] : usr/share/bash-completion/completions/_stripe 
│                │                       ├ [249] : usr/share/bash-completion/completions/_su 
│                │                       ├ [250] : usr/share/bash-completion/completions/_svn 
│                │                       ├ [251] : usr/share/bash-completion/completions/_svnadmin 
│                │                       ├ [252] : usr/share/bash-completion/completions/_svnlook 
│                │                       ├ [253] : usr/share/bash-completion/completions/_syft 
│                │                       ├ [254] : usr/share/bash-completion/completions/_talhelper 
│                │                       ├ [255] : usr/share/bash-completion/completions/_tanzu 
│                │                       ├ [256] : usr/share/bash-completion/completions/_tanzu-core 
│                │                       ├ [257] : usr/share/bash-completion/completions/_task 
│                │                       ├ [258] : usr/share/bash-completion/completions/_tctl 
│                │                       ├ [259] : usr/share/bash-completion/completions/_tendermint 
│                │                       ├ [260] : usr/share/bash-completion/completions/_terraform 
│                │                       ├ [261] : usr/share/bash-completion/completions/_tfctl 
│                │                       ├ [262] : usr/share/bash-completion/completions/_tilt 
│                │                       ├ [263] : usr/share/bash-completion/completions/_timoni 
│                │                       ├ [264] : usr/share/bash-completion/completions/_tkn 
│                │                       ├ [265] : usr/share/bash-completion/completions/_tkn-pac 
│                │                       ├ [266] : usr/share/bash-completion/completions/_tldr 
│                │                       ├ [267] : usr/share/bash-completion/completions/_todoist 
│                │                       ├ [268] : usr/share/bash-completion/completions/_tofu 
│                │                       ├ [269] : usr/share/bash-completion/completions/_tokio-console 
│                │                       ├ [270] : usr/share/bash-completion/completions/_trash 
│                │                       ├ [271] : usr/share/bash-completion/completions/_trash-empty 
│                │                       ├ [272] : usr/share/bash-completion/completions/_trash-list 
│                │                       ├ [273] : usr/share/bash-completion/completions/_trash-put 
│                │                       ├ [274] : usr/share/bash-completion/completions/_trash-restore 
│                │                       ├ [275] : usr/share/bash-completion/completions/_trivy 
│                │                       ├ [276] : usr/share/bash-completion/completions/_udevadm 
│                │                       ├ [277] : usr/share/bash-completion/completions/_umount 
│                │                       ├ [278] : usr/share/bash-completion/completions/_umount.linux 
│                │                       ├ [279] : usr/share/bash-completion/completions/_upctl 
│                │                       ├ [280] : usr/share/bash-completion/completions/_uv 
│                │                       ├ [281] : usr/share/bash-completion/completions/_uvx 
│                │                       ├ [282] : usr/share/bash-completion/completions/_vacuum 
│                │                       ├ [283] : usr/share/bash-completion/completions/_vault 
│                │                       ├ [284] : usr/share/bash-completion/completions/_vela 
│                │                       ├ [285] : usr/share/bash-completion/completions/_velero 
│                │                       ├ [286] : usr/share/bash-completion/completions/_venom 
│                │                       ├ [287] : usr/share/bash-completion/completions/_virtctl 
│                │                       ├ [288] : usr/share/bash-completion/completions/_wasmer 
│                │                       ├ [289] : usr/share/bash-completion/completions/_wasmer-headless 
│                │                       ├ [290] : usr/share/bash-completion/completions/_watchexec 
│                │                       ├ [291] : usr/share/bash-completion/completions/_write 
│                │                       ├ [292] : usr/share/bash-completion/completions/_xc 
│                │                       ├ [293] : usr/share/bash-completion/completions/_xm 
│                │                       ├ [294] : usr/share/bash-completion/completions/_yq 
│                │                       ├ [295] : usr/share/bash-completion/completions/_ytt 
│                │                       ├ [296] : usr/share/bash-completion/completions/_yum 
│                │                       ├ [297] : usr/share/bash-completion/completions/_zarf 
│                │                       ├ [298] : usr/share/bash-completion/completions/_zitadel 
│                │                       ├ [299] : usr/share/bash-completion/completions/_zola 
│                │                       ├ [300] : usr/share/bash-completion/completions/a2x 
│                │                       ├ [301] : usr/share/bash-completion/completions/abook 
│                │                       ├ [302] : usr/share/bash-completion/completions/aclocal 
│                │                       ├ [303] : usr/share/bash-completion/completions/aclocal-1.10 
│                │                       ├ [304] : usr/share/bash-completion/completions/aclocal-1.11 
│                │                       ├ [305] : usr/share/bash-completion/completions/aclocal-1.12 
│                │                       ├ [306] : usr/share/bash-completion/completions/aclocal-1.13 
│                │                       ├ [307] : usr/share/bash-completion/completions/aclocal-1.14 
│                │                       ├ [308] : usr/share/bash-completion/completions/aclocal-1.15 
│                │                       ├ [309] : usr/share/bash-completion/completions/aclocal-1.16 
│                │                       ├ [310] : usr/share/bash-completion/completions/acpi 
│                │                       ├ [311] : usr/share/bash-completion/completions/add_members 
│                │                       ├ [312] : usr/share/bash-completion/completions/alias 
│                │                       ├ [313] : usr/share/bash-completion/completions/alpine 
│                │                       ├ [314] : usr/share/bash-completion/completions/alternatives 
│                │                       ├ [315] : usr/share/bash-completion/completions/animate 
│                │                       ├ [316] : usr/share/bash-completion/completions/ant 
│                │                       ├ [317] : usr/share/bash-completion/completions/apache2ctl 
│                │                       ├ [318] : usr/share/bash-completion/completions/appdata-validate 
│                │                       ├ [319] : usr/share/bash-completion/completions/apropos 
│                │                       ├ [320] : usr/share/bash-completion/completions/apt-build 
│                │                       ├ [321] : usr/share/bash-completion/completions/apt-cache 
│                │                       ├ [322] : usr/share/bash-completion/completions/apt-get 
│                │                       ├ [323] : usr/share/bash-completion/completions/apt-mark 
│                │                       ├ [324] : usr/share/bash-completion/completions/aptitude 
│                │                       ├ [325] : usr/share/bash-completion/completions/aptitude-curses 
│                │                       ├ [326] : usr/share/bash-completion/completions/arch 
│                │                       ├ [327] : usr/share/bash-completion/completions/arm-koji 
│                │                       ├ [328] : usr/share/bash-completion/completions/arp 
│                │                       ├ [329] : usr/share/bash-completion/completions/arping 
│                │                       ├ [330] : usr/share/bash-completion/completions/arpspoof 
│                │                       ├ [331] : usr/share/bash-completion/completions/asciidoc 
│                │                       ├ [332] : usr/share/bash-completion/completions/asciidoc.py 
│                │                       ├ [333] : usr/share/bash-completion/completions/aspell 
│                │                       ├ [334] : usr/share/bash-completion/completions/autoconf 
│                │                       ├ [335] : usr/share/bash-completion/completions/autoheader 
│                │                       ├ [336] : usr/share/bash-completion/completions/automake 
│                │                       ├ [337] : usr/share/bash-completion/completions/automake-1.10 
│                │                       ├ [338] : usr/share/bash-completion/completions/automake-1.11 
│                │                       ├ [339] : usr/share/bash-completion/completions/automake-1.12 
│                │                       ├ [340] : usr/share/bash-completion/completions/automake-1.13 
│                │                       ├ [341] : usr/share/bash-completion/completions/automake-1.14 
│                │                       ├ [342] : usr/share/bash-completion/completions/automake-1.15 
│                │                       ├ [343] : usr/share/bash-completion/completions/automake-1.16 
│                │                       ├ [344] : usr/share/bash-completion/completions/autoreconf 
│                │                       ├ [345] : usr/share/bash-completion/completions/autorpm 
│                │                       ├ [346] : usr/share/bash-completion/completions/autoscan 
│                │                       ├ [347] : usr/share/bash-completion/completions/autossh 
│                │                       ├ [348] : usr/share/bash-completion/completions/autoupdate 
│                │                       ├ [349] : usr/share/bash-completion/completions/avahi-browse 
│                │                       ├ [350] : usr/share/bash-completion/completions/avahi-browse-domains 
│                │                       ├ [351] : usr/share/bash-completion/completions/avctrl 
│                │                       ├ [352] : usr/share/bash-completion/completions/b2sum 
│                │                       ├ [353] : usr/share/bash-completion/completions/badblocks 
│                │                       ├ [354] : usr/share/bash-completion/completions/bind 
│                │                       ├ [355] : usr/share/bash-completion/completions/bk 
│                │                       ├ [356] : usr/share/bash-completion/completions/bmake 
│                │                       ├ [357] : usr/share/bash-completion/completions/brave 
│                │                       ├ [358] : usr/share/bash-completion/completions/brave-browser 
│                │                       ├ [359] : usr/share/bash-completion/completions/brctl 
│                │                       ├ [360] : usr/share/bash-completion/completions/bsdtar 
│                │                       ├ [361] : usr/share/bash-completion/completions/btdownloadcurses.py 
│                │                       ├ [362] : usr/share/bash-completion/completions/btdownloadgui.py 
│                │                       ├ [363] : usr/share/bash-completion/completions/btdownloadheadless.py 
│                │                       ├ [364] : usr/share/bash-completion/completions/bts 
│                │                       ├ [365] : usr/share/bash-completion/completions/bzip2 
│                │                       ├ [366] : usr/share/bash-completion/completions/c++ 
│                │                       ├ [367] : usr/share/bash-completion/completions/cancel 
│                │                       ├ [368] : usr/share/bash-completion/completions/cardctl 
│                │                       ├ [369] : usr/share/bash-completion/completions/carton 
│                │                       ├ [370] : usr/share/bash-completion/completions/cc 
│                │                       ├ [371] : usr/share/bash-completion/completions/ccache 
│                │                       ├ [372] : usr/share/bash-completion/completions/ccze 
│                │                       ├ [373] : usr/share/bash-completion/completions/cd 
│                │                       ├ [374] : usr/share/bash-completion/completions/cdrecord 
│                │                       ├ [375] : usr/share/bash-completion/completions/cfagent 
│                │                       ├ [376] : usr/share/bash-completion/completions/cfrun 
│                │                       ├ [377] : usr/share/bash-completion/completions/chage 
│                │                       ├ [378] : usr/share/bash-completion/completions/change_pw 
│                │                       ├ [379] : usr/share/bash-completion/completions/check_db 
│                │                       ├ [380] : usr/share/bash-completion/completions/check_perms 
│                │                       ├ [381] : usr/share/bash-completion/completions/checksec 
│                │                       ├ [382] : usr/share/bash-completion/completions/chflags 
│                │                       ├ [383] : usr/share/bash-completion/completions/chgrp 
│                │                       ├ [384] : usr/share/bash-completion/completions/chkconfig 
│                │                       ├ [385] : usr/share/bash-completion/completions/chmod 
│                │                       ├ [386] : usr/share/bash-completion/completions/chown 
│                │                       ├ [387] : usr/share/bash-completion/completions/chpasswd 
│                │                       ├ [388] : usr/share/bash-completion/completions/chrome 
│                │                       ├ [389] : usr/share/bash-completion/completions/chromium 
│                │                       ├ [390] : usr/share/bash-completion/completions/chromium-browser 
│                │                       ├ [391] : usr/share/bash-completion/completions/chronyc 
│                │                       ├ [392] : usr/share/bash-completion/completions/chrpath 
│                │                       ├ [393] : usr/share/bash-completion/completions/ci 
│                │                       ├ [394] : usr/share/bash-completion/completions/ciptool 
│                │                       ├ [395] : usr/share/bash-completion/completions/civclient 
│                │                       ├ [396] : usr/share/bash-completion/completions/civserver 
│                │                       ├ [397] : usr/share/bash-completion/completions/cksfv 
│                │                       ├ [398] : usr/share/bash-completion/completions/cksum 
│                │                       ├ [399] : usr/share/bash-completion/completions/cleanarch 
│                │                       ├ [400] : usr/share/bash-completion/completions/clisp 
│                │                       ├ [401] : usr/share/bash-completion/completions/clone_member 
│                │                       ├ [402] : usr/share/bash-completion/completions/clzip 
│                │                       ├ [403] : usr/share/bash-completion/completions/co 
│                │                       ├ [404] : usr/share/bash-completion/completions/colormake 
│                │                       ├ [405] : usr/share/bash-completion/completions/compare 
│                │                       ├ [406] : usr/share/bash-completion/completions/compgen 
│                │                       ├ [407] : usr/share/bash-completion/completions/complete 
│                │                       ├ [408] : usr/share/bash-completion/completions/composite 
│                │                       ├ [409] : usr/share/bash-completion/completions/config_list 
│                │                       ├ [410] : usr/share/bash-completion/completions/configure 
│                │                       ├ [411] : usr/share/bash-completion/completions/conjure 
│                │                       ├ [412] : usr/share/bash-completion/completions/convert 
│                │                       ├ [413] : usr/share/bash-completion/completions/cowsay 
│                │                       ├ [414] : usr/share/bash-completion/completions/cowthink 
│                │                       ├ [415] : usr/share/bash-completion/completions/cpan2dist 
│                │                       ├ [416] : usr/share/bash-completion/completions/cpio 
│                │                       ├ [417] : usr/share/bash-completion/completions/cppcheck 
│                │                       ├ [418] : usr/share/bash-completion/completions/createdb 
│                │                       ├ [419] : usr/share/bash-completion/completions/createuser 
│                │                       ├ [420] : usr/share/bash-completion/completions/crontab 
│                │                       ├ [421] : usr/share/bash-completion/completions/cryptsetup 
│                │                       ├ [422] : usr/share/bash-completion/completions/curl 
│                │                       ├ [423] : usr/share/bash-completion/completions/cvs 
│                │                       ├ [424] : usr/share/bash-completion/completions/cvsps 
│                │                       ├ [425] : usr/share/bash-completion/completions/dcop 
│                │                       ├ [426] : usr/share/bash-completion/completions/dd 
│                │                       ├ [427] : usr/share/bash-completion/completions/declare 
│                │                       ├ [428] : usr/share/bash-completion/completions/deja-dup 
│                │                       ├ [429] : usr/share/bash-completion/completions/desktop-file-validate 
│                │                       ├ [430] : usr/share/bash-completion/completions/dfutool 
│                │                       ├ [431] : usr/share/bash-completion/completions/dhclient 
│                │                       ├ [432] : usr/share/bash-completion/completions/dict 
│                │                       ├ [433] : usr/share/bash-completion/completions/display 
│                │                       ├ [434] : usr/share/bash-completion/completions/dmypy 
│                │                       ├ [435] : usr/share/bash-completion/completions/dnssec-keygen 
│                │                       ├ [436] : usr/share/bash-completion/completions/dnsspoof 
│                │                       ├ [437] : usr/share/bash-completion/completions/doas 
│                │                       ├ [438] : usr/share/bash-completion/completions/dot 
│                │                       ├ [439] : usr/share/bash-completion/completions/dpkg 
│                │                       ├ [440] : usr/share/bash-completion/completions/dpkg-deb 
│                │                       ├ [441] : usr/share/bash-completion/completions/dpkg-query 
│                │                       ├ [442] : usr/share/bash-completion/completions/dpkg-reconfigure 
│                │                       ├ [443] : usr/share/bash-completion/completions/dpkg-source 
│                │                       ├ [444] : usr/share/bash-completion/completions/dropdb 
│                │                       ├ [445] : usr/share/bash-completion/completions/dropuser 
│                │                       ├ [446] : usr/share/bash-completion/completions/dselect 
│                │                       ├ [447] : usr/share/bash-completion/completions/dsniff 
│                │                       ├ [448] : usr/share/bash-completion/completions/dumpdb 
│                │                       ├ [449] : usr/share/bash-completion/completions/dumpe2fs 
│                │                       ├ [450] : usr/share/bash-completion/completions/e2freefrag 
│                │                       ├ [451] : usr/share/bash-completion/completions/e2label 
│                │                       ├ [452] : usr/share/bash-completion/completions/ebtables 
│                │                       ├ [453] : usr/share/bash-completion/completions/ecryptfs-migrate-home 
│                │                       ├ [454] : usr/share/bash-completion/completions/edquota 
│                │                       ├ [455] : usr/share/bash-completion/completions/env 
│                │                       ├ [456] : usr/share/bash-completion/completions/eog 
│                │                       ├ [457] : usr/share/bash-completion/completions/ether-wake 
│                │                       ├ [458] : usr/share/bash-completion/completions/etherwake 
│                │                       ├ [459] : usr/share/bash-completion/completions/evince 
│                │                       ├ [460] : usr/share/bash-completion/completions/explodepkg 
│                │                       ├ [461] : usr/share/bash-completion/completions/export 
│                │                       ├ [462] : usr/share/bash-completion/completions/f77 
│                │                       ├ [463] : usr/share/bash-completion/completions/f95 
│                │                       ├ [464] : usr/share/bash-completion/completions/faillog 
│                │                       ├ [465] : usr/share/bash-completion/completions/fbgs 
│                │                       ├ [466] : usr/share/bash-completion/completions/fbi 
│                │                       ├ [467] : usr/share/bash-completion/completions/feh 
│                │                       ├ [468] : usr/share/bash-completion/completions/file 
│                │                       ├ [469] : usr/share/bash-completion/completions/file-roller 
│                │                       ├ [470] : usr/share/bash-completion/completions/filebucket 
│                │                       ├ [471] : usr/share/bash-completion/completions/filefrag 
│                │                       ├ [472] : usr/share/bash-completion/completions/filesnarf 
│                │                       ├ [473] : usr/share/bash-completion/completions/find 
│                │                       ├ [474] : usr/share/bash-completion/completions/find_member 
│                │                       ├ [475] : usr/share/bash-completion/completions/fio 
│                │                       ├ [476] : usr/share/bash-completion/completions/firefox 
│                │                       ├ [477] : usr/share/bash-completion/completions/firefox-esr 
│                │                       ├ [478] : usr/share/bash-completion/completions/flake8 
│                │                       ├ [479] : usr/share/bash-completion/completions/fprintd-delete 
│                │                       ├ [480] : usr/share/bash-completion/completions/fprintd-enroll 
│                │                       ├ [481] : usr/share/bash-completion/completions/fprintd-list 
│                │                       ├ [482] : usr/share/bash-completion/completions/fprintd-verify 
│                │                       ├ [483] : usr/share/bash-completion/completions/free 
│                │                       ├ [484] : usr/share/bash-completion/completions/freeciv 
│                │                       ├ [485] : usr/share/bash-completion/completions/freeciv-gtk2 
│                │                       ├ [486] : usr/share/bash-completion/completions/freeciv-gtk3 
│                │                       ├ [487] : usr/share/bash-completion/completions/freeciv-sdl 
│                │                       ├ [488] : usr/share/bash-completion/completions/freeciv-server 
│                │                       ├ [489] : usr/share/bash-completion/completions/freeciv-xaw 
│                │                       ├ [490] : usr/share/bash-completion/completions/fsnotifywait 
│                │                       ├ [491] : usr/share/bash-completion/completions/fsnotifywatch 
│                │                       ├ [492] : usr/share/bash-completion/completions/function 
│                │                       ├ [493] : usr/share/bash-completion/completions/fusermount 
│                │                       ├ [494] : usr/share/bash-completion/completions/g++ 
│                │                       ├ [495] : usr/share/bash-completion/completions/g++-5 
│                │                       ├ [496] : usr/share/bash-completion/completions/g++-6 
│                │                       ├ [497] : usr/share/bash-completion/completions/g++-7 
│                │                       ├ [498] : usr/share/bash-completion/completions/g++-8 
│                │                       ├ [499] : usr/share/bash-completion/completions/g4 
│                │                       ├ [500] : usr/share/bash-completion/completions/g77 
│                │                       ├ [501] : usr/share/bash-completion/completions/g95 
│                │                       ├ [502] : usr/share/bash-completion/completions/gcc 
│                │                       ├ [503] : usr/share/bash-completion/completions/gcc-5 
│                │                       ├ [504] : usr/share/bash-completion/completions/gcc-6 
│                │                       ├ [505] : usr/share/bash-completion/completions/gcc-7 
│                │                       ├ [506] : usr/share/bash-completion/completions/gcc-8 
│                │                       ├ [507] : usr/share/bash-completion/completions/gccgo 
│                │                       ├ [508] : usr/share/bash-completion/completions/gccgo-5 
│                │                       ├ [509] : usr/share/bash-completion/completions/gccgo-6 
│                │                       ├ [510] : usr/share/bash-completion/completions/gccgo-7 
│                │                       ├ [511] : usr/share/bash-completion/completions/gccgo-8 
│                │                       ├ [512] : usr/share/bash-completion/completions/gcj 
│                │                       ├ [513] : usr/share/bash-completion/completions/gcl 
│                │                       ├ [514] : usr/share/bash-completion/completions/gdb 
│                │                       ├ [515] : usr/share/bash-completion/completions/genaliases 
│                │                       ├ [516] : usr/share/bash-completion/completions/gendiff 
│                │                       ├ [517] : usr/share/bash-completion/completions/genisoimage 
│                │                       ├ [518] : usr/share/bash-completion/completions/geoiplookup 
│                │                       ├ [519] : usr/share/bash-completion/completions/geoiplookup6 
│                │                       ├ [520] : usr/share/bash-completion/completions/getconf 
│                │                       ├ [521] : usr/share/bash-completion/completions/getent 
│                │                       ├ [522] : usr/share/bash-completion/completions/gfortran 
│                │                       ├ [523] : usr/share/bash-completion/completions/gfortran-5 
│                │                       ├ [524] : usr/share/bash-completion/completions/gfortran-6 
│                │                       ├ [525] : usr/share/bash-completion/completions/gfortran-7 
│                │                       ├ [526] : usr/share/bash-completion/completions/gfortran-8 
│                │                       ├ [527] : usr/share/bash-completion/completions/gkrellm 
│                │                       ├ [528] : usr/share/bash-completion/completions/gkrellm2 
│                │                       ├ [529] : usr/share/bash-completion/completions/gm 
│                │                       ├ [530] : usr/share/bash-completion/completions/gmake 
│                │                       ├ [531] : usr/share/bash-completion/completions/gmplayer 
│                │                       ├ [532] : usr/share/bash-completion/completions/gnatmake 
│                │                       ├ [533] : usr/share/bash-completion/completions/gnokii 
│                │                       ├ [534] : usr/share/bash-completion/completions/gnome-mplayer 
│                │                       ├ [535] : usr/share/bash-completion/completions/gnome-screenshot 
│                │                       ├ [536] : usr/share/bash-completion/completions/gnumake 
│                │                       ├ [537] : usr/share/bash-completion/completions/google-chrome 
│                │                       ├ [538] : usr/share/bash-completion/completions/google-chrome-stable 
│                │                       ├ [539] : usr/share/bash-completion/completions/gpasswd 
│                │                       ├ [540] : usr/share/bash-completion/completions/gpc 
│                │                       ├ [541] : usr/share/bash-completion/completions/gpg 
│                │                       ├ [542] : usr/share/bash-completion/completions/gpg2 
│                │                       ├ [543] : usr/share/bash-completion/completions/gpgv 
│                │                       ├ [544] : usr/share/bash-completion/completions/gpgv2 
│                │                       ├ [545] : usr/share/bash-completion/completions/gphoto2 
│                │                       ├ [546] : usr/share/bash-completion/completions/gprof 
│                │                       ├ [547] : usr/share/bash-completion/completions/groupadd 
│                │                       ├ [548] : usr/share/bash-completion/completions/groupdel 
│                │                       ├ [549] : usr/share/bash-completion/completions/groupmems 
│                │                       ├ [550] : usr/share/bash-completion/completions/groupmod 
│                │                       ├ [551] : usr/share/bash-completion/completions/growisofs 
│                │                       ├ [552] : usr/share/bash-completion/completions/grpck 
│                │                       ├ [553] : usr/share/bash-completion/completions/gssdp-device-sniffer 
│                │                       ├ [554] : usr/share/bash-completion/completions/gssdp-discover 
│                │                       ├ [555] : usr/share/bash-completion/completions/gtar 
│                │                       ├ [556] : usr/share/bash-completion/completions/gzip 
│                │                       ├ [557] : usr/share/bash-completion/completions/hash 
│                │                       ├ [558] : usr/share/bash-completion/completions/hciattach 
│                │                       ├ [559] : usr/share/bash-completion/completions/hciconfig 
│                │                       ├ [560] : usr/share/bash-completion/completions/hcitool 
│                │                       ├ [561] : usr/share/bash-completion/completions/hddtemp 
│                │                       ├ [562] : usr/share/bash-completion/completions/help 
│                │                       ├ [563] : usr/share/bash-completion/completions/hid2hci 
│                │                       ├ [564] : usr/share/bash-completion/completions/host 
│                │                       ├ [565] : usr/share/bash-completion/completions/hostname 
│                │                       ├ [566] : usr/share/bash-completion/completions/hping 
│                │                       ├ [567] : usr/share/bash-completion/completions/hping2 
│                │                       ├ [568] : usr/share/bash-completion/completions/hping3 
│                │                       ├ [569] : usr/share/bash-completion/completions/htop 
│                │                       ├ [570] : usr/share/bash-completion/completions/htpasswd 
│                │                       ├ [571] : usr/share/bash-completion/completions/hunspell 
│                │                       ├ [572] : usr/share/bash-completion/completions/iceweasel 
│                │                       ├ [573] : usr/share/bash-completion/completions/iconv 
│                │                       ├ [574] : usr/share/bash-completion/completions/id 
│                │                       ├ [575] : usr/share/bash-completion/completions/identify 
│                │                       ├ [576] : usr/share/bash-completion/completions/idn 
│                │                       ├ [577] : usr/share/bash-completion/completions/ifdown 
│                │                       ├ [578] : usr/share/bash-completion/completions/ifquery 
│                │                       ├ [579] : usr/share/bash-completion/completions/ifstat 
│                │                       ├ [580] : usr/share/bash-completion/completions/ifstatus 
│                │                       ├ [581] : usr/share/bash-completion/completions/iftop 
│                │                       ├ [582] : usr/share/bash-completion/completions/ifup 
│                │                       ├ [583] : usr/share/bash-completion/completions/import 
│                │                       ├ [584] : usr/share/bash-completion/completions/influx 
│                │                       ├ [585] : usr/share/bash-completion/completions/info 
│                │                       ├ [586] : usr/share/bash-completion/completions/inject 
│                │                       ├ [587] : usr/share/bash-completion/completions/inotifywait 
│                │                       ├ [588] : usr/share/bash-completion/completions/inotifywatch 
│                │                       ├ [589] : usr/share/bash-completion/completions/installpkg 
│                │                       ├ [590] : usr/share/bash-completion/completions/interdiff 
│                │                       ├ [591] : usr/share/bash-completion/completions/invoke-rc.d 
│                │                       ├ [592] : usr/share/bash-completion/completions/ip 
│                │                       ├ [593] : usr/share/bash-completion/completions/ipcalc 
│                │                       ├ [594] : usr/share/bash-completion/completions/iperf 
│                │                       ├ [595] : usr/share/bash-completion/completions/iperf3 
│                │                       ├ [596] : usr/share/bash-completion/completions/ipmitool 
│                │                       ├ [597] : usr/share/bash-completion/completions/ipsec 
│                │                       ├ [598] : usr/share/bash-completion/completions/iptables 
│                │                       ├ [599] : usr/share/bash-completion/completions/ipv6calc 
│                │                       ├ [600] : usr/share/bash-completion/completions/iscsiadm 
│                │                       ├ [601] : usr/share/bash-completion/completions/isort 
│                │                       ├ [602] : usr/share/bash-completion/completions/isql 
│                │                       ├ [603] : usr/share/bash-completion/completions/iwconfig 
│                │                       ├ [604] : usr/share/bash-completion/completions/iwlist 
│                │                       ├ [605] : usr/share/bash-completion/completions/iwpriv 
│                │                       ├ [606] : usr/share/bash-completion/completions/iwspy 
│                │                       ├ [607] : usr/share/bash-completion/completions/jar 
│                │                       ├ [608] : usr/share/bash-completion/completions/jarsigner 
│                │                       ├ [609] : usr/share/bash-completion/completions/java 
│                │                       ├ [610] : usr/share/bash-completion/completions/javac 
│                │                       ├ [611] : usr/share/bash-completion/completions/javadoc 
│                │                       ├ [612] : usr/share/bash-completion/completions/javaws 
│                │                       ├ [613] : usr/share/bash-completion/completions/jpegoptim 
│                │                       ├ [614] : usr/share/bash-completion/completions/jps 
│                │                       ├ [615] : usr/share/bash-completion/completions/jq 
│                │                       ├ [616] : usr/share/bash-completion/completions/jshint 
│                │                       ├ [617] : usr/share/bash-completion/completions/json_xs 
│                │                       ├ [618] : usr/share/bash-completion/completions/jsonschema 
│                │                       ├ [619] : usr/share/bash-completion/completions/k3b 
│                │                       ├ [620] : usr/share/bash-completion/completions/kcov 
│                │                       ├ [621] : usr/share/bash-completion/completions/kill 
│                │                       ├ [622] : usr/share/bash-completion/completions/killall 
│                │                       ├ [623] : usr/share/bash-completion/completions/koji 
│                │                       ├ [624] : usr/share/bash-completion/completions/kplayer 
│                │                       ├ [625] : usr/share/bash-completion/completions/ktutil 
│                │                       ├ [626] : usr/share/bash-completion/completions/l2ping 
│                │                       ├ [627] : usr/share/bash-completion/completions/larch 
│                │                       ├ [628] : usr/share/bash-completion/completions/lastlog 
│                │                       ├ [629] : usr/share/bash-completion/completions/lbzip2 
│                │                       ├ [630] : usr/share/bash-completion/completions/ldapadd 
│                │                       ├ [631] : usr/share/bash-completion/completions/ldapcompare 
│                │                       ├ [632] : usr/share/bash-completion/completions/ldapdelete 
│                │                       ├ [633] : usr/share/bash-completion/completions/ldapmodify 
│                │                       ├ [634] : usr/share/bash-completion/completions/ldapmodrdn 
│                │                       ├ [635] : usr/share/bash-completion/completions/ldappasswd 
│                │                       ├ [636] : usr/share/bash-completion/completions/ldapsearch 
│                │                       ├ [637] : usr/share/bash-completion/completions/ldapvi 
│                │                       ├ [638] : usr/share/bash-completion/completions/ldapwhoami 
│                │                       ├ [639] : usr/share/bash-completion/completions/lftp 
│                │                       ├ [640] : usr/share/bash-completion/completions/lftpget 
│                │                       ├ [641] : usr/share/bash-completion/completions/lilo 
│                │                       ├ [642] : usr/share/bash-completion/completions/links 
│                │                       ├ [643] : usr/share/bash-completion/completions/links2 
│                │                       ├ [644] : usr/share/bash-completion/completions/lintian 
│                │                       ├ [645] : usr/share/bash-completion/completions/lintian-info 
│                │                       ├ [646] : usr/share/bash-completion/completions/lisp 
│                │                       ├ [647] : usr/share/bash-completion/completions/list_admins 
│                │                       ├ [648] : usr/share/bash-completion/completions/list_lists 
│                │                       ├ [649] : usr/share/bash-completion/completions/list_members 
│                │                       ├ [650] : usr/share/bash-completion/completions/list_owners 
│                │                       ├ [651] : usr/share/bash-completion/completions/locale-gen 
│                │                       ├ [652] : usr/share/bash-completion/completions/lpq 
│                │                       ├ [653] : usr/share/bash-completion/completions/lpr 
│                │                       ├ [654] : usr/share/bash-completion/completions/lrzip 
│                │                       ├ [655] : usr/share/bash-completion/completions/lsof 
│                │                       ├ [656] : usr/share/bash-completion/completions/lsscsi 
│                │                       ├ [657] : usr/share/bash-completion/completions/lsusb 
│                │                       ├ [658] : usr/share/bash-completion/completions/lua 
│                │                       ├ [659] : usr/share/bash-completion/completions/lua5.0 
│                │                       ├ [660] : usr/share/bash-completion/completions/lua5.1 
│                │                       ├ [661] : usr/share/bash-completion/completions/lua5.2 
│                │                       ├ [662] : usr/share/bash-completion/completions/lua5.3 
│                │                       ├ [663] : usr/share/bash-completion/completions/lua5.4 
│                │                       ├ [664] : usr/share/bash-completion/completions/lua50 
│                │                       ├ [665] : usr/share/bash-completion/completions/lua51 
│                │                       ├ [666] : usr/share/bash-completion/completions/lua52 
│                │                       ├ [667] : usr/share/bash-completion/completions/lua53 
│                │                       ├ [668] : usr/share/bash-completion/completions/lua54 
│                │                       ├ [669] : usr/share/bash-completion/completions/luac 
│                │                       ├ [670] : usr/share/bash-completion/completions/luac5.0 
│                │                       ├ [671] : usr/share/bash-completion/completions/luac5.1 
│                │                       ├ [672] : usr/share/bash-completion/completions/luac5.2 
│                │                       ├ [673] : usr/share/bash-completion/completions/luac5.3 
│                │                       ├ [674] : usr/share/bash-completion/completions/luac5.4 
│                │                       ├ [675] : usr/share/bash-completion/completions/luac50 
│                │                       ├ [676] : usr/share/bash-completion/completions/luac51 
│                │                       ├ [677] : usr/share/bash-completion/completions/luac52 
│                │                       ├ [678] : usr/share/bash-completion/completions/luac53 
│                │                       ├ [679] : usr/share/bash-completion/completions/luac54 
│                │                       ├ [680] : usr/share/bash-completion/completions/luseradd 
│                │                       ├ [681] : usr/share/bash-completion/completions/luserdel 
│                │                       ├ [682] : usr/share/bash-completion/completions/lusermod 
│                │                       ├ [683] : usr/share/bash-completion/completions/lvchange 
│                │                       ├ [684] : usr/share/bash-completion/completions/lvcreate 
│                │                       ├ [685] : usr/share/bash-completion/completions/lvdisplay 
│                │                       ├ [686] : usr/share/bash-completion/completions/lvextend 
│                │                       ├ [687] : usr/share/bash-completion/completions/lvm 
│                │                       ├ [688] : usr/share/bash-completion/completions/lvmdiskscan 
│                │                       ├ [689] : usr/share/bash-completion/completions/lvreduce 
│                │                       ├ [690] : usr/share/bash-completion/completions/lvremove 
│                │                       ├ [691] : usr/share/bash-completion/completions/lvrename 
│                │                       ├ [692] : usr/share/bash-completion/completions/lvresize 
│                │                       ├ [693] : usr/share/bash-completion/completions/lvs 
│                │                       ├ [694] : usr/share/bash-completion/completions/lvscan 
│                │                       ├ [695] : usr/share/bash-completion/completions/lz4 
│                │                       ├ [696] : usr/share/bash-completion/completions/lz4c 
│                │                       ├ [697] : usr/share/bash-completion/completions/lzip 
│                │                       ├ [698] : usr/share/bash-completion/completions/lzma 
│                │                       ├ [699] : usr/share/bash-completion/completions/lzop 
│                │                       ├ [700] : usr/share/bash-completion/completions/macof 
│                │                       ├ [701] : usr/share/bash-completion/completions/mailmanctl 
│                │                       ├ [702] : usr/share/bash-completion/completions/mailsnarf 
│                │                       ├ [703] : usr/share/bash-completion/completions/make 
│                │                       ├ [704] : usr/share/bash-completion/completions/man 
│                │                       ├ [705] : usr/share/bash-completion/completions/mc 
│                │                       ├ [706] : usr/share/bash-completion/completions/mcrypt 
│                │                       ├ [707] : usr/share/bash-completion/completions/md5sum 
│                │                       ├ [708] : usr/share/bash-completion/completions/mdadm 
│                │                       ├ [709] : usr/share/bash-completion/completions/mdecrypt 
│                │                       ├ [710] : usr/share/bash-completion/completions/mdtool 
│                │                       ├ [711] : usr/share/bash-completion/completions/medusa 
│                │                       ├ [712] : usr/share/bash-completion/completions/mencoder 
│                │                       ├ [713] : usr/share/bash-completion/completions/mfiutil 
│                │                       ├ [714] : usr/share/bash-completion/completions/micropython 
│                │                       ├ [715] : usr/share/bash-completion/completions/mii-diag 
│                │                       ├ [716] : usr/share/bash-completion/completions/mii-tool 
│                │                       ├ [717] : usr/share/bash-completion/completions/minicom 
│                │                       ├ [718] : usr/share/bash-completion/completions/mkinitrd 
│                │                       ├ [719] : usr/share/bash-completion/completions/mkisofs 
│                │                       ├ [720] : usr/share/bash-completion/completions/mktemp 
│                │                       ├ [721] : usr/share/bash-completion/completions/mmsitepass 
│                │                       ├ [722] : usr/share/bash-completion/completions/mogrify 
│                │                       ├ [723] : usr/share/bash-completion/completions/monodevelop 
│                │                       ├ [724] : usr/share/bash-completion/completions/montage 
│                │                       ├ [725] : usr/share/bash-completion/completions/mozilla-firefox 
│                │                       ├ [726] : usr/share/bash-completion/completions/mplayer 
│                │                       ├ [727] : usr/share/bash-completion/completions/mplayer2 
│                │                       ├ [728] : usr/share/bash-completion/completions/mr 
│                │                       ├ [729] : usr/share/bash-completion/completions/mrsasutil 
│                │                       ├ [730] : usr/share/bash-completion/completions/msgsnarf 
│                │                       ├ [731] : usr/share/bash-completion/completions/msynctool 
│                │                       ├ [732] : usr/share/bash-completion/completions/mtx 
│                │                       ├ [733] : usr/share/bash-completion/completions/munin-node-configure 
│                │                       ├ [734] : usr/share/bash-completion/completions/munin-run 
│                │                       ├ [735] : usr/share/bash-completion/completions/munin-update 
│                │                       ├ [736] : usr/share/bash-completion/completions/munindoc 
│                │                       ├ [737] : usr/share/bash-completion/completions/mussh 
│                │                       ├ [738] : usr/share/bash-completion/completions/mutt 
│                │                       ├ [739] : usr/share/bash-completion/completions/muttng 
│                │                       ├ [740] : usr/share/bash-completion/completions/mypy 
│                │                       ├ [741] : usr/share/bash-completion/completions/mysql 
│                │                       ├ [742] : usr/share/bash-completion/completions/mysqladmin 
│                │                       ├ [743] : usr/share/bash-completion/completions/nc 
│                │                       ├ [744] : usr/share/bash-completion/completions/ncftp 
│                │                       ├ [745] : usr/share/bash-completion/completions/neomutt 
│                │                       ├ [746] : usr/share/bash-completion/completions/nethogs 
│                │                       ├ [747] : usr/share/bash-completion/completions/newlist 
│                │                       ├ [748] : usr/share/bash-completion/completions/newusers 
│                │                       ├ [749] : usr/share/bash-completion/completions/ngrep 
│                │                       ├ [750] : usr/share/bash-completion/completions/nload 
│                │                       ├ [751] : usr/share/bash-completion/completions/nmap 
│                │                       ├ [752] : usr/share/bash-completion/completions/nproc 
│                │                       ├ [753] : usr/share/bash-completion/completions/nslookup 
│                │                       ├ [754] : usr/share/bash-completion/completions/nsupdate 
│                │                       ├ [755] : usr/share/bash-completion/completions/ntpdate 
│                │                       ├ [756] : usr/share/bash-completion/completions/oggdec 
│                │                       ├ [757] : usr/share/bash-completion/completions/openssl 
│                │                       ├ [758] : usr/share/bash-completion/completions/opera 
│                │                       ├ [759] : usr/share/bash-completion/completions/optipng 
│                │                       ├ [760] : usr/share/bash-completion/completions/p4 
│                │                       ├ [761] : usr/share/bash-completion/completions/pack200 
│                │                       ├ [762] : usr/share/bash-completion/completions/passwd 
│                │                       ├ [763] : usr/share/bash-completion/completions/patch 
│                │                       ├ [764] : usr/share/bash-completion/completions/pbzip2 
│                │                       ├ [765] : usr/share/bash-completion/completions/pccardctl 
│                │                       ├ [766] : usr/share/bash-completion/completions/pdftoppm 
│                │                       ├ [767] : usr/share/bash-completion/completions/pdftotext 
│                │                       ├ [768] : usr/share/bash-completion/completions/pdlzip 
│                │                       ├ [769] : usr/share/bash-completion/completions/perl 
│                │                       ├ [770] : usr/share/bash-completion/completions/perlcritic 
│                │                       ├ [771] : usr/share/bash-completion/completions/perldoc 
│                │                       ├ [772] : usr/share/bash-completion/completions/perltidy 
│                │                       ├ [773] : usr/share/bash-completion/completions/pgrep 
│                │                       ├ [774] : usr/share/bash-completion/completions/phing 
│                │                       ├ [775] : usr/share/bash-completion/completions/pidof 
│                │                       ├ [776] : usr/share/bash-completion/completions/pigz 
│                │                       ├ [777] : usr/share/bash-completion/completions/pine 
│                │                       ├ [778] : usr/share/bash-completion/completions/pinfo 
│                │                       ├ [779] : usr/share/bash-completion/completions/ping 
│                │                       ├ [780] : usr/share/bash-completion/completions/ping4 
│                │                       ├ [781] : usr/share/bash-completion/completions/ping6 
│                │                       ├ [782] : usr/share/bash-completion/completions/pkg-config 
│                │                       ├ [783] : usr/share/bash-completion/completions/pkg-get 
│                │                       ├ [784] : usr/share/bash-completion/completions/pkgadd 
│                │                       ├ [785] : usr/share/bash-completion/completions/pkgconf 
│                │                       ├ [786] : usr/share/bash-completion/completions/pkgrm 
│                │                       ├ [787] : usr/share/bash-completion/completions/pkgtool 
│                │                       ├ [788] : usr/share/bash-completion/completions/pkill 
│                │                       ├ [789] : usr/share/bash-completion/completions/plague-client 
│                │                       ├ [790] : usr/share/bash-completion/completions/plzip 
│                │                       ├ [791] : usr/share/bash-completion/completions/pm-hibernate 
│                │                       ├ [792] : usr/share/bash-completion/completions/pm-is-supported 
│                │                       ├ [793] : usr/share/bash-completion/completions/pm-powersave 
│                │                       ├ [794] : usr/share/bash-completion/completions/pm-suspend 
│                │                       ├ [795] : usr/share/bash-completion/completions/pm-suspend-hybrid 
│                │                       ├ [796] : usr/share/bash-completion/completions/pmake 
│                │                       ├ [797] : usr/share/bash-completion/completions/pngfix 
│                │                       ├ [798] : usr/share/bash-completion/completions/postalias 
│                │                       ├ [799] : usr/share/bash-completion/completions/postcat 
│                │                       ├ [800] : usr/share/bash-completion/completions/postconf 
│                │                       ├ [801] : usr/share/bash-completion/completions/postfix 
│                │                       ├ [802] : usr/share/bash-completion/completions/postmap 
│                │                       ├ [803] : usr/share/bash-completion/completions/postsuper 
│                │                       ├ [804] : usr/share/bash-completion/completions/povray 
│                │                       ├ [805] : usr/share/bash-completion/completions/ppc-koji 
│                │                       ├ [806] : usr/share/bash-completion/completions/prelink 
│                │                       ├ [807] : usr/share/bash-completion/completions/printenv 
│                │                       ├ [808] : usr/share/bash-completion/completions/protoc 
│                │                       ├ [809] : usr/share/bash-completion/completions/ps 
│                │                       ├ [810] : usr/share/bash-completion/completions/psql 
│                │                       ├ [811] : usr/share/bash-completion/completions/puppet 
│                │                       ├ [812] : usr/share/bash-completion/completions/puppetca 
│                │                       ├ [813] : usr/share/bash-completion/completions/puppetd 
│                │                       ├ [814] : usr/share/bash-completion/completions/puppetdoc 
│                │                       ├ [815] : usr/share/bash-completion/completions/puppetmasterd 
│                │                       ├ [816] : usr/share/bash-completion/completions/puppetqd 
│                │                       ├ [817] : usr/share/bash-completion/completions/puppetrun 
│                │                       ├ [818] : usr/share/bash-completion/completions/pushd 
│                │                       ├ [819] : usr/share/bash-completion/completions/pv 
│                │                       ├ [820] : usr/share/bash-completion/completions/pvchange 
│                │                       ├ [821] : usr/share/bash-completion/completions/pvcreate 
│                │                       ├ [822] : usr/share/bash-completion/completions/pvdisplay 
│                │                       ├ [823] : usr/share/bash-completion/completions/pvmove 
│                │                       ├ [824] : usr/share/bash-completion/completions/pvremove 
│                │                       ├ [825] : usr/share/bash-completion/completions/pvs 
│                │                       ├ [826] : usr/share/bash-completion/completions/pvscan 
│                │                       ├ [827] : usr/share/bash-completion/completions/pwck 
│                │                       ├ [828] : usr/share/bash-completion/completions/pwd 
│                │                       ├ [829] : usr/share/bash-completion/completions/pwdx 
│                │                       ├ [830] : usr/share/bash-completion/completions/pwgen 
│                │                       ├ [831] : usr/share/bash-completion/completions/pxz 
│                │                       ├ [832] : usr/share/bash-completion/completions/py.test 
│                │                       ├ [833] : usr/share/bash-completion/completions/py.test-2 
│                │                       ├ [834] : usr/share/bash-completion/completions/py.test-3 
│                │                       ├ [835] : usr/share/bash-completion/completions/pycodestyle 
│                │                       ├ [836] : usr/share/bash-completion/completions/pydoc 
│                │                       ├ [837] : usr/share/bash-completion/completions/pydoc3 
│                │                       ├ [838] : usr/share/bash-completion/completions/pydocstyle 
│                │                       ├ [839] : usr/share/bash-completion/completions/pyflakes 
│                │                       ├ [840] : usr/share/bash-completion/completions/pylint 
│                │                       ├ [841] : usr/share/bash-completion/completions/pylint-2 
│                │                       ├ [842] : usr/share/bash-completion/completions/pylint-3 
│                │                       ├ [843] : usr/share/bash-completion/completions/pypy 
│                │                       ├ [844] : usr/share/bash-completion/completions/pypy3 
│                │                       ├ [845] : usr/share/bash-completion/completions/pyston 
│                │                       ├ [846] : usr/share/bash-completion/completions/pyston3 
│                │                       ├ [847] : usr/share/bash-completion/completions/pytest 
│                │                       ├ [848] : usr/share/bash-completion/completions/pytest-2 
│                │                       ├ [849] : usr/share/bash-completion/completions/pytest-3 
│                │                       ├ [850] : usr/share/bash-completion/completions/python 
│                │                       ├ [851] : usr/share/bash-completion/completions/python2 
│                │                       ├ [852] : usr/share/bash-completion/completions/python2.7 
│                │                       ├ [853] : usr/share/bash-completion/completions/python3 
│                │                       ├ [854] : usr/share/bash-completion/completions/python3.10 
│                │                       ├ [855] : usr/share/bash-completion/completions/python3.11 
│                │                       ├ [856] : usr/share/bash-completion/completions/python3.12 
│                │                       ├ [857] : usr/share/bash-completion/completions/python3.13 
│                │                       ├ [858] : usr/share/bash-completion/completions/python3.3 
│                │                       ├ [859] : usr/share/bash-completion/completions/python3.4 
│                │                       ├ [860] : usr/share/bash-completion/completions/python3.5 
│                │                       ├ [861] : usr/share/bash-completion/completions/python3.6 
│                │                       ├ [862] : usr/share/bash-completion/completions/python3.7 
│                │                       ├ [863] : usr/share/bash-completion/completions/python3.8 
│                │                       ├ [864] : usr/share/bash-completion/completions/python3.9 
│                │                       ├ [865] : usr/share/bash-completion/completions/pyvenv 
│                │                       ├ [866] : usr/share/bash-completion/completions/pyvenv-3.10 
│                │                       ├ [867] : usr/share/bash-completion/completions/pyvenv-3.11 
│                │                       ├ [868] : usr/share/bash-completion/completions/pyvenv-3.12 
│                │                       ├ [869] : usr/share/bash-completion/completions/pyvenv-3.13 
│                │                       ├ [870] : usr/share/bash-completion/completions/pyvenv-3.4 
│                │                       ├ [871] : usr/share/bash-completion/completions/pyvenv-3.5 
│                │                       ├ [872] : usr/share/bash-completion/completions/pyvenv-3.6 
│                │                       ├ [873] : usr/share/bash-completion/completions/pyvenv-3.7 
│                │                       ├ [874] : usr/share/bash-completion/completions/pyvenv-3.8 
│                │                       ├ [875] : usr/share/bash-completion/completions/pyvenv-3.9 
│                │                       ├ [876] : usr/share/bash-completion/completions/qdbus 
│                │                       ├ [877] : usr/share/bash-completion/completions/qemu 
│                │                       ├ [878] : usr/share/bash-completion/completions/qemu-kvm 
│                │                       ├ [879] : usr/share/bash-completion/completions/qemu-system-i386 
│                │                       ├ [880] : usr/share/bash-completion/completions/qemu-system-x86_64 
│                │                       ├ [881] : usr/share/bash-completion/completions/qrunner 
│                │                       ├ [882] : usr/share/bash-completion/completions/querybts 
│                │                       ├ [883] : usr/share/bash-completion/completions/quota 
│                │                       ├ [884] : usr/share/bash-completion/completions/quotacheck 
│                │                       ├ [885] : usr/share/bash-completion/completions/quotaoff 
│                │                       ├ [886] : usr/share/bash-completion/completions/quotaon 
│                │                       ├ [887] : usr/share/bash-completion/completions/radvdump 
│                │                       ├ [888] : usr/share/bash-completion/completions/ralsh 
│                │                       ├ [889] : usr/share/bash-completion/completions/rcs 
│                │                       ├ [890] : usr/share/bash-completion/completions/rcsdiff 
│                │                       ├ [891] : usr/share/bash-completion/completions/rdesktop 
│                │                       ├ [892] : usr/share/bash-completion/completions/rdict 
│                │                       ├ [893] : usr/share/bash-completion/completions/remove_members 
│                │                       ├ [894] : usr/share/bash-completion/completions/removepkg 
│                │                       ├ [895] : usr/share/bash-completion/completions/reportbug 
│                │                       ├ [896] : usr/share/bash-completion/completions/repquota 
│                │                       ├ [897] : usr/share/bash-completion/completions/resolvconf 
│                │                       ├ [898] : usr/share/bash-completion/completions/rfcomm 
│                │                       ├ [899] : usr/share/bash-completion/completions/ri 
│                │                       ├ [900] : usr/share/bash-completion/completions/rlog 
│                │                       ├ [901] : usr/share/bash-completion/completions/rmlist 
│                │                       ├ [902] : usr/share/bash-completion/completions/route 
│                │                       ├ [903] : usr/share/bash-completion/completions/rpcdebug 
│                │                       ├ [904] : usr/share/bash-completion/completions/rpm 
│                │                       ├ [905] : usr/share/bash-completion/completions/rpm2targz 
│                │                       ├ [906] : usr/share/bash-completion/completions/rpm2tgz 
│                │                       ├ [907] : usr/share/bash-completion/completions/rpm2txz 
│                │                       ├ [908] : usr/share/bash-completion/completions/rpmbuild 
│                │                       ├ [909] : usr/share/bash-completion/completions/rpmbuild-md5 
│                │                       ├ [910] : usr/share/bash-completion/completions/rpmcheck 
│                │                       ├ [911] : usr/share/bash-completion/completions/rrdtool 
│                │                       ├ [912] : usr/share/bash-completion/completions/rsync 
│                │                       ├ [913] : usr/share/bash-completion/completions/s390-koji 
│                │                       ├ [914] : usr/share/bash-completion/completions/sbcl 
│                │                       ├ [915] : usr/share/bash-completion/completions/sbcl-mt 
│                │                       ├ [916] : usr/share/bash-completion/completions/sbopkg 
│                │                       ├ [917] : usr/share/bash-completion/completions/scp 
│                │                       ├ [918] : usr/share/bash-completion/completions/screen 
│                │                       ├ [919] : usr/share/bash-completion/completions/scrub 
│                │                       ├ [920] : usr/share/bash-completion/completions/sdptool 
│                │                       ├ [921] : usr/share/bash-completion/completions/set 
│                │                       ├ [922] : usr/share/bash-completion/completions/setquota 
│                │                       ├ [923] : usr/share/bash-completion/completions/sftp 
│                │                       ├ [924] : usr/share/bash-completion/completions/sh 
│                │                       ├ [925] : usr/share/bash-completion/completions/sha1sum 
│                │                       ├ [926] : usr/share/bash-completion/completions/sha224sum 
│                │                       ├ [927] : usr/share/bash-completion/completions/sha256sum 
│                │                       ├ [928] : usr/share/bash-completion/completions/sha384sum 
│                │                       ├ [929] : usr/share/bash-completion/completions/sha512sum 
│                │                       ├ [930] : usr/share/bash-completion/completions/shasum 
│                │                       ├ [931] : usr/share/bash-completion/completions/shellcheck 
│                │                       ├ [932] : usr/share/bash-completion/completions/sidedoor 
│                │                       ├ [933] : usr/share/bash-completion/completions/sitecopy 
│                │                       ├ [934] : usr/share/bash-completion/completions/slabtop 
│                │                       ├ [935] : usr/share/bash-completion/completions/slapt-get 
│                │                       ├ [936] : usr/share/bash-completion/completions/slapt-src 
│                │                       ├ [937] : usr/share/bash-completion/completions/slogin 
│                │                       ├ [938] : usr/share/bash-completion/completions/smartctl 
│                │                       ├ [939] : usr/share/bash-completion/completions/smbcacls 
│                │                       ├ [940] : usr/share/bash-completion/completions/smbclient 
│                │                       ├ [941] : usr/share/bash-completion/completions/smbcquotas 
│                │                       ├ [942] : usr/share/bash-completion/completions/smbget 
│                │                       ├ [943] : usr/share/bash-completion/completions/smbpasswd 
│                │                       ├ [944] : usr/share/bash-completion/completions/smbtar 
│                │                       ├ [945] : usr/share/bash-completion/completions/smbtree 
│                │                       ├ [946] : usr/share/bash-completion/completions/snownews 
│                │                       ├ [947] : usr/share/bash-completion/completions/sparc-koji 
│                │                       ├ [948] : usr/share/bash-completion/completions/spovray 
│                │                       ├ [949] : usr/share/bash-completion/completions/sqlite3 
│                │                       ├ [950] : usr/share/bash-completion/completions/ss 
│                │                       ├ [951] : usr/share/bash-completion/completions/ssh 
│                │                       ├ [952] : usr/share/bash-completion/completions/ssh-add 
│                │                       ├ [953] : usr/share/bash-completion/completions/ssh-copy-id 
│                │                       ├ [954] : usr/share/bash-completion/completions/ssh-keygen 
│                │                       ├ [955] : usr/share/bash-completion/completions/ssh-keyscan 
│                │                       ├ [956] : usr/share/bash-completion/completions/sshfs 
│                │                       ├ [957] : usr/share/bash-completion/completions/sshmitm 
│                │                       ├ [958] : usr/share/bash-completion/completions/sshow 
│                │                       ├ [959] : usr/share/bash-completion/completions/star 
│                │                       ├ [960] : usr/share/bash-completion/completions/strace 
│                │                       ├ [961] : usr/share/bash-completion/completions/stream 
│                │                       ├ [962] : usr/share/bash-completion/completions/strings 
│                │                       ├ [963] : usr/share/bash-completion/completions/sudo 
│                │                       ├ [964] : usr/share/bash-completion/completions/sudoedit 
│                │                       ├ [965] : usr/share/bash-completion/completions/svcadm 
│                │                       ├ [966] : usr/share/bash-completion/completions/svk 
│                │                       ├ [967] : usr/share/bash-completion/completions/sync_members 
│                │                       ├ [968] : usr/share/bash-completion/completions/synclient 
│                │                       ├ [969] : usr/share/bash-completion/completions/sysbench 
│                │                       ├ [970] : usr/share/bash-completion/completions/sysctl 
│                │                       ├ [971] : usr/share/bash-completion/completions/tar 
│                │                       ├ [972] : usr/share/bash-completion/completions/tcpdump 
│                │                       ├ [973] : usr/share/bash-completion/completions/tcpkill 
│                │                       ├ [974] : usr/share/bash-completion/completions/tcpnice 
│                │                       ├ [975] : usr/share/bash-completion/completions/tightvncviewer 
│                │                       ├ [976] : usr/share/bash-completion/completions/timeout 
│                │                       ├ [977] : usr/share/bash-completion/completions/tipc 
│                │                       ├ [978] : usr/share/bash-completion/completions/tmux 
│                │                       ├ [979] : usr/share/bash-completion/completions/tox 
│                │                       ├ [980] : usr/share/bash-completion/completions/tracepath 
│                │                       ├ [981] : usr/share/bash-completion/completions/tracepath6 
│                │                       ├ [982] : usr/share/bash-completion/completions/tree 
│                │                       ├ [983] : usr/share/bash-completion/completions/truncate 
│                │                       ├ [984] : usr/share/bash-completion/completions/tshark 
│                │                       ├ [985] : usr/share/bash-completion/completions/tsig-keygen 
│                │                       ├ [986] : usr/share/bash-completion/completions/tune2fs 
│                │                       ├ [987] : usr/share/bash-completion/completions/typeset 
│                │                       ├ [988] : usr/share/bash-completion/completions/ulimit 
│                │                       ├ [989] : usr/share/bash-completion/completions/unace 
│                │                       ├ [990] : usr/share/bash-completion/completions/unpack200 
│                │                       ├ [991] : usr/share/bash-completion/completions/unrar 
│                │                       ├ [992] : usr/share/bash-completion/completions/unshunt 
│                │                       ├ [993] : usr/share/bash-completion/completions/update-alternatives 
│                │                       ├ [994] : usr/share/bash-completion/completions/update-rc.d 
│                │                       ├ [995] : usr/share/bash-completion/completions/upgradepkg 
│                │                       ├ [996] : usr/share/bash-completion/completions/urlsnarf 
│                │                       ├ [997] : usr/share/bash-completion/completions/useradd 
│                │                       ├ [998] : usr/share/bash-completion/completions/userdel 
│                │                       ├ [999] : usr/share/bash-completion/completions/usermod 
│                │                       ├ [1000]: usr/share/bash-completion/completions/valgrind 
│                │                       ├ [1001]: usr/share/bash-completion/completions/vgcfgbackup 
│                │                       ├ [1002]: usr/share/bash-completion/completions/vgcfgrestore 
│                │                       ├ [1003]: usr/share/bash-completion/completions/vgchange 
│                │                       ├ [1004]: usr/share/bash-completion/completions/vgck 
│                │                       ├ [1005]: usr/share/bash-completion/completions/vgconvert 
│                │                       ├ [1006]: usr/share/bash-completion/completions/vgcreate 
│                │                       ├ [1007]: usr/share/bash-completion/completions/vgdisplay 
│                │                       ├ [1008]: usr/share/bash-completion/completions/vgexport 
│                │                       ├ [1009]: usr/share/bash-completion/completions/vgextend 
│                │                       ├ [1010]: usr/share/bash-completion/completions/vgimport 
│                │                       ├ [1011]: usr/share/bash-completion/completions/vgmerge 
│                │                       ├ [1012]: usr/share/bash-completion/completions/vgmknodes 
│                │                       ├ [1013]: usr/share/bash-completion/completions/vgreduce 
│                │                       ├ [1014]: usr/share/bash-completion/completions/vgremove 
│                │                       ├ [1015]: usr/share/bash-completion/completions/vgrename 
│                │                       ├ [1016]: usr/share/bash-completion/completions/vgs 
│                │                       ├ [1017]: usr/share/bash-completion/completions/vgscan 
│                │                       ├ [1018]: usr/share/bash-completion/completions/vgsplit 
│                │                       ├ [1019]: usr/share/bash-completion/completions/vigr 
│                │                       ├ [1020]: usr/share/bash-completion/completions/vipw 
│                │                       ├ [1021]: usr/share/bash-completion/completions/vmstat 
│                │                       ├ [1022]: usr/share/bash-completion/completions/vncviewer 
│                │                       ├ [1023]: usr/share/bash-completion/completions/vpnc 
│                │                       ├ [1024]: usr/share/bash-completion/completions/watch 
│                │                       ├ [1025]: usr/share/bash-completion/completions/webmitm 
│                │                       ├ [1026]: usr/share/bash-completion/completions/wget 
│                │                       ├ [1027]: usr/share/bash-completion/completions/whatis 
│                │                       ├ [1028]: usr/share/bash-completion/completions/wine 
│                │                       ├ [1029]: usr/share/bash-completion/completions/wine-development 
│                │                       ├ [1030]: usr/share/bash-completion/completions/wine-stable 
│                │                       ├ [1031]: usr/share/bash-completion/completions/wine64 
│                │                       ├ [1032]: usr/share/bash-completion/completions/wine64-development 
│                │                       ├ [1033]: usr/share/bash-completion/completions/wine64-stable 
│                │                       ├ [1034]: usr/share/bash-completion/completions/withlist 
│                │                       ├ [1035]: usr/share/bash-completion/completions/wodim 
│                │                       ├ [1036]: usr/share/bash-completion/completions/wol 
│                │                       ├ [1037]: usr/share/bash-completion/completions/wsimport 
│                │                       ├ [1038]: usr/share/bash-completion/completions/wtf 
│                │                       ├ [1039]: usr/share/bash-completion/completions/wvdial 
│                │                       ├ [1040]: usr/share/bash-completion/completions/xdg-mime 
│                │                       ├ [1041]: usr/share/bash-completion/completions/xdg-settings 
│                │                       ├ [1042]: usr/share/bash-completion/completions/xev 
│                │                       ├ [1043]: usr/share/bash-completion/completions/xfreerdp 
│                │                       ├ [1044]: usr/share/bash-completion/completions/xgamma 
│                │                       ├ [1045]: usr/share/bash-completion/completions/xhost 
│                │                       ├ [1046]: usr/share/bash-completion/completions/xmllint 
│                │                       ├ [1047]: usr/share/bash-completion/completions/xmlwf 
│                │                       ├ [1048]: usr/share/bash-completion/completions/xmms 
│                │                       ├ [1049]: usr/share/bash-completion/completions/xmodmap 
│                │                       ├ [1050]: usr/share/bash-completion/completions/xpovray 
│                │                       ├ [1051]: usr/share/bash-completion/completions/xrandr 
│                │                       ├ [1052]: usr/share/bash-completion/completions/xrdb 
│                │                       ├ [1053]: usr/share/bash-completion/completions/xsltproc 
│                │                       ├ [1054]: usr/share/bash-completion/completions/xvfb-run 
│                │                       ├ [1055]: usr/share/bash-completion/completions/xvnc4viewer 
│                │                       ├ [1056]: usr/share/bash-completion/completions/xxd 
│                │                       ├ [1057]: usr/share/bash-completion/completions/xz 
│                │                       ├ [1058]: usr/share/bash-completion/completions/xzdec 
│                │                       ├ [1059]: usr/share/bash-completion/completions/ypcat 
│                │                       ├ [1060]: usr/share/bash-completion/completions/ypmatch 
│                │                       ├ [1061]: usr/share/bash-completion/completions/yum-arch 
│                │                       ├ [1062]: usr/share/bash-completion/completions/zopfli 
│                │                       ├ [1063]: usr/share/bash-completion/completions/zopflipng 
│                │                       ├ [1064]: usr/share/bash-completion/helpers/make-extract-targets.awk 
│                │                       ├ [1065]: usr/share/bash-completion/helpers/perl 
│                │                       ╰ [1066]: usr/share/bash-completion/helpers/python 
│                ├ [9]  ╭ ID            : brotli-libs@1.2.0-r0 
│                │      ├ Name          : brotli-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/brotli-libs@1.2.0-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : b299b9e27780dd4f 
│                │      ├ Version       : 1.2.0-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : brotli 
│                │      ├ SrcVersion    : 1.2.0-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : prspkt <prspkt@protonmail.com> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:0814694602f35d2741e916fdcb4c9a1e0ec50b42 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libbrotlicommon.so.1 
│                │                       ├ [1]: usr/lib/libbrotlicommon.so.1.2.0 
│                │                       ├ [2]: usr/lib/libbrotlidec.so.1 
│                │                       ├ [3]: usr/lib/libbrotlidec.so.1.2.0 
│                │                       ├ [4]: usr/lib/libbrotlienc.so.1 
│                │                       ╰ [5]: usr/lib/libbrotlienc.so.1.2.0 
│                ├ [10] ╭ ID            : busybox@1.37.0-r29 
│                │      ├ Name          : busybox 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/busybox@1.37.0-r29?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 9dc34ceb8949e72c 
│                │      ├ Version       : 1.37.0-r29 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : busybox 
│                │      ├ SrcVersion    : 1.37.0-r29 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Sören Tempel <soeren+alpine@soeren-tempel.net> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4bb9078dc355d2cd18ac470cde0f4bc0b3a27a96 
│                │      ╰ InstalledFiles ╭ [0]: bin/busybox 
│                │                       ├ [1]: etc/securetty 
│                │                       ├ [2]: etc/busybox-paths.d/busybox 
│                │                       ├ [3]: etc/logrotate.d/acpid 
│                │                       ├ [4]: etc/network/if-up.d/dad 
│                │                       ├ [5]: etc/udhcpc/udhcpc.conf 
│                │                       ╰ [6]: usr/share/udhcpc/default.script 
│                ├ [11] ╭ ID            : busybox-binsh@1.37.0-r29 
│                │      ├ Name          : busybox-binsh 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/busybox-binsh@1.37.0-r29?arch=x86_64&distro=3.2
│                │      │                │       3.0 
│                │      │                ╰ UID : 2add9820dd1f5e50 
│                │      ├ Version       : 1.37.0-r29 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : busybox 
│                │      ├ SrcVersion    : 1.37.0-r29 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Sören Tempel <soeren+alpine@soeren-tempel.net> 
│                │      ├ DependsOn      ─ [0]: busybox@1.37.0-r29 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:0430c7a2208bee624182f50cb4dee02943103230 
│                │      ╰ InstalledFiles ─ [0]: bin/sh 
│                ├ [12] ╭ ID            : c-ares@1.34.5-r0 
│                │      ├ Name          : c-ares 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/c-ares@1.34.5-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : d42a24c1ed8d1a3b 
│                │      ├ Version       : 1.34.5-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : c-ares 
│                │      ├ SrcVersion    : 1.34.5-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Carlo Landmeter <clandmeter@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:8a338faabd9dfb0e542f744412befafbe097626b 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libcares.so.2 
│                │                       ╰ [1]: usr/lib/libcares.so.2.19.4 
│                ├ [13] ╭ ID            : ca-certificates@20251003-r0 
│                │      ├ Name          : ca-certificates 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/ca-certificates@20251003-r0?arch=x86_64&distro=
│                │      │                │       3.23.0 
│                │      │                ╰ UID : dd004463b296da59 
│                │      ├ Version       : 20251003-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : ca-certificates 
│                │      ├ SrcVersion    : 20251003-r0 
│                │      ├ Licenses       ╭ [0]: MPL-2.0 
│                │      │                ╰ [1]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: busybox-binsh@1.37.0-r29 
│                │      │                ├ [1]: libcrypto3@3.5.4-r0 
│                │      │                ╰ [2]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:3b10fd335b2af819c4fd3562900e76fd6ea304c5 
│                │      ╰ InstalledFiles ╭ [0]  : etc/ca-certificates.conf 
│                │                       ├ [1]  : etc/apk/protected_paths.d/ca-certificates.list 
│                │                       ├ [2]  : etc/ca-certificates/update.d/certhash 
│                │                       ├ [3]  : usr/bin/c_rehash 
│                │                       ├ [4]  : usr/sbin/update-ca-certificates 
│                │                       ├ [5]  : usr/share/ca-certificates/mozilla/ACCVRAIZ1.crt 
│                │                       ├ [6]  : usr/share/ca-certificates/mozilla/AC_RAIZ_FNMT-RCM.crt 
│                │                       ├ [7]  : usr/share/ca-certificates/mozilla/AC_RAIZ_FNMT-RCM_SERVIDORES
│                │                       │        _SEGUROS.crt 
│                │                       ├ [8]  : usr/share/ca-certificates/mozilla/ANF_Secure_Server_Root_CA.crt 
│                │                       ├ [9]  : usr/share/ca-certificates/mozilla/Actalis_Authentication_Root
│                │                       │        _CA.crt 
│                │                       ├ [10] : usr/share/ca-certificates/mozilla/AffirmTrust_Commercial.crt 
│                │                       ├ [11] : usr/share/ca-certificates/mozilla/AffirmTrust_Networking.crt 
│                │                       ├ [12] : usr/share/ca-certificates/mozilla/AffirmTrust_Premium.crt 
│                │                       ├ [13] : usr/share/ca-certificates/mozilla/AffirmTrust_Premium_ECC.crt 
│                │                       ├ [14] : usr/share/ca-certificates/mozilla/Amazon_Root_CA_1.crt 
│                │                       ├ [15] : usr/share/ca-certificates/mozilla/Amazon_Root_CA_2.crt 
│                │                       ├ [16] : usr/share/ca-certificates/mozilla/Amazon_Root_CA_3.crt 
│                │                       ├ [17] : usr/share/ca-certificates/mozilla/Amazon_Root_CA_4.crt 
│                │                       ├ [18] : usr/share/ca-certificates/mozilla/Atos_TrustedRoot_2011.crt 
│                │                       ├ [19] : usr/share/ca-certificates/mozilla/Atos_TrustedRoot_Root_CA_EC
│                │                       │        C_TLS_2021.crt 
│                │                       ├ [20] : usr/share/ca-certificates/mozilla/Atos_TrustedRoot_Root_CA_RS
│                │                       │        A_TLS_2021.crt 
│                │                       ├ [21] : usr/share/ca-certificates/mozilla/Autoridad_de_Certificacion_
│                │                       │        Firmaprofesional_CIF_A62634068.crt 
│                │                       ├ [22] : usr/share/ca-certificates/mozilla/BJCA_Global_Root_CA1.crt 
│                │                       ├ [23] : usr/share/ca-certificates/mozilla/BJCA_Global_Root_CA2.crt 
│                │                       ├ [24] : usr/share/ca-certificates/mozilla/Buypass_Class_2_Root_CA.crt 
│                │                       ├ [25] : usr/share/ca-certificates/mozilla/Buypass_Class_3_Root_CA.crt 
│                │                       ├ [26] : usr/share/ca-certificates/mozilla/CA_Disig_Root_R2.crt 
│                │                       ├ [27] : usr/share/ca-certificates/mozilla/CFCA_EV_ROOT.crt 
│                │                       ├ [28] : usr/share/ca-certificates/mozilla/COMODO_Certification_Author
│                │                       │        ity.crt 
│                │                       ├ [29] : usr/share/ca-certificates/mozilla/COMODO_ECC_Certification_Au
│                │                       │        thority.crt 
│                │                       ├ [30] : usr/share/ca-certificates/mozilla/COMODO_RSA_Certification_Au
│                │                       │        thority.crt 
│                │                       ├ [31] : usr/share/ca-certificates/mozilla/Certainly_Root_E1.crt 
│                │                       ├ [32] : usr/share/ca-certificates/mozilla/Certainly_Root_R1.crt 
│                │                       ├ [33] : usr/share/ca-certificates/mozilla/Certigna.crt 
│                │                       ├ [34] : usr/share/ca-certificates/mozilla/Certigna_Root_CA.crt 
│                │                       ├ [35] : usr/share/ca-certificates/mozilla/Certum_EC-384_CA.crt 
│                │                       ├ [36] : usr/share/ca-certificates/mozilla/Certum_Trusted_Network_CA.crt 
│                │                       ├ [37] : usr/share/ca-certificates/mozilla/Certum_Trusted_Network_CA_2
│                │                       │        .crt 
│                │                       ├ [38] : usr/share/ca-certificates/mozilla/Certum_Trusted_Root_CA.crt 
│                │                       ├ [39] : usr/share/ca-certificates/mozilla/CommScope_Public_Trust_ECC_
│                │                       │        Root-01.crt 
│                │                       ├ [40] : usr/share/ca-certificates/mozilla/CommScope_Public_Trust_ECC_
│                │                       │        Root-02.crt 
│                │                       ├ [41] : usr/share/ca-certificates/mozilla/CommScope_Public_Trust_RSA_
│                │                       │        Root-01.crt 
│                │                       ├ [42] : usr/share/ca-certificates/mozilla/CommScope_Public_Trust_RSA_
│                │                       │        Root-02.crt 
│                │                       ├ [43] : usr/share/ca-certificates/mozilla/D-TRUST_BR_Root_CA_1_2020.crt 
│                │                       ├ [44] : usr/share/ca-certificates/mozilla/D-TRUST_BR_Root_CA_2_2023.crt 
│                │                       ├ [45] : usr/share/ca-certificates/mozilla/D-TRUST_EV_Root_CA_1_2020.crt 
│                │                       ├ [46] : usr/share/ca-certificates/mozilla/D-TRUST_EV_Root_CA_2_2023.crt 
│                │                       ├ [47] : usr/share/ca-certificates/mozilla/D-TRUST_Root_Class_3_CA_2_2
│                │                       │        009.crt 
│                │                       ├ [48] : usr/share/ca-certificates/mozilla/D-TRUST_Root_Class_3_CA_2_E
│                │                       │        V_2009.crt 
│                │                       ├ [49] : usr/share/ca-certificates/mozilla/DigiCert_Assured_ID_Root_CA
│                │                       │        .crt 
│                │                       ├ [50] : usr/share/ca-certificates/mozilla/DigiCert_Assured_ID_Root_G2
│                │                       │        .crt 
│                │                       ├ [51] : usr/share/ca-certificates/mozilla/DigiCert_Assured_ID_Root_G3
│                │                       │        .crt 
│                │                       ├ [52] : usr/share/ca-certificates/mozilla/DigiCert_Global_Root_CA.crt 
│                │                       ├ [53] : usr/share/ca-certificates/mozilla/DigiCert_Global_Root_G2.crt 
│                │                       ├ [54] : usr/share/ca-certificates/mozilla/DigiCert_Global_Root_G3.crt 
│                │                       ├ [55] : usr/share/ca-certificates/mozilla/DigiCert_High_Assurance_EV_
│                │                       │        Root_CA.crt 
│                │                       ├ [56] : usr/share/ca-certificates/mozilla/DigiCert_TLS_ECC_P384_Root_
│                │                       │        G5.crt 
│                │                       ├ [57] : usr/share/ca-certificates/mozilla/DigiCert_TLS_RSA4096_Root_G
│                │                       │        5.crt 
│                │                       ├ [58] : usr/share/ca-certificates/mozilla/DigiCert_Trusted_Root_G4.crt 
│                │                       ├ [59] : usr/share/ca-certificates/mozilla/Entrust_Root_Certification_
│                │                       │        Authority.crt 
│                │                       ├ [60] : usr/share/ca-certificates/mozilla/Entrust_Root_Certification_
│                │                       │        Authority_-_EC1.crt 
│                │                       ├ [61] : usr/share/ca-certificates/mozilla/Entrust_Root_Certification_
│                │                       │        Authority_-_G2.crt 
│                │                       ├ [62] : usr/share/ca-certificates/mozilla/FIRMAPROFESIONAL_CA_ROOT-A_
│                │                       │        WEB.crt 
│                │                       ├ [63] : usr/share/ca-certificates/mozilla/GDCA_TrustAUTH_R5_ROOT.crt 
│                │                       ├ [64] : usr/share/ca-certificates/mozilla/GLOBALTRUST_2020.crt 
│                │                       ├ [65] : usr/share/ca-certificates/mozilla/GTS_Root_R1.crt 
│                │                       ├ [66] : usr/share/ca-certificates/mozilla/GTS_Root_R2.crt 
│                │                       ├ [67] : usr/share/ca-certificates/mozilla/GTS_Root_R3.crt 
│                │                       ├ [68] : usr/share/ca-certificates/mozilla/GTS_Root_R4.crt 
│                │                       ├ [69] : usr/share/ca-certificates/mozilla/GlobalSign_ECC_Root_CA_-_R4
│                │                       │        .crt 
│                │                       ├ [70] : usr/share/ca-certificates/mozilla/GlobalSign_ECC_Root_CA_-_R5
│                │                       │        .crt 
│                │                       ├ [71] : usr/share/ca-certificates/mozilla/GlobalSign_Root_CA_-_R3.crt 
│                │                       ├ [72] : usr/share/ca-certificates/mozilla/GlobalSign_Root_CA_-_R6.crt 
│                │                       ├ [73] : usr/share/ca-certificates/mozilla/GlobalSign_Root_E46.crt 
│                │                       ├ [74] : usr/share/ca-certificates/mozilla/GlobalSign_Root_R46.crt 
│                │                       ├ [75] : usr/share/ca-certificates/mozilla/Go_Daddy_Root_Certificate_A
│                │                       │        uthority_-_G2.crt 
│                │                       ├ [76] : usr/share/ca-certificates/mozilla/HARICA_TLS_ECC_Root_CA_2021
│                │                       │        .crt 
│                │                       ├ [77] : usr/share/ca-certificates/mozilla/HARICA_TLS_RSA_Root_CA_2021
│                │                       │        .crt 
│                │                       ├ [78] : usr/share/ca-certificates/mozilla/Hellenic_Academic_and_Resea
│                │                       │        rch_Institutions_ECC_RootCA_2015.crt 
│                │                       ├ [79] : usr/share/ca-certificates/mozilla/Hellenic_Academic_and_Resea
│                │                       │        rch_Institutions_RootCA_2015.crt 
│                │                       ├ [80] : usr/share/ca-certificates/mozilla/HiPKI_Root_CA_-_G1.crt 
│                │                       ├ [81] : usr/share/ca-certificates/mozilla/Hongkong_Post_Root_CA_3.crt 
│                │                       ├ [82] : usr/share/ca-certificates/mozilla/ISRG_Root_X1.crt 
│                │                       ├ [83] : usr/share/ca-certificates/mozilla/ISRG_Root_X2.crt 
│                │                       ├ [84] : usr/share/ca-certificates/mozilla/IdenTrust_Commercial_Root_C
│                │                       │        A_1.crt 
│                │                       ├ [85] : usr/share/ca-certificates/mozilla/IdenTrust_Public_Sector_Roo
│                │                       │        t_CA_1.crt 
│                │                       ├ [86] : usr/share/ca-certificates/mozilla/Izenpe.com.crt 
│                │                       ├ [87] : usr/share/ca-certificates/mozilla/Microsec_e-Szigno_Root_CA_2
│                │                       │        009.crt 
│                │                       ├ [88] : usr/share/ca-certificates/mozilla/Microsoft_ECC_Root_Certific
│                │                       │        ate_Authority_2017.crt 
│                │                       ├ [89] : usr/share/ca-certificates/mozilla/Microsoft_RSA_Root_Certific
│                │                       │        ate_Authority_2017.crt 
│                │                       ├ [90] : usr/share/ca-certificates/mozilla/NAVER_Global_Root_Certifica
│                │                       │        tion_Authority.crt 
│                │                       ├ [91] : usr/share/ca-certificates/mozilla/NetLock_Arany_=Class_Gold=_
│                │                       │        Főtanúsítvány.crt 
│                │                       ├ [92] : usr/share/ca-certificates/mozilla/OISTE_Server_Root_ECC_G1.crt 
│                │                       ├ [93] : usr/share/ca-certificates/mozilla/OISTE_Server_Root_RSA_G1.crt 
│                │                       ├ [94] : usr/share/ca-certificates/mozilla/OISTE_WISeKey_Global_Root_G
│                │                       │        B_CA.crt 
│                │                       ├ [95] : usr/share/ca-certificates/mozilla/OISTE_WISeKey_Global_Root_G
│                │                       │        C_CA.crt 
│                │                       ├ [96] : usr/share/ca-certificates/mozilla/QuoVadis_Root_CA_1_G3.crt 
│                │                       ├ [97] : usr/share/ca-certificates/mozilla/QuoVadis_Root_CA_2.crt 
│                │                       ├ [98] : usr/share/ca-certificates/mozilla/QuoVadis_Root_CA_2_G3.crt 
│                │                       ├ [99] : usr/share/ca-certificates/mozilla/QuoVadis_Root_CA_3.crt 
│                │                       ├ [100]: usr/share/ca-certificates/mozilla/QuoVadis_Root_CA_3_G3.crt 
│                │                       ├ [101]: usr/share/ca-certificates/mozilla/SSL.com_EV_Root_Certificati
│                │                       │        on_Authority_ECC.crt 
│                │                       ├ [102]: usr/share/ca-certificates/mozilla/SSL.com_EV_Root_Certificati
│                │                       │        on_Authority_RSA_R2.crt 
│                │                       ├ [103]: usr/share/ca-certificates/mozilla/SSL.com_Root_Certification_
│                │                       │        Authority_ECC.crt 
│                │                       ├ [104]: usr/share/ca-certificates/mozilla/SSL.com_Root_Certification_
│                │                       │        Authority_RSA.crt 
│                │                       ├ [105]: usr/share/ca-certificates/mozilla/SSL.com_TLS_ECC_Root_CA_202
│                │                       │        2.crt 
│                │                       ├ [106]: usr/share/ca-certificates/mozilla/SSL.com_TLS_RSA_Root_CA_202
│                │                       │        2.crt 
│                │                       ├ [107]: usr/share/ca-certificates/mozilla/SZAFIR_ROOT_CA2.crt 
│                │                       ├ [108]: usr/share/ca-certificates/mozilla/Sectigo_Public_Server_Authe
│                │                       │        ntication_Root_E46.crt 
│                │                       ├ [109]: usr/share/ca-certificates/mozilla/Sectigo_Public_Server_Authe
│                │                       │        ntication_Root_R46.crt 
│                │                       ├ [110]: usr/share/ca-certificates/mozilla/SecureSign_Root_CA12.crt 
│                │                       ├ [111]: usr/share/ca-certificates/mozilla/SecureSign_Root_CA14.crt 
│                │                       ├ [112]: usr/share/ca-certificates/mozilla/SecureSign_Root_CA15.crt 
│                │                       ├ [113]: usr/share/ca-certificates/mozilla/SecureTrust_CA.crt 
│                │                       ├ [114]: usr/share/ca-certificates/mozilla/Secure_Global_CA.crt 
│                │                       ├ [115]: usr/share/ca-certificates/mozilla/Security_Communication_ECC_
│                │                       │        RootCA1.crt 
│                │                       ├ [116]: usr/share/ca-certificates/mozilla/Security_Communication_Root
│                │                       │        CA2.crt 
│                │                       ├ [117]: usr/share/ca-certificates/mozilla/Starfield_Root_Certificate_
│                │                       │        Authority_-_G2.crt 
│                │                       ├ [118]: usr/share/ca-certificates/mozilla/Starfield_Services_Root_Cer
│                │                       │        tificate_Authority_-_G2.crt 
│                │                       ├ [119]: usr/share/ca-certificates/mozilla/SwissSign_Gold_CA_-_G2.crt 
│                │                       ├ [120]: usr/share/ca-certificates/mozilla/SwissSign_RSA_TLS_Root_CA_2
│                │                       │        022_-_1.crt 
│                │                       ├ [121]: usr/share/ca-certificates/mozilla/T-TeleSec_GlobalRoot_Class_
│                │                       │        2.crt 
│                │                       ├ [122]: usr/share/ca-certificates/mozilla/T-TeleSec_GlobalRoot_Class_
│                │                       │        3.crt 
│                │                       ├ [123]: usr/share/ca-certificates/mozilla/TUBITAK_Kamu_SM_SSL_Kok_Ser
│                │                       │        tifikasi_-_Surum_1.crt 
│                │                       ├ [124]: usr/share/ca-certificates/mozilla/TWCA_CYBER_Root_CA.crt 
│                │                       ├ [125]: usr/share/ca-certificates/mozilla/TWCA_Global_Root_CA.crt 
│                │                       ├ [126]: usr/share/ca-certificates/mozilla/TWCA_Root_Certification_Aut
│                │                       │        hority.crt 
│                │                       ├ [127]: usr/share/ca-certificates/mozilla/Telekom_Security_TLS_ECC_Ro
│                │                       │        ot_2020.crt 
│                │                       ├ [128]: usr/share/ca-certificates/mozilla/Telekom_Security_TLS_RSA_Ro
│                │                       │        ot_2023.crt 
│                │                       ├ [129]: usr/share/ca-certificates/mozilla/TeliaSonera_Root_CA_v1.crt 
│                │                       ├ [130]: usr/share/ca-certificates/mozilla/Telia_Root_CA_v2.crt 
│                │                       ├ [131]: usr/share/ca-certificates/mozilla/TrustAsia_Global_Root_CA_G3
│                │                       │        .crt 
│                │                       ├ [132]: usr/share/ca-certificates/mozilla/TrustAsia_Global_Root_CA_G4
│                │                       │        .crt 
│                │                       ├ [133]: usr/share/ca-certificates/mozilla/TrustAsia_TLS_ECC_Root_CA.crt 
│                │                       ├ [134]: usr/share/ca-certificates/mozilla/TrustAsia_TLS_RSA_Root_CA.crt 
│                │                       ├ [135]: usr/share/ca-certificates/mozilla/Trustwave_Global_Certificat
│                │                       │        ion_Authority.crt 
│                │                       ├ [136]: usr/share/ca-certificates/mozilla/Trustwave_Global_ECC_P256_C
│                │                       │        ertification_Authority.crt 
│                │                       ├ [137]: usr/share/ca-certificates/mozilla/Trustwave_Global_ECC_P384_C
│                │                       │        ertification_Authority.crt 
│                │                       ├ [138]: usr/share/ca-certificates/mozilla/TunTrust_Root_CA.crt 
│                │                       ├ [139]: usr/share/ca-certificates/mozilla/UCA_Extended_Validation_Roo
│                │                       │        t.crt 
│                │                       ├ [140]: usr/share/ca-certificates/mozilla/UCA_Global_G2_Root.crt 
│                │                       ├ [141]: usr/share/ca-certificates/mozilla/USERTrust_ECC_Certification
│                │                       │        _Authority.crt 
│                │                       ├ [142]: usr/share/ca-certificates/mozilla/USERTrust_RSA_Certification
│                │                       │        _Authority.crt 
│                │                       ├ [143]: usr/share/ca-certificates/mozilla/certSIGN_ROOT_CA.crt 
│                │                       ├ [144]: usr/share/ca-certificates/mozilla/certSIGN_Root_CA_G2.crt 
│                │                       ├ [145]: usr/share/ca-certificates/mozilla/e-Szigno_Root_CA_2017.crt 
│                │                       ├ [146]: usr/share/ca-certificates/mozilla/ePKI_Root_Certification_Aut
│                │                       │        hority.crt 
│                │                       ├ [147]: usr/share/ca-certificates/mozilla/emSign_ECC_Root_CA_-_C3.crt 
│                │                       ├ [148]: usr/share/ca-certificates/mozilla/emSign_ECC_Root_CA_-_G3.crt 
│                │                       ├ [149]: usr/share/ca-certificates/mozilla/emSign_Root_CA_-_C1.crt 
│                │                       ├ [150]: usr/share/ca-certificates/mozilla/emSign_Root_CA_-_G1.crt 
│                │                       ├ [151]: usr/share/ca-certificates/mozilla/vTrus_ECC_Root_CA.crt 
│                │                       ╰ [152]: usr/share/ca-certificates/mozilla/vTrus_Root_CA.crt 
│                ├ [14] ╭ ID            : ca-certificates-bundle@20251003-r0 
│                │      ├ Name          : ca-certificates-bundle 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/ca-certificates-bundle@20251003-r0?arch=x86_64&
│                │      │                │       distro=3.23.0 
│                │      │                ╰ UID : 601aed1e41b824a1 
│                │      ├ Version       : 20251003-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : ca-certificates 
│                │      ├ SrcVersion    : 20251003-r0 
│                │      ├ Licenses       ╭ [0]: MPL-2.0 
│                │      │                ╰ [1]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:63ebe72ba79f548b6cdc8a9894e16a90d80f42b0 
│                │      ╰ InstalledFiles ╭ [0]: etc/ssl/cert.pem 
│                │                       ├ [1]: etc/ssl/certs/ca-certificates.crt 
│                │                       ├ [2]: etc/ssl1.1/cert.pem 
│                │                       ╰ [3]: etc/ssl1.1/certs 
│                ├ [15] ╭ ID            : curl@8.17.0-r1 
│                │      ├ Name          : curl 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/curl@8.17.0-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 88ffdbbc87036140 
│                │      ├ Version       : 8.17.0-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : curl 
│                │      ├ SrcVersion    : 8.17.0-r1 
│                │      ├ Licenses       ─ [0]: curl 
│                │      ├ Maintainer    : Achill Gilgenast <achill@achill.org> 
│                │      ├ DependsOn      ╭ [0]: libcurl@8.17.0-r1 
│                │      │                ├ [1]: musl@1.2.5-r21 
│                │      │                ╰ [2]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:c467d4938a8ffc55afe3b1a6223787e0ecd60036 
│                │      ╰ InstalledFiles ╭ [0]: usr/bin/curl 
│                │                       ╰ [1]: usr/bin/wcurl 
│                ├ [16] ╭ ID            : e2fsprogs-libs@1.47.3-r0 
│                │      ├ Name          : e2fsprogs-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/e2fsprogs-libs@1.47.3-r0?arch=x86_64&distro=3.2
│                │      │                │       3.0 
│                │      │                ╰ UID : 6f119f437ef3fe4f 
│                │      ├ Version       : 1.47.3-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : e2fsprogs 
│                │      ├ SrcVersion    : 1.47.3-r0 
│                │      ├ Licenses       ╭ [0]: GPL-2.0-or-later 
│                │      │                ├ [1]: LGPL-2.0-or-later 
│                │      │                ├ [2]: BSD-3-Clause 
│                │      │                ╰ [3]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libcom_err@1.47.3-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:a6f2f8d1af4ae9aa344c38b0a4829743af49719f 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libe2p.so.2 
│                │                       ├ [1]: usr/lib/libe2p.so.2.3 
│                │                       ├ [2]: usr/lib/libext2fs.so.2 
│                │                       ├ [3]: usr/lib/libext2fs.so.2.4 
│                │                       ├ [4]: usr/lib/libss.so.2 
│                │                       ╰ [5]: usr/lib/libss.so.2.0 
│                ├ [17] ╭ ID            : glib@2.86.2-r1 
│                │      ├ Name          : glib 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/glib@2.86.2-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 7bb934b8fbb18761 
│                │      ├ Version       : 2.86.2-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : glib 
│                │      ├ SrcVersion    : 2.86.2-r1 
│                │      ├ Licenses       ─ [0]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : team/gnome <pabloyoyoista@postmarketos.org> 
│                │      ├ DependsOn      ╭ [0]: busybox-binsh@1.37.0-r29 
│                │      │                ├ [1]: libffi@3.5.2-r0 
│                │      │                ├ [2]: libintl@0.24.1-r1 
│                │      │                ├ [3]: libmount@2.41.2-r0 
│                │      │                ├ [4]: musl@1.2.5-r21 
│                │      │                ├ [5]: pcre2@10.47-r0 
│                │      │                ╰ [6]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:b83c13bab07fb5975705675357024c3092e711da 
│                │      ╰ InstalledFiles ╭ [0] : usr/bin/gapplication 
│                │                       ├ [1] : usr/bin/gdbus 
│                │                       ├ [2] : usr/bin/gi-compile-repository 
│                │                       ├ [3] : usr/bin/gi-decompile-typelib 
│                │                       ├ [4] : usr/bin/gi-inspect-typelib 
│                │                       ├ [5] : usr/bin/gio 
│                │                       ├ [6] : usr/bin/gio-querymodules 
│                │                       ├ [7] : usr/bin/glib-compile-schemas 
│                │                       ├ [8] : usr/bin/gsettings 
│                │                       ├ [9] : usr/lib/libgio-2.0.so.0 
│                │                       ├ [10]: usr/lib/libgio-2.0.so.0.8600.2 
│                │                       ├ [11]: usr/lib/libgirepository-2.0.so.0 
│                │                       ├ [12]: usr/lib/libgirepository-2.0.so.0.8600.2 
│                │                       ├ [13]: usr/lib/libglib-2.0.so.0 
│                │                       ├ [14]: usr/lib/libglib-2.0.so.0.8600.2 
│                │                       ├ [15]: usr/lib/libgmodule-2.0.so.0 
│                │                       ├ [16]: usr/lib/libgmodule-2.0.so.0.8600.2 
│                │                       ├ [17]: usr/lib/libgobject-2.0.so.0 
│                │                       ├ [18]: usr/lib/libgobject-2.0.so.0.8600.2 
│                │                       ├ [19]: usr/lib/libgthread-2.0.so.0 
│                │                       ├ [20]: usr/lib/libgthread-2.0.so.0.8600.2 
│                │                       ├ [21]: usr/lib/girepository-1.0/GIRepository-3.0.typelib 
│                │                       ├ [22]: usr/lib/girepository-1.0/GLib-2.0.typelib 
│                │                       ├ [23]: usr/lib/girepository-1.0/GLibUnix-2.0.typelib 
│                │                       ├ [24]: usr/lib/girepository-1.0/GModule-2.0.typelib 
│                │                       ├ [25]: usr/lib/girepository-1.0/GObject-2.0.typelib 
│                │                       ├ [26]: usr/lib/girepository-1.0/Gio-2.0.typelib 
│                │                       ├ [27]: usr/lib/girepository-1.0/GioUnix-2.0.typelib 
│                │                       ╰ [28]: usr/libexec/gio-launch-desktop 
│                ├ [18] ╭ ID            : glib-bash-completion@2.86.2-r1 
│                │      ├ Name          : glib-bash-completion 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/glib-bash-completion@2.86.2-r1?arch=x86_64&dist
│                │      │                │       ro=3.23.0 
│                │      │                ╰ UID : 645194dca5620d07 
│                │      ├ Version       : 2.86.2-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : glib 
│                │      ├ SrcVersion    : 2.86.2-r1 
│                │      ├ Licenses       ─ [0]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : team/gnome <pabloyoyoista@postmarketos.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:082ac02ad2d97e26dc2a950f704a9b79d7a8e92e 
│                │      ╰ InstalledFiles ╭ [0]: usr/share/bash-completion/completions/gapplication 
│                │                       ├ [1]: usr/share/bash-completion/completions/gdbus 
│                │                       ├ [2]: usr/share/bash-completion/completions/gio 
│                │                       ├ [3]: usr/share/bash-completion/completions/gresource 
│                │                       ╰ [4]: usr/share/bash-completion/completions/gsettings 
│                ├ [19] ╭ ID            : gpm-libs@1.20.7-r6 
│                │      ├ Name          : gpm-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/gpm-libs@1.20.7-r6?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : f4664fc7eac981f5 
│                │      ├ Version       : 1.20.7-r6 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : gpm 
│                │      ├ SrcVersion    : 1.20.7-r6 
│                │      ├ Licenses       ─ [0]: GPL-2.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libncursesw@6.5_p20251123-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:665674d7650e217aa46c621976193a641f1fcfe2 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libgpm.so.2 
│                │                       ╰ [1]: usr/lib/libgpm.so.2.1.0 
│                ├ [20] ╭ ID            : gzip@1.14-r2 
│                │      ├ Name          : gzip 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/gzip@1.14-r2?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 50ed785e9b1450fc 
│                │      ├ Version       : 1.14-r2 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : gzip 
│                │      ├ SrcVersion    : 1.14-r2 
│                │      ├ Licenses       ─ [0]: GPL-3.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: less@685-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:7565a31df3cb312f77b3cfacddd46647e76bd9c6 
│                │      ╰ InstalledFiles ╭ [0] : bin/gunzip 
│                │                       ├ [1] : bin/gzip 
│                │                       ├ [2] : bin/zcat 
│                │                       ├ [3] : usr/bin/gzexe 
│                │                       ├ [4] : usr/bin/uncompress 
│                │                       ├ [5] : usr/bin/zcmp 
│                │                       ├ [6] : usr/bin/zdiff 
│                │                       ├ [7] : usr/bin/zegrep 
│                │                       ├ [8] : usr/bin/zfgrep 
│                │                       ├ [9] : usr/bin/zforce 
│                │                       ├ [10]: usr/bin/zgrep 
│                │                       ├ [11]: usr/bin/zless 
│                │                       ├ [12]: usr/bin/zmore 
│                │                       ╰ [13]: usr/bin/znew 
│                ├ [21] ╭ ID            : less@685-r0 
│                │      ├ Name          : less 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/less@685-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 121ca08bee5e40b8 
│                │      ├ Version       : 685-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : less 
│                │      ├ SrcVersion    : 685-r0 
│                │      ├ Licenses       ╭ [0]: GPL-3.0-or-later 
│                │      │                ╰ [1]: BSD-2-Clause 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: libncursesw@6.5_p20251123-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4ac19fdd4fb4f290eecbedf6d67e34f10a084505 
│                │      ╰ InstalledFiles ╭ [0]: usr/bin/less 
│                │                       ├ [1]: usr/bin/lessecho 
│                │                       ╰ [2]: usr/bin/lesskey 
│                ├ [22] ╭ ID            : libapk@3.0.1-r1 
│                │      ├ Name          : libapk 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libapk@3.0.1-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : ea7fc98bdd4681a4 
│                │      ├ Version       : 3.0.1-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : apk-tools 
│                │      ├ SrcVersion    : 3.0.1-r1 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libcrypto3@3.5.4-r0 
│                │      │                ├ [1]: libssl3@3.5.4-r0 
│                │      │                ├ [2]: musl@1.2.5-r21 
│                │      │                ╰ [3]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:cf978e17820ec8522e4751d26473513b86312996 
│                │      ╰ InstalledFiles ─ [0]: usr/lib/libapk.so.3.0.0 
│                ├ [23] ╭ ID            : libblkid@2.41.2-r0 
│                │      ├ Name          : libblkid 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libblkid@2.41.2-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 81e45e1af6545c9d 
│                │      ├ Version       : 2.41.2-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : util-linux 
│                │      ├ SrcVersion    : 2.41.2-r0 
│                │      ├ Licenses       ─ [0]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libeconf@0.8.0-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:9996f8adb0a3f5a36c199ca5c8f682d3cae0603d 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libblkid.so.1 
│                │                       ╰ [1]: usr/lib/libblkid.so.1.1.0 
│                ├ [24] ╭ ID            : libcom_err@1.47.3-r0 
│                │      ├ Name          : libcom_err 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libcom_err@1.47.3-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : c141c324f3029ad9 
│                │      ├ Version       : 1.47.3-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : e2fsprogs 
│                │      ├ SrcVersion    : 1.47.3-r0 
│                │      ├ Licenses       ╭ [0]: GPL-2.0-or-later 
│                │      │                ├ [1]: LGPL-2.0-or-later 
│                │      │                ├ [2]: BSD-3-Clause 
│                │      │                ╰ [3]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:6661c874b35451cbd0687ea5d147d10ae65d1207 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libcom_err.so.2 
│                │                       ╰ [1]: usr/lib/libcom_err.so.2.1 
│                ├ [25] ╭ ID            : libcrypto3@3.5.4-r0 
│                │      ├ Name          : libcrypto3 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libcrypto3@3.5.4-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 408e92b2477d153d 
│                │      ├ Version       : 3.5.4-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : openssl 
│                │      ├ SrcVersion    : 3.5.4-r0 
│                │      ├ Licenses       ─ [0]: Apache-2.0 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:9d9982f901abe45b113c1efbd3cf5f6027100c5b 
│                │      ╰ InstalledFiles ╭ [0]: etc/ssl/ct_log_list.cnf 
│                │                       ├ [1]: etc/ssl/ct_log_list.cnf.dist 
│                │                       ├ [2]: etc/ssl/openssl.cnf 
│                │                       ├ [3]: etc/ssl/openssl.cnf.dist 
│                │                       ├ [4]: usr/lib/libcrypto.so.3 
│                │                       ├ [5]: usr/lib/engines-3/afalg.so 
│                │                       ├ [6]: usr/lib/engines-3/capi.so 
│                │                       ├ [7]: usr/lib/engines-3/loader_attic.so 
│                │                       ├ [8]: usr/lib/engines-3/padlock.so 
│                │                       ╰ [9]: usr/lib/ossl-modules/legacy.so 
│                ├ [26] ╭ ID            : libcurl@8.17.0-r1 
│                │      ├ Name          : libcurl 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libcurl@8.17.0-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 58407caa98add697 
│                │      ├ Version       : 8.17.0-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : curl 
│                │      ├ SrcVersion    : 8.17.0-r1 
│                │      ├ Licenses       ─ [0]: curl 
│                │      ├ Maintainer    : Achill Gilgenast <achill@achill.org> 
│                │      ├ DependsOn      ╭ [0] : brotli-libs@1.2.0-r0 
│                │      │                ├ [1] : c-ares@1.34.5-r0 
│                │      │                ├ [2] : ca-certificates-bundle@20251003-r0 
│                │      │                ├ [3] : libcrypto3@3.5.4-r0 
│                │      │                ├ [4] : libidn2@2.3.8-r0 
│                │      │                ├ [5] : libpsl@0.21.5-r3 
│                │      │                ├ [6] : libssl3@3.5.4-r0 
│                │      │                ├ [7] : musl@1.2.5-r21 
│                │      │                ├ [8] : nghttp2-libs@1.68.0-r0 
│                │      │                ├ [9] : nghttp3@1.13.1-r0 
│                │      │                ├ [10]: zlib@1.3.1-r2 
│                │      │                ╰ [11]: zstd-libs@1.5.7-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4018e686de80aa87659e95c1e62a3539c1d2542f 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libcurl.so.4 
│                │                       ╰ [1]: usr/lib/libcurl.so.4.8.0 
│                ├ [27] ╭ ID            : libeconf@0.8.0-r0 
│                │      ├ Name          : libeconf 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libeconf@0.8.0-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 7ccc0a2ddeed1641 
│                │      ├ Version       : 0.8.0-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libeconf 
│                │      ├ SrcVersion    : 0.8.0-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:75c2033c9c25773a58b22dc199cb02b240247fba 
│                │      ╰ InstalledFiles ╭ [0]: usr/bin/econftool 
│                │                       ├ [1]: usr/lib/libeconf.so.0 
│                │                       ╰ [2]: usr/lib/libeconf.so.0.8.0 
│                ├ [28] ╭ ID            : libevent@2.1.12-r8 
│                │      ├ Name          : libevent 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libevent@2.1.12-r8?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 1c11bf149d42b048 
│                │      ├ Version       : 2.1.12-r8 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libevent 
│                │      ├ SrcVersion    : 2.1.12-r8 
│                │      ├ Licenses       ─ [0]: BSD-3-Clause 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libcrypto3@3.5.4-r0 
│                │      │                ├ [1]: libssl3@3.5.4-r0 
│                │      │                ╰ [2]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:b5d3e42cfb21b218fa78c23d12d58b248f0d1dbe 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libevent-2.1.so.7 
│                │                       ├ [1]: usr/lib/libevent-2.1.so.7.0.1 
│                │                       ├ [2]: usr/lib/libevent_core-2.1.so.7 
│                │                       ├ [3]: usr/lib/libevent_core-2.1.so.7.0.1 
│                │                       ├ [4]: usr/lib/libevent_extra-2.1.so.7 
│                │                       ├ [5]: usr/lib/libevent_extra-2.1.so.7.0.1 
│                │                       ├ [6]: usr/lib/libevent_openssl-2.1.so.7 
│                │                       ├ [7]: usr/lib/libevent_openssl-2.1.so.7.0.1 
│                │                       ├ [8]: usr/lib/libevent_pthreads-2.1.so.7 
│                │                       ╰ [9]: usr/lib/libevent_pthreads-2.1.so.7.0.1 
│                ├ [29] ╭ ID            : libffi@3.5.2-r0 
│                │      ├ Name          : libffi 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libffi@3.5.2-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 4fc060c603e622cf 
│                │      ├ Version       : 3.5.2-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libffi 
│                │      ├ SrcVersion    : 3.5.2-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:50679beb8093d7c2ecbf0a919465b0ed08d80c3f 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libffi.so.8 
│                │                       ╰ [1]: usr/lib/libffi.so.8.2.0 
│                ├ [30] ╭ ID            : libidn2@2.3.8-r0 
│                │      ├ Name          : libidn2 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libidn2@2.3.8-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : c2443df88b387ef9 
│                │      ├ Version       : 2.3.8-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libidn2 
│                │      ├ SrcVersion    : 2.3.8-r0 
│                │      ├ Licenses       ╭ [0]: GPL-2.0-or-later 
│                │      │                ╰ [1]: LGPL-3.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libunistring@1.4.1-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:ae187b51fa0223e13d8a4df74b8e90912f2144d8 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libidn2.so.0 
│                │                       ╰ [1]: usr/lib/libidn2.so.0.4.0 
│                ├ [31] ╭ ID            : libintl@0.24.1-r1 
│                │      ├ Name          : libintl 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libintl@0.24.1-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 53e7c13dd77c5ec5 
│                │      ├ Version       : 0.24.1-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : gettext 
│                │      ├ SrcVersion    : 0.24.1-r1 
│                │      ├ Licenses       ─ [0]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : Carlo Landmeter <clandmeter@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:0d8738141e8b7cf11c830ec8b400e5b43bd1fc6e 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libintl.so.8 
│                │                       ╰ [1]: usr/lib/libintl.so.8.4.3 
│                ├ [32] ╭ ID            : libmount@2.41.2-r0 
│                │      ├ Name          : libmount 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libmount@2.41.2-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : a0f614fbc0540cdc 
│                │      ├ Version       : 2.41.2-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : util-linux 
│                │      ├ SrcVersion    : 2.41.2-r0 
│                │      ├ Licenses       ─ [0]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libblkid@2.41.2-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:48dcba13f62380d0b580cbb60014d08c721d2a36 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libmount.so.1 
│                │                       ╰ [1]: usr/lib/libmount.so.1.1.0 
│                ├ [33] ╭ ID            : libncursesw@6.5_p20251123-r0 
│                │      ├ Name          : libncursesw 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libncursesw@6.5_p20251123-r0?arch=x86_64&distro
│                │      │                │       =3.23.0 
│                │      │                ╰ UID : a35409bd0514dd78 
│                │      ├ Version       : 6.5_p20251123-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : ncurses 
│                │      ├ SrcVersion    : 6.5_p20251123-r0 
│                │      ├ Licenses       ─ [0]: X-11 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: musl@1.2.5-r21 
│                │      │                ╰ [1]: ncurses-terminfo-base@6.5_p20251123-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:649d3041c52b80620fb50a98f5979d25ebbe1523 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libncursesw.so.6 
│                │                       ╰ [1]: usr/lib/libncursesw.so.6.5 
│                ├ [34] ╭ ID            : libproc2@4.0.5-r0 
│                │      ├ Name          : libproc2 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libproc2@4.0.5-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : efa2cac78ce6bca3 
│                │      ├ Version       : 4.0.5-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : procps-ng 
│                │      ├ SrcVersion    : 4.0.5-r0 
│                │      ├ Licenses       ╭ [0]: GPL-2.0-or-later 
│                │      │                ╰ [1]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: musl@1.2.5-r21 
│                │      │                ╰ [1]: utmps-libs@0.1.3.1-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:06de98d317d886db529997f71c177198ddefede5 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libproc2.so.1 
│                │                       ╰ [1]: usr/lib/libproc2.so.1.0.0 
│                ├ [35] ╭ ID            : libpsl@0.21.5-r3 
│                │      ├ Name          : libpsl 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libpsl@0.21.5-r3?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 8b1aec6ba0e2c44f 
│                │      ├ Version       : 0.21.5-r3 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libpsl 
│                │      ├ SrcVersion    : 0.21.5-r3 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libidn2@2.3.8-r0 
│                │      │                ├ [1]: libunistring@1.4.1-r0 
│                │      │                ╰ [2]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:9103905efb1892668c2ffcd27a887ea432feb5ca 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libpsl.so.5 
│                │                       ╰ [1]: usr/lib/libpsl.so.5.3.5 
│                ├ [36] ╭ ID            : libssh2@1.11.1-r1 
│                │      ├ Name          : libssh2 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libssh2@1.11.1-r1?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 9ba037421d7c428e 
│                │      ├ Version       : 1.11.1-r1 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libssh2 
│                │      ├ SrcVersion    : 1.11.1-r1 
│                │      ├ Licenses       ─ [0]: BSD-3-Clause 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libcrypto3@3.5.4-r0 
│                │      │                ├ [1]: musl@1.2.5-r21 
│                │      │                ╰ [2]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4aa1c491e1be97f1d952292428da5386595f36d1 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libssh2.so.1 
│                │                       ╰ [1]: usr/lib/libssh2.so.1.0.1 
│                ├ [37] ╭ ID            : libssl3@3.5.4-r0 
│                │      ├ Name          : libssl3 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libssl3@3.5.4-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 99db358db738ceeb 
│                │      ├ Version       : 3.5.4-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : openssl 
│                │      ├ SrcVersion    : 3.5.4-r0 
│                │      ├ Licenses       ─ [0]: Apache-2.0 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libcrypto3@3.5.4-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:6fb228fd4cbe34e05c60028aeace1dad4855e2c2 
│                │      ╰ InstalledFiles ─ [0]: usr/lib/libssl.so.3 
│                ├ [38] ╭ ID            : libunistring@1.4.1-r0 
│                │      ├ Name          : libunistring 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/libunistring@1.4.1-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 7200a20237fda131 
│                │      ├ Version       : 1.4.1-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : libunistring 
│                │      ├ SrcVersion    : 1.4.1-r0 
│                │      ├ Licenses       ╭ [0]: GPL-2.0-or-later 
│                │      │                ╰ [1]: LGPL-3.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:6e56562bde456bee5971787d3d95c34e84ced797 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libunistring.so.5 
│                │                       ╰ [1]: usr/lib/libunistring.so.5.2.1 
│                ├ [39] ╭ ID            : man-pages@6.16-r0 
│                │      ├ Name          : man-pages 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/man-pages@6.16-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : e43b7134bab197be 
│                │      ├ Version       : 6.16-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : man-pages 
│                │      ├ SrcVersion    : 6.16-r0 
│                │      ├ Licenses       ─ [0]: GPL-2.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:d5c824499142b26479c1b6cb066cd673e4572025 
│                │      ╰ InstalledFiles ╭ [0]   : usr/bin/diffman-git 
│                │                       ├ [1]   : usr/bin/mansect 
│                │                       ├ [2]   : usr/bin/pdfman 
│                │                       ├ [3]   : usr/bin/sortman 
│                │                       ├ [4]   : usr/share/man/man1/diffman-git.1.gz 
│                │                       ├ [5]   : usr/share/man/man1/getent.1.gz 
│                │                       ├ [6]   : usr/share/man/man1/intro.1.gz 
│                │                       ├ [7]   : usr/share/man/man1/ldd.1.gz 
│                │                       ├ [8]   : usr/share/man/man1/locale.1.gz 
│                │                       ├ [9]   : usr/share/man/man1/localedef.1.gz 
│                │                       ├ [10]  : usr/share/man/man1/mansect.1.gz 
│                │                       ├ [11]  : usr/share/man/man1/memusage.1.gz 
│                │                       ├ [12]  : usr/share/man/man1/memusagestat.1.gz 
│                │                       ├ [13]  : usr/share/man/man1/mtrace.1.gz 
│                │                       ├ [14]  : usr/share/man/man1/pdfman.1.gz 
│                │                       ├ [15]  : usr/share/man/man1/pldd.1.gz 
│                │                       ├ [16]  : usr/share/man/man1/sortman.1.gz 
│                │                       ├ [17]  : usr/share/man/man1/sprof.1.gz 
│                │                       ├ [18]  : usr/share/man/man1/time.1.gz 
│                │                       ├ [19]  : usr/share/man/man2/_Exit.2.gz 
│                │                       ├ [20]  : usr/share/man/man2/__clone2.2.gz 
│                │                       ├ [21]  : usr/share/man/man2/_exit.2.gz 
│                │                       ├ [22]  : usr/share/man/man2/_llseek.2.gz 
│                │                       ├ [23]  : usr/share/man/man2/_newselect.2.gz 
│                │                       ├ [24]  : usr/share/man/man2/_syscall.2.gz 
│                │                       ├ [25]  : usr/share/man/man2/_sysctl.2.gz 
│                │                       ├ [26]  : usr/share/man/man2/accept.2.gz 
│                │                       ├ [27]  : usr/share/man/man2/accept4.2.gz 
│                │                       ├ [28]  : usr/share/man/man2/access.2.gz 
│                │                       ├ [29]  : usr/share/man/man2/acct.2.gz 
│                │                       ├ [30]  : usr/share/man/man2/add_key.2.gz 
│                │                       ├ [31]  : usr/share/man/man2/adjtimex.2.gz 
│                │                       ├ [32]  : usr/share/man/man2/afs_syscall.2.gz 
│                │                       ├ [33]  : usr/share/man/man2/alarm.2.gz 
│                │                       ├ [34]  : usr/share/man/man2/alloc_hugepages.2.gz 
│                │                       ├ [35]  : usr/share/man/man2/arch_prctl.2.gz 
│                │                       ├ [36]  : usr/share/man/man2/arm_fadvise.2.gz 
│                │                       ├ [37]  : usr/share/man/man2/arm_fadvise64_64.2.gz 
│                │                       ├ [38]  : usr/share/man/man2/arm_sync_file_range.2.gz 
│                │                       ├ [39]  : usr/share/man/man2/bdflush.2.gz 
│                │                       ├ [40]  : usr/share/man/man2/bind.2.gz 
│                │                       ├ [41]  : usr/share/man/man2/bpf.2.gz 
│                │                       ├ [42]  : usr/share/man/man2/break.2.gz 
│                │                       ├ [43]  : usr/share/man/man2/brk.2.gz 
│                │                       ├ [44]  : usr/share/man/man2/cacheflush.2.gz 
│                │                       ├ [45]  : usr/share/man/man2/cachestat.2.gz 
│                │                       ├ [46]  : usr/share/man/man2/capget.2.gz 
│                │                       ├ [47]  : usr/share/man/man2/capset.2.gz 
│                │                       ├ [48]  : usr/share/man/man2/chdir.2.gz 
│                │                       ├ [49]  : usr/share/man/man2/chmod.2.gz 
│                │                       ├ [50]  : usr/share/man/man2/chown.2.gz 
│                │                       ├ [51]  : usr/share/man/man2/chown32.2.gz 
│                │                       ├ [52]  : usr/share/man/man2/chroot.2.gz 
│                │                       ├ [53]  : usr/share/man/man2/clock_adjtime.2.gz 
│                │                       ├ [54]  : usr/share/man/man2/clock_getres.2.gz 
│                │                       ├ [55]  : usr/share/man/man2/clock_gettime.2.gz 
│                │                       ├ [56]  : usr/share/man/man2/clock_nanosleep.2.gz 
│                │                       ├ [57]  : usr/share/man/man2/clock_settime.2.gz 
│                │                       ├ [58]  : usr/share/man/man2/clone.2.gz 
│                │                       ├ [59]  : usr/share/man/man2/clone2.2.gz 
│                │                       ├ [60]  : usr/share/man/man2/clone3.2.gz 
│                │                       ├ [61]  : usr/share/man/man2/close.2.gz 
│                │                       ├ [62]  : usr/share/man/man2/close_range.2.gz 
│                │                       ├ [63]  : usr/share/man/man2/connect.2.gz 
│                │                       ├ [64]  : usr/share/man/man2/copy_file_range.2.gz 
│                │                       ├ [65]  : usr/share/man/man2/creat.2.gz 
│                │                       ├ [66]  : usr/share/man/man2/create_module.2.gz 
│                │                       ├ [67]  : usr/share/man/man2/delete_module.2.gz 
│                │                       ├ [68]  : usr/share/man/man2/dup.2.gz 
│                │                       ├ [69]  : usr/share/man/man2/dup2.2.gz 
│                │                       ├ [70]  : usr/share/man/man2/dup3.2.gz 
│                │                       ├ [71]  : usr/share/man/man2/epoll_create.2.gz 
│                │                       ├ [72]  : usr/share/man/man2/epoll_create1.2.gz 
│                │                       ├ [73]  : usr/share/man/man2/epoll_ctl.2.gz 
│                │                       ├ [74]  : usr/share/man/man2/epoll_pwait.2.gz 
│                │                       ├ [75]  : usr/share/man/man2/epoll_pwait2.2.gz 
│                │                       ├ [76]  : usr/share/man/man2/epoll_wait.2.gz 
│                │                       ├ [77]  : usr/share/man/man2/eventfd.2.gz 
│                │                       ├ [78]  : usr/share/man/man2/eventfd2.2.gz 
│                │                       ├ [79]  : usr/share/man/man2/execve.2.gz 
│                │                       ├ [80]  : usr/share/man/man2/execveat.2.gz 
│                │                       ├ [81]  : usr/share/man/man2/exit.2.gz 
│                │                       ├ [82]  : usr/share/man/man2/exit_group.2.gz 
│                │                       ├ [83]  : usr/share/man/man2/faccessat.2.gz 
│                │                       ├ [84]  : usr/share/man/man2/faccessat2.2.gz 
│                │                       ├ [85]  : usr/share/man/man2/fadvise64.2.gz 
│                │                       ├ [86]  : usr/share/man/man2/fadvise64_64.2.gz 
│                │                       ├ [87]  : usr/share/man/man2/fallocate.2.gz 
│                │                       ├ [88]  : usr/share/man/man2/fanotify_init.2.gz 
│                │                       ├ [89]  : usr/share/man/man2/fanotify_mark.2.gz 
│                │                       ├ [90]  : usr/share/man/man2/fattach.2.gz 
│                │                       ├ [91]  : usr/share/man/man2/fchdir.2.gz 
│                │                       ├ [92]  : usr/share/man/man2/fchmod.2.gz 
│                │                       ├ [93]  : usr/share/man/man2/fchmodat.2.gz 
│                │                       ├ [94]  : usr/share/man/man2/fchown.2.gz 
│                │                       ├ [95]  : usr/share/man/man2/fchown32.2.gz 
│                │                       ├ [96]  : usr/share/man/man2/fchownat.2.gz 
│                │                       ├ [97]  : usr/share/man/man2/fcntl.2.gz 
│                │                       ├ [98]  : usr/share/man/man2/fcntl64.2.gz 
│                │                       ├ [99]  : usr/share/man/man2/fcntl_locking.2.gz 
│                │                       ├ [100] : usr/share/man/man2/fdatasync.2.gz 
│                │                       ├ [101] : usr/share/man/man2/fdetach.2.gz 
│                │                       ├ [102] : usr/share/man/man2/fgetxattr.2.gz 
│                │                       ├ [103] : usr/share/man/man2/finit_module.2.gz 
│                │                       ├ [104] : usr/share/man/man2/flistxattr.2.gz 
│                │                       ├ [105] : usr/share/man/man2/flock.2.gz 
│                │                       ├ [106] : usr/share/man/man2/fork.2.gz 
│                │                       ├ [107] : usr/share/man/man2/free_hugepages.2.gz 
│                │                       ├ [108] : usr/share/man/man2/fremovexattr.2.gz 
│                │                       ├ [109] : usr/share/man/man2/fsconfig.2.gz 
│                │                       ├ [110] : usr/share/man/man2/fsetxattr.2.gz 
│                │                       ├ [111] : usr/share/man/man2/fsmount.2.gz 
│                │                       ├ [112] : usr/share/man/man2/fsopen.2.gz 
│                │                       ├ [113] : usr/share/man/man2/fspick.2.gz 
│                │                       ├ [114] : usr/share/man/man2/fstat.2.gz 
│                │                       ├ [115] : usr/share/man/man2/fstat64.2.gz 
│                │                       ├ [116] : usr/share/man/man2/fstatat.2.gz 
│                │                       ├ [117] : usr/share/man/man2/fstatat64.2.gz 
│                │                       ├ [118] : usr/share/man/man2/fstatfs.2.gz 
│                │                       ├ [119] : usr/share/man/man2/fstatfs64.2.gz 
│                │                       ├ [120] : usr/share/man/man2/fsync.2.gz 
│                │                       ├ [121] : usr/share/man/man2/ftruncate.2.gz 
│                │                       ├ [122] : usr/share/man/man2/ftruncate64.2.gz 
│                │                       ├ [123] : usr/share/man/man2/futex.2.gz 
│                │                       ├ [124] : usr/share/man/man2/futimesat.2.gz 
│                │                       ├ [125] : usr/share/man/man2/get_kernel_syms.2.gz 
│                │                       ├ [126] : usr/share/man/man2/get_mempolicy.2.gz 
│                │                       ├ [127] : usr/share/man/man2/get_robust_list.2.gz 
│                │                       ├ [128] : usr/share/man/man2/get_thread_area.2.gz 
│                │                       ├ [129] : usr/share/man/man2/getcpu.2.gz 
│                │                       ├ [130] : usr/share/man/man2/getcwd.2.gz 
│                │                       ├ [131] : usr/share/man/man2/getdents.2.gz 
│                │                       ├ [132] : usr/share/man/man2/getdents64.2.gz 
│                │                       ├ [133] : usr/share/man/man2/getdomainname.2.gz 
│                │                       ├ [134] : usr/share/man/man2/getegid.2.gz 
│                │                       ├ [135] : usr/share/man/man2/getegid32.2.gz 
│                │                       ├ [136] : usr/share/man/man2/geteuid.2.gz 
│                │                       ├ [137] : usr/share/man/man2/geteuid32.2.gz 
│                │                       ├ [138] : usr/share/man/man2/getgid.2.gz 
│                │                       ├ [139] : usr/share/man/man2/getgid32.2.gz 
│                │                       ├ [140] : usr/share/man/man2/getgroups.2.gz 
│                │                       ├ [141] : usr/share/man/man2/getgroups32.2.gz 
│                │                       ├ [142] : usr/share/man/man2/gethostname.2.gz 
│                │                       ├ [143] : usr/share/man/man2/getitimer.2.gz 
│                │                       ├ [144] : usr/share/man/man2/getmsg.2.gz 
│                │                       ├ [145] : usr/share/man/man2/getpagesize.2.gz 
│                │                       ├ [146] : usr/share/man/man2/getpeername.2.gz 
│                │                       ├ [147] : usr/share/man/man2/getpgid.2.gz 
│                │                       ├ [148] : usr/share/man/man2/getpgrp.2.gz 
│                │                       ├ [149] : usr/share/man/man2/getpid.2.gz 
│                │                       ├ [150] : usr/share/man/man2/getpmsg.2.gz 
│                │                       ├ [151] : usr/share/man/man2/getppid.2.gz 
│                │                       ├ [152] : usr/share/man/man2/getpriority.2.gz 
│                │                       ├ [153] : usr/share/man/man2/getrandom.2.gz 
│                │                       ├ [154] : usr/share/man/man2/getresgid.2.gz 
│                │                       ├ [155] : usr/share/man/man2/getresgid32.2.gz 
│                │                       ├ [156] : usr/share/man/man2/getresuid.2.gz 
│                │                       ├ [157] : usr/share/man/man2/getresuid32.2.gz 
│                │                       ├ [158] : usr/share/man/man2/getrlimit.2.gz 
│                │                       ├ [159] : usr/share/man/man2/getrusage.2.gz 
│                │                       ├ [160] : usr/share/man/man2/getsid.2.gz 
│                │                       ├ [161] : usr/share/man/man2/getsockname.2.gz 
│                │                       ├ [162] : usr/share/man/man2/getsockopt.2.gz 
│                │                       ├ [163] : usr/share/man/man2/gettid.2.gz 
│                │                       ├ [164] : usr/share/man/man2/gettimeofday.2.gz 
│                │                       ├ [165] : usr/share/man/man2/getuid.2.gz 
│                │                       ├ [166] : usr/share/man/man2/getuid32.2.gz 
│                │                       ├ [167] : usr/share/man/man2/getunwind.2.gz 
│                │                       ├ [168] : usr/share/man/man2/getxattr.2.gz 
│                │                       ├ [169] : usr/share/man/man2/gtty.2.gz 
│                │                       ├ [170] : usr/share/man/man2/idle.2.gz 
│                │                       ├ [171] : usr/share/man/man2/inb.2.gz 
│                │                       ├ [172] : usr/share/man/man2/inb_p.2.gz 
│                │                       ├ [173] : usr/share/man/man2/init_module.2.gz 
│                │                       ├ [174] : usr/share/man/man2/inl.2.gz 
│                │                       ├ [175] : usr/share/man/man2/inl_p.2.gz 
│                │                       ├ [176] : usr/share/man/man2/inotify_add_watch.2.gz 
│                │                       ├ [177] : usr/share/man/man2/inotify_init.2.gz 
│                │                       ├ [178] : usr/share/man/man2/inotify_init1.2.gz 
│                │                       ├ [179] : usr/share/man/man2/inotify_rm_watch.2.gz 
│                │                       ├ [180] : usr/share/man/man2/insb.2.gz 
│                │                       ├ [181] : usr/share/man/man2/insl.2.gz 
│                │                       ├ [182] : usr/share/man/man2/insw.2.gz 
│                │                       ├ [183] : usr/share/man/man2/intro.2.gz 
│                │                       ├ [184] : usr/share/man/man2/inw.2.gz 
│                │                       ├ [185] : usr/share/man/man2/inw_p.2.gz 
│                │                       ├ [186] : usr/share/man/man2/io_cancel.2.gz 
│                │                       ├ [187] : usr/share/man/man2/io_destroy.2.gz 
│                │                       ├ [188] : usr/share/man/man2/io_getevents.2.gz 
│                │                       ├ [189] : usr/share/man/man2/io_setup.2.gz 
│                │                       ├ [190] : usr/share/man/man2/io_submit.2.gz 
│                │                       ├ [191] : usr/share/man/man2/ioctl.2.gz 
│                │                       ├ [192] : usr/share/man/man2/ioctl_console.2.gz 
│                │                       ├ [193] : usr/share/man/man2/ioctl_eventpoll.2.gz 
│                │                       ├ [194] : usr/share/man/man2/ioctl_fat.2.gz 
│                │                       ├ [195] : usr/share/man/man2/ioctl_fs.2.gz 
│                │                       ├ [196] : usr/share/man/man2/ioctl_fsmap.2.gz 
│                │                       ├ [197] : usr/share/man/man2/ioctl_kd.2.gz 
│                │                       ├ [198] : usr/share/man/man2/ioctl_nsfs.2.gz 
│                │                       ├ [199] : usr/share/man/man2/ioctl_pipe.2.gz 
│                │                       ├ [200] : usr/share/man/man2/ioctl_tty.2.gz 
│                │                       ├ [201] : usr/share/man/man2/ioctl_userfaultfd.2.gz 
│                │                       ├ [202] : usr/share/man/man2/ioctl_vt.2.gz 
│                │                       ├ [203] : usr/share/man/man2/ioperm.2.gz 
│                │                       ├ [204] : usr/share/man/man2/iopl.2.gz 
│                │                       ├ [205] : usr/share/man/man2/ioprio_get.2.gz 
│                │                       ├ [206] : usr/share/man/man2/ioprio_set.2.gz 
│                │                       ├ [207] : usr/share/man/man2/ipc.2.gz 
│                │                       ├ [208] : usr/share/man/man2/isastream.2.gz 
│                │                       ├ [209] : usr/share/man/man2/kcmp.2.gz 
│                │                       ├ [210] : usr/share/man/man2/kexec_file_load.2.gz 
│                │                       ├ [211] : usr/share/man/man2/kexec_load.2.gz 
│                │                       ├ [212] : usr/share/man/man2/keyctl.2.gz 
│                │                       ├ [213] : usr/share/man/man2/kill.2.gz 
│                │                       ├ [214] : usr/share/man/man2/landlock_add_rule.2.gz 
│                │                       ├ [215] : usr/share/man/man2/landlock_create_ruleset.2.gz 
│                │                       ├ [216] : usr/share/man/man2/landlock_restrict_self.2.gz 
│                │                       ├ [217] : usr/share/man/man2/lchown.2.gz 
│                │                       ├ [218] : usr/share/man/man2/lchown32.2.gz 
│                │                       ├ [219] : usr/share/man/man2/lgetxattr.2.gz 
│                │                       ├ [220] : usr/share/man/man2/link.2.gz 
│                │                       ├ [221] : usr/share/man/man2/linkat.2.gz 
│                │                       ├ [222] : usr/share/man/man2/listen.2.gz 
│                │                       ├ [223] : usr/share/man/man2/listmount.2.gz 
│                │                       ├ [224] : usr/share/man/man2/listxattr.2.gz 
│                │                       ├ [225] : usr/share/man/man2/llistxattr.2.gz 
│                │                       ├ [226] : usr/share/man/man2/llseek.2.gz 
│                │                       ├ [227] : usr/share/man/man2/lock.2.gz 
│                │                       ├ [228] : usr/share/man/man2/lookup_dcookie.2.gz 
│                │                       ├ [229] : usr/share/man/man2/lremovexattr.2.gz 
│                │                       ├ [230] : usr/share/man/man2/lseek.2.gz 
│                │                       ├ [231] : usr/share/man/man2/lsetxattr.2.gz 
│                │                       ├ [232] : usr/share/man/man2/lstat.2.gz 
│                │                       ├ [233] : usr/share/man/man2/lstat64.2.gz 
│                │                       ├ [234] : usr/share/man/man2/madvise.2.gz 
│                │                       ├ [235] : usr/share/man/man2/madvise1.2.gz 
│                │                       ├ [236] : usr/share/man/man2/mbind.2.gz 
│                │                       ├ [237] : usr/share/man/man2/membarrier.2.gz 
│                │                       ├ [238] : usr/share/man/man2/memfd_create.2.gz 
│                │                       ├ [239] : usr/share/man/man2/memfd_secret.2.gz 
│                │                       ├ [240] : usr/share/man/man2/migrate_pages.2.gz 
│                │                       ├ [241] : usr/share/man/man2/mincore.2.gz 
│                │                       ├ [242] : usr/share/man/man2/mkdir.2.gz 
│                │                       ├ [243] : usr/share/man/man2/mkdirat.2.gz 
│                │                       ├ [244] : usr/share/man/man2/mknod.2.gz 
│                │                       ├ [245] : usr/share/man/man2/mknodat.2.gz 
│                │                       ├ [246] : usr/share/man/man2/mlock.2.gz 
│                │                       ├ [247] : usr/share/man/man2/mlock2.2.gz 
│                │                       ├ [248] : usr/share/man/man2/mlockall.2.gz 
│                │                       ├ [249] : usr/share/man/man2/mmap.2.gz 
│                │                       ├ [250] : usr/share/man/man2/mmap2.2.gz 
│                │                       ├ [251] : usr/share/man/man2/modify_ldt.2.gz 
│                │                       ├ [252] : usr/share/man/man2/mount.2.gz 
│                │                       ├ [253] : usr/share/man/man2/mount_setattr.2.gz 
│                │                       ├ [254] : usr/share/man/man2/move_mount.2.gz 
│                │                       ├ [255] : usr/share/man/man2/move_pages.2.gz 
│                │                       ├ [256] : usr/share/man/man2/mprotect.2.gz 
│                │                       ├ [257] : usr/share/man/man2/mpx.2.gz 
│                │                       ├ [258] : usr/share/man/man2/mq_getsetattr.2.gz 
│                │                       ├ [259] : usr/share/man/man2/mq_notify.2.gz 
│                │                       ├ [260] : usr/share/man/man2/mq_open.2.gz 
│                │                       ├ [261] : usr/share/man/man2/mq_timedreceive.2.gz 
│                │                       ├ [262] : usr/share/man/man2/mq_timedsend.2.gz 
│                │                       ├ [263] : usr/share/man/man2/mq_unlink.2.gz 
│                │                       ├ [264] : usr/share/man/man2/mremap.2.gz 
│                │                       ├ [265] : usr/share/man/man2/msgctl.2.gz 
│                │                       ├ [266] : usr/share/man/man2/msgget.2.gz 
│                │                       ├ [267] : usr/share/man/man2/msgop.2.gz 
│                │                       ├ [268] : usr/share/man/man2/msgrcv.2.gz 
│                │                       ├ [269] : usr/share/man/man2/msgsnd.2.gz 
│                │                       ├ [270] : usr/share/man/man2/msync.2.gz 
│                │                       ├ [271] : usr/share/man/man2/munlock.2.gz 
│                │                       ├ [272] : usr/share/man/man2/munlockall.2.gz 
│                │                       ├ [273] : usr/share/man/man2/munmap.2.gz 
│                │                       ├ [274] : usr/share/man/man2/name_to_handle_at.2.gz 
│                │                       ├ [275] : usr/share/man/man2/nanosleep.2.gz 
│                │                       ├ [276] : usr/share/man/man2/newfstatat.2.gz 
│                │                       ├ [277] : usr/share/man/man2/nfsservctl.2.gz 
│                │                       ├ [278] : usr/share/man/man2/nice.2.gz 
│                │                       ├ [279] : usr/share/man/man2/oldfstat.2.gz 
│                │                       ├ [280] : usr/share/man/man2/oldlstat.2.gz 
│                │                       ├ [281] : usr/share/man/man2/oldolduname.2.gz 
│                │                       ├ [282] : usr/share/man/man2/oldstat.2.gz 
│                │                       ├ [283] : usr/share/man/man2/olduname.2.gz 
│                │                       ├ [284] : usr/share/man/man2/open.2.gz 
│                │                       ├ [285] : usr/share/man/man2/open_by_handle_at.2.gz 
│                │                       ├ [286] : usr/share/man/man2/open_tree.2.gz 
│                │                       ├ [287] : usr/share/man/man2/open_tree_attr.2.gz 
│                │                       ├ [288] : usr/share/man/man2/openat.2.gz 
│                │                       ├ [289] : usr/share/man/man2/openat2.2.gz 
│                │                       ├ [290] : usr/share/man/man2/outb.2.gz 
│                │                       ├ [291] : usr/share/man/man2/outb_p.2.gz 
│                │                       ├ [292] : usr/share/man/man2/outl.2.gz 
│                │                       ├ [293] : usr/share/man/man2/outl_p.2.gz 
│                │                       ├ [294] : usr/share/man/man2/outsb.2.gz 
│                │                       ├ [295] : usr/share/man/man2/outsl.2.gz 
│                │                       ├ [296] : usr/share/man/man2/outsw.2.gz 
│                │                       ├ [297] : usr/share/man/man2/outw.2.gz 
│                │                       ├ [298] : usr/share/man/man2/outw_p.2.gz 
│                │                       ├ [299] : usr/share/man/man2/pause.2.gz 
│                │                       ├ [300] : usr/share/man/man2/pciconfig_iobase.2.gz 
│                │                       ├ [301] : usr/share/man/man2/pciconfig_read.2.gz 
│                │                       ├ [302] : usr/share/man/man2/pciconfig_write.2.gz 
│                │                       ├ [303] : usr/share/man/man2/perf_event_open.2.gz 
│                │                       ├ [304] : usr/share/man/man2/perfmonctl.2.gz 
│                │                       ├ [305] : usr/share/man/man2/personality.2.gz 
│                │                       ├ [306] : usr/share/man/man2/phys.2.gz 
│                │                       ├ [307] : usr/share/man/man2/pidfd_getfd.2.gz 
│                │                       ├ [308] : usr/share/man/man2/pidfd_open.2.gz 
│                │                       ├ [309] : usr/share/man/man2/pidfd_send_signal.2.gz 
│                │                       ├ [310] : usr/share/man/man2/pipe.2.gz 
│                │                       ├ [311] : usr/share/man/man2/pipe2.2.gz 
│                │                       ├ [312] : usr/share/man/man2/pivot_root.2.gz 
│                │                       ├ [313] : usr/share/man/man2/pkey_alloc.2.gz 
│                │                       ├ [314] : usr/share/man/man2/pkey_free.2.gz 
│                │                       ├ [315] : usr/share/man/man2/pkey_mprotect.2.gz 
│                │                       ├ [316] : usr/share/man/man2/poll.2.gz 
│                │                       ├ [317] : usr/share/man/man2/posix_fadvise.2.gz 
│                │                       ├ [318] : usr/share/man/man2/ppoll.2.gz 
│                │                       ├ [319] : usr/share/man/man2/prctl.2.gz 
│                │                       ├ [320] : usr/share/man/man2/pread.2.gz 
│                │                       ├ [321] : usr/share/man/man2/pread64.2.gz 
│                │                       ├ [322] : usr/share/man/man2/preadv.2.gz 
│                │                       ├ [323] : usr/share/man/man2/preadv2.2.gz 
│                │                       ├ [324] : usr/share/man/man2/prlimit.2.gz 
│                │                       ├ [325] : usr/share/man/man2/prlimit64.2.gz 
│                │                       ├ [326] : usr/share/man/man2/process_madvise.2.gz 
│                │                       ├ [327] : usr/share/man/man2/process_vm_readv.2.gz 
│                │                       ├ [328] : usr/share/man/man2/process_vm_writev.2.gz 
│                │                       ├ [329] : usr/share/man/man2/prof.2.gz 
│                │                       ├ [330] : usr/share/man/man2/pselect.2.gz 
│                │                       ├ [331] : usr/share/man/man2/pselect6.2.gz 
│                │                       ├ [332] : usr/share/man/man2/ptrace.2.gz 
│                │                       ├ [333] : usr/share/man/man2/putmsg.2.gz 
│                │                       ├ [334] : usr/share/man/man2/putpmsg.2.gz 
│                │                       ├ [335] : usr/share/man/man2/pwrite.2.gz 
│                │                       ├ [336] : usr/share/man/man2/pwrite64.2.gz 
│                │                       ├ [337] : usr/share/man/man2/pwritev.2.gz 
│                │                       ├ [338] : usr/share/man/man2/pwritev2.2.gz 
│                │                       ├ [339] : usr/share/man/man2/query_module.2.gz 
│                │                       ├ [340] : usr/share/man/man2/quotactl.2.gz 
│                │                       ├ [341] : usr/share/man/man2/quotactl_fd.2.gz 
│                │                       ├ [342] : usr/share/man/man2/read.2.gz 
│                │                       ├ [343] : usr/share/man/man2/readahead.2.gz 
│                │                       ├ [344] : usr/share/man/man2/readdir.2.gz 
│                │                       ├ [345] : usr/share/man/man2/readlink.2.gz 
│                │                       ├ [346] : usr/share/man/man2/readlinkat.2.gz 
│                │                       ├ [347] : usr/share/man/man2/readv.2.gz 
│                │                       ├ [348] : usr/share/man/man2/reboot.2.gz 
│                │                       ├ [349] : usr/share/man/man2/recv.2.gz 
│                │                       ├ [350] : usr/share/man/man2/recvfrom.2.gz 
│                │                       ├ [351] : usr/share/man/man2/recvmmsg.2.gz 
│                │                       ├ [352] : usr/share/man/man2/recvmsg.2.gz 
│                │                       ├ [353] : usr/share/man/man2/remap_file_pages.2.gz 
│                │                       ├ [354] : usr/share/man/man2/removexattr.2.gz 
│                │                       ├ [355] : usr/share/man/man2/rename.2.gz 
│                │                       ├ [356] : usr/share/man/man2/renameat.2.gz 
│                │                       ├ [357] : usr/share/man/man2/renameat2.2.gz 
│                │                       ├ [358] : usr/share/man/man2/request_key.2.gz 
│                │                       ├ [359] : usr/share/man/man2/restart_syscall.2.gz 
│                │                       ├ [360] : usr/share/man/man2/riscv_flush_icache.2.gz 
│                │                       ├ [361] : usr/share/man/man2/rmdir.2.gz 
│                │                       ├ [362] : usr/share/man/man2/rt_sigaction.2.gz 
│                │                       ├ [363] : usr/share/man/man2/rt_sigpending.2.gz 
│                │                       ├ [364] : usr/share/man/man2/rt_sigprocmask.2.gz 
│                │                       ├ [365] : usr/share/man/man2/rt_sigqueueinfo.2.gz 
│                │                       ├ [366] : usr/share/man/man2/rt_sigreturn.2.gz 
│                │                       ├ [367] : usr/share/man/man2/rt_sigsuspend.2.gz 
│                │                       ├ [368] : usr/share/man/man2/rt_sigtimedwait.2.gz 
│                │                       ├ [369] : usr/share/man/man2/rt_tgsigqueueinfo.2.gz 
│                │                       ├ [370] : usr/share/man/man2/s390_guarded_storage.2.gz 
│                │                       ├ [371] : usr/share/man/man2/s390_pci_mmio_read.2.gz 
│                │                       ├ [372] : usr/share/man/man2/s390_pci_mmio_write.2.gz 
│                │                       ├ [373] : usr/share/man/man2/s390_runtime_instr.2.gz 
│                │                       ├ [374] : usr/share/man/man2/s390_sthyi.2.gz 
│                │                       ├ [375] : usr/share/man/man2/sbrk.2.gz 
│                │                       ├ [376] : usr/share/man/man2/sched_get_priority_max.2.gz 
│                │                       ├ [377] : usr/share/man/man2/sched_get_priority_min.2.gz 
│                │                       ├ [378] : usr/share/man/man2/sched_getaffinity.2.gz 
│                │                       ├ [379] : usr/share/man/man2/sched_getattr.2.gz 
│                │                       ├ [380] : usr/share/man/man2/sched_getparam.2.gz 
│                │                       ├ [381] : usr/share/man/man2/sched_getscheduler.2.gz 
│                │                       ├ [382] : usr/share/man/man2/sched_rr_get_interval.2.gz 
│                │                       ├ [383] : usr/share/man/man2/sched_setaffinity.2.gz 
│                │                       ├ [384] : usr/share/man/man2/sched_setattr.2.gz 
│                │                       ├ [385] : usr/share/man/man2/sched_setparam.2.gz 
│                │                       ├ [386] : usr/share/man/man2/sched_setscheduler.2.gz 
│                │                       ├ [387] : usr/share/man/man2/sched_yield.2.gz 
│                │                       ├ [388] : usr/share/man/man2/seccomp.2.gz 
│                │                       ├ [389] : usr/share/man/man2/seccomp_unotify.2.gz 
│                │                       ├ [390] : usr/share/man/man2/security.2.gz 
│                │                       ├ [391] : usr/share/man/man2/select.2.gz 
│                │                       ├ [392] : usr/share/man/man2/select_tut.2.gz 
│                │                       ├ [393] : usr/share/man/man2/semctl.2.gz 
│                │                       ├ [394] : usr/share/man/man2/semget.2.gz 
│                │                       ├ [395] : usr/share/man/man2/semop.2.gz 
│                │                       ├ [396] : usr/share/man/man2/semtimedop.2.gz 
│                │                       ├ [397] : usr/share/man/man2/send.2.gz 
│                │                       ├ [398] : usr/share/man/man2/sendfile.2.gz 
│                │                       ├ [399] : usr/share/man/man2/sendfile64.2.gz 
│                │                       ├ [400] : usr/share/man/man2/sendmmsg.2.gz 
│                │                       ├ [401] : usr/share/man/man2/sendmsg.2.gz 
│                │                       ├ [402] : usr/share/man/man2/sendto.2.gz 
│                │                       ├ [403] : usr/share/man/man2/set_mempolicy.2.gz 
│                │                       ├ [404] : usr/share/man/man2/set_robust_list.2.gz 
│                │                       ├ [405] : usr/share/man/man2/set_thread_area.2.gz 
│                │                       ├ [406] : usr/share/man/man2/set_tid_address.2.gz 
│                │                       ├ [407] : usr/share/man/man2/setdomainname.2.gz 
│                │                       ├ [408] : usr/share/man/man2/setegid.2.gz 
│                │                       ├ [409] : usr/share/man/man2/seteuid.2.gz 
│                │                       ├ [410] : usr/share/man/man2/setfsgid.2.gz 
│                │                       ├ [411] : usr/share/man/man2/setfsgid32.2.gz 
│                │                       ├ [412] : usr/share/man/man2/setfsuid.2.gz 
│                │                       ├ [413] : usr/share/man/man2/setfsuid32.2.gz 
│                │                       ├ [414] : usr/share/man/man2/setgid.2.gz 
│                │                       ├ [415] : usr/share/man/man2/setgid32.2.gz 
│                │                       ├ [416] : usr/share/man/man2/setgroups.2.gz 
│                │                       ├ [417] : usr/share/man/man2/setgroups32.2.gz 
│                │                       ├ [418] : usr/share/man/man2/sethostname.2.gz 
│                │                       ├ [419] : usr/share/man/man2/setitimer.2.gz 
│                │                       ├ [420] : usr/share/man/man2/setns.2.gz 
│                │                       ├ [421] : usr/share/man/man2/setpgid.2.gz 
│                │                       ├ [422] : usr/share/man/man2/setpgrp.2.gz 
│                │                       ├ [423] : usr/share/man/man2/setpriority.2.gz 
│                │                       ├ [424] : usr/share/man/man2/setregid.2.gz 
│                │                       ├ [425] : usr/share/man/man2/setregid32.2.gz 
│                │                       ├ [426] : usr/share/man/man2/setresgid.2.gz 
│                │                       ├ [427] : usr/share/man/man2/setresgid32.2.gz 
│                │                       ├ [428] : usr/share/man/man2/setresuid.2.gz 
│                │                       ├ [429] : usr/share/man/man2/setresuid32.2.gz 
│                │                       ├ [430] : usr/share/man/man2/setreuid.2.gz 
│                │                       ├ [431] : usr/share/man/man2/setreuid32.2.gz 
│                │                       ├ [432] : usr/share/man/man2/setrlimit.2.gz 
│                │                       ├ [433] : usr/share/man/man2/setsid.2.gz 
│                │                       ├ [434] : usr/share/man/man2/setsockopt.2.gz 
│                │                       ├ [435] : usr/share/man/man2/settimeofday.2.gz 
│                │                       ├ [436] : usr/share/man/man2/setuid.2.gz 
│                │                       ├ [437] : usr/share/man/man2/setuid32.2.gz 
│                │                       ├ [438] : usr/share/man/man2/setup.2.gz 
│                │                       ├ [439] : usr/share/man/man2/setxattr.2.gz 
│                │                       ├ [440] : usr/share/man/man2/sgetmask.2.gz 
│                │                       ├ [441] : usr/share/man/man2/shmat.2.gz 
│                │                       ├ [442] : usr/share/man/man2/shmctl.2.gz 
│                │                       ├ [443] : usr/share/man/man2/shmdt.2.gz 
│                │                       ├ [444] : usr/share/man/man2/shmget.2.gz 
│                │                       ├ [445] : usr/share/man/man2/shmop.2.gz 
│                │                       ├ [446] : usr/share/man/man2/shutdown.2.gz 
│                │                       ├ [447] : usr/share/man/man2/sigaction.2.gz 
│                │                       ├ [448] : usr/share/man/man2/sigaltstack.2.gz 
│                │                       ├ [449] : usr/share/man/man2/signal.2.gz 
│                │                       ├ [450] : usr/share/man/man2/signalfd.2.gz 
│                │                       ├ [451] : usr/share/man/man2/signalfd4.2.gz 
│                │                       ├ [452] : usr/share/man/man2/sigpending.2.gz 
│                │                       ├ [453] : usr/share/man/man2/sigprocmask.2.gz 
│                │                       ├ [454] : usr/share/man/man2/sigreturn.2.gz 
│                │                       ├ [455] : usr/share/man/man2/sigsuspend.2.gz 
│                │                       ├ [456] : usr/share/man/man2/sigtimedwait.2.gz 
│                │                       ├ [457] : usr/share/man/man2/sigwaitinfo.2.gz 
│                │                       ├ [458] : usr/share/man/man2/socket.2.gz 
│                │                       ├ [459] : usr/share/man/man2/socketcall.2.gz 
│                │                       ├ [460] : usr/share/man/man2/socketpair.2.gz 
│                │                       ├ [461] : usr/share/man/man2/splice.2.gz 
│                │                       ├ [462] : usr/share/man/man2/spu_create.2.gz 
│                │                       ├ [463] : usr/share/man/man2/spu_run.2.gz 
│                │                       ├ [464] : usr/share/man/man2/ssetmask.2.gz 
│                │                       ├ [465] : usr/share/man/man2/stat.2.gz 
│                │                       ├ [466] : usr/share/man/man2/stat64.2.gz 
│                │                       ├ [467] : usr/share/man/man2/statfs.2.gz 
│                │                       ├ [468] : usr/share/man/man2/statfs64.2.gz 
│                │                       ├ [469] : usr/share/man/man2/statmount.2.gz 
│                │                       ├ [470] : usr/share/man/man2/statx.2.gz 
│                │                       ├ [471] : usr/share/man/man2/stime.2.gz 
│                │                       ├ [472] : usr/share/man/man2/stty.2.gz 
│                │                       ├ [473] : usr/share/man/man2/subpage_prot.2.gz 
│                │                       ├ [474] : usr/share/man/man2/swapoff.2.gz 
│                │                       ├ [475] : usr/share/man/man2/swapon.2.gz 
│                │                       ├ [476] : usr/share/man/man2/symlink.2.gz 
│                │                       ├ [477] : usr/share/man/man2/symlinkat.2.gz 
│                │                       ├ [478] : usr/share/man/man2/sync.2.gz 
│                │                       ├ [479] : usr/share/man/man2/sync_file_range.2.gz 
│                │                       ├ [480] : usr/share/man/man2/sync_file_range2.2.gz 
│                │                       ├ [481] : usr/share/man/man2/syncfs.2.gz 
│                │                       ├ [482] : usr/share/man/man2/syscall.2.gz 
│                │                       ├ [483] : usr/share/man/man2/syscalls.2.gz 
│                │                       ├ [484] : usr/share/man/man2/sysctl.2.gz 
│                │                       ├ [485] : usr/share/man/man2/sysfs.2.gz 
│                │                       ├ [486] : usr/share/man/man2/sysinfo.2.gz 
│                │                       ├ [487] : usr/share/man/man2/syslog.2.gz 
│                │                       ├ [488] : usr/share/man/man2/tee.2.gz 
│                │                       ├ [489] : usr/share/man/man2/tgkill.2.gz 
│                │                       ├ [490] : usr/share/man/man2/time.2.gz 
│                │                       ├ [491] : usr/share/man/man2/timer_create.2.gz 
│                │                       ├ [492] : usr/share/man/man2/timer_delete.2.gz 
│                │                       ├ [493] : usr/share/man/man2/timer_getoverrun.2.gz 
│                │                       ├ [494] : usr/share/man/man2/timer_gettime.2.gz 
│                │                       ├ [495] : usr/share/man/man2/timer_settime.2.gz 
│                │                       ├ [496] : usr/share/man/man2/timerfd_create.2.gz 
│                │                       ├ [497] : usr/share/man/man2/timerfd_gettime.2.gz 
│                │                       ├ [498] : usr/share/man/man2/timerfd_settime.2.gz 
│                │                       ├ [499] : usr/share/man/man2/times.2.gz 
│                │                       ├ [500] : usr/share/man/man2/tkill.2.gz 
│                │                       ├ [501] : usr/share/man/man2/truncate.2.gz 
│                │                       ├ [502] : usr/share/man/man2/truncate64.2.gz 
│                │                       ├ [503] : usr/share/man/man2/tuxcall.2.gz 
│                │                       ├ [504] : usr/share/man/man2/ugetrlimit.2.gz 
│                │                       ├ [505] : usr/share/man/man2/umask.2.gz 
│                │                       ├ [506] : usr/share/man/man2/umount.2.gz 
│                │                       ├ [507] : usr/share/man/man2/umount2.2.gz 
│                │                       ├ [508] : usr/share/man/man2/uname.2.gz 
│                │                       ├ [509] : usr/share/man/man2/unimplemented.2.gz 
│                │                       ├ [510] : usr/share/man/man2/unlink.2.gz 
│                │                       ├ [511] : usr/share/man/man2/unlinkat.2.gz 
│                │                       ├ [512] : usr/share/man/man2/unshare.2.gz 
│                │                       ├ [513] : usr/share/man/man2/uretprobe.2.gz 
│                │                       ├ [514] : usr/share/man/man2/uselib.2.gz 
│                │                       ├ [515] : usr/share/man/man2/userfaultfd.2.gz 
│                │                       ├ [516] : usr/share/man/man2/ustat.2.gz 
│                │                       ├ [517] : usr/share/man/man2/utime.2.gz 
│                │                       ├ [518] : usr/share/man/man2/utimensat.2.gz 
│                │                       ├ [519] : usr/share/man/man2/utimes.2.gz 
│                │                       ├ [520] : usr/share/man/man2/vfork.2.gz 
│                │                       ├ [521] : usr/share/man/man2/vhangup.2.gz 
│                │                       ├ [522] : usr/share/man/man2/vm86.2.gz 
│                │                       ├ [523] : usr/share/man/man2/vm86old.2.gz 
│                │                       ├ [524] : usr/share/man/man2/vmsplice.2.gz 
│                │                       ├ [525] : usr/share/man/man2/vserver.2.gz 
│                │                       ├ [526] : usr/share/man/man2/wait.2.gz 
│                │                       ├ [527] : usr/share/man/man2/wait3.2.gz 
│                │                       ├ [528] : usr/share/man/man2/wait4.2.gz 
│                │                       ├ [529] : usr/share/man/man2/waitid.2.gz 
│                │                       ├ [530] : usr/share/man/man2/waitpid.2.gz 
│                │                       ├ [531] : usr/share/man/man2/write.2.gz 
│                │                       ├ [532] : usr/share/man/man2/writev.2.gz 
│                │                       ├ [533] : usr/share/man/man2const/EPIOCGPARAMS.2const.gz 
│                │                       ├ [534] : usr/share/man/man2const/EPIOCSPARAMS.2const.gz 
│                │                       ├ [535] : usr/share/man/man2const/FAT_IOCTL_GET_ATTRIBUTES.2const.gz 
│                │                       ├ [536] : usr/share/man/man2const/FAT_IOCTL_GET_VOLUME_ID.2const.gz 
│                │                       ├ [537] : usr/share/man/man2const/FAT_IOCTL_SET_ATTRIBUTES.2const.gz 
│                │                       ├ [538] : usr/share/man/man2const/FICLONE.2const.gz 
│                │                       ├ [539] : usr/share/man/man2const/FICLONERANGE.2const.gz 
│                │                       ├ [540] : usr/share/man/man2const/FIDEDUPERANGE.2const.gz 
│                │                       ├ [541] : usr/share/man/man2const/FIONREAD.2const.gz 
│                │                       ├ [542] : usr/share/man/man2const/FS_IOC_GETFLAGS.2const.gz 
│                │                       ├ [543] : usr/share/man/man2const/FS_IOC_GETFSLABEL.2const.gz 
│                │                       ├ [544] : usr/share/man/man2const/FS_IOC_GETFSMAP.2const.gz 
│                │                       ├ [545] : usr/share/man/man2const/FS_IOC_SETFLAGS.2const.gz 
│                │                       ├ [546] : usr/share/man/man2const/FS_IOC_SETFSLABEL.2const.gz 
│                │                       ├ [547] : usr/share/man/man2const/FUTEX_CMP_REQUEUE.2const.gz 
│                │                       ├ [548] : usr/share/man/man2const/FUTEX_CMP_REQUEUE_PI.2const.gz 
│                │                       ├ [549] : usr/share/man/man2const/FUTEX_FD.2const.gz 
│                │                       ├ [550] : usr/share/man/man2const/FUTEX_LOCK_PI.2const.gz 
│                │                       ├ [551] : usr/share/man/man2const/FUTEX_LOCK_PI2.2const.gz 
│                │                       ├ [552] : usr/share/man/man2const/FUTEX_REQUEUE.2const.gz 
│                │                       ├ [553] : usr/share/man/man2const/FUTEX_TRYLOCK_PI.2const.gz 
│                │                       ├ [554] : usr/share/man/man2const/FUTEX_UNLOCK_PI.2const.gz 
│                │                       ├ [555] : usr/share/man/man2const/FUTEX_WAIT.2const.gz 
│                │                       ├ [556] : usr/share/man/man2const/FUTEX_WAIT_BITSET.2const.gz 
│                │                       ├ [557] : usr/share/man/man2const/FUTEX_WAIT_REQUEUE_PI.2const.gz 
│                │                       ├ [558] : usr/share/man/man2const/FUTEX_WAKE.2const.gz 
│                │                       ├ [559] : usr/share/man/man2const/FUTEX_WAKE_BITSET.2const.gz 
│                │                       ├ [560] : usr/share/man/man2const/FUTEX_WAKE_OP.2const.gz 
│                │                       ├ [561] : usr/share/man/man2const/F_ADD_SEALS.2const.gz 
│                │                       ├ [562] : usr/share/man/man2const/F_DUPFD.2const.gz 
│                │                       ├ [563] : usr/share/man/man2const/F_DUPFD_CLOEXEC.2const.gz 
│                │                       ├ [564] : usr/share/man/man2const/F_GETFD.2const.gz 
│                │                       ├ [565] : usr/share/man/man2const/F_GETFL.2const.gz 
│                │                       ├ [566] : usr/share/man/man2const/F_GETLEASE.2const.gz 
│                │                       ├ [567] : usr/share/man/man2const/F_GETLK.2const.gz 
│                │                       ├ [568] : usr/share/man/man2const/F_GETOWN.2const.gz 
│                │                       ├ [569] : usr/share/man/man2const/F_GETOWN_EX.2const.gz 
│                │                       ├ [570] : usr/share/man/man2const/F_GETPIPE_SZ.2const.gz 
│                │                       ├ [571] : usr/share/man/man2const/F_GETSIG.2const.gz 
│                │                       ├ [572] : usr/share/man/man2const/F_GET_FILE_RW_HINT.2const.gz 
│                │                       ├ [573] : usr/share/man/man2const/F_GET_RW_HINT.2const.gz 
│                │                       ├ [574] : usr/share/man/man2const/F_GET_SEALS.2const.gz 
│                │                       ├ [575] : usr/share/man/man2const/F_NOTIFY.2const.gz 
│                │                       ├ [576] : usr/share/man/man2const/F_OFD_GETLK.2const.gz 
│                │                       ├ [577] : usr/share/man/man2const/F_OFD_SETLK.2const.gz 
│                │                       ├ [578] : usr/share/man/man2const/F_OFD_SETLKW.2const.gz 
│                │                       ├ [579] : usr/share/man/man2const/F_SETFD.2const.gz 
│                │                       ├ [580] : usr/share/man/man2const/F_SETFL.2const.gz 
│                │                       ├ [581] : usr/share/man/man2const/F_SETLEASE.2const.gz 
│                │                       ├ [582] : usr/share/man/man2const/F_SETLK.2const.gz 
│                │                       ├ [583] : usr/share/man/man2const/F_SETLKW.2const.gz 
│                │                       ├ [584] : usr/share/man/man2const/F_SETOWN.2const.gz 
│                │                       ├ [585] : usr/share/man/man2const/F_SETOWN_EX.2const.gz 
│                │                       ├ [586] : usr/share/man/man2const/F_SETPIPE_SZ.2const.gz 
│                │                       ├ [587] : usr/share/man/man2const/F_SETSIG.2const.gz 
│                │                       ├ [588] : usr/share/man/man2const/F_SET_FILE_RW_HINT.2const.gz 
│                │                       ├ [589] : usr/share/man/man2const/F_SET_RW_HINT.2const.gz 
│                │                       ├ [590] : usr/share/man/man2const/GIO_CMAP.2const.gz 
│                │                       ├ [591] : usr/share/man/man2const/GIO_FONT.2const.gz 
│                │                       ├ [592] : usr/share/man/man2const/GIO_FONTX.2const.gz 
│                │                       ├ [593] : usr/share/man/man2const/GIO_SCRNMAP.2const.gz 
│                │                       ├ [594] : usr/share/man/man2const/GIO_UNIMAP.2const.gz 
│                │                       ├ [595] : usr/share/man/man2const/GIO_UNISCRNMAP.2const.gz 
│                │                       ├ [596] : usr/share/man/man2const/KDADDIO.2const.gz 
│                │                       ├ [597] : usr/share/man/man2const/KDDELIO.2const.gz 
│                │                       ├ [598] : usr/share/man/man2const/KDDISABIO.2const.gz 
│                │                       ├ [599] : usr/share/man/man2const/KDENABIO.2const.gz 
│                │                       ├ [600] : usr/share/man/man2const/KDGETKEYCODE.2const.gz 
│                │                       ├ [601] : usr/share/man/man2const/KDGETLED.2const.gz 
│                │                       ├ [602] : usr/share/man/man2const/KDGETMODE.2const.gz 
│                │                       ├ [603] : usr/share/man/man2const/KDGKBDIACR.2const.gz 
│                │                       ├ [604] : usr/share/man/man2const/KDGKBENT.2const.gz 
│                │                       ├ [605] : usr/share/man/man2const/KDGKBLED.2const.gz 
│                │                       ├ [606] : usr/share/man/man2const/KDGKBMETA.2const.gz 
│                │                       ├ [607] : usr/share/man/man2const/KDGKBMODE.2const.gz 
│                │                       ├ [608] : usr/share/man/man2const/KDGKBSENT.2const.gz 
│                │                       ├ [609] : usr/share/man/man2const/KDGKBTYPE.2const.gz 
│                │                       ├ [610] : usr/share/man/man2const/KDMKTONE.2const.gz 
│                │                       ├ [611] : usr/share/man/man2const/KDSETKEYCODE.2const.gz 
│                │                       ├ [612] : usr/share/man/man2const/KDSETLED.2const.gz 
│                │                       ├ [613] : usr/share/man/man2const/KDSETMODE.2const.gz 
│                │                       ├ [614] : usr/share/man/man2const/KDSIGACCEPT.2const.gz 
│                │                       ├ [615] : usr/share/man/man2const/KDSKBENT.2const.gz 
│                │                       ├ [616] : usr/share/man/man2const/KDSKBLED.2const.gz 
│                │                       ├ [617] : usr/share/man/man2const/KDSKBMETA.2const.gz 
│                │                       ├ [618] : usr/share/man/man2const/KDSKBMODE.2const.gz 
│                │                       ├ [619] : usr/share/man/man2const/KDSKBSENT.2const.gz 
│                │                       ├ [620] : usr/share/man/man2const/KEYCTL_ASSUME_AUTHORITY.2const.gz 
│                │                       ├ [621] : usr/share/man/man2const/KEYCTL_CHOWN.2const.gz 
│                │                       ├ [622] : usr/share/man/man2const/KEYCTL_CLEAR.2const.gz 
│                │                       ├ [623] : usr/share/man/man2const/KEYCTL_DESCRIBE.2const.gz 
│                │                       ├ [624] : usr/share/man/man2const/KEYCTL_DH_COMPUTE.2const.gz 
│                │                       ├ [625] : usr/share/man/man2const/KEYCTL_GET_KEYRING_ID.2const.gz 
│                │                       ├ [626] : usr/share/man/man2const/KEYCTL_GET_PERSISTENT.2const.gz 
│                │                       ├ [627] : usr/share/man/man2const/KEYCTL_GET_SECURITY.2const.gz 
│                │                       ├ [628] : usr/share/man/man2const/KEYCTL_INSTANTIATE.2const.gz 
│                │                       ├ [629] : usr/share/man/man2const/KEYCTL_INSTANTIATE_IOV.2const.gz 
│                │                       ├ [630] : usr/share/man/man2const/KEYCTL_INVALIDATE.2const.gz 
│                │                       ├ [631] : usr/share/man/man2const/KEYCTL_JOIN_SESSION_KEYRING.2const.gz 
│                │                       ├ [632] : usr/share/man/man2const/KEYCTL_LINK.2const.gz 
│                │                       ├ [633] : usr/share/man/man2const/KEYCTL_NEGATE.2const.gz 
│                │                       ├ [634] : usr/share/man/man2const/KEYCTL_READ.2const.gz 
│                │                       ├ [635] : usr/share/man/man2const/KEYCTL_REJECT.2const.gz 
│                │                       ├ [636] : usr/share/man/man2const/KEYCTL_RESTRICT_KEYRING.2const.gz 
│                │                       ├ [637] : usr/share/man/man2const/KEYCTL_REVOKE.2const.gz 
│                │                       ├ [638] : usr/share/man/man2const/KEYCTL_SEARCH.2const.gz 
│                │                       ├ [639] : usr/share/man/man2const/KEYCTL_SESSION_TO_PARENT.2const.gz 
│                │                       ├ [640] : usr/share/man/man2const/KEYCTL_SETPERM.2const.gz 
│                │                       ├ [641] : usr/share/man/man2const/KEYCTL_SET_REQKEY_KEYRING.2const.gz 
│                │                       ├ [642] : usr/share/man/man2const/KEYCTL_SET_TIMEOUT.2const.gz 
│                │                       ├ [643] : usr/share/man/man2const/KEYCTL_UNLINK.2const.gz 
│                │                       ├ [644] : usr/share/man/man2const/KEYCTL_UPDATE.2const.gz 
│                │                       ├ [645] : usr/share/man/man2const/KIOCSOUND.2const.gz 
│                │                       ├ [646] : usr/share/man/man2const/NS_GET_NSTYPE.2const.gz 
│                │                       ├ [647] : usr/share/man/man2const/NS_GET_OWNER_UID.2const.gz 
│                │                       ├ [648] : usr/share/man/man2const/NS_GET_PARENT.2const.gz 
│                │                       ├ [649] : usr/share/man/man2const/NS_GET_USERNS.2const.gz 
│                │                       ├ [650] : usr/share/man/man2const/PAGEMAP_SCAN.2const.gz 
│                │                       ├ [651] : usr/share/man/man2const/PIO_CMAP.2const.gz 
│                │                       ├ [652] : usr/share/man/man2const/PIO_FONT.2const.gz 
│                │                       ├ [653] : usr/share/man/man2const/PIO_FONTRESET.2const.gz 
│                │                       ├ [654] : usr/share/man/man2const/PIO_FONTX.2const.gz 
│                │                       ├ [655] : usr/share/man/man2const/PIO_SCRNMAP.2const.gz 
│                │                       ├ [656] : usr/share/man/man2const/PIO_UNIMAP.2const.gz 
│                │                       ├ [657] : usr/share/man/man2const/PIO_UNIMAPCLR.2const.gz 
│                │                       ├ [658] : usr/share/man/man2const/PIO_UNISCRNMAP.2const.gz 
│                │                       ├ [659] : usr/share/man/man2const/PR_CAPBSET_DROP.2const.gz 
│                │                       ├ [660] : usr/share/man/man2const/PR_CAPBSET_READ.2const.gz 
│                │                       ├ [661] : usr/share/man/man2const/PR_CAP_AMBIENT.2const.gz 
│                │                       ├ [662] : usr/share/man/man2const/PR_CAP_AMBIENT_CLEAR_ALL.2const.gz 
│                │                       ├ [663] : usr/share/man/man2const/PR_CAP_AMBIENT_IS_SET.2const.gz 
│                │                       ├ [664] : usr/share/man/man2const/PR_CAP_AMBIENT_LOWER.2const.gz 
│                │                       ├ [665] : usr/share/man/man2const/PR_CAP_AMBIENT_RAISE.2const.gz 
│                │                       ├ [666] : usr/share/man/man2const/PR_FUTEX_HASH.2const.gz 
│                │                       ├ [667] : usr/share/man/man2const/PR_FUTEX_HASH_GET_SLOTS.2const.gz 
│                │                       ├ [668] : usr/share/man/man2const/PR_FUTEX_HASH_SET_SLOTS.2const.gz 
│                │                       ├ [669] : usr/share/man/man2const/PR_GET_AUXV.2const.gz 
│                │                       ├ [670] : usr/share/man/man2const/PR_GET_CHILD_SUBREAPER.2const.gz 
│                │                       ├ [671] : usr/share/man/man2const/PR_GET_DUMPABLE.2const.gz 
│                │                       ├ [672] : usr/share/man/man2const/PR_GET_ENDIAN.2const.gz 
│                │                       ├ [673] : usr/share/man/man2const/PR_GET_FPEMU.2const.gz 
│                │                       ├ [674] : usr/share/man/man2const/PR_GET_FPEXC.2const.gz 
│                │                       ├ [675] : usr/share/man/man2const/PR_GET_FP_MODE.2const.gz 
│                │                       ├ [676] : usr/share/man/man2const/PR_GET_IO_FLUSHER.2const.gz 
│                │                       ├ [677] : usr/share/man/man2const/PR_GET_KEEPCAPS.2const.gz 
│                │                       ├ [678] : usr/share/man/man2const/PR_GET_MDWE.2const.gz 
│                │                       ├ [679] : usr/share/man/man2const/PR_GET_NAME.2const.gz 
│                │                       ├ [680] : usr/share/man/man2const/PR_GET_NO_NEW_PRIVS.2const.gz 
│                │                       ├ [681] : usr/share/man/man2const/PR_GET_PDEATHSIG.2const.gz 
│                │                       ├ [682] : usr/share/man/man2const/PR_GET_SECCOMP.2const.gz 
│                │                       ├ [683] : usr/share/man/man2const/PR_GET_SECUREBITS.2const.gz 
│                │                       ├ [684] : usr/share/man/man2const/PR_GET_SPECULATION_CTRL.2const.gz 
│                │                       ├ [685] : usr/share/man/man2const/PR_GET_TAGGED_ADDR_CTRL.2const.gz 
│                │                       ├ [686] : usr/share/man/man2const/PR_GET_THP_DISABLE.2const.gz 
│                │                       ├ [687] : usr/share/man/man2const/PR_GET_TID_ADDRESS.2const.gz 
│                │                       ├ [688] : usr/share/man/man2const/PR_GET_TIMERSLACK.2const.gz 
│                │                       ├ [689] : usr/share/man/man2const/PR_GET_TIMING.2const.gz 
│                │                       ├ [690] : usr/share/man/man2const/PR_GET_TSC.2const.gz 
│                │                       ├ [691] : usr/share/man/man2const/PR_GET_UNALIGN.2const.gz 
│                │                       ├ [692] : usr/share/man/man2const/PR_MCE_KILL.2const.gz 
│                │                       ├ [693] : usr/share/man/man2const/PR_MCE_KILL_CLEAR.2const.gz 
│                │                       ├ [694] : usr/share/man/man2const/PR_MCE_KILL_GET.2const.gz 
│                │                       ├ [695] : usr/share/man/man2const/PR_MCE_KILL_SET.2const.gz 
│                │                       ├ [696] : usr/share/man/man2const/PR_MPX_DISABLE_MANAGEMENT.2const.gz 
│                │                       ├ [697] : usr/share/man/man2const/PR_MPX_ENABLE_MANAGEMENT.2const.gz 
│                │                       ├ [698] : usr/share/man/man2const/PR_PAC_RESET_KEYS.2const.gz 
│                │                       ├ [699] : usr/share/man/man2const/PR_RISCV_SET_ICACHE_FLUSH_CTX.2const
│                │                       │         .gz 
│                │                       ├ [700] : usr/share/man/man2const/PR_SET_CHILD_SUBREAPER.2const.gz 
│                │                       ├ [701] : usr/share/man/man2const/PR_SET_DUMPABLE.2const.gz 
│                │                       ├ [702] : usr/share/man/man2const/PR_SET_ENDIAN.2const.gz 
│                │                       ├ [703] : usr/share/man/man2const/PR_SET_FPEMU.2const.gz 
│                │                       ├ [704] : usr/share/man/man2const/PR_SET_FPEXC.2const.gz 
│                │                       ├ [705] : usr/share/man/man2const/PR_SET_FP_MODE.2const.gz 
│                │                       ├ [706] : usr/share/man/man2const/PR_SET_IO_FLUSHER.2const.gz 
│                │                       ├ [707] : usr/share/man/man2const/PR_SET_KEEPCAPS.2const.gz 
│                │                       ├ [708] : usr/share/man/man2const/PR_SET_MDWE.2const.gz 
│                │                       ├ [709] : usr/share/man/man2const/PR_SET_MM.2const.gz 
│                │                       ├ [710] : usr/share/man/man2const/PR_SET_MM_ARG_END.2const.gz 
│                │                       ├ [711] : usr/share/man/man2const/PR_SET_MM_ARG_START.2const.gz 
│                │                       ├ [712] : usr/share/man/man2const/PR_SET_MM_AUXV.2const.gz 
│                │                       ├ [713] : usr/share/man/man2const/PR_SET_MM_BRK.2const.gz 
│                │                       ├ [714] : usr/share/man/man2const/PR_SET_MM_END_CODE.2const.gz 
│                │                       ├ [715] : usr/share/man/man2const/PR_SET_MM_END_DATA.2const.gz 
│                │                       ├ [716] : usr/share/man/man2const/PR_SET_MM_ENV_END.2const.gz 
│                │                       ├ [717] : usr/share/man/man2const/PR_SET_MM_ENV_START.2const.gz 
│                │                       ├ [718] : usr/share/man/man2const/PR_SET_MM_EXE_FILE.2const.gz 
│                │                       ├ [719] : usr/share/man/man2const/PR_SET_MM_MAP.2const.gz 
│                │                       ├ [720] : usr/share/man/man2const/PR_SET_MM_MAP_SIZE.2const.gz 
│                │                       ├ [721] : usr/share/man/man2const/PR_SET_MM_START_BRK.2const.gz 
│                │                       ├ [722] : usr/share/man/man2const/PR_SET_MM_START_CODE.2const.gz 
│                │                       ├ [723] : usr/share/man/man2const/PR_SET_MM_START_DATA.2const.gz 
│                │                       ├ [724] : usr/share/man/man2const/PR_SET_MM_START_STACK.2const.gz 
│                │                       ├ [725] : usr/share/man/man2const/PR_SET_NAME.2const.gz 
│                │                       ├ [726] : usr/share/man/man2const/PR_SET_NO_NEW_PRIVS.2const.gz 
│                │                       ├ [727] : usr/share/man/man2const/PR_SET_PDEATHSIG.2const.gz 
│                │                       ├ [728] : usr/share/man/man2const/PR_SET_PTRACER.2const.gz 
│                │                       ├ [729] : usr/share/man/man2const/PR_SET_SECCOMP.2const.gz 
│                │                       ├ [730] : usr/share/man/man2const/PR_SET_SECUREBITS.2const.gz 
│                │                       ├ [731] : usr/share/man/man2const/PR_SET_SPECULATION_CTRL.2const.gz 
│                │                       ├ [732] : usr/share/man/man2const/PR_SET_SYSCALL_USER_DISPATCH.2const.gz 
│                │                       ├ [733] : usr/share/man/man2const/PR_SET_TAGGED_ADDR_CTRL.2const.gz 
│                │                       ├ [734] : usr/share/man/man2const/PR_SET_THP_DISABLE.2const.gz 
│                │                       ├ [735] : usr/share/man/man2const/PR_SET_TIMERSLACK.2const.gz 
│                │                       ├ [736] : usr/share/man/man2const/PR_SET_TIMING.2const.gz 
│                │                       ├ [737] : usr/share/man/man2const/PR_SET_TSC.2const.gz 
│                │                       ├ [738] : usr/share/man/man2const/PR_SET_UNALIGN.2const.gz 
│                │                       ├ [739] : usr/share/man/man2const/PR_SET_VMA.2const.gz 
│                │                       ├ [740] : usr/share/man/man2const/PR_SVE_GET_VL.2const.gz 
│                │                       ├ [741] : usr/share/man/man2const/PR_SVE_SET_VL.2const.gz 
│                │                       ├ [742] : usr/share/man/man2const/PR_TASK_PERF_EVENTS_DISABLE.2const.gz 
│                │                       ├ [743] : usr/share/man/man2const/PR_TASK_PERF_EVENTS_ENABLE.2const.gz 
│                │                       ├ [744] : usr/share/man/man2const/TCFLSH.2const.gz 
│                │                       ├ [745] : usr/share/man/man2const/TCGETA.2const.gz 
│                │                       ├ [746] : usr/share/man/man2const/TCGETS.2const.gz 
│                │                       ├ [747] : usr/share/man/man2const/TCGETS2.2const.gz 
│                │                       ├ [748] : usr/share/man/man2const/TCSBRK.2const.gz 
│                │                       ├ [749] : usr/share/man/man2const/TCSBRKP.2const.gz 
│                │                       ├ [750] : usr/share/man/man2const/TCSETA.2const.gz 
│                │                       ├ [751] : usr/share/man/man2const/TCSETAF.2const.gz 
│                │                       ├ [752] : usr/share/man/man2const/TCSETAW.2const.gz 
│                │                       ├ [753] : usr/share/man/man2const/TCSETS.2const.gz 
│                │                       ├ [754] : usr/share/man/man2const/TCSETS2.2const.gz 
│                │                       ├ [755] : usr/share/man/man2const/TCSETSF.2const.gz 
│                │                       ├ [756] : usr/share/man/man2const/TCSETSF2.2const.gz 
│                │                       ├ [757] : usr/share/man/man2const/TCSETSW.2const.gz 
│                │                       ├ [758] : usr/share/man/man2const/TCSETSW2.2const.gz 
│                │                       ├ [759] : usr/share/man/man2const/TCXONC.2const.gz 
│                │                       ├ [760] : usr/share/man/man2const/TIOCCBRK.2const.gz 
│                │                       ├ [761] : usr/share/man/man2const/TIOCCONS.2const.gz 
│                │                       ├ [762] : usr/share/man/man2const/TIOCEXCL.2const.gz 
│                │                       ├ [763] : usr/share/man/man2const/TIOCGETD.2const.gz 
│                │                       ├ [764] : usr/share/man/man2const/TIOCGEXCL.2const.gz 
│                │                       ├ [765] : usr/share/man/man2const/TIOCGICOUNT.2const.gz 
│                │                       ├ [766] : usr/share/man/man2const/TIOCGLCKTRMIOS.2const.gz 
│                │                       ├ [767] : usr/share/man/man2const/TIOCGPGRP.2const.gz 
│                │                       ├ [768] : usr/share/man/man2const/TIOCGPKT.2const.gz 
│                │                       ├ [769] : usr/share/man/man2const/TIOCGPTLCK.2const.gz 
│                │                       ├ [770] : usr/share/man/man2const/TIOCGPTPEER.2const.gz 
│                │                       ├ [771] : usr/share/man/man2const/TIOCGSID.2const.gz 
│                │                       ├ [772] : usr/share/man/man2const/TIOCGSOFTCAR.2const.gz 
│                │                       ├ [773] : usr/share/man/man2const/TIOCGWINSZ.2const.gz 
│                │                       ├ [774] : usr/share/man/man2const/TIOCINQ.2const.gz 
│                │                       ├ [775] : usr/share/man/man2const/TIOCLINUX.2const.gz 
│                │                       ├ [776] : usr/share/man/man2const/TIOCMBIC.2const.gz 
│                │                       ├ [777] : usr/share/man/man2const/TIOCMBIS.2const.gz 
│                │                       ├ [778] : usr/share/man/man2const/TIOCMGET.2const.gz 
│                │                       ├ [779] : usr/share/man/man2const/TIOCMIWAIT.2const.gz 
│                │                       ├ [780] : usr/share/man/man2const/TIOCMSET.2const.gz 
│                │                       ├ [781] : usr/share/man/man2const/TIOCNOTTY.2const.gz 
│                │                       ├ [782] : usr/share/man/man2const/TIOCNXCL.2const.gz 
│                │                       ├ [783] : usr/share/man/man2const/TIOCOUTQ.2const.gz 
│                │                       ├ [784] : usr/share/man/man2const/TIOCPKT.2const.gz 
│                │                       ├ [785] : usr/share/man/man2const/TIOCSBRK.2const.gz 
│                │                       ├ [786] : usr/share/man/man2const/TIOCSCTTY.2const.gz 
│                │                       ├ [787] : usr/share/man/man2const/TIOCSERGETLSR.2const.gz 
│                │                       ├ [788] : usr/share/man/man2const/TIOCSETD.2const.gz 
│                │                       ├ [789] : usr/share/man/man2const/TIOCSLCKTRMIOS.2const.gz 
│                │                       ├ [790] : usr/share/man/man2const/TIOCSPGRP.2const.gz 
│                │                       ├ [791] : usr/share/man/man2const/TIOCSPTLCK.2const.gz 
│                │                       ├ [792] : usr/share/man/man2const/TIOCSSOFTCAR.2const.gz 
│                │                       ├ [793] : usr/share/man/man2const/TIOCSTI.2const.gz 
│                │                       ├ [794] : usr/share/man/man2const/TIOCSWINSZ.2const.gz 
│                │                       ├ [795] : usr/share/man/man2const/TIOCTTYGSTRUCT.2const.gz 
│                │                       ├ [796] : usr/share/man/man2const/UFFDIO_API.2const.gz 
│                │                       ├ [797] : usr/share/man/man2const/UFFDIO_CONTINUE.2const.gz 
│                │                       ├ [798] : usr/share/man/man2const/UFFDIO_COPY.2const.gz 
│                │                       ├ [799] : usr/share/man/man2const/UFFDIO_MOVE.2const.gz 
│                │                       ├ [800] : usr/share/man/man2const/UFFDIO_POISON.2const.gz 
│                │                       ├ [801] : usr/share/man/man2const/UFFDIO_REGISTER.2const.gz 
│                │                       ├ [802] : usr/share/man/man2const/UFFDIO_UNREGISTER.2const.gz 
│                │                       ├ [803] : usr/share/man/man2const/UFFDIO_WAKE.2const.gz 
│                │                       ├ [804] : usr/share/man/man2const/UFFDIO_WRITEPROTECT.2const.gz 
│                │                       ├ [805] : usr/share/man/man2const/UFFDIO_ZEROPAGE.2const.gz 
│                │                       ├ [806] : usr/share/man/man2const/VFAT_IOCTL_READDIR_BOTH.2const.gz 
│                │                       ├ [807] : usr/share/man/man2const/VFAT_IOCTL_READDIR_SHORT.2const.gz 
│                │                       ├ [808] : usr/share/man/man2const/VT_ACTIVATE.2const.gz 
│                │                       ├ [809] : usr/share/man/man2const/VT_DISALLOCATE.2const.gz 
│                │                       ├ [810] : usr/share/man/man2const/VT_GETCONSIZECSRPOS.2const.gz 
│                │                       ├ [811] : usr/share/man/man2const/VT_GETMODE.2const.gz 
│                │                       ├ [812] : usr/share/man/man2const/VT_GETSTATE.2const.gz 
│                │                       ├ [813] : usr/share/man/man2const/VT_OPENQRY.2const.gz 
│                │                       ├ [814] : usr/share/man/man2const/VT_RELDISP.2const.gz 
│                │                       ├ [815] : usr/share/man/man2const/VT_RESIZE.2const.gz 
│                │                       ├ [816] : usr/share/man/man2const/VT_RESIZEX.2const.gz 
│                │                       ├ [817] : usr/share/man/man2const/VT_SETMODE.2const.gz 
│                │                       ├ [818] : usr/share/man/man2const/VT_WAITACTIVE.2const.gz 
│                │                       ├ [819] : usr/share/man/man2type/mount_attr.2type.gz 
│                │                       ├ [820] : usr/share/man/man2type/open_how.2type.gz 
│                │                       ├ [821] : usr/share/man/man3/CIRCLEQ_EMPTY.3.gz 
│                │                       ├ [822] : usr/share/man/man3/CIRCLEQ_ENTRY.3.gz 
│                │                       ├ [823] : usr/share/man/man3/CIRCLEQ_FIRST.3.gz 
│                │                       ├ [824] : usr/share/man/man3/CIRCLEQ_FOREACH.3.gz 
│                │                       ├ [825] : usr/share/man/man3/CIRCLEQ_FOREACH_REVERSE.3.gz 
│                │                       ├ [826] : usr/share/man/man3/CIRCLEQ_HEAD.3.gz 
│                │                       ├ [827] : usr/share/man/man3/CIRCLEQ_HEAD_INITIALIZER.3.gz 
│                │                       ├ [828] : usr/share/man/man3/CIRCLEQ_INIT.3.gz 
│                │                       ├ [829] : usr/share/man/man3/CIRCLEQ_INSERT_AFTER.3.gz 
│                │                       ├ [830] : usr/share/man/man3/CIRCLEQ_INSERT_BEFORE.3.gz 
│                │                       ├ [831] : usr/share/man/man3/CIRCLEQ_INSERT_HEAD.3.gz 
│                │                       ├ [832] : usr/share/man/man3/CIRCLEQ_INSERT_TAIL.3.gz 
│                │                       ├ [833] : usr/share/man/man3/CIRCLEQ_LAST.3.gz 
│                │                       ├ [834] : usr/share/man/man3/CIRCLEQ_LOOP_NEXT.3.gz 
│                │                       ├ [835] : usr/share/man/man3/CIRCLEQ_LOOP_PREV.3.gz 
│                │                       ├ [836] : usr/share/man/man3/CIRCLEQ_NEXT.3.gz 
│                │                       ├ [837] : usr/share/man/man3/CIRCLEQ_PREV.3.gz 
│                │                       ├ [838] : usr/share/man/man3/CIRCLEQ_REMOVE.3.gz 
│                │                       ├ [839] : usr/share/man/man3/CMSG_ALIGN.3.gz 
│                │                       ├ [840] : usr/share/man/man3/CMSG_DATA.3.gz 
│                │                       ├ [841] : usr/share/man/man3/CMSG_FIRSTHDR.3.gz 
│                │                       ├ [842] : usr/share/man/man3/CMSG_LEN.3.gz 
│                │                       ├ [843] : usr/share/man/man3/CMSG_NXTHDR.3.gz 
│                │                       ├ [844] : usr/share/man/man3/CMSG_SPACE.3.gz 
│                │                       ├ [845] : usr/share/man/man3/CPU_ALLOC.3.gz 
│                │                       ├ [846] : usr/share/man/man3/CPU_ALLOC_SIZE.3.gz 
│                │                       ├ [847] : usr/share/man/man3/CPU_AND.3.gz 
│                │                       ├ [848] : usr/share/man/man3/CPU_AND_S.3.gz 
│                │                       ├ [849] : usr/share/man/man3/CPU_CLR.3.gz 
│                │                       ├ [850] : usr/share/man/man3/CPU_CLR_S.3.gz 
│                │                       ├ [851] : usr/share/man/man3/CPU_COUNT.3.gz 
│                │                       ├ [852] : usr/share/man/man3/CPU_COUNT_S.3.gz 
│                │                       ├ [853] : usr/share/man/man3/CPU_EQUAL.3.gz 
│                │                       ├ [854] : usr/share/man/man3/CPU_EQUAL_S.3.gz 
│                │                       ├ [855] : usr/share/man/man3/CPU_FREE.3.gz 
│                │                       ├ [856] : usr/share/man/man3/CPU_ISSET.3.gz 
│                │                       ├ [857] : usr/share/man/man3/CPU_ISSET_S.3.gz 
│                │                       ├ [858] : usr/share/man/man3/CPU_OR.3.gz 
│                │                       ├ [859] : usr/share/man/man3/CPU_OR_S.3.gz 
│                │                       ├ [860] : usr/share/man/man3/CPU_SET.3.gz 
│                │                       ├ [861] : usr/share/man/man3/CPU_SET_S.3.gz 
│                │                       ├ [862] : usr/share/man/man3/CPU_XOR.3.gz 
│                │                       ├ [863] : usr/share/man/man3/CPU_XOR_S.3.gz 
│                │                       ├ [864] : usr/share/man/man3/CPU_ZERO.3.gz 
│                │                       ├ [865] : usr/share/man/man3/CPU_ZERO_S.3.gz 
│                │                       ├ [866] : usr/share/man/man3/DES_FAILED.3.gz 
│                │                       ├ [867] : usr/share/man/man3/FD_CLR.3.gz 
│                │                       ├ [868] : usr/share/man/man3/FD_ISSET.3.gz 
│                │                       ├ [869] : usr/share/man/man3/FD_SET.3.gz 
│                │                       ├ [870] : usr/share/man/man3/FD_ZERO.3.gz 
│                │                       ├ [871] : usr/share/man/man3/HUGE_VAL.3.gz 
│                │                       ├ [872] : usr/share/man/man3/HUGE_VALF.3.gz 
│                │                       ├ [873] : usr/share/man/man3/HUGE_VALL.3.gz 
│                │                       ├ [874] : usr/share/man/man3/INFINITY.3.gz 
│                │                       ├ [875] : usr/share/man/man3/LIST_EMPTY.3.gz 
│                │                       ├ [876] : usr/share/man/man3/LIST_ENTRY.3.gz 
│                │                       ├ [877] : usr/share/man/man3/LIST_FIRST.3.gz 
│                │                       ├ [878] : usr/share/man/man3/LIST_FOREACH.3.gz 
│                │                       ├ [879] : usr/share/man/man3/LIST_HEAD.3.gz 
│                │                       ├ [880] : usr/share/man/man3/LIST_HEAD_INITIALIZER.3.gz 
│                │                       ├ [881] : usr/share/man/man3/LIST_INIT.3.gz 
│                │                       ├ [882] : usr/share/man/man3/LIST_INSERT_AFTER.3.gz 
│                │                       ├ [883] : usr/share/man/man3/LIST_INSERT_BEFORE.3.gz 
│                │                       ├ [884] : usr/share/man/man3/LIST_INSERT_HEAD.3.gz 
│                │                       ├ [885] : usr/share/man/man3/LIST_NEXT.3.gz 
│                │                       ├ [886] : usr/share/man/man3/LIST_REMOVE.3.gz 
│                │                       ├ [887] : usr/share/man/man3/MAX.3.gz 
│                │                       ├ [888] : usr/share/man/man3/MB_CUR_MAX.3.gz 
│                │                       ├ [889] : usr/share/man/man3/MB_LEN_MAX.3.gz 
│                │                       ├ [890] : usr/share/man/man3/MIN.3.gz 
│                │                       ├ [891] : usr/share/man/man3/NAN.3.gz 
│                │                       ├ [892] : usr/share/man/man3/SIMPLEQ_EMPTY.3.gz 
│                │                       ├ [893] : usr/share/man/man3/SIMPLEQ_ENTRY.3.gz 
│                │                       ├ [894] : usr/share/man/man3/SIMPLEQ_FIRST.3.gz 
│                │                       ├ [895] : usr/share/man/man3/SIMPLEQ_FOREACH.3.gz 
│                │                       ├ [896] : usr/share/man/man3/SIMPLEQ_HEAD.3.gz 
│                │                       ├ [897] : usr/share/man/man3/SIMPLEQ_HEAD_INITIALIZER.3.gz 
│                │                       ├ [898] : usr/share/man/man3/SIMPLEQ_INIT.3.gz 
│                │                       ├ [899] : usr/share/man/man3/SIMPLEQ_INSERT_AFTER.3.gz 
│                │                       ├ [900] : usr/share/man/man3/SIMPLEQ_INSERT_HEAD.3.gz 
│                │                       ├ [901] : usr/share/man/man3/SIMPLEQ_INSERT_TAIL.3.gz 
│                │                       ├ [902] : usr/share/man/man3/SIMPLEQ_NEXT.3.gz 
│                │                       ├ [903] : usr/share/man/man3/SIMPLEQ_REMOVE.3.gz 
│                │                       ├ [904] : usr/share/man/man3/SIMPLEQ_REMOVE_HEAD.3.gz 
│                │                       ├ [905] : usr/share/man/man3/SLIST_EMPTY.3.gz 
│                │                       ├ [906] : usr/share/man/man3/SLIST_ENTRY.3.gz 
│                │                       ├ [907] : usr/share/man/man3/SLIST_FIRST.3.gz 
│                │                       ├ [908] : usr/share/man/man3/SLIST_FOREACH.3.gz 
│                │                       ├ [909] : usr/share/man/man3/SLIST_HEAD.3.gz 
│                │                       ├ [910] : usr/share/man/man3/SLIST_HEAD_INITIALIZER.3.gz 
│                │                       ├ [911] : usr/share/man/man3/SLIST_INIT.3.gz 
│                │                       ├ [912] : usr/share/man/man3/SLIST_INSERT_AFTER.3.gz 
│                │                       ├ [913] : usr/share/man/man3/SLIST_INSERT_HEAD.3.gz 
│                │                       ├ [914] : usr/share/man/man3/SLIST_NEXT.3.gz 
│                │                       ├ [915] : usr/share/man/man3/SLIST_REMOVE.3.gz 
│                │                       ├ [916] : usr/share/man/man3/SLIST_REMOVE_HEAD.3.gz 
│                │                       ├ [917] : usr/share/man/man3/STAILQ_CONCAT.3.gz 
│                │                       ├ [918] : usr/share/man/man3/STAILQ_EMPTY.3.gz 
│                │                       ├ [919] : usr/share/man/man3/STAILQ_ENTRY.3.gz 
│                │                       ├ [920] : usr/share/man/man3/STAILQ_FIRST.3.gz 
│                │                       ├ [921] : usr/share/man/man3/STAILQ_FOREACH.3.gz 
│                │                       ├ [922] : usr/share/man/man3/STAILQ_HEAD.3.gz 
│                │                       ├ [923] : usr/share/man/man3/STAILQ_HEAD_INITIALIZER.3.gz 
│                │                       ├ [924] : usr/share/man/man3/STAILQ_INIT.3.gz 
│                │                       ├ [925] : usr/share/man/man3/STAILQ_INSERT_AFTER.3.gz 
│                │                       ├ [926] : usr/share/man/man3/STAILQ_INSERT_HEAD.3.gz 
│                │                       ├ [927] : usr/share/man/man3/STAILQ_INSERT_TAIL.3.gz 
│                │                       ├ [928] : usr/share/man/man3/STAILQ_NEXT.3.gz 
│                │                       ├ [929] : usr/share/man/man3/STAILQ_REMOVE.3.gz 
│                │                       ├ [930] : usr/share/man/man3/STAILQ_REMOVE_HEAD.3.gz 
│                │                       ├ [931] : usr/share/man/man3/S_ISBLK.3.gz 
│                │                       ├ [932] : usr/share/man/man3/S_ISCHR.3.gz 
│                │                       ├ [933] : usr/share/man/man3/S_ISDIR.3.gz 
│                │                       ├ [934] : usr/share/man/man3/S_ISFIFO.3.gz 
│                │                       ├ [935] : usr/share/man/man3/S_ISLNK.3.gz 
│                │                       ├ [936] : usr/share/man/man3/S_ISREG.3.gz 
│                │                       ├ [937] : usr/share/man/man3/S_ISSOCK.3.gz 
│                │                       ├ [938] : usr/share/man/man3/TAILQ_CONCAT.3.gz 
│                │                       ├ [939] : usr/share/man/man3/TAILQ_EMPTY.3.gz 
│                │                       ├ [940] : usr/share/man/man3/TAILQ_ENTRY.3.gz 
│                │                       ├ [941] : usr/share/man/man3/TAILQ_FIRST.3.gz 
│                │                       ├ [942] : usr/share/man/man3/TAILQ_FOREACH.3.gz 
│                │                       ├ [943] : usr/share/man/man3/TAILQ_FOREACH_REVERSE.3.gz 
│                │                       ├ [944] : usr/share/man/man3/TAILQ_HEAD.3.gz 
│                │                       ├ [945] : usr/share/man/man3/TAILQ_HEAD_INITIALIZER.3.gz 
│                │                       ├ [946] : usr/share/man/man3/TAILQ_INIT.3.gz 
│                │                       ├ [947] : usr/share/man/man3/TAILQ_INSERT_AFTER.3.gz 
│                │                       ├ [948] : usr/share/man/man3/TAILQ_INSERT_BEFORE.3.gz 
│                │                       ├ [949] : usr/share/man/man3/TAILQ_INSERT_HEAD.3.gz 
│                │                       ├ [950] : usr/share/man/man3/TAILQ_INSERT_TAIL.3.gz 
│                │                       ├ [951] : usr/share/man/man3/TAILQ_LAST.3.gz 
│                │                       ├ [952] : usr/share/man/man3/TAILQ_NEXT.3.gz 
│                │                       ├ [953] : usr/share/man/man3/TAILQ_PREV.3.gz 
│                │                       ├ [954] : usr/share/man/man3/TAILQ_REMOVE.3.gz 
│                │                       ├ [955] : usr/share/man/man3/TAILQ_SWAP.3.gz 
│                │                       ├ [956] : usr/share/man/man3/TIMESPEC_TO_TIMEVAL.3.gz 
│                │                       ├ [957] : usr/share/man/man3/TIMEVAL_TO_TIMESPEC.3.gz 
│                │                       ├ [958] : usr/share/man/man3/_Fork.3.gz 
│                │                       ├ [959] : usr/share/man/man3/_Generic.3.gz 
│                │                       ├ [960] : usr/share/man/man3/_Static_assert.3.gz 
│                │                       ├ [961] : usr/share/man/man3/__after_morecore_hook.3.gz 
│                │                       ├ [962] : usr/share/man/man3/__fbufsize.3.gz 
│                │                       ├ [963] : usr/share/man/man3/__flbf.3.gz 
│                │                       ├ [964] : usr/share/man/man3/__fpending.3.gz 
│                │                       ├ [965] : usr/share/man/man3/__fpurge.3.gz 
│                │                       ├ [966] : usr/share/man/man3/__freadable.3.gz 
│                │                       ├ [967] : usr/share/man/man3/__freading.3.gz 
│                │                       ├ [968] : usr/share/man/man3/__free_hook.3.gz 
│                │                       ├ [969] : usr/share/man/man3/__fsetlocking.3.gz 
│                │                       ├ [970] : usr/share/man/man3/__fwritable.3.gz 
│                │                       ├ [971] : usr/share/man/man3/__fwriting.3.gz 
│                │                       ├ [972] : usr/share/man/man3/__malloc_hook.3.gz 
│                │                       ├ [973] : usr/share/man/man3/__malloc_initialize_hook.3.gz 
│                │                       ├ [974] : usr/share/man/man3/__memalign_hook.3.gz 
│                │                       ├ [975] : usr/share/man/man3/__ppc_get_timebase.3.gz 
│                │                       ├ [976] : usr/share/man/man3/__ppc_get_timebase_freq.3.gz 
│                │                       ├ [977] : usr/share/man/man3/__ppc_mdoio.3.gz 
│                │                       ├ [978] : usr/share/man/man3/__ppc_mdoom.3.gz 
│                │                       ├ [979] : usr/share/man/man3/__ppc_set_ppr_low.3.gz 
│                │                       ├ [980] : usr/share/man/man3/__ppc_set_ppr_med.3.gz 
│                │                       ├ [981] : usr/share/man/man3/__ppc_set_ppr_med_high.3.gz 
│                │                       ├ [982] : usr/share/man/man3/__ppc_set_ppr_med_low.3.gz 
│                │                       ├ [983] : usr/share/man/man3/__ppc_set_ppr_very_low.3.gz 
│                │                       ├ [984] : usr/share/man/man3/__ppc_yield.3.gz 
│                │                       ├ [985] : usr/share/man/man3/__realloc_hook.3.gz 
│                │                       ├ [986] : usr/share/man/man3/__riscv_flush_icache.3.gz 
│                │                       ├ [987] : usr/share/man/man3/__setfpucw.3.gz 
│                │                       ├ [988] : usr/share/man/man3/_flushlbf.3.gz 
│                │                       ├ [989] : usr/share/man/man3/a64l.3.gz 
│                │                       ├ [990] : usr/share/man/man3/abort.3.gz 
│                │                       ├ [991] : usr/share/man/man3/abs.3.gz 
│                │                       ├ [992] : usr/share/man/man3/acos.3.gz 
│                │                       ├ [993] : usr/share/man/man3/acosf.3.gz 
│                │                       ├ [994] : usr/share/man/man3/acosh.3.gz 
│                │                       ├ [995] : usr/share/man/man3/acoshf.3.gz 
│                │                       ├ [996] : usr/share/man/man3/acoshl.3.gz 
│                │                       ├ [997] : usr/share/man/man3/acosl.3.gz 
│                │                       ├ [998] : usr/share/man/man3/addmntent.3.gz 
│                │                       ├ [999] : usr/share/man/man3/addseverity.3.gz 
│                │                       ├ [1000]: usr/share/man/man3/adjtime.3.gz 
│                │                       ├ [1001]: usr/share/man/man3/aio_cancel.3.gz 
│                │                       ├ [1002]: usr/share/man/man3/aio_error.3.gz 
│                │                       ├ [1003]: usr/share/man/man3/aio_fsync.3.gz 
│                │                       ├ [1004]: usr/share/man/man3/aio_init.3.gz 
│                │                       ├ [1005]: usr/share/man/man3/aio_read.3.gz 
│                │                       ├ [1006]: usr/share/man/man3/aio_return.3.gz 
│                │                       ├ [1007]: usr/share/man/man3/aio_suspend.3.gz 
│                │                       ├ [1008]: usr/share/man/man3/aio_write.3.gz 
│                │                       ├ [1009]: usr/share/man/man3/aligned_alloc.3.gz 
│                │                       ├ [1010]: usr/share/man/man3/alloca.3.gz 
│                │                       ├ [1011]: usr/share/man/man3/alphasort.3.gz 
│                │                       ├ [1012]: usr/share/man/man3/arc4random.3.gz 
│                │                       ├ [1013]: usr/share/man/man3/arc4random_buf.3.gz 
│                │                       ├ [1014]: usr/share/man/man3/arc4random_uniform.3.gz 
│                │                       ├ [1015]: usr/share/man/man3/argz.3.gz 
│                │                       ├ [1016]: usr/share/man/man3/argz_add.3.gz 
│                │                       ├ [1017]: usr/share/man/man3/argz_add_sep.3.gz 
│                │                       ├ [1018]: usr/share/man/man3/argz_append.3.gz 
│                │                       ├ [1019]: usr/share/man/man3/argz_count.3.gz 
│                │                       ├ [1020]: usr/share/man/man3/argz_create.3.gz 
│                │                       ├ [1021]: usr/share/man/man3/argz_create_sep.3.gz 
│                │                       ├ [1022]: usr/share/man/man3/argz_delete.3.gz 
│                │                       ├ [1023]: usr/share/man/man3/argz_extract.3.gz 
│                │                       ├ [1024]: usr/share/man/man3/argz_insert.3.gz 
│                │                       ├ [1025]: usr/share/man/man3/argz_next.3.gz 
│                │                       ├ [1026]: usr/share/man/man3/argz_replace.3.gz 
│                │                       ├ [1027]: usr/share/man/man3/argz_stringify.3.gz 
│                │                       ├ [1028]: usr/share/man/man3/asctime.3.gz 
│                │                       ├ [1029]: usr/share/man/man3/asctime_r.3.gz 
│                │                       ├ [1030]: usr/share/man/man3/asin.3.gz 
│                │                       ├ [1031]: usr/share/man/man3/asinf.3.gz 
│                │                       ├ [1032]: usr/share/man/man3/asinh.3.gz 
│                │                       ├ [1033]: usr/share/man/man3/asinhf.3.gz 
│                │                       ├ [1034]: usr/share/man/man3/asinhl.3.gz 
│                │                       ├ [1035]: usr/share/man/man3/asinl.3.gz 
│                │                       ├ [1036]: usr/share/man/man3/asprintf.3.gz 
│                │                       ├ [1037]: usr/share/man/man3/assert.3.gz 
│                │                       ├ [1038]: usr/share/man/man3/assert_perror.3.gz 
│                │                       ├ [1039]: usr/share/man/man3/atan.3.gz 
│                │                       ├ [1040]: usr/share/man/man3/atan2.3.gz 
│                │                       ├ [1041]: usr/share/man/man3/atan2f.3.gz 
│                │                       ├ [1042]: usr/share/man/man3/atan2l.3.gz 
│                │                       ├ [1043]: usr/share/man/man3/atanf.3.gz 
│                │                       ├ [1044]: usr/share/man/man3/atanh.3.gz 
│                │                       ├ [1045]: usr/share/man/man3/atanhf.3.gz 
│                │                       ├ [1046]: usr/share/man/man3/atanhl.3.gz 
│                │                       ├ [1047]: usr/share/man/man3/atanl.3.gz 
│                │                       ├ [1048]: usr/share/man/man3/atexit.3.gz 
│                │                       ├ [1049]: usr/share/man/man3/atof.3.gz 
│                │                       ├ [1050]: usr/share/man/man3/atoi.3.gz 
│                │                       ├ [1051]: usr/share/man/man3/atol.3.gz 
│                │                       ├ [1052]: usr/share/man/man3/atoll.3.gz 
│                │                       ├ [1053]: usr/share/man/man3/atoq.3.gz 
│                │                       ├ [1054]: usr/share/man/man3/auth_destroy.3.gz 
│                │                       ├ [1055]: usr/share/man/man3/authnone_create.3.gz 
│                │                       ├ [1056]: usr/share/man/man3/authunix_create.3.gz 
│                │                       ├ [1057]: usr/share/man/man3/authunix_create_default.3.gz 
│                │                       ├ [1058]: usr/share/man/man3/backtrace.3.gz 
│                │                       ├ [1059]: usr/share/man/man3/backtrace_symbols.3.gz 
│                │                       ├ [1060]: usr/share/man/man3/backtrace_symbols_fd.3.gz 
│                │                       ├ [1061]: usr/share/man/man3/basename.3.gz 
│                │                       ├ [1062]: usr/share/man/man3/bcmp.3.gz 
│                │                       ├ [1063]: usr/share/man/man3/bcopy.3.gz 
│                │                       ├ [1064]: usr/share/man/man3/be16toh.3.gz 
│                │                       ├ [1065]: usr/share/man/man3/be32toh.3.gz 
│                │                       ├ [1066]: usr/share/man/man3/be64toh.3.gz 
│                │                       ├ [1067]: usr/share/man/man3/bindresvport.3.gz 
│                │                       ├ [1068]: usr/share/man/man3/bsd_signal.3.gz 
│                │                       ├ [1069]: usr/share/man/man3/bsearch.3.gz 
│                │                       ├ [1070]: usr/share/man/man3/bstring.3.gz 
│                │                       ├ [1071]: usr/share/man/man3/bswap.3.gz 
│                │                       ├ [1072]: usr/share/man/man3/bswap_16.3.gz 
│                │                       ├ [1073]: usr/share/man/man3/bswap_32.3.gz 
│                │                       ├ [1074]: usr/share/man/man3/bswap_64.3.gz 
│                │                       ├ [1075]: usr/share/man/man3/btowc.3.gz 
│                │                       ├ [1076]: usr/share/man/man3/btree.3.gz 
│                │                       ├ [1077]: usr/share/man/man3/byteorder.3.gz 
│                │                       ├ [1078]: usr/share/man/man3/bzero.3.gz 
│                │                       ├ [1079]: usr/share/man/man3/cabs.3.gz 
│                │                       ├ [1080]: usr/share/man/man3/cabsf.3.gz 
│                │                       ├ [1081]: usr/share/man/man3/cabsl.3.gz 
│                │                       ├ [1082]: usr/share/man/man3/cacos.3.gz 
│                │                       ├ [1083]: usr/share/man/man3/cacosf.3.gz 
│                │                       ├ [1084]: usr/share/man/man3/cacosh.3.gz 
│                │                       ├ [1085]: usr/share/man/man3/cacoshf.3.gz 
│                │                       ├ [1086]: usr/share/man/man3/cacoshl.3.gz 
│                │                       ├ [1087]: usr/share/man/man3/cacosl.3.gz 
│                │                       ├ [1088]: usr/share/man/man3/calloc.3.gz 
│                │                       ├ [1089]: usr/share/man/man3/callrpc.3.gz 
│                │                       ├ [1090]: usr/share/man/man3/canonicalize_file_name.3.gz 
│                │                       ├ [1091]: usr/share/man/man3/carg.3.gz 
│                │                       ├ [1092]: usr/share/man/man3/cargf.3.gz 
│                │                       ├ [1093]: usr/share/man/man3/cargl.3.gz 
│                │                       ├ [1094]: usr/share/man/man3/casin.3.gz 
│                │                       ├ [1095]: usr/share/man/man3/casinf.3.gz 
│                │                       ├ [1096]: usr/share/man/man3/casinh.3.gz 
│                │                       ├ [1097]: usr/share/man/man3/casinhf.3.gz 
│                │                       ├ [1098]: usr/share/man/man3/casinhl.3.gz 
│                │                       ├ [1099]: usr/share/man/man3/casinl.3.gz 
│                │                       ├ [1100]: usr/share/man/man3/catan.3.gz 
│                │                       ├ [1101]: usr/share/man/man3/catanf.3.gz 
│                │                       ├ [1102]: usr/share/man/man3/catanh.3.gz 
│                │                       ├ [1103]: usr/share/man/man3/catanhf.3.gz 
│                │                       ├ [1104]: usr/share/man/man3/catanhl.3.gz 
│                │                       ├ [1105]: usr/share/man/man3/catanl.3.gz 
│                │                       ├ [1106]: usr/share/man/man3/catclose.3.gz 
│                │                       ├ [1107]: usr/share/man/man3/catgets.3.gz 
│                │                       ├ [1108]: usr/share/man/man3/catopen.3.gz 
│                │                       ├ [1109]: usr/share/man/man3/cbc_crypt.3.gz 
│                │                       ├ [1110]: usr/share/man/man3/cbrt.3.gz 
│                │                       ├ [1111]: usr/share/man/man3/cbrtf.3.gz 
│                │                       ├ [1112]: usr/share/man/man3/cbrtl.3.gz 
│                │                       ├ [1113]: usr/share/man/man3/ccos.3.gz 
│                │                       ├ [1114]: usr/share/man/man3/ccosf.3.gz 
│                │                       ├ [1115]: usr/share/man/man3/ccosh.3.gz 
│                │                       ├ [1116]: usr/share/man/man3/ccoshf.3.gz 
│                │                       ├ [1117]: usr/share/man/man3/ccoshl.3.gz 
│                │                       ├ [1118]: usr/share/man/man3/ccosl.3.gz 
│                │                       ├ [1119]: usr/share/man/man3/ceil.3.gz 
│                │                       ├ [1120]: usr/share/man/man3/ceilf.3.gz 
│                │                       ├ [1121]: usr/share/man/man3/ceill.3.gz 
│                │                       ├ [1122]: usr/share/man/man3/cexp.3.gz 
│                │                       ├ [1123]: usr/share/man/man3/cexp2.3.gz 
│                │                       ├ [1124]: usr/share/man/man3/cexp2f.3.gz 
│                │                       ├ [1125]: usr/share/man/man3/cexp2l.3.gz 
│                │                       ├ [1126]: usr/share/man/man3/cexpf.3.gz 
│                │                       ├ [1127]: usr/share/man/man3/cexpl.3.gz 
│                │                       ├ [1128]: usr/share/man/man3/cfgetispeed.3.gz 
│                │                       ├ [1129]: usr/share/man/man3/cfgetospeed.3.gz 
│                │                       ├ [1130]: usr/share/man/man3/cfmakeraw.3.gz 
│                │                       ├ [1131]: usr/share/man/man3/cfree.3.gz 
│                │                       ├ [1132]: usr/share/man/man3/cfsetispeed.3.gz 
│                │                       ├ [1133]: usr/share/man/man3/cfsetospeed.3.gz 
│                │                       ├ [1134]: usr/share/man/man3/cfsetspeed.3.gz 
│                │                       ├ [1135]: usr/share/man/man3/cimag.3.gz 
│                │                       ├ [1136]: usr/share/man/man3/cimagf.3.gz 
│                │                       ├ [1137]: usr/share/man/man3/cimagl.3.gz 
│                │                       ├ [1138]: usr/share/man/man3/circleq.3.gz 
│                │                       ├ [1139]: usr/share/man/man3/clearenv.3.gz 
│                │                       ├ [1140]: usr/share/man/man3/clearerr.3.gz 
│                │                       ├ [1141]: usr/share/man/man3/clearerr_unlocked.3.gz 
│                │                       ├ [1142]: usr/share/man/man3/clnt_broadcast.3.gz 
│                │                       ├ [1143]: usr/share/man/man3/clnt_call.3.gz 
│                │                       ├ [1144]: usr/share/man/man3/clnt_control.3.gz 
│                │                       ├ [1145]: usr/share/man/man3/clnt_create.3.gz 
│                │                       ├ [1146]: usr/share/man/man3/clnt_destroy.3.gz 
│                │                       ├ [1147]: usr/share/man/man3/clnt_freeres.3.gz 
│                │                       ├ [1148]: usr/share/man/man3/clnt_geterr.3.gz 
│                │                       ├ [1149]: usr/share/man/man3/clnt_pcreateerror.3.gz 
│                │                       ├ [1150]: usr/share/man/man3/clnt_perrno.3.gz 
│                │                       ├ [1151]: usr/share/man/man3/clnt_perror.3.gz 
│                │                       ├ [1152]: usr/share/man/man3/clnt_spcreateerror.3.gz 
│                │                       ├ [1153]: usr/share/man/man3/clnt_sperrno.3.gz 
│                │                       ├ [1154]: usr/share/man/man3/clnt_sperror.3.gz 
│                │                       ├ [1155]: usr/share/man/man3/clntraw_create.3.gz 
│                │                       ├ [1156]: usr/share/man/man3/clnttcp_create.3.gz 
│                │                       ├ [1157]: usr/share/man/man3/clntudp_bufcreate.3.gz 
│                │                       ├ [1158]: usr/share/man/man3/clntudp_create.3.gz 
│                │                       ├ [1159]: usr/share/man/man3/clock.3.gz 
│                │                       ├ [1160]: usr/share/man/man3/clock_getcpuclockid.3.gz 
│                │                       ├ [1161]: usr/share/man/man3/clog.3.gz 
│                │                       ├ [1162]: usr/share/man/man3/clog10.3.gz 
│                │                       ├ [1163]: usr/share/man/man3/clog10f.3.gz 
│                │                       ├ [1164]: usr/share/man/man3/clog10l.3.gz 
│                │                       ├ [1165]: usr/share/man/man3/clog2.3.gz 
│                │                       ├ [1166]: usr/share/man/man3/clog2f.3.gz 
│                │                       ├ [1167]: usr/share/man/man3/clog2l.3.gz 
│                │                       ├ [1168]: usr/share/man/man3/clogf.3.gz 
│                │                       ├ [1169]: usr/share/man/man3/clogl.3.gz 
│                │                       ├ [1170]: usr/share/man/man3/closedir.3.gz 
│                │                       ├ [1171]: usr/share/man/man3/closelog.3.gz 
│                │                       ├ [1172]: usr/share/man/man3/cmsg.3.gz 
│                │                       ├ [1173]: usr/share/man/man3/confstr.3.gz 
│                │                       ├ [1174]: usr/share/man/man3/conj.3.gz 
│                │                       ├ [1175]: usr/share/man/man3/conjf.3.gz 
│                │                       ├ [1176]: usr/share/man/man3/conjl.3.gz 
│                │                       ├ [1177]: usr/share/man/man3/copysign.3.gz 
│                │                       ├ [1178]: usr/share/man/man3/copysignf.3.gz 
│                │                       ├ [1179]: usr/share/man/man3/copysignl.3.gz 
│                │                       ├ [1180]: usr/share/man/man3/cos.3.gz 
│                │                       ├ [1181]: usr/share/man/man3/cosf.3.gz 
│                │                       ├ [1182]: usr/share/man/man3/cosh.3.gz 
│                │                       ├ [1183]: usr/share/man/man3/coshf.3.gz 
│                │                       ├ [1184]: usr/share/man/man3/coshl.3.gz 
│                │                       ├ [1185]: usr/share/man/man3/cosl.3.gz 
│                │                       ├ [1186]: usr/share/man/man3/countof.3.gz 
│                │                       ├ [1187]: usr/share/man/man3/cpow.3.gz 
│                │                       ├ [1188]: usr/share/man/man3/cpowf.3.gz 
│                │                       ├ [1189]: usr/share/man/man3/cpowl.3.gz 
│                │                       ├ [1190]: usr/share/man/man3/cproj.3.gz 
│                │                       ├ [1191]: usr/share/man/man3/cprojf.3.gz 
│                │                       ├ [1192]: usr/share/man/man3/cprojl.3.gz 
│                │                       ├ [1193]: usr/share/man/man3/creal.3.gz 
│                │                       ├ [1194]: usr/share/man/man3/crealf.3.gz 
│                │                       ├ [1195]: usr/share/man/man3/creall.3.gz 
│                │                       ├ [1196]: usr/share/man/man3/crypt.3.gz 
│                │                       ├ [1197]: usr/share/man/man3/crypt_r.3.gz 
│                │                       ├ [1198]: usr/share/man/man3/csin.3.gz 
│                │                       ├ [1199]: usr/share/man/man3/csinf.3.gz 
│                │                       ├ [1200]: usr/share/man/man3/csinh.3.gz 
│                │                       ├ [1201]: usr/share/man/man3/csinhf.3.gz 
│                │                       ├ [1202]: usr/share/man/man3/csinhl.3.gz 
│                │                       ├ [1203]: usr/share/man/man3/csinl.3.gz 
│                │                       ├ [1204]: usr/share/man/man3/csqrt.3.gz 
│                │                       ├ [1205]: usr/share/man/man3/csqrtf.3.gz 
│                │                       ├ [1206]: usr/share/man/man3/csqrtl.3.gz 
│                │                       ├ [1207]: usr/share/man/man3/ctan.3.gz 
│                │                       ├ [1208]: usr/share/man/man3/ctanf.3.gz 
│                │                       ├ [1209]: usr/share/man/man3/ctanh.3.gz 
│                │                       ├ [1210]: usr/share/man/man3/ctanhf.3.gz 
│                │                       ├ [1211]: usr/share/man/man3/ctanhl.3.gz 
│                │                       ├ [1212]: usr/share/man/man3/ctanl.3.gz 
│                │                       ├ [1213]: usr/share/man/man3/ctermid.3.gz 
│                │                       ├ [1214]: usr/share/man/man3/ctime.3.gz 
│                │                       ├ [1215]: usr/share/man/man3/ctime_r.3.gz 
│                │                       ├ [1216]: usr/share/man/man3/cuserid.3.gz 
│                │                       ├ [1217]: usr/share/man/man3/daemon.3.gz 
│                │                       ├ [1218]: usr/share/man/man3/daylight.3.gz 
│                │                       ├ [1219]: usr/share/man/man3/db.3.gz 
│                │                       ├ [1220]: usr/share/man/man3/dbopen.3.gz 
│                │                       ├ [1221]: usr/share/man/man3/des_crypt.3.gz 
│                │                       ├ [1222]: usr/share/man/man3/des_setparity.3.gz 
│                │                       ├ [1223]: usr/share/man/man3/difftime.3.gz 
│                │                       ├ [1224]: usr/share/man/man3/dirfd.3.gz 
│                │                       ├ [1225]: usr/share/man/man3/dirname.3.gz 
│                │                       ├ [1226]: usr/share/man/man3/div.3.gz 
│                │                       ├ [1227]: usr/share/man/man3/dl_iterate_phdr.3.gz 
│                │                       ├ [1228]: usr/share/man/man3/dladdr.3.gz 
│                │                       ├ [1229]: usr/share/man/man3/dladdr1.3.gz 
│                │                       ├ [1230]: usr/share/man/man3/dlclose.3.gz 
│                │                       ├ [1231]: usr/share/man/man3/dlerror.3.gz 
│                │                       ├ [1232]: usr/share/man/man3/dlinfo.3.gz 
│                │                       ├ [1233]: usr/share/man/man3/dlmopen.3.gz 
│                │                       ├ [1234]: usr/share/man/man3/dlopen.3.gz 
│                │                       ├ [1235]: usr/share/man/man3/dlsym.3.gz 
│                │                       ├ [1236]: usr/share/man/man3/dlvsym.3.gz 
│                │                       ├ [1237]: usr/share/man/man3/dn_comp.3.gz 
│                │                       ├ [1238]: usr/share/man/man3/dn_expand.3.gz 
│                │                       ├ [1239]: usr/share/man/man3/dprintf.3.gz 
│                │                       ├ [1240]: usr/share/man/man3/drand48.3.gz 
│                │                       ├ [1241]: usr/share/man/man3/drand48_r.3.gz 
│                │                       ├ [1242]: usr/share/man/man3/drem.3.gz 
│                │                       ├ [1243]: usr/share/man/man3/dremf.3.gz 
│                │                       ├ [1244]: usr/share/man/man3/dreml.3.gz 
│                │                       ├ [1245]: usr/share/man/man3/duplocale.3.gz 
│                │                       ├ [1246]: usr/share/man/man3/dysize.3.gz 
│                │                       ├ [1247]: usr/share/man/man3/eaccess.3.gz 
│                │                       ├ [1248]: usr/share/man/man3/ecb_crypt.3.gz 
│                │                       ├ [1249]: usr/share/man/man3/ecvt.3.gz 
│                │                       ├ [1250]: usr/share/man/man3/ecvt_r.3.gz 
│                │                       ├ [1251]: usr/share/man/man3/edata.3.gz 
│                │                       ├ [1252]: usr/share/man/man3/encrypt.3.gz 
│                │                       ├ [1253]: usr/share/man/man3/encrypt_r.3.gz 
│                │                       ├ [1254]: usr/share/man/man3/end.3.gz 
│                │                       ├ [1255]: usr/share/man/man3/endaliasent.3.gz 
│                │                       ├ [1256]: usr/share/man/man3/endfsent.3.gz 
│                │                       ├ [1257]: usr/share/man/man3/endgrent.3.gz 
│                │                       ├ [1258]: usr/share/man/man3/endhostent.3.gz 
│                │                       ├ [1259]: usr/share/man/man3/endian.3.gz 
│                │                       ├ [1260]: usr/share/man/man3/endmntent.3.gz 
│                │                       ├ [1261]: usr/share/man/man3/endnetent.3.gz 
│                │                       ├ [1262]: usr/share/man/man3/endnetgrent.3.gz 
│                │                       ├ [1263]: usr/share/man/man3/endprotoent.3.gz 
│                │                       ├ [1264]: usr/share/man/man3/endpwent.3.gz 
│                │                       ├ [1265]: usr/share/man/man3/endrpcent.3.gz 
│                │                       ├ [1266]: usr/share/man/man3/endservent.3.gz 
│                │                       ├ [1267]: usr/share/man/man3/endspent.3.gz 
│                │                       ├ [1268]: usr/share/man/man3/endttyent.3.gz 
│                │                       ├ [1269]: usr/share/man/man3/endusershell.3.gz 
│                │                       ├ [1270]: usr/share/man/man3/endutent.3.gz 
│                │                       ├ [1271]: usr/share/man/man3/endutxent.3.gz 
│                │                       ├ [1272]: usr/share/man/man3/envz.3.gz 
│                │                       ├ [1273]: usr/share/man/man3/envz_add.3.gz 
│                │                       ├ [1274]: usr/share/man/man3/envz_entry.3.gz 
│                │                       ├ [1275]: usr/share/man/man3/envz_get.3.gz 
│                │                       ├ [1276]: usr/share/man/man3/envz_merge.3.gz 
│                │                       ├ [1277]: usr/share/man/man3/envz_remove.3.gz 
│                │                       ├ [1278]: usr/share/man/man3/envz_strip.3.gz 
│                │                       ├ [1279]: usr/share/man/man3/erand48.3.gz 
│                │                       ├ [1280]: usr/share/man/man3/erand48_r.3.gz 
│                │                       ├ [1281]: usr/share/man/man3/erf.3.gz 
│                │                       ├ [1282]: usr/share/man/man3/erfc.3.gz 
│                │                       ├ [1283]: usr/share/man/man3/erfcf.3.gz 
│                │                       ├ [1284]: usr/share/man/man3/erfcl.3.gz 
│                │                       ├ [1285]: usr/share/man/man3/erff.3.gz 
│                │                       ├ [1286]: usr/share/man/man3/erfl.3.gz 
│                │                       ├ [1287]: usr/share/man/man3/err.3.gz 
│                │                       ├ [1288]: usr/share/man/man3/errno.3.gz 
│                │                       ├ [1289]: usr/share/man/man3/error.3.gz 
│                │                       ├ [1290]: usr/share/man/man3/error_at_line.3.gz 
│                │                       ├ [1291]: usr/share/man/man3/error_message_count.3.gz 
│                │                       ├ [1292]: usr/share/man/man3/error_one_per_line.3.gz 
│                │                       ├ [1293]: usr/share/man/man3/error_print_progname.3.gz 
│                │                       ├ [1294]: usr/share/man/man3/errx.3.gz 
│                │                       ├ [1295]: usr/share/man/man3/etext.3.gz 
│                │                       ├ [1296]: usr/share/man/man3/ether_aton.3.gz 
│                │                       ├ [1297]: usr/share/man/man3/ether_aton_r.3.gz 
│                │                       ├ [1298]: usr/share/man/man3/ether_hostton.3.gz 
│                │                       ├ [1299]: usr/share/man/man3/ether_line.3.gz 
│                │                       ├ [1300]: usr/share/man/man3/ether_ntoa.3.gz 
│                │                       ├ [1301]: usr/share/man/man3/ether_ntoa_r.3.gz 
│                │                       ├ [1302]: usr/share/man/man3/ether_ntohost.3.gz 
│                │                       ├ [1303]: usr/share/man/man3/euidaccess.3.gz 
│                │                       ├ [1304]: usr/share/man/man3/eventfd_read.3.gz 
│                │                       ├ [1305]: usr/share/man/man3/eventfd_write.3.gz 
│                │                       ├ [1306]: usr/share/man/man3/exec.3.gz 
│                │                       ├ [1307]: usr/share/man/man3/execl.3.gz 
│                │                       ├ [1308]: usr/share/man/man3/execle.3.gz 
│                │                       ├ [1309]: usr/share/man/man3/execlp.3.gz 
│                │                       ├ [1310]: usr/share/man/man3/execv.3.gz 
│                │                       ├ [1311]: usr/share/man/man3/execvp.3.gz 
│                │                       ├ [1312]: usr/share/man/man3/execvpe.3.gz 
│                │                       ├ [1313]: usr/share/man/man3/exit.3.gz 
│                │                       ├ [1314]: usr/share/man/man3/exp.3.gz 
│                │                       ├ [1315]: usr/share/man/man3/exp10.3.gz 
│                │                       ├ [1316]: usr/share/man/man3/exp10f.3.gz 
│                │                       ├ [1317]: usr/share/man/man3/exp10l.3.gz 
│                │                       ├ [1318]: usr/share/man/man3/exp2.3.gz 
│                │                       ├ [1319]: usr/share/man/man3/exp2f.3.gz 
│                │                       ├ [1320]: usr/share/man/man3/exp2l.3.gz 
│                │                       ├ [1321]: usr/share/man/man3/expf.3.gz 
│                │                       ├ [1322]: usr/share/man/man3/expl.3.gz 
│                │                       ├ [1323]: usr/share/man/man3/explicit_bzero.3.gz 
│                │                       ├ [1324]: usr/share/man/man3/expm1.3.gz 
│                │                       ├ [1325]: usr/share/man/man3/expm1f.3.gz 
│                │                       ├ [1326]: usr/share/man/man3/expm1l.3.gz 
│                │                       ├ [1327]: usr/share/man/man3/fabs.3.gz 
│                │                       ├ [1328]: usr/share/man/man3/fabsf.3.gz 
│                │                       ├ [1329]: usr/share/man/man3/fabsl.3.gz 
│                │                       ├ [1330]: usr/share/man/man3/fclose.3.gz 
│                │                       ├ [1331]: usr/share/man/man3/fcloseall.3.gz 
│                │                       ├ [1332]: usr/share/man/man3/fcvt.3.gz 
│                │                       ├ [1333]: usr/share/man/man3/fcvt_r.3.gz 
│                │                       ├ [1334]: usr/share/man/man3/fdim.3.gz 
│                │                       ├ [1335]: usr/share/man/man3/fdimf.3.gz 
│                │                       ├ [1336]: usr/share/man/man3/fdiml.3.gz 
│                │                       ├ [1337]: usr/share/man/man3/fdopen.3.gz 
│                │                       ├ [1338]: usr/share/man/man3/fdopendir.3.gz 
│                │                       ├ [1339]: usr/share/man/man3/feclearexcept.3.gz 
│                │                       ├ [1340]: usr/share/man/man3/fedisableexcept.3.gz 
│                │                       ├ [1341]: usr/share/man/man3/feenableexcept.3.gz 
│                │                       ├ [1342]: usr/share/man/man3/fegetenv.3.gz 
│                │                       ├ [1343]: usr/share/man/man3/fegetexcept.3.gz 
│                │                       ├ [1344]: usr/share/man/man3/fegetexceptflag.3.gz 
│                │                       ├ [1345]: usr/share/man/man3/fegetround.3.gz 
│                │                       ├ [1346]: usr/share/man/man3/feholdexcept.3.gz 
│                │                       ├ [1347]: usr/share/man/man3/fenv.3.gz 
│                │                       ├ [1348]: usr/share/man/man3/feof.3.gz 
│                │                       ├ [1349]: usr/share/man/man3/feof_unlocked.3.gz 
│                │                       ├ [1350]: usr/share/man/man3/feraiseexcept.3.gz 
│                │                       ├ [1351]: usr/share/man/man3/ferror.3.gz 
│                │                       ├ [1352]: usr/share/man/man3/ferror_unlocked.3.gz 
│                │                       ├ [1353]: usr/share/man/man3/fesetenv.3.gz 
│                │                       ├ [1354]: usr/share/man/man3/fesetexceptflag.3.gz 
│                │                       ├ [1355]: usr/share/man/man3/fesetround.3.gz 
│                │                       ├ [1356]: usr/share/man/man3/fetestexcept.3.gz 
│                │                       ├ [1357]: usr/share/man/man3/feupdateenv.3.gz 
│                │                       ├ [1358]: usr/share/man/man3/fexecve.3.gz 
│                │                       ├ [1359]: usr/share/man/man3/fflush.3.gz 
│                │                       ├ [1360]: usr/share/man/man3/fflush_unlocked.3.gz 
│                │                       ├ [1361]: usr/share/man/man3/ffs.3.gz 
│                │                       ├ [1362]: usr/share/man/man3/ffsl.3.gz 
│                │                       ├ [1363]: usr/share/man/man3/ffsll.3.gz 
│                │                       ├ [1364]: usr/share/man/man3/fgetc.3.gz 
│                │                       ├ [1365]: usr/share/man/man3/fgetc_unlocked.3.gz 
│                │                       ├ [1366]: usr/share/man/man3/fgetgrent.3.gz 
│                │                       ├ [1367]: usr/share/man/man3/fgetgrent_r.3.gz 
│                │                       ├ [1368]: usr/share/man/man3/fgetpos.3.gz 
│                │                       ├ [1369]: usr/share/man/man3/fgetpwent.3.gz 
│                │                       ├ [1370]: usr/share/man/man3/fgetpwent_r.3.gz 
│                │                       ├ [1371]: usr/share/man/man3/fgets.3.gz 
│                │                       ├ [1372]: usr/share/man/man3/fgets_unlocked.3.gz 
│                │                       ├ [1373]: usr/share/man/man3/fgetspent.3.gz 
│                │                       ├ [1374]: usr/share/man/man3/fgetspent_r.3.gz 
│                │                       ├ [1375]: usr/share/man/man3/fgetwc.3.gz 
│                │                       ├ [1376]: usr/share/man/man3/fgetwc_unlocked.3.gz 
│                │                       ├ [1377]: usr/share/man/man3/fgetws.3.gz 
│                │                       ├ [1378]: usr/share/man/man3/fgetws_unlocked.3.gz 
│                │                       ├ [1379]: usr/share/man/man3/fileno.3.gz 
│                │                       ├ [1380]: usr/share/man/man3/fileno_unlocked.3.gz 
│                │                       ├ [1381]: usr/share/man/man3/finite.3.gz 
│                │                       ├ [1382]: usr/share/man/man3/finitef.3.gz 
│                │                       ├ [1383]: usr/share/man/man3/finitel.3.gz 
│                │                       ├ [1384]: usr/share/man/man3/flockfile.3.gz 
│                │                       ├ [1385]: usr/share/man/man3/floor.3.gz 
│                │                       ├ [1386]: usr/share/man/man3/floorf.3.gz 
│                │                       ├ [1387]: usr/share/man/man3/floorl.3.gz 
│                │                       ├ [1388]: usr/share/man/man3/fma.3.gz 
│                │                       ├ [1389]: usr/share/man/man3/fmaf.3.gz 
│                │                       ├ [1390]: usr/share/man/man3/fmal.3.gz 
│                │                       ├ [1391]: usr/share/man/man3/fmax.3.gz 
│                │                       ├ [1392]: usr/share/man/man3/fmaxf.3.gz 
│                │                       ├ [1393]: usr/share/man/man3/fmaxl.3.gz 
│                │                       ├ [1394]: usr/share/man/man3/fmemopen.3.gz 
│                │                       ├ [1395]: usr/share/man/man3/fmin.3.gz 
│                │                       ├ [1396]: usr/share/man/man3/fminf.3.gz 
│                │                       ├ [1397]: usr/share/man/man3/fminl.3.gz 
│                │                       ├ [1398]: usr/share/man/man3/fmod.3.gz 
│                │                       ├ [1399]: usr/share/man/man3/fmodf.3.gz 
│                │                       ├ [1400]: usr/share/man/man3/fmodl.3.gz 
│                │                       ├ [1401]: usr/share/man/man3/fmtmsg.3.gz 
│                │                       ├ [1402]: usr/share/man/man3/fnmatch.3.gz 
│                │                       ├ [1403]: usr/share/man/man3/fopen.3.gz 
│                │                       ├ [1404]: usr/share/man/man3/fopencookie.3.gz 
│                │                       ├ [1405]: usr/share/man/man3/forkpty.3.gz 
│                │                       ├ [1406]: usr/share/man/man3/fpathconf.3.gz 
│                │                       ├ [1407]: usr/share/man/man3/fpclassify.3.gz 
│                │                       ├ [1408]: usr/share/man/man3/fprintf.3.gz 
│                │                       ├ [1409]: usr/share/man/man3/fpurge.3.gz 
│                │                       ├ [1410]: usr/share/man/man3/fputc.3.gz 
│                │                       ├ [1411]: usr/share/man/man3/fputc_unlocked.3.gz 
│                │                       ├ [1412]: usr/share/man/man3/fputs.3.gz 
│                │                       ├ [1413]: usr/share/man/man3/fputs_unlocked.3.gz 
│                │                       ├ [1414]: usr/share/man/man3/fputwc.3.gz 
│                │                       ├ [1415]: usr/share/man/man3/fputwc_unlocked.3.gz 
│                │                       ├ [1416]: usr/share/man/man3/fputws.3.gz 
│                │                       ├ [1417]: usr/share/man/man3/fputws_unlocked.3.gz 
│                │                       ├ [1418]: usr/share/man/man3/fread.3.gz 
│                │                       ├ [1419]: usr/share/man/man3/fread_unlocked.3.gz 
│                │                       ├ [1420]: usr/share/man/man3/free.3.gz 
│                │                       ├ [1421]: usr/share/man/man3/freeaddrinfo.3.gz 
│                │                       ├ [1422]: usr/share/man/man3/freehostent.3.gz 
│                │                       ├ [1423]: usr/share/man/man3/freeifaddrs.3.gz 
│                │                       ├ [1424]: usr/share/man/man3/freelocale.3.gz 
│                │                       ├ [1425]: usr/share/man/man3/freopen.3.gz 
│                │                       ├ [1426]: usr/share/man/man3/frexp.3.gz 
│                │                       ├ [1427]: usr/share/man/man3/frexpf.3.gz 
│                │                       ├ [1428]: usr/share/man/man3/frexpl.3.gz 
│                │                       ├ [1429]: usr/share/man/man3/fscanf.3.gz 
│                │                       ├ [1430]: usr/share/man/man3/fseek.3.gz 
│                │                       ├ [1431]: usr/share/man/man3/fseeko.3.gz 
│                │                       ├ [1432]: usr/share/man/man3/fsetpos.3.gz 
│                │                       ├ [1433]: usr/share/man/man3/fstatvfs.3.gz 
│                │                       ├ [1434]: usr/share/man/man3/ftell.3.gz 
│                │                       ├ [1435]: usr/share/man/man3/ftello.3.gz 
│                │                       ├ [1436]: usr/share/man/man3/ftime.3.gz 
│                │                       ├ [1437]: usr/share/man/man3/ftok.3.gz 
│                │                       ├ [1438]: usr/share/man/man3/ftrylockfile.3.gz 
│                │                       ├ [1439]: usr/share/man/man3/fts.3.gz 
│                │                       ├ [1440]: usr/share/man/man3/fts_children.3.gz 
│                │                       ├ [1441]: usr/share/man/man3/fts_close.3.gz 
│                │                       ├ [1442]: usr/share/man/man3/fts_open.3.gz 
│                │                       ├ [1443]: usr/share/man/man3/fts_read.3.gz 
│                │                       ├ [1444]: usr/share/man/man3/fts_set.3.gz 
│                │                       ├ [1445]: usr/share/man/man3/ftw.3.gz 
│                │                       ├ [1446]: usr/share/man/man3/funlockfile.3.gz 
│                │                       ├ [1447]: usr/share/man/man3/futimens.3.gz 
│                │                       ├ [1448]: usr/share/man/man3/futimes.3.gz 
│                │                       ├ [1449]: usr/share/man/man3/fwide.3.gz 
│                │                       ├ [1450]: usr/share/man/man3/fwprintf.3.gz 
│                │                       ├ [1451]: usr/share/man/man3/fwrite.3.gz 
│                │                       ├ [1452]: usr/share/man/man3/fwrite_unlocked.3.gz 
│                │                       ├ [1453]: usr/share/man/man3/gai_cancel.3.gz 
│                │                       ├ [1454]: usr/share/man/man3/gai_error.3.gz 
│                │                       ├ [1455]: usr/share/man/man3/gai_strerror.3.gz 
│                │                       ├ [1456]: usr/share/man/man3/gai_suspend.3.gz 
│                │                       ├ [1457]: usr/share/man/man3/gamma.3.gz 
│                │                       ├ [1458]: usr/share/man/man3/gammaf.3.gz 
│                │                       ├ [1459]: usr/share/man/man3/gammal.3.gz 
│                │                       ├ [1460]: usr/share/man/man3/gcvt.3.gz 
│                │                       ├ [1461]: usr/share/man/man3/get_avphys_pages.3.gz 
│                │                       ├ [1462]: usr/share/man/man3/get_current_dir_name.3.gz 
│                │                       ├ [1463]: usr/share/man/man3/get_myaddress.3.gz 
│                │                       ├ [1464]: usr/share/man/man3/get_nprocs.3.gz 
│                │                       ├ [1465]: usr/share/man/man3/get_nprocs_conf.3.gz 
│                │                       ├ [1466]: usr/share/man/man3/get_phys_pages.3.gz 
│                │                       ├ [1467]: usr/share/man/man3/getaddrinfo.3.gz 
│                │                       ├ [1468]: usr/share/man/man3/getaddrinfo_a.3.gz 
│                │                       ├ [1469]: usr/share/man/man3/getaliasbyname.3.gz 
│                │                       ├ [1470]: usr/share/man/man3/getaliasbyname_r.3.gz 
│                │                       ├ [1471]: usr/share/man/man3/getaliasent.3.gz 
│                │                       ├ [1472]: usr/share/man/man3/getaliasent_r.3.gz 
│                │                       ├ [1473]: usr/share/man/man3/getauxval.3.gz 
│                │                       ├ [1474]: usr/share/man/man3/getc.3.gz 
│                │                       ├ [1475]: usr/share/man/man3/getc_unlocked.3.gz 
│                │                       ├ [1476]: usr/share/man/man3/getchar.3.gz 
│                │                       ├ [1477]: usr/share/man/man3/getchar_unlocked.3.gz 
│                │                       ├ [1478]: usr/share/man/man3/getcontext.3.gz 
│                │                       ├ [1479]: usr/share/man/man3/getcwd.3.gz 
│                │                       ├ [1480]: usr/share/man/man3/getdate.3.gz 
│                │                       ├ [1481]: usr/share/man/man3/getdate_err.3.gz 
│                │                       ├ [1482]: usr/share/man/man3/getdate_r.3.gz 
│                │                       ├ [1483]: usr/share/man/man3/getdelim.3.gz 
│                │                       ├ [1484]: usr/share/man/man3/getdirentries.3.gz 
│                │                       ├ [1485]: usr/share/man/man3/getdtablesize.3.gz 
│                │                       ├ [1486]: usr/share/man/man3/getentropy.3.gz 
│                │                       ├ [1487]: usr/share/man/man3/getenv.3.gz 
│                │                       ├ [1488]: usr/share/man/man3/getfsent.3.gz 
│                │                       ├ [1489]: usr/share/man/man3/getfsfile.3.gz 
│                │                       ├ [1490]: usr/share/man/man3/getfsspec.3.gz 
│                │                       ├ [1491]: usr/share/man/man3/getgrent.3.gz 
│                │                       ├ [1492]: usr/share/man/man3/getgrent_r.3.gz 
│                │                       ├ [1493]: usr/share/man/man3/getgrgid.3.gz 
│                │                       ├ [1494]: usr/share/man/man3/getgrgid_r.3.gz 
│                │                       ├ [1495]: usr/share/man/man3/getgrnam.3.gz 
│                │                       ├ [1496]: usr/share/man/man3/getgrnam_r.3.gz 
│                │                       ├ [1497]: usr/share/man/man3/getgrouplist.3.gz 
│                │                       ├ [1498]: usr/share/man/man3/gethostbyaddr.3.gz 
│                │                       ├ [1499]: usr/share/man/man3/gethostbyaddr_r.3.gz 
│                │                       ├ [1500]: usr/share/man/man3/gethostbyname.3.gz 
│                │                       ├ [1501]: usr/share/man/man3/gethostbyname2.3.gz 
│                │                       ├ [1502]: usr/share/man/man3/gethostbyname2_r.3.gz 
│                │                       ├ [1503]: usr/share/man/man3/gethostbyname_r.3.gz 
│                │                       ├ [1504]: usr/share/man/man3/gethostent.3.gz 
│                │                       ├ [1505]: usr/share/man/man3/gethostent_r.3.gz 
│                │                       ├ [1506]: usr/share/man/man3/gethostid.3.gz 
│                │                       ├ [1507]: usr/share/man/man3/getifaddrs.3.gz 
│                │                       ├ [1508]: usr/share/man/man3/getipnodebyaddr.3.gz 
│                │                       ├ [1509]: usr/share/man/man3/getipnodebyname.3.gz 
│                │                       ├ [1510]: usr/share/man/man3/getline.3.gz 
│                │                       ├ [1511]: usr/share/man/man3/getloadavg.3.gz 
│                │                       ├ [1512]: usr/share/man/man3/getlogin.3.gz 
│                │                       ├ [1513]: usr/share/man/man3/getlogin_r.3.gz 
│                │                       ├ [1514]: usr/share/man/man3/getmntent.3.gz 
│                │                       ├ [1515]: usr/share/man/man3/getmntent_r.3.gz 
│                │                       ├ [1516]: usr/share/man/man3/getnameinfo.3.gz 
│                │                       ├ [1517]: usr/share/man/man3/getnetbyaddr.3.gz 
│                │                       ├ [1518]: usr/share/man/man3/getnetbyaddr_r.3.gz 
│                │                       ├ [1519]: usr/share/man/man3/getnetbyname.3.gz 
│                │                       ├ [1520]: usr/share/man/man3/getnetbyname_r.3.gz 
│                │                       ├ [1521]: usr/share/man/man3/getnetent.3.gz 
│                │                       ├ [1522]: usr/share/man/man3/getnetent_r.3.gz 
│                │                       ├ [1523]: usr/share/man/man3/getnetgrent.3.gz 
│                │                       ├ [1524]: usr/share/man/man3/getnetgrent_r.3.gz 
│                │                       ├ [1525]: usr/share/man/man3/getopt.3.gz 
│                │                       ├ [1526]: usr/share/man/man3/getopt_long.3.gz 
│                │                       ├ [1527]: usr/share/man/man3/getopt_long_only.3.gz 
│                │                       ├ [1528]: usr/share/man/man3/getpass.3.gz 
│                │                       ├ [1529]: usr/share/man/man3/getprotobyname.3.gz 
│                │                       ├ [1530]: usr/share/man/man3/getprotobyname_r.3.gz 
│                │                       ├ [1531]: usr/share/man/man3/getprotobynumber.3.gz 
│                │                       ├ [1532]: usr/share/man/man3/getprotobynumber_r.3.gz 
│                │                       ├ [1533]: usr/share/man/man3/getprotoent.3.gz 
│                │                       ├ [1534]: usr/share/man/man3/getprotoent_r.3.gz 
│                │                       ├ [1535]: usr/share/man/man3/getpt.3.gz 
│                │                       ├ [1536]: usr/share/man/man3/getpw.3.gz 
│                │                       ├ [1537]: usr/share/man/man3/getpwent.3.gz 
│                │                       ├ [1538]: usr/share/man/man3/getpwent_r.3.gz 
│                │                       ├ [1539]: usr/share/man/man3/getpwnam.3.gz 
│                │                       ├ [1540]: usr/share/man/man3/getpwnam_r.3.gz 
│                │                       ├ [1541]: usr/share/man/man3/getpwuid.3.gz 
│                │                       ├ [1542]: usr/share/man/man3/getpwuid_r.3.gz 
│                │                       ├ [1543]: usr/share/man/man3/getrpcbyname.3.gz 
│                │                       ├ [1544]: usr/share/man/man3/getrpcbyname_r.3.gz 
│                │                       ├ [1545]: usr/share/man/man3/getrpcbynumber.3.gz 
│                │                       ├ [1546]: usr/share/man/man3/getrpcbynumber_r.3.gz 
│                │                       ├ [1547]: usr/share/man/man3/getrpcent.3.gz 
│                │                       ├ [1548]: usr/share/man/man3/getrpcent_r.3.gz 
│                │                       ├ [1549]: usr/share/man/man3/getrpcport.3.gz 
│                │                       ├ [1550]: usr/share/man/man3/gets.3.gz 
│                │                       ├ [1551]: usr/share/man/man3/getservbyname.3.gz 
│                │                       ├ [1552]: usr/share/man/man3/getservbyname_r.3.gz 
│                │                       ├ [1553]: usr/share/man/man3/getservbyport.3.gz 
│                │                       ├ [1554]: usr/share/man/man3/getservbyport_r.3.gz 
│                │                       ├ [1555]: usr/share/man/man3/getservent.3.gz 
│                │                       ├ [1556]: usr/share/man/man3/getservent_r.3.gz 
│                │                       ├ [1557]: usr/share/man/man3/getspent.3.gz 
│                │                       ├ [1558]: usr/share/man/man3/getspent_r.3.gz 
│                │                       ├ [1559]: usr/share/man/man3/getspnam.3.gz 
│                │                       ├ [1560]: usr/share/man/man3/getspnam_r.3.gz 
│                │                       ├ [1561]: usr/share/man/man3/getsubopt.3.gz 
│                │                       ├ [1562]: usr/share/man/man3/getttyent.3.gz 
│                │                       ├ [1563]: usr/share/man/man3/getttynam.3.gz 
│                │                       ├ [1564]: usr/share/man/man3/getusershell.3.gz 
│                │                       ├ [1565]: usr/share/man/man3/getutent.3.gz 
│                │                       ├ [1566]: usr/share/man/man3/getutent_r.3.gz 
│                │                       ├ [1567]: usr/share/man/man3/getutid.3.gz 
│                │                       ├ [1568]: usr/share/man/man3/getutid_r.3.gz 
│                │                       ├ [1569]: usr/share/man/man3/getutline.3.gz 
│                │                       ├ [1570]: usr/share/man/man3/getutline_r.3.gz 
│                │                       ├ [1571]: usr/share/man/man3/getutmp.3.gz 
│                │                       ├ [1572]: usr/share/man/man3/getutmpx.3.gz 
│                │                       ├ [1573]: usr/share/man/man3/getutxent.3.gz 
│                │                       ├ [1574]: usr/share/man/man3/getutxid.3.gz 
│                │                       ├ [1575]: usr/share/man/man3/getutxline.3.gz 
│                │                       ├ [1576]: usr/share/man/man3/getw.3.gz 
│                │                       ├ [1577]: usr/share/man/man3/getwc.3.gz 
│                │                       ├ [1578]: usr/share/man/man3/getwc_unlocked.3.gz 
│                │                       ├ [1579]: usr/share/man/man3/getwchar.3.gz 
│                │                       ├ [1580]: usr/share/man/man3/getwchar_unlocked.3.gz 
│                │                       ├ [1581]: usr/share/man/man3/getwd.3.gz 
│                │                       ├ [1582]: usr/share/man/man3/glob.3.gz 
│                │                       ├ [1583]: usr/share/man/man3/globfree.3.gz 
│                │                       ├ [1584]: usr/share/man/man3/gmtime.3.gz 
│                │                       ├ [1585]: usr/share/man/man3/gmtime_r.3.gz 
│                │                       ├ [1586]: usr/share/man/man3/gnu_dev_major.3.gz 
│                │                       ├ [1587]: usr/share/man/man3/gnu_dev_makedev.3.gz 
│                │                       ├ [1588]: usr/share/man/man3/gnu_dev_minor.3.gz 
│                │                       ├ [1589]: usr/share/man/man3/gnu_get_libc_release.3.gz 
│                │                       ├ [1590]: usr/share/man/man3/gnu_get_libc_version.3.gz 
│                │                       ├ [1591]: usr/share/man/man3/grantpt.3.gz 
│                │                       ├ [1592]: usr/share/man/man3/group_member.3.gz 
│                │                       ├ [1593]: usr/share/man/man3/gsignal.3.gz 
│                │                       ├ [1594]: usr/share/man/man3/h_errno.3.gz 
│                │                       ├ [1595]: usr/share/man/man3/hash.3.gz 
│                │                       ├ [1596]: usr/share/man/man3/hasmntopt.3.gz 
│                │                       ├ [1597]: usr/share/man/man3/hcreate.3.gz 
│                │                       ├ [1598]: usr/share/man/man3/hcreate_r.3.gz 
│                │                       ├ [1599]: usr/share/man/man3/hdestroy.3.gz 
│                │                       ├ [1600]: usr/share/man/man3/hdestroy_r.3.gz 
│                │                       ├ [1601]: usr/share/man/man3/herror.3.gz 
│                │                       ├ [1602]: usr/share/man/man3/hsearch.3.gz 
│                │                       ├ [1603]: usr/share/man/man3/hsearch_r.3.gz 
│                │                       ├ [1604]: usr/share/man/man3/hstrerror.3.gz 
│                │                       ├ [1605]: usr/share/man/man3/htobe16.3.gz 
│                │                       ├ [1606]: usr/share/man/man3/htobe32.3.gz 
│                │                       ├ [1607]: usr/share/man/man3/htobe64.3.gz 
│                │                       ├ [1608]: usr/share/man/man3/htole16.3.gz 
│                │                       ├ [1609]: usr/share/man/man3/htole32.3.gz 
│                │                       ├ [1610]: usr/share/man/man3/htole64.3.gz 
│                │                       ├ [1611]: usr/share/man/man3/htonl.3.gz 
│                │                       ├ [1612]: usr/share/man/man3/htons.3.gz 
│                │                       ├ [1613]: usr/share/man/man3/hypot.3.gz 
│                │                       ├ [1614]: usr/share/man/man3/hypotf.3.gz 
│                │                       ├ [1615]: usr/share/man/man3/hypotl.3.gz 
│                │                       ├ [1616]: usr/share/man/man3/if_freenameindex.3.gz 
│                │                       ├ [1617]: usr/share/man/man3/if_indextoname.3.gz 
│                │                       ├ [1618]: usr/share/man/man3/if_nameindex.3.gz 
│                │                       ├ [1619]: usr/share/man/man3/if_nametoindex.3.gz 
│                │                       ├ [1620]: usr/share/man/man3/ilogb.3.gz 
│                │                       ├ [1621]: usr/share/man/man3/ilogbf.3.gz 
│                │                       ├ [1622]: usr/share/man/man3/ilogbl.3.gz 
│                │                       ├ [1623]: usr/share/man/man3/imaxabs.3.gz 
│                │                       ├ [1624]: usr/share/man/man3/imaxdiv.3.gz 
│                │                       ├ [1625]: usr/share/man/man3/index.3.gz 
│                │                       ├ [1626]: usr/share/man/man3/inet.3.gz 
│                │                       ├ [1627]: usr/share/man/man3/inet_addr.3.gz 
│                │                       ├ [1628]: usr/share/man/man3/inet_aton.3.gz 
│                │                       ├ [1629]: usr/share/man/man3/inet_lnaof.3.gz 
│                │                       ├ [1630]: usr/share/man/man3/inet_makeaddr.3.gz 
│                │                       ├ [1631]: usr/share/man/man3/inet_net_ntop.3.gz 
│                │                       ├ [1632]: usr/share/man/man3/inet_net_pton.3.gz 
│                │                       ├ [1633]: usr/share/man/man3/inet_netof.3.gz 
│                │                       ├ [1634]: usr/share/man/man3/inet_network.3.gz 
│                │                       ├ [1635]: usr/share/man/man3/inet_ntoa.3.gz 
│                │                       ├ [1636]: usr/share/man/man3/inet_ntop.3.gz 
│                │                       ├ [1637]: usr/share/man/man3/inet_pton.3.gz 
│                │                       ├ [1638]: usr/share/man/man3/initgroups.3.gz 
│                │                       ├ [1639]: usr/share/man/man3/initstate.3.gz 
│                │                       ├ [1640]: usr/share/man/man3/initstate_r.3.gz 
│                │                       ├ [1641]: usr/share/man/man3/innetgr.3.gz 
│                │                       ├ [1642]: usr/share/man/man3/insque.3.gz 
│                │                       ├ [1643]: usr/share/man/man3/intro.3.gz 
│                │                       ├ [1644]: usr/share/man/man3/iruserok.3.gz 
│                │                       ├ [1645]: usr/share/man/man3/iruserok_af.3.gz 
│                │                       ├ [1646]: usr/share/man/man3/isalnum.3.gz 
│                │                       ├ [1647]: usr/share/man/man3/isalnum_l.3.gz 
│                │                       ├ [1648]: usr/share/man/man3/isalpha.3.gz 
│                │                       ├ [1649]: usr/share/man/man3/isalpha_l.3.gz 
│                │                       ├ [1650]: usr/share/man/man3/isascii.3.gz 
│                │                       ├ [1651]: usr/share/man/man3/isascii_l.3.gz 
│                │                       ├ [1652]: usr/share/man/man3/isatty.3.gz 
│                │                       ├ [1653]: usr/share/man/man3/isblank.3.gz 
│                │                       ├ [1654]: usr/share/man/man3/isblank_l.3.gz 
│                │                       ├ [1655]: usr/share/man/man3/iscntrl.3.gz 
│                │                       ├ [1656]: usr/share/man/man3/iscntrl_l.3.gz 
│                │                       ├ [1657]: usr/share/man/man3/isdigit.3.gz 
│                │                       ├ [1658]: usr/share/man/man3/isdigit_l.3.gz 
│                │                       ├ [1659]: usr/share/man/man3/isfdtype.3.gz 
│                │                       ├ [1660]: usr/share/man/man3/isfinite.3.gz 
│                │                       ├ [1661]: usr/share/man/man3/isgraph.3.gz 
│                │                       ├ [1662]: usr/share/man/man3/isgraph_l.3.gz 
│                │                       ├ [1663]: usr/share/man/man3/isgreater.3.gz 
│                │                       ├ [1664]: usr/share/man/man3/isgreaterequal.3.gz 
│                │                       ├ [1665]: usr/share/man/man3/isinf.3.gz 
│                │                       ├ [1666]: usr/share/man/man3/isinff.3.gz 
│                │                       ├ [1667]: usr/share/man/man3/isinfl.3.gz 
│                │                       ├ [1668]: usr/share/man/man3/isless.3.gz 
│                │                       ├ [1669]: usr/share/man/man3/islessequal.3.gz 
│                │                       ├ [1670]: usr/share/man/man3/islessgreater.3.gz 
│                │                       ├ [1671]: usr/share/man/man3/islower.3.gz 
│                │                       ├ [1672]: usr/share/man/man3/islower_l.3.gz 
│                │                       ├ [1673]: usr/share/man/man3/isnan.3.gz 
│                │                       ├ [1674]: usr/share/man/man3/isnanf.3.gz 
│                │                       ├ [1675]: usr/share/man/man3/isnanl.3.gz 
│                │                       ├ [1676]: usr/share/man/man3/isnormal.3.gz 
│                │                       ├ [1677]: usr/share/man/man3/isprint.3.gz 
│                │                       ├ [1678]: usr/share/man/man3/isprint_l.3.gz 
│                │                       ├ [1679]: usr/share/man/man3/ispunct.3.gz 
│                │                       ├ [1680]: usr/share/man/man3/ispunct_l.3.gz 
│                │                       ├ [1681]: usr/share/man/man3/isspace.3.gz 
│                │                       ├ [1682]: usr/share/man/man3/isspace_l.3.gz 
│                │                       ├ [1683]: usr/share/man/man3/isunordered.3.gz 
│                │                       ├ [1684]: usr/share/man/man3/isupper.3.gz 
│                │                       ├ [1685]: usr/share/man/man3/isupper_l.3.gz 
│                │                       ├ [1686]: usr/share/man/man3/iswalnum.3.gz 
│                │                       ├ [1687]: usr/share/man/man3/iswalpha.3.gz 
│                │                       ├ [1688]: usr/share/man/man3/iswblank.3.gz 
│                │                       ├ [1689]: usr/share/man/man3/iswcntrl.3.gz 
│                │                       ├ [1690]: usr/share/man/man3/iswctype.3.gz 
│                │                       ├ [1691]: usr/share/man/man3/iswdigit.3.gz 
│                │                       ├ [1692]: usr/share/man/man3/iswgraph.3.gz 
│                │                       ├ [1693]: usr/share/man/man3/iswlower.3.gz 
│                │                       ├ [1694]: usr/share/man/man3/iswprint.3.gz 
│                │                       ├ [1695]: usr/share/man/man3/iswpunct.3.gz 
│                │                       ├ [1696]: usr/share/man/man3/iswspace.3.gz 
│                │                       ├ [1697]: usr/share/man/man3/iswupper.3.gz 
│                │                       ├ [1698]: usr/share/man/man3/iswxdigit.3.gz 
│                │                       ├ [1699]: usr/share/man/man3/isxdigit.3.gz 
│                │                       ├ [1700]: usr/share/man/man3/isxdigit_l.3.gz 
│                │                       ├ [1701]: usr/share/man/man3/j0.3.gz 
│                │                       ├ [1702]: usr/share/man/man3/j0f.3.gz 
│                │                       ├ [1703]: usr/share/man/man3/j0l.3.gz 
│                │                       ├ [1704]: usr/share/man/man3/j1.3.gz 
│                │                       ├ [1705]: usr/share/man/man3/j1f.3.gz 
│                │                       ├ [1706]: usr/share/man/man3/j1l.3.gz 
│                │                       ├ [1707]: usr/share/man/man3/jn.3.gz 
│                │                       ├ [1708]: usr/share/man/man3/jnf.3.gz 
│                │                       ├ [1709]: usr/share/man/man3/jnl.3.gz 
│                │                       ├ [1710]: usr/share/man/man3/jrand48.3.gz 
│                │                       ├ [1711]: usr/share/man/man3/jrand48_r.3.gz 
│                │                       ├ [1712]: usr/share/man/man3/key_decryptsession.3.gz 
│                │                       ├ [1713]: usr/share/man/man3/key_encryptsession.3.gz 
│                │                       ├ [1714]: usr/share/man/man3/key_gendes.3.gz 
│                │                       ├ [1715]: usr/share/man/man3/key_secretkey_is_set.3.gz 
│                │                       ├ [1716]: usr/share/man/man3/key_setsecret.3.gz 
│                │                       ├ [1717]: usr/share/man/man3/killpg.3.gz 
│                │                       ├ [1718]: usr/share/man/man3/klogctl.3.gz 
│                │                       ├ [1719]: usr/share/man/man3/l64a.3.gz 
│                │                       ├ [1720]: usr/share/man/man3/labs.3.gz 
│                │                       ├ [1721]: usr/share/man/man3/lckpwdf.3.gz 
│                │                       ├ [1722]: usr/share/man/man3/lcong48.3.gz 
│                │                       ├ [1723]: usr/share/man/man3/lcong48_r.3.gz 
│                │                       ├ [1724]: usr/share/man/man3/ldexp.3.gz 
│                │                       ├ [1725]: usr/share/man/man3/ldexpf.3.gz 
│                │                       ├ [1726]: usr/share/man/man3/ldexpl.3.gz 
│                │                       ├ [1727]: usr/share/man/man3/ldiv.3.gz 
│                │                       ├ [1728]: usr/share/man/man3/le16toh.3.gz 
│                │                       ├ [1729]: usr/share/man/man3/le32toh.3.gz 
│                │                       ├ [1730]: usr/share/man/man3/le64toh.3.gz 
│                │                       ├ [1731]: usr/share/man/man3/lfind.3.gz 
│                │                       ├ [1732]: usr/share/man/man3/lgamma.3.gz 
│                │                       ├ [1733]: usr/share/man/man3/lgamma_r.3.gz 
│                │                       ├ [1734]: usr/share/man/man3/lgammaf.3.gz 
│                │                       ├ [1735]: usr/share/man/man3/lgammaf_r.3.gz 
│                │                       ├ [1736]: usr/share/man/man3/lgammal.3.gz 
│                │                       ├ [1737]: usr/share/man/man3/lgammal_r.3.gz 
│                │                       ├ [1738]: usr/share/man/man3/lio_listio.3.gz 
│                │                       ├ [1739]: usr/share/man/man3/list.3.gz 
│                │                       ├ [1740]: usr/share/man/man3/llabs.3.gz 
│                │                       ├ [1741]: usr/share/man/man3/lldiv.3.gz 
│                │                       ├ [1742]: usr/share/man/man3/llrint.3.gz 
│                │                       ├ [1743]: usr/share/man/man3/llrintf.3.gz 
│                │                       ├ [1744]: usr/share/man/man3/llrintl.3.gz 
│                │                       ├ [1745]: usr/share/man/man3/llround.3.gz 
│                │                       ├ [1746]: usr/share/man/man3/llroundf.3.gz 
│                │                       ├ [1747]: usr/share/man/man3/llroundl.3.gz 
│                │                       ├ [1748]: usr/share/man/man3/localeconv.3.gz 
│                │                       ├ [1749]: usr/share/man/man3/localtime.3.gz 
│                │                       ├ [1750]: usr/share/man/man3/localtime_r.3.gz 
│                │                       ├ [1751]: usr/share/man/man3/lockf.3.gz 
│                │                       ├ [1752]: usr/share/man/man3/log.3.gz 
│                │                       ├ [1753]: usr/share/man/man3/log10.3.gz 
│                │                       ├ [1754]: usr/share/man/man3/log10f.3.gz 
│                │                       ├ [1755]: usr/share/man/man3/log10l.3.gz 
│                │                       ├ [1756]: usr/share/man/man3/log1p.3.gz 
│                │                       ├ [1757]: usr/share/man/man3/log1pf.3.gz 
│                │                       ├ [1758]: usr/share/man/man3/log1pl.3.gz 
│                │                       ├ [1759]: usr/share/man/man3/log2.3.gz 
│                │                       ├ [1760]: usr/share/man/man3/log2f.3.gz 
│                │                       ├ [1761]: usr/share/man/man3/log2l.3.gz 
│                │                       ├ [1762]: usr/share/man/man3/logb.3.gz 
│                │                       ├ [1763]: usr/share/man/man3/logbf.3.gz 
│                │                       ├ [1764]: usr/share/man/man3/logbl.3.gz 
│                │                       ├ [1765]: usr/share/man/man3/logf.3.gz 
│                │                       ├ [1766]: usr/share/man/man3/login.3.gz 
│                │                       ├ [1767]: usr/share/man/man3/login_tty.3.gz 
│                │                       ├ [1768]: usr/share/man/man3/logl.3.gz 
│                │                       ├ [1769]: usr/share/man/man3/logout.3.gz 
│                │                       ├ [1770]: usr/share/man/man3/logwtmp.3.gz 
│                │                       ├ [1771]: usr/share/man/man3/longjmp.3.gz 
│                │                       ├ [1772]: usr/share/man/man3/lrand48.3.gz 
│                │                       ├ [1773]: usr/share/man/man3/lrand48_r.3.gz 
│                │                       ├ [1774]: usr/share/man/man3/lrint.3.gz 
│                │                       ├ [1775]: usr/share/man/man3/lrintf.3.gz 
│                │                       ├ [1776]: usr/share/man/man3/lrintl.3.gz 
│                │                       ├ [1777]: usr/share/man/man3/lround.3.gz 
│                │                       ├ [1778]: usr/share/man/man3/lroundf.3.gz 
│                │                       ├ [1779]: usr/share/man/man3/lroundl.3.gz 
│                │                       ├ [1780]: usr/share/man/man3/lsearch.3.gz 
│                │                       ├ [1781]: usr/share/man/man3/lseek64.3.gz 
│                │                       ├ [1782]: usr/share/man/man3/lutimes.3.gz 
│                │                       ├ [1783]: usr/share/man/man3/major.3.gz 
│                │                       ├ [1784]: usr/share/man/man3/makecontext.3.gz 
│                │                       ├ [1785]: usr/share/man/man3/makedev.3.gz 
│                │                       ├ [1786]: usr/share/man/man3/mallinfo.3.gz 
│                │                       ├ [1787]: usr/share/man/man3/mallinfo2.3.gz 
│                │                       ├ [1788]: usr/share/man/man3/malloc.3.gz 
│                │                       ├ [1789]: usr/share/man/man3/malloc_get_state.3.gz 
│                │                       ├ [1790]: usr/share/man/man3/malloc_hook.3.gz 
│                │                       ├ [1791]: usr/share/man/man3/malloc_info.3.gz 
│                │                       ├ [1792]: usr/share/man/man3/malloc_set_state.3.gz 
│                │                       ├ [1793]: usr/share/man/man3/malloc_stats.3.gz 
│                │                       ├ [1794]: usr/share/man/man3/malloc_trim.3.gz 
│                │                       ├ [1795]: usr/share/man/man3/malloc_usable_size.3.gz 
│                │                       ├ [1796]: usr/share/man/man3/mallopt.3.gz 
│                │                       ├ [1797]: usr/share/man/man3/matherr.3.gz 
│                │                       ├ [1798]: usr/share/man/man3/mblen.3.gz 
│                │                       ├ [1799]: usr/share/man/man3/mbrlen.3.gz 
│                │                       ├ [1800]: usr/share/man/man3/mbrtowc.3.gz 
│                │                       ├ [1801]: usr/share/man/man3/mbsinit.3.gz 
│                │                       ├ [1802]: usr/share/man/man3/mbsnrtowcs.3.gz 
│                │                       ├ [1803]: usr/share/man/man3/mbsrtowcs.3.gz 
│                │                       ├ [1804]: usr/share/man/man3/mbstowcs.3.gz 
│                │                       ├ [1805]: usr/share/man/man3/mbtowc.3.gz 
│                │                       ├ [1806]: usr/share/man/man3/mcheck.3.gz 
│                │                       ├ [1807]: usr/share/man/man3/mcheck_check_all.3.gz 
│                │                       ├ [1808]: usr/share/man/man3/mcheck_pedantic.3.gz 
│                │                       ├ [1809]: usr/share/man/man3/memalign.3.gz 
│                │                       ├ [1810]: usr/share/man/man3/memccpy.3.gz 
│                │                       ├ [1811]: usr/share/man/man3/memchr.3.gz 
│                │                       ├ [1812]: usr/share/man/man3/memcmp.3.gz 
│                │                       ├ [1813]: usr/share/man/man3/memcpy.3.gz 
│                │                       ├ [1814]: usr/share/man/man3/memeq.3.gz 
│                │                       ├ [1815]: usr/share/man/man3/memfrob.3.gz 
│                │                       ├ [1816]: usr/share/man/man3/memmem.3.gz 
│                │                       ├ [1817]: usr/share/man/man3/memmove.3.gz 
│                │                       ├ [1818]: usr/share/man/man3/mempcpy.3.gz 
│                │                       ├ [1819]: usr/share/man/man3/memrchr.3.gz 
│                │                       ├ [1820]: usr/share/man/man3/memset.3.gz 
│                │                       ├ [1821]: usr/share/man/man3/minor.3.gz 
│                │                       ├ [1822]: usr/share/man/man3/mkdtemp.3.gz 
│                │                       ├ [1823]: usr/share/man/man3/mkfifo.3.gz 
│                │                       ├ [1824]: usr/share/man/man3/mkfifoat.3.gz 
│                │                       ├ [1825]: usr/share/man/man3/mkostemp.3.gz 
│                │                       ├ [1826]: usr/share/man/man3/mkostemps.3.gz 
│                │                       ├ [1827]: usr/share/man/man3/mkstemp.3.gz 
│                │                       ├ [1828]: usr/share/man/man3/mkstemps.3.gz 
│                │                       ├ [1829]: usr/share/man/man3/mktemp.3.gz 
│                │                       ├ [1830]: usr/share/man/man3/mktime.3.gz 
│                │                       ├ [1831]: usr/share/man/man3/mmap64.3.gz 
│                │                       ├ [1832]: usr/share/man/man3/modf.3.gz 
│                │                       ├ [1833]: usr/share/man/man3/modff.3.gz 
│                │                       ├ [1834]: usr/share/man/man3/modfl.3.gz 
│                │                       ├ [1835]: usr/share/man/man3/mpool.3.gz 
│                │                       ├ [1836]: usr/share/man/man3/mprobe.3.gz 
│                │                       ├ [1837]: usr/share/man/man3/mq_close.3.gz 
│                │                       ├ [1838]: usr/share/man/man3/mq_getattr.3.gz 
│                │                       ├ [1839]: usr/share/man/man3/mq_notify.3.gz 
│                │                       ├ [1840]: usr/share/man/man3/mq_open.3.gz 
│                │                       ├ [1841]: usr/share/man/man3/mq_receive.3.gz 
│                │                       ├ [1842]: usr/share/man/man3/mq_send.3.gz 
│                │                       ├ [1843]: usr/share/man/man3/mq_setattr.3.gz 
│                │                       ├ [1844]: usr/share/man/man3/mq_timedreceive.3.gz 
│                │                       ├ [1845]: usr/share/man/man3/mq_timedsend.3.gz 
│                │                       ├ [1846]: usr/share/man/man3/mq_unlink.3.gz 
│                │                       ├ [1847]: usr/share/man/man3/mrand48.3.gz 
│                │                       ├ [1848]: usr/share/man/man3/mrand48_r.3.gz 
│                │                       ├ [1849]: usr/share/man/man3/mtrace.3.gz 
│                │                       ├ [1850]: usr/share/man/man3/muntrace.3.gz 
│                │                       ├ [1851]: usr/share/man/man3/nan.3.gz 
│                │                       ├ [1852]: usr/share/man/man3/nanf.3.gz 
│                │                       ├ [1853]: usr/share/man/man3/nanl.3.gz 
│                │                       ├ [1854]: usr/share/man/man3/nearbyint.3.gz 
│                │                       ├ [1855]: usr/share/man/man3/nearbyintf.3.gz 
│                │                       ├ [1856]: usr/share/man/man3/nearbyintl.3.gz 
│                │                       ├ [1857]: usr/share/man/man3/netlink.3.gz 
│                │                       ├ [1858]: usr/share/man/man3/newlocale.3.gz 
│                │                       ├ [1859]: usr/share/man/man3/nextafter.3.gz 
│                │                       ├ [1860]: usr/share/man/man3/nextafterf.3.gz 
│                │                       ├ [1861]: usr/share/man/man3/nextafterl.3.gz 
│                │                       ├ [1862]: usr/share/man/man3/nextdown.3.gz 
│                │                       ├ [1863]: usr/share/man/man3/nextdownf.3.gz 
│                │                       ├ [1864]: usr/share/man/man3/nextdownl.3.gz 
│                │                       ├ [1865]: usr/share/man/man3/nexttoward.3.gz 
│                │                       ├ [1866]: usr/share/man/man3/nexttowardf.3.gz 
│                │                       ├ [1867]: usr/share/man/man3/nexttowardl.3.gz 
│                │                       ├ [1868]: usr/share/man/man3/nextup.3.gz 
│                │                       ├ [1869]: usr/share/man/man3/nextupf.3.gz 
│                │                       ├ [1870]: usr/share/man/man3/nextupl.3.gz 
│                │                       ├ [1871]: usr/share/man/man3/nftw.3.gz 
│                │                       ├ [1872]: usr/share/man/man3/nl_langinfo.3.gz 
│                │                       ├ [1873]: usr/share/man/man3/nl_langinfo_l.3.gz 
│                │                       ├ [1874]: usr/share/man/man3/nrand48.3.gz 
│                │                       ├ [1875]: usr/share/man/man3/nrand48_r.3.gz 
│                │                       ├ [1876]: usr/share/man/man3/ntohl.3.gz 
│                │                       ├ [1877]: usr/share/man/man3/ntohs.3.gz 
│                │                       ├ [1878]: usr/share/man/man3/ntp_adjtime.3.gz 
│                │                       ├ [1879]: usr/share/man/man3/ntp_gettime.3.gz 
│                │                       ├ [1880]: usr/share/man/man3/ntp_gettimex.3.gz 
│                │                       ├ [1881]: usr/share/man/man3/offsetof.3.gz 
│                │                       ├ [1882]: usr/share/man/man3/on_exit.3.gz 
│                │                       ├ [1883]: usr/share/man/man3/open_memstream.3.gz 
│                │                       ├ [1884]: usr/share/man/man3/open_wmemstream.3.gz 
│                │                       ├ [1885]: usr/share/man/man3/opendir.3.gz 
│                │                       ├ [1886]: usr/share/man/man3/openlog.3.gz 
│                │                       ├ [1887]: usr/share/man/man3/openpty.3.gz 
│                │                       ├ [1888]: usr/share/man/man3/optarg.3.gz 
│                │                       ├ [1889]: usr/share/man/man3/opterr.3.gz 
│                │                       ├ [1890]: usr/share/man/man3/optind.3.gz 
│                │                       ├ [1891]: usr/share/man/man3/optopt.3.gz 
│                │                       ├ [1892]: usr/share/man/man3/passwd2des.3.gz 
│                │                       ├ [1893]: usr/share/man/man3/pathconf.3.gz 
│                │                       ├ [1894]: usr/share/man/man3/pclose.3.gz 
│                │                       ├ [1895]: usr/share/man/man3/perror.3.gz 
│                │                       ├ [1896]: usr/share/man/man3/pmap_getmaps.3.gz 
│                │                       ├ [1897]: usr/share/man/man3/pmap_getport.3.gz 
│                │                       ├ [1898]: usr/share/man/man3/pmap_rmtcall.3.gz 
│                │                       ├ [1899]: usr/share/man/man3/pmap_set.3.gz 
│                │                       ├ [1900]: usr/share/man/man3/pmap_unset.3.gz 
│                │                       ├ [1901]: usr/share/man/man3/popen.3.gz 
│                │                       ├ [1902]: usr/share/man/man3/posix_fallocate.3.gz 
│                │                       ├ [1903]: usr/share/man/man3/posix_madvise.3.gz 
│                │                       ├ [1904]: usr/share/man/man3/posix_memalign.3.gz 
│                │                       ├ [1905]: usr/share/man/man3/posix_openpt.3.gz 
│                │                       ├ [1906]: usr/share/man/man3/posix_spawn.3.gz 
│                │                       ├ [1907]: usr/share/man/man3/posix_spawnp.3.gz 
│                │                       ├ [1908]: usr/share/man/man3/pow.3.gz 
│                │                       ├ [1909]: usr/share/man/man3/pow10.3.gz 
│                │                       ├ [1910]: usr/share/man/man3/pow10f.3.gz 
│                │                       ├ [1911]: usr/share/man/man3/pow10l.3.gz 
│                │                       ├ [1912]: usr/share/man/man3/powerof2.3.gz 
│                │                       ├ [1913]: usr/share/man/man3/powf.3.gz 
│                │                       ├ [1914]: usr/share/man/man3/powl.3.gz 
│                │                       ├ [1915]: usr/share/man/man3/printf.3.gz 
│                │                       ├ [1916]: usr/share/man/man3/profil.3.gz 
│                │                       ├ [1917]: usr/share/man/man3/program_invocation_name.3.gz 
│                │                       ├ [1918]: usr/share/man/man3/program_invocation_short_name.3.gz 
│                │                       ├ [1919]: usr/share/man/man3/psiginfo.3.gz 
│                │                       ├ [1920]: usr/share/man/man3/psignal.3.gz 
│                │                       ├ [1921]: usr/share/man/man3/pthread_atfork.3.gz 
│                │                       ├ [1922]: usr/share/man/man3/pthread_attr_destroy.3.gz 
│                │                       ├ [1923]: usr/share/man/man3/pthread_attr_getaffinity_np.3.gz 
│                │                       ├ [1924]: usr/share/man/man3/pthread_attr_getdetachstate.3.gz 
│                │                       ├ [1925]: usr/share/man/man3/pthread_attr_getguardsize.3.gz 
│                │                       ├ [1926]: usr/share/man/man3/pthread_attr_getinheritsched.3.gz 
│                │                       ├ [1927]: usr/share/man/man3/pthread_attr_getschedparam.3.gz 
│                │                       ├ [1928]: usr/share/man/man3/pthread_attr_getschedpolicy.3.gz 
│                │                       ├ [1929]: usr/share/man/man3/pthread_attr_getscope.3.gz 
│                │                       ├ [1930]: usr/share/man/man3/pthread_attr_getsigmask_np.3.gz 
│                │                       ├ [1931]: usr/share/man/man3/pthread_attr_getstack.3.gz 
│                │                       ├ [1932]: usr/share/man/man3/pthread_attr_getstackaddr.3.gz 
│                │                       ├ [1933]: usr/share/man/man3/pthread_attr_getstacksize.3.gz 
│                │                       ├ [1934]: usr/share/man/man3/pthread_attr_init.3.gz 
│                │                       ├ [1935]: usr/share/man/man3/pthread_attr_setaffinity_np.3.gz 
│                │                       ├ [1936]: usr/share/man/man3/pthread_attr_setdetachstate.3.gz 
│                │                       ├ [1937]: usr/share/man/man3/pthread_attr_setguardsize.3.gz 
│                │                       ├ [1938]: usr/share/man/man3/pthread_attr_setinheritsched.3.gz 
│                │                       ├ [1939]: usr/share/man/man3/pthread_attr_setschedparam.3.gz 
│                │                       ├ [1940]: usr/share/man/man3/pthread_attr_setschedpolicy.3.gz 
│                │                       ├ [1941]: usr/share/man/man3/pthread_attr_setscope.3.gz 
│                │                       ├ [1942]: usr/share/man/man3/pthread_attr_setsigmask_np.3.gz 
│                │                       ├ [1943]: usr/share/man/man3/pthread_attr_setstack.3.gz 
│                │                       ├ [1944]: usr/share/man/man3/pthread_attr_setstackaddr.3.gz 
│                │                       ├ [1945]: usr/share/man/man3/pthread_attr_setstacksize.3.gz 
│                │                       ├ [1946]: usr/share/man/man3/pthread_cancel.3.gz 
│                │                       ├ [1947]: usr/share/man/man3/pthread_cleanup_pop.3.gz 
│                │                       ├ [1948]: usr/share/man/man3/pthread_cleanup_pop_restore_np.3.gz 
│                │                       ├ [1949]: usr/share/man/man3/pthread_cleanup_push.3.gz 
│                │                       ├ [1950]: usr/share/man/man3/pthread_cleanup_push_defer_np.3.gz 
│                │                       ├ [1951]: usr/share/man/man3/pthread_cond_broadcast.3.gz 
│                │                       ├ [1952]: usr/share/man/man3/pthread_cond_destroy.3.gz 
│                │                       ├ [1953]: usr/share/man/man3/pthread_cond_init.3.gz 
│                │                       ├ [1954]: usr/share/man/man3/pthread_cond_signal.3.gz 
│                │                       ├ [1955]: usr/share/man/man3/pthread_cond_timedwait.3.gz 
│                │                       ├ [1956]: usr/share/man/man3/pthread_cond_wait.3.gz 
│                │                       ├ [1957]: usr/share/man/man3/pthread_condattr_destroy.3.gz 
│                │                       ├ [1958]: usr/share/man/man3/pthread_condattr_init.3.gz 
│                │                       ├ [1959]: usr/share/man/man3/pthread_create.3.gz 
│                │                       ├ [1960]: usr/share/man/man3/pthread_detach.3.gz 
│                │                       ├ [1961]: usr/share/man/man3/pthread_equal.3.gz 
│                │                       ├ [1962]: usr/share/man/man3/pthread_exit.3.gz 
│                │                       ├ [1963]: usr/share/man/man3/pthread_getaffinity_np.3.gz 
│                │                       ├ [1964]: usr/share/man/man3/pthread_getattr_default_np.3.gz 
│                │                       ├ [1965]: usr/share/man/man3/pthread_getattr_np.3.gz 
│                │                       ├ [1966]: usr/share/man/man3/pthread_getconcurrency.3.gz 
│                │                       ├ [1967]: usr/share/man/man3/pthread_getcpuclockid.3.gz 
│                │                       ├ [1968]: usr/share/man/man3/pthread_getname_np.3.gz 
│                │                       ├ [1969]: usr/share/man/man3/pthread_getschedparam.3.gz 
│                │                       ├ [1970]: usr/share/man/man3/pthread_getspecific.3.gz 
│                │                       ├ [1971]: usr/share/man/man3/pthread_join.3.gz 
│                │                       ├ [1972]: usr/share/man/man3/pthread_key_create.3.gz 
│                │                       ├ [1973]: usr/share/man/man3/pthread_key_delete.3.gz 
│                │                       ├ [1974]: usr/share/man/man3/pthread_kill.3.gz 
│                │                       ├ [1975]: usr/share/man/man3/pthread_kill_other_threads_np.3.gz 
│                │                       ├ [1976]: usr/share/man/man3/pthread_mutex_consistent.3.gz 
│                │                       ├ [1977]: usr/share/man/man3/pthread_mutex_consistent_np.3.gz 
│                │                       ├ [1978]: usr/share/man/man3/pthread_mutex_destroy.3.gz 
│                │                       ├ [1979]: usr/share/man/man3/pthread_mutex_init.3.gz 
│                │                       ├ [1980]: usr/share/man/man3/pthread_mutex_lock.3.gz 
│                │                       ├ [1981]: usr/share/man/man3/pthread_mutex_trylock.3.gz 
│                │                       ├ [1982]: usr/share/man/man3/pthread_mutex_unlock.3.gz 
│                │                       ├ [1983]: usr/share/man/man3/pthread_mutexattr_destroy.3.gz 
│                │                       ├ [1984]: usr/share/man/man3/pthread_mutexattr_getkind_np.3.gz 
│                │                       ├ [1985]: usr/share/man/man3/pthread_mutexattr_getpshared.3.gz 
│                │                       ├ [1986]: usr/share/man/man3/pthread_mutexattr_getrobust.3.gz 
│                │                       ├ [1987]: usr/share/man/man3/pthread_mutexattr_getrobust_np.3.gz 
│                │                       ├ [1988]: usr/share/man/man3/pthread_mutexattr_gettype.3.gz 
│                │                       ├ [1989]: usr/share/man/man3/pthread_mutexattr_init.3.gz 
│                │                       ├ [1990]: usr/share/man/man3/pthread_mutexattr_setkind_np.3.gz 
│                │                       ├ [1991]: usr/share/man/man3/pthread_mutexattr_setpshared.3.gz 
│                │                       ├ [1992]: usr/share/man/man3/pthread_mutexattr_setrobust.3.gz 
│                │                       ├ [1993]: usr/share/man/man3/pthread_mutexattr_setrobust_np.3.gz 
│                │                       ├ [1994]: usr/share/man/man3/pthread_mutexattr_settype.3.gz 
│                │                       ├ [1995]: usr/share/man/man3/pthread_once.3.gz 
│                │                       ├ [1996]: usr/share/man/man3/pthread_rwlockattr_getkind_np.3.gz 
│                │                       ├ [1997]: usr/share/man/man3/pthread_rwlockattr_setkind_np.3.gz 
│                │                       ├ [1998]: usr/share/man/man3/pthread_self.3.gz 
│                │                       ├ [1999]: usr/share/man/man3/pthread_setaffinity_np.3.gz 
│                │                       ├ [2000]: usr/share/man/man3/pthread_setattr_default_np.3.gz 
│                │                       ├ [2001]: usr/share/man/man3/pthread_setcancelstate.3.gz 
│                │                       ├ [2002]: usr/share/man/man3/pthread_setcanceltype.3.gz 
│                │                       ├ [2003]: usr/share/man/man3/pthread_setconcurrency.3.gz 
│                │                       ├ [2004]: usr/share/man/man3/pthread_setname_np.3.gz 
│                │                       ├ [2005]: usr/share/man/man3/pthread_setschedparam.3.gz 
│                │                       ├ [2006]: usr/share/man/man3/pthread_setschedprio.3.gz 
│                │                       ├ [2007]: usr/share/man/man3/pthread_setspecific.3.gz 
│                │                       ├ [2008]: usr/share/man/man3/pthread_sigmask.3.gz 
│                │                       ├ [2009]: usr/share/man/man3/pthread_sigqueue.3.gz 
│                │                       ├ [2010]: usr/share/man/man3/pthread_spin_destroy.3.gz 
│                │                       ├ [2011]: usr/share/man/man3/pthread_spin_init.3.gz 
│                │                       ├ [2012]: usr/share/man/man3/pthread_spin_lock.3.gz 
│                │                       ├ [2013]: usr/share/man/man3/pthread_spin_trylock.3.gz 
│                │                       ├ [2014]: usr/share/man/man3/pthread_spin_unlock.3.gz 
│                │                       ├ [2015]: usr/share/man/man3/pthread_testcancel.3.gz 
│                │                       ├ [2016]: usr/share/man/man3/pthread_timedjoin_np.3.gz 
│                │                       ├ [2017]: usr/share/man/man3/pthread_tryjoin_np.3.gz 
│                │                       ├ [2018]: usr/share/man/man3/pthread_yield.3.gz 
│                │                       ├ [2019]: usr/share/man/man3/ptsname.3.gz 
│                │                       ├ [2020]: usr/share/man/man3/ptsname_r.3.gz 
│                │                       ├ [2021]: usr/share/man/man3/putc.3.gz 
│                │                       ├ [2022]: usr/share/man/man3/putc_unlocked.3.gz 
│                │                       ├ [2023]: usr/share/man/man3/putchar.3.gz 
│                │                       ├ [2024]: usr/share/man/man3/putchar_unlocked.3.gz 
│                │                       ├ [2025]: usr/share/man/man3/putenv.3.gz 
│                │                       ├ [2026]: usr/share/man/man3/putgrent.3.gz 
│                │                       ├ [2027]: usr/share/man/man3/putpwent.3.gz 
│                │                       ├ [2028]: usr/share/man/man3/puts.3.gz 
│                │                       ├ [2029]: usr/share/man/man3/putspent.3.gz 
│                │                       ├ [2030]: usr/share/man/man3/pututline.3.gz 
│                │                       ├ [2031]: usr/share/man/man3/pututxline.3.gz 
│                │                       ├ [2032]: usr/share/man/man3/putw.3.gz 
│                │                       ├ [2033]: usr/share/man/man3/putwc.3.gz 
│                │                       ├ [2034]: usr/share/man/man3/putwc_unlocked.3.gz 
│                │                       ├ [2035]: usr/share/man/man3/putwchar.3.gz 
│                │                       ├ [2036]: usr/share/man/man3/putwchar_unlocked.3.gz 
│                │                       ├ [2037]: usr/share/man/man3/pvalloc.3.gz 
│                │                       ├ [2038]: usr/share/man/man3/qecvt.3.gz 
│                │                       ├ [2039]: usr/share/man/man3/qecvt_r.3.gz 
│                │                       ├ [2040]: usr/share/man/man3/qfcvt.3.gz 
│                │                       ├ [2041]: usr/share/man/man3/qfcvt_r.3.gz 
│                │                       ├ [2042]: usr/share/man/man3/qgcvt.3.gz 
│                │                       ├ [2043]: usr/share/man/man3/qsort.3.gz 
│                │                       ├ [2044]: usr/share/man/man3/qsort_r.3.gz 
│                │                       ├ [2045]: usr/share/man/man3/queue.3.gz 
│                │                       ├ [2046]: usr/share/man/man3/raise.3.gz 
│                │                       ├ [2047]: usr/share/man/man3/rand.3.gz 
│                │                       ├ [2048]: usr/share/man/man3/rand_r.3.gz 
│                │                       ├ [2049]: usr/share/man/man3/random.3.gz 
│                │                       ├ [2050]: usr/share/man/man3/random_r.3.gz 
│                │                       ├ [2051]: usr/share/man/man3/rawmemchr.3.gz 
│                │                       ├ [2052]: usr/share/man/man3/rcmd.3.gz 
│                │                       ├ [2053]: usr/share/man/man3/rcmd_af.3.gz 
│                │                       ├ [2054]: usr/share/man/man3/re_comp.3.gz 
│                │                       ├ [2055]: usr/share/man/man3/re_exec.3.gz 
│                │                       ├ [2056]: usr/share/man/man3/readdir.3.gz 
│                │                       ├ [2057]: usr/share/man/man3/readdir_r.3.gz 
│                │                       ├ [2058]: usr/share/man/man3/realloc.3.gz 
│                │                       ├ [2059]: usr/share/man/man3/reallocarray.3.gz 
│                │                       ├ [2060]: usr/share/man/man3/realpath.3.gz 
│                │                       ├ [2061]: usr/share/man/man3/recno.3.gz 
│                │                       ├ [2062]: usr/share/man/man3/regcomp.3.gz 
│                │                       ├ [2063]: usr/share/man/man3/regerror.3.gz 
│                │                       ├ [2064]: usr/share/man/man3/regex.3.gz 
│                │                       ├ [2065]: usr/share/man/man3/regexec.3.gz 
│                │                       ├ [2066]: usr/share/man/man3/regfree.3.gz 
│                │                       ├ [2067]: usr/share/man/man3/register_printf_modifier.3.gz 
│                │                       ├ [2068]: usr/share/man/man3/register_printf_specifier.3.gz 
│                │                       ├ [2069]: usr/share/man/man3/register_printf_type.3.gz 
│                │                       ├ [2070]: usr/share/man/man3/registerrpc.3.gz 
│                │                       ├ [2071]: usr/share/man/man3/remainder.3.gz 
│                │                       ├ [2072]: usr/share/man/man3/remainderf.3.gz 
│                │                       ├ [2073]: usr/share/man/man3/remainderl.3.gz 
│                │                       ├ [2074]: usr/share/man/man3/remove.3.gz 
│                │                       ├ [2075]: usr/share/man/man3/remque.3.gz 
│                │                       ├ [2076]: usr/share/man/man3/remquo.3.gz 
│                │                       ├ [2077]: usr/share/man/man3/remquof.3.gz 
│                │                       ├ [2078]: usr/share/man/man3/remquol.3.gz 
│                │                       ├ [2079]: usr/share/man/man3/res_init.3.gz 
│                │                       ├ [2080]: usr/share/man/man3/res_mkquery.3.gz 
│                │                       ├ [2081]: usr/share/man/man3/res_nclose.3.gz 
│                │                       ├ [2082]: usr/share/man/man3/res_ninit.3.gz 
│                │                       ├ [2083]: usr/share/man/man3/res_nmkquery.3.gz 
│                │                       ├ [2084]: usr/share/man/man3/res_nquery.3.gz 
│                │                       ├ [2085]: usr/share/man/man3/res_nquerydomain.3.gz 
│                │                       ├ [2086]: usr/share/man/man3/res_nsearch.3.gz 
│                │                       ├ [2087]: usr/share/man/man3/res_nsend.3.gz 
│                │                       ├ [2088]: usr/share/man/man3/res_query.3.gz 
│                │                       ├ [2089]: usr/share/man/man3/res_querydomain.3.gz 
│                │                       ├ [2090]: usr/share/man/man3/res_search.3.gz 
│                │                       ├ [2091]: usr/share/man/man3/res_send.3.gz 
│                │                       ├ [2092]: usr/share/man/man3/resolver.3.gz 
│                │                       ├ [2093]: usr/share/man/man3/rewind.3.gz 
│                │                       ├ [2094]: usr/share/man/man3/rewinddir.3.gz 
│                │                       ├ [2095]: usr/share/man/man3/rexec.3.gz 
│                │                       ├ [2096]: usr/share/man/man3/rexec_af.3.gz 
│                │                       ├ [2097]: usr/share/man/man3/rindex.3.gz 
│                │                       ├ [2098]: usr/share/man/man3/rint.3.gz 
│                │                       ├ [2099]: usr/share/man/man3/rintf.3.gz 
│                │                       ├ [2100]: usr/share/man/man3/rintl.3.gz 
│                │                       ├ [2101]: usr/share/man/man3/round.3.gz 
│                │                       ├ [2102]: usr/share/man/man3/roundf.3.gz 
│                │                       ├ [2103]: usr/share/man/man3/roundl.3.gz 
│                │                       ├ [2104]: usr/share/man/man3/roundup.3.gz 
│                │                       ├ [2105]: usr/share/man/man3/rpc.3.gz 
│                │                       ├ [2106]: usr/share/man/man3/rpmatch.3.gz 
│                │                       ├ [2107]: usr/share/man/man3/rresvport.3.gz 
│                │                       ├ [2108]: usr/share/man/man3/rresvport_af.3.gz 
│                │                       ├ [2109]: usr/share/man/man3/rtime.3.gz 
│                │                       ├ [2110]: usr/share/man/man3/rtnetlink.3.gz 
│                │                       ├ [2111]: usr/share/man/man3/ruserok.3.gz 
│                │                       ├ [2112]: usr/share/man/man3/ruserok_af.3.gz 
│                │                       ├ [2113]: usr/share/man/man3/scalb.3.gz 
│                │                       ├ [2114]: usr/share/man/man3/scalbf.3.gz 
│                │                       ├ [2115]: usr/share/man/man3/scalbl.3.gz 
│                │                       ├ [2116]: usr/share/man/man3/scalbln.3.gz 
│                │                       ├ [2117]: usr/share/man/man3/scalblnf.3.gz 
│                │                       ├ [2118]: usr/share/man/man3/scalblnl.3.gz 
│                │                       ├ [2119]: usr/share/man/man3/scalbn.3.gz 
│                │                       ├ [2120]: usr/share/man/man3/scalbnf.3.gz 
│                │                       ├ [2121]: usr/share/man/man3/scalbnl.3.gz 
│                │                       ├ [2122]: usr/share/man/man3/scandir.3.gz 
│                │                       ├ [2123]: usr/share/man/man3/scandirat.3.gz 
│                │                       ├ [2124]: usr/share/man/man3/scanf.3.gz 
│                │                       ├ [2125]: usr/share/man/man3/sched_getcpu.3.gz 
│                │                       ├ [2126]: usr/share/man/man3/secure_getenv.3.gz 
│                │                       ├ [2127]: usr/share/man/man3/seed48.3.gz 
│                │                       ├ [2128]: usr/share/man/man3/seed48_r.3.gz 
│                │                       ├ [2129]: usr/share/man/man3/seekdir.3.gz 
│                │                       ├ [2130]: usr/share/man/man3/sem_close.3.gz 
│                │                       ├ [2131]: usr/share/man/man3/sem_destroy.3.gz 
│                │                       ├ [2132]: usr/share/man/man3/sem_getvalue.3.gz 
│                │                       ├ [2133]: usr/share/man/man3/sem_init.3.gz 
│                │                       ├ [2134]: usr/share/man/man3/sem_open.3.gz 
│                │                       ├ [2135]: usr/share/man/man3/sem_post.3.gz 
│                │                       ├ [2136]: usr/share/man/man3/sem_timedwait.3.gz 
│                │                       ├ [2137]: usr/share/man/man3/sem_trywait.3.gz 
│                │                       ├ [2138]: usr/share/man/man3/sem_unlink.3.gz 
│                │                       ├ [2139]: usr/share/man/man3/sem_wait.3.gz 
│                │                       ├ [2140]: usr/share/man/man3/setaliasent.3.gz 
│                │                       ├ [2141]: usr/share/man/man3/setbuf.3.gz 
│                │                       ├ [2142]: usr/share/man/man3/setbuffer.3.gz 
│                │                       ├ [2143]: usr/share/man/man3/setcontext.3.gz 
│                │                       ├ [2144]: usr/share/man/man3/setenv.3.gz 
│                │                       ├ [2145]: usr/share/man/man3/setfsent.3.gz 
│                │                       ├ [2146]: usr/share/man/man3/setgrent.3.gz 
│                │                       ├ [2147]: usr/share/man/man3/sethostent.3.gz 
│                │                       ├ [2148]: usr/share/man/man3/sethostid.3.gz 
│                │                       ├ [2149]: usr/share/man/man3/setjmp.3.gz 
│                │                       ├ [2150]: usr/share/man/man3/setkey.3.gz 
│                │                       ├ [2151]: usr/share/man/man3/setkey_r.3.gz 
│                │                       ├ [2152]: usr/share/man/man3/setlinebuf.3.gz 
│                │                       ├ [2153]: usr/share/man/man3/setlocale.3.gz 
│                │                       ├ [2154]: usr/share/man/man3/setlogmask.3.gz 
│                │                       ├ [2155]: usr/share/man/man3/setmntent.3.gz 
│                │                       ├ [2156]: usr/share/man/man3/setnetent.3.gz 
│                │                       ├ [2157]: usr/share/man/man3/setnetgrent.3.gz 
│                │                       ├ [2158]: usr/share/man/man3/setprotoent.3.gz 
│                │                       ├ [2159]: usr/share/man/man3/setpwent.3.gz 
│                │                       ├ [2160]: usr/share/man/man3/setrpcent.3.gz 
│                │                       ├ [2161]: usr/share/man/man3/setservent.3.gz 
│                │                       ├ [2162]: usr/share/man/man3/setspent.3.gz 
│                │                       ├ [2163]: usr/share/man/man3/setstate.3.gz 
│                │                       ├ [2164]: usr/share/man/man3/setstate_r.3.gz 
│                │                       ├ [2165]: usr/share/man/man3/setttyent.3.gz 
│                │                       ├ [2166]: usr/share/man/man3/setusershell.3.gz 
│                │                       ├ [2167]: usr/share/man/man3/setutent.3.gz 
│                │                       ├ [2168]: usr/share/man/man3/setutxent.3.gz 
│                │                       ├ [2169]: usr/share/man/man3/setvbuf.3.gz 
│                │                       ├ [2170]: usr/share/man/man3/sgetspent.3.gz 
│                │                       ├ [2171]: usr/share/man/man3/sgetspent_r.3.gz 
│                │                       ├ [2172]: usr/share/man/man3/shm_open.3.gz 
│                │                       ├ [2173]: usr/share/man/man3/shm_unlink.3.gz 
│                │                       ├ [2174]: usr/share/man/man3/sigabbrev_np.3.gz 
│                │                       ├ [2175]: usr/share/man/man3/sigaddset.3.gz 
│                │                       ├ [2176]: usr/share/man/man3/sigandset.3.gz 
│                │                       ├ [2177]: usr/share/man/man3/sigblock.3.gz 
│                │                       ├ [2178]: usr/share/man/man3/sigdelset.3.gz 
│                │                       ├ [2179]: usr/share/man/man3/sigdescr_np.3.gz 
│                │                       ├ [2180]: usr/share/man/man3/sigemptyset.3.gz 
│                │                       ├ [2181]: usr/share/man/man3/sigfillset.3.gz 
│                │                       ├ [2182]: usr/share/man/man3/siggetmask.3.gz 
│                │                       ├ [2183]: usr/share/man/man3/sighold.3.gz 
│                │                       ├ [2184]: usr/share/man/man3/sigignore.3.gz 
│                │                       ├ [2185]: usr/share/man/man3/siginterrupt.3.gz 
│                │                       ├ [2186]: usr/share/man/man3/sigisemptyset.3.gz 
│                │                       ├ [2187]: usr/share/man/man3/sigismember.3.gz 
│                │                       ├ [2188]: usr/share/man/man3/siglongjmp.3.gz 
│                │                       ├ [2189]: usr/share/man/man3/sigmask.3.gz 
│                │                       ├ [2190]: usr/share/man/man3/signbit.3.gz 
│                │                       ├ [2191]: usr/share/man/man3/signgam.3.gz 
│                │                       ├ [2192]: usr/share/man/man3/significand.3.gz 
│                │                       ├ [2193]: usr/share/man/man3/significandf.3.gz 
│                │                       ├ [2194]: usr/share/man/man3/significandl.3.gz 
│                │                       ├ [2195]: usr/share/man/man3/sigorset.3.gz 
│                │                       ├ [2196]: usr/share/man/man3/sigpause.3.gz 
│                │                       ├ [2197]: usr/share/man/man3/sigqueue.3.gz 
│                │                       ├ [2198]: usr/share/man/man3/sigrelse.3.gz 
│                │                       ├ [2199]: usr/share/man/man3/sigset.3.gz 
│                │                       ├ [2200]: usr/share/man/man3/sigsetjmp.3.gz 
│                │                       ├ [2201]: usr/share/man/man3/sigsetmask.3.gz 
│                │                       ├ [2202]: usr/share/man/man3/sigsetops.3.gz 
│                │                       ├ [2203]: usr/share/man/man3/sigstack.3.gz 
│                │                       ├ [2204]: usr/share/man/man3/sigvec.3.gz 
│                │                       ├ [2205]: usr/share/man/man3/sigwait.3.gz 
│                │                       ├ [2206]: usr/share/man/man3/simpleq.3.gz 
│                │                       ├ [2207]: usr/share/man/man3/sin.3.gz 
│                │                       ├ [2208]: usr/share/man/man3/sincos.3.gz 
│                │                       ├ [2209]: usr/share/man/man3/sincosf.3.gz 
│                │                       ├ [2210]: usr/share/man/man3/sincosl.3.gz 
│                │                       ├ [2211]: usr/share/man/man3/sinf.3.gz 
│                │                       ├ [2212]: usr/share/man/man3/sinh.3.gz 
│                │                       ├ [2213]: usr/share/man/man3/sinhf.3.gz 
│                │                       ├ [2214]: usr/share/man/man3/sinhl.3.gz 
│                │                       ├ [2215]: usr/share/man/man3/sinl.3.gz 
│                │                       ├ [2216]: usr/share/man/man3/sleep.3.gz 
│                │                       ├ [2217]: usr/share/man/man3/slist.3.gz 
│                │                       ├ [2218]: usr/share/man/man3/snprintf.3.gz 
│                │                       ├ [2219]: usr/share/man/man3/sockatmark.3.gz 
│                │                       ├ [2220]: usr/share/man/man3/sprintf.3.gz 
│                │                       ├ [2221]: usr/share/man/man3/sqrt.3.gz 
│                │                       ├ [2222]: usr/share/man/man3/sqrtf.3.gz 
│                │                       ├ [2223]: usr/share/man/man3/sqrtl.3.gz 
│                │                       ├ [2224]: usr/share/man/man3/srand.3.gz 
│                │                       ├ [2225]: usr/share/man/man3/srand48.3.gz 
│                │                       ├ [2226]: usr/share/man/man3/srand48_r.3.gz 
│                │                       ├ [2227]: usr/share/man/man3/srandom.3.gz 
│                │                       ├ [2228]: usr/share/man/man3/srandom_r.3.gz 
│                │                       ├ [2229]: usr/share/man/man3/sscanf.3.gz 
│                │                       ├ [2230]: usr/share/man/man3/ssignal.3.gz 
│                │                       ├ [2231]: usr/share/man/man3/stailq.3.gz 
│                │                       ├ [2232]: usr/share/man/man3/static_assert.3.gz 
│                │                       ├ [2233]: usr/share/man/man3/statvfs.3.gz 
│                │                       ├ [2234]: usr/share/man/man3/stdarg.3.gz 
│                │                       ├ [2235]: usr/share/man/man3/stderr.3.gz 
│                │                       ├ [2236]: usr/share/man/man3/stdin.3.gz 
│                │                       ├ [2237]: usr/share/man/man3/stdio.3.gz 
│                │                       ├ [2238]: usr/share/man/man3/stdio_ext.3.gz 
│                │                       ├ [2239]: usr/share/man/man3/stdout.3.gz 
│                │                       ├ [2240]: usr/share/man/man3/stpcpy.3.gz 
│                │                       ├ [2241]: usr/share/man/man3/stpncpy.3.gz 
│                │                       ├ [2242]: usr/share/man/man3/strcasecmp.3.gz 
│                │                       ├ [2243]: usr/share/man/man3/strcasestr.3.gz 
│                │                       ├ [2244]: usr/share/man/man3/strcat.3.gz 
│                │                       ├ [2245]: usr/share/man/man3/strchr.3.gz 
│                │                       ├ [2246]: usr/share/man/man3/strchrnul.3.gz 
│                │                       ├ [2247]: usr/share/man/man3/strcmp.3.gz 
│                │                       ├ [2248]: usr/share/man/man3/strcoll.3.gz 
│                │                       ├ [2249]: usr/share/man/man3/strcpy.3.gz 
│                │                       ├ [2250]: usr/share/man/man3/strcspn.3.gz 
│                │                       ├ [2251]: usr/share/man/man3/strdup.3.gz 
│                │                       ├ [2252]: usr/share/man/man3/strdupa.3.gz 
│                │                       ├ [2253]: usr/share/man/man3/streq.3.gz 
│                │                       ├ [2254]: usr/share/man/man3/strerror.3.gz 
│                │                       ├ [2255]: usr/share/man/man3/strerror_l.3.gz 
│                │                       ├ [2256]: usr/share/man/man3/strerror_r.3.gz 
│                │                       ├ [2257]: usr/share/man/man3/strerrordesc_np.3.gz 
│                │                       ├ [2258]: usr/share/man/man3/strerrorname_np.3.gz 
│                │                       ├ [2259]: usr/share/man/man3/strfmon.3.gz 
│                │                       ├ [2260]: usr/share/man/man3/strfmon_l.3.gz 
│                │                       ├ [2261]: usr/share/man/man3/strfromd.3.gz 
│                │                       ├ [2262]: usr/share/man/man3/strfromf.3.gz 
│                │                       ├ [2263]: usr/share/man/man3/strfroml.3.gz 
│                │                       ├ [2264]: usr/share/man/man3/strfry.3.gz 
│                │                       ├ [2265]: usr/share/man/man3/strftime.3.gz 
│                │                       ├ [2266]: usr/share/man/man3/strftime_l.3.gz 
│                │                       ├ [2267]: usr/share/man/man3/string.3.gz 
│                │                       ├ [2268]: usr/share/man/man3/strlen.3.gz 
│                │                       ├ [2269]: usr/share/man/man3/strncasecmp.3.gz 
│                │                       ├ [2270]: usr/share/man/man3/strncat.3.gz 
│                │                       ├ [2271]: usr/share/man/man3/strncmp.3.gz 
│                │                       ├ [2272]: usr/share/man/man3/strncpy.3.gz 
│                │                       ├ [2273]: usr/share/man/man3/strndup.3.gz 
│                │                       ├ [2274]: usr/share/man/man3/strndupa.3.gz 
│                │                       ├ [2275]: usr/share/man/man3/strnlen.3.gz 
│                │                       ├ [2276]: usr/share/man/man3/strpbrk.3.gz 
│                │                       ├ [2277]: usr/share/man/man3/strptime.3.gz 
│                │                       ├ [2278]: usr/share/man/man3/strrchr.3.gz 
│                │                       ├ [2279]: usr/share/man/man3/strsep.3.gz 
│                │                       ├ [2280]: usr/share/man/man3/strsignal.3.gz 
│                │                       ├ [2281]: usr/share/man/man3/strspn.3.gz 
│                │                       ├ [2282]: usr/share/man/man3/strstr.3.gz 
│                │                       ├ [2283]: usr/share/man/man3/strtod.3.gz 
│                │                       ├ [2284]: usr/share/man/man3/strtof.3.gz 
│                │                       ├ [2285]: usr/share/man/man3/strtoimax.3.gz 
│                │                       ├ [2286]: usr/share/man/man3/strtok.3.gz 
│                │                       ├ [2287]: usr/share/man/man3/strtok_r.3.gz 
│                │                       ├ [2288]: usr/share/man/man3/strtol.3.gz 
│                │                       ├ [2289]: usr/share/man/man3/strtold.3.gz 
│                │                       ├ [2290]: usr/share/man/man3/strtoll.3.gz 
│                │                       ├ [2291]: usr/share/man/man3/strtoq.3.gz 
│                │                       ├ [2292]: usr/share/man/man3/strtoul.3.gz 
│                │                       ├ [2293]: usr/share/man/man3/strtoull.3.gz 
│                │                       ├ [2294]: usr/share/man/man3/strtoumax.3.gz 
│                │                       ├ [2295]: usr/share/man/man3/strtouq.3.gz 
│                │                       ├ [2296]: usr/share/man/man3/strverscmp.3.gz 
│                │                       ├ [2297]: usr/share/man/man3/strxfrm.3.gz 
│                │                       ├ [2298]: usr/share/man/man3/svc_destroy.3.gz 
│                │                       ├ [2299]: usr/share/man/man3/svc_freeargs.3.gz 
│                │                       ├ [2300]: usr/share/man/man3/svc_getargs.3.gz 
│                │                       ├ [2301]: usr/share/man/man3/svc_getcaller.3.gz 
│                │                       ├ [2302]: usr/share/man/man3/svc_getreq.3.gz 
│                │                       ├ [2303]: usr/share/man/man3/svc_getreqset.3.gz 
│                │                       ├ [2304]: usr/share/man/man3/svc_register.3.gz 
│                │                       ├ [2305]: usr/share/man/man3/svc_run.3.gz 
│                │                       ├ [2306]: usr/share/man/man3/svc_sendreply.3.gz 
│                │                       ├ [2307]: usr/share/man/man3/svc_unregister.3.gz 
│                │                       ├ [2308]: usr/share/man/man3/svcerr_auth.3.gz 
│                │                       ├ [2309]: usr/share/man/man3/svcerr_decode.3.gz 
│                │                       ├ [2310]: usr/share/man/man3/svcerr_noproc.3.gz 
│                │                       ├ [2311]: usr/share/man/man3/svcerr_noprog.3.gz 
│                │                       ├ [2312]: usr/share/man/man3/svcerr_progvers.3.gz 
│                │                       ├ [2313]: usr/share/man/man3/svcerr_systemerr.3.gz 
│                │                       ├ [2314]: usr/share/man/man3/svcerr_weakauth.3.gz 
│                │                       ├ [2315]: usr/share/man/man3/svcfd_create.3.gz 
│                │                       ├ [2316]: usr/share/man/man3/svcraw_create.3.gz 
│                │                       ├ [2317]: usr/share/man/man3/svctcp_create.3.gz 
│                │                       ├ [2318]: usr/share/man/man3/svcudp_bufcreate.3.gz 
│                │                       ├ [2319]: usr/share/man/man3/svcudp_create.3.gz 
│                │                       ├ [2320]: usr/share/man/man3/swab.3.gz 
│                │                       ├ [2321]: usr/share/man/man3/swapcontext.3.gz 
│                │                       ├ [2322]: usr/share/man/man3/swprintf.3.gz 
│                │                       ├ [2323]: usr/share/man/man3/sys_errlist.3.gz 
│                │                       ├ [2324]: usr/share/man/man3/sys_nerr.3.gz 
│                │                       ├ [2325]: usr/share/man/man3/sys_siglist.3.gz 
│                │                       ├ [2326]: usr/share/man/man3/sysconf.3.gz 
│                │                       ├ [2327]: usr/share/man/man3/syslog.3.gz 
│                │                       ├ [2328]: usr/share/man/man3/system.3.gz 
│                │                       ├ [2329]: usr/share/man/man3/sysv_signal.3.gz 
│                │                       ├ [2330]: usr/share/man/man3/tailq.3.gz 
│                │                       ├ [2331]: usr/share/man/man3/tan.3.gz 
│                │                       ├ [2332]: usr/share/man/man3/tanf.3.gz 
│                │                       ├ [2333]: usr/share/man/man3/tanh.3.gz 
│                │                       ├ [2334]: usr/share/man/man3/tanhf.3.gz 
│                │                       ├ [2335]: usr/share/man/man3/tanhl.3.gz 
│                │                       ├ [2336]: usr/share/man/man3/tanl.3.gz 
│                │                       ├ [2337]: usr/share/man/man3/tcdrain.3.gz 
│                │                       ├ [2338]: usr/share/man/man3/tcflow.3.gz 
│                │                       ├ [2339]: usr/share/man/man3/tcflush.3.gz 
│                │                       ├ [2340]: usr/share/man/man3/tcgetattr.3.gz 
│                │                       ├ [2341]: usr/share/man/man3/tcgetpgrp.3.gz 
│                │                       ├ [2342]: usr/share/man/man3/tcgetsid.3.gz 
│                │                       ├ [2343]: usr/share/man/man3/tcsendbreak.3.gz 
│                │                       ├ [2344]: usr/share/man/man3/tcsetattr.3.gz 
│                │                       ├ [2345]: usr/share/man/man3/tcsetpgrp.3.gz 
│                │                       ├ [2346]: usr/share/man/man3/tdelete.3.gz 
│                │                       ├ [2347]: usr/share/man/man3/tdestroy.3.gz 
│                │                       ├ [2348]: usr/share/man/man3/telldir.3.gz 
│                │                       ├ [2349]: usr/share/man/man3/tempnam.3.gz 
│                │                       ├ [2350]: usr/share/man/man3/termios.3.gz 
│                │                       ├ [2351]: usr/share/man/man3/tfind.3.gz 
│                │                       ├ [2352]: usr/share/man/man3/tgamma.3.gz 
│                │                       ├ [2353]: usr/share/man/man3/tgammaf.3.gz 
│                │                       ├ [2354]: usr/share/man/man3/tgammal.3.gz 
│                │                       ├ [2355]: usr/share/man/man3/timegm.3.gz 
│                │                       ├ [2356]: usr/share/man/man3/timelocal.3.gz 
│                │                       ├ [2357]: usr/share/man/man3/timeradd.3.gz 
│                │                       ├ [2358]: usr/share/man/man3/timerclear.3.gz 
│                │                       ├ [2359]: usr/share/man/man3/timercmp.3.gz 
│                │                       ├ [2360]: usr/share/man/man3/timerisset.3.gz 
│                │                       ├ [2361]: usr/share/man/man3/timersub.3.gz 
│                │                       ├ [2362]: usr/share/man/man3/timespec_get.3.gz 
│                │                       ├ [2363]: usr/share/man/man3/timespec_getres.3.gz 
│                │                       ├ [2364]: usr/share/man/man3/timezone.3.gz 
│                │                       ├ [2365]: usr/share/man/man3/tmpfile.3.gz 
│                │                       ├ [2366]: usr/share/man/man3/tmpnam.3.gz 
│                │                       ├ [2367]: usr/share/man/man3/tmpnam_r.3.gz 
│                │                       ├ [2368]: usr/share/man/man3/toascii.3.gz 
│                │                       ├ [2369]: usr/share/man/man3/tolower.3.gz 
│                │                       ├ [2370]: usr/share/man/man3/tolower_l.3.gz 
│                │                       ├ [2371]: usr/share/man/man3/toupper.3.gz 
│                │                       ├ [2372]: usr/share/man/man3/toupper_l.3.gz 
│                │                       ├ [2373]: usr/share/man/man3/towctrans.3.gz 
│                │                       ├ [2374]: usr/share/man/man3/towlower.3.gz 
│                │                       ├ [2375]: usr/share/man/man3/towlower_l.3.gz 
│                │                       ├ [2376]: usr/share/man/man3/towupper.3.gz 
│                │                       ├ [2377]: usr/share/man/man3/towupper_l.3.gz 
│                │                       ├ [2378]: usr/share/man/man3/trunc.3.gz 
│                │                       ├ [2379]: usr/share/man/man3/truncf.3.gz 
│                │                       ├ [2380]: usr/share/man/man3/truncl.3.gz 
│                │                       ├ [2381]: usr/share/man/man3/tsearch.3.gz 
│                │                       ├ [2382]: usr/share/man/man3/ttyname.3.gz 
│                │                       ├ [2383]: usr/share/man/man3/ttyname_r.3.gz 
│                │                       ├ [2384]: usr/share/man/man3/ttyslot.3.gz 
│                │                       ├ [2385]: usr/share/man/man3/twalk.3.gz 
│                │                       ├ [2386]: usr/share/man/man3/twalk_r.3.gz 
│                │                       ├ [2387]: usr/share/man/man3/tzname.3.gz 
│                │                       ├ [2388]: usr/share/man/man3/tzset.3.gz 
│                │                       ├ [2389]: usr/share/man/man3/uabs.3.gz 
│                │                       ├ [2390]: usr/share/man/man3/ualarm.3.gz 
│                │                       ├ [2391]: usr/share/man/man3/uimaxabs.3.gz 
│                │                       ├ [2392]: usr/share/man/man3/ulabs.3.gz 
│                │                       ├ [2393]: usr/share/man/man3/ulckpwdf.3.gz 
│                │                       ├ [2394]: usr/share/man/man3/ulimit.3.gz 
│                │                       ├ [2395]: usr/share/man/man3/ullabs.3.gz 
│                │                       ├ [2396]: usr/share/man/man3/umaxabs.3.gz 
│                │                       ├ [2397]: usr/share/man/man3/undocumented.3.gz 
│                │                       ├ [2398]: usr/share/man/man3/ungetc.3.gz 
│                │                       ├ [2399]: usr/share/man/man3/ungetwc.3.gz 
│                │                       ├ [2400]: usr/share/man/man3/unlocked_stdio.3.gz 
│                │                       ├ [2401]: usr/share/man/man3/unlockpt.3.gz 
│                │                       ├ [2402]: usr/share/man/man3/unsetenv.3.gz 
│                │                       ├ [2403]: usr/share/man/man3/updwtmp.3.gz 
│                │                       ├ [2404]: usr/share/man/man3/updwtmpx.3.gz 
│                │                       ├ [2405]: usr/share/man/man3/uselocale.3.gz 
│                │                       ├ [2406]: usr/share/man/man3/usleep.3.gz 
│                │                       ├ [2407]: usr/share/man/man3/utmpname.3.gz 
│                │                       ├ [2408]: usr/share/man/man3/utmpxname.3.gz 
│                │                       ├ [2409]: usr/share/man/man3/va_arg.3.gz 
│                │                       ├ [2410]: usr/share/man/man3/va_copy.3.gz 
│                │                       ├ [2411]: usr/share/man/man3/va_end.3.gz 
│                │                       ├ [2412]: usr/share/man/man3/va_start.3.gz 
│                │                       ├ [2413]: usr/share/man/man3/valloc.3.gz 
│                │                       ├ [2414]: usr/share/man/man3/vasprintf.3.gz 
│                │                       ├ [2415]: usr/share/man/man3/vdprintf.3.gz 
│                │                       ├ [2416]: usr/share/man/man3/verr.3.gz 
│                │                       ├ [2417]: usr/share/man/man3/verrx.3.gz 
│                │                       ├ [2418]: usr/share/man/man3/versionsort.3.gz 
│                │                       ├ [2419]: usr/share/man/man3/vfprintf.3.gz 
│                │                       ├ [2420]: usr/share/man/man3/vfscanf.3.gz 
│                │                       ├ [2421]: usr/share/man/man3/vfwprintf.3.gz 
│                │                       ├ [2422]: usr/share/man/man3/vlimit.3.gz 
│                │                       ├ [2423]: usr/share/man/man3/vprintf.3.gz 
│                │                       ├ [2424]: usr/share/man/man3/vscanf.3.gz 
│                │                       ├ [2425]: usr/share/man/man3/vsnprintf.3.gz 
│                │                       ├ [2426]: usr/share/man/man3/vsprintf.3.gz 
│                │                       ├ [2427]: usr/share/man/man3/vsscanf.3.gz 
│                │                       ├ [2428]: usr/share/man/man3/vswprintf.3.gz 
│                │                       ├ [2429]: usr/share/man/man3/vsyslog.3.gz 
│                │                       ├ [2430]: usr/share/man/man3/vtimes.3.gz 
│                │                       ├ [2431]: usr/share/man/man3/vwarn.3.gz 
│                │                       ├ [2432]: usr/share/man/man3/vwarnx.3.gz 
│                │                       ├ [2433]: usr/share/man/man3/vwprintf.3.gz 
│                │                       ├ [2434]: usr/share/man/man3/warn.3.gz 
│                │                       ├ [2435]: usr/share/man/man3/warnx.3.gz 
│                │                       ├ [2436]: usr/share/man/man3/wcpcpy.3.gz 
│                │                       ├ [2437]: usr/share/man/man3/wcpncpy.3.gz 
│                │                       ├ [2438]: usr/share/man/man3/wcrtomb.3.gz 
│                │                       ├ [2439]: usr/share/man/man3/wcscasecmp.3.gz 
│                │                       ├ [2440]: usr/share/man/man3/wcscat.3.gz 
│                │                       ├ [2441]: usr/share/man/man3/wcschr.3.gz 
│                │                       ├ [2442]: usr/share/man/man3/wcscmp.3.gz 
│                │                       ├ [2443]: usr/share/man/man3/wcscpy.3.gz 
│                │                       ├ [2444]: usr/share/man/man3/wcscspn.3.gz 
│                │                       ├ [2445]: usr/share/man/man3/wcsdup.3.gz 
│                │                       ├ [2446]: usr/share/man/man3/wcslen.3.gz 
│                │                       ├ [2447]: usr/share/man/man3/wcsncasecmp.3.gz 
│                │                       ├ [2448]: usr/share/man/man3/wcsncat.3.gz 
│                │                       ├ [2449]: usr/share/man/man3/wcsncmp.3.gz 
│                │                       ├ [2450]: usr/share/man/man3/wcsncpy.3.gz 
│                │                       ├ [2451]: usr/share/man/man3/wcsnlen.3.gz 
│                │                       ├ [2452]: usr/share/man/man3/wcsnrtombs.3.gz 
│                │                       ├ [2453]: usr/share/man/man3/wcspbrk.3.gz 
│                │                       ├ [2454]: usr/share/man/man3/wcsrchr.3.gz 
│                │                       ├ [2455]: usr/share/man/man3/wcsrtombs.3.gz 
│                │                       ├ [2456]: usr/share/man/man3/wcsspn.3.gz 
│                │                       ├ [2457]: usr/share/man/man3/wcsstr.3.gz 
│                │                       ├ [2458]: usr/share/man/man3/wcstoimax.3.gz 
│                │                       ├ [2459]: usr/share/man/man3/wcstok.3.gz 
│                │                       ├ [2460]: usr/share/man/man3/wcstombs.3.gz 
│                │                       ├ [2461]: usr/share/man/man3/wcstoumax.3.gz 
│                │                       ├ [2462]: usr/share/man/man3/wcswidth.3.gz 
│                │                       ├ [2463]: usr/share/man/man3/wctob.3.gz 
│                │                       ├ [2464]: usr/share/man/man3/wctomb.3.gz 
│                │                       ├ [2465]: usr/share/man/man3/wctrans.3.gz 
│                │                       ├ [2466]: usr/share/man/man3/wctype.3.gz 
│                │                       ├ [2467]: usr/share/man/man3/wcwidth.3.gz 
│                │                       ├ [2468]: usr/share/man/man3/wmemchr.3.gz 
│                │                       ├ [2469]: usr/share/man/man3/wmemcmp.3.gz 
│                │                       ├ [2470]: usr/share/man/man3/wmemcpy.3.gz 
│                │                       ├ [2471]: usr/share/man/man3/wmemmove.3.gz 
│                │                       ├ [2472]: usr/share/man/man3/wmempcpy.3.gz 
│                │                       ├ [2473]: usr/share/man/man3/wmemset.3.gz 
│                │                       ├ [2474]: usr/share/man/man3/wordexp.3.gz 
│                │                       ├ [2475]: usr/share/man/man3/wordfree.3.gz 
│                │                       ├ [2476]: usr/share/man/man3/wprintf.3.gz 
│                │                       ├ [2477]: usr/share/man/man3/xcrypt.3.gz 
│                │                       ├ [2478]: usr/share/man/man3/xdecrypt.3.gz 
│                │                       ├ [2479]: usr/share/man/man3/xdr.3.gz 
│                │                       ├ [2480]: usr/share/man/man3/xdr_accepted_reply.3.gz 
│                │                       ├ [2481]: usr/share/man/man3/xdr_array.3.gz 
│                │                       ├ [2482]: usr/share/man/man3/xdr_authunix_parms.3.gz 
│                │                       ├ [2483]: usr/share/man/man3/xdr_bool.3.gz 
│                │                       ├ [2484]: usr/share/man/man3/xdr_bytes.3.gz 
│                │                       ├ [2485]: usr/share/man/man3/xdr_callhdr.3.gz 
│                │                       ├ [2486]: usr/share/man/man3/xdr_callmsg.3.gz 
│                │                       ├ [2487]: usr/share/man/man3/xdr_char.3.gz 
│                │                       ├ [2488]: usr/share/man/man3/xdr_destroy.3.gz 
│                │                       ├ [2489]: usr/share/man/man3/xdr_double.3.gz 
│                │                       ├ [2490]: usr/share/man/man3/xdr_enum.3.gz 
│                │                       ├ [2491]: usr/share/man/man3/xdr_float.3.gz 
│                │                       ├ [2492]: usr/share/man/man3/xdr_free.3.gz 
│                │                       ├ [2493]: usr/share/man/man3/xdr_getpos.3.gz 
│                │                       ├ [2494]: usr/share/man/man3/xdr_inline.3.gz 
│                │                       ├ [2495]: usr/share/man/man3/xdr_int.3.gz 
│                │                       ├ [2496]: usr/share/man/man3/xdr_long.3.gz 
│                │                       ├ [2497]: usr/share/man/man3/xdr_opaque.3.gz 
│                │                       ├ [2498]: usr/share/man/man3/xdr_opaque_auth.3.gz 
│                │                       ├ [2499]: usr/share/man/man3/xdr_pmap.3.gz 
│                │                       ├ [2500]: usr/share/man/man3/xdr_pmaplist.3.gz 
│                │                       ├ [2501]: usr/share/man/man3/xdr_pointer.3.gz 
│                │                       ├ [2502]: usr/share/man/man3/xdr_reference.3.gz 
│                │                       ├ [2503]: usr/share/man/man3/xdr_rejected_reply.3.gz 
│                │                       ├ [2504]: usr/share/man/man3/xdr_replymsg.3.gz 
│                │                       ├ [2505]: usr/share/man/man3/xdr_setpos.3.gz 
│                │                       ├ [2506]: usr/share/man/man3/xdr_short.3.gz 
│                │                       ├ [2507]: usr/share/man/man3/xdr_string.3.gz 
│                │                       ├ [2508]: usr/share/man/man3/xdr_u_char.3.gz 
│                │                       ├ [2509]: usr/share/man/man3/xdr_u_int.3.gz 
│                │                       ├ [2510]: usr/share/man/man3/xdr_u_long.3.gz 
│                │                       ├ [2511]: usr/share/man/man3/xdr_u_short.3.gz 
│                │                       ├ [2512]: usr/share/man/man3/xdr_union.3.gz 
│                │                       ├ [2513]: usr/share/man/man3/xdr_vector.3.gz 
│                │                       ├ [2514]: usr/share/man/man3/xdr_void.3.gz 
│                │                       ├ [2515]: usr/share/man/man3/xdr_wrapstring.3.gz 
│                │                       ├ [2516]: usr/share/man/man3/xdrmem_create.3.gz 
│                │                       ├ [2517]: usr/share/man/man3/xdrrec_create.3.gz 
│                │                       ├ [2518]: usr/share/man/man3/xdrrec_endofrecord.3.gz 
│                │                       ├ [2519]: usr/share/man/man3/xdrrec_eof.3.gz 
│                │                       ├ [2520]: usr/share/man/man3/xdrrec_skiprecord.3.gz 
│                │                       ├ [2521]: usr/share/man/man3/xdrstdio_create.3.gz 
│                │                       ├ [2522]: usr/share/man/man3/xencrypt.3.gz 
│                │                       ├ [2523]: usr/share/man/man3/xprt_register.3.gz 
│                │                       ├ [2524]: usr/share/man/man3/xprt_unregister.3.gz 
│                │                       ├ [2525]: usr/share/man/man3/y0.3.gz 
│                │                       ├ [2526]: usr/share/man/man3/y0f.3.gz 
│                │                       ├ [2527]: usr/share/man/man3/y0l.3.gz 
│                │                       ├ [2528]: usr/share/man/man3/y1.3.gz 
│                │                       ├ [2529]: usr/share/man/man3/y1f.3.gz 
│                │                       ├ [2530]: usr/share/man/man3/y1l.3.gz 
│                │                       ├ [2531]: usr/share/man/man3/yn.3.gz 
│                │                       ├ [2532]: usr/share/man/man3/ynf.3.gz 
│                │                       ├ [2533]: usr/share/man/man3/ynl.3.gz 
│                │                       ├ [2534]: usr/share/man/man3attr/gnu::aligned.3attr.gz 
│                │                       ├ [2535]: usr/share/man/man3attr/gnu::format.3attr.gz 
│                │                       ├ [2536]: usr/share/man/man3attr/intro.3attr.gz 
│                │                       ├ [2537]: usr/share/man/man3const/EOF.3const.gz 
│                │                       ├ [2538]: usr/share/man/man3const/EXIT_FAILURE.3const.gz 
│                │                       ├ [2539]: usr/share/man/man3const/EXIT_SUCCESS.3const.gz 
│                │                       ├ [2540]: usr/share/man/man3const/NULL.3const.gz 
│                │                       ├ [2541]: usr/share/man/man3const/PA_CHAR.3const.gz 
│                │                       ├ [2542]: usr/share/man/man3const/PA_DOUBLE.3const.gz 
│                │                       ├ [2543]: usr/share/man/man3const/PA_FLAG_LONG.3const.gz 
│                │                       ├ [2544]: usr/share/man/man3const/PA_FLAG_LONG_DOUBLE.3const.gz 
│                │                       ├ [2545]: usr/share/man/man3const/PA_FLAG_LONG_LONG.3const.gz 
│                │                       ├ [2546]: usr/share/man/man3const/PA_FLAG_PTR.3const.gz 
│                │                       ├ [2547]: usr/share/man/man3const/PA_FLAG_SHORT.3const.gz 
│                │                       ├ [2548]: usr/share/man/man3const/PA_FLOAT.3const.gz 
│                │                       ├ [2549]: usr/share/man/man3const/PA_INT.3const.gz 
│                │                       ├ [2550]: usr/share/man/man3const/PA_LAST.3const.gz 
│                │                       ├ [2551]: usr/share/man/man3const/PA_POINTER.3const.gz 
│                │                       ├ [2552]: usr/share/man/man3const/PA_STRING.3const.gz 
│                │                       ├ [2553]: usr/share/man/man3const/PA_WCHAR.3const.gz 
│                │                       ├ [2554]: usr/share/man/man3const/PA_WSTRING.3const.gz 
│                │                       ├ [2555]: usr/share/man/man3head/printf.h.3head.gz 
│                │                       ├ [2556]: usr/share/man/man3head/sysexits.h.3head.gz 
│                │                       ├ [2557]: usr/share/man/man3type/FILE.3type.gz 
│                │                       ├ [2558]: usr/share/man/man3type/aiocb.3type.gz 
│                │                       ├ [2559]: usr/share/man/man3type/blkcnt_t.3type.gz 
│                │                       ├ [2560]: usr/share/man/man3type/blksize_t.3type.gz 
│                │                       ├ [2561]: usr/share/man/man3type/cc_t.3type.gz 
│                │                       ├ [2562]: usr/share/man/man3type/clock_t.3type.gz 
│                │                       ├ [2563]: usr/share/man/man3type/clockid_t.3type.gz 
│                │                       ├ [2564]: usr/share/man/man3type/dev_t.3type.gz 
│                │                       ├ [2565]: usr/share/man/man3type/div_t.3type.gz 
│                │                       ├ [2566]: usr/share/man/man3type/double_t.3type.gz 
│                │                       ├ [2567]: usr/share/man/man3type/epoll_data.3type.gz 
│                │                       ├ [2568]: usr/share/man/man3type/epoll_data_t.3type.gz 
│                │                       ├ [2569]: usr/share/man/man3type/epoll_event.3type.gz 
│                │                       ├ [2570]: usr/share/man/man3type/fenv_t.3type.gz 
│                │                       ├ [2571]: usr/share/man/man3type/fexcept_t.3type.gz 
│                │                       ├ [2572]: usr/share/man/man3type/float_t.3type.gz 
│                │                       ├ [2573]: usr/share/man/man3type/gid_t.3type.gz 
│                │                       ├ [2574]: usr/share/man/man3type/id_t.3type.gz 
│                │                       ├ [2575]: usr/share/man/man3type/imaxdiv_t.3type.gz 
│                │                       ├ [2576]: usr/share/man/man3type/in6_addr.3type.gz 
│                │                       ├ [2577]: usr/share/man/man3type/in_addr.3type.gz 
│                │                       ├ [2578]: usr/share/man/man3type/in_addr_t.3type.gz 
│                │                       ├ [2579]: usr/share/man/man3type/in_port_t.3type.gz 
│                │                       ├ [2580]: usr/share/man/man3type/int16_t.3type.gz 
│                │                       ├ [2581]: usr/share/man/man3type/int32_t.3type.gz 
│                │                       ├ [2582]: usr/share/man/man3type/int64_t.3type.gz 
│                │                       ├ [2583]: usr/share/man/man3type/int8_t.3type.gz 
│                │                       ├ [2584]: usr/share/man/man3type/intN_t.3type.gz 
│                │                       ├ [2585]: usr/share/man/man3type/intmax_t.3type.gz 
│                │                       ├ [2586]: usr/share/man/man3type/intptr_t.3type.gz 
│                │                       ├ [2587]: usr/share/man/man3type/iovec.3type.gz 
│                │                       ├ [2588]: usr/share/man/man3type/itimerspec.3type.gz 
│                │                       ├ [2589]: usr/share/man/man3type/lconv.3type.gz 
│                │                       ├ [2590]: usr/share/man/man3type/ldiv_t.3type.gz 
│                │                       ├ [2591]: usr/share/man/man3type/lldiv_t.3type.gz 
│                │                       ├ [2592]: usr/share/man/man3type/locale_t.3type.gz 
│                │                       ├ [2593]: usr/share/man/man3type/loff_t.3type.gz 
│                │                       ├ [2594]: usr/share/man/man3type/mbstate_t.3type.gz 
│                │                       ├ [2595]: usr/share/man/man3type/mode_t.3type.gz 
│                │                       ├ [2596]: usr/share/man/man3type/off64_t.3type.gz 
│                │                       ├ [2597]: usr/share/man/man3type/off_t.3type.gz 
│                │                       ├ [2598]: usr/share/man/man3type/pid_t.3type.gz 
│                │                       ├ [2599]: usr/share/man/man3type/printf_arginfo_size_function.3type.gz 
│                │                       ├ [2600]: usr/share/man/man3type/printf_function.3type.gz 
│                │                       ├ [2601]: usr/share/man/man3type/printf_info.3type.gz 
│                │                       ├ [2602]: usr/share/man/man3type/printf_va_arg_function.3type.gz 
│                │                       ├ [2603]: usr/share/man/man3type/ptrdiff_t.3type.gz 
│                │                       ├ [2604]: usr/share/man/man3type/regex_t.3type.gz 
│                │                       ├ [2605]: usr/share/man/man3type/regmatch_t.3type.gz 
│                │                       ├ [2606]: usr/share/man/man3type/regoff_t.3type.gz 
│                │                       ├ [2607]: usr/share/man/man3type/rlim_t.3type.gz 
│                │                       ├ [2608]: usr/share/man/man3type/rlimit.3type.gz 
│                │                       ├ [2609]: usr/share/man/man3type/sa_family_t.3type.gz 
│                │                       ├ [2610]: usr/share/man/man3type/sigevent.3type.gz 
│                │                       ├ [2611]: usr/share/man/man3type/siginfo_t.3type.gz 
│                │                       ├ [2612]: usr/share/man/man3type/sigset_t.3type.gz 
│                │                       ├ [2613]: usr/share/man/man3type/sigval.3type.gz 
│                │                       ├ [2614]: usr/share/man/man3type/size_t.3type.gz 
│                │                       ├ [2615]: usr/share/man/man3type/sockaddr.3type.gz 
│                │                       ├ [2616]: usr/share/man/man3type/sockaddr_in.3type.gz 
│                │                       ├ [2617]: usr/share/man/man3type/sockaddr_in6.3type.gz 
│                │                       ├ [2618]: usr/share/man/man3type/sockaddr_storage.3type.gz 
│                │                       ├ [2619]: usr/share/man/man3type/sockaddr_un.3type.gz 
│                │                       ├ [2620]: usr/share/man/man3type/socklen_t.3type.gz 
│                │                       ├ [2621]: usr/share/man/man3type/speed_t.3type.gz 
│                │                       ├ [2622]: usr/share/man/man3type/ssize_t.3type.gz 
│                │                       ├ [2623]: usr/share/man/man3type/stat.3type.gz 
│                │                       ├ [2624]: usr/share/man/man3type/suseconds_t.3type.gz 
│                │                       ├ [2625]: usr/share/man/man3type/tcflag_t.3type.gz 
│                │                       ├ [2626]: usr/share/man/man3type/time_t.3type.gz 
│                │                       ├ [2627]: usr/share/man/man3type/timer_t.3type.gz 
│                │                       ├ [2628]: usr/share/man/man3type/timespec.3type.gz 
│                │                       ├ [2629]: usr/share/man/man3type/timeval.3type.gz 
│                │                       ├ [2630]: usr/share/man/man3type/tm.3type.gz 
│                │                       ├ [2631]: usr/share/man/man3type/uid_t.3type.gz 
│                │                       ├ [2632]: usr/share/man/man3type/uint16_t.3type.gz 
│                │                       ├ [2633]: usr/share/man/man3type/uint32_t.3type.gz 
│                │                       ├ [2634]: usr/share/man/man3type/uint64_t.3type.gz 
│                │                       ├ [2635]: usr/share/man/man3type/uint8_t.3type.gz 
│                │                       ├ [2636]: usr/share/man/man3type/uintN_t.3type.gz 
│                │                       ├ [2637]: usr/share/man/man3type/uintmax_t.3type.gz 
│                │                       ├ [2638]: usr/share/man/man3type/uintptr_t.3type.gz 
│                │                       ├ [2639]: usr/share/man/man3type/useconds_t.3type.gz 
│                │                       ├ [2640]: usr/share/man/man3type/va_list.3type.gz 
│                │                       ├ [2641]: usr/share/man/man3type/void.3type.gz 
│                │                       ├ [2642]: usr/share/man/man3type/wchar_t.3type.gz 
│                │                       ├ [2643]: usr/share/man/man3type/wint_t.3type.gz 
│                │                       ├ [2644]: usr/share/man/man4/cciss.4.gz 
│                │                       ├ [2645]: usr/share/man/man4/console_codes.4.gz 
│                │                       ├ [2646]: usr/share/man/man4/console_ioctl.4.gz 
│                │                       ├ [2647]: usr/share/man/man4/cpuid.4.gz 
│                │                       ├ [2648]: usr/share/man/man4/dsp56k.4.gz 
│                │                       ├ [2649]: usr/share/man/man4/fd.4.gz 
│                │                       ├ [2650]: usr/share/man/man4/full.4.gz 
│                │                       ├ [2651]: usr/share/man/man4/fuse.4.gz 
│                │                       ├ [2652]: usr/share/man/man4/hd.4.gz 
│                │                       ├ [2653]: usr/share/man/man4/hpsa.4.gz 
│                │                       ├ [2654]: usr/share/man/man4/initrd.4.gz 
│                │                       ├ [2655]: usr/share/man/man4/intro.4.gz 
│                │                       ├ [2656]: usr/share/man/man4/kmem.4.gz 
│                │                       ├ [2657]: usr/share/man/man4/lirc.4.gz 
│                │                       ├ [2658]: usr/share/man/man4/loop-control.4.gz 
│                │                       ├ [2659]: usr/share/man/man4/loop.4.gz 
│                │                       ├ [2660]: usr/share/man/man4/lp.4.gz 
│                │                       ├ [2661]: usr/share/man/man4/mem.4.gz 
│                │                       ├ [2662]: usr/share/man/man4/mouse.4.gz 
│                │                       ├ [2663]: usr/share/man/man4/msr.4.gz 
│                │                       ├ [2664]: usr/share/man/man4/null.4.gz 
│                │                       ├ [2665]: usr/share/man/man4/port.4.gz 
│                │                       ├ [2666]: usr/share/man/man4/ptmx.4.gz 
│                │                       ├ [2667]: usr/share/man/man4/pts.4.gz 
│                │                       ├ [2668]: usr/share/man/man4/ram.4.gz 
│                │                       ├ [2669]: usr/share/man/man4/random.4.gz 
│                │                       ├ [2670]: usr/share/man/man4/rtc.4.gz 
│                │                       ├ [2671]: usr/share/man/man4/sd.4.gz 
│                │                       ├ [2672]: usr/share/man/man4/sk98lin.4.gz 
│                │                       ├ [2673]: usr/share/man/man4/smartpqi.4.gz 
│                │                       ├ [2674]: usr/share/man/man4/st.4.gz 
│                │                       ├ [2675]: usr/share/man/man4/tty.4.gz 
│                │                       ├ [2676]: usr/share/man/man4/ttyS.4.gz 
│                │                       ├ [2677]: usr/share/man/man4/tty_ioctl.4.gz 
│                │                       ├ [2678]: usr/share/man/man4/urandom.4.gz 
│                │                       ├ [2679]: usr/share/man/man4/vcs.4.gz 
│                │                       ├ [2680]: usr/share/man/man4/vcsa.4.gz 
│                │                       ├ [2681]: usr/share/man/man4/veth.4.gz 
│                │                       ├ [2682]: usr/share/man/man4/wavelan.4.gz 
│                │                       ├ [2683]: usr/share/man/man4/zero.4.gz 
│                │                       ├ [2684]: usr/share/man/man5/acct.5.gz 
│                │                       ├ [2685]: usr/share/man/man5/charmap.5.gz 
│                │                       ├ [2686]: usr/share/man/man5/core.5.gz 
│                │                       ├ [2687]: usr/share/man/man5/dir_colors.5.gz 
│                │                       ├ [2688]: usr/share/man/man5/elf.5.gz 
│                │                       ├ [2689]: usr/share/man/man5/erofs.5.gz 
│                │                       ├ [2690]: usr/share/man/man5/filesystems.5.gz 
│                │                       ├ [2691]: usr/share/man/man5/fs.5.gz 
│                │                       ├ [2692]: usr/share/man/man5/ftpusers.5.gz 
│                │                       ├ [2693]: usr/share/man/man5/gai.conf.5.gz 
│                │                       ├ [2694]: usr/share/man/man5/group.5.gz 
│                │                       ├ [2695]: usr/share/man/man5/host.conf.5.gz 
│                │                       ├ [2696]: usr/share/man/man5/hosts.5.gz 
│                │                       ├ [2697]: usr/share/man/man5/hosts.equiv.5.gz 
│                │                       ├ [2698]: usr/share/man/man5/intro.5.gz 
│                │                       ├ [2699]: usr/share/man/man5/issue.5.gz 
│                │                       ├ [2700]: usr/share/man/man5/locale.5.gz 
│                │                       ├ [2701]: usr/share/man/man5/motd.5.gz 
│                │                       ├ [2702]: usr/share/man/man5/networks.5.gz 
│                │                       ├ [2703]: usr/share/man/man5/nologin.5.gz 
│                │                       ├ [2704]: usr/share/man/man5/nscd.conf.5.gz 
│                │                       ├ [2705]: usr/share/man/man5/nss.5.gz 
│                │                       ├ [2706]: usr/share/man/man5/nsswitch.conf.5.gz 
│                │                       ├ [2707]: usr/share/man/man5/passwd.5.gz 
│                │                       ├ [2708]: usr/share/man/man5/proc.5.gz 
│                │                       ├ [2709]: usr/share/man/man5/proc_apm.5.gz 
│                │                       ├ [2710]: usr/share/man/man5/proc_buddyinfo.5.gz 
│                │                       ├ [2711]: usr/share/man/man5/proc_bus.5.gz 
│                │                       ├ [2712]: usr/share/man/man5/proc_cgroups.5.gz 
│                │                       ├ [2713]: usr/share/man/man5/proc_cmdline.5.gz 
│                │                       ├ [2714]: usr/share/man/man5/proc_config.gz.5.gz 
│                │                       ├ [2715]: usr/share/man/man5/proc_cpuinfo.5.gz 
│                │                       ├ [2716]: usr/share/man/man5/proc_crypto.5.gz 
│                │                       ├ [2717]: usr/share/man/man5/proc_devices.5.gz 
│                │                       ├ [2718]: usr/share/man/man5/proc_diskstats.5.gz 
│                │                       ├ [2719]: usr/share/man/man5/proc_dma.5.gz 
│                │                       ├ [2720]: usr/share/man/man5/proc_driver.5.gz 
│                │                       ├ [2721]: usr/share/man/man5/proc_execdomains.5.gz 
│                │                       ├ [2722]: usr/share/man/man5/proc_fb.5.gz 
│                │                       ├ [2723]: usr/share/man/man5/proc_filesystems.5.gz 
│                │                       ├ [2724]: usr/share/man/man5/proc_fs.5.gz 
│                │                       ├ [2725]: usr/share/man/man5/proc_ide.5.gz 
│                │                       ├ [2726]: usr/share/man/man5/proc_interrupts.5.gz 
│                │                       ├ [2727]: usr/share/man/man5/proc_iomem.5.gz 
│                │                       ├ [2728]: usr/share/man/man5/proc_ioports.5.gz 
│                │                       ├ [2729]: usr/share/man/man5/proc_kallsyms.5.gz 
│                │                       ├ [2730]: usr/share/man/man5/proc_kcore.5.gz 
│                │                       ├ [2731]: usr/share/man/man5/proc_key-users.5.gz 
│                │                       ├ [2732]: usr/share/man/man5/proc_keys.5.gz 
│                │                       ├ [2733]: usr/share/man/man5/proc_kmsg.5.gz 
│                │                       ├ [2734]: usr/share/man/man5/proc_kpagecgroup.5.gz 
│                │                       ├ [2735]: usr/share/man/man5/proc_kpagecount.5.gz 
│                │                       ├ [2736]: usr/share/man/man5/proc_kpageflags.5.gz 
│                │                       ├ [2737]: usr/share/man/man5/proc_ksyms.5.gz 
│                │                       ├ [2738]: usr/share/man/man5/proc_loadavg.5.gz 
│                │                       ├ [2739]: usr/share/man/man5/proc_locks.5.gz 
│                │                       ├ [2740]: usr/share/man/man5/proc_malloc.5.gz 
│                │                       ├ [2741]: usr/share/man/man5/proc_meminfo.5.gz 
│                │                       ├ [2742]: usr/share/man/man5/proc_modules.5.gz 
│                │                       ├ [2743]: usr/share/man/man5/proc_mounts.5.gz 
│                │                       ├ [2744]: usr/share/man/man5/proc_mtrr.5.gz 
│                │                       ├ [2745]: usr/share/man/man5/proc_net.5.gz 
│                │                       ├ [2746]: usr/share/man/man5/proc_partitions.5.gz 
│                │                       ├ [2747]: usr/share/man/man5/proc_pci.5.gz 
│                │                       ├ [2748]: usr/share/man/man5/proc_pid.5.gz 
│                │                       ├ [2749]: usr/share/man/man5/proc_pid_attr.5.gz 
│                │                       ├ [2750]: usr/share/man/man5/proc_pid_autogroup.5.gz 
│                │                       ├ [2751]: usr/share/man/man5/proc_pid_auxv.5.gz 
│                │                       ├ [2752]: usr/share/man/man5/proc_pid_cgroup.5.gz 
│                │                       ├ [2753]: usr/share/man/man5/proc_pid_clear_refs.5.gz 
│                │                       ├ [2754]: usr/share/man/man5/proc_pid_cmdline.5.gz 
│                │                       ├ [2755]: usr/share/man/man5/proc_pid_comm.5.gz 
│                │                       ├ [2756]: usr/share/man/man5/proc_pid_coredump_filter.5.gz 
│                │                       ├ [2757]: usr/share/man/man5/proc_pid_cpuset.5.gz 
│                │                       ├ [2758]: usr/share/man/man5/proc_pid_cwd.5.gz 
│                │                       ├ [2759]: usr/share/man/man5/proc_pid_environ.5.gz 
│                │                       ├ [2760]: usr/share/man/man5/proc_pid_exe.5.gz 
│                │                       ├ [2761]: usr/share/man/man5/proc_pid_fd.5.gz 
│                │                       ├ [2762]: usr/share/man/man5/proc_pid_fdinfo.5.gz 
│                │                       ├ [2763]: usr/share/man/man5/proc_pid_gid_map.5.gz 
│                │                       ├ [2764]: usr/share/man/man5/proc_pid_io.5.gz 
│                │                       ├ [2765]: usr/share/man/man5/proc_pid_limits.5.gz 
│                │                       ├ [2766]: usr/share/man/man5/proc_pid_map_files.5.gz 
│                │                       ├ [2767]: usr/share/man/man5/proc_pid_maps.5.gz 
│                │                       ├ [2768]: usr/share/man/man5/proc_pid_mem.5.gz 
│                │                       ├ [2769]: usr/share/man/man5/proc_pid_mountinfo.5.gz 
│                │                       ├ [2770]: usr/share/man/man5/proc_pid_mounts.5.gz 
│                │                       ├ [2771]: usr/share/man/man5/proc_pid_mountstats.5.gz 
│                │                       ├ [2772]: usr/share/man/man5/proc_pid_net.5.gz 
│                │                       ├ [2773]: usr/share/man/man5/proc_pid_ns.5.gz 
│                │                       ├ [2774]: usr/share/man/man5/proc_pid_numa_maps.5.gz 
│                │                       ├ [2775]: usr/share/man/man5/proc_pid_oom_adj.5.gz 
│                │                       ├ [2776]: usr/share/man/man5/proc_pid_oom_score.5.gz 
│                │                       ├ [2777]: usr/share/man/man5/proc_pid_oom_score_adj.5.gz 
│                │                       ├ [2778]: usr/share/man/man5/proc_pid_pagemap.5.gz 
│                │                       ├ [2779]: usr/share/man/man5/proc_pid_personality.5.gz 
│                │                       ├ [2780]: usr/share/man/man5/proc_pid_projid_map.5.gz 
│                │                       ├ [2781]: usr/share/man/man5/proc_pid_root.5.gz 
│                │                       ├ [2782]: usr/share/man/man5/proc_pid_seccomp.5.gz 
│                │                       ├ [2783]: usr/share/man/man5/proc_pid_setgroups.5.gz 
│                │                       ├ [2784]: usr/share/man/man5/proc_pid_smaps.5.gz 
│                │                       ├ [2785]: usr/share/man/man5/proc_pid_stack.5.gz 
│                │                       ├ [2786]: usr/share/man/man5/proc_pid_stat.5.gz 
│                │                       ├ [2787]: usr/share/man/man5/proc_pid_statm.5.gz 
│                │                       ├ [2788]: usr/share/man/man5/proc_pid_status.5.gz 
│                │                       ├ [2789]: usr/share/man/man5/proc_pid_syscall.5.gz 
│                │                       ├ [2790]: usr/share/man/man5/proc_pid_task.5.gz 
│                │                       ├ [2791]: usr/share/man/man5/proc_pid_timers.5.gz 
│                │                       ├ [2792]: usr/share/man/man5/proc_pid_timerslack_ns.5.gz 
│                │                       ├ [2793]: usr/share/man/man5/proc_pid_uid_map.5.gz 
│                │                       ├ [2794]: usr/share/man/man5/proc_pid_wchan.5.gz 
│                │                       ├ [2795]: usr/share/man/man5/proc_profile.5.gz 
│                │                       ├ [2796]: usr/share/man/man5/proc_scsi.5.gz 
│                │                       ├ [2797]: usr/share/man/man5/proc_self.5.gz 
│                │                       ├ [2798]: usr/share/man/man5/proc_slabinfo.5.gz 
│                │                       ├ [2799]: usr/share/man/man5/proc_stat.5.gz 
│                │                       ├ [2800]: usr/share/man/man5/proc_swaps.5.gz 
│                │                       ├ [2801]: usr/share/man/man5/proc_sys.5.gz 
│                │                       ├ [2802]: usr/share/man/man5/proc_sys_abi.5.gz 
│                │                       ├ [2803]: usr/share/man/man5/proc_sys_debug.5.gz 
│                │                       ├ [2804]: usr/share/man/man5/proc_sys_dev.5.gz 
│                │                       ├ [2805]: usr/share/man/man5/proc_sys_fs.5.gz 
│                │                       ├ [2806]: usr/share/man/man5/proc_sys_kernel.5.gz 
│                │                       ├ [2807]: usr/share/man/man5/proc_sys_net.5.gz 
│                │                       ├ [2808]: usr/share/man/man5/proc_sys_proc.5.gz 
│                │                       ├ [2809]: usr/share/man/man5/proc_sys_sunrpc.5.gz 
│                │                       ├ [2810]: usr/share/man/man5/proc_sys_user.5.gz 
│                │                       ├ [2811]: usr/share/man/man5/proc_sys_vm.5.gz 
│                │                       ├ [2812]: usr/share/man/man5/proc_sysrq-trigger.5.gz 
│                │                       ├ [2813]: usr/share/man/man5/proc_sysvipc.5.gz 
│                │                       ├ [2814]: usr/share/man/man5/proc_thread-self.5.gz 
│                │                       ├ [2815]: usr/share/man/man5/proc_tid.5.gz 
│                │                       ├ [2816]: usr/share/man/man5/proc_tid_children.5.gz 
│                │                       ├ [2817]: usr/share/man/man5/proc_timer_list.5.gz 
│                │                       ├ [2818]: usr/share/man/man5/proc_timer_stats.5.gz 
│                │                       ├ [2819]: usr/share/man/man5/proc_tty.5.gz 
│                │                       ├ [2820]: usr/share/man/man5/proc_uptime.5.gz 
│                │                       ├ [2821]: usr/share/man/man5/proc_version.5.gz 
│                │                       ├ [2822]: usr/share/man/man5/proc_vmstat.5.gz 
│                │                       ├ [2823]: usr/share/man/man5/proc_zoneinfo.5.gz 
│                │                       ├ [2824]: usr/share/man/man5/procfs.5.gz 
│                │                       ├ [2825]: usr/share/man/man5/protocols.5.gz 
│                │                       ├ [2826]: usr/share/man/man5/repertoiremap.5.gz 
│                │                       ├ [2827]: usr/share/man/man5/resolv.conf.5.gz 
│                │                       ├ [2828]: usr/share/man/man5/resolver.5.gz 
│                │                       ├ [2829]: usr/share/man/man5/rpc.5.gz 
│                │                       ├ [2830]: usr/share/man/man5/securetty.5.gz 
│                │                       ├ [2831]: usr/share/man/man5/services.5.gz 
│                │                       ├ [2832]: usr/share/man/man5/shells.5.gz 
│                │                       ├ [2833]: usr/share/man/man5/slabinfo.5.gz 
│                │                       ├ [2834]: usr/share/man/man5/sysfs.5.gz 
│                │                       ├ [2835]: usr/share/man/man5/termcap.5.gz 
│                │                       ├ [2836]: usr/share/man/man5/tmpfs.5.gz 
│                │                       ├ [2837]: usr/share/man/man5/ttytype.5.gz 
│                │                       ├ [2838]: usr/share/man/man5/utmp.5.gz 
│                │                       ├ [2839]: usr/share/man/man5/utmpx.5.gz 
│                │                       ├ [2840]: usr/share/man/man5/wtmp.5.gz 
│                │                       ├ [2841]: usr/share/man/man6/intro.6.gz 
│                │                       ├ [2842]: usr/share/man/man7/address_families.7.gz 
│                │                       ├ [2843]: usr/share/man/man7/aio.7.gz 
│                │                       ├ [2844]: usr/share/man/man7/armscii-8.7.gz 
│                │                       ├ [2845]: usr/share/man/man7/arp.7.gz 
│                │                       ├ [2846]: usr/share/man/man7/ascii.7.gz 
│                │                       ├ [2847]: usr/share/man/man7/attributes.7.gz 
│                │                       ├ [2848]: usr/share/man/man7/boot.7.gz 
│                │                       ├ [2849]: usr/share/man/man7/bootparam.7.gz 
│                │                       ├ [2850]: usr/share/man/man7/bpf-helpers.7.gz 
│                │                       ├ [2851]: usr/share/man/man7/capabilities.7.gz 
│                │                       ├ [2852]: usr/share/man/man7/cgroup_namespaces.7.gz 
│                │                       ├ [2853]: usr/share/man/man7/cgroups.7.gz 
│                │                       ├ [2854]: usr/share/man/man7/charsets.7.gz 
│                │                       ├ [2855]: usr/share/man/man7/complex.7.gz 
│                │                       ├ [2856]: usr/share/man/man7/cp1251.7.gz 
│                │                       ├ [2857]: usr/share/man/man7/cp1252.7.gz 
│                │                       ├ [2858]: usr/share/man/man7/cpuset.7.gz 
│                │                       ├ [2859]: usr/share/man/man7/credentials.7.gz 
│                │                       ├ [2860]: usr/share/man/man7/ddp.7.gz 
│                │                       ├ [2861]: usr/share/man/man7/environ.7.gz 
│                │                       ├ [2862]: usr/share/man/man7/epoll.7.gz 
│                │                       ├ [2863]: usr/share/man/man7/fanotify.7.gz 
│                │                       ├ [2864]: usr/share/man/man7/feature_test_macros.7.gz 
│                │                       ├ [2865]: usr/share/man/man7/fifo.7.gz 
│                │                       ├ [2866]: usr/share/man/man7/futex.7.gz 
│                │                       ├ [2867]: usr/share/man/man7/glibc.7.gz 
│                │                       ├ [2868]: usr/share/man/man7/glob.7.gz 
│                │                       ├ [2869]: usr/share/man/man7/hier.7.gz 
│                │                       ├ [2870]: usr/share/man/man7/hostname.7.gz 
│                │                       ├ [2871]: usr/share/man/man7/icmp.7.gz 
│                │                       ├ [2872]: usr/share/man/man7/inode.7.gz 
│                │                       ├ [2873]: usr/share/man/man7/inotify.7.gz 
│                │                       ├ [2874]: usr/share/man/man7/intro.7.gz 
│                │                       ├ [2875]: usr/share/man/man7/ip.7.gz 
│                │                       ├ [2876]: usr/share/man/man7/ipc_namespaces.7.gz 
│                │                       ├ [2877]: usr/share/man/man7/ipv6.7.gz 
│                │                       ├ [2878]: usr/share/man/man7/iso-8859-1.7.gz 
│                │                       ├ [2879]: usr/share/man/man7/iso-8859-10.7.gz 
│                │                       ├ [2880]: usr/share/man/man7/iso-8859-11.7.gz 
│                │                       ├ [2881]: usr/share/man/man7/iso-8859-13.7.gz 
│                │                       ├ [2882]: usr/share/man/man7/iso-8859-14.7.gz 
│                │                       ├ [2883]: usr/share/man/man7/iso-8859-15.7.gz 
│                │                       ├ [2884]: usr/share/man/man7/iso-8859-16.7.gz 
│                │                       ├ [2885]: usr/share/man/man7/iso-8859-2.7.gz 
│                │                       ├ [2886]: usr/share/man/man7/iso-8859-3.7.gz 
│                │                       ├ [2887]: usr/share/man/man7/iso-8859-4.7.gz 
│                │                       ├ [2888]: usr/share/man/man7/iso-8859-5.7.gz 
│                │                       ├ [2889]: usr/share/man/man7/iso-8859-6.7.gz 
│                │                       ├ [2890]: usr/share/man/man7/iso-8859-7.7.gz 
│                │                       ├ [2891]: usr/share/man/man7/iso-8859-8.7.gz 
│                │                       ├ [2892]: usr/share/man/man7/iso-8859-9.7.gz 
│                │                       ├ [2893]: usr/share/man/man7/iso_8859-1.7.gz 
│                │                       ├ [2894]: usr/share/man/man7/iso_8859-10.7.gz 
│                │                       ├ [2895]: usr/share/man/man7/iso_8859-11.7.gz 
│                │                       ├ [2896]: usr/share/man/man7/iso_8859-13.7.gz 
│                │                       ├ [2897]: usr/share/man/man7/iso_8859-14.7.gz 
│                │                       ├ [2898]: usr/share/man/man7/iso_8859-15.7.gz 
│                │                       ├ [2899]: usr/share/man/man7/iso_8859-16.7.gz 
│                │                       ├ [2900]: usr/share/man/man7/iso_8859-2.7.gz 
│                │                       ├ [2901]: usr/share/man/man7/iso_8859-3.7.gz 
│                │                       ├ [2902]: usr/share/man/man7/iso_8859-4.7.gz 
│                │                       ├ [2903]: usr/share/man/man7/iso_8859-5.7.gz 
│                │                       ├ [2904]: usr/share/man/man7/iso_8859-6.7.gz 
│                │                       ├ [2905]: usr/share/man/man7/iso_8859-7.7.gz 
│                │                       ├ [2906]: usr/share/man/man7/iso_8859-8.7.gz 
│                │                       ├ [2907]: usr/share/man/man7/iso_8859-9.7.gz 
│                │                       ├ [2908]: usr/share/man/man7/iso_8859_1.7.gz 
│                │                       ├ [2909]: usr/share/man/man7/iso_8859_10.7.gz 
│                │                       ├ [2910]: usr/share/man/man7/iso_8859_11.7.gz 
│                │                       ├ [2911]: usr/share/man/man7/iso_8859_13.7.gz 
│                │                       ├ [2912]: usr/share/man/man7/iso_8859_14.7.gz 
│                │                       ├ [2913]: usr/share/man/man7/iso_8859_15.7.gz 
│                │                       ├ [2914]: usr/share/man/man7/iso_8859_16.7.gz 
│                │                       ├ [2915]: usr/share/man/man7/iso_8859_2.7.gz 
│                │                       ├ [2916]: usr/share/man/man7/iso_8859_3.7.gz 
│                │                       ├ [2917]: usr/share/man/man7/iso_8859_4.7.gz 
│                │                       ├ [2918]: usr/share/man/man7/iso_8859_5.7.gz 
│                │                       ├ [2919]: usr/share/man/man7/iso_8859_6.7.gz 
│                │                       ├ [2920]: usr/share/man/man7/iso_8859_7.7.gz 
│                │                       ├ [2921]: usr/share/man/man7/iso_8859_8.7.gz 
│                │                       ├ [2922]: usr/share/man/man7/iso_8859_9.7.gz 
│                │                       ├ [2923]: usr/share/man/man7/kernel_lockdown.7.gz 
│                │                       ├ [2924]: usr/share/man/man7/keyrings.7.gz 
│                │                       ├ [2925]: usr/share/man/man7/koi8-r.7.gz 
│                │                       ├ [2926]: usr/share/man/man7/koi8-u.7.gz 
│                │                       ├ [2927]: usr/share/man/man7/landlock.7.gz 
│                │                       ├ [2928]: usr/share/man/man7/latin1.7.gz 
│                │                       ├ [2929]: usr/share/man/man7/latin10.7.gz 
│                │                       ├ [2930]: usr/share/man/man7/latin2.7.gz 
│                │                       ├ [2931]: usr/share/man/man7/latin3.7.gz 
│                │                       ├ [2932]: usr/share/man/man7/latin4.7.gz 
│                │                       ├ [2933]: usr/share/man/man7/latin5.7.gz 
│                │                       ├ [2934]: usr/share/man/man7/latin6.7.gz 
│                │                       ├ [2935]: usr/share/man/man7/latin7.7.gz 
│                │                       ├ [2936]: usr/share/man/man7/latin8.7.gz 
│                │                       ├ [2937]: usr/share/man/man7/latin9.7.gz 
│                │                       ├ [2938]: usr/share/man/man7/libc.7.gz 
│                │                       ├ [2939]: usr/share/man/man7/locale.7.gz 
│                │                       ├ [2940]: usr/share/man/man7/mailaddr.7.gz 
│                │                       ├ [2941]: usr/share/man/man7/math_error.7.gz 
│                │                       ├ [2942]: usr/share/man/man7/mctp.7.gz 
│                │                       ├ [2943]: usr/share/man/man7/mount_namespaces.7.gz 
│                │                       ├ [2944]: usr/share/man/man7/mq_overview.7.gz 
│                │                       ├ [2945]: usr/share/man/man7/namespaces.7.gz 
│                │                       ├ [2946]: usr/share/man/man7/netdevice.7.gz 
│                │                       ├ [2947]: usr/share/man/man7/netlink.7.gz 
│                │                       ├ [2948]: usr/share/man/man7/network_namespaces.7.gz 
│                │                       ├ [2949]: usr/share/man/man7/nptl.7.gz 
│                │                       ├ [2950]: usr/share/man/man7/numa.7.gz 
│                │                       ├ [2951]: usr/share/man/man7/operator.7.gz 
│                │                       ├ [2952]: usr/share/man/man7/packet.7.gz 
│                │                       ├ [2953]: usr/share/man/man7/path_resolution.7.gz 
│                │                       ├ [2954]: usr/share/man/man7/pathname.7.gz 
│                │                       ├ [2955]: usr/share/man/man7/persistent-keyring.7.gz 
│                │                       ├ [2956]: usr/share/man/man7/pid_namespaces.7.gz 
│                │                       ├ [2957]: usr/share/man/man7/pipe.7.gz 
│                │                       ├ [2958]: usr/share/man/man7/pkeys.7.gz 
│                │                       ├ [2959]: usr/share/man/man7/posixoptions.7.gz 
│                │                       ├ [2960]: usr/share/man/man7/precedence.7.gz 
│                │                       ├ [2961]: usr/share/man/man7/process-keyring.7.gz 
│                │                       ├ [2962]: usr/share/man/man7/pthreads.7.gz 
│                │                       ├ [2963]: usr/share/man/man7/pty.7.gz 
│                │                       ├ [2964]: usr/share/man/man7/queue.7.gz 
│                │                       ├ [2965]: usr/share/man/man7/random.7.gz 
│                │                       ├ [2966]: usr/share/man/man7/raw.7.gz 
│                │                       ├ [2967]: usr/share/man/man7/regex.7.gz 
│                │                       ├ [2968]: usr/share/man/man7/rtld-audit.7.gz 
│                │                       ├ [2969]: usr/share/man/man7/rtnetlink.7.gz 
│                │                       ├ [2970]: usr/share/man/man7/sched.7.gz 
│                │                       ├ [2971]: usr/share/man/man7/sem_overview.7.gz 
│                │                       ├ [2972]: usr/share/man/man7/session-keyring.7.gz 
│                │                       ├ [2973]: usr/share/man/man7/shm_overview.7.gz 
│                │                       ├ [2974]: usr/share/man/man7/sigevent.7.gz 
│                │                       ├ [2975]: usr/share/man/man7/signal-safety.7.gz 
│                │                       ├ [2976]: usr/share/man/man7/signal.7.gz 
│                │                       ├ [2977]: usr/share/man/man7/sock_diag.7.gz 
│                │                       ├ [2978]: usr/share/man/man7/socket.7.gz 
│                │                       ├ [2979]: usr/share/man/man7/spufs.7.gz 
│                │                       ├ [2980]: usr/share/man/man7/standards.7.gz 
│                │                       ├ [2981]: usr/share/man/man7/string_copying.7.gz 
│                │                       ├ [2982]: usr/share/man/man7/suffixes.7.gz 
│                │                       ├ [2983]: usr/share/man/man7/svipc.7.gz 
│                │                       ├ [2984]: usr/share/man/man7/symlink.7.gz 
│                │                       ├ [2985]: usr/share/man/man7/system_data_types.7.gz 
│                │                       ├ [2986]: usr/share/man/man7/sysvipc.7.gz 
│                │                       ├ [2987]: usr/share/man/man7/tcp.7.gz 
│                │                       ├ [2988]: usr/share/man/man7/termio.7.gz 
│                │                       ├ [2989]: usr/share/man/man7/thread-keyring.7.gz 
│                │                       ├ [2990]: usr/share/man/man7/time.7.gz 
│                │                       ├ [2991]: usr/share/man/man7/time_namespaces.7.gz 
│                │                       ├ [2992]: usr/share/man/man7/tis-620.7.gz 
│                │                       ├ [2993]: usr/share/man/man7/udp.7.gz 
│                │                       ├ [2994]: usr/share/man/man7/udplite.7.gz 
│                │                       ├ [2995]: usr/share/man/man7/unicode.7.gz 
│                │                       ├ [2996]: usr/share/man/man7/units.7.gz 
│                │                       ├ [2997]: usr/share/man/man7/unix.7.gz 
│                │                       ├ [2998]: usr/share/man/man7/uri.7.gz 
│                │                       ├ [2999]: usr/share/man/man7/url.7.gz 
│                │                       ├ [3000]: usr/share/man/man7/urn.7.gz 
│                │                       ├ [3001]: usr/share/man/man7/user-keyring.7.gz 
│                │                       ├ [3002]: usr/share/man/man7/user-session-keyring.7.gz 
│                │                       ├ [3003]: usr/share/man/man7/user_namespaces.7.gz 
│                │                       ├ [3004]: usr/share/man/man7/utf-8.7.gz 
│                │                       ├ [3005]: usr/share/man/man7/utf8.7.gz 
│                │                       ├ [3006]: usr/share/man/man7/uts_namespaces.7.gz 
│                │                       ├ [3007]: usr/share/man/man7/vdso.7.gz 
│                │                       ├ [3008]: usr/share/man/man7/vsock.7.gz 
│                │                       ├ [3009]: usr/share/man/man7/x25.7.gz 
│                │                       ├ [3010]: usr/share/man/man7/xattr.7.gz 
│                │                       ├ [3011]: usr/share/man/man8/iconvconfig.8.gz 
│                │                       ├ [3012]: usr/share/man/man8/intro.8.gz 
│                │                       ├ [3013]: usr/share/man/man8/ld-linux.8.gz 
│                │                       ├ [3014]: usr/share/man/man8/ld-linux.so.8.gz 
│                │                       ├ [3015]: usr/share/man/man8/ld.so.8.gz 
│                │                       ├ [3016]: usr/share/man/man8/ldconfig.8.gz 
│                │                       ├ [3017]: usr/share/man/man8/nscd.8.gz 
│                │                       ╰ [3018]: usr/share/man/man8/sln.8.gz 
│                ├ [40] ╭ ID            : mandoc@1.14.6-r13 
│                │      ├ Name          : mandoc 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/mandoc@1.14.6-r13?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 74bb57c3e89338bb 
│                │      ├ Version       : 1.14.6-r13 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : mandoc 
│                │      ├ SrcVersion    : 1.14.6-r13 
│                │      ├ Licenses       ─ [0]: ISC 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: musl@1.2.5-r21 
│                │      │                ╰ [1]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:8bcdf6860fb55e4a22198192bf306c3ad5fb3e4f 
│                │      ╰ InstalledFiles ╭ [0]: usr/bin/demandoc 
│                │                       ├ [1]: usr/bin/man 
│                │                       ├ [2]: usr/bin/mandoc 
│                │                       ╰ [3]: usr/lib/libmandoc.so 
│                ├ [41] ╭ ID            : mc@4.8.33-r2 
│                │      ├ Name          : mc 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/mc@4.8.33-r2?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 8decbf07b7224b1b 
│                │      ├ Version       : 4.8.33-r2 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : mc 
│                │      ├ SrcVersion    : 4.8.33-r2 
│                │      ├ Licenses       ─ [0]: GPL-3.0-or-later 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: e2fsprogs-libs@1.47.3-r0 
│                │      │                ├ [1]: glib@2.86.2-r1 
│                │      │                ├ [2]: gpm-libs@1.20.7-r6 
│                │      │                ├ [3]: libintl@0.24.1-r1 
│                │      │                ├ [4]: libssh2@1.11.1-r1 
│                │      │                ├ [5]: musl@1.2.5-r21 
│                │      │                ╰ [6]: slang@2.3.3-r3 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:a3f1847a619ef084a885b917f210a222ccbd45d7 
│                │      ╰ InstalledFiles ╭ [0]  : etc/mc/edit.indent.rc 
│                │                       ├ [1]  : etc/mc/filehighlight.ini 
│                │                       ├ [2]  : etc/mc/mc.default.keymap 
│                │                       ├ [3]  : etc/mc/mc.emacs.keymap 
│                │                       ├ [4]  : etc/mc/mc.ext.ini 
│                │                       ├ [5]  : etc/mc/mc.keymap 
│                │                       ├ [6]  : etc/mc/mc.menu 
│                │                       ├ [7]  : etc/mc/mc.vim.keymap 
│                │                       ├ [8]  : etc/mc/mcedit.menu 
│                │                       ├ [9]  : etc/mc/sfs.ini 
│                │                       ├ [10] : usr/bin/mc 
│                │                       ├ [11] : usr/bin/mcdiff 
│                │                       ├ [12] : usr/bin/mcedit 
│                │                       ├ [13] : usr/bin/mcview 
│                │                       ├ [14] : usr/lib/mc/cons.saver 
│                │                       ├ [15] : usr/lib/mc/mc-wrapper.csh 
│                │                       ├ [16] : usr/lib/mc/mc-wrapper.sh 
│                │                       ├ [17] : usr/lib/mc/mc.csh 
│                │                       ├ [18] : usr/lib/mc/mc.sh 
│                │                       ├ [19] : usr/lib/mc/ext.d/archive.sh 
│                │                       ├ [20] : usr/lib/mc/ext.d/doc.sh 
│                │                       ├ [21] : usr/lib/mc/ext.d/image.sh 
│                │                       ├ [22] : usr/lib/mc/ext.d/misc.sh 
│                │                       ├ [23] : usr/lib/mc/ext.d/package.sh 
│                │                       ├ [24] : usr/lib/mc/ext.d/sound.sh 
│                │                       ├ [25] : usr/lib/mc/ext.d/text.sh 
│                │                       ├ [26] : usr/lib/mc/ext.d/video.sh 
│                │                       ├ [27] : usr/lib/mc/ext.d/web.sh 
│                │                       ├ [28] : usr/lib/mc/extfs.d/a+ 
│                │                       ├ [29] : usr/lib/mc/extfs.d/apt+ 
│                │                       ├ [30] : usr/lib/mc/extfs.d/audio 
│                │                       ├ [31] : usr/lib/mc/extfs.d/bpp 
│                │                       ├ [32] : usr/lib/mc/extfs.d/changesetfs 
│                │                       ├ [33] : usr/lib/mc/extfs.d/deb 
│                │                       ├ [34] : usr/lib/mc/extfs.d/deba 
│                │                       ├ [35] : usr/lib/mc/extfs.d/debd 
│                │                       ├ [36] : usr/lib/mc/extfs.d/dpkg+ 
│                │                       ├ [37] : usr/lib/mc/extfs.d/gitfs+ 
│                │                       ├ [38] : usr/lib/mc/extfs.d/hp48+ 
│                │                       ├ [39] : usr/lib/mc/extfs.d/iso9660 
│                │                       ├ [40] : usr/lib/mc/extfs.d/lslR 
│                │                       ├ [41] : usr/lib/mc/extfs.d/mailfs 
│                │                       ├ [42] : usr/lib/mc/extfs.d/patchfs 
│                │                       ├ [43] : usr/lib/mc/extfs.d/patchsetfs 
│                │                       ├ [44] : usr/lib/mc/extfs.d/rpm 
│                │                       ├ [45] : usr/lib/mc/extfs.d/rpms+ 
│                │                       ├ [46] : usr/lib/mc/extfs.d/s3+ 
│                │                       ├ [47] : usr/lib/mc/extfs.d/torrent 
│                │                       ├ [48] : usr/lib/mc/extfs.d/trpm 
│                │                       ├ [49] : usr/lib/mc/extfs.d/u7z 
│                │                       ├ [50] : usr/lib/mc/extfs.d/uace 
│                │                       ├ [51] : usr/lib/mc/extfs.d/ualz 
│                │                       ├ [52] : usr/lib/mc/extfs.d/uar 
│                │                       ├ [53] : usr/lib/mc/extfs.d/uarc 
│                │                       ├ [54] : usr/lib/mc/extfs.d/uarj 
│                │                       ├ [55] : usr/lib/mc/extfs.d/uc1541 
│                │                       ├ [56] : usr/lib/mc/extfs.d/ucab 
│                │                       ├ [57] : usr/lib/mc/extfs.d/uha 
│                │                       ├ [58] : usr/lib/mc/extfs.d/ulha 
│                │                       ├ [59] : usr/lib/mc/extfs.d/ulib 
│                │                       ├ [60] : usr/lib/mc/extfs.d/unar 
│                │                       ├ [61] : usr/lib/mc/extfs.d/urar 
│                │                       ├ [62] : usr/lib/mc/extfs.d/uwim 
│                │                       ├ [63] : usr/lib/mc/extfs.d/uzip 
│                │                       ├ [64] : usr/lib/mc/extfs.d/uzoo 
│                │                       ├ [65] : usr/lib/mc/shell/append 
│                │                       ├ [66] : usr/lib/mc/shell/chmod 
│                │                       ├ [67] : usr/lib/mc/shell/chown 
│                │                       ├ [68] : usr/lib/mc/shell/fexists 
│                │                       ├ [69] : usr/lib/mc/shell/get 
│                │                       ├ [70] : usr/lib/mc/shell/hardlink 
│                │                       ├ [71] : usr/lib/mc/shell/info 
│                │                       ├ [72] : usr/lib/mc/shell/ln 
│                │                       ├ [73] : usr/lib/mc/shell/ls 
│                │                       ├ [74] : usr/lib/mc/shell/mkdir 
│                │                       ├ [75] : usr/lib/mc/shell/mv 
│                │                       ├ [76] : usr/lib/mc/shell/rmdir 
│                │                       ├ [77] : usr/lib/mc/shell/send 
│                │                       ├ [78] : usr/lib/mc/shell/unlink 
│                │                       ├ [79] : usr/lib/mc/shell/utime 
│                │                       ├ [80] : usr/share/mc/mc.charsets 
│                │                       ├ [81] : usr/share/mc/mc.lib 
│                │                       ├ [82] : usr/share/mc/help/mc.hlp 
│                │                       ├ [83] : usr/share/mc/hints/mc.hint 
│                │                       ├ [84] : usr/share/mc/skins/dark.ini 
│                │                       ├ [85] : usr/share/mc/skins/darkfar.ini 
│                │                       ├ [86] : usr/share/mc/skins/default.ini 
│                │                       ├ [87] : usr/share/mc/skins/double-lines.ini 
│                │                       ├ [88] : usr/share/mc/skins/featured-plus.ini 
│                │                       ├ [89] : usr/share/mc/skins/featured.ini 
│                │                       ├ [90] : usr/share/mc/skins/gotar.ini 
│                │                       ├ [91] : usr/share/mc/skins/gray-green-purple256.ini 
│                │                       ├ [92] : usr/share/mc/skins/gray-orange-blue256.ini 
│                │                       ├ [93] : usr/share/mc/skins/julia256.ini 
│                │                       ├ [94] : usr/share/mc/skins/julia256root.ini 
│                │                       ├ [95] : usr/share/mc/skins/mc46.ini 
│                │                       ├ [96] : usr/share/mc/skins/modarcon16-defbg-thin.ini 
│                │                       ├ [97] : usr/share/mc/skins/modarcon16-defbg.ini 
│                │                       ├ [98] : usr/share/mc/skins/modarcon16-thin.ini 
│                │                       ├ [99] : usr/share/mc/skins/modarcon16.ini 
│                │                       ├ [100]: usr/share/mc/skins/modarcon16root-defbg-thin.ini 
│                │                       ├ [101]: usr/share/mc/skins/modarcon16root-defbg.ini 
│                │                       ├ [102]: usr/share/mc/skins/modarcon16root-thin.ini 
│                │                       ├ [103]: usr/share/mc/skins/modarcon16root.ini 
│                │                       ├ [104]: usr/share/mc/skins/modarin256-defbg-thin.ini 
│                │                       ├ [105]: usr/share/mc/skins/modarin256-defbg.ini 
│                │                       ├ [106]: usr/share/mc/skins/modarin256-thin.ini 
│                │                       ├ [107]: usr/share/mc/skins/modarin256.ini 
│                │                       ├ [108]: usr/share/mc/skins/modarin256root-defbg-thin.ini 
│                │                       ├ [109]: usr/share/mc/skins/modarin256root-defbg.ini 
│                │                       ├ [110]: usr/share/mc/skins/modarin256root-thin.ini 
│                │                       ├ [111]: usr/share/mc/skins/modarin256root.ini 
│                │                       ├ [112]: usr/share/mc/skins/nicedark.ini 
│                │                       ├ [113]: usr/share/mc/skins/sand256.ini 
│                │                       ├ [114]: usr/share/mc/skins/seasons-autumn16M.ini 
│                │                       ├ [115]: usr/share/mc/skins/seasons-spring16M.ini 
│                │                       ├ [116]: usr/share/mc/skins/seasons-summer16M.ini 
│                │                       ├ [117]: usr/share/mc/skins/seasons-winter16M.ini 
│                │                       ├ [118]: usr/share/mc/skins/xoria256-thin.ini 
│                │                       ├ [119]: usr/share/mc/skins/xoria256.ini 
│                │                       ├ [120]: usr/share/mc/skins/xoria256root-thin.ini 
│                │                       ├ [121]: usr/share/mc/skins/yadt256-defbg.ini 
│                │                       ├ [122]: usr/share/mc/skins/yadt256.ini 
│                │                       ├ [123]: usr/share/mc/syntax/PKGBUILD.syntax 
│                │                       ├ [124]: usr/share/mc/syntax/Syntax 
│                │                       ├ [125]: usr/share/mc/syntax/ada95.syntax 
│                │                       ├ [126]: usr/share/mc/syntax/as.syntax 
│                │                       ├ [127]: usr/share/mc/syntax/aspx.syntax 
│                │                       ├ [128]: usr/share/mc/syntax/assembler.syntax 
│                │                       ├ [129]: usr/share/mc/syntax/awk.syntax 
│                │                       ├ [130]: usr/share/mc/syntax/b.syntax 
│                │                       ├ [131]: usr/share/mc/syntax/c.syntax 
│                │                       ├ [132]: usr/share/mc/syntax/cabal.syntax 
│                │                       ├ [133]: usr/share/mc/syntax/changelog.syntax 
│                │                       ├ [134]: usr/share/mc/syntax/cmake.syntax 
│                │                       ├ [135]: usr/share/mc/syntax/cobol.syntax 
│                │                       ├ [136]: usr/share/mc/syntax/cs.syntax 
│                │                       ├ [137]: usr/share/mc/syntax/css.syntax 
│                │                       ├ [138]: usr/share/mc/syntax/cuda.syntax 
│                │                       ├ [139]: usr/share/mc/syntax/cxx.syntax 
│                │                       ├ [140]: usr/share/mc/syntax/cython.syntax 
│                │                       ├ [141]: usr/share/mc/syntax/d.syntax 
│                │                       ├ [142]: usr/share/mc/syntax/debian-changelog.syntax 
│                │                       ├ [143]: usr/share/mc/syntax/debian-control.syntax 
│                │                       ├ [144]: usr/share/mc/syntax/debian-description.syntax 
│                │                       ├ [145]: usr/share/mc/syntax/debian-sources-list.syntax 
│                │                       ├ [146]: usr/share/mc/syntax/diff.syntax 
│                │                       ├ [147]: usr/share/mc/syntax/dlink.syntax 
│                │                       ├ [148]: usr/share/mc/syntax/dos.syntax 
│                │                       ├ [149]: usr/share/mc/syntax/dot.syntax 
│                │                       ├ [150]: usr/share/mc/syntax/ebuild.syntax 
│                │                       ├ [151]: usr/share/mc/syntax/eiffel.syntax 
│                │                       ├ [152]: usr/share/mc/syntax/erlang.syntax 
│                │                       ├ [153]: usr/share/mc/syntax/f90.syntax 
│                │                       ├ [154]: usr/share/mc/syntax/filehighlight.syntax 
│                │                       ├ [155]: usr/share/mc/syntax/fortran.syntax 
│                │                       ├ [156]: usr/share/mc/syntax/glsl.syntax 
│                │                       ├ [157]: usr/share/mc/syntax/go.syntax 
│                │                       ├ [158]: usr/share/mc/syntax/haskell.syntax 
│                │                       ├ [159]: usr/share/mc/syntax/hive.syntax 
│                │                       ├ [160]: usr/share/mc/syntax/html.syntax 
│                │                       ├ [161]: usr/share/mc/syntax/idl.syntax 
│                │                       ├ [162]: usr/share/mc/syntax/ini.syntax 
│                │                       ├ [163]: usr/share/mc/syntax/j.syntax 
│                │                       ├ [164]: usr/share/mc/syntax/jal.syntax 
│                │                       ├ [165]: usr/share/mc/syntax/java.syntax 
│                │                       ├ [166]: usr/share/mc/syntax/js.syntax 
│                │                       ├ [167]: usr/share/mc/syntax/json.syntax 
│                │                       ├ [168]: usr/share/mc/syntax/kotlin.syntax 
│                │                       ├ [169]: usr/share/mc/syntax/latex.syntax 
│                │                       ├ [170]: usr/share/mc/syntax/lisp.syntax 
│                │                       ├ [171]: usr/share/mc/syntax/lkr.syntax 
│                │                       ├ [172]: usr/share/mc/syntax/lsm.syntax 
│                │                       ├ [173]: usr/share/mc/syntax/lua.syntax 
│                │                       ├ [174]: usr/share/mc/syntax/m4.syntax 
│                │                       ├ [175]: usr/share/mc/syntax/mail.syntax 
│                │                       ├ [176]: usr/share/mc/syntax/makefile.syntax 
│                │                       ├ [177]: usr/share/mc/syntax/markdown.syntax 
│                │                       ├ [178]: usr/share/mc/syntax/meson.syntax 
│                │                       ├ [179]: usr/share/mc/syntax/ml.syntax 
│                │                       ├ [180]: usr/share/mc/syntax/named.syntax 
│                │                       ├ [181]: usr/share/mc/syntax/nemerle.syntax 
│                │                       ├ [182]: usr/share/mc/syntax/nroff.syntax 
│                │                       ├ [183]: usr/share/mc/syntax/octave.syntax 
│                │                       ├ [184]: usr/share/mc/syntax/opencl.syntax 
│                │                       ├ [185]: usr/share/mc/syntax/osl.syntax 
│                │                       ├ [186]: usr/share/mc/syntax/pascal.syntax 
│                │                       ├ [187]: usr/share/mc/syntax/perl.syntax 
│                │                       ├ [188]: usr/share/mc/syntax/php.syntax 
│                │                       ├ [189]: usr/share/mc/syntax/po.syntax 
│                │                       ├ [190]: usr/share/mc/syntax/povray.syntax 
│                │                       ├ [191]: usr/share/mc/syntax/privoxy.syntax 
│                │                       ├ [192]: usr/share/mc/syntax/procmail.syntax 
│                │                       ├ [193]: usr/share/mc/syntax/properties.syntax 
│                │                       ├ [194]: usr/share/mc/syntax/protobuf.syntax 
│                │                       ├ [195]: usr/share/mc/syntax/puppet.syntax 
│                │                       ├ [196]: usr/share/mc/syntax/python.syntax 
│                │                       ├ [197]: usr/share/mc/syntax/r.syntax 
│                │                       ├ [198]: usr/share/mc/syntax/ruby.syntax 
│                │                       ├ [199]: usr/share/mc/syntax/rust.syntax 
│                │                       ├ [200]: usr/share/mc/syntax/sh.syntax 
│                │                       ├ [201]: usr/share/mc/syntax/slang.syntax 
│                │                       ├ [202]: usr/share/mc/syntax/smalltalk.syntax 
│                │                       ├ [203]: usr/share/mc/syntax/spec.syntax 
│                │                       ├ [204]: usr/share/mc/syntax/spice.syntax 
│                │                       ├ [205]: usr/share/mc/syntax/sql.syntax 
│                │                       ├ [206]: usr/share/mc/syntax/strace.syntax 
│                │                       ├ [207]: usr/share/mc/syntax/swift.syntax 
│                │                       ├ [208]: usr/share/mc/syntax/swig.syntax 
│                │                       ├ [209]: usr/share/mc/syntax/syntax.syntax 
│                │                       ├ [210]: usr/share/mc/syntax/tcl.syntax 
│                │                       ├ [211]: usr/share/mc/syntax/texinfo.syntax 
│                │                       ├ [212]: usr/share/mc/syntax/toml.syntax 
│                │                       ├ [213]: usr/share/mc/syntax/ts.syntax 
│                │                       ├ [214]: usr/share/mc/syntax/tt.syntax 
│                │                       ├ [215]: usr/share/mc/syntax/unknown.syntax 
│                │                       ├ [216]: usr/share/mc/syntax/verilog.syntax 
│                │                       ├ [217]: usr/share/mc/syntax/vhdl.syntax 
│                │                       ├ [218]: usr/share/mc/syntax/xml.syntax 
│                │                       ├ [219]: usr/share/mc/syntax/yabasic.syntax 
│                │                       ├ [220]: usr/share/mc/syntax/yaml.syntax 
│                │                       ├ [221]: usr/share/mc/syntax/yum-repo.syntax 
│                │                       ╰ [222]: usr/share/mc/syntax/yxx.syntax 
│                ├ [42] ╭ ID            : mimalloc2@2.2.3-r2 
│                │      ├ Name          : mimalloc2 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/mimalloc2@2.2.3-r2?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : de33d9e487654f8d 
│                │      ├ Version       : 2.2.3-r2 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : mimalloc2 
│                │      ├ SrcVersion    : 2.2.3-r2 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Jakub Jirutka <jakub@jirutka.cz> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:3bf2a1468098e66e2649ac261dec49c02624f7a1 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libmimalloc-secure.so.2 
│                │                       ├ [1]: usr/lib/libmimalloc-secure.so.2.2 
│                │                       ├ [2]: usr/lib/libmimalloc.so.2 
│                │                       ╰ [3]: usr/lib/libmimalloc.so.2.2 
│                ├ [43] ╭ ID            : musl@1.2.5-r21 
│                │      ├ Name          : musl 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/musl@1.2.5-r21?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 509a164ecbc034e0 
│                │      ├ Version       : 1.2.5-r21 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : musl 
│                │      ├ SrcVersion    : 1.2.5-r21 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4dcd8f28bb875b9a45d3c7afbafcb7c063ddcc4c 
│                │      ╰ InstalledFiles ╭ [0]: lib/ld-musl-x86_64.so.1 
│                │                       ╰ [1]: lib/libc.musl-x86_64.so.1 
│                ├ [44] ╭ ID            : musl-utils@1.2.5-r21 
│                │      ├ Name          : musl-utils 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/musl-utils@1.2.5-r21?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : ce2cff7818ec0836 
│                │      ├ Version       : 1.2.5-r21 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : musl 
│                │      ├ SrcVersion    : 1.2.5-r21 
│                │      ├ Licenses       ╭ [0]: MIT 
│                │      │                ├ [1]: BSD-2-Clause 
│                │      │                ╰ [2]: GPL-2.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: musl@1.2.5-r21 
│                │      │                ╰ [1]: scanelf@1.3.8-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:793ce8115cfc734d044044e5a6b93cbce69bbb42 
│                │      ╰ InstalledFiles ╭ [0]: sbin/ldconfig 
│                │                       ├ [1]: usr/bin/getconf 
│                │                       ├ [2]: usr/bin/getent 
│                │                       ├ [3]: usr/bin/iconv 
│                │                       ╰ [4]: usr/bin/ldd 
│                ├ [45] ╭ ID            : ncurses-terminfo-base@6.5_p20251123-r0 
│                │      ├ Name          : ncurses-terminfo-base 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/ncurses-terminfo-base@6.5_p20251123-r0?arch=x86
│                │      │                │       _64&distro=3.23.0 
│                │      │                ╰ UID : b39472a9551d7178 
│                │      ├ Version       : 6.5_p20251123-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : ncurses 
│                │      ├ SrcVersion    : 6.5_p20251123-r0 
│                │      ├ Licenses       ─ [0]: X-11 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:57bd1d8124ec957eefea2314bdf45b0ed1068cee 
│                │      ╰ InstalledFiles ╭ [0] : etc/terminfo/a/alacritty 
│                │                       ├ [1] : etc/terminfo/a/ansi 
│                │                       ├ [2] : etc/terminfo/d/dumb 
│                │                       ├ [3] : etc/terminfo/g/gnome 
│                │                       ├ [4] : etc/terminfo/g/gnome-256color 
│                │                       ├ [5] : etc/terminfo/k/konsole 
│                │                       ├ [6] : etc/terminfo/k/konsole-256color 
│                │                       ├ [7] : etc/terminfo/k/konsole-linux 
│                │                       ├ [8] : etc/terminfo/l/linux 
│                │                       ├ [9] : etc/terminfo/p/putty 
│                │                       ├ [10]: etc/terminfo/p/putty-256color 
│                │                       ├ [11]: etc/terminfo/r/rxvt 
│                │                       ├ [12]: etc/terminfo/r/rxvt-256color 
│                │                       ├ [13]: etc/terminfo/s/screen 
│                │                       ├ [14]: etc/terminfo/s/screen-256color 
│                │                       ├ [15]: etc/terminfo/s/st-0.6 
│                │                       ├ [16]: etc/terminfo/s/st-0.7 
│                │                       ├ [17]: etc/terminfo/s/st-0.8 
│                │                       ├ [18]: etc/terminfo/s/st-0.8.5 
│                │                       ├ [19]: etc/terminfo/s/st-16color 
│                │                       ├ [20]: etc/terminfo/s/st-256color 
│                │                       ├ [21]: etc/terminfo/s/st-direct 
│                │                       ├ [22]: etc/terminfo/s/sun 
│                │                       ├ [23]: etc/terminfo/t/terminator 
│                │                       ├ [24]: etc/terminfo/t/terminology 
│                │                       ├ [25]: etc/terminfo/t/terminology-0.6.1 
│                │                       ├ [26]: etc/terminfo/t/terminology-1.0.0 
│                │                       ├ [27]: etc/terminfo/t/terminology-1.8.1 
│                │                       ├ [28]: etc/terminfo/t/tmux 
│                │                       ├ [29]: etc/terminfo/t/tmux-256color 
│                │                       ├ [30]: etc/terminfo/v/vt100 
│                │                       ├ [31]: etc/terminfo/v/vt102 
│                │                       ├ [32]: etc/terminfo/v/vt200 
│                │                       ├ [33]: etc/terminfo/v/vt220 
│                │                       ├ [34]: etc/terminfo/v/vt52 
│                │                       ├ [35]: etc/terminfo/v/vte 
│                │                       ├ [36]: etc/terminfo/v/vte-256color 
│                │                       ├ [37]: etc/terminfo/x/xterm 
│                │                       ├ [38]: etc/terminfo/x/xterm-256color 
│                │                       ├ [39]: etc/terminfo/x/xterm-color 
│                │                       ╰ [40]: etc/terminfo/x/xterm-xfree86 
│                ├ [46] ╭ ID            : nghttp2-libs@1.68.0-r0 
│                │      ├ Name          : nghttp2-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/nghttp2-libs@1.68.0-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : dca2be8e80b615ee 
│                │      ├ Version       : 1.68.0-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : nghttp2 
│                │      ├ SrcVersion    : 1.68.0-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Francesco Colista <fcolista@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:584b6a1b0aed58a3f543bfd77729b0d8a8b1745b 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libnghttp2.so.14 
│                │                       ╰ [1]: usr/lib/libnghttp2.so.14.29.2 
│                ├ [47] ╭ ID            : nghttp3@1.13.1-r0 
│                │      ├ Name          : nghttp3 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/nghttp3@1.13.1-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 47a1d1cccc4a6c6 
│                │      ├ Version       : 1.13.1-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : nghttp3 
│                │      ├ SrcVersion    : 1.13.1-r0 
│                │      ├ Licenses       ─ [0]: MIT 
│                │      ├ Maintainer    : Jakub Jirutka <jakub@jirutka.cz> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:e48fcb3e81f7e46a42e3926d8513c83b7798774b 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libnghttp3.so.9 
│                │                       ╰ [1]: usr/lib/libnghttp3.so.9.5.1 
│                ├ [48] ╭ ID            : openssl@3.5.4-r0 
│                │      ├ Name          : openssl 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/openssl@3.5.4-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 5935edfed16e31e7 
│                │      ├ Version       : 3.5.4-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : openssl 
│                │      ├ SrcVersion    : 3.5.4-r0 
│                │      ├ Licenses       ─ [0]: Apache-2.0 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libcrypto3@3.5.4-r0 
│                │      │                ├ [1]: libssl3@3.5.4-r0 
│                │      │                ╰ [2]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:7cb1a0d4cf4752f32477c3a35a84484e25e82b15 
│                │      ╰ InstalledFiles ─ [0]: usr/bin/openssl 
│                ├ [49] ╭ ID            : pcre2@10.47-r0 
│                │      ├ Name          : pcre2 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/pcre2@10.47-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 24f01972c58dff6a 
│                │      ├ Version       : 10.47-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : pcre2 
│                │      ├ SrcVersion    : 10.47-r0 
│                │      ├ Licenses       ─ [0]: BSD-3-Clause 
│                │      ├ Maintainer    : Jakub Jirutka <jakub@jirutka.cz> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:549059958151627bb0f5469bded945988b1bc24b 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libpcre2-8.so.0 
│                │                       ├ [1]: usr/lib/libpcre2-8.so.0.15.0 
│                │                       ├ [2]: usr/lib/libpcre2-posix.so.3 
│                │                       ╰ [3]: usr/lib/libpcre2-posix.so.3.0.7 
│                ├ [50] ╭ ID            : procps-ng@4.0.5-r0 
│                │      ├ Name          : procps-ng 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/procps-ng@4.0.5-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 348892ea10d2ca6e 
│                │      ├ Version       : 4.0.5-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : procps-ng 
│                │      ├ SrcVersion    : 4.0.5-r0 
│                │      ├ Licenses       ╭ [0]: GPL-2.0-or-later 
│                │      │                ╰ [1]: LGPL-2.1-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ╭ [0]: libintl@0.24.1-r1 
│                │      │                ├ [1]: libncursesw@6.5_p20251123-r0 
│                │      │                ├ [2]: libproc2@4.0.5-r0 
│                │      │                ├ [3]: musl@1.2.5-r21 
│                │      │                ╰ [4]: utmps-libs@0.1.3.1-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:475002748f145d15159e475308f44bd441ae6488 
│                │      ╰ InstalledFiles ╭ [0] : bin/hugetop 
│                │                       ├ [1] : bin/pidof 
│                │                       ├ [2] : bin/pidwait 
│                │                       ├ [3] : bin/ps 
│                │                       ├ [4] : bin/slabtop 
│                │                       ├ [5] : bin/tload 
│                │                       ├ [6] : bin/vmstat 
│                │                       ├ [7] : bin/w 
│                │                       ├ [8] : bin/watch 
│                │                       ├ [9] : sbin/sysctl 
│                │                       ├ [10]: usr/bin/free 
│                │                       ├ [11]: usr/bin/pgrep 
│                │                       ├ [12]: usr/bin/pkill 
│                │                       ├ [13]: usr/bin/pmap 
│                │                       ├ [14]: usr/bin/pwdx 
│                │                       ├ [15]: usr/bin/top 
│                │                       ╰ [16]: usr/bin/uptime 
│                ├ [51] ╭ ID            : readline@8.3.1-r0 
│                │      ├ Name          : readline 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/readline@8.3.1-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : d457c7cf22fbe30b 
│                │      ├ Version       : 8.3.1-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : readline 
│                │      ├ SrcVersion    : 8.3.1-r0 
│                │      ├ Licenses       ─ [0]: GPL-3.0-or-later 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: libncursesw@6.5_p20251123-r0 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:20dfeb3984988b8977558424cff511cd4f4ebf4c 
│                │      ╰ InstalledFiles ╭ [0]: etc/inputrc 
│                │                       ├ [1]: usr/lib/libreadline.so.8 
│                │                       ╰ [2]: usr/lib/libreadline.so.8.3 
│                ├ [52] ╭ ID            : scanelf@1.3.8-r2 
│                │      ├ Name          : scanelf 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/scanelf@1.3.8-r2?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 2d30f8070e641de7 
│                │      ├ Version       : 1.3.8-r2 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : pax-utils 
│                │      ├ SrcVersion    : 1.3.8-r2 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:a3f6b84d745992475a9777da9b7fa012c5eb0588 
│                │      ╰ InstalledFiles ─ [0]: usr/bin/scanelf 
│                ├ [53] ╭ ID            : skalibs-libs@2.14.4.0-r0 
│                │      ├ Name          : skalibs-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/skalibs-libs@2.14.4.0-r0?arch=x86_64&distro=3.2
│                │      │                │       3.0 
│                │      │                ╰ UID : 916c5bae827b19dd 
│                │      ├ Version       : 2.14.4.0-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : skalibs 
│                │      ├ SrcVersion    : 2.14.4.0-r0 
│                │      ├ Licenses       ─ [0]: ISC 
│                │      ├ Maintainer    : Laurent Bercot <ska-devel@skarnet.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:8ca4ae34fad485e55b63727912e5f8f39efb134a 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libskarnet.so.2.14 
│                │                       ╰ [1]: usr/lib/libskarnet.so.2.14.4.0 
│                ├ [54] ╭ ID            : slang@2.3.3-r3 
│                │      ├ Name          : slang 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/slang@2.3.3-r3?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : a7281bf7f423da94 
│                │      ├ Version       : 2.3.3-r3 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : slang 
│                │      ├ SrcVersion    : 2.3.3-r3 
│                │      ├ Licenses       ─ [0]: GPL-2.0-or-later 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:0073f55b982a022ee9cb665281d1a254cf13f36f 
│                │      ╰ InstalledFiles ╭ [0]  : etc/slsh.rc 
│                │                       ├ [1]  : usr/bin/slsh 
│                │                       ├ [2]  : usr/lib/libslang.so.2 
│                │                       ├ [3]  : usr/lib/libslang.so.2.3.3 
│                │                       ├ [4]  : usr/lib/slang/v2/modules/base64-module.so 
│                │                       ├ [5]  : usr/lib/slang/v2/modules/chksum-module.so 
│                │                       ├ [6]  : usr/lib/slang/v2/modules/csv-module.so 
│                │                       ├ [7]  : usr/lib/slang/v2/modules/fcntl-module.so 
│                │                       ├ [8]  : usr/lib/slang/v2/modules/fork-module.so 
│                │                       ├ [9]  : usr/lib/slang/v2/modules/histogram-module.so 
│                │                       ├ [10] : usr/lib/slang/v2/modules/iconv-module.so 
│                │                       ├ [11] : usr/lib/slang/v2/modules/json-module.so 
│                │                       ├ [12] : usr/lib/slang/v2/modules/rand-module.so 
│                │                       ├ [13] : usr/lib/slang/v2/modules/select-module.so 
│                │                       ├ [14] : usr/lib/slang/v2/modules/slsmg-module.so 
│                │                       ├ [15] : usr/lib/slang/v2/modules/socket-module.so 
│                │                       ├ [16] : usr/lib/slang/v2/modules/stats-module.so 
│                │                       ├ [17] : usr/lib/slang/v2/modules/sysconf-module.so 
│                │                       ├ [18] : usr/lib/slang/v2/modules/termios-module.so 
│                │                       ├ [19] : usr/lib/slang/v2/modules/varray-module.so 
│                │                       ├ [20] : usr/share/slsh/arrayfuns.sl 
│                │                       ├ [21] : usr/share/slsh/autoload.sl 
│                │                       ├ [22] : usr/share/slsh/base64.sl 
│                │                       ├ [23] : usr/share/slsh/chksum.sl 
│                │                       ├ [24] : usr/share/slsh/cmdopt.sl 
│                │                       ├ [25] : usr/share/slsh/csv.sl 
│                │                       ├ [26] : usr/share/slsh/fcntl.sl 
│                │                       ├ [27] : usr/share/slsh/fork.sl 
│                │                       ├ [28] : usr/share/slsh/fswalk.sl 
│                │                       ├ [29] : usr/share/slsh/glob.sl 
│                │                       ├ [30] : usr/share/slsh/histogram.sl 
│                │                       ├ [31] : usr/share/slsh/iconv.sl 
│                │                       ├ [32] : usr/share/slsh/json.sl 
│                │                       ├ [33] : usr/share/slsh/listfuns.sl 
│                │                       ├ [34] : usr/share/slsh/onig.sl 
│                │                       ├ [35] : usr/share/slsh/pcre.sl 
│                │                       ├ [36] : usr/share/slsh/png.sl 
│                │                       ├ [37] : usr/share/slsh/print.sl 
│                │                       ├ [38] : usr/share/slsh/process.sl 
│                │                       ├ [39] : usr/share/slsh/profile.sl 
│                │                       ├ [40] : usr/share/slsh/rand.sl 
│                │                       ├ [41] : usr/share/slsh/readascii.sl 
│                │                       ├ [42] : usr/share/slsh/require.sl 
│                │                       ├ [43] : usr/share/slsh/select.sl 
│                │                       ├ [44] : usr/share/slsh/setfuns.sl 
│                │                       ├ [45] : usr/share/slsh/sldb.sl 
│                │                       ├ [46] : usr/share/slsh/sldbcore.sl 
│                │                       ├ [47] : usr/share/slsh/sldbsock.sl 
│                │                       ├ [48] : usr/share/slsh/slshhelp.sl 
│                │                       ├ [49] : usr/share/slsh/slshrl.sl 
│                │                       ├ [50] : usr/share/slsh/slsmg.sl 
│                │                       ├ [51] : usr/share/slsh/socket.sl 
│                │                       ├ [52] : usr/share/slsh/stats.sl 
│                │                       ├ [53] : usr/share/slsh/stkcheck.sl 
│                │                       ├ [54] : usr/share/slsh/structfuns.sl 
│                │                       ├ [55] : usr/share/slsh/sysconf.sl 
│                │                       ├ [56] : usr/share/slsh/termios.sl 
│                │                       ├ [57] : usr/share/slsh/timestamp.sl 
│                │                       ├ [58] : usr/share/slsh/varray.sl 
│                │                       ├ [59] : usr/share/slsh/zlib.sl 
│                │                       ├ [60] : usr/share/slsh/cmaps/cool.map 
│                │                       ├ [61] : usr/share/slsh/cmaps/coolwarm.map 
│                │                       ├ [62] : usr/share/slsh/cmaps/copper.map 
│                │                       ├ [63] : usr/share/slsh/cmaps/cubicl.map 
│                │                       ├ [64] : usr/share/slsh/cmaps/cubicyf.map 
│                │                       ├ [65] : usr/share/slsh/cmaps/drywet.map 
│                │                       ├ [66] : usr/share/slsh/cmaps/ds9b.map 
│                │                       ├ [67] : usr/share/slsh/cmaps/ds9sls.map 
│                │                       ├ [68] : usr/share/slsh/cmaps/edge.map 
│                │                       ├ [69] : usr/share/slsh/cmaps/gebco.map 
│                │                       ├ [70] : usr/share/slsh/cmaps/globe.map 
│                │                       ├ [71] : usr/share/slsh/cmaps/gray.map 
│                │                       ├ [72] : usr/share/slsh/cmaps/haxby.map 
│                │                       ├ [73] : usr/share/slsh/cmaps/hot.map 
│                │                       ├ [74] : usr/share/slsh/cmaps/jet.map 
│                │                       ├ [75] : usr/share/slsh/cmaps/no_green.map 
│                │                       ├ [76] : usr/share/slsh/cmaps/ocean.map 
│                │                       ├ [77] : usr/share/slsh/cmaps/polar.map 
│                │                       ├ [78] : usr/share/slsh/cmaps/rainbow.map 
│                │                       ├ [79] : usr/share/slsh/cmaps/red2green.map 
│                │                       ├ [80] : usr/share/slsh/cmaps/relief.map 
│                │                       ├ [81] : usr/share/slsh/cmaps/sealand.map 
│                │                       ├ [82] : usr/share/slsh/cmaps/seis.map 
│                │                       ├ [83] : usr/share/slsh/cmaps/split.map 
│                │                       ├ [84] : usr/share/slsh/cmaps/topo.map 
│                │                       ├ [85] : usr/share/slsh/cmaps/wysiwyg.map 
│                │                       ├ [86] : usr/share/slsh/help/arrayfuns.hlp 
│                │                       ├ [87] : usr/share/slsh/help/base64funs.hlp 
│                │                       ├ [88] : usr/share/slsh/help/chksumfuns.hlp 
│                │                       ├ [89] : usr/share/slsh/help/cmdopt.hlp 
│                │                       ├ [90] : usr/share/slsh/help/csvfuns.hlp 
│                │                       ├ [91] : usr/share/slsh/help/forkfuns.hlp 
│                │                       ├ [92] : usr/share/slsh/help/fswalk.hlp 
│                │                       ├ [93] : usr/share/slsh/help/glob.hlp 
│                │                       ├ [94] : usr/share/slsh/help/histfuns.hlp 
│                │                       ├ [95] : usr/share/slsh/help/jsonfuns.hlp 
│                │                       ├ [96] : usr/share/slsh/help/listfuns.hlp 
│                │                       ├ [97] : usr/share/slsh/help/onigfuns.hlp 
│                │                       ├ [98] : usr/share/slsh/help/pcrefuns.hlp 
│                │                       ├ [99] : usr/share/slsh/help/pngfuns.hlp 
│                │                       ├ [100]: usr/share/slsh/help/print.hlp 
│                │                       ├ [101]: usr/share/slsh/help/process.hlp 
│                │                       ├ [102]: usr/share/slsh/help/profile.hlp 
│                │                       ├ [103]: usr/share/slsh/help/randfuns.hlp 
│                │                       ├ [104]: usr/share/slsh/help/readascii.hlp 
│                │                       ├ [105]: usr/share/slsh/help/require.hlp 
│                │                       ├ [106]: usr/share/slsh/help/setfuns.hlp 
│                │                       ├ [107]: usr/share/slsh/help/slsmg.hlp 
│                │                       ├ [108]: usr/share/slsh/help/sockfuns.hlp 
│                │                       ├ [109]: usr/share/slsh/help/statsfuns.hlp 
│                │                       ├ [110]: usr/share/slsh/help/structfuns.hlp 
│                │                       ├ [111]: usr/share/slsh/help/timestamp.hlp 
│                │                       ├ [112]: usr/share/slsh/rline/complete.sl 
│                │                       ├ [113]: usr/share/slsh/rline/editfuns.sl 
│                │                       ├ [114]: usr/share/slsh/rline/editor.sl 
│                │                       ├ [115]: usr/share/slsh/rline/emacskeys.sl 
│                │                       ├ [116]: usr/share/slsh/rline/history.sl 
│                │                       ├ [117]: usr/share/slsh/rline/histsrch.sl 
│                │                       ├ [118]: usr/share/slsh/rline/slrline.rc 
│                │                       ├ [119]: usr/share/slsh/rline/vikeys.sl 
│                │                       ├ [120]: usr/share/slsh/scripts/jpegsize 
│                │                       ├ [121]: usr/share/slsh/scripts/lsrpm 
│                │                       ├ [122]: usr/share/slsh/scripts/slcov 
│                │                       ├ [123]: usr/share/slsh/scripts/sldb 
│                │                       ├ [124]: usr/share/slsh/scripts/slprof 
│                │                       ├ [125]: usr/share/slsh/scripts/slstkchk 
│                │                       ├ [126]: usr/share/slsh/scripts/svnsh 
│                │                       ├ [127]: usr/share/slsh/statslib/ad_test.sl 
│                │                       ├ [128]: usr/share/slsh/statslib/ks_test.sl 
│                │                       ╰ [129]: usr/share/slsh/statslib/kuiper.sl 
│                ├ [55] ╭ ID            : ssl_client@1.37.0-r29 
│                │      ├ Name          : ssl_client 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/ssl_client@1.37.0-r29?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 1138b38b7d7cd9e7 
│                │      ├ Version       : 1.37.0-r29 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : busybox 
│                │      ├ SrcVersion    : 1.37.0-r29 
│                │      ├ Licenses       ─ [0]: GPL-2.0-only 
│                │      ├ Maintainer    : Sören Tempel <soeren+alpine@soeren-tempel.net> 
│                │      ├ DependsOn      ╭ [0]: libcrypto3@3.5.4-r0 
│                │      │                ├ [1]: libssl3@3.5.4-r0 
│                │      │                ╰ [2]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:c4cef5aa030704c1f7a32bbb31574326869c51dc 
│                │      ╰ InstalledFiles ─ [0]: usr/bin/ssl_client 
│                ├ [56] ╭ ID            : sudo@1.9.17_p2-r0 
│                │      ├ Name          : sudo 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/sudo@1.9.17_p2-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 7b977442aed81bdc 
│                │      ├ Version       : 1.9.17_p2-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : sudo 
│                │      ├ SrcVersion    : 1.9.17_p2-r0 
│                │      ├ Licenses       ╭ [0]: custom 
│                │      │                ╰ [1]: ISC 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: musl@1.2.5-r21 
│                │      │                ╰ [1]: zlib@1.3.1-r2 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:28f01919930702fb0541ac009f9c2483079ba6b6 
│                │      ╰ InstalledFiles ╭ [0] : etc/sudo.conf 
│                │                       ├ [1] : etc/sudo_logsrvd.conf 
│                │                       ├ [2] : etc/sudoers 
│                │                       ├ [3] : usr/bin/cvtsudoers 
│                │                       ├ [4] : usr/bin/sudo 
│                │                       ├ [5] : usr/bin/sudoedit 
│                │                       ├ [6] : usr/bin/sudoreplay 
│                │                       ├ [7] : usr/lib/sudo/audit_json.so 
│                │                       ├ [8] : usr/lib/sudo/group_file.so 
│                │                       ├ [9] : usr/lib/sudo/libsudo_util.so 
│                │                       ├ [10]: usr/lib/sudo/libsudo_util.so.0 
│                │                       ├ [11]: usr/lib/sudo/libsudo_util.so.0.0.0 
│                │                       ├ [12]: usr/lib/sudo/sudo_intercept.so 
│                │                       ├ [13]: usr/lib/sudo/sudo_noexec.so 
│                │                       ├ [14]: usr/lib/sudo/sudoers.so 
│                │                       ├ [15]: usr/lib/sudo/system_group.so 
│                │                       ├ [16]: usr/sbin/sudo_logsrvd 
│                │                       ├ [17]: usr/sbin/sudo_sendlog 
│                │                       ╰ [18]: usr/sbin/visudo 
│                ├ [57] ╭ ID            : tar@1.35-r4 
│                │      ├ Name          : tar 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/tar@1.35-r4?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 4e017ca975e22554 
│                │      ├ Version       : 1.35-r4 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : tar 
│                │      ├ SrcVersion    : 1.35-r4 
│                │      ├ Licenses       ─ [0]: GPL-3.0-or-later 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: acl-libs@2.3.2-r1 
│                │      │                ╰ [1]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:2355ca3eece8193ed6cfdcca58672378391178d3 
│                │      ╰ InstalledFiles ╭ [0]: bin/tar 
│                │                       ╰ [1]: usr/libexec/rmt 
│                ├ [58] ╭ ID            : tmux@3.6a-r0 
│                │      ├ Name          : tmux 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/tmux@3.6a-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 56ceefe890f8c849 
│                │      ├ Version       : 3.6a-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : tmux 
│                │      ├ SrcVersion    : 3.6a-r0 
│                │      ├ Licenses       ─ [0]: ISC 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: libevent@2.1.12-r8 
│                │      │                ├ [1]: libncursesw@6.5_p20251123-r0 
│                │      │                ├ [2]: musl@1.2.5-r21 
│                │      │                ╰ [3]: ncurses-terminfo-base@6.5_p20251123-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:4dc24c4a8dca3bfe162c590f64c2a4e3458e112d 
│                │      ╰ InstalledFiles ─ [0]: usr/bin/tmux 
│                ├ [59] ╭ ID            : util-linux-doc@2.41.2-r0 
│                │      ├ Name          : util-linux-doc 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/util-linux-doc@2.41.2-r0?arch=x86_64&distro=3.2
│                │      │                │       3.0 
│                │      │                ╰ UID : 8f2548ba6fa13854 
│                │      ├ Version       : 2.41.2-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : util-linux 
│                │      ├ SrcVersion    : 2.41.2-r0 
│                │      ├ Licenses       ╭ [0]: GPL-3.0-or-later 
│                │      │                ├ [1]: GPL-2.0-or-later 
│                │      │                ├ [2]: GPL-2.0-only 
│                │      │                ├ [3]: GPL-1.0-only 
│                │      │                ├ [4]: LGPL-2.1-or-later 
│                │      │                ├ [5]: BSD-1-Clause 
│                │      │                ├ [6]: BSD-3-Clause 
│                │      │                ├ [7]: BSD-4-Clause-UC 
│                │      │                ├ [8]: MIT 
│                │      │                ╰ [9]: Public-Domain 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:0cc90b6ab1dbfe474357e16b0124422c7823104e 
│                │      ╰ InstalledFiles ╭ [0]  : usr/share/doc/util-linux/getopt-example.bash 
│                │                       ├ [1]  : usr/share/doc/util-linux/getopt-example.tcsh 
│                │                       ├ [2]  : usr/share/man/man1/bits.1.gz 
│                │                       ├ [3]  : usr/share/man/man1/cal.1.gz 
│                │                       ├ [4]  : usr/share/man/man1/choom.1.gz 
│                │                       ├ [5]  : usr/share/man/man1/chrt.1.gz 
│                │                       ├ [6]  : usr/share/man/man1/colcrt.1.gz 
│                │                       ├ [7]  : usr/share/man/man1/colrm.1.gz 
│                │                       ├ [8]  : usr/share/man/man1/column.1.gz 
│                │                       ├ [9]  : usr/share/man/man1/coresched.1.gz 
│                │                       ├ [10] : usr/share/man/man1/dmesg.1.gz 
│                │                       ├ [11] : usr/share/man/man1/eject.1.gz 
│                │                       ├ [12] : usr/share/man/man1/enosys.1.gz 
│                │                       ├ [13] : usr/share/man/man1/exch.1.gz 
│                │                       ├ [14] : usr/share/man/man1/fadvise.1.gz 
│                │                       ├ [15] : usr/share/man/man1/fallocate.1.gz 
│                │                       ├ [16] : usr/share/man/man1/fincore.1.gz 
│                │                       ├ [17] : usr/share/man/man1/flock.1.gz 
│                │                       ├ [18] : usr/share/man/man1/getopt.1.gz 
│                │                       ├ [19] : usr/share/man/man1/hardlink.1.gz 
│                │                       ├ [20] : usr/share/man/man1/hexdump.1.gz 
│                │                       ├ [21] : usr/share/man/man1/ionice.1.gz 
│                │                       ├ [22] : usr/share/man/man1/ipcmk.1.gz 
│                │                       ├ [23] : usr/share/man/man1/ipcrm.1.gz 
│                │                       ├ [24] : usr/share/man/man1/ipcs.1.gz 
│                │                       ├ [25] : usr/share/man/man1/irqtop.1.gz 
│                │                       ├ [26] : usr/share/man/man1/logger.1.gz 
│                │                       ├ [27] : usr/share/man/man1/look.1.gz 
│                │                       ├ [28] : usr/share/man/man1/lsclocks.1.gz 
│                │                       ├ [29] : usr/share/man/man1/lscpu.1.gz 
│                │                       ├ [30] : usr/share/man/man1/lsfd.1.gz 
│                │                       ├ [31] : usr/share/man/man1/lsipc.1.gz 
│                │                       ├ [32] : usr/share/man/man1/lsirq.1.gz 
│                │                       ├ [33] : usr/share/man/man1/lsmem.1.gz 
│                │                       ├ [34] : usr/share/man/man1/mcookie.1.gz 
│                │                       ├ [35] : usr/share/man/man1/mesg.1.gz 
│                │                       ├ [36] : usr/share/man/man1/more.1.gz 
│                │                       ├ [37] : usr/share/man/man1/mountpoint.1.gz 
│                │                       ├ [38] : usr/share/man/man1/namei.1.gz 
│                │                       ├ [39] : usr/share/man/man1/nsenter.1.gz 
│                │                       ├ [40] : usr/share/man/man1/pipesz.1.gz 
│                │                       ├ [41] : usr/share/man/man1/prlimit.1.gz 
│                │                       ├ [42] : usr/share/man/man1/rename.1.gz 
│                │                       ├ [43] : usr/share/man/man1/renice.1.gz 
│                │                       ├ [44] : usr/share/man/man1/rev.1.gz 
│                │                       ├ [45] : usr/share/man/man1/runuser.1.gz 
│                │                       ├ [46] : usr/share/man/man1/script.1.gz 
│                │                       ├ [47] : usr/share/man/man1/scriptlive.1.gz 
│                │                       ├ [48] : usr/share/man/man1/scriptreplay.1.gz 
│                │                       ├ [49] : usr/share/man/man1/setpgid.1.gz 
│                │                       ├ [50] : usr/share/man/man1/setpriv.1.gz 
│                │                       ├ [51] : usr/share/man/man1/setsid.1.gz 
│                │                       ├ [52] : usr/share/man/man1/setterm.1.gz 
│                │                       ├ [53] : usr/share/man/man1/taskset.1.gz 
│                │                       ├ [54] : usr/share/man/man1/uclampset.1.gz 
│                │                       ├ [55] : usr/share/man/man1/ul.1.gz 
│                │                       ├ [56] : usr/share/man/man1/unshare.1.gz 
│                │                       ├ [57] : usr/share/man/man1/utmpdump.1.gz 
│                │                       ├ [58] : usr/share/man/man1/uuidgen.1.gz 
│                │                       ├ [59] : usr/share/man/man1/uuidparse.1.gz 
│                │                       ├ [60] : usr/share/man/man1/waitpid.1.gz 
│                │                       ├ [61] : usr/share/man/man1/wall.1.gz 
│                │                       ├ [62] : usr/share/man/man1/whereis.1.gz 
│                │                       ├ [63] : usr/share/man/man3/libblkid.3.gz 
│                │                       ├ [64] : usr/share/man/man3/ll2_import_lastlog.3.gz 
│                │                       ├ [65] : usr/share/man/man3/ll2_read_all.3.gz 
│                │                       ├ [66] : usr/share/man/man3/ll2_read_entry.3.gz 
│                │                       ├ [67] : usr/share/man/man3/ll2_remove_entry.3.gz 
│                │                       ├ [68] : usr/share/man/man3/ll2_rename_user.3.gz 
│                │                       ├ [69] : usr/share/man/man3/ll2_update_login_time.3.gz 
│                │                       ├ [70] : usr/share/man/man3/ll2_write_entry.3.gz 
│                │                       ├ [71] : usr/share/man/man3/uuid.3.gz 
│                │                       ├ [72] : usr/share/man/man3/uuid_clear.3.gz 
│                │                       ├ [73] : usr/share/man/man3/uuid_compare.3.gz 
│                │                       ├ [74] : usr/share/man/man3/uuid_copy.3.gz 
│                │                       ├ [75] : usr/share/man/man3/uuid_generate.3.gz 
│                │                       ├ [76] : usr/share/man/man3/uuid_generate_random.3.gz 
│                │                       ├ [77] : usr/share/man/man3/uuid_generate_time.3.gz 
│                │                       ├ [78] : usr/share/man/man3/uuid_generate_time_safe.3.gz 
│                │                       ├ [79] : usr/share/man/man3/uuid_is_null.3.gz 
│                │                       ├ [80] : usr/share/man/man3/uuid_parse.3.gz 
│                │                       ├ [81] : usr/share/man/man3/uuid_time.3.gz 
│                │                       ├ [82] : usr/share/man/man3/uuid_unparse.3.gz 
│                │                       ├ [83] : usr/share/man/man5/adjtime_config.5.gz 
│                │                       ├ [84] : usr/share/man/man5/fstab.5.gz 
│                │                       ├ [85] : usr/share/man/man5/scols-filter.5.gz 
│                │                       ├ [86] : usr/share/man/man5/terminal-colors.d.5.gz 
│                │                       ├ [87] : usr/share/man/man8/addpart.8.gz 
│                │                       ├ [88] : usr/share/man/man8/agetty.8.gz 
│                │                       ├ [89] : usr/share/man/man8/blkdiscard.8.gz 
│                │                       ├ [90] : usr/share/man/man8/blkid.8.gz 
│                │                       ├ [91] : usr/share/man/man8/blkpr.8.gz 
│                │                       ├ [92] : usr/share/man/man8/blkzone.8.gz 
│                │                       ├ [93] : usr/share/man/man8/blockdev.8.gz 
│                │                       ├ [94] : usr/share/man/man8/cfdisk.8.gz 
│                │                       ├ [95] : usr/share/man/man8/chcpu.8.gz 
│                │                       ├ [96] : usr/share/man/man8/chmem.8.gz 
│                │                       ├ [97] : usr/share/man/man8/ctrlaltdel.8.gz 
│                │                       ├ [98] : usr/share/man/man8/delpart.8.gz 
│                │                       ├ [99] : usr/share/man/man8/fdisk.8.gz 
│                │                       ├ [100]: usr/share/man/man8/findfs.8.gz 
│                │                       ├ [101]: usr/share/man/man8/findmnt.8.gz 
│                │                       ├ [102]: usr/share/man/man8/fsck.8.gz 
│                │                       ├ [103]: usr/share/man/man8/fsck.cramfs.8.gz 
│                │                       ├ [104]: usr/share/man/man8/fsck.minix.8.gz 
│                │                       ├ [105]: usr/share/man/man8/fsfreeze.8.gz 
│                │                       ├ [106]: usr/share/man/man8/fstrim.8.gz 
│                │                       ├ [107]: usr/share/man/man8/hwclock.8.gz 
│                │                       ├ [108]: usr/share/man/man8/i386.8.gz 
│                │                       ├ [109]: usr/share/man/man8/isosize.8.gz 
│                │                       ├ [110]: usr/share/man/man8/ldattach.8.gz 
│                │                       ├ [111]: usr/share/man/man8/linux32.8.gz 
│                │                       ├ [112]: usr/share/man/man8/linux64.8.gz 
│                │                       ├ [113]: usr/share/man/man8/losetup.8.gz 
│                │                       ├ [114]: usr/share/man/man8/lsblk.8.gz 
│                │                       ├ [115]: usr/share/man/man8/lslocks.8.gz 
│                │                       ├ [116]: usr/share/man/man8/lsns.8.gz 
│                │                       ├ [117]: usr/share/man/man8/mkfs.8.gz 
│                │                       ├ [118]: usr/share/man/man8/mkfs.bfs.8.gz 
│                │                       ├ [119]: usr/share/man/man8/mkfs.cramfs.8.gz 
│                │                       ├ [120]: usr/share/man/man8/mkfs.minix.8.gz 
│                │                       ├ [121]: usr/share/man/man8/mkswap.8.gz 
│                │                       ├ [122]: usr/share/man/man8/mount.8.gz 
│                │                       ├ [123]: usr/share/man/man8/pam_lastlog2.8.gz 
│                │                       ├ [124]: usr/share/man/man8/partx.8.gz 
│                │                       ├ [125]: usr/share/man/man8/pivot_root.8.gz 
│                │                       ├ [126]: usr/share/man/man8/readprofile.8.gz 
│                │                       ├ [127]: usr/share/man/man8/resizepart.8.gz 
│                │                       ├ [128]: usr/share/man/man8/rfkill.8.gz 
│                │                       ├ [129]: usr/share/man/man8/rtcwake.8.gz 
│                │                       ├ [130]: usr/share/man/man8/setarch.8.gz 
│                │                       ├ [131]: usr/share/man/man8/sfdisk.8.gz 
│                │                       ├ [132]: usr/share/man/man8/swaplabel.8.gz 
│                │                       ├ [133]: usr/share/man/man8/swapoff.8.gz 
│                │                       ├ [134]: usr/share/man/man8/swapon.8.gz 
│                │                       ├ [135]: usr/share/man/man8/switch_root.8.gz 
│                │                       ├ [136]: usr/share/man/man8/umount.8.gz 
│                │                       ├ [137]: usr/share/man/man8/uname26.8.gz 
│                │                       ├ [138]: usr/share/man/man8/wdctl.8.gz 
│                │                       ├ [139]: usr/share/man/man8/wipefs.8.gz 
│                │                       ├ [140]: usr/share/man/man8/x86_64.8.gz 
│                │                       ╰ [141]: usr/share/man/man8/zramctl.8.gz 
│                ├ [60] ╭ ID            : utmps-libs@0.1.3.1-r0 
│                │      ├ Name          : utmps-libs 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/utmps-libs@0.1.3.1-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 68dd637551201f63 
│                │      ├ Version       : 0.1.3.1-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : utmps 
│                │      ├ SrcVersion    : 0.1.3.1-r0 
│                │      ├ Licenses       ─ [0]: ISC 
│                │      ├ Maintainer    : Laurent Bercot <ska-devel@skarnet.org> 
│                │      ├ DependsOn      ╭ [0]: musl@1.2.5-r21 
│                │      │                ╰ [1]: skalibs-libs@2.14.4.0-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:d1b08eb3000d104b5670bf768af4384591021538 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libutmps.so.0.1 
│                │                       ╰ [1]: usr/lib/libutmps.so.0.1.3.1 
│                ├ [61] ╭ ID            : vim@9.1.1952-r0 
│                │      ├ Name          : vim 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/vim@9.1.1952-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : daa5b7fbda8eb7f5 
│                │      ├ Version       : 9.1.1952-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : vim 
│                │      ├ SrcVersion    : 9.1.1952-r0 
│                │      ├ Licenses       ─ [0]: Vim 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ╭ [0]: libncursesw@6.5_p20251123-r0 
│                │      │                ├ [1]: musl@1.2.5-r21 
│                │      │                ├ [2]: vim-common@9.1.1952-r0 
│                │      │                ╰ [3]: xxd@9.1.1952-r0 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:f394d93f81116461f61c94abbfd9ec6f77333731 
│                │      ╰ InstalledFiles ╭ [0]: usr/bin/ex 
│                │                       ├ [1]: usr/bin/rview 
│                │                       ├ [2]: usr/bin/rvim 
│                │                       ├ [3]: usr/bin/view 
│                │                       ╰ [4]: usr/bin/vim 
│                ├ [62] ╭ ID            : vim-common@9.1.1952-r0 
│                │      ├ Name          : vim-common 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/vim-common@9.1.1952-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 87505353fde7a261 
│                │      ├ Version       : 9.1.1952-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : vim 
│                │      ├ SrcVersion    : 9.1.1952-r0 
│                │      ├ Licenses       ─ [0]: Vim 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:05c3ff0ed47b4afbb89abca7f39bdba414a49135 
│                │      ╰ InstalledFiles ╭ [0]   : etc/vim/vimrc 
│                │                       ├ [1]   : usr/share/vim/vim91/LICENSE 
│                │                       ├ [2]   : usr/share/vim/vim91/README.txt 
│                │                       ├ [3]   : usr/share/vim/vim91/bugreport.vim 
│                │                       ├ [4]   : usr/share/vim/vim91/defaults.vim 
│                │                       ├ [5]   : usr/share/vim/vim91/delmenu.vim 
│                │                       ├ [6]   : usr/share/vim/vim91/evim.vim 
│                │                       ├ [7]   : usr/share/vim/vim91/filetype.vim 
│                │                       ├ [8]   : usr/share/vim/vim91/ftoff.vim 
│                │                       ├ [9]   : usr/share/vim/vim91/ftplugin.vim 
│                │                       ├ [10]  : usr/share/vim/vim91/ftplugof.vim 
│                │                       ├ [11]  : usr/share/vim/vim91/gvimrc_example.vim 
│                │                       ├ [12]  : usr/share/vim/vim91/indent.vim 
│                │                       ├ [13]  : usr/share/vim/vim91/indoff.vim 
│                │                       ├ [14]  : usr/share/vim/vim91/menu.vim 
│                │                       ├ [15]  : usr/share/vim/vim91/mswin.vim 
│                │                       ├ [16]  : usr/share/vim/vim91/optwin.vim 
│                │                       ├ [17]  : usr/share/vim/vim91/scripts.vim 
│                │                       ├ [18]  : usr/share/vim/vim91/synmenu.vim 
│                │                       ├ [19]  : usr/share/vim/vim91/vimrc_example.vim 
│                │                       ├ [20]  : usr/share/vim/vim91/autoload/README.txt 
│                │                       ├ [21]  : usr/share/vim/vim91/autoload/RstFold.vim 
│                │                       ├ [22]  : usr/share/vim/vim91/autoload/ada.vim 
│                │                       ├ [23]  : usr/share/vim/vim91/autoload/adacomplete.vim 
│                │                       ├ [24]  : usr/share/vim/vim91/autoload/bitbake.vim 
│                │                       ├ [25]  : usr/share/vim/vim91/autoload/cargo.vim 
│                │                       ├ [26]  : usr/share/vim/vim91/autoload/ccomplete.vim 
│                │                       ├ [27]  : usr/share/vim/vim91/autoload/clojurecomplete.vim 
│                │                       ├ [28]  : usr/share/vim/vim91/autoload/context.vim 
│                │                       ├ [29]  : usr/share/vim/vim91/autoload/contextcomplete.vim 
│                │                       ├ [30]  : usr/share/vim/vim91/autoload/csscomplete.vim 
│                │                       ├ [31]  : usr/share/vim/vim91/autoload/decada.vim 
│                │                       ├ [32]  : usr/share/vim/vim91/autoload/freebasic.vim 
│                │                       ├ [33]  : usr/share/vim/vim91/autoload/getscript.vim 
│                │                       ├ [34]  : usr/share/vim/vim91/autoload/gnat.vim 
│                │                       ├ [35]  : usr/share/vim/vim91/autoload/gzip.vim 
│                │                       ├ [36]  : usr/share/vim/vim91/autoload/hare.vim 
│                │                       ├ [37]  : usr/share/vim/vim91/autoload/haskellcomplete.vim 
│                │                       ├ [38]  : usr/share/vim/vim91/autoload/hcl.vim 
│                │                       ├ [39]  : usr/share/vim/vim91/autoload/htmlcomplete.vim 
│                │                       ├ [40]  : usr/share/vim/vim91/autoload/htmlfold.vim 
│                │                       ├ [41]  : usr/share/vim/vim91/autoload/javaformat.vim 
│                │                       ├ [42]  : usr/share/vim/vim91/autoload/javascriptcomplete.vim 
│                │                       ├ [43]  : usr/share/vim/vim91/autoload/modula2.vim 
│                │                       ├ [44]  : usr/share/vim/vim91/autoload/paste.vim 
│                │                       ├ [45]  : usr/share/vim/vim91/autoload/phpcomplete.vim 
│                │                       ├ [46]  : usr/share/vim/vim91/autoload/python.vim 
│                │                       ├ [47]  : usr/share/vim/vim91/autoload/python3complete.vim 
│                │                       ├ [48]  : usr/share/vim/vim91/autoload/pythoncomplete.vim 
│                │                       ├ [49]  : usr/share/vim/vim91/autoload/racket.vim 
│                │                       ├ [50]  : usr/share/vim/vim91/autoload/rubycomplete.vim 
│                │                       ├ [51]  : usr/share/vim/vim91/autoload/rust.vim 
│                │                       ├ [52]  : usr/share/vim/vim91/autoload/rustfmt.vim 
│                │                       ├ [53]  : usr/share/vim/vim91/autoload/spellfile.vim 
│                │                       ├ [54]  : usr/share/vim/vim91/autoload/spotbugs.vim 
│                │                       ├ [55]  : usr/share/vim/vim91/autoload/sqlcomplete.vim 
│                │                       ├ [56]  : usr/share/vim/vim91/autoload/syntaxcomplete.vim 
│                │                       ├ [57]  : usr/share/vim/vim91/autoload/tar.vim 
│                │                       ├ [58]  : usr/share/vim/vim91/autoload/tohtml.vim 
│                │                       ├ [59]  : usr/share/vim/vim91/autoload/tutor.vim 
│                │                       ├ [60]  : usr/share/vim/vim91/autoload/typeset.vim 
│                │                       ├ [61]  : usr/share/vim/vim91/autoload/typst.vim 
│                │                       ├ [62]  : usr/share/vim/vim91/autoload/vimball.vim 
│                │                       ├ [63]  : usr/share/vim/vim91/autoload/vimcomplete.vim 
│                │                       ├ [64]  : usr/share/vim/vim91/autoload/vimgoto.vim 
│                │                       ├ [65]  : usr/share/vim/vim91/autoload/xmlcomplete.vim 
│                │                       ├ [66]  : usr/share/vim/vim91/autoload/xmlformat.vim 
│                │                       ├ [67]  : usr/share/vim/vim91/autoload/zip.vim 
│                │                       ├ [68]  : usr/share/vim/vim91/autoload/cargo/quickfix.vim 
│                │                       ├ [69]  : usr/share/vim/vim91/autoload/dist/ft.vim 
│                │                       ├ [70]  : usr/share/vim/vim91/autoload/dist/json.vim 
│                │                       ├ [71]  : usr/share/vim/vim91/autoload/dist/man.vim 
│                │                       ├ [72]  : usr/share/vim/vim91/autoload/dist/script.vim 
│                │                       ├ [73]  : usr/share/vim/vim91/autoload/dist/vim.vim 
│                │                       ├ [74]  : usr/share/vim/vim91/autoload/dist/vim9.vim 
│                │                       ├ [75]  : usr/share/vim/vim91/autoload/dist/vimindent.vim 
│                │                       ├ [76]  : usr/share/vim/vim91/autoload/rust/debugging.vim 
│                │                       ├ [77]  : usr/share/vim/vim91/autoload/xml/html32.vim 
│                │                       ├ [78]  : usr/share/vim/vim91/autoload/xml/html401f.vim 
│                │                       ├ [79]  : usr/share/vim/vim91/autoload/xml/html401s.vim 
│                │                       ├ [80]  : usr/share/vim/vim91/autoload/xml/html401t.vim 
│                │                       ├ [81]  : usr/share/vim/vim91/autoload/xml/html40f.vim 
│                │                       ├ [82]  : usr/share/vim/vim91/autoload/xml/html40s.vim 
│                │                       ├ [83]  : usr/share/vim/vim91/autoload/xml/html40t.vim 
│                │                       ├ [84]  : usr/share/vim/vim91/autoload/xml/xhtml10f.vim 
│                │                       ├ [85]  : usr/share/vim/vim91/autoload/xml/xhtml10s.vim 
│                │                       ├ [86]  : usr/share/vim/vim91/autoload/xml/xhtml10t.vim 
│                │                       ├ [87]  : usr/share/vim/vim91/autoload/xml/xhtml11.vim 
│                │                       ├ [88]  : usr/share/vim/vim91/autoload/xml/xsd.vim 
│                │                       ├ [89]  : usr/share/vim/vim91/autoload/xml/xsl.vim 
│                │                       ├ [90]  : usr/share/vim/vim91/colors/README.txt 
│                │                       ├ [91]  : usr/share/vim/vim91/colors/blue.vim 
│                │                       ├ [92]  : usr/share/vim/vim91/colors/darkblue.vim 
│                │                       ├ [93]  : usr/share/vim/vim91/colors/default.vim 
│                │                       ├ [94]  : usr/share/vim/vim91/colors/delek.vim 
│                │                       ├ [95]  : usr/share/vim/vim91/colors/desert.vim 
│                │                       ├ [96]  : usr/share/vim/vim91/colors/elflord.vim 
│                │                       ├ [97]  : usr/share/vim/vim91/colors/evening.vim 
│                │                       ├ [98]  : usr/share/vim/vim91/colors/habamax.vim 
│                │                       ├ [99]  : usr/share/vim/vim91/colors/industry.vim 
│                │                       ├ [100] : usr/share/vim/vim91/colors/koehler.vim 
│                │                       ├ [101] : usr/share/vim/vim91/colors/lunaperche.vim 
│                │                       ├ [102] : usr/share/vim/vim91/colors/morning.vim 
│                │                       ├ [103] : usr/share/vim/vim91/colors/murphy.vim 
│                │                       ├ [104] : usr/share/vim/vim91/colors/pablo.vim 
│                │                       ├ [105] : usr/share/vim/vim91/colors/peachpuff.vim 
│                │                       ├ [106] : usr/share/vim/vim91/colors/quiet.vim 
│                │                       ├ [107] : usr/share/vim/vim91/colors/retrobox.vim 
│                │                       ├ [108] : usr/share/vim/vim91/colors/ron.vim 
│                │                       ├ [109] : usr/share/vim/vim91/colors/shine.vim 
│                │                       ├ [110] : usr/share/vim/vim91/colors/slate.vim 
│                │                       ├ [111] : usr/share/vim/vim91/colors/sorbet.vim 
│                │                       ├ [112] : usr/share/vim/vim91/colors/torte.vim 
│                │                       ├ [113] : usr/share/vim/vim91/colors/unokai.vim 
│                │                       ├ [114] : usr/share/vim/vim91/colors/wildcharm.vim 
│                │                       ├ [115] : usr/share/vim/vim91/colors/zaibatsu.vim 
│                │                       ├ [116] : usr/share/vim/vim91/colors/zellner.vim 
│                │                       ├ [117] : usr/share/vim/vim91/colors/lists/csscolors.vim 
│                │                       ├ [118] : usr/share/vim/vim91/colors/lists/default.vim 
│                │                       ├ [119] : usr/share/vim/vim91/colors/tools/check_colors.vim 
│                │                       ├ [120] : usr/share/vim/vim91/compiler/README.txt 
│                │                       ├ [121] : usr/share/vim/vim91/compiler/ant.vim 
│                │                       ├ [122] : usr/share/vim/vim91/compiler/bash.vim 
│                │                       ├ [123] : usr/share/vim/vim91/compiler/bcc.vim 
│                │                       ├ [124] : usr/share/vim/vim91/compiler/bdf.vim 
│                │                       ├ [125] : usr/share/vim/vim91/compiler/biome.vim 
│                │                       ├ [126] : usr/share/vim/vim91/compiler/cargo.vim 
│                │                       ├ [127] : usr/share/vim/vim91/compiler/checkstyle.vim 
│                │                       ├ [128] : usr/share/vim/vim91/compiler/cm3.vim 
│                │                       ├ [129] : usr/share/vim/vim91/compiler/context.vim 
│                │                       ├ [130] : usr/share/vim/vim91/compiler/cppcheck.vim 
│                │                       ├ [131] : usr/share/vim/vim91/compiler/cs.vim 
│                │                       ├ [132] : usr/share/vim/vim91/compiler/csslint.vim 
│                │                       ├ [133] : usr/share/vim/vim91/compiler/cucumber.vim 
│                │                       ├ [134] : usr/share/vim/vim91/compiler/dart.vim 
│                │                       ├ [135] : usr/share/vim/vim91/compiler/dart2js.vim 
│                │                       ├ [136] : usr/share/vim/vim91/compiler/dart2native.vim 
│                │                       ├ [137] : usr/share/vim/vim91/compiler/dartanalyser.vim 
│                │                       ├ [138] : usr/share/vim/vim91/compiler/dartdevc.vim 
│                │                       ├ [139] : usr/share/vim/vim91/compiler/dartdoc.vim 
│                │                       ├ [140] : usr/share/vim/vim91/compiler/dartfmt.vim 
│                │                       ├ [141] : usr/share/vim/vim91/compiler/decada.vim 
│                │                       ├ [142] : usr/share/vim/vim91/compiler/dot.vim 
│                │                       ├ [143] : usr/share/vim/vim91/compiler/dotnet.vim 
│                │                       ├ [144] : usr/share/vim/vim91/compiler/erlang.vim 
│                │                       ├ [145] : usr/share/vim/vim91/compiler/eruby.vim 
│                │                       ├ [146] : usr/share/vim/vim91/compiler/eslint.vim 
│                │                       ├ [147] : usr/share/vim/vim91/compiler/fbc.vim 
│                │                       ├ [148] : usr/share/vim/vim91/compiler/fortran_F.vim 
│                │                       ├ [149] : usr/share/vim/vim91/compiler/fortran_cv.vim 
│                │                       ├ [150] : usr/share/vim/vim91/compiler/fortran_elf90.vim 
│                │                       ├ [151] : usr/share/vim/vim91/compiler/fortran_g77.vim 
│                │                       ├ [152] : usr/share/vim/vim91/compiler/fortran_lf95.vim 
│                │                       ├ [153] : usr/share/vim/vim91/compiler/fpc.vim 
│                │                       ├ [154] : usr/share/vim/vim91/compiler/g95.vim 
│                │                       ├ [155] : usr/share/vim/vim91/compiler/gawk.vim 
│                │                       ├ [156] : usr/share/vim/vim91/compiler/gcc.vim 
│                │                       ├ [157] : usr/share/vim/vim91/compiler/gfortran.vim 
│                │                       ├ [158] : usr/share/vim/vim91/compiler/ghc.vim 
│                │                       ├ [159] : usr/share/vim/vim91/compiler/gjs.vim 
│                │                       ├ [160] : usr/share/vim/vim91/compiler/gleam_build.vim 
│                │                       ├ [161] : usr/share/vim/vim91/compiler/gm2.vim 
│                │                       ├ [162] : usr/share/vim/vim91/compiler/gnat.vim 
│                │                       ├ [163] : usr/share/vim/vim91/compiler/go.vim 
│                │                       ├ [164] : usr/share/vim/vim91/compiler/groff.vim 
│                │                       ├ [165] : usr/share/vim/vim91/compiler/haml.vim 
│                │                       ├ [166] : usr/share/vim/vim91/compiler/hare.vim 
│                │                       ├ [167] : usr/share/vim/vim91/compiler/hp_acc.vim 
│                │                       ├ [168] : usr/share/vim/vim91/compiler/icc.vim 
│                │                       ├ [169] : usr/share/vim/vim91/compiler/icon.vim 
│                │                       ├ [170] : usr/share/vim/vim91/compiler/ifort.vim 
│                │                       ├ [171] : usr/share/vim/vim91/compiler/intel.vim 
│                │                       ├ [172] : usr/share/vim/vim91/compiler/irix5_c.vim 
│                │                       ├ [173] : usr/share/vim/vim91/compiler/irix5_cpp.vim 
│                │                       ├ [174] : usr/share/vim/vim91/compiler/javac.vim 
│                │                       ├ [175] : usr/share/vim/vim91/compiler/jest.vim 
│                │                       ├ [176] : usr/share/vim/vim91/compiler/jikes.vim 
│                │                       ├ [177] : usr/share/vim/vim91/compiler/jjs.vim 
│                │                       ├ [178] : usr/share/vim/vim91/compiler/jq.vim 
│                │                       ├ [179] : usr/share/vim/vim91/compiler/jshint.vim 
│                │                       ├ [180] : usr/share/vim/vim91/compiler/jsonlint.vim 
│                │                       ├ [181] : usr/share/vim/vim91/compiler/make.vim 
│                │                       ├ [182] : usr/share/vim/vim91/compiler/maven.vim 
│                │                       ├ [183] : usr/share/vim/vim91/compiler/mcs.vim 
│                │                       ├ [184] : usr/share/vim/vim91/compiler/mips_c.vim 
│                │                       ├ [185] : usr/share/vim/vim91/compiler/mipspro_c89.vim 
│                │                       ├ [186] : usr/share/vim/vim91/compiler/mipspro_cpp.vim 
│                │                       ├ [187] : usr/share/vim/vim91/compiler/modelsim_vcom.vim 
│                │                       ├ [188] : usr/share/vim/vim91/compiler/msbuild.vim 
│                │                       ├ [189] : usr/share/vim/vim91/compiler/msvc.vim 
│                │                       ├ [190] : usr/share/vim/vim91/compiler/mypy.vim 
│                │                       ├ [191] : usr/share/vim/vim91/compiler/neato.vim 
│                │                       ├ [192] : usr/share/vim/vim91/compiler/ocaml.vim 
│                │                       ├ [193] : usr/share/vim/vim91/compiler/onsgmls.vim 
│                │                       ├ [194] : usr/share/vim/vim91/compiler/pandoc.vim 
│                │                       ├ [195] : usr/share/vim/vim91/compiler/pbx.vim 
│                │                       ├ [196] : usr/share/vim/vim91/compiler/perl.vim 
│                │                       ├ [197] : usr/share/vim/vim91/compiler/perlcritic.vim 
│                │                       ├ [198] : usr/share/vim/vim91/compiler/php.vim 
│                │                       ├ [199] : usr/share/vim/vim91/compiler/phpstan.vim 
│                │                       ├ [200] : usr/share/vim/vim91/compiler/pip_compile.vim 
│                │                       ├ [201] : usr/share/vim/vim91/compiler/podchecker.vim 
│                │                       ├ [202] : usr/share/vim/vim91/compiler/powershell.vim 
│                │                       ├ [203] : usr/share/vim/vim91/compiler/pylint.vim 
│                │                       ├ [204] : usr/share/vim/vim91/compiler/pytest.vim 
│                │                       ├ [205] : usr/share/vim/vim91/compiler/pyunit.vim 
│                │                       ├ [206] : usr/share/vim/vim91/compiler/raco.vim 
│                │                       ├ [207] : usr/share/vim/vim91/compiler/racomake.vim 
│                │                       ├ [208] : usr/share/vim/vim91/compiler/racosetup.vim 
│                │                       ├ [209] : usr/share/vim/vim91/compiler/racotest.vim 
│                │                       ├ [210] : usr/share/vim/vim91/compiler/rake.vim 
│                │                       ├ [211] : usr/share/vim/vim91/compiler/rhino.vim 
│                │                       ├ [212] : usr/share/vim/vim91/compiler/rime_deployer.vim 
│                │                       ├ [213] : usr/share/vim/vim91/compiler/rspec.vim 
│                │                       ├ [214] : usr/share/vim/vim91/compiler/rst.vim 
│                │                       ├ [215] : usr/share/vim/vim91/compiler/rubocop.vim 
│                │                       ├ [216] : usr/share/vim/vim91/compiler/ruby.vim 
│                │                       ├ [217] : usr/share/vim/vim91/compiler/rubyunit.vim 
│                │                       ├ [218] : usr/share/vim/vim91/compiler/ruff.vim 
│                │                       ├ [219] : usr/share/vim/vim91/compiler/rustc.vim 
│                │                       ├ [220] : usr/share/vim/vim91/compiler/sass.vim 
│                │                       ├ [221] : usr/share/vim/vim91/compiler/scdoc.vim 
│                │                       ├ [222] : usr/share/vim/vim91/compiler/se.vim 
│                │                       ├ [223] : usr/share/vim/vim91/compiler/shellcheck.vim 
│                │                       ├ [224] : usr/share/vim/vim91/compiler/sml.vim 
│                │                       ├ [225] : usr/share/vim/vim91/compiler/spectral.vim 
│                │                       ├ [226] : usr/share/vim/vim91/compiler/splint.vim 
│                │                       ├ [227] : usr/share/vim/vim91/compiler/spotbugs.vim 
│                │                       ├ [228] : usr/share/vim/vim91/compiler/stack.vim 
│                │                       ├ [229] : usr/share/vim/vim91/compiler/standard.vim 
│                │                       ├ [230] : usr/share/vim/vim91/compiler/stylelint.vim 
│                │                       ├ [231] : usr/share/vim/vim91/compiler/svelte-check.vim 
│                │                       ├ [232] : usr/share/vim/vim91/compiler/tcl.vim 
│                │                       ├ [233] : usr/share/vim/vim91/compiler/tex.vim 
│                │                       ├ [234] : usr/share/vim/vim91/compiler/tidy.vim 
│                │                       ├ [235] : usr/share/vim/vim91/compiler/tombi.vim 
│                │                       ├ [236] : usr/share/vim/vim91/compiler/ts-node.vim 
│                │                       ├ [237] : usr/share/vim/vim91/compiler/tsc.vim 
│                │                       ├ [238] : usr/share/vim/vim91/compiler/typedoc.vim 
│                │                       ├ [239] : usr/share/vim/vim91/compiler/typst.vim 
│                │                       ├ [240] : usr/share/vim/vim91/compiler/vimdoc.vim 
│                │                       ├ [241] : usr/share/vim/vim91/compiler/xbuild.vim 
│                │                       ├ [242] : usr/share/vim/vim91/compiler/xmllint.vim 
│                │                       ├ [243] : usr/share/vim/vim91/compiler/xmlwf.vim 
│                │                       ├ [244] : usr/share/vim/vim91/compiler/xo.vim 
│                │                       ├ [245] : usr/share/vim/vim91/compiler/yamllint.vim 
│                │                       ├ [246] : usr/share/vim/vim91/compiler/zig.vim 
│                │                       ├ [247] : usr/share/vim/vim91/compiler/zig_build.vim 
│                │                       ├ [248] : usr/share/vim/vim91/compiler/zig_build_exe.vim 
│                │                       ├ [249] : usr/share/vim/vim91/compiler/zig_test.vim 
│                │                       ├ [250] : usr/share/vim/vim91/compiler/zsh.vim 
│                │                       ├ [251] : usr/share/vim/vim91/doc/arabic.txt 
│                │                       ├ [252] : usr/share/vim/vim91/doc/autocmd.txt 
│                │                       ├ [253] : usr/share/vim/vim91/doc/builtin.txt 
│                │                       ├ [254] : usr/share/vim/vim91/doc/change.txt 
│                │                       ├ [255] : usr/share/vim/vim91/doc/channel.txt 
│                │                       ├ [256] : usr/share/vim/vim91/doc/cmdline.txt 
│                │                       ├ [257] : usr/share/vim/vim91/doc/debug.txt 
│                │                       ├ [258] : usr/share/vim/vim91/doc/debugger.txt 
│                │                       ├ [259] : usr/share/vim/vim91/doc/develop.txt 
│                │                       ├ [260] : usr/share/vim/vim91/doc/diff.txt 
│                │                       ├ [261] : usr/share/vim/vim91/doc/digraph.txt 
│                │                       ├ [262] : usr/share/vim/vim91/doc/editing.txt 
│                │                       ├ [263] : usr/share/vim/vim91/doc/eval.txt 
│                │                       ├ [264] : usr/share/vim/vim91/doc/farsi.txt 
│                │                       ├ [265] : usr/share/vim/vim91/doc/filetype.txt 
│                │                       ├ [266] : usr/share/vim/vim91/doc/fold.txt 
│                │                       ├ [267] : usr/share/vim/vim91/doc/ft_ada.txt 
│                │                       ├ [268] : usr/share/vim/vim91/doc/ft_context.txt 
│                │                       ├ [269] : usr/share/vim/vim91/doc/ft_hare.txt 
│                │                       ├ [270] : usr/share/vim/vim91/doc/ft_mp.txt 
│                │                       ├ [271] : usr/share/vim/vim91/doc/ft_ps1.txt 
│                │                       ├ [272] : usr/share/vim/vim91/doc/ft_raku.txt 
│                │                       ├ [273] : usr/share/vim/vim91/doc/ft_rust.txt 
│                │                       ├ [274] : usr/share/vim/vim91/doc/ft_sql.txt 
│                │                       ├ [275] : usr/share/vim/vim91/doc/gui.txt 
│                │                       ├ [276] : usr/share/vim/vim91/doc/gui_w32.txt 
│                │                       ├ [277] : usr/share/vim/vim91/doc/gui_x11.txt 
│                │                       ├ [278] : usr/share/vim/vim91/doc/hangulin.txt 
│                │                       ├ [279] : usr/share/vim/vim91/doc/hebrew.txt 
│                │                       ├ [280] : usr/share/vim/vim91/doc/help.txt 
│                │                       ├ [281] : usr/share/vim/vim91/doc/helphelp.txt 
│                │                       ├ [282] : usr/share/vim/vim91/doc/howto.txt 
│                │                       ├ [283] : usr/share/vim/vim91/doc/if_cscop.txt 
│                │                       ├ [284] : usr/share/vim/vim91/doc/if_lua.txt 
│                │                       ├ [285] : usr/share/vim/vim91/doc/if_mzsch.txt 
│                │                       ├ [286] : usr/share/vim/vim91/doc/if_ole.txt 
│                │                       ├ [287] : usr/share/vim/vim91/doc/if_perl.txt 
│                │                       ├ [288] : usr/share/vim/vim91/doc/if_pyth.txt 
│                │                       ├ [289] : usr/share/vim/vim91/doc/if_ruby.txt 
│                │                       ├ [290] : usr/share/vim/vim91/doc/if_sniff.txt 
│                │                       ├ [291] : usr/share/vim/vim91/doc/if_tcl.txt 
│                │                       ├ [292] : usr/share/vim/vim91/doc/indent.txt 
│                │                       ├ [293] : usr/share/vim/vim91/doc/index.txt 
│                │                       ├ [294] : usr/share/vim/vim91/doc/insert.txt 
│                │                       ├ [295] : usr/share/vim/vim91/doc/intro.txt 
│                │                       ├ [296] : usr/share/vim/vim91/doc/map.txt 
│                │                       ├ [297] : usr/share/vim/vim91/doc/mbyte.txt 
│                │                       ├ [298] : usr/share/vim/vim91/doc/message.txt 
│                │                       ├ [299] : usr/share/vim/vim91/doc/mlang.txt 
│                │                       ├ [300] : usr/share/vim/vim91/doc/motion.txt 
│                │                       ├ [301] : usr/share/vim/vim91/doc/netbeans.txt 
│                │                       ├ [302] : usr/share/vim/vim91/doc/options.txt 
│                │                       ├ [303] : usr/share/vim/vim91/doc/os_390.txt 
│                │                       ├ [304] : usr/share/vim/vim91/doc/os_amiga.txt 
│                │                       ├ [305] : usr/share/vim/vim91/doc/os_beos.txt 
│                │                       ├ [306] : usr/share/vim/vim91/doc/os_dos.txt 
│                │                       ├ [307] : usr/share/vim/vim91/doc/os_haiku.txt 
│                │                       ├ [308] : usr/share/vim/vim91/doc/os_mac.txt 
│                │                       ├ [309] : usr/share/vim/vim91/doc/os_mint.txt 
│                │                       ├ [310] : usr/share/vim/vim91/doc/os_msdos.txt 
│                │                       ├ [311] : usr/share/vim/vim91/doc/os_os2.txt 
│                │                       ├ [312] : usr/share/vim/vim91/doc/os_qnx.txt 
│                │                       ├ [313] : usr/share/vim/vim91/doc/os_risc.txt 
│                │                       ├ [314] : usr/share/vim/vim91/doc/os_unix.txt 
│                │                       ├ [315] : usr/share/vim/vim91/doc/os_vms.txt 
│                │                       ├ [316] : usr/share/vim/vim91/doc/os_win32.txt 
│                │                       ├ [317] : usr/share/vim/vim91/doc/pattern.txt 
│                │                       ├ [318] : usr/share/vim/vim91/doc/pi_getscript.txt 
│                │                       ├ [319] : usr/share/vim/vim91/doc/pi_gzip.txt 
│                │                       ├ [320] : usr/share/vim/vim91/doc/pi_logipat.txt 
│                │                       ├ [321] : usr/share/vim/vim91/doc/pi_netrw.txt 
│                │                       ├ [322] : usr/share/vim/vim91/doc/pi_paren.txt 
│                │                       ├ [323] : usr/share/vim/vim91/doc/pi_spec.txt 
│                │                       ├ [324] : usr/share/vim/vim91/doc/pi_tar.txt 
│                │                       ├ [325] : usr/share/vim/vim91/doc/pi_tutor.txt 
│                │                       ├ [326] : usr/share/vim/vim91/doc/pi_vimball.txt 
│                │                       ├ [327] : usr/share/vim/vim91/doc/pi_zip.txt 
│                │                       ├ [328] : usr/share/vim/vim91/doc/popup.txt 
│                │                       ├ [329] : usr/share/vim/vim91/doc/print.txt 
│                │                       ├ [330] : usr/share/vim/vim91/doc/quickfix.txt 
│                │                       ├ [331] : usr/share/vim/vim91/doc/quickref.txt 
│                │                       ├ [332] : usr/share/vim/vim91/doc/quotes.txt 
│                │                       ├ [333] : usr/share/vim/vim91/doc/recover.txt 
│                │                       ├ [334] : usr/share/vim/vim91/doc/remote.txt 
│                │                       ├ [335] : usr/share/vim/vim91/doc/repeat.txt 
│                │                       ├ [336] : usr/share/vim/vim91/doc/rileft.txt 
│                │                       ├ [337] : usr/share/vim/vim91/doc/russian.txt 
│                │                       ├ [338] : usr/share/vim/vim91/doc/scroll.txt 
│                │                       ├ [339] : usr/share/vim/vim91/doc/sign.txt 
│                │                       ├ [340] : usr/share/vim/vim91/doc/spell.txt 
│                │                       ├ [341] : usr/share/vim/vim91/doc/sponsor.txt 
│                │                       ├ [342] : usr/share/vim/vim91/doc/starting.txt 
│                │                       ├ [343] : usr/share/vim/vim91/doc/syntax.txt 
│                │                       ├ [344] : usr/share/vim/vim91/doc/tabpage.txt 
│                │                       ├ [345] : usr/share/vim/vim91/doc/tags 
│                │                       ├ [346] : usr/share/vim/vim91/doc/tagsrch.txt 
│                │                       ├ [347] : usr/share/vim/vim91/doc/term.txt 
│                │                       ├ [348] : usr/share/vim/vim91/doc/terminal.txt 
│                │                       ├ [349] : usr/share/vim/vim91/doc/testing.txt 
│                │                       ├ [350] : usr/share/vim/vim91/doc/textprop.txt 
│                │                       ├ [351] : usr/share/vim/vim91/doc/tips.txt 
│                │                       ├ [352] : usr/share/vim/vim91/doc/todo.txt 
│                │                       ├ [353] : usr/share/vim/vim91/doc/uganda.txt 
│                │                       ├ [354] : usr/share/vim/vim91/doc/undo.txt 
│                │                       ├ [355] : usr/share/vim/vim91/doc/userfunc.txt 
│                │                       ├ [356] : usr/share/vim/vim91/doc/usr_01.txt 
│                │                       ├ [357] : usr/share/vim/vim91/doc/usr_02.txt 
│                │                       ├ [358] : usr/share/vim/vim91/doc/usr_03.txt 
│                │                       ├ [359] : usr/share/vim/vim91/doc/usr_04.txt 
│                │                       ├ [360] : usr/share/vim/vim91/doc/usr_05.txt 
│                │                       ├ [361] : usr/share/vim/vim91/doc/usr_06.txt 
│                │                       ├ [362] : usr/share/vim/vim91/doc/usr_07.txt 
│                │                       ├ [363] : usr/share/vim/vim91/doc/usr_08.txt 
│                │                       ├ [364] : usr/share/vim/vim91/doc/usr_09.txt 
│                │                       ├ [365] : usr/share/vim/vim91/doc/usr_10.txt 
│                │                       ├ [366] : usr/share/vim/vim91/doc/usr_11.txt 
│                │                       ├ [367] : usr/share/vim/vim91/doc/usr_12.txt 
│                │                       ├ [368] : usr/share/vim/vim91/doc/usr_20.txt 
│                │                       ├ [369] : usr/share/vim/vim91/doc/usr_21.txt 
│                │                       ├ [370] : usr/share/vim/vim91/doc/usr_22.txt 
│                │                       ├ [371] : usr/share/vim/vim91/doc/usr_23.txt 
│                │                       ├ [372] : usr/share/vim/vim91/doc/usr_24.txt 
│                │                       ├ [373] : usr/share/vim/vim91/doc/usr_25.txt 
│                │                       ├ [374] : usr/share/vim/vim91/doc/usr_26.txt 
│                │                       ├ [375] : usr/share/vim/vim91/doc/usr_27.txt 
│                │                       ├ [376] : usr/share/vim/vim91/doc/usr_28.txt 
│                │                       ├ [377] : usr/share/vim/vim91/doc/usr_29.txt 
│                │                       ├ [378] : usr/share/vim/vim91/doc/usr_30.txt 
│                │                       ├ [379] : usr/share/vim/vim91/doc/usr_31.txt 
│                │                       ├ [380] : usr/share/vim/vim91/doc/usr_32.txt 
│                │                       ├ [381] : usr/share/vim/vim91/doc/usr_40.txt 
│                │                       ├ [382] : usr/share/vim/vim91/doc/usr_41.txt 
│                │                       ├ [383] : usr/share/vim/vim91/doc/usr_42.txt 
│                │                       ├ [384] : usr/share/vim/vim91/doc/usr_43.txt 
│                │                       ├ [385] : usr/share/vim/vim91/doc/usr_44.txt 
│                │                       ├ [386] : usr/share/vim/vim91/doc/usr_45.txt 
│                │                       ├ [387] : usr/share/vim/vim91/doc/usr_50.txt 
│                │                       ├ [388] : usr/share/vim/vim91/doc/usr_51.txt 
│                │                       ├ [389] : usr/share/vim/vim91/doc/usr_52.txt 
│                │                       ├ [390] : usr/share/vim/vim91/doc/usr_90.txt 
│                │                       ├ [391] : usr/share/vim/vim91/doc/usr_toc.txt 
│                │                       ├ [392] : usr/share/vim/vim91/doc/various.txt 
│                │                       ├ [393] : usr/share/vim/vim91/doc/version4.txt 
│                │                       ├ [394] : usr/share/vim/vim91/doc/version5.txt 
│                │                       ├ [395] : usr/share/vim/vim91/doc/version6.txt 
│                │                       ├ [396] : usr/share/vim/vim91/doc/version7.txt 
│                │                       ├ [397] : usr/share/vim/vim91/doc/version8.txt 
│                │                       ├ [398] : usr/share/vim/vim91/doc/version9.txt 
│                │                       ├ [399] : usr/share/vim/vim91/doc/vi_diff.txt 
│                │                       ├ [400] : usr/share/vim/vim91/doc/vietnamese.txt 
│                │                       ├ [401] : usr/share/vim/vim91/doc/vim2html.pl 
│                │                       ├ [402] : usr/share/vim/vim91/doc/vim9.txt 
│                │                       ├ [403] : usr/share/vim/vim91/doc/vim9class.txt 
│                │                       ├ [404] : usr/share/vim/vim91/doc/visual.txt 
│                │                       ├ [405] : usr/share/vim/vim91/doc/wayland.txt 
│                │                       ├ [406] : usr/share/vim/vim91/doc/windows.txt 
│                │                       ├ [407] : usr/share/vim/vim91/doc/workshop.txt 
│                │                       ├ [408] : usr/share/vim/vim91/ftplugin/8th.vim 
│                │                       ├ [409] : usr/share/vim/vim91/ftplugin/README.txt 
│                │                       ├ [410] : usr/share/vim/vim91/ftplugin/a2ps.vim 
│                │                       ├ [411] : usr/share/vim/vim91/ftplugin/aap.vim 
│                │                       ├ [412] : usr/share/vim/vim91/ftplugin/abap.vim 
│                │                       ├ [413] : usr/share/vim/vim91/ftplugin/abaqus.vim 
│                │                       ├ [414] : usr/share/vim/vim91/ftplugin/abnf.vim 
│                │                       ├ [415] : usr/share/vim/vim91/ftplugin/ada.vim 
│                │                       ├ [416] : usr/share/vim/vim91/ftplugin/alsaconf.vim 
│                │                       ├ [417] : usr/share/vim/vim91/ftplugin/ant.vim 
│                │                       ├ [418] : usr/share/vim/vim91/ftplugin/antlr4.vim 
│                │                       ├ [419] : usr/share/vim/vim91/ftplugin/apache.vim 
│                │                       ├ [420] : usr/share/vim/vim91/ftplugin/arch.vim 
│                │                       ├ [421] : usr/share/vim/vim91/ftplugin/arduino.vim 
│                │                       ├ [422] : usr/share/vim/vim91/ftplugin/art.vim 
│                │                       ├ [423] : usr/share/vim/vim91/ftplugin/asciidoc.vim 
│                │                       ├ [424] : usr/share/vim/vim91/ftplugin/asm.vim 
│                │                       ├ [425] : usr/share/vim/vim91/ftplugin/aspvbs.vim 
│                │                       ├ [426] : usr/share/vim/vim91/ftplugin/astro.vim 
│                │                       ├ [427] : usr/share/vim/vim91/ftplugin/asy.vim 
│                │                       ├ [428] : usr/share/vim/vim91/ftplugin/autohotkey.vim 
│                │                       ├ [429] : usr/share/vim/vim91/ftplugin/automake.vim 
│                │                       ├ [430] : usr/share/vim/vim91/ftplugin/autopkgtest.vim 
│                │                       ├ [431] : usr/share/vim/vim91/ftplugin/awk.vim 
│                │                       ├ [432] : usr/share/vim/vim91/ftplugin/bash.vim 
│                │                       ├ [433] : usr/share/vim/vim91/ftplugin/basic.vim 
│                │                       ├ [434] : usr/share/vim/vim91/ftplugin/bdf.vim 
│                │                       ├ [435] : usr/share/vim/vim91/ftplugin/bindzone.vim 
│                │                       ├ [436] : usr/share/vim/vim91/ftplugin/bitbake.vim 
│                │                       ├ [437] : usr/share/vim/vim91/ftplugin/bp.vim 
│                │                       ├ [438] : usr/share/vim/vim91/ftplugin/brighterscript.vim 
│                │                       ├ [439] : usr/share/vim/vim91/ftplugin/brightscript.vim 
│                │                       ├ [440] : usr/share/vim/vim91/ftplugin/bst.vim 
│                │                       ├ [441] : usr/share/vim/vim91/ftplugin/btm.vim 
│                │                       ├ [442] : usr/share/vim/vim91/ftplugin/bzl.vim 
│                │                       ├ [443] : usr/share/vim/vim91/ftplugin/c.vim 
│                │                       ├ [444] : usr/share/vim/vim91/ftplugin/c3.vim 
│                │                       ├ [445] : usr/share/vim/vim91/ftplugin/cabal.vim 
│                │                       ├ [446] : usr/share/vim/vim91/ftplugin/calendar.vim 
│                │                       ├ [447] : usr/share/vim/vim91/ftplugin/cdrdaoconf.vim 
│                │                       ├ [448] : usr/share/vim/vim91/ftplugin/cedar.vim 
│                │                       ├ [449] : usr/share/vim/vim91/ftplugin/cfg.vim 
│                │                       ├ [450] : usr/share/vim/vim91/ftplugin/cgdbrc.vim 
│                │                       ├ [451] : usr/share/vim/vim91/ftplugin/ch.vim 
│                │                       ├ [452] : usr/share/vim/vim91/ftplugin/changelog.vim 
│                │                       ├ [453] : usr/share/vim/vim91/ftplugin/chatito.vim 
│                │                       ├ [454] : usr/share/vim/vim91/ftplugin/chicken.vim 
│                │                       ├ [455] : usr/share/vim/vim91/ftplugin/clojure.vim 
│                │                       ├ [456] : usr/share/vim/vim91/ftplugin/cmake.vim 
│                │                       ├ [457] : usr/share/vim/vim91/ftplugin/cmakecache.vim 
│                │                       ├ [458] : usr/share/vim/vim91/ftplugin/cobol.vim 
│                │                       ├ [459] : usr/share/vim/vim91/ftplugin/codeowners.vim 
│                │                       ├ [460] : usr/share/vim/vim91/ftplugin/conf.vim 
│                │                       ├ [461] : usr/share/vim/vim91/ftplugin/config.vim 
│                │                       ├ [462] : usr/share/vim/vim91/ftplugin/confini.vim 
│                │                       ├ [463] : usr/share/vim/vim91/ftplugin/context.vim 
│                │                       ├ [464] : usr/share/vim/vim91/ftplugin/cook.vim 
│                │                       ├ [465] : usr/share/vim/vim91/ftplugin/corn.vim 
│                │                       ├ [466] : usr/share/vim/vim91/ftplugin/cpp.vim 
│                │                       ├ [467] : usr/share/vim/vim91/ftplugin/crm.vim 
│                │                       ├ [468] : usr/share/vim/vim91/ftplugin/crontab.vim 
│                │                       ├ [469] : usr/share/vim/vim91/ftplugin/cs.vim 
│                │                       ├ [470] : usr/share/vim/vim91/ftplugin/csc.vim 
│                │                       ├ [471] : usr/share/vim/vim91/ftplugin/csh.vim 
│                │                       ├ [472] : usr/share/vim/vim91/ftplugin/css.vim 
│                │                       ├ [473] : usr/share/vim/vim91/ftplugin/csv.vim 
│                │                       ├ [474] : usr/share/vim/vim91/ftplugin/cucumber.vim 
│                │                       ├ [475] : usr/share/vim/vim91/ftplugin/cuda.vim 
│                │                       ├ [476] : usr/share/vim/vim91/ftplugin/cvsrc.vim 
│                │                       ├ [477] : usr/share/vim/vim91/ftplugin/dart.vim 
│                │                       ├ [478] : usr/share/vim/vim91/ftplugin/dax.vim 
│                │                       ├ [479] : usr/share/vim/vim91/ftplugin/deb822sources.vim 
│                │                       ├ [480] : usr/share/vim/vim91/ftplugin/debchangelog.vim 
│                │                       ├ [481] : usr/share/vim/vim91/ftplugin/debcontrol.vim 
│                │                       ├ [482] : usr/share/vim/vim91/ftplugin/debsources.vim 
│                │                       ├ [483] : usr/share/vim/vim91/ftplugin/denyhosts.vim 
│                │                       ├ [484] : usr/share/vim/vim91/ftplugin/desktop.vim 
│                │                       ├ [485] : usr/share/vim/vim91/ftplugin/dictconf.vim 
│                │                       ├ [486] : usr/share/vim/vim91/ftplugin/dictdconf.vim 
│                │                       ├ [487] : usr/share/vim/vim91/ftplugin/diff.vim 
│                │                       ├ [488] : usr/share/vim/vim91/ftplugin/dircolors.vim 
│                │                       ├ [489] : usr/share/vim/vim91/ftplugin/dnsmasq.vim 
│                │                       ├ [490] : usr/share/vim/vim91/ftplugin/docbk.vim 
│                │                       ├ [491] : usr/share/vim/vim91/ftplugin/dockerfile.vim 
│                │                       ├ [492] : usr/share/vim/vim91/ftplugin/dosbatch.vim 
│                │                       ├ [493] : usr/share/vim/vim91/ftplugin/dosini.vim 
│                │                       ├ [494] : usr/share/vim/vim91/ftplugin/dtd.vim 
│                │                       ├ [495] : usr/share/vim/vim91/ftplugin/dtrace.vim 
│                │                       ├ [496] : usr/share/vim/vim91/ftplugin/dts.vim 
│                │                       ├ [497] : usr/share/vim/vim91/ftplugin/dune.vim 
│                │                       ├ [498] : usr/share/vim/vim91/ftplugin/editorconfig.vim 
│                │                       ├ [499] : usr/share/vim/vim91/ftplugin/eiffel.vim 
│                │                       ├ [500] : usr/share/vim/vim91/ftplugin/elinks.vim 
│                │                       ├ [501] : usr/share/vim/vim91/ftplugin/elixir.vim 
│                │                       ├ [502] : usr/share/vim/vim91/ftplugin/elm.vim 
│                │                       ├ [503] : usr/share/vim/vim91/ftplugin/erlang.vim 
│                │                       ├ [504] : usr/share/vim/vim91/ftplugin/eruby.vim 
│                │                       ├ [505] : usr/share/vim/vim91/ftplugin/eterm.vim 
│                │                       ├ [506] : usr/share/vim/vim91/ftplugin/expect.vim 
│                │                       ├ [507] : usr/share/vim/vim91/ftplugin/exports.vim 
│                │                       ├ [508] : usr/share/vim/vim91/ftplugin/falcon.vim 
│                │                       ├ [509] : usr/share/vim/vim91/ftplugin/fennel.vim 
│                │                       ├ [510] : usr/share/vim/vim91/ftplugin/fetchmail.vim 
│                │                       ├ [511] : usr/share/vim/vim91/ftplugin/fga.vim 
│                │                       ├ [512] : usr/share/vim/vim91/ftplugin/fish.vim 
│                │                       ├ [513] : usr/share/vim/vim91/ftplugin/flexwiki.vim 
│                │                       ├ [514] : usr/share/vim/vim91/ftplugin/forth.vim 
│                │                       ├ [515] : usr/share/vim/vim91/ftplugin/fortran.vim 
│                │                       ├ [516] : usr/share/vim/vim91/ftplugin/fpcmake.vim 
│                │                       ├ [517] : usr/share/vim/vim91/ftplugin/framescript.vim 
│                │                       ├ [518] : usr/share/vim/vim91/ftplugin/freebasic.vim 
│                │                       ├ [519] : usr/share/vim/vim91/ftplugin/fstab.vim 
│                │                       ├ [520] : usr/share/vim/vim91/ftplugin/fvwm.vim 
│                │                       ├ [521] : usr/share/vim/vim91/ftplugin/gdb.vim 
│                │                       ├ [522] : usr/share/vim/vim91/ftplugin/gdscript.vim 
│                │                       ├ [523] : usr/share/vim/vim91/ftplugin/gdshader.vim 
│                │                       ├ [524] : usr/share/vim/vim91/ftplugin/gel.vim 
│                │                       ├ [525] : usr/share/vim/vim91/ftplugin/git.vim 
│                │                       ├ [526] : usr/share/vim/vim91/ftplugin/gitattributes.vim 
│                │                       ├ [527] : usr/share/vim/vim91/ftplugin/gitcommit.vim 
│                │                       ├ [528] : usr/share/vim/vim91/ftplugin/gitconfig.vim 
│                │                       ├ [529] : usr/share/vim/vim91/ftplugin/gitignore.vim 
│                │                       ├ [530] : usr/share/vim/vim91/ftplugin/gitrebase.vim 
│                │                       ├ [531] : usr/share/vim/vim91/ftplugin/gitsendemail.vim 
│                │                       ├ [532] : usr/share/vim/vim91/ftplugin/gleam.vim 
│                │                       ├ [533] : usr/share/vim/vim91/ftplugin/go.vim 
│                │                       ├ [534] : usr/share/vim/vim91/ftplugin/goaccess.vim 
│                │                       ├ [535] : usr/share/vim/vim91/ftplugin/gomod.vim 
│                │                       ├ [536] : usr/share/vim/vim91/ftplugin/gpg.vim 
│                │                       ├ [537] : usr/share/vim/vim91/ftplugin/gprof.vim 
│                │                       ├ [538] : usr/share/vim/vim91/ftplugin/graphql.vim 
│                │                       ├ [539] : usr/share/vim/vim91/ftplugin/groff.vim 
│                │                       ├ [540] : usr/share/vim/vim91/ftplugin/groovy.vim 
│                │                       ├ [541] : usr/share/vim/vim91/ftplugin/group.vim 
│                │                       ├ [542] : usr/share/vim/vim91/ftplugin/grub.vim 
│                │                       ├ [543] : usr/share/vim/vim91/ftplugin/gyp.vim 
│                │                       ├ [544] : usr/share/vim/vim91/ftplugin/haml.vim 
│                │                       ├ [545] : usr/share/vim/vim91/ftplugin/hamster.vim 
│                │                       ├ [546] : usr/share/vim/vim91/ftplugin/hare.vim 
│                │                       ├ [547] : usr/share/vim/vim91/ftplugin/haredoc.vim 
│                │                       ├ [548] : usr/share/vim/vim91/ftplugin/haskell.vim 
│                │                       ├ [549] : usr/share/vim/vim91/ftplugin/hcl.vim 
│                │                       ├ [550] : usr/share/vim/vim91/ftplugin/heex.vim 
│                │                       ├ [551] : usr/share/vim/vim91/ftplugin/help.vim 
│                │                       ├ [552] : usr/share/vim/vim91/ftplugin/hgcommit.vim 
│                │                       ├ [553] : usr/share/vim/vim91/ftplugin/hlsplaylist.vim 
│                │                       ├ [554] : usr/share/vim/vim91/ftplugin/hog.vim 
│                │                       ├ [555] : usr/share/vim/vim91/ftplugin/hostconf.vim 
│                │                       ├ [556] : usr/share/vim/vim91/ftplugin/hostsaccess.vim 
│                │                       ├ [557] : usr/share/vim/vim91/ftplugin/html.vim 
│                │                       ├ [558] : usr/share/vim/vim91/ftplugin/htmlangular.vim 
│                │                       ├ [559] : usr/share/vim/vim91/ftplugin/htmldjango.vim 
│                │                       ├ [560] : usr/share/vim/vim91/ftplugin/http.vim 
│                │                       ├ [561] : usr/share/vim/vim91/ftplugin/hurl.vim 
│                │                       ├ [562] : usr/share/vim/vim91/ftplugin/hyprlang.vim 
│                │                       ├ [563] : usr/share/vim/vim91/ftplugin/i3config.vim 
│                │                       ├ [564] : usr/share/vim/vim91/ftplugin/icon.vim 
│                │                       ├ [565] : usr/share/vim/vim91/ftplugin/idris2.vim 
│                │                       ├ [566] : usr/share/vim/vim91/ftplugin/indent.vim 
│                │                       ├ [567] : usr/share/vim/vim91/ftplugin/initex.vim 
│                │                       ├ [568] : usr/share/vim/vim91/ftplugin/ipkg.vim 
│                │                       ├ [569] : usr/share/vim/vim91/ftplugin/ishd.vim 
│                │                       ├ [570] : usr/share/vim/vim91/ftplugin/j.vim 
│                │                       ├ [571] : usr/share/vim/vim91/ftplugin/java.vim 
│                │                       ├ [572] : usr/share/vim/vim91/ftplugin/javacc.vim 
│                │                       ├ [573] : usr/share/vim/vim91/ftplugin/javascript.vim 
│                │                       ├ [574] : usr/share/vim/vim91/ftplugin/javascriptreact.vim 
│                │                       ├ [575] : usr/share/vim/vim91/ftplugin/jjdescription.vim 
│                │                       ├ [576] : usr/share/vim/vim91/ftplugin/jproperties.vim 
│                │                       ├ [577] : usr/share/vim/vim91/ftplugin/jq.vim 
│                │                       ├ [578] : usr/share/vim/vim91/ftplugin/json.vim 
│                │                       ├ [579] : usr/share/vim/vim91/ftplugin/json5.vim 
│                │                       ├ [580] : usr/share/vim/vim91/ftplugin/jsonc.vim 
│                │                       ├ [581] : usr/share/vim/vim91/ftplugin/jsonnet.vim 
│                │                       ├ [582] : usr/share/vim/vim91/ftplugin/jsp.vim 
│                │                       ├ [583] : usr/share/vim/vim91/ftplugin/julia.vim 
│                │                       ├ [584] : usr/share/vim/vim91/ftplugin/just.vim 
│                │                       ├ [585] : usr/share/vim/vim91/ftplugin/karel.vim 
│                │                       ├ [586] : usr/share/vim/vim91/ftplugin/kconfig.vim 
│                │                       ├ [587] : usr/share/vim/vim91/ftplugin/kdl.vim 
│                │                       ├ [588] : usr/share/vim/vim91/ftplugin/kerml.vim 
│                │                       ├ [589] : usr/share/vim/vim91/ftplugin/kivy.vim 
│                │                       ├ [590] : usr/share/vim/vim91/ftplugin/kotlin.vim 
│                │                       ├ [591] : usr/share/vim/vim91/ftplugin/kwt.vim 
│                │                       ├ [592] : usr/share/vim/vim91/ftplugin/lc.vim 
│                │                       ├ [593] : usr/share/vim/vim91/ftplugin/ld.vim 
│                │                       ├ [594] : usr/share/vim/vim91/ftplugin/ldapconf.vim 
│                │                       ├ [595] : usr/share/vim/vim91/ftplugin/leex.vim 
│                │                       ├ [596] : usr/share/vim/vim91/ftplugin/leo.vim 
│                │                       ├ [597] : usr/share/vim/vim91/ftplugin/less.vim 
│                │                       ├ [598] : usr/share/vim/vim91/ftplugin/lex.vim 
│                │                       ├ [599] : usr/share/vim/vim91/ftplugin/lf.vim 
│                │                       ├ [600] : usr/share/vim/vim91/ftplugin/lftp.vim 
│                │                       ├ [601] : usr/share/vim/vim91/ftplugin/libao.vim 
│                │                       ├ [602] : usr/share/vim/vim91/ftplugin/limits.vim 
│                │                       ├ [603] : usr/share/vim/vim91/ftplugin/liquid.vim 
│                │                       ├ [604] : usr/share/vim/vim91/ftplugin/lisp.vim 
│                │                       ├ [605] : usr/share/vim/vim91/ftplugin/livebook.vim 
│                │                       ├ [606] : usr/share/vim/vim91/ftplugin/llvm.vim 
│                │                       ├ [607] : usr/share/vim/vim91/ftplugin/lnk.vim 
│                │                       ├ [608] : usr/share/vim/vim91/ftplugin/lnkmap.vim 
│                │                       ├ [609] : usr/share/vim/vim91/ftplugin/logcheck.vim 
│                │                       ├ [610] : usr/share/vim/vim91/ftplugin/loginaccess.vim 
│                │                       ├ [611] : usr/share/vim/vim91/ftplugin/logindefs.vim 
│                │                       ├ [612] : usr/share/vim/vim91/ftplugin/logtalk.dict 
│                │                       ├ [613] : usr/share/vim/vim91/ftplugin/logtalk.vim 
│                │                       ├ [614] : usr/share/vim/vim91/ftplugin/lprolog.vim 
│                │                       ├ [615] : usr/share/vim/vim91/ftplugin/lua.vim 
│                │                       ├ [616] : usr/share/vim/vim91/ftplugin/luau.vim 
│                │                       ├ [617] : usr/share/vim/vim91/ftplugin/lynx.vim 
│                │                       ├ [618] : usr/share/vim/vim91/ftplugin/m17ndb.vim 
│                │                       ├ [619] : usr/share/vim/vim91/ftplugin/m3build.vim 
│                │                       ├ [620] : usr/share/vim/vim91/ftplugin/m3quake.vim 
│                │                       ├ [621] : usr/share/vim/vim91/ftplugin/m4.vim 
│                │                       ├ [622] : usr/share/vim/vim91/ftplugin/mail.vim 
│                │                       ├ [623] : usr/share/vim/vim91/ftplugin/mailaliases.vim 
│                │                       ├ [624] : usr/share/vim/vim91/ftplugin/mailcap.vim 
│                │                       ├ [625] : usr/share/vim/vim91/ftplugin/make.vim 
│                │                       ├ [626] : usr/share/vim/vim91/ftplugin/man.vim 
│                │                       ├ [627] : usr/share/vim/vim91/ftplugin/manconf.vim 
│                │                       ├ [628] : usr/share/vim/vim91/ftplugin/markdown.vim 
│                │                       ├ [629] : usr/share/vim/vim91/ftplugin/masm.vim 
│                │                       ├ [630] : usr/share/vim/vim91/ftplugin/matlab.vim 
│                │                       ├ [631] : usr/share/vim/vim91/ftplugin/mbsync.vim 
│                │                       ├ [632] : usr/share/vim/vim91/ftplugin/mediawiki.vim 
│                │                       ├ [633] : usr/share/vim/vim91/ftplugin/mermaid.vim 
│                │                       ├ [634] : usr/share/vim/vim91/ftplugin/meson.vim 
│                │                       ├ [635] : usr/share/vim/vim91/ftplugin/mf.vim 
│                │                       ├ [636] : usr/share/vim/vim91/ftplugin/mlir.vim 
│                │                       ├ [637] : usr/share/vim/vim91/ftplugin/mma.vim 
│                │                       ├ [638] : usr/share/vim/vim91/ftplugin/modconf.vim 
│                │                       ├ [639] : usr/share/vim/vim91/ftplugin/modula2.vim 
│                │                       ├ [640] : usr/share/vim/vim91/ftplugin/modula3.vim 
│                │                       ├ [641] : usr/share/vim/vim91/ftplugin/mojo.vim 
│                │                       ├ [642] : usr/share/vim/vim91/ftplugin/mp.vim 
│                │                       ├ [643] : usr/share/vim/vim91/ftplugin/mplayerconf.vim 
│                │                       ├ [644] : usr/share/vim/vim91/ftplugin/mrxvtrc.vim 
│                │                       ├ [645] : usr/share/vim/vim91/ftplugin/msmessages.vim 
│                │                       ├ [646] : usr/share/vim/vim91/ftplugin/mss.vim 
│                │                       ├ [647] : usr/share/vim/vim91/ftplugin/muttrc.vim 
│                │                       ├ [648] : usr/share/vim/vim91/ftplugin/mysql.vim 
│                │                       ├ [649] : usr/share/vim/vim91/ftplugin/nanorc.vim 
│                │                       ├ [650] : usr/share/vim/vim91/ftplugin/neomuttrc.vim 
│                │                       ├ [651] : usr/share/vim/vim91/ftplugin/netrc.vim 
│                │                       ├ [652] : usr/share/vim/vim91/ftplugin/nginx.vim 
│                │                       ├ [653] : usr/share/vim/vim91/ftplugin/nim.vim 
│                │                       ├ [654] : usr/share/vim/vim91/ftplugin/nix.vim 
│                │                       ├ [655] : usr/share/vim/vim91/ftplugin/nroff.vim 
│                │                       ├ [656] : usr/share/vim/vim91/ftplugin/nsis.vim 
│                │                       ├ [657] : usr/share/vim/vim91/ftplugin/nu.vim 
│                │                       ├ [658] : usr/share/vim/vim91/ftplugin/objc.vim 
│                │                       ├ [659] : usr/share/vim/vim91/ftplugin/objcpp.vim 
│                │                       ├ [660] : usr/share/vim/vim91/ftplugin/objdump.vim 
│                │                       ├ [661] : usr/share/vim/vim91/ftplugin/obse.vim 
│                │                       ├ [662] : usr/share/vim/vim91/ftplugin/ocaml.vim 
│                │                       ├ [663] : usr/share/vim/vim91/ftplugin/occam.vim 
│                │                       ├ [664] : usr/share/vim/vim91/ftplugin/octave.vim 
│                │                       ├ [665] : usr/share/vim/vim91/ftplugin/odin.vim 
│                │                       ├ [666] : usr/share/vim/vim91/ftplugin/ondir.vim 
│                │                       ├ [667] : usr/share/vim/vim91/ftplugin/opencl.vim 
│                │                       ├ [668] : usr/share/vim/vim91/ftplugin/openscad.vim 
│                │                       ├ [669] : usr/share/vim/vim91/ftplugin/openvpn.vim 
│                │                       ├ [670] : usr/share/vim/vim91/ftplugin/org.vim 
│                │                       ├ [671] : usr/share/vim/vim91/ftplugin/pamconf.vim 
│                │                       ├ [672] : usr/share/vim/vim91/ftplugin/pascal.vim 
│                │                       ├ [673] : usr/share/vim/vim91/ftplugin/passwd.vim 
│                │                       ├ [674] : usr/share/vim/vim91/ftplugin/pbtxt.vim 
│                │                       ├ [675] : usr/share/vim/vim91/ftplugin/pdf.vim 
│                │                       ├ [676] : usr/share/vim/vim91/ftplugin/perl.vim 
│                │                       ├ [677] : usr/share/vim/vim91/ftplugin/php.vim 
│                │                       ├ [678] : usr/share/vim/vim91/ftplugin/pinfo.vim 
│                │                       ├ [679] : usr/share/vim/vim91/ftplugin/pkl.vim 
│                │                       ├ [680] : usr/share/vim/vim91/ftplugin/plaintex.vim 
│                │                       ├ [681] : usr/share/vim/vim91/ftplugin/plsql.vim 
│                │                       ├ [682] : usr/share/vim/vim91/ftplugin/pod.vim 
│                │                       ├ [683] : usr/share/vim/vim91/ftplugin/poefilter.vim 
│                │                       ├ [684] : usr/share/vim/vim91/ftplugin/poke.vim 
│                │                       ├ [685] : usr/share/vim/vim91/ftplugin/postscr.vim 
│                │                       ├ [686] : usr/share/vim/vim91/ftplugin/pq.vim 
│                │                       ├ [687] : usr/share/vim/vim91/ftplugin/prisma.vim 
│                │                       ├ [688] : usr/share/vim/vim91/ftplugin/procmail.vim 
│                │                       ├ [689] : usr/share/vim/vim91/ftplugin/prolog.vim 
│                │                       ├ [690] : usr/share/vim/vim91/ftplugin/proto.vim 
│                │                       ├ [691] : usr/share/vim/vim91/ftplugin/protocols.vim 
│                │                       ├ [692] : usr/share/vim/vim91/ftplugin/ps1.vim 
│                │                       ├ [693] : usr/share/vim/vim91/ftplugin/ps1xml.vim 
│                │                       ├ [694] : usr/share/vim/vim91/ftplugin/ptx.vim 
│                │                       ├ [695] : usr/share/vim/vim91/ftplugin/purescript.vim 
│                │                       ├ [696] : usr/share/vim/vim91/ftplugin/pymanifest.vim 
│                │                       ├ [697] : usr/share/vim/vim91/ftplugin/pyrex.vim 
│                │                       ├ [698] : usr/share/vim/vim91/ftplugin/python.vim 
│                │                       ├ [699] : usr/share/vim/vim91/ftplugin/qb64.vim 
│                │                       ├ [700] : usr/share/vim/vim91/ftplugin/qf.vim 
│                │                       ├ [701] : usr/share/vim/vim91/ftplugin/qml.vim 
│                │                       ├ [702] : usr/share/vim/vim91/ftplugin/quake.vim 
│                │                       ├ [703] : usr/share/vim/vim91/ftplugin/quarto.vim 
│                │                       ├ [704] : usr/share/vim/vim91/ftplugin/r.vim 
│                │                       ├ [705] : usr/share/vim/vim91/ftplugin/racc.vim 
│                │                       ├ [706] : usr/share/vim/vim91/ftplugin/racket.vim 
│                │                       ├ [707] : usr/share/vim/vim91/ftplugin/raku.vim 
│                │                       ├ [708] : usr/share/vim/vim91/ftplugin/rasi.vim 
│                │                       ├ [709] : usr/share/vim/vim91/ftplugin/readline.vim 
│                │                       ├ [710] : usr/share/vim/vim91/ftplugin/registry.vim 
│                │                       ├ [711] : usr/share/vim/vim91/ftplugin/remind.vim 
│                │                       ├ [712] : usr/share/vim/vim91/ftplugin/requirements.vim 
│                │                       ├ [713] : usr/share/vim/vim91/ftplugin/rescript.vim 
│                │                       ├ [714] : usr/share/vim/vim91/ftplugin/reva.vim 
│                │                       ├ [715] : usr/share/vim/vim91/ftplugin/rhelp.vim 
│                │                       ├ [716] : usr/share/vim/vim91/ftplugin/rmd.vim 
│                │                       ├ [717] : usr/share/vim/vim91/ftplugin/rnc.vim 
│                │                       ├ [718] : usr/share/vim/vim91/ftplugin/rnoweb.vim 
│                │                       ├ [719] : usr/share/vim/vim91/ftplugin/roc.vim 
│                │                       ├ [720] : usr/share/vim/vim91/ftplugin/routeros.vim 
│                │                       ├ [721] : usr/share/vim/vim91/ftplugin/rpl.vim 
│                │                       ├ [722] : usr/share/vim/vim91/ftplugin/rrst.vim 
│                │                       ├ [723] : usr/share/vim/vim91/ftplugin/rst.vim 
│                │                       ├ [724] : usr/share/vim/vim91/ftplugin/ruby.vim 
│                │                       ├ [725] : usr/share/vim/vim91/ftplugin/rust.vim 
│                │                       ├ [726] : usr/share/vim/vim91/ftplugin/samba.vim 
│                │                       ├ [727] : usr/share/vim/vim91/ftplugin/sass.vim 
│                │                       ├ [728] : usr/share/vim/vim91/ftplugin/sbt.vim 
│                │                       ├ [729] : usr/share/vim/vim91/ftplugin/scala.vim 
│                │                       ├ [730] : usr/share/vim/vim91/ftplugin/scdoc.vim 
│                │                       ├ [731] : usr/share/vim/vim91/ftplugin/scheme.vim 
│                │                       ├ [732] : usr/share/vim/vim91/ftplugin/screen.vim 
│                │                       ├ [733] : usr/share/vim/vim91/ftplugin/scss.vim 
│                │                       ├ [734] : usr/share/vim/vim91/ftplugin/sed.vim 
│                │                       ├ [735] : usr/share/vim/vim91/ftplugin/sensors.vim 
│                │                       ├ [736] : usr/share/vim/vim91/ftplugin/services.vim 
│                │                       ├ [737] : usr/share/vim/vim91/ftplugin/setserial.vim 
│                │                       ├ [738] : usr/share/vim/vim91/ftplugin/sexplib.vim 
│                │                       ├ [739] : usr/share/vim/vim91/ftplugin/sgml.vim 
│                │                       ├ [740] : usr/share/vim/vim91/ftplugin/sh.vim 
│                │                       ├ [741] : usr/share/vim/vim91/ftplugin/shaderslang.vim 
│                │                       ├ [742] : usr/share/vim/vim91/ftplugin/sieve.vim 
│                │                       ├ [743] : usr/share/vim/vim91/ftplugin/slint.vim 
│                │                       ├ [744] : usr/share/vim/vim91/ftplugin/slpconf.vim 
│                │                       ├ [745] : usr/share/vim/vim91/ftplugin/slpreg.vim 
│                │                       ├ [746] : usr/share/vim/vim91/ftplugin/slpspi.vim 
│                │                       ├ [747] : usr/share/vim/vim91/ftplugin/sml.vim 
│                │                       ├ [748] : usr/share/vim/vim91/ftplugin/snakemake.vim 
│                │                       ├ [749] : usr/share/vim/vim91/ftplugin/solidity.vim 
│                │                       ├ [750] : usr/share/vim/vim91/ftplugin/solution.vim 
│                │                       ├ [751] : usr/share/vim/vim91/ftplugin/soy.vim 
│                │                       ├ [752] : usr/share/vim/vim91/ftplugin/spajson.vim 
│                │                       ├ [753] : usr/share/vim/vim91/ftplugin/spec.vim 
│                │                       ├ [754] : usr/share/vim/vim91/ftplugin/sql.vim 
│                │                       ├ [755] : usr/share/vim/vim91/ftplugin/squirrel.vim 
│                │                       ├ [756] : usr/share/vim/vim91/ftplugin/ssa.vim 
│                │                       ├ [757] : usr/share/vim/vim91/ftplugin/sshconfig.vim 
│                │                       ├ [758] : usr/share/vim/vim91/ftplugin/sshdconfig.vim 
│                │                       ├ [759] : usr/share/vim/vim91/ftplugin/stylus.vim 
│                │                       ├ [760] : usr/share/vim/vim91/ftplugin/sudoers.vim 
│                │                       ├ [761] : usr/share/vim/vim91/ftplugin/svelte.vim 
│                │                       ├ [762] : usr/share/vim/vim91/ftplugin/svg.vim 
│                │                       ├ [763] : usr/share/vim/vim91/ftplugin/sway.vim 
│                │                       ├ [764] : usr/share/vim/vim91/ftplugin/swayconfig.vim 
│                │                       ├ [765] : usr/share/vim/vim91/ftplugin/swift.vim 
│                │                       ├ [766] : usr/share/vim/vim91/ftplugin/swiftgyb.vim 
│                │                       ├ [767] : usr/share/vim/vim91/ftplugin/swig.vim 
│                │                       ├ [768] : usr/share/vim/vim91/ftplugin/sysctl.vim 
│                │                       ├ [769] : usr/share/vim/vim91/ftplugin/sysml.vim 
│                │                       ├ [770] : usr/share/vim/vim91/ftplugin/systemd.vim 
│                │                       ├ [771] : usr/share/vim/vim91/ftplugin/systemverilog.vim 
│                │                       ├ [772] : usr/share/vim/vim91/ftplugin/tap.vim 
│                │                       ├ [773] : usr/share/vim/vim91/ftplugin/tcl.vim 
│                │                       ├ [774] : usr/share/vim/vim91/ftplugin/tcsh.vim 
│                │                       ├ [775] : usr/share/vim/vim91/ftplugin/tera.vim 
│                │                       ├ [776] : usr/share/vim/vim91/ftplugin/terminfo.vim 
│                │                       ├ [777] : usr/share/vim/vim91/ftplugin/terraform.vim 
│                │                       ├ [778] : usr/share/vim/vim91/ftplugin/tex.vim 
│                │                       ├ [779] : usr/share/vim/vim91/ftplugin/text.vim 
│                │                       ├ [780] : usr/share/vim/vim91/ftplugin/tf.vim 
│                │                       ├ [781] : usr/share/vim/vim91/ftplugin/thrift.vim 
│                │                       ├ [782] : usr/share/vim/vim91/ftplugin/tiasm.vim 
│                │                       ├ [783] : usr/share/vim/vim91/ftplugin/tidy.vim 
│                │                       ├ [784] : usr/share/vim/vim91/ftplugin/tmux.vim 
│                │                       ├ [785] : usr/share/vim/vim91/ftplugin/toml.vim 
│                │                       ├ [786] : usr/share/vim/vim91/ftplugin/treetop.vim 
│                │                       ├ [787] : usr/share/vim/vim91/ftplugin/tt2html.vim 
│                │                       ├ [788] : usr/share/vim/vim91/ftplugin/tutor.vim 
│                │                       ├ [789] : usr/share/vim/vim91/ftplugin/twig.vim 
│                │                       ├ [790] : usr/share/vim/vim91/ftplugin/typescript.vim 
│                │                       ├ [791] : usr/share/vim/vim91/ftplugin/typescriptreact.vim 
│                │                       ├ [792] : usr/share/vim/vim91/ftplugin/typst.vim 
│                │                       ├ [793] : usr/share/vim/vim91/ftplugin/uc.vim 
│                │                       ├ [794] : usr/share/vim/vim91/ftplugin/uci.vim 
│                │                       ├ [795] : usr/share/vim/vim91/ftplugin/udevconf.vim 
│                │                       ├ [796] : usr/share/vim/vim91/ftplugin/udevperm.vim 
│                │                       ├ [797] : usr/share/vim/vim91/ftplugin/udevrules.vim 
│                │                       ├ [798] : usr/share/vim/vim91/ftplugin/unison.vim 
│                │                       ├ [799] : usr/share/vim/vim91/ftplugin/updatedb.vim 
│                │                       ├ [800] : usr/share/vim/vim91/ftplugin/urlshortcut.vim 
│                │                       ├ [801] : usr/share/vim/vim91/ftplugin/usd.vim 
│                │                       ├ [802] : usr/share/vim/vim91/ftplugin/v.vim 
│                │                       ├ [803] : usr/share/vim/vim91/ftplugin/vb.vim 
│                │                       ├ [804] : usr/share/vim/vim91/ftplugin/vdf.vim 
│                │                       ├ [805] : usr/share/vim/vim91/ftplugin/verilog.vim 
│                │                       ├ [806] : usr/share/vim/vim91/ftplugin/vhdl.vim 
│                │                       ├ [807] : usr/share/vim/vim91/ftplugin/vim.vim 
│                │                       ├ [808] : usr/share/vim/vim91/ftplugin/vroom.vim 
│                │                       ├ [809] : usr/share/vim/vim91/ftplugin/vue.vim 
│                │                       ├ [810] : usr/share/vim/vim91/ftplugin/wat.vim 
│                │                       ├ [811] : usr/share/vim/vim91/ftplugin/wget.vim 
│                │                       ├ [812] : usr/share/vim/vim91/ftplugin/wget2.vim 
│                │                       ├ [813] : usr/share/vim/vim91/ftplugin/xcompose.vim 
│                │                       ├ [814] : usr/share/vim/vim91/ftplugin/xdefaults.vim 
│                │                       ├ [815] : usr/share/vim/vim91/ftplugin/xf86conf.vim 
│                │                       ├ [816] : usr/share/vim/vim91/ftplugin/xhtml.vim 
│                │                       ├ [817] : usr/share/vim/vim91/ftplugin/xinetd.vim 
│                │                       ├ [818] : usr/share/vim/vim91/ftplugin/xml.vim 
│                │                       ├ [819] : usr/share/vim/vim91/ftplugin/xmodmap.vim 
│                │                       ├ [820] : usr/share/vim/vim91/ftplugin/xs.vim 
│                │                       ├ [821] : usr/share/vim/vim91/ftplugin/xsd.vim 
│                │                       ├ [822] : usr/share/vim/vim91/ftplugin/xslt.vim 
│                │                       ├ [823] : usr/share/vim/vim91/ftplugin/yacc.vim 
│                │                       ├ [824] : usr/share/vim/vim91/ftplugin/yaml.vim 
│                │                       ├ [825] : usr/share/vim/vim91/ftplugin/zathurarc.vim 
│                │                       ├ [826] : usr/share/vim/vim91/ftplugin/zig.vim 
│                │                       ├ [827] : usr/share/vim/vim91/ftplugin/zimbu.vim 
│                │                       ├ [828] : usr/share/vim/vim91/ftplugin/zsh.vim 
│                │                       ├ [829] : usr/share/vim/vim91/import/dist/vimhelp.vim 
│                │                       ├ [830] : usr/share/vim/vim91/import/dist/vimhighlight.vim 
│                │                       ├ [831] : usr/share/vim/vim91/indent/README.txt 
│                │                       ├ [832] : usr/share/vim/vim91/indent/aap.vim 
│                │                       ├ [833] : usr/share/vim/vim91/indent/ada.vim 
│                │                       ├ [834] : usr/share/vim/vim91/indent/ant.vim 
│                │                       ├ [835] : usr/share/vim/vim91/indent/arduino.vim 
│                │                       ├ [836] : usr/share/vim/vim91/indent/astro.vim 
│                │                       ├ [837] : usr/share/vim/vim91/indent/automake.vim 
│                │                       ├ [838] : usr/share/vim/vim91/indent/awk.vim 
│                │                       ├ [839] : usr/share/vim/vim91/indent/bash.vim 
│                │                       ├ [840] : usr/share/vim/vim91/indent/basic.vim 
│                │                       ├ [841] : usr/share/vim/vim91/indent/bib.vim 
│                │                       ├ [842] : usr/share/vim/vim91/indent/bitbake.vim 
│                │                       ├ [843] : usr/share/vim/vim91/indent/bst.vim 
│                │                       ├ [844] : usr/share/vim/vim91/indent/bzl.vim 
│                │                       ├ [845] : usr/share/vim/vim91/indent/c.vim 
│                │                       ├ [846] : usr/share/vim/vim91/indent/cdl.vim 
│                │                       ├ [847] : usr/share/vim/vim91/indent/ch.vim 
│                │                       ├ [848] : usr/share/vim/vim91/indent/chaiscript.vim 
│                │                       ├ [849] : usr/share/vim/vim91/indent/changelog.vim 
│                │                       ├ [850] : usr/share/vim/vim91/indent/chatito.vim 
│                │                       ├ [851] : usr/share/vim/vim91/indent/clojure.vim 
│                │                       ├ [852] : usr/share/vim/vim91/indent/cmake.vim 
│                │                       ├ [853] : usr/share/vim/vim91/indent/cobol.vim 
│                │                       ├ [854] : usr/share/vim/vim91/indent/config.vim 
│                │                       ├ [855] : usr/share/vim/vim91/indent/context.vim 
│                │                       ├ [856] : usr/share/vim/vim91/indent/cpp.vim 
│                │                       ├ [857] : usr/share/vim/vim91/indent/cs.vim 
│                │                       ├ [858] : usr/share/vim/vim91/indent/css.vim 
│                │                       ├ [859] : usr/share/vim/vim91/indent/cucumber.vim 
│                │                       ├ [860] : usr/share/vim/vim91/indent/cuda.vim 
│                │                       ├ [861] : usr/share/vim/vim91/indent/d.vim 
│                │                       ├ [862] : usr/share/vim/vim91/indent/dictconf.vim 
│                │                       ├ [863] : usr/share/vim/vim91/indent/dictdconf.vim 
│                │                       ├ [864] : usr/share/vim/vim91/indent/docbk.vim 
│                │                       ├ [865] : usr/share/vim/vim91/indent/dosbatch.vim 
│                │                       ├ [866] : usr/share/vim/vim91/indent/dtd.vim 
│                │                       ├ [867] : usr/share/vim/vim91/indent/dtrace.vim 
│                │                       ├ [868] : usr/share/vim/vim91/indent/dts.vim 
│                │                       ├ [869] : usr/share/vim/vim91/indent/dune.vim 
│                │                       ├ [870] : usr/share/vim/vim91/indent/dylan.vim 
│                │                       ├ [871] : usr/share/vim/vim91/indent/eiffel.vim 
│                │                       ├ [872] : usr/share/vim/vim91/indent/elm.vim 
│                │                       ├ [873] : usr/share/vim/vim91/indent/erlang.vim 
│                │                       ├ [874] : usr/share/vim/vim91/indent/eruby.vim 
│                │                       ├ [875] : usr/share/vim/vim91/indent/eterm.vim 
│                │                       ├ [876] : usr/share/vim/vim91/indent/expect.vim 
│                │                       ├ [877] : usr/share/vim/vim91/indent/falcon.vim 
│                │                       ├ [878] : usr/share/vim/vim91/indent/fennel.vim 
│                │                       ├ [879] : usr/share/vim/vim91/indent/fish.vim 
│                │                       ├ [880] : usr/share/vim/vim91/indent/fortran.vim 
│                │                       ├ [881] : usr/share/vim/vim91/indent/framescript.vim 
│                │                       ├ [882] : usr/share/vim/vim91/indent/freebasic.vim 
│                │                       ├ [883] : usr/share/vim/vim91/indent/gdscript.vim 
│                │                       ├ [884] : usr/share/vim/vim91/indent/gitconfig.vim 
│                │                       ├ [885] : usr/share/vim/vim91/indent/gitolite.vim 
│                │                       ├ [886] : usr/share/vim/vim91/indent/glsl.vim 
│                │                       ├ [887] : usr/share/vim/vim91/indent/go.vim 
│                │                       ├ [888] : usr/share/vim/vim91/indent/graphql.vim 
│                │                       ├ [889] : usr/share/vim/vim91/indent/gyp.vim 
│                │                       ├ [890] : usr/share/vim/vim91/indent/haml.vim 
│                │                       ├ [891] : usr/share/vim/vim91/indent/hamster.vim 
│                │                       ├ [892] : usr/share/vim/vim91/indent/hare.vim 
│                │                       ├ [893] : usr/share/vim/vim91/indent/hcl.vim 
│                │                       ├ [894] : usr/share/vim/vim91/indent/hog.vim 
│                │                       ├ [895] : usr/share/vim/vim91/indent/html.vim 
│                │                       ├ [896] : usr/share/vim/vim91/indent/htmldjango.vim 
│                │                       ├ [897] : usr/share/vim/vim91/indent/idlang.vim 
│                │                       ├ [898] : usr/share/vim/vim91/indent/idris2.vim 
│                │                       ├ [899] : usr/share/vim/vim91/indent/ishd.vim 
│                │                       ├ [900] : usr/share/vim/vim91/indent/j.vim 
│                │                       ├ [901] : usr/share/vim/vim91/indent/java.vim 
│                │                       ├ [902] : usr/share/vim/vim91/indent/javascript.vim 
│                │                       ├ [903] : usr/share/vim/vim91/indent/javascriptreact.vim 
│                │                       ├ [904] : usr/share/vim/vim91/indent/json.vim 
│                │                       ├ [905] : usr/share/vim/vim91/indent/json5.vim 
│                │                       ├ [906] : usr/share/vim/vim91/indent/jsonc.vim 
│                │                       ├ [907] : usr/share/vim/vim91/indent/jsp.vim 
│                │                       ├ [908] : usr/share/vim/vim91/indent/julia.vim 
│                │                       ├ [909] : usr/share/vim/vim91/indent/just.vim 
│                │                       ├ [910] : usr/share/vim/vim91/indent/kdl.vim 
│                │                       ├ [911] : usr/share/vim/vim91/indent/kotlin.vim 
│                │                       ├ [912] : usr/share/vim/vim91/indent/krl.vim 
│                │                       ├ [913] : usr/share/vim/vim91/indent/ld.vim 
│                │                       ├ [914] : usr/share/vim/vim91/indent/less.vim 
│                │                       ├ [915] : usr/share/vim/vim91/indent/lf.vim 
│                │                       ├ [916] : usr/share/vim/vim91/indent/lifelines.vim 
│                │                       ├ [917] : usr/share/vim/vim91/indent/liquid.vim 
│                │                       ├ [918] : usr/share/vim/vim91/indent/lisp.vim 
│                │                       ├ [919] : usr/share/vim/vim91/indent/livebook.vim 
│                │                       ├ [920] : usr/share/vim/vim91/indent/logtalk.vim 
│                │                       ├ [921] : usr/share/vim/vim91/indent/lua.vim 
│                │                       ├ [922] : usr/share/vim/vim91/indent/luau.vim 
│                │                       ├ [923] : usr/share/vim/vim91/indent/m17ndb.vim 
│                │                       ├ [924] : usr/share/vim/vim91/indent/mail.vim 
│                │                       ├ [925] : usr/share/vim/vim91/indent/make.vim 
│                │                       ├ [926] : usr/share/vim/vim91/indent/matlab.vim 
│                │                       ├ [927] : usr/share/vim/vim91/indent/meson.vim 
│                │                       ├ [928] : usr/share/vim/vim91/indent/mf.vim 
│                │                       ├ [929] : usr/share/vim/vim91/indent/mma.vim 
│                │                       ├ [930] : usr/share/vim/vim91/indent/mojo.vim 
│                │                       ├ [931] : usr/share/vim/vim91/indent/mp.vim 
│                │                       ├ [932] : usr/share/vim/vim91/indent/nginx.vim 
│                │                       ├ [933] : usr/share/vim/vim91/indent/nsis.vim 
│                │                       ├ [934] : usr/share/vim/vim91/indent/nu.vim 
│                │                       ├ [935] : usr/share/vim/vim91/indent/objc.vim 
│                │                       ├ [936] : usr/share/vim/vim91/indent/obse.vim 
│                │                       ├ [937] : usr/share/vim/vim91/indent/ocaml.vim 
│                │                       ├ [938] : usr/share/vim/vim91/indent/occam.vim 
│                │                       ├ [939] : usr/share/vim/vim91/indent/odin.vim 
│                │                       ├ [940] : usr/share/vim/vim91/indent/pascal.vim 
│                │                       ├ [941] : usr/share/vim/vim91/indent/perl.vim 
│                │                       ├ [942] : usr/share/vim/vim91/indent/php.vim 
│                │                       ├ [943] : usr/share/vim/vim91/indent/postscr.vim 
│                │                       ├ [944] : usr/share/vim/vim91/indent/pov.vim 
│                │                       ├ [945] : usr/share/vim/vim91/indent/prolog.vim 
│                │                       ├ [946] : usr/share/vim/vim91/indent/proto.vim 
│                │                       ├ [947] : usr/share/vim/vim91/indent/ps1.vim 
│                │                       ├ [948] : usr/share/vim/vim91/indent/pyrex.vim 
│                │                       ├ [949] : usr/share/vim/vim91/indent/python.vim 
│                │                       ├ [950] : usr/share/vim/vim91/indent/qb64.vim 
│                │                       ├ [951] : usr/share/vim/vim91/indent/qml.vim 
│                │                       ├ [952] : usr/share/vim/vim91/indent/quarto.vim 
│                │                       ├ [953] : usr/share/vim/vim91/indent/r.vim 
│                │                       ├ [954] : usr/share/vim/vim91/indent/racket.vim 
│                │                       ├ [955] : usr/share/vim/vim91/indent/raku.vim 
│                │                       ├ [956] : usr/share/vim/vim91/indent/raml.vim 
│                │                       ├ [957] : usr/share/vim/vim91/indent/rapid.vim 
│                │                       ├ [958] : usr/share/vim/vim91/indent/readline.vim 
│                │                       ├ [959] : usr/share/vim/vim91/indent/rhelp.vim 
│                │                       ├ [960] : usr/share/vim/vim91/indent/rmd.vim 
│                │                       ├ [961] : usr/share/vim/vim91/indent/rnoweb.vim 
│                │                       ├ [962] : usr/share/vim/vim91/indent/rpl.vim 
│                │                       ├ [963] : usr/share/vim/vim91/indent/rrst.vim 
│                │                       ├ [964] : usr/share/vim/vim91/indent/rst.vim 
│                │                       ├ [965] : usr/share/vim/vim91/indent/ruby.vim 
│                │                       ├ [966] : usr/share/vim/vim91/indent/rust.vim 
│                │                       ├ [967] : usr/share/vim/vim91/indent/sas.vim 
│                │                       ├ [968] : usr/share/vim/vim91/indent/sass.vim 
│                │                       ├ [969] : usr/share/vim/vim91/indent/scala.vim 
│                │                       ├ [970] : usr/share/vim/vim91/indent/scheme.vim 
│                │                       ├ [971] : usr/share/vim/vim91/indent/scss.vim 
│                │                       ├ [972] : usr/share/vim/vim91/indent/sdl.vim 
│                │                       ├ [973] : usr/share/vim/vim91/indent/sh.vim 
│                │                       ├ [974] : usr/share/vim/vim91/indent/sml.vim 
│                │                       ├ [975] : usr/share/vim/vim91/indent/solidity.vim 
│                │                       ├ [976] : usr/share/vim/vim91/indent/spajson.vim 
│                │                       ├ [977] : usr/share/vim/vim91/indent/sql.vim 
│                │                       ├ [978] : usr/share/vim/vim91/indent/sqlanywhere.vim 
│                │                       ├ [979] : usr/share/vim/vim91/indent/sshconfig.vim 
│                │                       ├ [980] : usr/share/vim/vim91/indent/stylus.vim 
│                │                       ├ [981] : usr/share/vim/vim91/indent/systemverilog.vim 
│                │                       ├ [982] : usr/share/vim/vim91/indent/tcl.vim 
│                │                       ├ [983] : usr/share/vim/vim91/indent/tcsh.vim 
│                │                       ├ [984] : usr/share/vim/vim91/indent/teraterm.vim 
│                │                       ├ [985] : usr/share/vim/vim91/indent/terraform.vim 
│                │                       ├ [986] : usr/share/vim/vim91/indent/tex.vim 
│                │                       ├ [987] : usr/share/vim/vim91/indent/tf.vim 
│                │                       ├ [988] : usr/share/vim/vim91/indent/thrift.vim 
│                │                       ├ [989] : usr/share/vim/vim91/indent/tilde.vim 
│                │                       ├ [990] : usr/share/vim/vim91/indent/treetop.vim 
│                │                       ├ [991] : usr/share/vim/vim91/indent/typescript.vim 
│                │                       ├ [992] : usr/share/vim/vim91/indent/typescriptreact.vim 
│                │                       ├ [993] : usr/share/vim/vim91/indent/typst.vim 
│                │                       ├ [994] : usr/share/vim/vim91/indent/vb.vim 
│                │                       ├ [995] : usr/share/vim/vim91/indent/verilog.vim 
│                │                       ├ [996] : usr/share/vim/vim91/indent/vhdl.vim 
│                │                       ├ [997] : usr/share/vim/vim91/indent/vim.vim 
│                │                       ├ [998] : usr/share/vim/vim91/indent/vroom.vim 
│                │                       ├ [999] : usr/share/vim/vim91/indent/vue.vim 
│                │                       ├ [1000]: usr/share/vim/vim91/indent/wat.vim 
│                │                       ├ [1001]: usr/share/vim/vim91/indent/xf86conf.vim 
│                │                       ├ [1002]: usr/share/vim/vim91/indent/xhtml.vim 
│                │                       ├ [1003]: usr/share/vim/vim91/indent/xinetd.vim 
│                │                       ├ [1004]: usr/share/vim/vim91/indent/xml.vim 
│                │                       ├ [1005]: usr/share/vim/vim91/indent/xsd.vim 
│                │                       ├ [1006]: usr/share/vim/vim91/indent/xslt.vim 
│                │                       ├ [1007]: usr/share/vim/vim91/indent/yacc.vim 
│                │                       ├ [1008]: usr/share/vim/vim91/indent/yaml.vim 
│                │                       ├ [1009]: usr/share/vim/vim91/indent/zig.vim 
│                │                       ├ [1010]: usr/share/vim/vim91/indent/zimbu.vim 
│                │                       ├ [1011]: usr/share/vim/vim91/indent/zsh.vim 
│                │                       ├ [1012]: usr/share/vim/vim91/macros/README.txt 
│                │                       ├ [1013]: usr/share/vim/vim91/macros/editexisting.vim 
│                │                       ├ [1014]: usr/share/vim/vim91/macros/justify.vim 
│                │                       ├ [1015]: usr/share/vim/vim91/macros/less.bat 
│                │                       ├ [1016]: usr/share/vim/vim91/macros/less.sh 
│                │                       ├ [1017]: usr/share/vim/vim91/macros/less.vim 
│                │                       ├ [1018]: usr/share/vim/vim91/macros/matchit.vim 
│                │                       ├ [1019]: usr/share/vim/vim91/macros/shellmenu.vim 
│                │                       ├ [1020]: usr/share/vim/vim91/macros/swapmous.vim 
│                │                       ├ [1021]: usr/share/vim/vim91/macros/hanoi/click.me 
│                │                       ├ [1022]: usr/share/vim/vim91/macros/hanoi/hanoi.vim 
│                │                       ├ [1023]: usr/share/vim/vim91/macros/hanoi/poster 
│                │                       ├ [1024]: usr/share/vim/vim91/macros/life/click.me 
│                │                       ├ [1025]: usr/share/vim/vim91/macros/life/life.vim 
│                │                       ├ [1026]: usr/share/vim/vim91/macros/maze/Makefile 
│                │                       ├ [1027]: usr/share/vim/vim91/macros/maze/README.txt 
│                │                       ├ [1028]: usr/share/vim/vim91/macros/maze/maze.c 
│                │                       ├ [1029]: usr/share/vim/vim91/macros/maze/maze_5.78 
│                │                       ├ [1030]: usr/share/vim/vim91/macros/maze/maze_mac 
│                │                       ├ [1031]: usr/share/vim/vim91/macros/maze/mazeansi.c 
│                │                       ├ [1032]: usr/share/vim/vim91/macros/maze/mazeclean.c 
│                │                       ├ [1033]: usr/share/vim/vim91/macros/maze/poster 
│                │                       ├ [1034]: usr/share/vim/vim91/macros/urm/README.txt 
│                │                       ├ [1035]: usr/share/vim/vim91/macros/urm/examples 
│                │                       ├ [1036]: usr/share/vim/vim91/macros/urm/urm 
│                │                       ├ [1037]: usr/share/vim/vim91/macros/urm/urm.vim 
│                │                       ├ [1038]: usr/share/vim/vim91/pack/dist/opt/cfilter/plugin/cfilter.vim 
│                │                       ├ [1039]: usr/share/vim/vim91/pack/dist/opt/comment/autoload/comment.vim 
│                │                       ├ [1040]: usr/share/vim/vim91/pack/dist/opt/comment/doc/comment.txt 
│                │                       ├ [1041]: usr/share/vim/vim91/pack/dist/opt/comment/doc/tags 
│                │                       ├ [1042]: usr/share/vim/vim91/pack/dist/opt/comment/plugin/comment.vim 
│                │                       ├ [1043]: usr/share/vim/vim91/pack/dist/opt/dvorak/dvorak/disable.vim 
│                │                       ├ [1044]: usr/share/vim/vim91/pack/dist/opt/dvorak/dvorak/enable.vim 
│                │                       ├ [1045]: usr/share/vim/vim91/pack/dist/opt/dvorak/plugin/dvorak.vim 
│                │                       ├ [1046]: usr/share/vim/vim91/pack/dist/opt/editexisting/plugin/editex
│                │                       │         isting.vim 
│                │                       ├ [1047]: usr/share/vim/vim91/pack/dist/opt/editorconfig/.editorconfig 
│                │                       ├ [1048]: usr/share/vim/vim91/pack/dist/opt/editorconfig/CONTRIBUTORS 
│                │                       ├ [1049]: usr/share/vim/vim91/pack/dist/opt/editorconfig/LICENSE 
│                │                       ├ [1050]: usr/share/vim/vim91/pack/dist/opt/editorconfig/LICENSE.PSF 
│                │                       ├ [1051]: usr/share/vim/vim91/pack/dist/opt/editorconfig/README.md 
│                │                       ├ [1052]: usr/share/vim/vim91/pack/dist/opt/editorconfig/autoload/edit
│                │                       │         orconfig.vim 
│                │                       ├ [1053]: usr/share/vim/vim91/pack/dist/opt/editorconfig/autoload/edit
│                │                       │         orconfig_core.vim 
│                │                       ├ [1054]: usr/share/vim/vim91/pack/dist/opt/editorconfig/autoload/edit
│                │                       │         orconfig_core/fnmatch.vim 
│                │                       ├ [1055]: usr/share/vim/vim91/pack/dist/opt/editorconfig/autoload/edit
│                │                       │         orconfig_core/handler.vim 
│                │                       ├ [1056]: usr/share/vim/vim91/pack/dist/opt/editorconfig/autoload/edit
│                │                       │         orconfig_core/ini.vim 
│                │                       ├ [1057]: usr/share/vim/vim91/pack/dist/opt/editorconfig/autoload/edit
│                │                       │         orconfig_core/util.vim 
│                │                       ├ [1058]: usr/share/vim/vim91/pack/dist/opt/editorconfig/doc/editorcon
│                │                       │         fig.txt 
│                │                       ├ [1059]: usr/share/vim/vim91/pack/dist/opt/editorconfig/doc/tags 
│                │                       ├ [1060]: usr/share/vim/vim91/pack/dist/opt/editorconfig/ftdetect/edit
│                │                       │         orconfig.vim 
│                │                       ├ [1061]: usr/share/vim/vim91/pack/dist/opt/editorconfig/plugin/editor
│                │                       │         config.vim 
│                │                       ├ [1062]: usr/share/vim/vim91/pack/dist/opt/helpcurwin/autoload/helpcu
│                │                       │         rwin.vim 
│                │                       ├ [1063]: usr/share/vim/vim91/pack/dist/opt/helpcurwin/doc/helpcurwin.
│                │                       │         txt 
│                │                       ├ [1064]: usr/share/vim/vim91/pack/dist/opt/helpcurwin/doc/tags 
│                │                       ├ [1065]: usr/share/vim/vim91/pack/dist/opt/helpcurwin/plugin/helpcurw
│                │                       │         in.vim 
│                │                       ├ [1066]: usr/share/vim/vim91/pack/dist/opt/helptoc/autoload/helptoc.vim 
│                │                       ├ [1067]: usr/share/vim/vim91/pack/dist/opt/helptoc/doc/helptoc.txt 
│                │                       ├ [1068]: usr/share/vim/vim91/pack/dist/opt/helptoc/doc/tags 
│                │                       ├ [1069]: usr/share/vim/vim91/pack/dist/opt/helptoc/plugin/helptoc.vim 
│                │                       ├ [1070]: usr/share/vim/vim91/pack/dist/opt/hlyank/plugin/hlyank.vim 
│                │                       ├ [1071]: usr/share/vim/vim91/pack/dist/opt/justify/plugin/justify.vim 
│                │                       ├ [1072]: usr/share/vim/vim91/pack/dist/opt/matchit/autoload/matchit.vim 
│                │                       ├ [1073]: usr/share/vim/vim91/pack/dist/opt/matchit/doc/matchit.txt 
│                │                       ├ [1074]: usr/share/vim/vim91/pack/dist/opt/matchit/doc/tags 
│                │                       ├ [1075]: usr/share/vim/vim91/pack/dist/opt/matchit/plugin/matchit.vim 
│                │                       ├ [1076]: usr/share/vim/vim91/pack/dist/opt/netrw/LICENSE.txt 
│                │                       ├ [1077]: usr/share/vim/vim91/pack/dist/opt/netrw/README.md 
│                │                       ├ [1078]: usr/share/vim/vim91/pack/dist/opt/netrw/autoload/netrw.vim 
│                │                       ├ [1079]: usr/share/vim/vim91/pack/dist/opt/netrw/autoload/netrw_gitig
│                │                       │         nore.vim 
│                │                       ├ [1080]: usr/share/vim/vim91/pack/dist/opt/netrw/autoload/netrw/fs.vim 
│                │                       ├ [1081]: usr/share/vim/vim91/pack/dist/opt/netrw/autoload/netrw/msg.vim 
│                │                       ├ [1082]: usr/share/vim/vim91/pack/dist/opt/netrw/autoload/netrw/os.vim 
│                │                       ├ [1083]: usr/share/vim/vim91/pack/dist/opt/netrw/doc/netrw.txt 
│                │                       ├ [1084]: usr/share/vim/vim91/pack/dist/opt/netrw/plugin/netrwPlugin.vim 
│                │                       ├ [1085]: usr/share/vim/vim91/pack/dist/opt/netrw/syntax/netrw.vim 
│                │                       ├ [1086]: usr/share/vim/vim91/pack/dist/opt/nohlsearch/plugin/nohlsear
│                │                       │         ch.vim 
│                │                       ├ [1087]: usr/share/vim/vim91/pack/dist/opt/shellmenu/plugin/shellmenu
│                │                       │         .vim 
│                │                       ├ [1088]: usr/share/vim/vim91/pack/dist/opt/swapmouse/plugin/swapmouse
│                │                       │         .vim 
│                │                       ├ [1089]: usr/share/vim/vim91/pack/dist/opt/termdebug/plugin/termdebug
│                │                       │         .vim 
│                │                       ├ [1090]: usr/share/vim/vim91/plugin/README.txt 
│                │                       ├ [1091]: usr/share/vim/vim91/plugin/getscriptPlugin.vim 
│                │                       ├ [1092]: usr/share/vim/vim91/plugin/gzip.vim 
│                │                       ├ [1093]: usr/share/vim/vim91/plugin/logiPat.vim 
│                │                       ├ [1094]: usr/share/vim/vim91/plugin/manpager.vim 
│                │                       ├ [1095]: usr/share/vim/vim91/plugin/matchparen.vim 
│                │                       ├ [1096]: usr/share/vim/vim91/plugin/netrwPlugin.vim 
│                │                       ├ [1097]: usr/share/vim/vim91/plugin/openPlugin.vim 
│                │                       ├ [1098]: usr/share/vim/vim91/plugin/rrhelper.vim 
│                │                       ├ [1099]: usr/share/vim/vim91/plugin/spellfile.vim 
│                │                       ├ [1100]: usr/share/vim/vim91/plugin/tarPlugin.vim 
│                │                       ├ [1101]: usr/share/vim/vim91/plugin/tohtml.vim 
│                │                       ├ [1102]: usr/share/vim/vim91/plugin/tutor.vim 
│                │                       ├ [1103]: usr/share/vim/vim91/plugin/vimballPlugin.vim 
│                │                       ├ [1104]: usr/share/vim/vim91/plugin/zipPlugin.vim 
│                │                       ├ [1105]: usr/share/vim/vim91/print/ascii.ps 
│                │                       ├ [1106]: usr/share/vim/vim91/print/cidfont.ps 
│                │                       ├ [1107]: usr/share/vim/vim91/print/cns_roman.ps 
│                │                       ├ [1108]: usr/share/vim/vim91/print/cp1250.ps 
│                │                       ├ [1109]: usr/share/vim/vim91/print/cp1251.ps 
│                │                       ├ [1110]: usr/share/vim/vim91/print/cp1252.ps 
│                │                       ├ [1111]: usr/share/vim/vim91/print/cp1253.ps 
│                │                       ├ [1112]: usr/share/vim/vim91/print/cp1254.ps 
│                │                       ├ [1113]: usr/share/vim/vim91/print/cp1255.ps 
│                │                       ├ [1114]: usr/share/vim/vim91/print/cp1257.ps 
│                │                       ├ [1115]: usr/share/vim/vim91/print/dec-mcs.ps 
│                │                       ├ [1116]: usr/share/vim/vim91/print/ebcdic-uk.ps 
│                │                       ├ [1117]: usr/share/vim/vim91/print/gb_roman.ps 
│                │                       ├ [1118]: usr/share/vim/vim91/print/hp-roman8.ps 
│                │                       ├ [1119]: usr/share/vim/vim91/print/iso-8859-10.ps 
│                │                       ├ [1120]: usr/share/vim/vim91/print/iso-8859-11.ps 
│                │                       ├ [1121]: usr/share/vim/vim91/print/iso-8859-13.ps 
│                │                       ├ [1122]: usr/share/vim/vim91/print/iso-8859-14.ps 
│                │                       ├ [1123]: usr/share/vim/vim91/print/iso-8859-15.ps 
│                │                       ├ [1124]: usr/share/vim/vim91/print/iso-8859-2.ps 
│                │                       ├ [1125]: usr/share/vim/vim91/print/iso-8859-3.ps 
│                │                       ├ [1126]: usr/share/vim/vim91/print/iso-8859-4.ps 
│                │                       ├ [1127]: usr/share/vim/vim91/print/iso-8859-5.ps 
│                │                       ├ [1128]: usr/share/vim/vim91/print/iso-8859-7.ps 
│                │                       ├ [1129]: usr/share/vim/vim91/print/iso-8859-8.ps 
│                │                       ├ [1130]: usr/share/vim/vim91/print/iso-8859-9.ps 
│                │                       ├ [1131]: usr/share/vim/vim91/print/jis_roman.ps 
│                │                       ├ [1132]: usr/share/vim/vim91/print/koi8-r.ps 
│                │                       ├ [1133]: usr/share/vim/vim91/print/koi8-u.ps 
│                │                       ├ [1134]: usr/share/vim/vim91/print/ks_roman.ps 
│                │                       ├ [1135]: usr/share/vim/vim91/print/latin1.ps 
│                │                       ├ [1136]: usr/share/vim/vim91/print/mac-roman.ps 
│                │                       ├ [1137]: usr/share/vim/vim91/print/prolog.ps 
│                │                       ├ [1138]: usr/share/vim/vim91/spell/check_locales.vim 
│                │                       ├ [1139]: usr/share/vim/vim91/spell/cleanadd.vim 
│                │                       ├ [1140]: usr/share/vim/vim91/spell/en.ascii.spl 
│                │                       ├ [1141]: usr/share/vim/vim91/spell/en.ascii.sug 
│                │                       ├ [1142]: usr/share/vim/vim91/spell/en.latin1.spl 
│                │                       ├ [1143]: usr/share/vim/vim91/spell/en.latin1.sug 
│                │                       ├ [1144]: usr/share/vim/vim91/spell/en.utf-8.spl 
│                │                       ├ [1145]: usr/share/vim/vim91/spell/en.utf-8.sug 
│                │                       ├ [1146]: usr/share/vim/vim91/spell/fixdup.vim 
│                │                       ├ [1147]: usr/share/vim/vim91/spell/he.vim 
│                │                       ├ [1148]: usr/share/vim/vim91/spell/spell.vim 
│                │                       ├ [1149]: usr/share/vim/vim91/spell/yi.vim 
│                │                       ├ [1150]: usr/share/vim/vim91/syntax/2html.vim 
│                │                       ├ [1151]: usr/share/vim/vim91/syntax/8th.vim 
│                │                       ├ [1152]: usr/share/vim/vim91/syntax/README.txt 
│                │                       ├ [1153]: usr/share/vim/vim91/syntax/a2ps.vim 
│                │                       ├ [1154]: usr/share/vim/vim91/syntax/a65.vim 
│                │                       ├ [1155]: usr/share/vim/vim91/syntax/aap.vim 
│                │                       ├ [1156]: usr/share/vim/vim91/syntax/abap.vim 
│                │                       ├ [1157]: usr/share/vim/vim91/syntax/abaqus.vim 
│                │                       ├ [1158]: usr/share/vim/vim91/syntax/abc.vim 
│                │                       ├ [1159]: usr/share/vim/vim91/syntax/abel.vim 
│                │                       ├ [1160]: usr/share/vim/vim91/syntax/abnf.vim 
│                │                       ├ [1161]: usr/share/vim/vim91/syntax/acedb.vim 
│                │                       ├ [1162]: usr/share/vim/vim91/syntax/ada.vim 
│                │                       ├ [1163]: usr/share/vim/vim91/syntax/aflex.vim 
│                │                       ├ [1164]: usr/share/vim/vim91/syntax/ahdl.vim 
│                │                       ├ [1165]: usr/share/vim/vim91/syntax/aidl.vim 
│                │                       ├ [1166]: usr/share/vim/vim91/syntax/alsaconf.vim 
│                │                       ├ [1167]: usr/share/vim/vim91/syntax/amiga.vim 
│                │                       ├ [1168]: usr/share/vim/vim91/syntax/aml.vim 
│                │                       ├ [1169]: usr/share/vim/vim91/syntax/ampl.vim 
│                │                       ├ [1170]: usr/share/vim/vim91/syntax/ant.vim 
│                │                       ├ [1171]: usr/share/vim/vim91/syntax/antlr.vim 
│                │                       ├ [1172]: usr/share/vim/vim91/syntax/antlr4.vim 
│                │                       ├ [1173]: usr/share/vim/vim91/syntax/apache.vim 
│                │                       ├ [1174]: usr/share/vim/vim91/syntax/apachestyle.vim 
│                │                       ├ [1175]: usr/share/vim/vim91/syntax/apkbuild.vim 
│                │                       ├ [1176]: usr/share/vim/vim91/syntax/aptconf.vim 
│                │                       ├ [1177]: usr/share/vim/vim91/syntax/arch.vim 
│                │                       ├ [1178]: usr/share/vim/vim91/syntax/arduino.vim 
│                │                       ├ [1179]: usr/share/vim/vim91/syntax/art.vim 
│                │                       ├ [1180]: usr/share/vim/vim91/syntax/asciidoc.vim 
│                │                       ├ [1181]: usr/share/vim/vim91/syntax/asm.vim 
│                │                       ├ [1182]: usr/share/vim/vim91/syntax/asm68k.vim 
│                │                       ├ [1183]: usr/share/vim/vim91/syntax/asmh8300.vim 
│                │                       ├ [1184]: usr/share/vim/vim91/syntax/asn.vim 
│                │                       ├ [1185]: usr/share/vim/vim91/syntax/aspperl.vim 
│                │                       ├ [1186]: usr/share/vim/vim91/syntax/aspvbs.vim 
│                │                       ├ [1187]: usr/share/vim/vim91/syntax/asterisk.vim 
│                │                       ├ [1188]: usr/share/vim/vim91/syntax/asteriskvm.vim 
│                │                       ├ [1189]: usr/share/vim/vim91/syntax/astro.vim 
│                │                       ├ [1190]: usr/share/vim/vim91/syntax/asy.vim 
│                │                       ├ [1191]: usr/share/vim/vim91/syntax/atlas.vim 
│                │                       ├ [1192]: usr/share/vim/vim91/syntax/autodoc.vim 
│                │                       ├ [1193]: usr/share/vim/vim91/syntax/autohotkey.vim 
│                │                       ├ [1194]: usr/share/vim/vim91/syntax/autoit.vim 
│                │                       ├ [1195]: usr/share/vim/vim91/syntax/automake.vim 
│                │                       ├ [1196]: usr/share/vim/vim91/syntax/autopkgtest.vim 
│                │                       ├ [1197]: usr/share/vim/vim91/syntax/ave.vim 
│                │                       ├ [1198]: usr/share/vim/vim91/syntax/avra.vim 
│                │                       ├ [1199]: usr/share/vim/vim91/syntax/awk.vim 
│                │                       ├ [1200]: usr/share/vim/vim91/syntax/ayacc.vim 
│                │                       ├ [1201]: usr/share/vim/vim91/syntax/b.vim 
│                │                       ├ [1202]: usr/share/vim/vim91/syntax/baan.vim 
│                │                       ├ [1203]: usr/share/vim/vim91/syntax/bash.vim 
│                │                       ├ [1204]: usr/share/vim/vim91/syntax/basic.vim 
│                │                       ├ [1205]: usr/share/vim/vim91/syntax/bc.vim 
│                │                       ├ [1206]: usr/share/vim/vim91/syntax/bdf.vim 
│                │                       ├ [1207]: usr/share/vim/vim91/syntax/bib.vim 
│                │                       ├ [1208]: usr/share/vim/vim91/syntax/bindzone.vim 
│                │                       ├ [1209]: usr/share/vim/vim91/syntax/bitbake.vim 
│                │                       ├ [1210]: usr/share/vim/vim91/syntax/blank.vim 
│                │                       ├ [1211]: usr/share/vim/vim91/syntax/bsdl.vim 
│                │                       ├ [1212]: usr/share/vim/vim91/syntax/bst.vim 
│                │                       ├ [1213]: usr/share/vim/vim91/syntax/btm.vim 
│                │                       ├ [1214]: usr/share/vim/vim91/syntax/bzl.vim 
│                │                       ├ [1215]: usr/share/vim/vim91/syntax/bzr.vim 
│                │                       ├ [1216]: usr/share/vim/vim91/syntax/c.vim 
│                │                       ├ [1217]: usr/share/vim/vim91/syntax/cabal.vim 
│                │                       ├ [1218]: usr/share/vim/vim91/syntax/cabalconfig.vim 
│                │                       ├ [1219]: usr/share/vim/vim91/syntax/cabalproject.vim 
│                │                       ├ [1220]: usr/share/vim/vim91/syntax/calendar.vim 
│                │                       ├ [1221]: usr/share/vim/vim91/syntax/cangjie.vim 
│                │                       ├ [1222]: usr/share/vim/vim91/syntax/catalog.vim 
│                │                       ├ [1223]: usr/share/vim/vim91/syntax/cdl.vim 
│                │                       ├ [1224]: usr/share/vim/vim91/syntax/cdrdaoconf.vim 
│                │                       ├ [1225]: usr/share/vim/vim91/syntax/cdrtoc.vim 
│                │                       ├ [1226]: usr/share/vim/vim91/syntax/cf.vim 
│                │                       ├ [1227]: usr/share/vim/vim91/syntax/cfg.vim 
│                │                       ├ [1228]: usr/share/vim/vim91/syntax/cgdbrc.vim 
│                │                       ├ [1229]: usr/share/vim/vim91/syntax/ch.vim 
│                │                       ├ [1230]: usr/share/vim/vim91/syntax/chaiscript.vim 
│                │                       ├ [1231]: usr/share/vim/vim91/syntax/change.vim 
│                │                       ├ [1232]: usr/share/vim/vim91/syntax/changelog.vim 
│                │                       ├ [1233]: usr/share/vim/vim91/syntax/chaskell.vim 
│                │                       ├ [1234]: usr/share/vim/vim91/syntax/chatito.vim 
│                │                       ├ [1235]: usr/share/vim/vim91/syntax/cheetah.vim 
│                │                       ├ [1236]: usr/share/vim/vim91/syntax/chicken.vim 
│                │                       ├ [1237]: usr/share/vim/vim91/syntax/chill.vim 
│                │                       ├ [1238]: usr/share/vim/vim91/syntax/chordpro.vim 
│                │                       ├ [1239]: usr/share/vim/vim91/syntax/chuck.vim 
│                │                       ├ [1240]: usr/share/vim/vim91/syntax/cl.vim 
│                │                       ├ [1241]: usr/share/vim/vim91/syntax/clean.vim 
│                │                       ├ [1242]: usr/share/vim/vim91/syntax/clipper.vim 
│                │                       ├ [1243]: usr/share/vim/vim91/syntax/clojure.vim 
│                │                       ├ [1244]: usr/share/vim/vim91/syntax/cmacro.vim 
│                │                       ├ [1245]: usr/share/vim/vim91/syntax/cmake.vim 
│                │                       ├ [1246]: usr/share/vim/vim91/syntax/cmakecache.vim 
│                │                       ├ [1247]: usr/share/vim/vim91/syntax/cmod.vim 
│                │                       ├ [1248]: usr/share/vim/vim91/syntax/cmusrc.vim 
│                │                       ├ [1249]: usr/share/vim/vim91/syntax/cobol.vim 
│                │                       ├ [1250]: usr/share/vim/vim91/syntax/coco.vim 
│                │                       ├ [1251]: usr/share/vim/vim91/syntax/codeowners.vim 
│                │                       ├ [1252]: usr/share/vim/vim91/syntax/colortest.vim 
│                │                       ├ [1253]: usr/share/vim/vim91/syntax/conaryrecipe.vim 
│                │                       ├ [1254]: usr/share/vim/vim91/syntax/conf.vim 
│                │                       ├ [1255]: usr/share/vim/vim91/syntax/config.vim 
│                │                       ├ [1256]: usr/share/vim/vim91/syntax/confini.vim 
│                │                       ├ [1257]: usr/share/vim/vim91/syntax/context.vim 
│                │                       ├ [1258]: usr/share/vim/vim91/syntax/cpp.vim 
│                │                       ├ [1259]: usr/share/vim/vim91/syntax/crm.vim 
│                │                       ├ [1260]: usr/share/vim/vim91/syntax/crontab.vim 
│                │                       ├ [1261]: usr/share/vim/vim91/syntax/cs.vim 
│                │                       ├ [1262]: usr/share/vim/vim91/syntax/csc.vim 
│                │                       ├ [1263]: usr/share/vim/vim91/syntax/csdl.vim 
│                │                       ├ [1264]: usr/share/vim/vim91/syntax/csh.vim 
│                │                       ├ [1265]: usr/share/vim/vim91/syntax/csp.vim 
│                │                       ├ [1266]: usr/share/vim/vim91/syntax/css.vim 
│                │                       ├ [1267]: usr/share/vim/vim91/syntax/csv.vim 
│                │                       ├ [1268]: usr/share/vim/vim91/syntax/cterm.vim 
│                │                       ├ [1269]: usr/share/vim/vim91/syntax/ctrlh.vim 
│                │                       ├ [1270]: usr/share/vim/vim91/syntax/cucumber.vim 
│                │                       ├ [1271]: usr/share/vim/vim91/syntax/cuda.vim 
│                │                       ├ [1272]: usr/share/vim/vim91/syntax/cupl.vim 
│                │                       ├ [1273]: usr/share/vim/vim91/syntax/cuplsim.vim 
│                │                       ├ [1274]: usr/share/vim/vim91/syntax/cvs.vim 
│                │                       ├ [1275]: usr/share/vim/vim91/syntax/cvsrc.vim 
│                │                       ├ [1276]: usr/share/vim/vim91/syntax/cweb.vim 
│                │                       ├ [1277]: usr/share/vim/vim91/syntax/cynlib.vim 
│                │                       ├ [1278]: usr/share/vim/vim91/syntax/cynpp.vim 
│                │                       ├ [1279]: usr/share/vim/vim91/syntax/d.vim 
│                │                       ├ [1280]: usr/share/vim/vim91/syntax/dart.vim 
│                │                       ├ [1281]: usr/share/vim/vim91/syntax/datascript.vim 
│                │                       ├ [1282]: usr/share/vim/vim91/syntax/dax.vim 
│                │                       ├ [1283]: usr/share/vim/vim91/syntax/dcd.vim 
│                │                       ├ [1284]: usr/share/vim/vim91/syntax/dcl.vim 
│                │                       ├ [1285]: usr/share/vim/vim91/syntax/deb822sources.vim 
│                │                       ├ [1286]: usr/share/vim/vim91/syntax/debchangelog.vim 
│                │                       ├ [1287]: usr/share/vim/vim91/syntax/debcontrol.vim 
│                │                       ├ [1288]: usr/share/vim/vim91/syntax/debcopyright.vim 
│                │                       ├ [1289]: usr/share/vim/vim91/syntax/debsources.vim 
│                │                       ├ [1290]: usr/share/vim/vim91/syntax/def.vim 
│                │                       ├ [1291]: usr/share/vim/vim91/syntax/denyhosts.vim 
│                │                       ├ [1292]: usr/share/vim/vim91/syntax/dep3patch.vim 
│                │                       ├ [1293]: usr/share/vim/vim91/syntax/desc.vim 
│                │                       ├ [1294]: usr/share/vim/vim91/syntax/desktop.vim 
│                │                       ├ [1295]: usr/share/vim/vim91/syntax/dictconf.vim 
│                │                       ├ [1296]: usr/share/vim/vim91/syntax/dictdconf.vim 
│                │                       ├ [1297]: usr/share/vim/vim91/syntax/diff.vim 
│                │                       ├ [1298]: usr/share/vim/vim91/syntax/dircolors.vim 
│                │                       ├ [1299]: usr/share/vim/vim91/syntax/dirpager.vim 
│                │                       ├ [1300]: usr/share/vim/vim91/syntax/diva.vim 
│                │                       ├ [1301]: usr/share/vim/vim91/syntax/django.vim 
│                │                       ├ [1302]: usr/share/vim/vim91/syntax/dns.vim 
│                │                       ├ [1303]: usr/share/vim/vim91/syntax/dnsmasq.vim 
│                │                       ├ [1304]: usr/share/vim/vim91/syntax/docbk.vim 
│                │                       ├ [1305]: usr/share/vim/vim91/syntax/docbksgml.vim 
│                │                       ├ [1306]: usr/share/vim/vim91/syntax/docbkxml.vim 
│                │                       ├ [1307]: usr/share/vim/vim91/syntax/dockerfile.vim 
│                │                       ├ [1308]: usr/share/vim/vim91/syntax/dosbatch.vim 
│                │                       ├ [1309]: usr/share/vim/vim91/syntax/dosini.vim 
│                │                       ├ [1310]: usr/share/vim/vim91/syntax/dot.vim 
│                │                       ├ [1311]: usr/share/vim/vim91/syntax/doxygen.vim 
│                │                       ├ [1312]: usr/share/vim/vim91/syntax/dracula.vim 
│                │                       ├ [1313]: usr/share/vim/vim91/syntax/dsl.vim 
│                │                       ├ [1314]: usr/share/vim/vim91/syntax/dtd.vim 
│                │                       ├ [1315]: usr/share/vim/vim91/syntax/dtml.vim 
│                │                       ├ [1316]: usr/share/vim/vim91/syntax/dtrace.vim 
│                │                       ├ [1317]: usr/share/vim/vim91/syntax/dts.vim 
│                │                       ├ [1318]: usr/share/vim/vim91/syntax/dune.vim 
│                │                       ├ [1319]: usr/share/vim/vim91/syntax/dylan.vim 
│                │                       ├ [1320]: usr/share/vim/vim91/syntax/dylanintr.vim 
│                │                       ├ [1321]: usr/share/vim/vim91/syntax/dylanlid.vim 
│                │                       ├ [1322]: usr/share/vim/vim91/syntax/ecd.vim 
│                │                       ├ [1323]: usr/share/vim/vim91/syntax/edif.vim 
│                │                       ├ [1324]: usr/share/vim/vim91/syntax/editorconfig.vim 
│                │                       ├ [1325]: usr/share/vim/vim91/syntax/eiffel.vim 
│                │                       ├ [1326]: usr/share/vim/vim91/syntax/elf.vim 
│                │                       ├ [1327]: usr/share/vim/vim91/syntax/elinks.vim 
│                │                       ├ [1328]: usr/share/vim/vim91/syntax/elm.vim 
│                │                       ├ [1329]: usr/share/vim/vim91/syntax/elmfilt.vim 
│                │                       ├ [1330]: usr/share/vim/vim91/syntax/erlang.vim 
│                │                       ├ [1331]: usr/share/vim/vim91/syntax/eruby.vim 
│                │                       ├ [1332]: usr/share/vim/vim91/syntax/esmtprc.vim 
│                │                       ├ [1333]: usr/share/vim/vim91/syntax/esqlc.vim 
│                │                       ├ [1334]: usr/share/vim/vim91/syntax/esterel.vim 
│                │                       ├ [1335]: usr/share/vim/vim91/syntax/eterm.vim 
│                │                       ├ [1336]: usr/share/vim/vim91/syntax/euphoria3.vim 
│                │                       ├ [1337]: usr/share/vim/vim91/syntax/euphoria4.vim 
│                │                       ├ [1338]: usr/share/vim/vim91/syntax/eviews.vim 
│                │                       ├ [1339]: usr/share/vim/vim91/syntax/exim.vim 
│                │                       ├ [1340]: usr/share/vim/vim91/syntax/expect.vim 
│                │                       ├ [1341]: usr/share/vim/vim91/syntax/exports.vim 
│                │                       ├ [1342]: usr/share/vim/vim91/syntax/falcon.vim 
│                │                       ├ [1343]: usr/share/vim/vim91/syntax/fan.vim 
│                │                       ├ [1344]: usr/share/vim/vim91/syntax/fasm.vim 
│                │                       ├ [1345]: usr/share/vim/vim91/syntax/fdcc.vim 
│                │                       ├ [1346]: usr/share/vim/vim91/syntax/fetchmail.vim 
│                │                       ├ [1347]: usr/share/vim/vim91/syntax/fgl.vim 
│                │                       ├ [1348]: usr/share/vim/vim91/syntax/fish.vim 
│                │                       ├ [1349]: usr/share/vim/vim91/syntax/flexwiki.vim 
│                │                       ├ [1350]: usr/share/vim/vim91/syntax/focexec.vim 
│                │                       ├ [1351]: usr/share/vim/vim91/syntax/form.vim 
│                │                       ├ [1352]: usr/share/vim/vim91/syntax/forth.vim 
│                │                       ├ [1353]: usr/share/vim/vim91/syntax/fortran.vim 
│                │                       ├ [1354]: usr/share/vim/vim91/syntax/foxpro.vim 
│                │                       ├ [1355]: usr/share/vim/vim91/syntax/fpcmake.vim 
│                │                       ├ [1356]: usr/share/vim/vim91/syntax/framescript.vim 
│                │                       ├ [1357]: usr/share/vim/vim91/syntax/freebasic.vim 
│                │                       ├ [1358]: usr/share/vim/vim91/syntax/fstab.vim 
│                │                       ├ [1359]: usr/share/vim/vim91/syntax/fvwm.vim 
│                │                       ├ [1360]: usr/share/vim/vim91/syntax/fvwm2m4.vim 
│                │                       ├ [1361]: usr/share/vim/vim91/syntax/gdb.vim 
│                │                       ├ [1362]: usr/share/vim/vim91/syntax/gdmo.vim 
│                │                       ├ [1363]: usr/share/vim/vim91/syntax/gdresource.vim 
│                │                       ├ [1364]: usr/share/vim/vim91/syntax/gdscript.vim 
│                │                       ├ [1365]: usr/share/vim/vim91/syntax/gdshader.vim 
│                │                       ├ [1366]: usr/share/vim/vim91/syntax/gedcom.vim 
│                │                       ├ [1367]: usr/share/vim/vim91/syntax/gel.vim 
│                │                       ├ [1368]: usr/share/vim/vim91/syntax/gemtext.vim 
│                │                       ├ [1369]: usr/share/vim/vim91/syntax/gift.vim 
│                │                       ├ [1370]: usr/share/vim/vim91/syntax/git.vim 
│                │                       ├ [1371]: usr/share/vim/vim91/syntax/gitattributes.vim 
│                │                       ├ [1372]: usr/share/vim/vim91/syntax/gitcommit.vim 
│                │                       ├ [1373]: usr/share/vim/vim91/syntax/gitconfig.vim 
│                │                       ├ [1374]: usr/share/vim/vim91/syntax/gitignore.vim 
│                │                       ├ [1375]: usr/share/vim/vim91/syntax/gitolite.vim 
│                │                       ├ [1376]: usr/share/vim/vim91/syntax/gitrebase.vim 
│                │                       ├ [1377]: usr/share/vim/vim91/syntax/gitsendemail.vim 
│                │                       ├ [1378]: usr/share/vim/vim91/syntax/gkrellmrc.vim 
│                │                       ├ [1379]: usr/share/vim/vim91/syntax/gleam.vim 
│                │                       ├ [1380]: usr/share/vim/vim91/syntax/glsl.vim 
│                │                       ├ [1381]: usr/share/vim/vim91/syntax/gnash.vim 
│                │                       ├ [1382]: usr/share/vim/vim91/syntax/gnuplot.vim 
│                │                       ├ [1383]: usr/share/vim/vim91/syntax/go.vim 
│                │                       ├ [1384]: usr/share/vim/vim91/syntax/goaccess.vim 
│                │                       ├ [1385]: usr/share/vim/vim91/syntax/godoc.vim 
│                │                       ├ [1386]: usr/share/vim/vim91/syntax/gp.vim 
│                │                       ├ [1387]: usr/share/vim/vim91/syntax/gpg.vim 
│                │                       ├ [1388]: usr/share/vim/vim91/syntax/gprof.vim 
│                │                       ├ [1389]: usr/share/vim/vim91/syntax/grads.vim 
│                │                       ├ [1390]: usr/share/vim/vim91/syntax/graphql.vim 
│                │                       ├ [1391]: usr/share/vim/vim91/syntax/gretl.vim 
│                │                       ├ [1392]: usr/share/vim/vim91/syntax/groff.vim 
│                │                       ├ [1393]: usr/share/vim/vim91/syntax/groovy.vim 
│                │                       ├ [1394]: usr/share/vim/vim91/syntax/group.vim 
│                │                       ├ [1395]: usr/share/vim/vim91/syntax/grub.vim 
│                │                       ├ [1396]: usr/share/vim/vim91/syntax/gsp.vim 
│                │                       ├ [1397]: usr/share/vim/vim91/syntax/gtkrc.vim 
│                │                       ├ [1398]: usr/share/vim/vim91/syntax/gvpr.vim 
│                │                       ├ [1399]: usr/share/vim/vim91/syntax/gyp.vim 
│                │                       ├ [1400]: usr/share/vim/vim91/syntax/haml.vim 
│                │                       ├ [1401]: usr/share/vim/vim91/syntax/hamster.vim 
│                │                       ├ [1402]: usr/share/vim/vim91/syntax/hare.vim 
│                │                       ├ [1403]: usr/share/vim/vim91/syntax/haredoc.vim 
│                │                       ├ [1404]: usr/share/vim/vim91/syntax/haskell.vim 
│                │                       ├ [1405]: usr/share/vim/vim91/syntax/haste.vim 
│                │                       ├ [1406]: usr/share/vim/vim91/syntax/hastepreproc.vim 
│                │                       ├ [1407]: usr/share/vim/vim91/syntax/hb.vim 
│                │                       ├ [1408]: usr/share/vim/vim91/syntax/hcl.vim 
│                │                       ├ [1409]: usr/share/vim/vim91/syntax/help.vim 
│                │                       ├ [1410]: usr/share/vim/vim91/syntax/help_it.vim 
│                │                       ├ [1411]: usr/share/vim/vim91/syntax/help_ru.vim 
│                │                       ├ [1412]: usr/share/vim/vim91/syntax/hercules.vim 
│                │                       ├ [1413]: usr/share/vim/vim91/syntax/hex.vim 
│                │                       ├ [1414]: usr/share/vim/vim91/syntax/hgcommit.vim 
│                │                       ├ [1415]: usr/share/vim/vim91/syntax/hitest.vim 
│                │                       ├ [1416]: usr/share/vim/vim91/syntax/hlsplaylist.vim 
│                │                       ├ [1417]: usr/share/vim/vim91/syntax/hog.vim 
│                │                       ├ [1418]: usr/share/vim/vim91/syntax/hollywood.vim 
│                │                       ├ [1419]: usr/share/vim/vim91/syntax/hostconf.vim 
│                │                       ├ [1420]: usr/share/vim/vim91/syntax/hostsaccess.vim 
│                │                       ├ [1421]: usr/share/vim/vim91/syntax/html.vim 
│                │                       ├ [1422]: usr/share/vim/vim91/syntax/htmlangular.vim 
│                │                       ├ [1423]: usr/share/vim/vim91/syntax/htmlcheetah.vim 
│                │                       ├ [1424]: usr/share/vim/vim91/syntax/htmldjango.vim 
│                │                       ├ [1425]: usr/share/vim/vim91/syntax/htmlm4.vim 
│                │                       ├ [1426]: usr/share/vim/vim91/syntax/htmlos.vim 
│                │                       ├ [1427]: usr/share/vim/vim91/syntax/hyprlang.vim 
│                │                       ├ [1428]: usr/share/vim/vim91/syntax/i3config.vim 
│                │                       ├ [1429]: usr/share/vim/vim91/syntax/ia64.vim 
│                │                       ├ [1430]: usr/share/vim/vim91/syntax/ibasic.vim 
│                │                       ├ [1431]: usr/share/vim/vim91/syntax/icemenu.vim 
│                │                       ├ [1432]: usr/share/vim/vim91/syntax/icon.vim 
│                │                       ├ [1433]: usr/share/vim/vim91/syntax/idl.vim 
│                │                       ├ [1434]: usr/share/vim/vim91/syntax/idlang.vim 
│                │                       ├ [1435]: usr/share/vim/vim91/syntax/idris2.vim 
│                │                       ├ [1436]: usr/share/vim/vim91/syntax/indent.vim 
│                │                       ├ [1437]: usr/share/vim/vim91/syntax/inform.vim 
│                │                       ├ [1438]: usr/share/vim/vim91/syntax/initex.vim 
│                │                       ├ [1439]: usr/share/vim/vim91/syntax/initng.vim 
│                │                       ├ [1440]: usr/share/vim/vim91/syntax/inittab.vim 
│                │                       ├ [1441]: usr/share/vim/vim91/syntax/ipfilter.vim 
│                │                       ├ [1442]: usr/share/vim/vim91/syntax/ipkg.vim 
│                │                       ├ [1443]: usr/share/vim/vim91/syntax/ishd.vim 
│                │                       ├ [1444]: usr/share/vim/vim91/syntax/iss.vim 
│                │                       ├ [1445]: usr/share/vim/vim91/syntax/ist.vim 
│                │                       ├ [1446]: usr/share/vim/vim91/syntax/j.vim 
│                │                       ├ [1447]: usr/share/vim/vim91/syntax/jal.vim 
│                │                       ├ [1448]: usr/share/vim/vim91/syntax/jam.vim 
│                │                       ├ [1449]: usr/share/vim/vim91/syntax/jargon.vim 
│                │                       ├ [1450]: usr/share/vim/vim91/syntax/java.vim 
│                │                       ├ [1451]: usr/share/vim/vim91/syntax/javacc.vim 
│                │                       ├ [1452]: usr/share/vim/vim91/syntax/javascript.vim 
│                │                       ├ [1453]: usr/share/vim/vim91/syntax/javascriptreact.vim 
│                │                       ├ [1454]: usr/share/vim/vim91/syntax/jess.vim 
│                │                       ├ [1455]: usr/share/vim/vim91/syntax/jgraph.vim 
│                │                       ├ [1456]: usr/share/vim/vim91/syntax/jinja.vim 
│                │                       ├ [1457]: usr/share/vim/vim91/syntax/jjdescription.vim 
│                │                       ├ [1458]: usr/share/vim/vim91/syntax/jovial.vim 
│                │                       ├ [1459]: usr/share/vim/vim91/syntax/jproperties.vim 
│                │                       ├ [1460]: usr/share/vim/vim91/syntax/jq.vim 
│                │                       ├ [1461]: usr/share/vim/vim91/syntax/json.vim 
│                │                       ├ [1462]: usr/share/vim/vim91/syntax/json5.vim 
│                │                       ├ [1463]: usr/share/vim/vim91/syntax/jsonc.vim 
│                │                       ├ [1464]: usr/share/vim/vim91/syntax/jsp.vim 
│                │                       ├ [1465]: usr/share/vim/vim91/syntax/julia.vim 
│                │                       ├ [1466]: usr/share/vim/vim91/syntax/just.vim 
│                │                       ├ [1467]: usr/share/vim/vim91/syntax/karel.vim 
│                │                       ├ [1468]: usr/share/vim/vim91/syntax/kconfig.vim 
│                │                       ├ [1469]: usr/share/vim/vim91/syntax/kdl.vim 
│                │                       ├ [1470]: usr/share/vim/vim91/syntax/kitty.vim 
│                │                       ├ [1471]: usr/share/vim/vim91/syntax/kivy.vim 
│                │                       ├ [1472]: usr/share/vim/vim91/syntax/kix.vim 
│                │                       ├ [1473]: usr/share/vim/vim91/syntax/kotlin.vim 
│                │                       ├ [1474]: usr/share/vim/vim91/syntax/krl.vim 
│                │                       ├ [1475]: usr/share/vim/vim91/syntax/kscript.vim 
│                │                       ├ [1476]: usr/share/vim/vim91/syntax/kwt.vim 
│                │                       ├ [1477]: usr/share/vim/vim91/syntax/lace.vim 
│                │                       ├ [1478]: usr/share/vim/vim91/syntax/latte.vim 
│                │                       ├ [1479]: usr/share/vim/vim91/syntax/lc.vim 
│                │                       ├ [1480]: usr/share/vim/vim91/syntax/ld.vim 
│                │                       ├ [1481]: usr/share/vim/vim91/syntax/ldapconf.vim 
│                │                       ├ [1482]: usr/share/vim/vim91/syntax/ldif.vim 
│                │                       ├ [1483]: usr/share/vim/vim91/syntax/leex.vim 
│                │                       ├ [1484]: usr/share/vim/vim91/syntax/less.vim 
│                │                       ├ [1485]: usr/share/vim/vim91/syntax/lex.vim 
│                │                       ├ [1486]: usr/share/vim/vim91/syntax/lf.vim 
│                │                       ├ [1487]: usr/share/vim/vim91/syntax/lftp.vim 
│                │                       ├ [1488]: usr/share/vim/vim91/syntax/lhaskell.vim 
│                │                       ├ [1489]: usr/share/vim/vim91/syntax/libao.vim 
│                │                       ├ [1490]: usr/share/vim/vim91/syntax/lidris2.vim 
│                │                       ├ [1491]: usr/share/vim/vim91/syntax/lifelines.vim 
│                │                       ├ [1492]: usr/share/vim/vim91/syntax/lilo.vim 
│                │                       ├ [1493]: usr/share/vim/vim91/syntax/limits.vim 
│                │                       ├ [1494]: usr/share/vim/vim91/syntax/liquid.vim 
│                │                       ├ [1495]: usr/share/vim/vim91/syntax/lisp.vim 
│                │                       ├ [1496]: usr/share/vim/vim91/syntax/lite.vim 
│                │                       ├ [1497]: usr/share/vim/vim91/syntax/litestep.vim 
│                │                       ├ [1498]: usr/share/vim/vim91/syntax/livebook.vim 
│                │                       ├ [1499]: usr/share/vim/vim91/syntax/lnk.vim 
│                │                       ├ [1500]: usr/share/vim/vim91/syntax/lnkmap.vim 
│                │                       ├ [1501]: usr/share/vim/vim91/syntax/log.vim 
│                │                       ├ [1502]: usr/share/vim/vim91/syntax/loginaccess.vim 
│                │                       ├ [1503]: usr/share/vim/vim91/syntax/logindefs.vim 
│                │                       ├ [1504]: usr/share/vim/vim91/syntax/logtalk.vim 
│                │                       ├ [1505]: usr/share/vim/vim91/syntax/lotos.vim 
│                │                       ├ [1506]: usr/share/vim/vim91/syntax/lout.vim 
│                │                       ├ [1507]: usr/share/vim/vim91/syntax/lpc.vim 
│                │                       ├ [1508]: usr/share/vim/vim91/syntax/lprolog.vim 
│                │                       ├ [1509]: usr/share/vim/vim91/syntax/lscript.vim 
│                │                       ├ [1510]: usr/share/vim/vim91/syntax/lsl.vim 
│                │                       ├ [1511]: usr/share/vim/vim91/syntax/lss.vim 
│                │                       ├ [1512]: usr/share/vim/vim91/syntax/lua.vim 
│                │                       ├ [1513]: usr/share/vim/vim91/syntax/luau.vim 
│                │                       ├ [1514]: usr/share/vim/vim91/syntax/lynx.vim 
│                │                       ├ [1515]: usr/share/vim/vim91/syntax/lyrics.vim 
│                │                       ├ [1516]: usr/share/vim/vim91/syntax/m17ndb.vim 
│                │                       ├ [1517]: usr/share/vim/vim91/syntax/m3build.vim 
│                │                       ├ [1518]: usr/share/vim/vim91/syntax/m3quake.vim 
│                │                       ├ [1519]: usr/share/vim/vim91/syntax/m4.vim 
│                │                       ├ [1520]: usr/share/vim/vim91/syntax/mail.vim 
│                │                       ├ [1521]: usr/share/vim/vim91/syntax/mailaliases.vim 
│                │                       ├ [1522]: usr/share/vim/vim91/syntax/mailcap.vim 
│                │                       ├ [1523]: usr/share/vim/vim91/syntax/make.vim 
│                │                       ├ [1524]: usr/share/vim/vim91/syntax/mallard.vim 
│                │                       ├ [1525]: usr/share/vim/vim91/syntax/man.vim 
│                │                       ├ [1526]: usr/share/vim/vim91/syntax/manconf.vim 
│                │                       ├ [1527]: usr/share/vim/vim91/syntax/manual.vim 
│                │                       ├ [1528]: usr/share/vim/vim91/syntax/maple.vim 
│                │                       ├ [1529]: usr/share/vim/vim91/syntax/markdown.vim 
│                │                       ├ [1530]: usr/share/vim/vim91/syntax/masm.vim 
│                │                       ├ [1531]: usr/share/vim/vim91/syntax/mason.vim 
│                │                       ├ [1532]: usr/share/vim/vim91/syntax/master.vim 
│                │                       ├ [1533]: usr/share/vim/vim91/syntax/matlab.vim 
│                │                       ├ [1534]: usr/share/vim/vim91/syntax/maxima.vim 
│                │                       ├ [1535]: usr/share/vim/vim91/syntax/mbsync.vim 
│                │                       ├ [1536]: usr/share/vim/vim91/syntax/mediawiki.vim 
│                │                       ├ [1537]: usr/share/vim/vim91/syntax/mel.vim 
│                │                       ├ [1538]: usr/share/vim/vim91/syntax/mermaid.vim 
│                │                       ├ [1539]: usr/share/vim/vim91/syntax/meson.vim 
│                │                       ├ [1540]: usr/share/vim/vim91/syntax/messages.vim 
│                │                       ├ [1541]: usr/share/vim/vim91/syntax/mf.vim 
│                │                       ├ [1542]: usr/share/vim/vim91/syntax/mgl.vim 
│                │                       ├ [1543]: usr/share/vim/vim91/syntax/mgp.vim 
│                │                       ├ [1544]: usr/share/vim/vim91/syntax/mib.vim 
│                │                       ├ [1545]: usr/share/vim/vim91/syntax/mix.vim 
│                │                       ├ [1546]: usr/share/vim/vim91/syntax/mma.vim 
│                │                       ├ [1547]: usr/share/vim/vim91/syntax/mmix.vim 
│                │                       ├ [1548]: usr/share/vim/vim91/syntax/mmp.vim 
│                │                       ├ [1549]: usr/share/vim/vim91/syntax/modconf.vim 
│                │                       ├ [1550]: usr/share/vim/vim91/syntax/model.vim 
│                │                       ├ [1551]: usr/share/vim/vim91/syntax/modsim3.vim 
│                │                       ├ [1552]: usr/share/vim/vim91/syntax/modula2.vim 
│                │                       ├ [1553]: usr/share/vim/vim91/syntax/modula3.vim 
│                │                       ├ [1554]: usr/share/vim/vim91/syntax/mojo.vim 
│                │                       ├ [1555]: usr/share/vim/vim91/syntax/monk.vim 
│                │                       ├ [1556]: usr/share/vim/vim91/syntax/moo.vim 
│                │                       ├ [1557]: usr/share/vim/vim91/syntax/mp.vim 
│                │                       ├ [1558]: usr/share/vim/vim91/syntax/mplayerconf.vim 
│                │                       ├ [1559]: usr/share/vim/vim91/syntax/mrxvtrc.vim 
│                │                       ├ [1560]: usr/share/vim/vim91/syntax/msidl.vim 
│                │                       ├ [1561]: usr/share/vim/vim91/syntax/msmessages.vim 
│                │                       ├ [1562]: usr/share/vim/vim91/syntax/msql.vim 
│                │                       ├ [1563]: usr/share/vim/vim91/syntax/mss.vim 
│                │                       ├ [1564]: usr/share/vim/vim91/syntax/mupad.vim 
│                │                       ├ [1565]: usr/share/vim/vim91/syntax/murphi.vim 
│                │                       ├ [1566]: usr/share/vim/vim91/syntax/mush.vim 
│                │                       ├ [1567]: usr/share/vim/vim91/syntax/muttrc.vim 
│                │                       ├ [1568]: usr/share/vim/vim91/syntax/mysql.vim 
│                │                       ├ [1569]: usr/share/vim/vim91/syntax/n1ql.vim 
│                │                       ├ [1570]: usr/share/vim/vim91/syntax/named.vim 
│                │                       ├ [1571]: usr/share/vim/vim91/syntax/nanorc.vim 
│                │                       ├ [1572]: usr/share/vim/vim91/syntax/nasm.vim 
│                │                       ├ [1573]: usr/share/vim/vim91/syntax/nastran.vim 
│                │                       ├ [1574]: usr/share/vim/vim91/syntax/natural.vim 
│                │                       ├ [1575]: usr/share/vim/vim91/syntax/ncf.vim 
│                │                       ├ [1576]: usr/share/vim/vim91/syntax/neomuttlog.vim 
│                │                       ├ [1577]: usr/share/vim/vim91/syntax/neomuttrc.vim 
│                │                       ├ [1578]: usr/share/vim/vim91/syntax/netrc.vim 
│                │                       ├ [1579]: usr/share/vim/vim91/syntax/nginx.vim 
│                │                       ├ [1580]: usr/share/vim/vim91/syntax/ninja.vim 
│                │                       ├ [1581]: usr/share/vim/vim91/syntax/nix.vim 
│                │                       ├ [1582]: usr/share/vim/vim91/syntax/nosyntax.vim 
│                │                       ├ [1583]: usr/share/vim/vim91/syntax/nqc.vim 
│                │                       ├ [1584]: usr/share/vim/vim91/syntax/nroff.vim 
│                │                       ├ [1585]: usr/share/vim/vim91/syntax/nsis.vim 
│                │                       ├ [1586]: usr/share/vim/vim91/syntax/nu.vim 
│                │                       ├ [1587]: usr/share/vim/vim91/syntax/obj.vim 
│                │                       ├ [1588]: usr/share/vim/vim91/syntax/objc.vim 
│                │                       ├ [1589]: usr/share/vim/vim91/syntax/objcpp.vim 
│                │                       ├ [1590]: usr/share/vim/vim91/syntax/obse.vim 
│                │                       ├ [1591]: usr/share/vim/vim91/syntax/ocaml.vim 
│                │                       ├ [1592]: usr/share/vim/vim91/syntax/occam.vim 
│                │                       ├ [1593]: usr/share/vim/vim91/syntax/odin.vim 
│                │                       ├ [1594]: usr/share/vim/vim91/syntax/omnimark.vim 
│                │                       ├ [1595]: usr/share/vim/vim91/syntax/ondir.vim 
│                │                       ├ [1596]: usr/share/vim/vim91/syntax/opam.vim 
│                │                       ├ [1597]: usr/share/vim/vim91/syntax/opencl.vim 
│                │                       ├ [1598]: usr/share/vim/vim91/syntax/openroad.vim 
│                │                       ├ [1599]: usr/share/vim/vim91/syntax/openscad.vim 
│                │                       ├ [1600]: usr/share/vim/vim91/syntax/openvpn.vim 
│                │                       ├ [1601]: usr/share/vim/vim91/syntax/opl.vim 
│                │                       ├ [1602]: usr/share/vim/vim91/syntax/ora.vim 
│                │                       ├ [1603]: usr/share/vim/vim91/syntax/org.vim 
│                │                       ├ [1604]: usr/share/vim/vim91/syntax/pacmanlog.vim 
│                │                       ├ [1605]: usr/share/vim/vim91/syntax/pamconf.vim 
│                │                       ├ [1606]: usr/share/vim/vim91/syntax/pamenv.vim 
│                │                       ├ [1607]: usr/share/vim/vim91/syntax/pandoc.vim 
│                │                       ├ [1608]: usr/share/vim/vim91/syntax/papp.vim 
│                │                       ├ [1609]: usr/share/vim/vim91/syntax/pascal.vim 
│                │                       ├ [1610]: usr/share/vim/vim91/syntax/passwd.vim 
│                │                       ├ [1611]: usr/share/vim/vim91/syntax/pbtxt.vim 
│                │                       ├ [1612]: usr/share/vim/vim91/syntax/pcap.vim 
│                │                       ├ [1613]: usr/share/vim/vim91/syntax/pccts.vim 
│                │                       ├ [1614]: usr/share/vim/vim91/syntax/pdf.vim 
│                │                       ├ [1615]: usr/share/vim/vim91/syntax/perl.vim 
│                │                       ├ [1616]: usr/share/vim/vim91/syntax/pf.vim 
│                │                       ├ [1617]: usr/share/vim/vim91/syntax/pfmain.vim 
│                │                       ├ [1618]: usr/share/vim/vim91/syntax/php.vim 
│                │                       ├ [1619]: usr/share/vim/vim91/syntax/phtml.vim 
│                │                       ├ [1620]: usr/share/vim/vim91/syntax/pic.vim 
│                │                       ├ [1621]: usr/share/vim/vim91/syntax/pike.vim 
│                │                       ├ [1622]: usr/share/vim/vim91/syntax/pilrc.vim 
│                │                       ├ [1623]: usr/share/vim/vim91/syntax/pine.vim 
│                │                       ├ [1624]: usr/share/vim/vim91/syntax/pinfo.vim 
│                │                       ├ [1625]: usr/share/vim/vim91/syntax/pkl.vim 
│                │                       ├ [1626]: usr/share/vim/vim91/syntax/plaintex.vim 
│                │                       ├ [1627]: usr/share/vim/vim91/syntax/pli.vim 
│                │                       ├ [1628]: usr/share/vim/vim91/syntax/plm.vim 
│                │                       ├ [1629]: usr/share/vim/vim91/syntax/plp.vim 
│                │                       ├ [1630]: usr/share/vim/vim91/syntax/plsql.vim 
│                │                       ├ [1631]: usr/share/vim/vim91/syntax/po.vim 
│                │                       ├ [1632]: usr/share/vim/vim91/syntax/pod.vim 
│                │                       ├ [1633]: usr/share/vim/vim91/syntax/poefilter.vim 
│                │                       ├ [1634]: usr/share/vim/vim91/syntax/poke.vim 
│                │                       ├ [1635]: usr/share/vim/vim91/syntax/postscr.vim 
│                │                       ├ [1636]: usr/share/vim/vim91/syntax/pov.vim 
│                │                       ├ [1637]: usr/share/vim/vim91/syntax/povini.vim 
│                │                       ├ [1638]: usr/share/vim/vim91/syntax/ppd.vim 
│                │                       ├ [1639]: usr/share/vim/vim91/syntax/ppwiz.vim 
│                │                       ├ [1640]: usr/share/vim/vim91/syntax/pq.vim 
│                │                       ├ [1641]: usr/share/vim/vim91/syntax/prescribe.vim 
│                │                       ├ [1642]: usr/share/vim/vim91/syntax/privoxy.vim 
│                │                       ├ [1643]: usr/share/vim/vim91/syntax/procmail.vim 
│                │                       ├ [1644]: usr/share/vim/vim91/syntax/progress.vim 
│                │                       ├ [1645]: usr/share/vim/vim91/syntax/prolog.vim 
│                │                       ├ [1646]: usr/share/vim/vim91/syntax/promela.vim 
│                │                       ├ [1647]: usr/share/vim/vim91/syntax/proto.vim 
│                │                       ├ [1648]: usr/share/vim/vim91/syntax/protocols.vim 
│                │                       ├ [1649]: usr/share/vim/vim91/syntax/prql.vim 
│                │                       ├ [1650]: usr/share/vim/vim91/syntax/ps1.vim 
│                │                       ├ [1651]: usr/share/vim/vim91/syntax/ps1xml.vim 
│                │                       ├ [1652]: usr/share/vim/vim91/syntax/psf.vim 
│                │                       ├ [1653]: usr/share/vim/vim91/syntax/psl.vim 
│                │                       ├ [1654]: usr/share/vim/vim91/syntax/ptcap.vim 
│                │                       ├ [1655]: usr/share/vim/vim91/syntax/ptx.vim 
│                │                       ├ [1656]: usr/share/vim/vim91/syntax/purifylog.vim 
│                │                       ├ [1657]: usr/share/vim/vim91/syntax/pymanifest.vim 
│                │                       ├ [1658]: usr/share/vim/vim91/syntax/pyrex.vim 
│                │                       ├ [1659]: usr/share/vim/vim91/syntax/python.vim 
│                │                       ├ [1660]: usr/share/vim/vim91/syntax/python2.vim 
│                │                       ├ [1661]: usr/share/vim/vim91/syntax/qb64.vim 
│                │                       ├ [1662]: usr/share/vim/vim91/syntax/qf.vim 
│                │                       ├ [1663]: usr/share/vim/vim91/syntax/qml.vim 
│                │                       ├ [1664]: usr/share/vim/vim91/syntax/quake.vim 
│                │                       ├ [1665]: usr/share/vim/vim91/syntax/quarto.vim 
│                │                       ├ [1666]: usr/share/vim/vim91/syntax/r.vim 
│                │                       ├ [1667]: usr/share/vim/vim91/syntax/racc.vim 
│                │                       ├ [1668]: usr/share/vim/vim91/syntax/racket.vim 
│                │                       ├ [1669]: usr/share/vim/vim91/syntax/radiance.vim 
│                │                       ├ [1670]: usr/share/vim/vim91/syntax/raku.vim 
│                │                       ├ [1671]: usr/share/vim/vim91/syntax/raml.vim 
│                │                       ├ [1672]: usr/share/vim/vim91/syntax/rapid.vim 
│                │                       ├ [1673]: usr/share/vim/vim91/syntax/rasi.vim 
│                │                       ├ [1674]: usr/share/vim/vim91/syntax/ratpoison.vim 
│                │                       ├ [1675]: usr/share/vim/vim91/syntax/rc.vim 
│                │                       ├ [1676]: usr/share/vim/vim91/syntax/rcs.vim 
│                │                       ├ [1677]: usr/share/vim/vim91/syntax/rcslog.vim 
│                │                       ├ [1678]: usr/share/vim/vim91/syntax/readline.vim 
│                │                       ├ [1679]: usr/share/vim/vim91/syntax/rebol.vim 
│                │                       ├ [1680]: usr/share/vim/vim91/syntax/redif.vim 
│                │                       ├ [1681]: usr/share/vim/vim91/syntax/registry.vim 
│                │                       ├ [1682]: usr/share/vim/vim91/syntax/rego.vim 
│                │                       ├ [1683]: usr/share/vim/vim91/syntax/remind.vim 
│                │                       ├ [1684]: usr/share/vim/vim91/syntax/requirements.vim 
│                │                       ├ [1685]: usr/share/vim/vim91/syntax/resolv.vim 
│                │                       ├ [1686]: usr/share/vim/vim91/syntax/reva.vim 
│                │                       ├ [1687]: usr/share/vim/vim91/syntax/rexx.vim 
│                │                       ├ [1688]: usr/share/vim/vim91/syntax/rhelp.vim 
│                │                       ├ [1689]: usr/share/vim/vim91/syntax/rib.vim 
│                │                       ├ [1690]: usr/share/vim/vim91/syntax/rmd.vim 
│                │                       ├ [1691]: usr/share/vim/vim91/syntax/rnc.vim 
│                │                       ├ [1692]: usr/share/vim/vim91/syntax/rng.vim 
│                │                       ├ [1693]: usr/share/vim/vim91/syntax/rnoweb.vim 
│                │                       ├ [1694]: usr/share/vim/vim91/syntax/robots.vim 
│                │                       ├ [1695]: usr/share/vim/vim91/syntax/routeros.vim 
│                │                       ├ [1696]: usr/share/vim/vim91/syntax/rpcgen.vim 
│                │                       ├ [1697]: usr/share/vim/vim91/syntax/rpl.vim 
│                │                       ├ [1698]: usr/share/vim/vim91/syntax/rrst.vim 
│                │                       ├ [1699]: usr/share/vim/vim91/syntax/rst.vim 
│                │                       ├ [1700]: usr/share/vim/vim91/syntax/rtf.vim 
│                │                       ├ [1701]: usr/share/vim/vim91/syntax/ruby.vim 
│                │                       ├ [1702]: usr/share/vim/vim91/syntax/rust.vim 
│                │                       ├ [1703]: usr/share/vim/vim91/syntax/salt.vim 
│                │                       ├ [1704]: usr/share/vim/vim91/syntax/samba.vim 
│                │                       ├ [1705]: usr/share/vim/vim91/syntax/sas.vim 
│                │                       ├ [1706]: usr/share/vim/vim91/syntax/sass.vim 
│                │                       ├ [1707]: usr/share/vim/vim91/syntax/sather.vim 
│                │                       ├ [1708]: usr/share/vim/vim91/syntax/sbt.vim 
│                │                       ├ [1709]: usr/share/vim/vim91/syntax/scala.vim 
│                │                       ├ [1710]: usr/share/vim/vim91/syntax/scdoc.vim 
│                │                       ├ [1711]: usr/share/vim/vim91/syntax/scheme.vim 
│                │                       ├ [1712]: usr/share/vim/vim91/syntax/scilab.vim 
│                │                       ├ [1713]: usr/share/vim/vim91/syntax/screen.vim 
│                │                       ├ [1714]: usr/share/vim/vim91/syntax/scss.vim 
│                │                       ├ [1715]: usr/share/vim/vim91/syntax/sd.vim 
│                │                       ├ [1716]: usr/share/vim/vim91/syntax/sdc.vim 
│                │                       ├ [1717]: usr/share/vim/vim91/syntax/sdl.vim 
│                │                       ├ [1718]: usr/share/vim/vim91/syntax/sed.vim 
│                │                       ├ [1719]: usr/share/vim/vim91/syntax/sendpr.vim 
│                │                       ├ [1720]: usr/share/vim/vim91/syntax/sensors.vim 
│                │                       ├ [1721]: usr/share/vim/vim91/syntax/services.vim 
│                │                       ├ [1722]: usr/share/vim/vim91/syntax/setserial.vim 
│                │                       ├ [1723]: usr/share/vim/vim91/syntax/sexplib.vim 
│                │                       ├ [1724]: usr/share/vim/vim91/syntax/sgml.vim 
│                │                       ├ [1725]: usr/share/vim/vim91/syntax/sgmldecl.vim 
│                │                       ├ [1726]: usr/share/vim/vim91/syntax/sgmllnx.vim 
│                │                       ├ [1727]: usr/share/vim/vim91/syntax/sh.vim 
│                │                       ├ [1728]: usr/share/vim/vim91/syntax/shaderslang.vim 
│                │                       ├ [1729]: usr/share/vim/vim91/syntax/sicad.vim 
│                │                       ├ [1730]: usr/share/vim/vim91/syntax/sieve.vim 
│                │                       ├ [1731]: usr/share/vim/vim91/syntax/sil.vim 
│                │                       ├ [1732]: usr/share/vim/vim91/syntax/simula.vim 
│                │                       ├ [1733]: usr/share/vim/vim91/syntax/sinda.vim 
│                │                       ├ [1734]: usr/share/vim/vim91/syntax/sindacmp.vim 
│                │                       ├ [1735]: usr/share/vim/vim91/syntax/sindaout.vim 
│                │                       ├ [1736]: usr/share/vim/vim91/syntax/sisu.vim 
│                │                       ├ [1737]: usr/share/vim/vim91/syntax/skill.vim 
│                │                       ├ [1738]: usr/share/vim/vim91/syntax/sl.vim 
│                │                       ├ [1739]: usr/share/vim/vim91/syntax/slang.vim 
│                │                       ├ [1740]: usr/share/vim/vim91/syntax/slice.vim 
│                │                       ├ [1741]: usr/share/vim/vim91/syntax/slpconf.vim 
│                │                       ├ [1742]: usr/share/vim/vim91/syntax/slpreg.vim 
│                │                       ├ [1743]: usr/share/vim/vim91/syntax/slpspi.vim 
│                │                       ├ [1744]: usr/share/vim/vim91/syntax/slrnrc.vim 
│                │                       ├ [1745]: usr/share/vim/vim91/syntax/slrnsc.vim 
│                │                       ├ [1746]: usr/share/vim/vim91/syntax/sm.vim 
│                │                       ├ [1747]: usr/share/vim/vim91/syntax/smarty.vim 
│                │                       ├ [1748]: usr/share/vim/vim91/syntax/smcl.vim 
│                │                       ├ [1749]: usr/share/vim/vim91/syntax/smil.vim 
│                │                       ├ [1750]: usr/share/vim/vim91/syntax/smith.vim 
│                │                       ├ [1751]: usr/share/vim/vim91/syntax/sml.vim 
│                │                       ├ [1752]: usr/share/vim/vim91/syntax/snnsnet.vim 
│                │                       ├ [1753]: usr/share/vim/vim91/syntax/snnspat.vim 
│                │                       ├ [1754]: usr/share/vim/vim91/syntax/snnsres.vim 
│                │                       ├ [1755]: usr/share/vim/vim91/syntax/snobol4.vim 
│                │                       ├ [1756]: usr/share/vim/vim91/syntax/solidity.vim 
│                │                       ├ [1757]: usr/share/vim/vim91/syntax/spajson.vim 
│                │                       ├ [1758]: usr/share/vim/vim91/syntax/spec.vim 
│                │                       ├ [1759]: usr/share/vim/vim91/syntax/specman.vim 
│                │                       ├ [1760]: usr/share/vim/vim91/syntax/spice.vim 
│                │                       ├ [1761]: usr/share/vim/vim91/syntax/splint.vim 
│                │                       ├ [1762]: usr/share/vim/vim91/syntax/spup.vim 
│                │                       ├ [1763]: usr/share/vim/vim91/syntax/spyce.vim 
│                │                       ├ [1764]: usr/share/vim/vim91/syntax/sql.vim 
│                │                       ├ [1765]: usr/share/vim/vim91/syntax/sqlanywhere.vim 
│                │                       ├ [1766]: usr/share/vim/vim91/syntax/sqlforms.vim 
│                │                       ├ [1767]: usr/share/vim/vim91/syntax/sqlhana.vim 
│                │                       ├ [1768]: usr/share/vim/vim91/syntax/sqlinformix.vim 
│                │                       ├ [1769]: usr/share/vim/vim91/syntax/sqlj.vim 
│                │                       ├ [1770]: usr/share/vim/vim91/syntax/sqloracle.vim 
│                │                       ├ [1771]: usr/share/vim/vim91/syntax/sqr.vim 
│                │                       ├ [1772]: usr/share/vim/vim91/syntax/squid.vim 
│                │                       ├ [1773]: usr/share/vim/vim91/syntax/squirrel.vim 
│                │                       ├ [1774]: usr/share/vim/vim91/syntax/srec.vim 
│                │                       ├ [1775]: usr/share/vim/vim91/syntax/srt.vim 
│                │                       ├ [1776]: usr/share/vim/vim91/syntax/ssa.vim 
│                │                       ├ [1777]: usr/share/vim/vim91/syntax/sshconfig.vim 
│                │                       ├ [1778]: usr/share/vim/vim91/syntax/sshdconfig.vim 
│                │                       ├ [1779]: usr/share/vim/vim91/syntax/st.vim 
│                │                       ├ [1780]: usr/share/vim/vim91/syntax/stata.vim 
│                │                       ├ [1781]: usr/share/vim/vim91/syntax/stp.vim 
│                │                       ├ [1782]: usr/share/vim/vim91/syntax/strace.vim 
│                │                       ├ [1783]: usr/share/vim/vim91/syntax/structurizr.vim 
│                │                       ├ [1784]: usr/share/vim/vim91/syntax/stylus.vim 
│                │                       ├ [1785]: usr/share/vim/vim91/syntax/sudoers.vim 
│                │                       ├ [1786]: usr/share/vim/vim91/syntax/svg.vim 
│                │                       ├ [1787]: usr/share/vim/vim91/syntax/svn.vim 
│                │                       ├ [1788]: usr/share/vim/vim91/syntax/swayconfig.vim 
│                │                       ├ [1789]: usr/share/vim/vim91/syntax/swift.vim 
│                │                       ├ [1790]: usr/share/vim/vim91/syntax/swiftgyb.vim 
│                │                       ├ [1791]: usr/share/vim/vim91/syntax/swig.vim 
│                │                       ├ [1792]: usr/share/vim/vim91/syntax/syncolor.vim 
│                │                       ├ [1793]: usr/share/vim/vim91/syntax/synload.vim 
│                │                       ├ [1794]: usr/share/vim/vim91/syntax/syntax.vim 
│                │                       ├ [1795]: usr/share/vim/vim91/syntax/sysctl.vim 
│                │                       ├ [1796]: usr/share/vim/vim91/syntax/systemd.vim 
│                │                       ├ [1797]: usr/share/vim/vim91/syntax/systemverilog.vim 
│                │                       ├ [1798]: usr/share/vim/vim91/syntax/tads.vim 
│                │                       ├ [1799]: usr/share/vim/vim91/syntax/tags.vim 
│                │                       ├ [1800]: usr/share/vim/vim91/syntax/tak.vim 
│                │                       ├ [1801]: usr/share/vim/vim91/syntax/takcmp.vim 
│                │                       ├ [1802]: usr/share/vim/vim91/syntax/takout.vim 
│                │                       ├ [1803]: usr/share/vim/vim91/syntax/tap.vim 
│                │                       ├ [1804]: usr/share/vim/vim91/syntax/tar.vim 
│                │                       ├ [1805]: usr/share/vim/vim91/syntax/taskdata.vim 
│                │                       ├ [1806]: usr/share/vim/vim91/syntax/taskedit.vim 
│                │                       ├ [1807]: usr/share/vim/vim91/syntax/tasm.vim 
│                │                       ├ [1808]: usr/share/vim/vim91/syntax/tcl.vim 
│                │                       ├ [1809]: usr/share/vim/vim91/syntax/tcsh.vim 
│                │                       ├ [1810]: usr/share/vim/vim91/syntax/template.vim 
│                │                       ├ [1811]: usr/share/vim/vim91/syntax/tera.vim 
│                │                       ├ [1812]: usr/share/vim/vim91/syntax/teraterm.vim 
│                │                       ├ [1813]: usr/share/vim/vim91/syntax/terminfo.vim 
│                │                       ├ [1814]: usr/share/vim/vim91/syntax/terraform.vim 
│                │                       ├ [1815]: usr/share/vim/vim91/syntax/tex.vim 
│                │                       ├ [1816]: usr/share/vim/vim91/syntax/texinfo.vim 
│                │                       ├ [1817]: usr/share/vim/vim91/syntax/texmf.vim 
│                │                       ├ [1818]: usr/share/vim/vim91/syntax/tf.vim 
│                │                       ├ [1819]: usr/share/vim/vim91/syntax/thrift.vim 
│                │                       ├ [1820]: usr/share/vim/vim91/syntax/tiasm.vim 
│                │                       ├ [1821]: usr/share/vim/vim91/syntax/tidy.vim 
│                │                       ├ [1822]: usr/share/vim/vim91/syntax/tilde.vim 
│                │                       ├ [1823]: usr/share/vim/vim91/syntax/tli.vim 
│                │                       ├ [1824]: usr/share/vim/vim91/syntax/tmux.vim 
│                │                       ├ [1825]: usr/share/vim/vim91/syntax/toml.vim 
│                │                       ├ [1826]: usr/share/vim/vim91/syntax/tpp.vim 
│                │                       ├ [1827]: usr/share/vim/vim91/syntax/trasys.vim 
│                │                       ├ [1828]: usr/share/vim/vim91/syntax/treetop.vim 
│                │                       ├ [1829]: usr/share/vim/vim91/syntax/trustees.vim 
│                │                       ├ [1830]: usr/share/vim/vim91/syntax/tsalt.vim 
│                │                       ├ [1831]: usr/share/vim/vim91/syntax/tsscl.vim 
│                │                       ├ [1832]: usr/share/vim/vim91/syntax/tssgm.vim 
│                │                       ├ [1833]: usr/share/vim/vim91/syntax/tssop.vim 
│                │                       ├ [1834]: usr/share/vim/vim91/syntax/tsv.vim 
│                │                       ├ [1835]: usr/share/vim/vim91/syntax/tt2.vim 
│                │                       ├ [1836]: usr/share/vim/vim91/syntax/tt2html.vim 
│                │                       ├ [1837]: usr/share/vim/vim91/syntax/tt2js.vim 
│                │                       ├ [1838]: usr/share/vim/vim91/syntax/tutor.vim 
│                │                       ├ [1839]: usr/share/vim/vim91/syntax/typescript.vim 
│                │                       ├ [1840]: usr/share/vim/vim91/syntax/typescriptreact.vim 
│                │                       ├ [1841]: usr/share/vim/vim91/syntax/typst.vim 
│                │                       ├ [1842]: usr/share/vim/vim91/syntax/uc.vim 
│                │                       ├ [1843]: usr/share/vim/vim91/syntax/uci.vim 
│                │                       ├ [1844]: usr/share/vim/vim91/syntax/udevconf.vim 
│                │                       ├ [1845]: usr/share/vim/vim91/syntax/udevperm.vim 
│                │                       ├ [1846]: usr/share/vim/vim91/syntax/udevrules.vim 
│                │                       ├ [1847]: usr/share/vim/vim91/syntax/uil.vim 
│                │                       ├ [1848]: usr/share/vim/vim91/syntax/unison.vim 
│                │                       ├ [1849]: usr/share/vim/vim91/syntax/updatedb.vim 
│                │                       ├ [1850]: usr/share/vim/vim91/syntax/upstart.vim 
│                │                       ├ [1851]: usr/share/vim/vim91/syntax/upstreamdat.vim 
│                │                       ├ [1852]: usr/share/vim/vim91/syntax/upstreaminstalllog.vim 
│                │                       ├ [1853]: usr/share/vim/vim91/syntax/upstreamlog.vim 
│                │                       ├ [1854]: usr/share/vim/vim91/syntax/upstreamrpt.vim 
│                │                       ├ [1855]: usr/share/vim/vim91/syntax/urlshortcut.vim 
│                │                       ├ [1856]: usr/share/vim/vim91/syntax/usserverlog.vim 
│                │                       ├ [1857]: usr/share/vim/vim91/syntax/usw2kagtlog.vim 
│                │                       ├ [1858]: usr/share/vim/vim91/syntax/valgrind.vim 
│                │                       ├ [1859]: usr/share/vim/vim91/syntax/vb.vim 
│                │                       ├ [1860]: usr/share/vim/vim91/syntax/vdf.vim 
│                │                       ├ [1861]: usr/share/vim/vim91/syntax/vera.vim 
│                │                       ├ [1862]: usr/share/vim/vim91/syntax/verilog.vim 
│                │                       ├ [1863]: usr/share/vim/vim91/syntax/verilogams.vim 
│                │                       ├ [1864]: usr/share/vim/vim91/syntax/vgrindefs.vim 
│                │                       ├ [1865]: usr/share/vim/vim91/syntax/vhdl.vim 
│                │                       ├ [1866]: usr/share/vim/vim91/syntax/vim.vim 
│                │                       ├ [1867]: usr/share/vim/vim91/syntax/viminfo.vim 
│                │                       ├ [1868]: usr/share/vim/vim91/syntax/vimnormal.vim 
│                │                       ├ [1869]: usr/share/vim/vim91/syntax/virata.vim 
│                │                       ├ [1870]: usr/share/vim/vim91/syntax/vmasm.vim 
│                │                       ├ [1871]: usr/share/vim/vim91/syntax/voscm.vim 
│                │                       ├ [1872]: usr/share/vim/vim91/syntax/vrml.vim 
│                │                       ├ [1873]: usr/share/vim/vim91/syntax/vroom.vim 
│                │                       ├ [1874]: usr/share/vim/vim91/syntax/vsejcl.vim 
│                │                       ├ [1875]: usr/share/vim/vim91/syntax/vue.vim 
│                │                       ├ [1876]: usr/share/vim/vim91/syntax/wat.vim 
│                │                       ├ [1877]: usr/share/vim/vim91/syntax/wdiff.vim 
│                │                       ├ [1878]: usr/share/vim/vim91/syntax/wdl.vim 
│                │                       ├ [1879]: usr/share/vim/vim91/syntax/web.vim 
│                │                       ├ [1880]: usr/share/vim/vim91/syntax/webmacro.vim 
│                │                       ├ [1881]: usr/share/vim/vim91/syntax/wget.vim 
│                │                       ├ [1882]: usr/share/vim/vim91/syntax/wget2.vim 
│                │                       ├ [1883]: usr/share/vim/vim91/syntax/whitespace.vim 
│                │                       ├ [1884]: usr/share/vim/vim91/syntax/winbatch.vim 
│                │                       ├ [1885]: usr/share/vim/vim91/syntax/wml.vim 
│                │                       ├ [1886]: usr/share/vim/vim91/syntax/wsh.vim 
│                │                       ├ [1887]: usr/share/vim/vim91/syntax/wsml.vim 
│                │                       ├ [1888]: usr/share/vim/vim91/syntax/wvdial.vim 
│                │                       ├ [1889]: usr/share/vim/vim91/syntax/xbl.vim 
│                │                       ├ [1890]: usr/share/vim/vim91/syntax/xcompose.vim 
│                │                       ├ [1891]: usr/share/vim/vim91/syntax/xdefaults.vim 
│                │                       ├ [1892]: usr/share/vim/vim91/syntax/xf86conf.vim 
│                │                       ├ [1893]: usr/share/vim/vim91/syntax/xhtml.vim 
│                │                       ├ [1894]: usr/share/vim/vim91/syntax/xinetd.vim 
│                │                       ├ [1895]: usr/share/vim/vim91/syntax/xkb.vim 
│                │                       ├ [1896]: usr/share/vim/vim91/syntax/xmath.vim 
│                │                       ├ [1897]: usr/share/vim/vim91/syntax/xml.vim 
│                │                       ├ [1898]: usr/share/vim/vim91/syntax/xmodmap.vim 
│                │                       ├ [1899]: usr/share/vim/vim91/syntax/xpm.vim 
│                │                       ├ [1900]: usr/share/vim/vim91/syntax/xpm2.vim 
│                │                       ├ [1901]: usr/share/vim/vim91/syntax/xquery.vim 
│                │                       ├ [1902]: usr/share/vim/vim91/syntax/xs.vim 
│                │                       ├ [1903]: usr/share/vim/vim91/syntax/xsd.vim 
│                │                       ├ [1904]: usr/share/vim/vim91/syntax/xslt.vim 
│                │                       ├ [1905]: usr/share/vim/vim91/syntax/xxd.vim 
│                │                       ├ [1906]: usr/share/vim/vim91/syntax/yacc.vim 
│                │                       ├ [1907]: usr/share/vim/vim91/syntax/yaml.vim 
│                │                       ├ [1908]: usr/share/vim/vim91/syntax/z8a.vim 
│                │                       ├ [1909]: usr/share/vim/vim91/syntax/zathurarc.vim 
│                │                       ├ [1910]: usr/share/vim/vim91/syntax/zig.vim 
│                │                       ├ [1911]: usr/share/vim/vim91/syntax/zimbu.vim 
│                │                       ├ [1912]: usr/share/vim/vim91/syntax/zir.vim 
│                │                       ├ [1913]: usr/share/vim/vim91/syntax/zserio.vim 
│                │                       ├ [1914]: usr/share/vim/vim91/syntax/zsh.vim 
│                │                       ├ [1915]: usr/share/vim/vim91/syntax/modula2/opt/iso.vim 
│                │                       ├ [1916]: usr/share/vim/vim91/syntax/modula2/opt/pim.vim 
│                │                       ├ [1917]: usr/share/vim/vim91/syntax/modula2/opt/r10.vim 
│                │                       ├ [1918]: usr/share/vim/vim91/syntax/shared/README.txt 
│                │                       ├ [1919]: usr/share/vim/vim91/syntax/shared/context-data-context.vim 
│                │                       ├ [1920]: usr/share/vim/vim91/syntax/shared/context-data-interfaces.vim 
│                │                       ├ [1921]: usr/share/vim/vim91/syntax/shared/context-data-metafun.vim 
│                │                       ├ [1922]: usr/share/vim/vim91/syntax/shared/context-data-tex.vim 
│                │                       ├ [1923]: usr/share/vim/vim91/syntax/shared/debarchitectures.vim 
│                │                       ├ [1924]: usr/share/vim/vim91/syntax/shared/debversions.vim 
│                │                       ├ [1925]: usr/share/vim/vim91/syntax/shared/hgcommitDiff.vim 
│                │                       ├ [1926]: usr/share/vim/vim91/syntax/shared/typescriptcommon.vim 
│                │                       ├ [1927]: usr/share/vim/vim91/tools/README.txt 
│                │                       ├ [1928]: usr/share/vim/vim91/tools/blink.c 
│                │                       ├ [1929]: usr/share/vim/vim91/tools/ccfilter.1 
│                │                       ├ [1930]: usr/share/vim/vim91/tools/ccfilter.c 
│                │                       ├ [1931]: usr/share/vim/vim91/tools/ccfilter_README.txt 
│                │                       ├ [1932]: usr/share/vim/vim91/tools/demoserver.py 
│                │                       ├ [1933]: usr/share/vim/vim91/tools/efm_filter.pl 
│                │                       ├ [1934]: usr/share/vim/vim91/tools/efm_filter.txt 
│                │                       ├ [1935]: usr/share/vim/vim91/tools/efm_perl.pl 
│                │                       ├ [1936]: usr/share/vim/vim91/tools/emoji_list.vim 
│                │                       ├ [1937]: usr/share/vim/vim91/tools/mve.awk 
│                │                       ├ [1938]: usr/share/vim/vim91/tools/mve.txt 
│                │                       ├ [1939]: usr/share/vim/vim91/tools/pltags.pl 
│                │                       ├ [1940]: usr/share/vim/vim91/tools/ref 
│                │                       ├ [1941]: usr/share/vim/vim91/tools/shtags.1 
│                │                       ├ [1942]: usr/share/vim/vim91/tools/shtags.pl 
│                │                       ├ [1943]: usr/share/vim/vim91/tools/unicode.vim 
│                │                       ├ [1944]: usr/share/vim/vim91/tools/vim132 
│                │                       ├ [1945]: usr/share/vim/vim91/tools/vim_vs_net.cmd 
│                │                       ├ [1946]: usr/share/vim/vim91/tools/vimm 
│                │                       ├ [1947]: usr/share/vim/vim91/tools/vimspell.sh 
│                │                       ├ [1948]: usr/share/vim/vim91/tools/vimspell.txt 
│                │                       ╰ [1949]: usr/share/vim/vim91/tools/xcmdsrv_client.c 
│                ├ [63] ╭ ID            : xxd@9.1.1952-r0 
│                │      ├ Name          : xxd 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/xxd@9.1.1952-r0?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : 68704576a2918884 
│                │      ├ Version       : 9.1.1952-r0 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : vim 
│                │      ├ SrcVersion    : 9.1.1952-r0 
│                │      ├ Licenses       ─ [0]: Vim 
│                │      ├ Maintainer    : Celeste <cielesti@protonmail.com> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:dd4b08f299a2d466b242589bcf752af21724a9ea 
│                │      ╰ InstalledFiles ─ [0]: usr/bin/xxd 
│                ├ [64] ╭ ID            : zlib@1.3.1-r2 
│                │      ├ Name          : zlib 
│                │      ├ Identifier     ╭ PURL: pkg:apk/alpine/zlib@1.3.1-r2?arch=x86_64&distro=3.23.0 
│                │      │                ╰ UID : c31e71c761b6c7b3 
│                │      ├ Version       : 1.3.1-r2 
│                │      ├ Arch          : x86_64 
│                │      ├ SrcName       : zlib 
│                │      ├ SrcVersion    : 1.3.1-r2 
│                │      ├ Licenses       ─ [0]: Zlib 
│                │      ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                │      ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                │      ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                │      │                │         49054a1b280 
│                │      │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                │      │                          fbf87a91d77 
│                │      ├ Digest        : sha1:7f6d1b44c82e08e09edc330137f50a408f87b6d6 
│                │      ╰ InstalledFiles ╭ [0]: usr/lib/libz.so.1 
│                │                       ╰ [1]: usr/lib/libz.so.1.3.1 
│                ╰ [65] ╭ ID            : zstd-libs@1.5.7-r2 
│                       ├ Name          : zstd-libs 
│                       ├ Identifier     ╭ PURL: pkg:apk/alpine/zstd-libs@1.5.7-r2?arch=x86_64&distro=3.23.0 
│                       │                ╰ UID : b14648875a02034 
│                       ├ Version       : 1.5.7-r2 
│                       ├ Arch          : x86_64 
│                       ├ SrcName       : zstd 
│                       ├ SrcVersion    : 1.5.7-r2 
│                       ├ Licenses       ╭ [0]: BSD-3-Clause 
│                       │                ╰ [1]: GPL-2.0-or-later 
│                       ├ Maintainer    : Natanael Copa <ncopa@alpinelinux.org> 
│                       ├ DependsOn      ─ [0]: musl@1.2.5-r21 
│                       ├ Layer          ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d1
│                       │                │         49054a1b280 
│                       │                ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37
│                       │                          fbf87a91d77 
│                       ├ Digest        : sha1:43ac44ea9c46b340ba31d8f7fe10469f2d4223f4 
│                       ╰ InstalledFiles ╭ [0]: usr/lib/libzstd.so.1 
│                                        ╰ [1]: usr/lib/libzstd.so.1.5.7 
╰ [1] ╭ Target  : Java 
      ├ Class   : lang-pkgs 
      ├ Type    : jar 
      ╰ Packages ╭ [0]  ╭ Name      : com.fasterxml.jackson.core:jackson-annotations 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-annotations@2.20 
                 │      │            ╰ UID : 8c51c23e51c8ef16 
                 │      ├ Version   : 2.20 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [1]  ╭ Name      : com.fasterxml.jackson.core:jackson-core 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-core@2.20.1 
                 │      │            ╰ UID : 9822b3547f110bc6 
                 │      ├ Version   : 2.20.1 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [2]  ╭ Name      : com.fasterxml.jackson.core:jackson-databind 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.fasterxml.jackson.core/jackson-databind@2.20.1 
                 │      │            ╰ UID : 4f8c9a471ff43465 
                 │      ├ Version   : 2.20.1 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [3]  ╭ Name      : com.fasterxml.jackson.dataformat:jackson-dataformat-toml 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.fasterxml.jackson.dataformat/jackson-dataformat-toml
                 │      │            │       @2.19.2 
                 │      │            ╰ UID : f187132d4296b98 
                 │      ├ Version   : 2.19.2 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [4]  ╭ Name      : com.github.mwiede:jsch 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.github.mwiede/jsch@2.27.7 
                 │      │            ╰ UID : 168f2be2e6ac4be5 
                 │      ├ Version   : 2.27.7 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [5]  ╭ Name      : com.github.vertical-blank:sql-formatter 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.github.vertical-blank/sql-formatter@2.0.5 
                 │      │            ╰ UID : 4aa6d74fa002054a 
                 │      ├ Version   : 2.0.5 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [6]  ╭ Name      : com.google.code.gson:gson 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.google.code.gson/gson@2.13.2 
                 │      │            ╰ UID : a60cbe5d2898b6fd 
                 │      ├ Version   : 2.13.2 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [7]  ╭ Name      : com.googlecode.juniversalchardet:juniversalchardet 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.googlecode.juniversalchardet/juniversalchardet@1.0.3 
                 │      │            ╰ UID : 59979d47f792d6c8 
                 │      ├ Version   : 1.0.3 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [8]  ╭ Name      : com.jcraft:jsch.agentproxy.connector-factory 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.connector-factory@0.0.9 
                 │      │            ╰ UID : c33f344564a099d2 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [9]  ╭ Name      : com.jcraft:jsch.agentproxy.core 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.core@0.0.9 
                 │      │            ╰ UID : 4be7fe5e595d9eb2 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [10] ╭ Name      : com.jcraft:jsch.agentproxy.jsch 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.jsch@0.0.9 
                 │      │            ╰ UID : 2c09ba989715b29 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [11] ╭ Name      : com.jcraft:jsch.agentproxy.pageant 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.pageant@0.0.9 
                 │      │            ╰ UID : 8affbecb98c67dc0 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [12] ╭ Name      : com.jcraft:jsch.agentproxy.sshagent 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.sshagent@0.0.9 
                 │      │            ╰ UID : 77f3ddb6f8158192 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [13] ╭ Name      : com.jcraft:jsch.agentproxy.svnkit-trilead-ssh2 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.svnkit-trilead-ssh2@0.0.9 
                 │      │            ╰ UID : dfc6f6319fc95cbe 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [14] ╭ Name      : com.jcraft:jsch.agentproxy.usocket-jna 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.usocket-jna@0.0.9 
                 │      │            ╰ UID : 80b49070dfd3f3a7 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [15] ╭ Name      : com.jcraft:jsch.agentproxy.usocket-nc 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.jcraft/jsch.agentproxy.usocket-nc@0.0.9 
                 │      │            ╰ UID : 8ce583c9bcf3a507 
                 │      ├ Version   : 0.0.9 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [16] ╭ Name      : com.sun.activation:javax.activation 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.sun.activation/javax.activation@1.2.0 
                 │      │            ╰ UID : 885b1754dac6edf 
                 │      ├ Version   : 1.2.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [17] ╭ Name      : com.sun.mail:javax.mail 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.sun.mail/javax.mail@1.6.2 
                 │      │            ╰ UID : eb67ca13361cdf7e 
                 │      ├ Version   : 1.6.2 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [18] ╭ Name      : com.warrenstrange:googleauth 
                 │      ├ Identifier ╭ PURL: pkg:maven/com.warrenstrange/googleauth@1.5.0 
                 │      │            ╰ UID : abdfc1ca334283c7 
                 │      ├ Version   : 1.5.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [19] ╭ Name      : commons-cli:commons-cli 
                 │      ├ Identifier ╭ PURL: pkg:maven/commons-cli/commons-cli@1.11.0 
                 │      │            ╰ UID : 7c850f7741b728f1 
                 │      ├ Version   : 1.11.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [20] ╭ Name      : commons-codec:commons-codec 
                 │      ├ Identifier ╭ PURL: pkg:maven/commons-codec/commons-codec@1.20.0 
                 │      │            ╰ UID : 36f72796c80a5f04 
                 │      ├ Version   : 1.20.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [21] ╭ Name      : commons-io:commons-io 
                 │      ├ Identifier ╭ PURL: pkg:maven/commons-io/commons-io@2.21.0 
                 │      │            ╰ UID : 4812ba05106027a5 
                 │      ├ Version   : 2.21.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [22] ╭ Name      : commons-logging:commons-logging 
                 │      ├ Identifier ╭ PURL: pkg:maven/commons-logging/commons-logging@1.3.5 
                 │      │            ╰ UID : 78410c5141b86fa 
                 │      ├ Version   : 1.3.5 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [23] ╭ Name      : commons-net:commons-net 
                 │      ├ Identifier ╭ PURL: pkg:maven/commons-net/commons-net@3.12.0 
                 │      │            ╰ UID : 1dfaef0fb0ac5d0b 
                 │      ├ Version   : 3.12.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [24] ╭ Name      : de.vandermeer:asciilist-j7 
                 │      ├ Identifier ╭ PURL: pkg:maven/de.vandermeer/asciilist-j7@1.0.0 
                 │      │            ╰ UID : d4e586b2e07acda4 
                 │      ├ Version   : 1.0.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [25] ╭ Name      : de.vandermeer:asciitable-j7 
                 │      ├ Identifier ╭ PURL: pkg:maven/de.vandermeer/asciitable-j7@1.0.1 
                 │      │            ╰ UID : 272a590ba643367f 
                 │      ├ Version   : 1.0.1 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [26] ╭ Name      : dnsjava:dnsjava 
                 │      ├ Identifier ╭ PURL: pkg:maven/dnsjava/dnsjava@3.6.3 
                 │      │            ╰ UID : 4b5e6e63b1733dfa 
                 │      ├ Version   : 3.6.3 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [27] ╭ Name      : io.jsonwebtoken:jjwt-api 
                 │      ├ Identifier ╭ PURL: pkg:maven/io.jsonwebtoken/jjwt-api@0.13.0 
                 │      │            ╰ UID : cdc3bc0a8b47e911 
                 │      ├ Version   : 0.13.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [28] ╭ Name      : io.jsonwebtoken:jjwt-gson 
                 │      ├ Identifier ╭ PURL: pkg:maven/io.jsonwebtoken/jjwt-gson@0.13.0 
                 │      │            ╰ UID : 9fc30d362e446fcd 
                 │      ├ Version   : 0.13.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [29] ╭ Name      : io.jsonwebtoken:jjwt-impl 
                 │      ├ Identifier ╭ PURL: pkg:maven/io.jsonwebtoken/jjwt-impl@0.13.0 
                 │      │            ╰ UID : d42e28c78bfe4cd6 
                 │      ├ Version   : 0.13.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [30] ╭ Name      : io.sigpipe:jbsdiff 
                 │      ├ Identifier ╭ PURL: pkg:maven/io.sigpipe/jbsdiff@1.0 
                 │      │            ╰ UID : 3ad9c9a90222e030 
                 │      ├ Version   : 1.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [31] ╭ Name      : jakarta.activation:jakarta.activation-api 
                 │      ├ Identifier ╭ PURL: pkg:maven/jakarta.activation/jakarta.activation-api@1.2.2 
                 │      │            ╰ UID : 84baa18824622446 
                 │      ├ Version   : 1.2.2 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [32] ╭ Name      : javax.xml.bind:jaxb-api 
                 │      ├ Identifier ╭ PURL: pkg:maven/javax.xml.bind/jaxb-api@2.3.1 
                 │      │            ╰ UID : 68f09018f4453b95 
                 │      ├ Version   : 2.3.1 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [33] ╭ Name      : jline:jline 
                 │      ├ Identifier ╭ PURL: pkg:maven/jline/jline@2.14.6 
                 │      │            ╰ UID : 6930774a112e73bc 
                 │      ├ Version   : 2.14.6 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [34] ╭ Name      : org.apache.commons:commons-collections4 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.apache.commons/commons-collections4@4.5.0 
                 │      │            ╰ UID : b6f26728bc972346 
                 │      ├ Version   : 4.5.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [35] ╭ Name      : org.apache.commons:commons-compress 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.apache.commons/commons-compress@1.28.0 
                 │      │            ╰ UID : 645d61b3c78fd14e 
                 │      ├ Version   : 1.28.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [36] ╭ Name      : org.apache.commons:commons-csv 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.apache.commons/commons-csv@1.14.1 
                 │      │            ╰ UID : fd28379ee7ee9be4 
                 │      ├ Version   : 1.14.1 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [37] ╭ Name      : org.apache.commons:commons-email 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.apache.commons/commons-email@1.6.0 
                 │      │            ╰ UID : 1cdb7e2822178209 
                 │      ├ Version   : 1.6.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [38] ╭ Name      : org.apache.commons:commons-lang3 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.apache.commons/commons-lang3@3.20.0 
                 │      │            ╰ UID : 2e779afc3ea0251d 
                 │      ├ Version   : 3.20.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [39] ╭ Name      : org.apache.commons:commons-math3 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.apache.commons/commons-math3@3.6.1 
                 │      │            ╰ UID : 3992f1c5b6195e89 
                 │      ├ Version   : 3.6.1 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [40] ╭ Name      : org.eclipse.jetty.compression:jetty-compression-common 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty.compression/jetty-compression-common@1
                 │      │            │       2.1.4 
                 │      │            ╰ UID : 98eb0f6a7b94cba2 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [41] ╭ Name      : org.eclipse.jetty.websocket:jetty-websocket-core-client 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty.websocket/jetty-websocket-core-client@
                 │      │            │       12.1.4 
                 │      │            ╰ UID : 4ac6a67496064613 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [42] ╭ Name      : org.eclipse.jetty.websocket:jetty-websocket-core-common 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty.websocket/jetty-websocket-core-common@
                 │      │            │       12.1.4 
                 │      │            ╰ UID : 92013e32518bb532 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [43] ╭ Name      : org.eclipse.jetty.websocket:jetty-websocket-jetty-api 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty.websocket/jetty-websocket-jetty-api@12
                 │      │            │       .1.4 
                 │      │            ╰ UID : 2fc6842321567d59 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [44] ╭ Name      : org.eclipse.jetty.websocket:jetty-websocket-jetty-client 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty.websocket/jetty-websocket-jetty-client
                 │      │            │       @12.1.4 
                 │      │            ╰ UID : c4d26c0eeba38988 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [45] ╭ Name      : org.eclipse.jetty.websocket:jetty-websocket-jetty-common 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty.websocket/jetty-websocket-jetty-common
                 │      │            │       @12.1.4 
                 │      │            ╰ UID : d85d2145de6f9fa2 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [46] ╭ Name      : org.eclipse.jetty:jetty-client 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty/jetty-client@12.1.3 
                 │      │            ╰ UID : 6f2abd14ed552ef5 
                 │      ├ Version   : 12.1.3 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [47] ╭ Name      : org.eclipse.jetty:jetty-http 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty/jetty-http@12.1.4 
                 │      │            ╰ UID : 2714f45b932050d8 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [48] ╭ Name      : org.eclipse.jetty:jetty-io 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty/jetty-io@12.1.3 
                 │      │            ╰ UID : 8c55ebadbdadfe4d 
                 │      ├ Version   : 12.1.3 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [49] ╭ Name      : org.eclipse.jetty:jetty-util 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.eclipse.jetty/jetty-util@12.1.4 
                 │      │            ╰ UID : 85f5538764077c02 
                 │      ├ Version   : 12.1.4 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [50] ╭ Name      : org.fusesource.hawtjni:hawtjni-runtime 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.hawtjni/hawtjni-runtime@1.17 
                 │      │            ╰ UID : 368c86360d5d2d6e 
                 │      ├ Version   : 1.17 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [51] ╭ Name      : org.fusesource.jansi:jansi 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi@1.18 
                 │      │            ╰ UID : 28003612621d63f7 
                 │      ├ Version   : 1.18 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [52] ╭ Name      : org.fusesource.jansi:jansi-freebsd32 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-freebsd32@1.8 
                 │      │            ╰ UID : 75689643540ac0cc 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [53] ╭ Name      : org.fusesource.jansi:jansi-freebsd64 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-freebsd64@1.8 
                 │      │            ╰ UID : cdf9cdca8706e16f 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [54] ╭ Name      : org.fusesource.jansi:jansi-linux32 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-linux32@1.8 
                 │      │            ╰ UID : 3d49c0eb4793e1f4 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [55] ╭ Name      : org.fusesource.jansi:jansi-linux64 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-linux64@1.8 
                 │      │            ╰ UID : 8b11f3d47b9658b2 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [56] ╭ Name      : org.fusesource.jansi:jansi-native 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-native@1.8 
                 │      │            ╰ UID : c89c538fba388aa2 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [57] ╭ Name      : org.fusesource.jansi:jansi-osx 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-osx@1.8 
                 │      │            ╰ UID : b0bc0de50b8059ad 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [58] ╭ Name      : org.fusesource.jansi:jansi-windows32 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-windows32@1.8 
                 │      │            ╰ UID : 7c1a51c801be878e 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [59] ╭ Name      : org.fusesource.jansi:jansi-windows64 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.fusesource.jansi/jansi-windows64@1.8 
                 │      │            ╰ UID : 6c10b179e44aabcb 
                 │      ├ Version   : 1.8 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [60] ╭ Name      : org.semver4j:semver4j 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.semver4j/semver4j@6.0.0 
                 │      │            ╰ UID : b4987f502c5eba1f 
                 │      ├ Version   : 6.0.0 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [61] ╭ Name      : org.slf4j:slf4j-api 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.slf4j/slf4j-api@2.0.17 
                 │      │            ╰ UID : 669ca5d81bb821ff 
                 │      ├ Version   : 2.0.17 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [62] ╭ Name      : org.slf4j:slf4j-nop 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.slf4j/slf4j-nop@2.0.17 
                 │      │            ╰ UID : 5e42b1280e39632b 
                 │      ├ Version   : 2.0.17 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ├ [63] ╭ Name      : org.snmp4j:snmp4j 
                 │      ├ Identifier ╭ PURL: pkg:maven/org.snmp4j/snmp4j@3.9.6 
                 │      │            ╰ UID : 9cf3d6b9898ef004 
                 │      ├ Version   : 3.9.6 
                 │      ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                 │      │            │         4a1b280 
                 │      │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                 │      │                      7a91d77 
                 │      ╰ FilePath  : openaf/openaf.jar 
                 ╰ [64] ╭ Name      : org.snmp4j:snmp4j-agent 
                        ├ Identifier ╭ PURL: pkg:maven/org.snmp4j/snmp4j-agent@3.8.2 
                        │            ╰ UID : 9ed630f1f75d1f9b 
                        ├ Version   : 3.8.2 
                        ├ Layer      ╭ Digest: sha256:a44e422ab615287a234e895ba05583a021647f92dd0f9911b68d14905
                        │            │         4a1b280 
                        │            ╰ DiffID: sha256:6a7ab8af953d5fdbff07e0fb2fbc8fffe84b0d610757cb3f35a37fbf8
                        │                      7a91d77 
                        ╰ FilePath  : openaf/openaf.jar 
````
