# ansible-nfsserver-onAWS
Delivery of a NFS server on AWS

# Prerequisiti AWS
Assicurarsi che sulle macchine sia presente:

* Un volume aggiuntivo per l'export
* Service Group con regole Inbound aperte per la connessione SSH
* che sia stato dato un ip alla scheda di rete

Sul server Ansible:
* Fare il download con git clone
* All'interno dell'inventory path inserire la "chiave.pem" per l'accesso in SSH
* Modificare il file hosts del server ansible aggiungendo gli ip degli host da raggiungere e nominandoli come specificato in nfsenv.hosts

# Installazione e configurazione iniziale dei nodi 
se necessario modificare le variabili sotto group_vars/all/vars.yml

* datadev_name: xvdb
* nfs_dir: "/nfs"

lanciare il playbook ansible con il comando:

* ansible-playbook -i nfsenv.hosts nfsenv.yml --key-file=./chiave.pem --user=centos