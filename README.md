# Netbox Ansible Playbooks

Playbooks for setting up or updating a Netbox install

### install Role

Assumptions:

1. Posgres DB is already running 

vars/main.yml variables

* netbox.version - Varision of Netbox to install
* netbox.superuser_email: email address of superuser, required for Django admin
* netbox.superuser_username: username of superuser, require for Django admin

* database.username - Username used to access Netbox PostgreSQL DB
* database.hostname - Hostname of server PostgreSQL DB is on


Extra Variables

* netbox_db_password - password for postgres DB.  

```
ansible-playbook netbox_install.yml -u $server_root_username -kK -i $server_hostname, -e netbox_db_password=$netbox_db_password -e superuser_password=$superuser_password
```

### upgrade Role



