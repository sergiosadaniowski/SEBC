
kinit



```
[ec2-user@ip-172-31-0-35 ~]$ kinit cloudera-scm@AGNOSTIC.COM
Password for cloudera-scm@AGNOSTIC.COM: 
[ec2-user@ip-172-31-0-35 ~]$ 

```


klist


```
[ec2-user@ip-172-31-0-35 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_1000
Default principal: cloudera-scm@AGNOSTIC.COM

Valid starting     Expires            Service principal
04/10/17 13:04:17  05/10/17 13:04:17  krbtgt/AGNOSTIC.COM@AGNOSTIC.COM
	renew until 11/10/17 13:04:17
[ec2-user@ip-172-31-0-35 ~]$ 


```


