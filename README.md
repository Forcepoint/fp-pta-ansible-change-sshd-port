# change-sshd-port

Change the default SSH port from 22 to whatever the ansible host is configured to use. 
Copied and modified with permission from https://dmsimard.com/2016/03/15/changing-the-ssh-port-with-ansible/
Modifications include running some of the commands with become, using the ansible_host variable instead
of inventory_hostname, and changing a when statement to fix a bug.

## Requirements

Do not run gather_facts when you call this role.

## Role Variables

None

## Dependencies

None

## Example Playbook

    - hosts: servers
      gather_facts: no
      roles:
         - { role: change-sshd-port }

## Example Hosts file

    [webservers]
    web01.somedomain.com ansible_port=1234

## License

Apache-2.0

## Author Information

Jeremy Cornett <jeremy.cornett@forcepoint.com>
