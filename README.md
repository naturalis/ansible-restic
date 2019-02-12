# Ansible role for restic

A more or less one-on-one fork of our [Puppet restic
module](https://github.com/naturalis/puppet-restic) to Ansible. Highly
opinionated and not necessarily for general use outside Naturalis.

## Requirements

TBD

## Role Variables

Aim is to use the same variables that are used in the [Puppet
module](https://github.com/naturalis/puppet-restic) with sane defaults.

You will have to provide values for the following variables:

```yaml
restic_aws_access_key: 'XXXXXXXXXXXXXXXXXX'
restic_aws_secret_key: 'XXXXXXXXXXXXXXXXXX'
restic_password: 'backuppassword'
restic_aws_repo: 's3:https://s3.amazonaws.com/restic-repo-name'
```

## Dependencies

TBD

## Example Playbook

This is a simple playbook in which the ansible-restic role is applied.

```yaml
---
- hosts: all
  gather_facts: true
  vars:
    cron: true
  roles:
    - ansible-restic

```

## License

BSD

## Author Information

Some code has been used from [this Ansible restic
role](https://github.com/donat-b/ansible-restic) by several authors.

The original Puppet module is written by Hugo van Duijn.
This fork is written by David Heijkamp.