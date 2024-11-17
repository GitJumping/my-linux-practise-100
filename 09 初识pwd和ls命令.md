# pwd



# ls

接收两个路径

```shell
[root@localhost noah]# ls /root/ /
/:
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

/root/:
anaconda-ks.cfg  initial-setup-ks.cfg
```

命令和参数之间一定要有空格，不然无法识别参数的。

## ls -l

```shell
[noah@localhost ~]$ ls -l
total 4
-rw-rw-r--. 1 noah noah  5 Jul 15 13:22 1.txt
drwxr-xr-x. 3 noah noah 17 Jun 22 10:50 Desktop
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Documents
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Downloads
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Music
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Pictures
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Public
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Templates
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Videos
# 文件类型 文件/目录的权限 文件个数 创建文件的用户的名字 文件大小 文件最后修改时间
```

长格式显示

## ls -a

显示所有文件，包括隐藏文件

## ls -r

以逆向形式进行排序

`-r`默认对文件名进行逆向显示

### ls -l -r

```shell
[noah@localhost ~]$ ls -l -r
total 4
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Videos
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Templates
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Public
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Pictures
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Music
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Downloads
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Documents
drwxr-xr-x. 3 noah noah 17 Jun 22 10:50 Desktop
-rw-rw-r--. 1 noah noah  5 Jul 15 13:22 1.txt
```

### ls -l -r -t

```shell
[noah@localhost ~]$ ls -l -r -t
total 4
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Videos
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Templates
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Public
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Pictures
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Music
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Downloads
drwxr-xr-x. 2 noah noah  6 Jun 22 10:12 Documents
drwxr-xr-x. 3 noah noah 17 Jun 22 10:50 Desktop
-rw-rw-r--. 1 noah noah  5 Jul 15 13:22 1.txt
```

### ls -lrt

## ls -R

```shell
[noah@localhost ~]$ ls -R
.:
1.txt  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos

./Desktop:
vmt

./Desktop/vmt:
manifest.txt  VMwareTools-10.3.25-20206839.tar.gz  vmware-tools-distrib  vmware-tools-upgrader-64

./Desktop/vmt/vmware-tools-distrib:
bin  doc  etc  FILES  INSTALL  installer  lib  vgauth  vmware-install.pl

./Desktop/vmt/vmware-tools-distrib/bin:
vm-support  vmware-config-tools.pl  vmware-uninstall-tools.pl

./Desktop/vmt/vmware-tools-distrib/doc:
INSTALL  open_source_licenses.txt  README

./Desktop/vmt/vmware-tools-distrib/etc:
installer.sh          messages        poweroff-vm-default  resume-vm-default  statechange.subr    vmware-tools                 vmware-tools-prelink.conf  vmware-user.Xresources  xsession-xdm.pl
manifest.txt.shipped  not_configured  poweron-vm-default   scripts            suspend-vm-default  vmware-tools-libraries.conf  vmware-user.desktop        xsession-gdm.sh         xsession-xdm.sh
```

显示文件夹里的文件

```shell
[noah@localhost ~]$ ls -lartR
.:
total 36
-rw-r--r--.  1 noah noah  231 Oct 30  2018 .bashrc
-rw-r--r--.  1 noah noah  193 Oct 30  2018 .bash_profile
-rw-r--r--.  1 noah noah   18 Oct 30  2018 .bash_logout
drwxr-xr-x.  4 noah noah   39 Jun 22 09:52 .mozilla
drwxr-xr-x.  3 root root   18 Jun 22 10:12 ..
drwx------.  3 noah noah   25 Jun 22 10:12 .dbus
drwx------.  3 noah noah   19 Jun 22 10:12 .local
-rw-------.  1 noah noah   16 Jun 22 10:12 .esd_auth
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Videos
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Templates
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Public
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Pictures
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Music
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Downloads
drwxr-xr-x.  2 noah noah    6 Jun 22 10:12 Documents
drwxr-xr-x. 14 noah noah  261 Jun 22 10:14 .config
drwxr-xr-x.  3 noah noah   17 Jun 22 10:50 Desktop
drwx------. 16 noah noah 4096 Jul 15 12:36 .cache
-rw-------.  1 noah noah  693 Jul 15 12:37 .bash_history
-rw-------.  1 noah noah 1860 Jul 15 12:49 .ICEauthority
-rw-rw-r--.  1 noah noah    5 Jul 15 13:22 1.txt
drwx------. 15 noah noah 4096 Jul 15 13:22
```

