# [repository_powertools](#repository_powertools)

**IMPORTANT**
This role will no longer be updated. you can use [robertdebock/ansible-role-powertools](https://github.com/robertdebock/ansible-role-powertools) as an alternative.

---


|GitHub|GitLab|
|------|------|
|[![github](https://github.com/mullholland/ansible-role-repository_powertools/workflows/Ansible%20Molecule/badge.svg)](https://github.com/mullholland/ansible-role-repository_powertools/actions)|[![gitlab](https://gitlab.com/mullholland/ansible-role-repository_powertools/badges/main/pipeline.svg)](https://gitlab.com/mullholland/ansible-role-repository_powertools)|

description

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
```yaml
---
repository_powertools_repo_file:
  EL:
    "8": "CentOS-Stream-PowerTools.repo"
  CentOS:
    "8": "CentOS-Stream-PowerTools.repo"
  Rocky:
    "8": "Rocky-PowerTools.repo"
  AlmaLinux:
    "8": "almalinux-powertools.repo"
```


## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true
  # vars:
  #   example_var: "value"
  roles:
    - role: "mullholland.repository_powertools"
```





## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

-   [centos-stream8](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream8)
-   [rockylinux8](https://hub.docker.com/r/mullholland/docker-molecule-rockylinux8)
-   [almalinux8](https://hub.docker.com/r/mullholland/docker-molecule-almalinux8)

The minimum version of Ansible required is 2.10, tests have been done to:

-   The previous versions.
-   The current version.



## [Exceptions](#exceptions)

Some variations of the build matrix do not work. These are the variations and reasons why the build won't work:

| variation                 | reason                 |
|---------------------------|------------------------|
| Ubuntu* | repo only supports RedHat/CentOS Server |
| Debian* | repo only supports RedHat/CentOS Server |
| Fedora* | repo only supports RedHat/CentOS Server |
| CentOS7 | repo does not exists on CentOS 7 |
| Ubi8 | repo does not exists on Ubi 8 |
| centos-stream9 | repo does not exists on CentOS-Stream9 |
| Amazonlinux | repo does not exists on Amazonlinux |


If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-repository_powertools/issues)

## [License](#license)

MIT


## [Author Information](#author-information)

[Mullholland](https://github.com/mullholland)

## [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
