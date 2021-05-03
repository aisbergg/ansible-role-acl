# Ansible Role: `aisbergg.acl`

This Ansible role for managing file ACL on linux systems and allows to manage is a wrapper around the [`acl`](https://docs.ansible.com/ansible/latest/collections/ansible/posix/acl_module.html) module. It does the following:

- install the requirements to work with file ACL
- creates file or directories if desired
- manages ACLs for files and directories

## Requirements

None.

## Role Variables

| Variable | Default | Comments |
|----------|---------|----------|
| `acl_apply_defaults` | `true` | When set to `true`, any default ACL entry will also be applied as a regular entry (== `setfacl -d -m u:foo:rwX && setfacl -m u:foo:rwX`). |
| `acl_acls` | `[]` | List of ACL to be set. Most of the parameters are the same as the ones of the official [ACL module](https://docs.ansible.com/ansible/latest/collections/ansible/posix/acl_module.html). |
| `acl_acls[].create` | `no` | Create a dir or file at the given path, if it doesn't exist already. (`no`, `dir`, `file`) |
| `acl_acls[].owner` |  | User the created file/dir. |
| `acl_acls[].group` |  | Group the created file/dir. |
| `acl_acls[].mode` |  | Mode of the created file/dir. |
| **`acl_acls[].path`** |  | The full path of the file or object. |
| `acl_acls[].recursive` |  | Recursively sets the specified ACL. |
| `acl_acls[].default` |  | If the target is a directory, setting this to yes will make it the default ACL for entities created inside the directory. Also if `acl_apply_defaults` is set to `true`, then both the normal and the default ACLs are applied. |
| `acl_acls[].recalculate_mask` |  | Select if and when to recalculate the effective right masks of the files. |
| **`acl_acls[].entity`** |  | The actual user or group that the ACL applies to when matching entity types user or group are selected. |
| `acl_acls[].state` | `present` | Define whether the ACL should be present or not. |
| `acl_acls[].follow` |  | Whether to follow symlinks on the path if a symlink is encountered. |
| `acl_acls[].etype` |  | The entity type of the ACL to apply, see setfacl documentation for more info. |
| `acl_acls[].permissions` |  | The permissions to apply/remove can be any combination of r, w and x (read, write and execute respectively) |
| `acl_acls[].use_nfsv4_acls` |  | Use NFSv4 ACLs instead of POSIX ACLs. |

</br>

\* **bold** variables are required

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  vars:
    acl_apply_defaults: true
    acl_acls:
      # grant user 'joe' read access to a file
      - path: /etc/foo.conf
        entity: joe
        etype: user
        permissions: r

      # create dir and set default and regular ACL for group 'bar'
      - path: /var/www
        create: dir
        owner: root
        group: root
        entity: bar
        etype: group
        permissions: rwX
        default: true
  roles:
    - aisbergg.acl
```

## License

MIT

## Author Information

Andre Lehmann (aisberg@posteo.de)
