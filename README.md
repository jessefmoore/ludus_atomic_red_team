# Ansible Role: Atomic Red Team ([Ludus](https://ludus.cloud))

An Ansible Role that installs [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) on Windows >= 10 hosts.

## Requirements

- community.windows
- ansible.windows

## Role Variables

None.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: hosts
  roles:
    - PrymalInstynct.ludus_atomic_red_team
```

## Example Ludus Range Config

```yaml
ludus:
  - vm_name: "{{ range_id }}-ad-dc-win2022-server-x64-1"
    hostname: "{{ range_id }}-DC01-2022"
    template: win2022-server-x64-template
    vlan: 10
    ip_last_octet: 11
    ram_gb: 6
    cpus: 4
    windows:
      sysprep: true
    domain:
      fqdn: ludus.domain
      role: primary-dc
    roles:
      - PrymalInstynct.ludus_atomic_red_team
```

## License

GPLv3

## Author Information

This role was created by [PrymalInstynct](https://github.com/PrymalInstynct), for [Ludus](https://ludus.cloud/).
