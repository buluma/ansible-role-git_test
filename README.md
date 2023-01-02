# [git_test](#git_test)

Install and configure git_test on your system.

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-git_test/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-git_test/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-git_test/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-git_test)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/buluma/git_test)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/buluma/git_test)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-git_test.svg)](https://github.com/buluma/ansible-role-git_test/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-git_test.svg)](https://github.com/buluma/ansible-role-git_test/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-git_test.svg)](https://github.com/buluma/ansible-role-git_test/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
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


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for git_test
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-git_test/blob/main/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-git_test/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|alpine|all|
|amazon|Candidate|
|el|8|
|debian|all|
|fedora|all|
|opensuse|all|
|ubuntu|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.


If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-git_test/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-git_test/blob/master/CHANGELOG.md)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)

### [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
