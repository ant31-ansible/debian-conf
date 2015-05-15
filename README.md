Debian Conf
==========

Depend on other roles to configure a server

Requirements
------------

Role Dependencies
----------------

```yaml
---
dependencies:
  - role: apt
    apt:
      ppa:
        - ppa:ubuntu-lxc/lxd-git-master
      packages:
        - zsh
        - ubuntu-standard
        - emacs24-nox
        - openssh-server
        - build-essential
        - git
        - ferm
        - aptitude
        - traceroute
        - zsh
        - tree
        - htop
        - vim
        - rsync
        - ssh
        - python
        - python2.7
        - python2.7-dev
        - iproute
        - gawk
        - discover
        - ssh-import-id
        - python-pip
        - ncurses-term
        - curl
        - btrfs-tools
        - nmap
        - ipython
        - python-lxc
        - bc
        - curl
        - ack-grep
        - autoconf
        - automake
        - sshpass
        - psutils

  - role: pip
    pip_packages:
      - ansible
      - progressbar
      - argparse
      - paramiko
      - jinja2

  - role: emacs-conf
  - role: zsh-conf
  - role: ferm-firewall
```

Dependencies
------------

 - None

Example Playbook
----------------

```yaml
---
- hosts: server
  roles:
    - debian-conf
```

License
-------

MIT
