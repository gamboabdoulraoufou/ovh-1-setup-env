### ovh-1-setup-env

This post show how to:
- setup Openstack API to manage cloud ressources (instance, network, etc.)
- setup 
- 
> Setup OpenStack command-line 

```sh
# install module
sudo pip install python-openstackclient

# configure open

# source file (execute this command into file which contains your file or specify your path)
source openrc.sh

# list your instances for test
nova list

+--------------------------------------+-------+--------+------------+-------------+----------------------------------------------------+
| ID                                   | Name  | Status | Task State | Power State | Networks                                           |
+--------------------------------------+-------+--------+------------+-------------+----------------------------------------------------+
| 85ad671d-3831-4fbb-a239-7731d8f1d1c4 | hdp-1 | ACTIVE | -          | Running     | Ext-Net=145.239.155.75, 2001:41d0:401:2100::2:d5eb |
| 25980044-d987-4458-ae2d-abfda659184a | hdp-2 | ACTIVE | -          | Running     | Ext-Net=145.239.155.76, 2001:41d0:401:2100::2:d5ec |
| 25247c79-111b-4987-b506-d20d8c71c0f3 | hdp-3 | ACTIVE | -          | Running     | Ext-Net=145.239.155.78, 2001:41d0:401:2100::2:d5ed |
+--------------------------------------+-------+--------+------------+-------------+----------------------------------------------------+

