[![role](https://img.shields.io/ansible/role/55779)](https://galaxy.ansible.com/trallnag/asdf_terraform)
[![quality](https://img.shields.io/ansible/quality/55779)](https://galaxy.ansible.com/trallnag/asdf_terraform)
[![downloads](https://img.shields.io/ansible/role/d/55779?label=downloads)](https://galaxy.ansible.com/trallnag/asdf_terraform)

# Ansible Role `trallnag.asdf_terraform`

Installs and setups [Terraform][tf] with [`asdf`][asdf] on Linux.

[tf]: https://www.terraform.io/
[asdf]: https://github.com/asdf-vm/asdf

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/asdf_terraform).

## Role Variables

```yaml
asdf_terraform_version:
  default: 1.0.3
  type: raw
  required: false
  description: >-
    Terraform version to install and activate globally.

asdf_terraform_git_url:
  default: https://github.com/asdf-community/asdf-hashicorp.git
  type: raw
  required: false
  description: >-
    Git repo containing the plugin.
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.asdf_terraform
      vars:
        asdf_terraform_version: 1.0.3
        asdf_terraform_git_url: https://github.com/asdf-community/asdf-hashicorp.git
```

## Special Requirements

* `asdf` must be installed.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
