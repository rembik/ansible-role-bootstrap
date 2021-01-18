Ansible Role: Bootstrap
=======================

[![][ci_badge]][ci]
[![][release_badge]][release]
[![][ansible_role_badge]][ansible_role]
[![][ansible_downloads_badge]][ansible_role]

Prepare your system to be managed by Ansible.

Requirements
------------

- Access to repositories containing system packages, likely on the internet.
- A recent Ansible version (tested last 2 stable major versions).

Role Variables
--------------

These defaults are set in `defaults/main.yml`:

```yaml
---
# defaults file for bootstrap

# The user to use to connect to machines.
bootstrap_user: root

# Do you want to wait for the host to be available?
bootstrap_wait_for_host: no

# The number of seconds you want to wait during connection test before failing.
bootstrap_timeout: 3
```

Dependencies
------------

None.

Example Playbook
----------------

This example is taken from `molecule/resources/converge.yml`:
```yaml
---
- name: Converge
  hosts: all
  gather_facts: no
  become: yes

  tasks:
    - include_role:
        name: ansible-role-bootstrap

```

Tests
-----

[![][python_badge]][python]
[![][ansible_badge]][ansible]

This role is tested periodically against the following Linux distributions:

|| [![][ansible_previous_badge]][ansible_previous] | [![][ansible_latest_badge]][ansible_latest] | [![][ansible_devel_badge]][ansible_devel] |
|---|---|---|---|
| [![][alpine_badge]][alpine] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][amazonlinux_badge]][amazonlinux] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][archlinux_badge]][archlinux] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][centos_badge]][centos] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][debian_badge]][debian] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][fedora_badge]][fedora] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][gentoo_badge]][gentoo] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][kali_badge]][kali] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][opensuse_badge]][opensuse] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][redhat_badge]][redhat] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |
| [![][ubuntu_badge]][ubuntu] | [![][x]][ci] | [![][x]][ci] | [![][x]][ci] |

> Asteriks means the build is allowed to fail, it's marked as an experimental build.

Contributing
------------

If you find issues, please register them at this [GitHub project issue page][issues] or consider contributing code by following this [guideline][contributing].

License
-------

[Apache License, Version 2.0][license]

Author Information
------------------

- [Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
- [Brian Rimek](https://github.com/rembik)


[ci]: https://github.com/rembik/ansible-role-bootstrap/actions
[travis_ci]: https://travis-ci.org/github/rembik/ansible-role-bootstrap
[release]: https://github.com/rembik/ansible-role-bootstrap/releases
[ansible_role]: https://galaxy.ansible.com/rembik/bootstrap

[ci_badge]: https://img.shields.io/github/workflow/status/rembik/ansible-role-bootstrap/CI/master?logo=github&label=test
[travis_ci_badge]: https://img.shields.io/travis/rembik/ansible-role-bootstrap/master.svg?logo=travis-ci&logoColor=EEE&label=test
[release_badge]: https://img.shields.io/github/release/rembik/ansible-role-bootstrap.svg?sort=semver&colorB=56b4b6&logo=github&logoColor=EEE
[ansible_role_badge]: https://img.shields.io/ansible/role/36340.svg?colorB=56b4b6&logo=ansible&logoColor=EEE
[ansible_downloads_badge]: https://img.shields.io/ansible/role/d/36340.svg?label=downloads&logo=ansible&logoColor=EEE

[issues]: https://github.com/rembik/ansible-role-bootstrap/issues/new/choose
[contributing]: http://github.com/rembik/ansible-role-bootstrap/tree/master/.github/CONTRIBUTING.md
[license]: https://github.com/rembik/ansible-role-bootstrap/blob/master/LICENSE

[python]: https://www.python.org/
[ansible]: https://ansible.com/
[ansible_previous]: https://docs.ansible.com/ansible/2.9/
[ansible_latest]: https://docs.ansible.com/ansible/2.10/
[ansible_devel]: https://docs.ansible.com/ansible/devel/

[python_badge]: https://img.shields.io/badge/python-3.9-1488C6.svg
[ansible_badge]: https://img.shields.io/badge/Ansible-2.9%20%7C%202.10%20%7C%20devel%2A-56b4b6.svg
[ansible_previous_badge]: https://img.shields.io/badge/2.9-56b4b6.svg
[ansible_latest_badge]: https://img.shields.io/badge/2.10-56b4b6.svg
[ansible_devel_badge]: https://img.shields.io/badge/devel%2A-56b4b6.svg

[alpine]: https://hub.docker.com/_/alpine
[amazonlinux]: https://hub.docker.com/_/amazonlinux
[archlinux]: https://hub.docker.com/r/archlinux/base
[centos]: https://hub.docker.com/_/centos
[debian]: https://hub.docker.com/_/debian
[fedora]: https://hub.docker.com/_/fedora
[gentoo]: https://hub.docker.com/r/gentoo/stage3-amd64
[kali]: https://hub.docker.com/r/kalilinux/kali
[opensuse]: https://hub.docker.com/_/opensuse
[redhat]: https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8/ubi
[ubuntu]: https://hub.docker.com/_/ubuntu

[alpine_badge]: https://img.shields.io/badge/Alpine-latest%20%7C%20edge%2A-1488C6.svg?logo=docker&logoColor=EEE
[amazonlinux_badge]: https://img.shields.io/badge/AmazonLinux-latest-1488C6.svg?logo=docker&logoColor=EEE
[archlinux_badge]: https://img.shields.io/badge/ArchLinux-latest-1488C6.svg?logo=docker&logoColor=EEE
[centos_badge]: https://img.shields.io/badge/CentOS-latest-1488C6.svg?logo=docker&logoColor=EEE
[debian_badge]: https://img.shields.io/badge/Debian-latest%20%7C%20unstable%2A-1488C6.svg?logo=docker&logoColor=EEE
[fedora_badge]: https://img.shields.io/badge/Fedora-latest%20%7C%20rawhide%2A-1488C6.svg?logo=docker&logoColor=EEE
[gentoo_badge]: https://img.shields.io/badge/Gentoo-latest%2A-1488C6.svg?logo=docker&logoColor=EEE
[kali_badge]: https://img.shields.io/badge/Kali-latest%2A-1488C6.svg?logo=docker&logoColor=EEE
[opensuse_badge]: https://img.shields.io/badge/openSUSE-Leap%20%7C%20Tumbleweed-1488C6.svg?logo=docker&logoColor=EEE
[redhat_badge]: https://img.shields.io/badge/RedHat-latest-1488C6.svg?logo=docker&logoColor=EEE
[ubuntu_badge]: https://img.shields.io/badge/Ubuntu-latest%20%7C%20devel%2A-1488C6.svg?logo=docker&logoColor=EEE
[x]: https://img.shields.io/badge/X-grey.svg
