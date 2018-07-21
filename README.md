
Ansible role for Git client:
https://galaxy.ansible.com/uvsmtid/git-client/

## Description ##

Role configures Git client.

When `set_author_git_config` variable set to `True`,
in addition to aliases and other git settings,
author name and email is configured.

When `is_regular_user_only` variable set to `True`,
system-wide configuration (which require elevated permissions)
is **not** applied and package installation is not performed.

## Requirements ##

Supported platform:
Fedora 20+

## Role Variables ##

Override author name and email (e.g. in `git-client.yaml`):

```
git_client_config:
    git_name: Yolanda Wrorfush
    git_email: yolanda.wrorfush@example.com
```

## Example Playbook ##

Playbook using `git-client.yaml`:

```
---

-   hosts: all
    vars_files:
        -   git-client.yaml
    tasks:
        -   import_role:
                name: uvsmtid.git-client
```

## License ##

[Apache][1]

---

[1]: LICENSE

