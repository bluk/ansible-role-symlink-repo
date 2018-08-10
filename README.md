ansible-role-symlink-repo
=========================

[![GitHub license](https://img.shields.io/github/license/bluk/ansible-role-symlink-repo.svg)](https://github.com/bluk/ansible-role-symlink-repo/blob/master/LICENSE) [![Build Status](https://travis-ci.org/bluk/ansible-role-symlink-repo.svg?branch=master)](https://travis-ci.org/bluk/ansible-role-symlink-repo)

An [Ansible](https://www.ansible.com) role to clone a repository and symbolically link files/dirs to a specific directory.

Requirements
------------

The destination directory must not contain existing files with the same names.

Role Variables
--------------

* `git_repo` - The git URL to clone.

* `git_repo_local_dest` - The path to clone the files to.

* `git_repo_dir_src` - The path in the git repository to symbolically link from.

* `symlink_local_dest` - The path to create the symbolic links

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: bluk.symlink_repo }
```

License
-------

Apache 2.0
