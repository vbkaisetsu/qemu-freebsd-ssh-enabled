FreeBSD image for QEMU with SSH
===============================

Account information
-------------------

* User: `root`
* Password: `password`

How to create this image?
--------------------------

1. Download qcow2 image from: https://download.freebsd.org/ftp/releases/VM-IMAGES/
2. Run the following commands in this image:
```sh
echo 'console="comconsole"' >> /boot/loader.conf
echo 'sshd_enable="YES"' >> /etc/rc.conf
echo 'Port 22' >> /etc/ssh/sshd_config
echo 'Protocol 2' >> /etc/ssh/sshd_config
echo 'PermitRootLogin yes' >> /etc/ssh/sshd_config
echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config
echo 'PermitEmptyPasswords no' >> /etc/ssh/sshd_config
```
