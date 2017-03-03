[![Build Status](https://travis-ci.org/viasite-ansible/ansible-role-git.svg?branch=master)](https://travis-ci.org/viasite-ansible/ansible-role-git)

## Includes:
- install git
- configure system /etc/gitconfig
- configure user ~/.gitconfig
- configure user ~/.gitignore



## Examples:

### Configure system /etc/gitconfig

```
hosts: all
vars:
  git_user: system
  git_config_color:
    ui: auto
roles:
  - git
```


### Configure user ~/.gitconfig
Default `git_user` set to `ansible_user_id`.

```
hosts: all
vars:
  git_config_color:
    ui: auto
roles:
  - git
```
