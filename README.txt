VManager - A frontend that makes QEMU easy to use.

Format: At the moment I'm providing two formats - tar.gz package that works on all linux distros, and Arch package.

Dependiences:
-qemu (necessary)
-zenity (necessary)
-ksh (necessary)
-qemu-arch-extra (opcional on ArchLinux)

Dependiences on FreeBSD:
-qemu
-zenity
-bash

(old) NOTE! Installation won't create desktop or application link. To run it you must type in terminal "vmanager" command
or create you own link to this command.

Latest version: 0.15

DOWNLOAD:
tar.gz for Linux: https://github.com/glowiak/vmanager/releases/download/0.15/vmanager-0.15-linux.tar.gz
tar.gz for FreeBSD: https://github.com/glowiak/vmanager/releases/download/0.15/vmanager-0.15_fp01-freebsd.tar.gz
Arch package: https://github.com/glowiak/vmanager/releases/download/0.15/vmanager-0.15-1-any.pkg.tar.zst
Debian package: not available yet.

DOWNLOAD OLD BUILDS:
v0.14/v0.14_fp01:
tar.gz for Linux: https://github.com/glowiak/vmanager/releases/download/0.14/vmanager-0.14-linux.tar.gz
0.14_fp01 tar.gz for FreeBSD: https://github.com/glowiak/vmanager/releases/download/0.14_fp01/vmanager-0.14_fp01-freebsd.tar.gz
Arch package: https://github.com/glowiak/vmanager/releases/download/0.14/vmanager-0.14-1-any.pkg.tar.zst
v0.13:
tar.gz for Linux: https://github.com/glowiak/vmanager/releases/download/0.13/vmanager-0.13-linux.tar.gz
tar.gz for FreeBSD: https://github.com/glowiak/vmanager/releases/download/0.13/vmanager-0.13-freebsd.tar.gz
Arch package: https://github.com/glowiak/vmanager/releases/download/0.13/vmanager-0.13-1-any.pkg.tar.zst
v0.12:
tar.gz package: https://github.com/glowiak/vmanager/releases/download/0.12/vmanager-0.12-linux.tar.gz
Arch package:https://github.com/glowiak/vmanager/releases/download/0.12/vmanager-0.12-1-x86_64.pkg.tar.zst
v0.11:
tar.gz package: https://github.com/glowiak/vmanager/releases/download/0.11/vmanager-0.11-linux.tar.gz
Arch package: https://github.com/glowiak/vmanager/releases/download/0.11/vmanager-0.11-1-x86_64.pkg.tar.zst

Path for 32 bit OSes (necessary if you have 32 bit os):
# rm /opt/vmanager/arch && echo "i386" >> /opt/vmanager/arch

Installation:
Arch package: # pacman -U <path to Arch package>
tar.gz package: # cd / && tar xzvf <path to tar.gz package>
Debian package: I'm don't providing debian package, because I'm not use debian.

Installation in other OSes:
NOTE!: This is only for versions older than 0.13!
FreeBSD:
(type this before installing): # mkdir -p /opt
Now install tar.gz package: # cd / && tar xvf <path to tar.gz package>
Path installation: # mv /usr/bin/vmanager /usr/local/bin/vmanager
More patches (you have to do it): delete "-enable-kvm" and "-cpu host" parts from /opt/vmanager/args
Done.

Using other architecture for VMs:
To do this you must:
on Arch: install qemu-arch-extra package and edit /opt/vmanager/arch file
on other distro/OS: edit /opt/vmanager/arch file

What I'll add in 0.13:
-support for FreeBSD without patches
-support for ArchLinux32 and ArchLinuxARM
-importing virtual machines

News in v0.14:
-repaired non-running vms on FreeBSD
-added icon to application menu

Bugs that I can't fix (bugzilla):
-BGFDB-001: Files or directories which names contains space are unsupported.


Used file extensions:
tar.gz  - package
pkg.tar.zst - Arch package
deb - Debian package (yet not available)
rpm - RedHat package (not available)
tar.xz  - source code (not available, because source code is installed to /opt/vmanager with package)

Should I move project to python 2 to get more portability?
