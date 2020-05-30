# Usage

Add your server to the hosts and the firs thing you want to do is run the common role as root to setup users
and the firewall, basic setup.

`ansible-playbook --user root -i hosts plays/common.yml --extra-vars 'ansible_ssh_pass=<pass>'`

Then you can run any other plays as your current user.

`ansible-playbook --user zac -i hosts plays/[play].yml`

# Dev
## Molecule

### Init a new role
`molecule init role role-name-here -d docker`

### Init in existing role
`molecule init scenario --role-name role-name-here -d docker`

# Personal Env

`ansible-playbook --connection=local --inventory 127.0.0.1, plays/personal.yml`