[![Build Status](https://travis-ci.org/viasite-ansible/ansible-role-git.svg?branch=master)](https://travis-ci.org/viasite-ansible/ansible-role-git)

## Includes:
- install git
- configure system /etc/gitconfig
- configure user ~/.gitconfig
- configure user ~/.gitignore

Tested on Ubuntu and macOS.

## Examples:

### Configure system /etc/gitconfig
Set `git_user: system` for write to `/etc/gitconfig`:
```
hosts: all
vars:
  git_user: system
  git_config_color:
    ui: auto
roles:
  - git
```


### Configure user ~/.gitconfig and ~/.gitignore
Default `git_user` set to `ansible_user_id`:
```
hosts: all
vars:
  git_config_color:
    ui: auto
  git_gitignore:
    - ".idea"
roles:
  - git
```
