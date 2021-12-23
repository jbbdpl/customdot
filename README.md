# customdot

Repository for customized dotfiles. Ansible playbooks/roles which prepares the shell environment on linux jump hosts. 

------Prerequisites--------
ssh-copy-id username@ip/dns  - copy your local ssh key(create them first if u dont have them) to jumphost under certain user

log in to each server manualy to exchange fingerprints - remember that for jumphost ip have different fingerprint then dns

sudo apt install figlet  -- install figlet for ansible plugins to work on ur local machine

--------------------

TO run

ansible-playbook main.yaml -i hosts -l [group name from hosts file]

make sure ur main.yaml file has same settings for ur group name
- name: Setup local environment
  hosts: group name from hosts file
  user: user_name
