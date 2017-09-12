# ansible-macos-avatar
A Ansible role to manage personal avatar pictures in macOS.

[![Build Status](https://img.shields.io/travis/feffi/ansible-macos-avatar.svg)](https://travis-ci.org/feffi/ansible-macos-avatar) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-macos-avatar/total.svg)](https://github.com/feffi/ansible-macos-avatar) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-macos-avatar.svg?style=social&label=Fork)](https://github.com/feffi/ansible-macos-avatar) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-macos-avatar.svg?style=social&label=Star)](https://github.com/feffi/ansible-macos-avatar) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-macos-avatar.svg?style=social&label=Watch)](https://github.com/feffi/ansible-macos-avatar) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-macos-avatar/blob/master/LICENSE)

## Requirements
- Ansible 2.3

### ansible.cfg
```
hash_behaviour = merge
```

## Install
Just add the role to your ``requirements.yml`` file:
```yaml
- src: https://github.com/feffi/ansible-macos-avatar.git
  name: feffi.macos-avatar
```

## Role Variables
All role based variables are listed below, along with default values:

```yaml
macos_avatar:
  # Download avatar from remote URL, e.g. gravatar
  url: ""

```

## Dependencies
None.

## Example Playbook

```yaml
    - hosts: all
      vars:
        macos_avatar:
          url: "https://www.gravatar.com/avatar/87a6f83874350b4f04d5731b450585f1?s=250&d=mm&r=x"
      roles:
        - { role: feffi.macos-avatar }
```
Or with local parameters:

```yaml
    - hosts: all
      roles:
        - { role: feffi.macos-avatar,
            macos_avatar: {
              url: "https://www.gravatar.com/avatar/87a6f83874350b4f04d5731b450585f1?s=250&d=mm&r=x"
            }
          }
```
