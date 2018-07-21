
Ansible role for Git client:
https://galaxy.ansible.com/uvsmtid/git-client/

## Description ##

Role configures Git client system-wide.

When `set_author_git_config` variable set to `True`,
in addition to aliases and other git settings,
author name and email is configured.

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

