# Ansible Role: Authoritative Bind

This role will assume the setup of an authoritative local nameserver via bind.

It's part of the ELAO [Ansible stack](http://ansible.elao.com) but can be used as a stand alone component.

## Requirements

- Ansible 1.7.2+

## Dependencies

None.

## Installation

## Role Handlers

|Name|Type|Description|
|----|-----------|-------|
`bind restart`|Service|Restart bind server

## Role Variables

|Name|Default|Type|Description|
|----|----|-----------|-------|
`bind_config_templates`|Array|Array|List of config files.
`bind_config_templates.named_conf`|-|String (filepath)|Custom path to global config file.
`bind_config_templates.named_conf_local`|-|String (filepath)|Custom path to local config file.
`bind_config_templates.named_conf_options`|-|String (filepath)|Custom path to options config file.
`bind_zones`|Array|Array|List of domain zones.
`bind_zones.domain`|-|String| domain name and TLD (Ex: elao.com).
`bind_zones.network`|-|String (filepath)|Zone network definition (Ex:172.16.1.0/24).
`bind_zones.responsible`|-|String (Email)|Contact mail address.

### Configuration example

## Example playbook

    - hosts: servers
      roles:
      - role: bind_authoritative

# Licence

MIT
