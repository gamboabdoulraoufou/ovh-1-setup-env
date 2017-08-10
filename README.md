### ovh-1-setup-env


This post show how to:
- setup Openstack API to manage cloud ressources (instance, network, etc.)
- setup 
- 


Pre-requisites:
- Python 2.7
- Python-pip
- root acces on your client
- internet connexion


> Setup OpenStack command-line 

```sh
# install openstackclient
pip install python-openstackclient

# install glanceclient
pip install python-glanceclient 

# install neutronclient
pip install python-neutronclient

# install novaclient
pip install python-novaclient

# install novaclient
pip install python-keystoneclient

# install novaclient
pip install python-swiftclient

# install novaclient
pip install python-cinderclient

# install cinder
pip install python-heatclient

# install ceilometerclient
pip install python-ceilometerclient

```

> Create openrc.sh file with the following parameters

![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/openrc.png)


> Source file (execute this command into file which contains your file or specify your path)

```sh
# souce 
source openrc.sh

```

> List instance

```sh
# list your instances 
nova list
```

![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/list.png)

> List networks

```sh
neutron net-list
```

![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/list3.png)


> Create your Network (vRack in this case)


> Attache network interface to existant VM

```sh
# attache network
nova interface-attach --net-id b19cb941-xxxx-xxxx-xxxx-581e8e7e4f54 instance-id

# check instance network
nova list
```


> From your server, list IP adress
```sh
# list ip adress from 
ip addr list
```

You should see 3 network inerfaces:
o : Loopback
eth0 : public interface
eth1 : private interface


> From your server, add VLAN IP adresse

```sh
# add private IP
ip addr add 192.168.0.3/24 dev eth1

# activate you IP
ip link set eth1 up

# check IP
ip addr list
```




> Attache network interface to existant VM
