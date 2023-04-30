
Ansible role for Git client:
https://galaxy.ansible.com/uvsmtid/git_client_role/

## Description ##

Role configures Git client.

Git config for author name and email is factored out into separate files:
*   `~/.gitconfig.author` for user-only config
*   `/etc/gitconfig.author` for system-wide config

When `set_author_git_config` variable set to `True`,
author name and email are automatically configured based on role variables (below).

When `is_regular_user_only` variable set to `True`,
system-wide configuration is **not** applied and package installation is not performed
(useful to avoid requirement for elevated permissions).

## Role variables ##

Override author name and email (e.g. in `git_client_role.yaml`):

```
git_client_config:
    git_name: Yolanda Wrorfush
    git_email: yolanda.wrorfush@example.com
```

## Example Playbook ##

Playbook using `git_client_role.yaml`:

```
---

-   hosts: all
    vars_files:
        -   git_client_config.yaml
    tasks:
        -   import_role:
                name: uvsmtid.git_client_role
```

## License ##

[Apache][1]

---

[1]: LICENSE

