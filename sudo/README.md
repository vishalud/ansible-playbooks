# Ansible Sudo Role




> `sudo` is an [ansible](http://www.ansible.com) role which:
>
> * installs sudo
> * configures sudo


## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# sudo_users:
#  - { name: '%foo', nopasswd: yes }
#  - { name: 'bar', nopasswd: no }
#  - name: '%foo'
#    nopasswd: yes
#    commands: '/bin/ls'
#  - name: 'bar'
#    nopasswd: no
#    commands: '/bin/nano'
#  - name: '%foo'
#    nopasswd: yes
#    commands: '/bin/nano /etc/hosts'

# list of username or %groupname
sudo_users: []
```

## Example playbook

```
- host: all
  roles:
    - sudo
  vars:
    sudo_users:
      - { name: 'foo', nopasswd: no }
      - { name: '%sudo', nopasswd: yes }
      - name: '%foo'
        nopasswd: yes
        commands: '/bin/ls'
      - name: 'bar'
        nopasswd: no
        commands: '/bin/nano'
      - name: '%foo'
        nopasswd: yes
        commands: '/bin/nano /etc/hosts'
```













