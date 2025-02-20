How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 52053
Username: picoplayer 
Password: pYkku7iMsS
```

Solución
A la hora de hablar de funciones automatizadas entra los cron jobs, tenemos que localizar donde se encuentra el archivo de crontab que es donde se guardan los cron jobs y ver dentro del archivo para ver la flag
```
picoplayer@challenge:~$ cd /

picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

picoplayer@challenge:/$ cd etc

picoplayer@challenge:/etc$ ls
adduser.conf            cloud         debconf.conf    fstab      hostname     kernel         logrotate.d    mke2fs.conf          pam.conf   rc0.d  resolv.conf  ssh        sysctl.conf  update-motd.d
alternatives            cron.d        debian_version  gai.conf   hosts        ld.so.cache    lsb-release    modules-load.d       pam.d      rc1.d  rmt          ssl        sysctl.d     wgetrc
apt                     cron.daily    default         group      hosts.allow  ld.so.conf     machine-id     mtab                 passwd     rc2.d  security     subgid     systemd      xattr.conf
bash.bashrc             cron.hourly   deluser.conf    group-     hosts.deny   ld.so.conf.d   magic          networkd-dispatcher  passwd-    rc3.d  selinux      subgid-    terminfo     xdg
bindresvport.blacklist  cron.monthly  dhcp            gshadow    init.d       legal          magic.mime     networks             profile    rc4.d  shadow       subuid     timezone
binfmt.d                cron.weekly   dpkg            gshadow-   inputrc      libaudit.conf  mailcap        nsswitch.conf        profile.d  rc5.d  shadow-      subuid-    tmpfiles.d
ca-certificates         crontab       e2scrub.conf    gss        issue        localtime      mailcap.order  opt                  python3    rc6.d  shells       sudoers    ucf.conf
ca-certificates.conf    dbus-1        environment     host.conf  issue.net    login.defs     mime.types     os-release           python3.8  rcS.d  skel         sudoers.d  ufw

picoplayer@challenge:/etc$ cat crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
```