# SymfonyOnDebian
Simple instructions on how to install Symfony on Debian Linux

I'm following these instructions: https://symfony.com/doc/current/setup.html

First we need to install PHP: https://linuxize.com/post/how-to-install-php-on-debian-10/

Below you can see the commands I executed in Debian terminal and their results.

```
root@debian:/home/pawel# sudo apt update
Get:1 http://security.debian.org/debian-security buster/updates InRelease [65.4 kB]
Hit:2 http://deb.debian.org/debian buster InRelease
Get:3 http://deb.debian.org/debian buster-updates InRelease [51.9 kB]
Get:4 http://security.debian.org/debian-security buster/updates/main Sources [179 kB]
Fetched 296 kB in 1s (441 kB/s) 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
All packages are up to date.
root@debian:/home/pawel# 
```

```
root@debian:/home/pawel# sudo apt install php libapache2-mod-php
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  libapache2-mod-php7.3 libsodium23 php-common php7.3 php7.3-cli php7.3-common php7.3-json php7.3-opcache php7.3-readline psmisc
Suggested packages:
  php-pear
The following NEW packages will be installed:
  libapache2-mod-php libapache2-mod-php7.3 libsodium23 php php-common php7.3 php7.3-cli php7.3-common php7.3-json php7.3-opcache
  php7.3-readline psmisc
0 upgraded, 12 newly installed, 0 to remove and 0 not upgraded.
Need to get 4,308 kB of archives.
After this operation, 18.6 MB of additional disk space will be used.
Do you want to continue? [Y/n] Y
Get:1 http://security.debian.org/debian-security buster/updates/main amd64 php7.3-common amd64 7.3.27-1~deb10u1 [960 kB]
Get:2 http://deb.debian.org/debian buster/main amd64 psmisc amd64 23.2-1 [126 kB]
Get:3 http://deb.debian.org/debian buster/main amd64 php-common all 2:69 [15.0 kB]
Get:4 http://deb.debian.org/debian buster/main amd64 libsodium23 amd64 1.0.17-1 [158 kB]
Get:5 http://deb.debian.org/debian buster/main amd64 libapache2-mod-php all 2:7.3+69 [6,120 B]
Get:6 http://deb.debian.org/debian buster/main amd64 php all 2:7.3+69 [5,964 B]
Get:7 http://security.debian.org/debian-security buster/updates/main amd64 php7.3-json amd64 7.3.27-1~deb10u1 [18.6 kB]
Get:8 http://security.debian.org/debian-security buster/updates/main amd64 php7.3-opcache amd64 7.3.27-1~deb10u1 [184 kB]
Get:9 http://security.debian.org/debian-security buster/updates/main amd64 php7.3-readline amd64 7.3.27-1~deb10u1 [12.0 kB]
Get:10 http://security.debian.org/debian-security buster/updates/main amd64 php7.3-cli amd64 7.3.27-1~deb10u1 [1,414 kB]
Get:11 http://security.debian.org/debian-security buster/updates/main amd64 libapache2-mod-php7.3 amd64 7.3.27-1~deb10u1 [1,362 kB]
Get:12 http://security.debian.org/debian-security buster/updates/main amd64 php7.3 all 7.3.27-1~deb10u1 [46.8 kB]
Fetched 4,308 kB in 1s (3,223 kB/s)
Selecting previously unselected package psmisc.
(Reading database ... 33471 files and directories currently installed.)
Preparing to unpack .../00-psmisc_23.2-1_amd64.deb ...
Unpacking psmisc (23.2-1) ...
Selecting previously unselected package php-common.
Preparing to unpack .../01-php-common_2%3a69_all.deb ...
Unpacking php-common (2:69) ...
Selecting previously unselected package php7.3-common.
Preparing to unpack .../02-php7.3-common_7.3.27-1~deb10u1_amd64.deb ...
Unpacking php7.3-common (7.3.27-1~deb10u1) ...
Selecting previously unselected package php7.3-json.
Preparing to unpack .../03-php7.3-json_7.3.27-1~deb10u1_amd64.deb ...
Unpacking php7.3-json (7.3.27-1~deb10u1) ...
Selecting previously unselected package php7.3-opcache.
Preparing to unpack .../04-php7.3-opcache_7.3.27-1~deb10u1_amd64.deb ...
Unpacking php7.3-opcache (7.3.27-1~deb10u1) ...
Selecting previously unselected package php7.3-readline.
Preparing to unpack .../05-php7.3-readline_7.3.27-1~deb10u1_amd64.deb ...
Unpacking php7.3-readline (7.3.27-1~deb10u1) ...
Selecting previously unselected package libsodium23:amd64.
Preparing to unpack .../06-libsodium23_1.0.17-1_amd64.deb ...
Unpacking libsodium23:amd64 (1.0.17-1) ...
Selecting previously unselected package php7.3-cli.
Preparing to unpack .../07-php7.3-cli_7.3.27-1~deb10u1_amd64.deb ...
Unpacking php7.3-cli (7.3.27-1~deb10u1) ...
Selecting previously unselected package libapache2-mod-php7.3.
Preparing to unpack .../08-libapache2-mod-php7.3_7.3.27-1~deb10u1_amd64.deb ...
Unpacking libapache2-mod-php7.3 (7.3.27-1~deb10u1) ...
Selecting previously unselected package libapache2-mod-php.
Preparing to unpack .../09-libapache2-mod-php_2%3a7.3+69_all.deb ...
Unpacking libapache2-mod-php (2:7.3+69) ...
Selecting previously unselected package php7.3.
Preparing to unpack .../10-php7.3_7.3.27-1~deb10u1_all.deb ...
Unpacking php7.3 (7.3.27-1~deb10u1) ...
Selecting previously unselected package php.
Preparing to unpack .../11-php_2%3a7.3+69_all.deb ...
Unpacking php (2:7.3+69) ...
Setting up libsodium23:amd64 (1.0.17-1) ...
Setting up psmisc (23.2-1) ...
Setting up php-common (2:69) ...
Created symlink /etc/systemd/system/timers.target.wants/phpsessionclean.timer → /lib/systemd/system/phpsessionclean.timer.
Setting up php7.3-common (7.3.27-1~deb10u1) ...

Creating config file /etc/php/7.3/mods-available/calendar.ini with new version

Creating config file /etc/php/7.3/mods-available/ctype.ini with new version

Creating config file /etc/php/7.3/mods-available/exif.ini with new version

Creating config file /etc/php/7.3/mods-available/fileinfo.ini with new version

Creating config file /etc/php/7.3/mods-available/ftp.ini with new version

Creating config file /etc/php/7.3/mods-available/gettext.ini with new version

Creating config file /etc/php/7.3/mods-available/iconv.ini with new version

Creating config file /etc/php/7.3/mods-available/pdo.ini with new version

Creating config file /etc/php/7.3/mods-available/phar.ini with new version

Creating config file /etc/php/7.3/mods-available/posix.ini with new version

Creating config file /etc/php/7.3/mods-available/shmop.ini with new version

Creating config file /etc/php/7.3/mods-available/sockets.ini with new version

Creating config file /etc/php/7.3/mods-available/sysvmsg.ini with new version

Creating config file /etc/php/7.3/mods-available/sysvsem.ini with new version

Creating config file /etc/php/7.3/mods-available/sysvshm.ini with new version

Creating config file /etc/php/7.3/mods-available/tokenizer.ini with new version
Setting up php7.3-opcache (7.3.27-1~deb10u1) ...

Creating config file /etc/php/7.3/mods-available/opcache.ini with new version
Setting up php7.3-json (7.3.27-1~deb10u1) ...

Creating config file /etc/php/7.3/mods-available/json.ini with new version
Setting up php7.3-readline (7.3.27-1~deb10u1) ...

Creating config file /etc/php/7.3/mods-available/readline.ini with new version
Setting up php7.3-cli (7.3.27-1~deb10u1) ...
update-alternatives: using /usr/bin/php7.3 to provide /usr/bin/php (php) in auto mode
update-alternatives: using /usr/bin/phar7.3 to provide /usr/bin/phar (phar) in auto mode
update-alternatives: using /usr/bin/phar.phar7.3 to provide /usr/bin/phar.phar (phar.phar) in auto mode

Creating config file /etc/php/7.3/cli/php.ini with new version
Setting up libapache2-mod-php7.3 (7.3.27-1~deb10u1) ...

Creating config file /etc/php/7.3/apache2/php.ini with new version
Module mpm_event disabled.
Enabling module mpm_prefork.
apache2_switch_mpm Switch to prefork
apache2_invoke: Enable module php7.3
Setting up libapache2-mod-php (2:7.3+69) ...
Setting up php7.3 (7.3.27-1~deb10u1) ...
Setting up php (2:7.3+69) ...
Processing triggers for man-db (2.8.5-2) ...
Processing triggers for libc-bin (2.28-10) ...
root@debian:/home/pawel# 
```
```
root@debian:/home/pawel# sudo systemctl restart apache2
root@debian:/home/pawel# 
```
```
root@debian:/home/pawel# cd /var/www/html
root@debian:/var/www/html# vi info.php
```
vi opens for editing new file
Press letter i to enter instert text mode & paste the following text:
```
<?php

phpinfo();
```
Press ESC to exit insert text mode. Type :wq to save the file and exit vi

Let's check what is my server's IP address:

```
root@debian:/var/www/html# ip add
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 08:00:27:28:d7:2b brd ff:ff:ff:ff:ff:ff
    inet 192.168.111.128/24 brd 192.168.111.255 scope global dynamic enp0s3
       valid_lft 82170sec preferred_lft 82170sec
    inet6 fe80::a00:27ff:fe28:d72b/64 scope link 
       valid_lft forever preferred_lft forever
root@debian:/var/www/html# 
```

We are interested in inet section, one with address different from 127.0.0.1. In our case it is 192.168.111.128. I enter this address in my browser in this format:

    http://your_server_ip/info.php

So it becomes

    http://192.168.111.128/info.php

Yeah! My result is this:

![image](https://user-images.githubusercontent.com/10007806/111873463-3c96b780-8988-11eb-9cb2-4c5282edf1a4.png)
