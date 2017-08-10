### ovh-1-setup-env

This post show how to:
- setup Openstack API to manage cloud ressources (instance, network, etc.)
- setup 
- 
> Setup OpenStack command-line 

```sh
# install module
sudo pip install python-openstackclient
```

> Create openrc.sh file with the following parameters

![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/openrc.png)


> Source file (execute this command into file which contains your file or specify your path)

```sh
source openrc.sh
```


## openrc.sh file contains something like this
#!/bin/bash
export OS_AUTH_URL=https://auth.cloud.ovh.net/v2.0/
export OS_TENANT_ID=xxxxxxxxxxx
export OS_TENANT_NAME="xxxxxxxx"
export OS_USERNAME="xxxxxxx"
export OS_PASSWORD="xxxxxxxx"
export OS_REGION_NAME="xxx"

# list your instances for test
nova list

# you should see something like this
+--------------------------------------+-------+--------+------------+-------------+----------------------------------------------------+
| ID                   | Name  | Status | Task State | Power State | Networks                                           |
+--------------------------------------+-------+--------+------------+-------------+----------------------------------------------------+
| hhhdnss-eushzs-zeerz | instance-1 | ACTIVE | -          | Running     | Ext-Net=xxx.xxx.xxx.xx, xxxx:xxxx:xxx:xxxx::x:xxxx |
| hhh23ss-eushzs-ze8rz | instance-2 | ACTIVE | -          | Running     | Ext-Net=xxx.xxx.xxx.xx, xxxx:xxxx:xxx:xxxx::x:xxxx |
| hhhdnss-eushzs-zeern | instance-3 | ACTIVE | -          | Running     | Ext-Net=xxx.xxx.xxx.xx, xxxx:xxxx:xxx:xxxx::x:xxxx |
+--------------------------------------+-------+--------+------------+-------------+----------------------------------------------------+

# nova net-list

```
