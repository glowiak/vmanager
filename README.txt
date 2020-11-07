VManager - A frontend that makes QEMU easy to use.

Format: At the moment I'm providing two formats - tar.gz package that works on all linux distros, and Arch package.

Dependiences:
-qemu (necessary)
-zenity (necessary)
-ksh (opcional)

DOWNLOAD:
tar.gz package: https://github.com/glowiak/vmanager/releases/download/0.11/vmanager-0.11-linux.tar.gz
Arch package: https://github.com/glowiak/vmanager/releases/download/0.11/vmanager-0.11-1-x86_64.pkg.tar.zst

Installation:
Arch package: # pacman -U <path to Arch package>
tar.gz package: # cd / && tar xvf <path to tar.gz package>
Debian package: I'm don't providing debian package, because I'm not use debian.

Installation in other OSes:
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
