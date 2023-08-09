# ansible_mysql

Installs and configures MySQL server on Ubuntu servers.

#Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global become: yes

#Role variables

Available variables are listed in vars/main.yml file
Also you can use -e(--extra-vars) flag to create databases, create users in the database and set the password for this user

#Usage

1. Genetare inventory file from config.toml: Run python3 generate_inventory.py
2. For mysql server installation run: ansible-playbook mysql.yml -i inventory
3. If you want to create new database, users and set password for this user run: ansible-playbook mysql.yml -i inventory -e "db_name=dev db_user=dev db_pass=passs"
