# github
Ansible roles to manage GitHub repos

## Installation
Clone this repo to your ansible roles directory.

Your ansible roles directory will be defined in your ansible.cfg file.

Use this command to find the directory:
```sh
(ansible-latest) user@server:~/ansible/roles/github$ echo $ANSIBLE_CONFIG
/home/user/ansible/ansible.cfg

(ansible-latest) user@server:~/ansible/roles/github$ cat $ANSIBLE_CONFIG | grep roles_path
roles_path    = roles

```

If your `roles_path` configuration variable is set to just `roles`, that means ansible-playbook will look in the runtime
directory for a directory called roles.

## Usage
```yml
- hosts: all

  roles:
    - github/oauth-token
```

## Specify username and password with basic auth

The role github/oauth-token will look for the following variables:
```
user: "{{ user }}"
password: "{{ password }}"
```
