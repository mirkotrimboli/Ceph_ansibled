# Ceph_ansibled
This playbook aims to produce a cluster Ceph.

# Release note
* The code work on multiple Operative Systems Linux based.
* It is tested with: Ubuntu 18.04LTS, 20.04LTS, CentOS 7.x, 8.x
* It is meant to get a Ceph cluster set up behind a proxy, you can choose between octopus, pacific and quincy versions by changing the variables, if necessary you can enable activities in the playbook yaml file.
* It is meant for work also on Cloud on IaaS.

# To use this code:
* Download the playbook.
* Edit your hosts file with IP and hostnames of your servers.
* Edit playbook hosts file with hostnames of your servers.
* create a private key for the user "cephadmin", rename the produced files as "cephadmin.pem, cephadmin.pub" and place them in the "keys" folder
* Compile file in group_vars directory as is it is explained.
* Then you must to move into the folder with command: "cd /absolute/path/to/playbook".
* Finally you can run the code with command: "ansible-playbook -i ceph.hosts ceph.yaml".

# For use on Cloud
* Edit playbook hosts file without references to password.
* You can run the code with command: "ansible-playbook -i ceph.hosts ceph.yaml --key-file=/absolute/path/to/key.pem".
