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
# souce 
source openrc.sh

```

> check yout configuration

```sh
# list your instances 
nova list

# list networks
```

![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/list.png)




# nova net-list

```
