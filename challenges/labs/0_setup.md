cloud provider : AWS 

instances by IP address and DNS name :



```

Instance 1
Public DNS (IPv4)  ec2-54-186-246-44.us-west-2.compute.amazonaws.com
public ip : 54.186.246.44
Private DNS  ip-172-31-9-71.us-west-2.compute.internal
Private IPs  172.31.9.71

Instance 2
Public DNS (IPv4)   ec2-34-214-96-250.us-west-2.compute.amazonaws.com
public ip 34.214.96.250
Private DNS ip-172-31-38-137.us-west-2.compute.internal
Private IPs 172.31.38.137


Instance 3
Public DNS (IPv4)  ec2-34-215-50-32.us-west-2.compute.amazonaws.com
public ip   34.215.50.32
Private DNS ip-172-31-4-34.us-west-2.compute.internal
Private IPs 172.31.4.34


Instance 4
Public DNS (IPv4) ec2-34-214-97-49.us-west-2.compute.amazonaws.com
public ip : 34.214.97.49
Private DNS ip-172-31-14-139.us-west-2.compute.internal
Private IPs 172.31.14.139


```


```
Linux release : Rhel 7.2 

file system capacity : 3 Discos 120 GB

output for yum repolist enabled :

sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                              repo name                                                           status
rhui-REGION-client-config-server-7/x86_64            Red Hat Update Infrastructure 2.0 Client Configuration Server 7          6
rhui-REGION-rhel-server-releases/7Server/x86_64      Red Hat Enterprise Linux Server 7 (RPMs)                            17.249
rhui-REGION-rhel-server-rh-common/7Server/x86_64     Red Hat Enterprise Linux Server 7 RH Common (RPMs)                     228
repolist: 17.483


```



```

List the /etc/passwd entries for saturn and haley

haley:x:2900:2900::/home/haley:/bin/bash
saturn:x:2800:2800::/home/saturn:/bin/bash



List the /etc/group entries for comets and planets

haley:x:2900:
saturn:x:2800:
planets:x:2901:saturn
comets:x:2902:haley

```