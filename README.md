# [repository_powertools](#repository_powertools)

|GitHub|GitLab|
|------|------|
|[![github](https://github.com/mullholland/ansible-role-repository_powertools/workflows/Ansible%20Molecule/badge.svg)](https://github.com/mullholland/ansible-role-repository_powertools/actions)|[![gitlab](https://gitlab.com/mullholland/ansible-role-repository_powertools/badges/master/pipeline.svg)](https://gitlab.com/mullholland/ansible-role-repository_powertools)|[![quality](https://img.shields.io/ansible/quality/unset)](https://galaxy.ansible.com/mullholland/repository_powertools)|

description

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
```yaml
---
repository_powertools_repo_file:
  EL:
    "7": "CentOS-Linux-PowerTools.repo"
    "8": "CentOS-Stream-PowerTools.repo"
  CentOS:
    "7": "CentOS-Linux-PowerTools.repo"
    "8": "CentOS-Stream-PowerTools.repo"
    "9": "CentOS-Stream-PowerTools.repo"
  Rocky:
    "8": "CentOS-Stream-PowerTools.repo"
  AlmaLinux:
    "8": "CentOS-Stream-PowerTools.repo"
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

-   [centos7](https://hub.docker.com/r/mullholland/docker-molecule-centos7)
-   [centos-stream8](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream8)
-   [centos-stream9](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream9)
-   [ubi8](https://hub.docker.com/r/mullholland/docker-molecule-ubi8)
-   [amazonlinux](https://hub.docker.com/r/mullholland/docker-molecule-amazonlinux)
-   [rockylinux8](https://hub.docker.com/r/mullholland/docker-molecule-rockylinux8)
-   [almalinux8](https://hub.docker.com/r/mullholland/docker-molecule-almalinux8)

The minimum version of Ansible required is 2.10, tests have been done to:

-   The last 2 versions.
-   The current version.



## [Exceptions](#exceptions)

Some variations of the build matrix do not work. These are the variations and reasons why the build won't work:

| variation                 | reason                 |
|---------------------------|------------------------|
| ubuntu* | repo only supports RedHat/CentOS Server |
| debian* | repo only supports RedHat/CentOS Server |
| fedora* | repo only supports RedHat/CentOS Server |


If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-repository_powertools/issues)

## [License](#license)

MIT


## [Author Information](#author-information)

[Mullholland](https://github.com/mullholland)

## [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
