# SSHKEYS manager

Add and revoque ssh keys dinamically from remote servers

## Steps

Move vars/userslist.yml.example to vars/userslist.yml
Fill the var `all_users_list` with your users list and their ssh keys (they can have multiple keys).

## How to use
The best way is leaving empty allowed_users and revoqued_users and call the playbook with --extra-vars

To add users keys to remote servers:
`ansible-playbook main.yml --extra-vars "allowed_users=User1,User2,User44"`

To remove users keys from remote servers:
`ansible-playbook main.yml --extra-vars "revoqued_users=User1,User2,User44"`
