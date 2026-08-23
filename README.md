# [Ansible role repository_powertools](#repository_powertools)

Enables the PowerTools/CodeReady Builder (CRB) repository on CentOS Stream, Rocky Linux and AlmaLinux

|GitHub|Downloads|Version|
|------|---------|-------|
|[![github](https://github.com/mullholland/ansible-role-repository_powertools/actions/workflows/molecule.yml/badge.svg)](https://github.com/mullholland/ansible-role-repository_powertools/actions/workflows/molecule.yml)|[![downloads](https://img.shields.io/ansible/role/d/mullholland/repository_powertools)](https://galaxy.ansible.com/mullholland/repository_powertools)|[![Version](https://img.shields.io/github/release/mullholland/ansible-role-repository_powertools.svg)](https://github.com/mullholland/ansible-role-repository_powertools/releases/)|
## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/mullholland/ansible-role-repository_powertools/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true
  roles:
    - role: "mullholland.repository_powertools"
```


## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/mullholland/ansible-role-repository_powertools/blob/master/defaults/main.yml):

```yaml
---
# dnf repo id that provides the PowerTools/CodeReady Builder repository,
# keyed by distribution_major_version. Renamed from "powertools" to "crb"
# starting with EL9 across CentOS Stream, Rocky Linux and AlmaLinux.
repository_powertools_repo_id:
  "8": powertools
  "9": crb
  "10": crb
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/mullholland/ansible-role-repository_powertools/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://mullholland.net) for further information.

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/r/mullholland/enterpriselinux)|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The version before the previous version.
- The previous version.
- The current version.

If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-repository_powertools/issues).

## [License](#license)

[MIT](https://github.com/mullholland/ansible-role-repository_powertools/blob/master/LICENSE).

## [Author Information](#author-information)

[Mullholland](https://mullholland.net)
