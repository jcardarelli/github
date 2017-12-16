# github
Ansible roles to manage GitHub repos

## Specify username and password with basic auth

The role github/oauth-token will look for the following variables:
```
user: "{{ user }}"
password: "{{ password }}"
```
