
Ansible role for Git client:
https://galaxy.ansible.com/uvsmtid/git-client-ansible-role/

## Description ##

Role configures Git client system-wide.

## Requirements ##

Supported platform:
Fedora 20+

## Role Variables ##

Override name and email:

```
git_client_config:
    git_name: Yolanda Wrorfush
    git_email: yolanda.wrorfush@example.com
```

## Example Playbook ##

```
---

-   hosts: all
    vars_files:
        -   git-client.yaml
    tasks:
        -   import_role:
                name: uvsmtid.git-client-ansible-role
```

## License ##

[Apache][1]

---

[1]: LICENSE

