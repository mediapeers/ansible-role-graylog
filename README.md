# Graylog role

Ansible role to install and setup Graylog 2 server. Also installs dependencies such as ElasticSearch and MongoDB.


## Requirements

Server running Ubuntu Linux, or other debiand based distro.


## Role Variables

Those variables have to be set:

Those variables can be overriden optionally:
- `graylog_major_version: 2.3`


## Dependencies

Depends on the ElasticSearch ansible role `mediapeers.elasticsearch`. Make sure that role installed in your Ansible project first.

## Example Playbook

Example Playbook with minimal set of required parameters:

    - hosts: servers
      vars:
        graylog_password_salt: abc123123123
        graylog_root_username: graylog
        graylog_root_password_sha2: asdccsd3123
        graylog_root_user_email: graylog@email.com
        graylog_public_hostname: 'https://dummy-hostname.com'
      roles:
         - mediapeers.graylog

## License

BSD

## Author Information

Stefan Horning <horning@mediapeers.com>
