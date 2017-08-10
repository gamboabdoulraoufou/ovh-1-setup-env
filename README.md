### ovh-1-setup-env


This post show how to:
- setup vRack (VLAN)
- setup Openstack API to manage cloud ressources (instance, network, etc.)
- assign private IP to a specific VM


Pre-requisites:
- Python 2.7
- Python-pip
- root acces on your client
- internet connexion


> Setup VLAN 

![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/vlan0.png)
![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/vlan1.png)
![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/vlan2.png)
![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/vlan3.png)
![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/vlan4.png)
![MetaStore remote database](https://github.com/gamboabdoulraoufou/ovh-1-setup-env/blob/master/img/vlan5.png)

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
nova interface-attach 85ad671d-3831-4fbb-a239-7731d8f1d1c4 --net-id c0eb174d-b681-4059-a630-68b5cd810741 --fixed-ip 192.168.0.21

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


> From your server, enable IP adress and check congif

```sh
# enable network interface
ip link set eth1 up

# check IP
ip addr list
```

