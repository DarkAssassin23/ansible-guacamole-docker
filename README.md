# Guacamole Docker Compose with Ansible

## About
An Ansible playbook to deploy Guacamole with Docker Compose

## Setup
1. Install Ansible
2. Install requirements: `ansible-galaxy collection install -r requirements.yml`
3. Rename `example.config.yml` and `example.inventory.ini` to `config.yml`
   and `inventory.ini` respectively, and modify them as desired. 

## Usage
```bash
ansible-playbook main.yml -i inventory.ini -K
```

Once the playbook completes, you should be able to navigate to the IP address
of the host you ran to playbook one at the given port you configured, e.g.,
`192.168.20.110:8080/guacamole/#/`. For your host, ensure the IP and port,
`192.168.20.110` and `8080` in this case, respectively, are what you
configured. Assuming everything was done properly, you should be greeted
with the following screen:

<img src="images/login.png" alt="Guacamole install success" width="100%" />

If you did not export an existing Guacamole database, the default credentials
will be `guacadmin` for both the username and password. If you exported
an existing Guacamole database, the username and password will be the same
as what they were on the previous installation, in which you exported the
database from.
