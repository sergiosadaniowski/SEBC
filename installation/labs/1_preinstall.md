
1.Check vm.swappiness on all your nodes

```

[ec2-user@ip-172-31-8-198 ~]$ cat /proc/sys/vm/swappiness
1
[ec2-user@ip-172-31-8-198 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[ec2-user@ip-172-31-8-198 ~]$ cat /proc/sys/vm/swappiness
1

```

2.Show the mount attributes of your volume(s)

```
[ec2-user@ip-172-31-8-198 ~]$ mount
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,size=15340256k,nr_inodes=3835064,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/net_cls type cgroup (rw,nosuid,nodev,noexec,relatime,net_cls)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/xvda2 on / type xfs (rw,relatime,attr2,inode64,noquota)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=29,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
mqueue on /dev/mqueue type mqueue (rw,relatime)
/dev/xvdb on /mnt/disco1 type ext4 (rw,relatime,data=ordered)
/dev/xvdc on /mnt/disco2 type ext4 (rw,relatime,data=ordered)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,size=3045488k,mode=700,uid=1000,gid=1000)
[ec2-user@ip-172-31-8-198 ~]$


```
3.If you have ext-based volumes, list the reserve space setting
????


4.Disable transparent hugepage support

```
[ec2-user@ip-172-31-8-198 ~]$ sudo su
[root@ip-172-31-8-198 ec2-user]#  echo never > /sys/kernel/mm/transparent_hugepage/enabled
[root@ip-172-31-8-198 ec2-user]# cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]
[root@ip-172-31-8-198 ec2-user]# always madvise [never]
```


5.List your network interface configuration

```
[ec2-user@ip-172-31-8-198 ~]$  ip link show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc pfifo_fast state UP mode DEFAULT qlen 1000
    link/ether 0a:29:55:7f:37:24 brd ff:ff:ff:ff:ff:ff
[ec2-user@ip-172-31-8-198 ~]$
```

6.Show that forward and reverse host lookups are correctly resolved

```
[ec2-user@ip-172-31-8-198 ~]$ nslookup ec2-34-215-96-48.us-west-2.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-34-215-96-48.us-west-2.compute.amazonaws.com
Address: 172.31.8.198

[ec2-user@ip-172-31-8-198 ~]$ nslookup 172.31.8.198
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
198.8.31.172.in-addr.arpa       name = ip-172-31-8-198.us-west-2.compute.internal.

Authoritative answers can be found from:

```

Show the nscd service is running

```
[root@ip-172-31-8-198 ec2-user]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-10-02 14:14:30 EDT; 5min ago
 Main PID: 2445 (nscd)
   CGroup: /system.slice/nscd.service
           └─2445 /usr/sbin/nscd

Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 monitoring file `/etc/hosts` (4)
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 monitoring directory `/etc` (2)
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 monitoring file `/etc/resolv.conf` (5)
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 monitoring directory `/etc` (2)
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 monitoring file `/etc/services` (6)
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 monitoring directory `/etc` (2)
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
Oct 02 14:14:30 ip-172-31-8-198.us-west-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Oct 02 14:14:49 ip-172-31-8-198.us-west-2.compute.internal nscd[2445]: 2445 checking for monitored file `/etc/netgroup': No such file or directory
[root@ip-172-31-8-198 ec2-user]#

```

Show the ntpd service is running

```
[root@ip-172-31-8-198 ec2-user]# systemctl enable ntpd
Created symlink from /etc/systemd/system/multi-user.target.wants/ntpd.service to /usr/lib/systemd/system/ntpd.service.
[root@ip-172-31-8-198 ec2-user]# systemctl start ntpd
[root@ip-172-31-8-198 ec2-user]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-10-02 14:16:35 EDT; 4s ago
  Process: 2513 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 2514 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─2514 /usr/sbin/ntpd -u ntp:ntp -g

Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: Listen and drop on 1 v6wildcard :: UDP 123
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: Listen normally on 2 lo 127.0.0.1 UDP 123
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: Listen normally on 3 eth0 172.31.8.198 UDP 123
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: Listen normally on 4 lo ::1 UDP 123
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: Listen normally on 5 eth0 fe80::829:55ff:fe7f:3724 UDP 123
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: Listening on routing socket on fd #22 for interface updates
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal systemd[1]: Started Network Time Service.
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: 0.0.0.0 c016 06 restart
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Oct 02 14:16:35 ip-172-31-8-198.us-west-2.compute.internal ntpd[2514]: 0.0.0.0 c011 01 freq_not_set
[root@ip-172-31-8-198 ec2-user]#

```


