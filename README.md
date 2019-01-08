ansible-role-symlink-repo
=========================

An [Ansible][ansible] role to clone a repository and symbolically link
files/dirs to a specific directory.

Requirements
------------

By default, the destination directory must not contain existing files with the same
names.

Role Variables
--------------

* `git_repo` - The git URL to clone.

* `git_repo_local_dest` - The path to clone the files to.

* `git_repo_dir_src` - The path in the git repository to symbolically link from.

* `git_accept_hostkey` - If the hostkey should automatically be accepted.

* `git_force` - If the repository should discord changes in the directory.

* `git_recursive` - If any submodules should be checked out.

* `git_remote` - The name of the remote to give.

* `git_update` - If the repository should be updated.

* `git_verify_commit` - If the commit's GPG signature should be verified.

* `git_version` - The version to checkout.

* `symlink_local_dest` - The path to create the symbolic links.

* `symlink_local_force_replace` - Replace existing files with symbolic links.

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

[Apache-2.0][LICENSE]

[ansible]: https://www.ansible.com
[LICENSE]: LICENSE
