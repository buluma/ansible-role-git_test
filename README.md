# [Ansible role git_test](#git_test)

Install and configure git_test on your system.

|GitHub|Version|Issues|Pull Requests|
|------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-git_test/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-git_test/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-git_test.svg)](https://github.com/buluma/ansible-role-git_test/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-git_test.svg)](https://github.com/buluma/ansible-role-git_test/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-git_test.svg)](https://github.com/buluma/ansible-role-git_test/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-git_test/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: yes

  vars:
    git_username: root
    git_groupname: root
    git_repository_destination: /root
    git_repositories:
      - repo: https://github.com/buluma/buluma.bootstrap
        dest: bootstrap
      - repo: https://github.com/buluma/buluma.bootstrap
        dest: bootstrap-force
        force: yes
      - repo: https://github.com/buluma/buluma.bootstrap
        dest: bootstrap-version
        version: "v2.0.0"

  roles:
    - role: buluma.git_test
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-git_test/blob/master/defaults/main.yml):

```yaml
---
# defaults file for git_test
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-git_test/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-git_test/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/repository/docker/buluma/alpine/general)|all|
|[Amazon](https://hub.docker.com/repository/docker/buluma/amazonlinux/general)|Candidate|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|8|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|all|
|[Fedora](https://hub.docker.com/repository/docker/buluma/fedora/general)|all|
|[opensuse](https://hub.docker.com/repository/docker/buluma/opensuse/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-git_test/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-git_test/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-git_test/blob/master/LICENSE).

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)


### [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
