		Домашнее задание 4

1. Создаем виртуальную машину 

Создаем файл vagrant, копируем в него содержимое с методического пособия и запускаем vagrant up

```
user@ubuntu-vm:~/DZ-OTUS$ cd DZ-4
user@ubuntu-vm:~/DZ-OTUS/DZ-4$ touch vagrantfile
user@ubuntu-vm:~/DZ-OTUS/DZ-4$ nano vagrantfile
user@ubuntu-vm:~/DZ-OTUS/DZ-4$ vagrant up
==> vagrant: A new version of Vagrant is available: 2.3.6 (installed version: 2.3.4)!
==> vagrant: To upgrade visit: https://www.vagrantup.com/downloads.html

Bringing machine 'zfs' up with 'virtualbox' provider...
==> zfs: Importing base box 'centos/7'...
==> zfs: Matching MAC address for NAT networking...
==> zfs: Checking if box 'centos/7' version '2004.01' is up to date...
==> zfs: Setting the name of the VM: DZ-4_zfs_1684744903294_33170
==> zfs: Clearing any previously set network interfaces...
==> zfs: Preparing network interfaces based on configuration...
    zfs: Adapter 1: nat
==> zfs: Forwarding ports...
    zfs: 22 (guest) => 2222 (host) (adapter 1)
==> zfs: Running 'pre-boot' VM customizations...
==> zfs: Booting VM...
==> zfs: Waiting for machine to boot. This may take a few minutes...
    zfs: SSH address: 127.0.0.1:2222
    zfs: SSH username: vagrant
    zfs: SSH auth method: private key
    zfs:
    zfs: Vagrant insecure key detected. Vagrant will automatically replace
    zfs: this with a newly generated keypair for better security.
    zfs:
    zfs: Inserting generated public key within guest...
    zfs: Removing insecure key from the guest if it's present...
    zfs: Key inserted! Disconnecting and reconnecting using new SSH key...
==> zfs: Machine booted and ready!
==> zfs: Checking for guest additions in VM...
    zfs: No guest additions were detected on the base box for this VM! Guest
    zfs: additions are required for forwarded ports, shared folders, host only
    zfs: networking, and more. If SSH fails on this machine, please install
    zfs: the guest additions and repackage the box to continue.
    zfs:
    zfs: This is not an error message; everything may continue to work properly,
    zfs: in which case you may ignore this message.
==> zfs: Setting hostname...
==> zfs: Rsyncing folder: /home/user/DZ-OTUS/DZ-4/ => /vagrant
==> zfs: Running provisioner: shell...
    zfs: Running: inline script
    zfs: Loaded plugins: fastestmirror
    zfs: Examining /var/tmp/yum-root-23qJB8/zfs-release.el7_8.noarch.rpm: zfs-release-1-7.8.noarch
    zfs: Marking /var/tmp/yum-root-23qJB8/zfs-release.el7_8.noarch.rpm to be installed
    zfs: Resolving Dependencies
    zfs: --> Running transaction check
    zfs: ---> Package zfs-release.noarch 0:1-7.8 will be installed
    zfs: --> Finished Dependency Resolution
    zfs:
    zfs: Dependencies Resolved
    zfs:
    zfs: ================================================================================
    zfs:  Package          Arch        Version      Repository                      Size
    zfs: ================================================================================
    zfs: Installing:
    zfs:  zfs-release      noarch      1-7.8        /zfs-release.el7_8.noarch      2.9 k
    zfs:
    zfs: Transaction Summary
    zfs: ================================================================================
    zfs: Install  1 Package
    zfs:
    zfs: Total size: 2.9 k
    zfs: Installed size: 2.9 k
    zfs: Downloading packages:
    zfs: Running transaction check
    zfs: Running transaction test
    zfs: Transaction test succeeded
    zfs: Running transaction
    zfs:   Installing : zfs-release-1-7.8.noarch                                     1/1
    zfs:   Verifying  : zfs-release-1-7.8.noarch                                     1/1
    zfs:
    zfs: Installed:
    zfs:   zfs-release.noarch 0:1-7.8
    zfs:
    zfs: Complete!
    zfs: Loaded plugins: fastestmirror
    zfs: Determining fastest mirrors
    zfs:  * base: ftp.fau.de
    zfs:  * extras: artfiles.org
    zfs:  * updates: ftp.rz.uni-frankfurt.de
    zfs: Resolving Dependencies
    zfs: --> Running transaction check
    zfs: ---> Package epel-release.noarch 0:7-11 will be installed
    zfs: ---> Package kernel-devel.x86_64 0:3.10.0-1160.90.1.el7 will be installed
    zfs: --> Processing Dependency: perl for package: kernel-devel-3.10.0-1160.90.1.el7.x86_64
    zfs: ---> Package zfs.x86_64 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: zfs-kmod = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzpool2 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzfs2 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libuutil1 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libnvpair1 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: sysstat for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzpool.so.2()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzfs_core.so.1()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzfs.so.2()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libuutil.so.1()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libnvpair.so.1()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Running transaction check
    zfs: ---> Package libnvpair1.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libuutil1.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libzfs2.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libzpool2.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package perl.x86_64 4:5.16.3-299.el7_9 will be installed
    zfs: --> Processing Dependency: perl-libs = 4:5.16.3-299.el7_9 for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Socket) >= 1.3 for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Scalar::Util) >= 1.10 for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl-macros for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl-libs for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(threads::shared) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(threads) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(constant) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Time::Local) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Time::HiRes) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Storable) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Socket) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Scalar::Util) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Pod::Simple::XHTML) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Pod::Simple::Search) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Getopt::Long) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Filter::Util::Call) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(File::Temp) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(File::Spec::Unix) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(File::Spec::Functions) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(File::Spec) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(File::Path) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Exporter) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Cwd) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: perl(Carp) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: --> Processing Dependency: libperl.so()(64bit) for package: 4:perl-5.16.3-299.el7_9.x86_64
    zfs: ---> Package sysstat.x86_64 0:10.1.5-20.el7_9 will be installed
    zfs: --> Processing Dependency: libsensors.so.4()(64bit) for package: sysstat-10.1.5-20.el7_9.x86_64
    zfs: ---> Package zfs-dkms.noarch 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: dkms >= 2.2.0.3 for package: zfs-dkms-0.8.5-1.el7.noarch
    zfs: --> Processing Dependency: gcc for package: zfs-dkms-0.8.5-1.el7.noarch
    zfs: --> Running transaction check
    zfs: ---> Package gcc.x86_64 0:4.8.5-44.el7 will be installed
    zfs: --> Processing Dependency: libgomp = 4.8.5-44.el7 for package: gcc-4.8.5-44.el7.x86_64
    zfs: --> Processing Dependency: cpp = 4.8.5-44.el7 for package: gcc-4.8.5-44.el7.x86_64
    zfs: --> Processing Dependency: libgcc >= 4.8.5-44.el7 for package: gcc-4.8.5-44.el7.x86_64
    zfs: --> Processing Dependency: glibc-devel >= 2.2.90-12 for package: gcc-4.8.5-44.el7.x86_64
    zfs: --> Processing Dependency: libmpfr.so.4()(64bit) for package: gcc-4.8.5-44.el7.x86_64
    zfs: --> Processing Dependency: libmpc.so.3()(64bit) for package: gcc-4.8.5-44.el7.x86_64
    zfs: ---> Package lm_sensors-libs.x86_64 0:3.4.0-8.20160601gitf9185e5.el7 will be installed
    zfs: ---> Package perl-Carp.noarch 0:1.26-244.el7 will be installed
    zfs: ---> Package perl-Exporter.noarch 0:5.68-3.el7 will be installed
    zfs: ---> Package perl-File-Path.noarch 0:2.09-2.el7 will be installed
    zfs: ---> Package perl-File-Temp.noarch 0:0.23.01-3.el7 will be installed
    zfs: ---> Package perl-Filter.x86_64 0:1.49-3.el7 will be installed
    zfs: ---> Package perl-Getopt-Long.noarch 0:2.40-3.el7 will be installed
    zfs: --> Processing Dependency: perl(Pod::Usage) >= 1.14 for package: perl-Getopt-Long-2.40-3.el7.noarch
    zfs: --> Processing Dependency: perl(Text::ParseWords) for package: perl-Getopt-Long-2.40-3.el7.noarch
    zfs: ---> Package perl-PathTools.x86_64 0:3.40-5.el7 will be installed
    zfs: ---> Package perl-Pod-Simple.noarch 1:3.28-4.el7 will be installed
    zfs: --> Processing Dependency: perl(Pod::Escapes) >= 1.04 for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
    zfs: --> Processing Dependency: perl(Encode) for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
    zfs: ---> Package perl-Scalar-List-Utils.x86_64 0:1.27-248.el7 will be installed
    zfs: ---> Package perl-Socket.x86_64 0:2.010-5.el7 will be installed
    zfs: ---> Package perl-Storable.x86_64 0:2.45-3.el7 will be installed
    zfs: ---> Package perl-Time-HiRes.x86_64 4:1.9725-3.el7 will be installed
    zfs: ---> Package perl-Time-Local.noarch 0:1.2300-2.el7 will be installed
    zfs: ---> Package perl-constant.noarch 0:1.27-2.el7 will be installed
    zfs: ---> Package perl-libs.x86_64 4:5.16.3-299.el7_9 will be installed
    zfs: ---> Package perl-macros.x86_64 4:5.16.3-299.el7_9 will be installed
    zfs: ---> Package perl-threads.x86_64 0:1.87-4.el7 will be installed
    zfs: ---> Package perl-threads-shared.x86_64 0:1.43-6.el7 will be installed
    zfs: ---> Package zfs-dkms.noarch 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: dkms >= 2.2.0.3 for package: zfs-dkms-0.8.5-1.el7.noarch
    zfs: --> Running transaction check
    zfs: ---> Package cpp.x86_64 0:4.8.5-44.el7 will be installed
    zfs: ---> Package glibc-devel.x86_64 0:2.17-326.el7_9 will be installed
    zfs: --> Processing Dependency: glibc-headers = 2.17-326.el7_9 for package: glibc-devel-2.17-326.el7_9.x86_64
    zfs: --> Processing Dependency: glibc = 2.17-326.el7_9 for package: glibc-devel-2.17-326.el7_9.x86_64
    zfs: --> Processing Dependency: glibc-headers for package: glibc-devel-2.17-326.el7_9.x86_64
    zfs: ---> Package libgcc.x86_64 0:4.8.5-39.el7 will be updated
    zfs: ---> Package libgcc.x86_64 0:4.8.5-44.el7 will be an update
    zfs: ---> Package libgomp.x86_64 0:4.8.5-39.el7 will be updated
    zfs: ---> Package libgomp.x86_64 0:4.8.5-44.el7 will be an update
    zfs: ---> Package libmpc.x86_64 0:1.0.1-3.el7 will be installed
    zfs: ---> Package mpfr.x86_64 0:3.1.1-4.el7 will be installed
    zfs: ---> Package perl-Encode.x86_64 0:2.51-7.el7 will be installed
    zfs: ---> Package perl-Pod-Escapes.noarch 1:1.04-299.el7_9 will be installed
    zfs: ---> Package perl-Pod-Usage.noarch 0:1.63-3.el7 will be installed
    zfs: --> Processing Dependency: perl(Pod::Text) >= 3.15 for package: perl-Pod-Usage-1.63-3.el7.noarch
    zfs: --> Processing Dependency: perl-Pod-Perldoc for package: perl-Pod-Usage-1.63-3.el7.noarch
    zfs: ---> Package perl-Text-ParseWords.noarch 0:3.29-4.el7 will be installed
    zfs: ---> Package zfs-dkms.noarch 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: dkms >= 2.2.0.3 for package: zfs-dkms-0.8.5-1.el7.noarch
    zfs: --> Running transaction check
    zfs: ---> Package glibc.x86_64 0:2.17-307.el7.1 will be updated
    zfs: --> Processing Dependency: glibc = 2.17-307.el7.1 for package: glibc-common-2.17-307.el7.1.x86_64
    zfs: ---> Package glibc.x86_64 0:2.17-326.el7_9 will be an update
    zfs: ---> Package glibc-headers.x86_64 0:2.17-326.el7_9 will be installed
    zfs: --> Processing Dependency: kernel-headers >= 2.2.1 for package: glibc-headers-2.17-326.el7_9.x86_64
    zfs: --> Processing Dependency: kernel-headers for package: glibc-headers-2.17-326.el7_9.x86_64
    zfs: ---> Package perl-Pod-Perldoc.noarch 0:3.20-4.el7 will be installed
    zfs: --> Processing Dependency: perl(parent) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
    zfs: --> Processing Dependency: perl(HTTP::Tiny) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
    zfs: ---> Package perl-podlators.noarch 0:2.5.1-3.el7 will be installed
    zfs: ---> Package zfs-dkms.noarch 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: dkms >= 2.2.0.3 for package: zfs-dkms-0.8.5-1.el7.noarch
    zfs: --> Running transaction check
    zfs: ---> Package glibc-common.x86_64 0:2.17-307.el7.1 will be updated
    zfs: ---> Package glibc-common.x86_64 0:2.17-326.el7_9 will be an update
    zfs: ---> Package kernel-headers.x86_64 0:3.10.0-1160.90.1.el7 will be installed
    zfs: ---> Package perl-HTTP-Tiny.noarch 0:0.033-3.el7 will be installed
    zfs: ---> Package perl-parent.noarch 1:0.225-244.el7 will be installed
    zfs: ---> Package zfs-dkms.noarch 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: dkms >= 2.2.0.3 for package: zfs-dkms-0.8.5-1.el7.noarch
    zfs: --> Finished Dependency Resolution
    zfs:  You could try using --skip-broken to work around the problem
    zfs: Error: Package: zfs-dkms-0.8.5-1.el7.noarch (zfs)
    zfs:            Requires: dkms >= 2.2.0.3
    zfs:  You could try running: rpm -Va --nofiles --nodigest
    zfs: Loaded plugins: fastestmirror
    zfs: ================================== repo: zfs ===================================
    zfs: [zfs]
    zfs: async = True
    zfs: bandwidth = 0
    zfs: base_persistdir = /var/lib/yum/repos/x86_64/7
    zfs: baseurl = http://download.zfsonlinux.org/epel/7.8/x86_64/
    zfs: cache = 0
    zfs: cachedir = /var/cache/yum/x86_64/7/zfs
    zfs: check_config_file_age = True
    zfs: compare_providers_priority = 80
    zfs: cost = 1000
    zfs: deltarpm_metadata_percentage = 100
    zfs: deltarpm_percentage =
    zfs: enabled = 0
    zfs: enablegroups = True
    zfs: exclude =
    zfs: failovermethod = priority
    zfs: ftp_disable_epsv = False
    zfs: gpgcadir = /var/lib/yum/repos/x86_64/7/zfs/gpgcadir
    zfs: gpgcakey =
    zfs: gpgcheck = True
    zfs: gpgdir = /var/lib/yum/repos/x86_64/7/zfs/gpgdir
    zfs: gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-zfsonlinux
    zfs: hdrdir = /var/cache/yum/x86_64/7/zfs/headers
    zfs: http_caching = all
    zfs: includepkgs =
    zfs: ip_resolve =
    zfs: keepalive = True
    zfs: keepcache = False
    zfs: mddownloadpolicy = sqlite
    zfs: mdpolicy = group:small
    zfs: mediaid =
    zfs: metadata_expire = 604800
    zfs: metadata_expire_filter = read-only:present
    zfs: metalink =
    zfs: minrate = 0
    zfs: mirrorlist =
    zfs: mirrorlist_expire = 86400
    zfs: name = ZFS on Linux for EL7 - dkms
    zfs: old_base_cache_dir =
    zfs: password =
    zfs: persistdir = /var/lib/yum/repos/x86_64/7/zfs
    zfs: pkgdir = /var/cache/yum/x86_64/7/zfs/packages
    zfs: proxy = False
    zfs: proxy_dict =
    zfs: proxy_password =
    zfs: proxy_username =
    zfs: repo_gpgcheck = False
    zfs: retries = 10
    zfs: skip_if_unavailable = False
    zfs: ssl_check_cert_permissions = True
    zfs: sslcacert =
    zfs: sslclientcert =
    zfs: sslclientkey =
    zfs: sslverify = True
    zfs: throttle = 0
    zfs: timeout = 30.0
    zfs: ui_id = zfs/x86_64
    zfs: ui_repoid_vars = releasever,
    zfs:    basearch
    zfs: username =
    zfs:
    zfs: Loaded plugins: fastestmirror
    zfs: ================================ repo: zfs-kmod ================================
    zfs: [zfs-kmod]
    zfs: async = True
    zfs: bandwidth = 0
    zfs: base_persistdir = /var/lib/yum/repos/x86_64/7
    zfs: baseurl = http://download.zfsonlinux.org/epel/7.8/kmod/x86_64/
    zfs: cache = 0
    zfs: cachedir = /var/cache/yum/x86_64/7/zfs-kmod
    zfs: check_config_file_age = True
    zfs: compare_providers_priority = 80
    zfs: cost = 1000
    zfs: deltarpm_metadata_percentage = 100
    zfs: deltarpm_percentage =
    zfs: enabled = 1
    zfs: enablegroups = True
    zfs: exclude =
    zfs: failovermethod = priority
    zfs: ftp_disable_epsv = False
    zfs: gpgcadir = /var/lib/yum/repos/x86_64/7/zfs-kmod/gpgcadir
    zfs: gpgcakey =
    zfs: gpgcheck = True
    zfs: gpgdir = /var/lib/yum/repos/x86_64/7/zfs-kmod/gpgdir
    zfs: gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-zfsonlinux
    zfs: hdrdir = /var/cache/yum/x86_64/7/zfs-kmod/headers
    zfs: http_caching = all
    zfs: includepkgs =
    zfs: ip_resolve =
    zfs: keepalive = True
    zfs: keepcache = False
    zfs: mddownloadpolicy = sqlite
    zfs: mdpolicy = group:small
    zfs: mediaid =
    zfs: metadata_expire = 604800
    zfs: metadata_expire_filter = read-only:present
    zfs: metalink =
    zfs: minrate = 0
    zfs: mirrorlist =
    zfs: mirrorlist_expire = 86400
    zfs: name = ZFS on Linux for EL7 - kmod
    zfs: old_base_cache_dir =
    zfs: password =
    zfs: persistdir = /var/lib/yum/repos/x86_64/7/zfs-kmod
    zfs: pkgdir = /var/cache/yum/x86_64/7/zfs-kmod/packages
    zfs: proxy = False
    zfs: proxy_dict =
    zfs: proxy_password =
    zfs: proxy_username =
    zfs: repo_gpgcheck = False
    zfs: retries = 10
    zfs: skip_if_unavailable = False
    zfs: ssl_check_cert_permissions = True
    zfs: sslcacert =
    zfs: sslclientcert =
    zfs: sslclientkey =
    zfs: sslverify = True
    zfs: throttle = 0
    zfs: timeout = 30.0
    zfs: ui_id = zfs-kmod/x86_64
    zfs: ui_repoid_vars = releasever,
    zfs:    basearch
    zfs: username =
    zfs:
    zfs: Loaded plugins: fastestmirror
    zfs: Loading mirror speeds from cached hostfile
    zfs:  * base: ftp.fau.de
    zfs:  * extras: artfiles.org
    zfs:  * updates: ftp.rz.uni-frankfurt.de
    zfs: Resolving Dependencies
    zfs: --> Running transaction check
    zfs: ---> Package zfs.x86_64 0:0.8.5-1.el7 will be installed
    zfs: --> Processing Dependency: zfs-kmod = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzpool2 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzfs2 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libuutil1 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libnvpair1 = 0.8.5 for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: sysstat for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzpool.so.2()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzfs_core.so.1()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libzfs.so.2()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libuutil.so.1()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Processing Dependency: libnvpair.so.1()(64bit) for package: zfs-0.8.5-1.el7.x86_64
    zfs: --> Running transaction check
    zfs: ---> Package kmod-zfs.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libnvpair1.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libuutil1.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libzfs2.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package libzpool2.x86_64 0:0.8.5-1.el7 will be installed
    zfs: ---> Package sysstat.x86_64 0:10.1.5-20.el7_9 will be installed
    zfs: --> Processing Dependency: libsensors.so.4()(64bit) for package: sysstat-10.1.5-20.el7_9.x86_64
    zfs: --> Running transaction check
    zfs: ---> Package lm_sensors-libs.x86_64 0:3.4.0-8.20160601gitf9185e5.el7 will be installed
    zfs: --> Finished Dependency Resolution
    zfs:
    zfs: Dependencies Resolved
    zfs:
    zfs: ================================================================================
    zfs:  Package           Arch     Version                            Repository  Size
    zfs: ================================================================================
    zfs: Installing:
    zfs:  zfs               x86_64   0.8.5-1.el7                        zfs-kmod   486 k
    zfs: Installing for dependencies:
    zfs:  kmod-zfs          x86_64   0.8.5-1.el7                        zfs-kmod   1.1 M
    zfs:  libnvpair1        x86_64   0.8.5-1.el7                        zfs-kmod    32 k
    zfs:  libuutil1         x86_64   0.8.5-1.el7                        zfs-kmod    26 k
    zfs:  libzfs2           x86_64   0.8.5-1.el7                        zfs-kmod   208 k
    zfs:  libzpool2         x86_64   0.8.5-1.el7                        zfs-kmod   861 k
    zfs:  lm_sensors-libs   x86_64   3.4.0-8.20160601gitf9185e5.el7     base        42 k
    zfs:  sysstat           x86_64   10.1.5-20.el7_9                    updates    315 k
    zfs:
    zfs: Transaction Summary
    zfs: ================================================================================
    zfs: Install  1 Package (+7 Dependent packages)
    zfs:
    zfs: Total download size: 3.0 M
    zfs: Installed size: 11 M
    zfs: Downloading packages:
    zfs: Public key for lm_sensors-libs-3.4.0-8.20160601gitf9185e5.el7.x86_64.rpm is not installed
    zfs: warning: /var/cache/yum/x86_64/7/base/packages/lm_sensors-libs-3.4.0-8.20160601gitf9185e5.el7.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID f4a80eb5: NOKEY
    zfs: Public key for sysstat-10.1.5-20.el7_9.x86_64.rpm is not installed
    zfs: --------------------------------------------------------------------------------
    zfs: Total                                              1.1 MB/s | 3.0 MB  00:02
    zfs: Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    zfs: Importing GPG key 0xF4A80EB5:
    zfs:  Userid     : "CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>"
    zfs:  Fingerprint: 6341 ab27 53d7 8a78 a7c2 7bb1 24c6 a8a7 f4a8 0eb5
    zfs:  Package    : centos-release-7-8.2003.0.el7.centos.x86_64 (@anaconda)
    zfs:  From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    zfs: Running transaction check
    zfs: Running transaction test
    zfs: Transaction test succeeded
    zfs: Running transaction
    zfs:   Installing : libnvpair1-0.8.5-1.el7.x86_64                                1/8
    zfs:   Installing : libuutil1-0.8.5-1.el7.x86_64                                 2/8
    zfs:   Installing : libzfs2-0.8.5-1.el7.x86_64                                   3/8
    zfs:   Installing : libzpool2-0.8.5-1.el7.x86_64                                 4/8
    zfs:   Installing : lm_sensors-libs-3.4.0-8.20160601gitf9185e5.el7.x86_64        5/8
    zfs:   Installing : sysstat-10.1.5-20.el7_9.x86_64                               6/8
    zfs:   Installing : kmod-zfs-0.8.5-1.el7.x86_64                                  7/8
    zfs:   Installing : zfs-0.8.5-1.el7.x86_64                                       8/8
    zfs:   Verifying  : libuutil1-0.8.5-1.el7.x86_64                                 1/8
    zfs:   Verifying  : libzfs2-0.8.5-1.el7.x86_64                                   2/8
    zfs:   Verifying  : zfs-0.8.5-1.el7.x86_64                                       3/8
    zfs:   Verifying  : sysstat-10.1.5-20.el7_9.x86_64                               4/8
    zfs:   Verifying  : kmod-zfs-0.8.5-1.el7.x86_64                                  5/8
    zfs:   Verifying  : libnvpair1-0.8.5-1.el7.x86_64                                6/8
    zfs:   Verifying  : lm_sensors-libs-3.4.0-8.20160601gitf9185e5.el7.x86_64        7/8
    zfs:   Verifying  : libzpool2-0.8.5-1.el7.x86_64                                 8/8
    zfs:
    zfs: Installed:
    zfs:   zfs.x86_64 0:0.8.5-1.el7
    zfs:
    zfs: Dependency Installed:
    zfs:   kmod-zfs.x86_64 0:0.8.5-1.el7
    zfs:   libnvpair1.x86_64 0:0.8.5-1.el7
    zfs:   libuutil1.x86_64 0:0.8.5-1.el7
    zfs:   libzfs2.x86_64 0:0.8.5-1.el7
    zfs:   libzpool2.x86_64 0:0.8.5-1.el7
    zfs:   lm_sensors-libs.x86_64 0:3.4.0-8.20160601gitf9185e5.el7
    zfs:   sysstat.x86_64 0:10.1.5-20.el7_9
    zfs:
    zfs: Complete!
    zfs: Loaded plugins: fastestmirror
    zfs: Loading mirror speeds from cached hostfile
    zfs:  * base: ftp.fau.de
    zfs:  * extras: artfiles.org
    zfs:  * updates: ftp.rz.uni-frankfurt.de
    zfs: Resolving Dependencies
    zfs: --> Running transaction check
    zfs: ---> Package wget.x86_64 0:1.14-18.el7_6.1 will be installed
    zfs: --> Finished Dependency Resolution
    zfs:
    zfs: Dependencies Resolved
    zfs:
    zfs: ================================================================================
    zfs:  Package        Arch             Version                   Repository      Size
    zfs: ================================================================================
    zfs: Installing:
    zfs:  wget           x86_64           1.14-18.el7_6.1           base           547 k
    zfs:
    zfs: Transaction Summary
    zfs: ================================================================================
    zfs: Install  1 Package
    zfs:
    zfs: Total download size: 547 k
    zfs: Installed size: 2.0 M
    zfs: Downloading packages:
    zfs: Running transaction check
    zfs: Running transaction test
    zfs: Transaction test succeeded
    zfs: Running transaction
    zfs:   Installing : wget-1.14-18.el7_6.1.x86_64                                  1/1
    zfs:   Verifying  : wget-1.14-18.el7_6.1.x86_64                                  1/1
    zfs:
    zfs: Installed:
    zfs:   wget.x86_64 0:1.14-18.el7_6.1
    zfs:
    zfs: Complete!

```

2. Подключаемся к нашей машине, и переходим в root пользователя

```
user@ubuntu-vm:~/DZ-OTUS/DZ-4$ vagrant ssh
[vagrant@zfs ~]$
[vagrant@zfs ~]$ sudo -i
[root@zfs ~]#

```

3. Смотрим список всех дисков, которые есть в виртуальной машине: lsblk

```

[root@zfs ~]# lsblk
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda      8:0    0   40G  0 disk
`-sda1   8:1    0   40G  0 part /
sdb      8:16   0  512M  0 disk
sdc      8:32   0  512M  0 disk
sdd      8:48   0  512M  0 disk
sde      8:64   0  512M  0 disk
sdf      8:80   0  512M  0 disk
sdg      8:96   0  512M  0 disk
sdh      8:112  0  512M  0 disk
sdi      8:128  0  512M  0 disk

```

4. Создаём пул из двух дисков в режиме RAID 1, cоздадим ещё 3 пула:

```

[root@zfs ~]# zpool create otus1 mirror /dev/sdb /dev/sdc
[root@zfs ~]# zpool create otus2 mirror /dev/sdd /dev/sde
[root@zfs ~]# zpool create otus3 mirror /dev/sdf /dev/sdg
[root@zfs ~]# zpool create otus4 mirror /dev/sdh /dev/sdi

```

5. Смотрим информацию о пулах: zpool list

```

[root@zfs ~]# zpool list
NAME    SIZE  ALLOC   FREE  CKPOINT  EXPANDSZ   FRAG    CAP  DEDUP    HEALTH  ALTROOT
otus1   480M  91.5K   480M        -         -     0%     0%  1.00x    ONLINE  -
otus2   480M  91.5K   480M        -         -     0%     0%  1.00x    ONLINE  -
otus3   480M  91.5K   480M        -         -     0%     0%  1.00x    ONLINE  -
otus4   480M  91.5K   480M        -         -     0%     0%  1.00x    ONLINE  -

```

6. Добавим разные алгоритмы сжатия в каждую файловую систему:

```

[root@zfs ~]# zfs set compression=lzjb otus1
[root@zfs ~]# zfs set compression=lz4 otus2
[root@zfs ~]# zfs set compression=gzip-9 otus3
[root@zfs ~]# zfs set compression=zle otus4

```

7. Проверим, что все файловые системы имеют разные методы сжатия:

```

[root@zfs ~]# zfs get all | grep compression
otus1  compression           lzjb                   local
otus2  compression           lz4                    local
otus3  compression           gzip-9                 local
otus4  compression           zle                    local

```

8. Скачаем один и тот же текстовый файл во все пулы:

```

[root@zfs ~]# for i in {1..4}; do wget -P /otus$i https://gutenberg.org/cache/epub/2600/pg2600.converter.log; done
--2023-05-22 09:01:31--  https://gutenberg.org/cache/epub/2600/pg2600.converter.log
Resolving gutenberg.org (gutenberg.org)... 152.19.134.47, 2610:28:3090:3000:0:bad:cafe:47
Connecting to gutenberg.org (gutenberg.org)|152.19.134.47|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 40931771 (39M) [text/plain]
Saving to: '/otus1/pg2600.converter.log'

100%[======================================================================>] 40,931,771  2.85MB/s   in 20s

2023-05-22 09:01:53 (1.91 MB/s) - '/otus1/pg2600.converter.log' saved [40931771/40931771]

--2023-05-22 09:01:53--  https://gutenberg.org/cache/epub/2600/pg2600.converter.log
Resolving gutenberg.org (gutenberg.org)... 152.19.134.47, 2610:28:3090:3000:0:bad:cafe:47
Connecting to gutenberg.org (gutenberg.org)|152.19.134.47|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 40931771 (39M) [text/plain]
Saving to: '/otus2/pg2600.converter.log'

100%[======================================================================>] 40,931,771  3.83MB/s   in 20s

2023-05-22 09:02:13 (2.00 MB/s) - '/otus2/pg2600.converter.log' saved [40931771/40931771]

--2023-05-22 09:02:13--  https://gutenberg.org/cache/epub/2600/pg2600.converter.log
Resolving gutenberg.org (gutenberg.org)... 152.19.134.47, 2610:28:3090:3000:0:bad:cafe:47
Connecting to gutenberg.org (gutenberg.org)|152.19.134.47|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 40931771 (39M) [text/plain]
Saving to: '/otus3/pg2600.converter.log'

100%[======================================================================>] 40,931,771  1.12MB/s   in 40s

2023-05-22 09:02:53 (1011 KB/s) - '/otus3/pg2600.converter.log' saved [40931771/40931771]

--2023-05-22 09:02:53--  https://gutenberg.org/cache/epub/2600/pg2600.converter.log
Resolving gutenberg.org (gutenberg.org)... 152.19.134.47, 2610:28:3090:3000:0:bad:cafe:47
Connecting to gutenberg.org (gutenberg.org)|152.19.134.47|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 40931771 (39M) [text/plain]
Saving to: '/otus4/pg2600.converter.log'

100%[======================================================================>] 40,931,771  2.86MB/s   in 19s

2023-05-22 09:03:12 (2.07 MB/s) - '/otus4/pg2600.converter.log' saved [40931771/40931771]

```

9. Проверим, что файл был скачан во все пулы:

```

[root@zfs ~]# ls -l /otus*
/otus1:
total 22048
-rw-r--r--. 1 root root 40931771 May  2 08:18 pg2600.converter.log

/otus2:
total 17985
-rw-r--r--. 1 root root 40931771 May  2 08:18 pg2600.converter.log

/otus3:
total 10955
-rw-r--r--. 1 root root 40931771 May  2 08:18 pg2600.converter.log

/otus4:
total 40000
-rw-r--r--. 1 root root 40931771 May  2 08:18 pg2600.converter.log

```

10. Проверим, сколько места занимает один и тот же файл в разных пулах и проверим степень сжатия файлов:

```

[root@zfs ~]# zfs list
NAME    USED  AVAIL     REFER  MOUNTPOINT
otus1  21.6M   330M     21.6M  /otus1
otus2  17.7M   334M     17.6M  /otus2
otus3  10.8M   341M     10.7M  /otus3
otus4  39.2M   313M     39.1M  /otus4

[root@zfs ~]# zfs get all | grep compressratio | grep -v ref
otus1  compressratio         1.81x                  -
otus2  compressratio         2.22x                  -
otus3  compressratio         3.65x                  -
otus4  compressratio         1.00x                  -

```

11. Определение настроек пула. Скачиваем архив в домашний каталог:

```

[root@zfs ~]# curl -L 'https://drive.google.com/uc?export=download&id=1KRBNW33QWqbvbVHa3hLJivOAt60yukkg&confirm=t' > archive.tar.gz
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:--  0:00:07 --:--:--     0
100 7104k  100 7104k    0     0   794k      0  0:00:08  0:00:08 --:--:-- 5620k
[root@zfs ~]#
[root@zfs ~]#
[root@zfs ~]# ls -llh
total 7.0M
-rw-------. 1 root root 5.5K Apr 30  2020 anaconda-ks.cfg
-rw-r--r--. 1 root root 7.0M May 22 14:11 archive.tar.gz
-rw-------. 1 root root 5.2K Apr 30  2020 original-ks.cfg

```

12. Разархивируем архив

```
[root@zfs ~]# tar -xzvf archive.tar.gz
zpoolexport/
zpoolexport/filea
zpoolexport/fileb
[root@zfs ~]#

```

13. Проверим, возможно ли импортировать данный каталог в пул:

```

[root@zfs ~]# zpool import -d zpoolexport/
   pool: otus
     id: 6554193320433390805
  state: ONLINE
 action: The pool can be imported using its name or numeric identifier.
 config:

        otus                         ONLINE
          mirror-0                   ONLINE
            /root/zpoolexport/filea  ONLINE
            /root/zpoolexport/fileb  ONLINE
[root@zfs ~]#

```

14. Сделаем импорт данного пула к нам в ОС:

```

[root@zfs ~]# zpool import -d zpoolexport/ otus
[root@zfs ~]#
[root@zfs ~]# zpool status
  pool: otus
 state: ONLINE
  scan: none requested
config:

        NAME                         STATE     READ WRITE CKSUM
        otus                         ONLINE       0     0     0
          mirror-0                   ONLINE       0     0     0
            /root/zpoolexport/filea  ONLINE       0     0     0
            /root/zpoolexport/fileb  ONLINE       0     0     0

errors: No known data errors

  pool: otus1
 state: ONLINE
  scan: none requested
config:

        NAME        STATE     READ WRITE CKSUM
        otus1       ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            sdb     ONLINE       0     0     0
            sdc     ONLINE       0     0     0

errors: No known data errors

  pool: otus2
 state: ONLINE
  scan: none requested
config:

        NAME        STATE     READ WRITE CKSUM
        otus2       ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            sdd     ONLINE       0     0     0
            sde     ONLINE       0     0     0

errors: No known data errors

  pool: otus3
 state: ONLINE
  scan: none requested
config:

        NAME        STATE     READ WRITE CKSUM
        otus3       ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            sdf     ONLINE       0     0     0
            sdg     ONLINE       0     0     0

errors: No known data errors

  pool: otus4
 state: ONLINE
  scan: none requested
config:

        NAME        STATE     READ WRITE CKSUM
        otus4       ONLINE       0     0     0
          mirror-0  ONLINE       0     0     0
            sdh     ONLINE       0     0     0
            sdi     ONLINE       0     0     0

errors: No known data errors

```

15. Далее нам нужно определить настройки. Запрос сразу всех параметром файловой системы: zfs get all otus

```

[root@zfs ~]#  zpool get all otus
NAME  PROPERTY                       VALUE                          SOURCE
otus  size                           480M                           -
otus  capacity                       0%                             -
otus  altroot                        -                              default
otus  health                         ONLINE                         -
otus  guid                           6554193320433390805            -
otus  version                        -                              default
otus  bootfs                         -                              default
otus  delegation                     on                             default
otus  autoreplace                    off                            default
otus  cachefile                      -                              default
otus  failmode                       wait                           default
otus  listsnapshots                  off                            default
otus  autoexpand                     off                            default
otus  dedupditto                     0                              default
otus  dedupratio                     1.00x                          -
otus  free                           478M                           -
otus  allocated                      2.09M                          -
otus  readonly                       off                            -
otus  ashift                         0                              default
otus  comment                        -                              default
otus  expandsize                     -                              -
otus  freeing                        0                              -
otus  fragmentation                  0%                             -
otus  leaked                         0                              -
otus  multihost                      off                            default
otus  checkpoint                     -                              -
otus  load_guid                      16047893165903334621           -
otus  autotrim                       off                            default
otus  feature@async_destroy          enabled                        local
otus  feature@empty_bpobj            active                         local
otus  feature@lz4_compress           active                         local
otus  feature@multi_vdev_crash_dump  enabled                        local
otus  feature@spacemap_histogram     active                         local
otus  feature@enabled_txg            active                         local
otus  feature@hole_birth             active                         local
otus  feature@extensible_dataset     active                         local
otus  feature@embedded_data          active                         local
otus  feature@bookmarks              enabled                        local
otus  feature@filesystem_limits      enabled                        local
otus  feature@large_blocks           enabled                        local
otus  feature@large_dnode            enabled                        local
otus  feature@sha512                 enabled                        local
otus  feature@skein                  enabled                        local
otus  feature@edonr                  enabled                        local
otus  feature@userobj_accounting     active                         local
otus  feature@encryption             enabled                        local
otus  feature@project_quota          active                         local
otus  feature@device_removal         enabled                        local
otus  feature@obsolete_counts        enabled                        local
otus  feature@zpool_checkpoint       enabled                        local
otus  feature@spacemap_v2            active                         local
otus  feature@allocation_classes     enabled                        local
otus  feature@resilver_defer         enabled                        local
otus  feature@bookmark_v2            enabled                        local

```

15. C помощью команды grep можно уточнить конкретный параметр

```

[root@zfs ~]# zfs get available otus
NAME  PROPERTY   VALUE  SOURCE
otus  available  350M   -

[root@zfs ~]# zfs get readonly otus
NAME  PROPERTY  VALUE   SOURCE
otus  readonly  off     default

[root@zfs ~]# zfs get recordsize otus
NAME  PROPERTY    VALUE    SOURCE
otus  recordsize  128K     local

[root@zfs ~]# zfs get compression otus
NAME  PROPERTY     VALUE     SOURCE
otus  compression  zle       local

[root@zfs ~]# zfs get checksum otus
NAME  PROPERTY  VALUE      SOURCE
otus  checksum  sha256     local


```

16. Работа со снапшотом, поиск сообщения от преподавателя. Скачаем файл, указанный в задании

```

[root@zfs ~]# wget -O otus_task2.file --no-check-certificate "https://drive.google.com/u/0/uc?id=1gH8gCL9y7Nd5Ti3IRmplZPF1XjzxeRAG&export=download"
--2023-05-22 14:33:29--  https://drive.google.com/u/0/uc?id=1gH8gCL9y7Nd5Ti3IRmplZPF1XjzxeRAG&export=download
Resolving drive.google.com (drive.google.com)... 209.85.233.194, 2a00:1450:4010:c0b::c2
Connecting to drive.google.com (drive.google.com)|209.85.233.194|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://drive.google.com/uc?id=1gH8gCL9y7Nd5Ti3IRmplZPF1XjzxeRAG&export=download [following]
--2023-05-22 14:33:29--  https://drive.google.com/uc?id=1gH8gCL9y7Nd5Ti3IRmplZPF1XjzxeRAG&export=download
Reusing existing connection to drive.google.com:443.
HTTP request sent, awaiting response... 303 See Other
Location: https://doc-00-bo-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/p1rd137bmhuknkf58inju3bgkl8vhkvm/1684765950000/16189157874053420687/*/1gH8gCL9y7Nd5Ti3IRmplZPF1XjzxeRAG?e=download&uuid=af38b9a7-4729-4747-b0fc-45f4738836d9 [following]
Warning: wildcards not supported in HTTP.
--2023-05-22 14:33:33--  https://doc-00-bo-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/p1rd137bmhuknkf58inju3bgkl8vhkvm/1684765950000/16189157874053420687/*/1gH8gCL9y7Nd5Ti3IRmplZPF1XjzxeRAG?e=download&uuid=af38b9a7-4729-4747-b0fc-45f4738836d9
Resolving doc-00-bo-docs.googleusercontent.com (doc-00-bo-docs.googleusercontent.com)... 64.233.165.132, 2a00:1450:4010:c08::84
Connecting to doc-00-bo-docs.googleusercontent.com (doc-00-bo-docs.googleusercontent.com)|64.233.165.132|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 5432736 (5.2M) [application/octet-stream]
Saving to: 'otus_task2.file'

100%[======================================================================>] 5,432,736   4.93MB/s   in 1.1s

2023-05-22 14:33:35 (4.93 MB/s) - 'otus_task2.file' saved [5432736/5432736]

[root@zfs ~]#
[root@zfs ~]#
[root@zfs ~]#
[root@zfs ~]#
[root@zfs ~]# ls -llh
total 13M
-rw-------. 1 root root 5.5K Apr 30  2020 anaconda-ks.cfg
-rw-r--r--. 1 root root 7.0M May 22 14:11 archive.tar.gz
-rw-------. 1 root root 5.2K Apr 30  2020 original-ks.cfg
-rw-r--r--. 1 root root 5.2M May 22 14:33 otus_task2.file
drwxr-xr-x. 2 root root   32 May 15  2020 zpoolexport

```

17. Восстановим файловую систему из снапшота

```

[root@zfs ~]# zfs receive otus/test@today < otus_task2.file

```

18. Далее, ищем в каталоге /otus/test файл с именем “secret_message”

```

[root@zfs /]#  find /otus/test -name "secret_message"
/otus/test/task1/file_mess/secret_message

```

19. Смотрим содержимое найденного файла:

```
[root@zfs /]# cat /otus/test/task1/file_mess/secret_message
https://github.com/sindresorhus/awesome

```






 



# dz-4
