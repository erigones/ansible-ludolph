Ludolph
=========

Ansible role for installing Ludolph - The monitoring Jabber bot.

Requirements
------------

ansible >= 1.3

Role Variables
--------------

```
ludolph_user: ludolph
ludolph_group: ludolph
ludolph_homedir: /home/ludolph
ludolph_shell: /sbin/nologin

ludolph_daemon: True
ludolph_pidfile: /tmp/ludolph.pid
ludolph_logfile: /tmp/ludolph.log
ludolph_loglevel: INFO

ludolph_webserver_host: "127.0.0.1"
ludolph_webserver_port: 8222

ludolph_cron_enable: True

ludolph_nick: Ludolph

ludolph_xmpp_username: ludolph@erigones.com
ludolph_xmpp_password: SecretPassw0rd

ludolph_xmpp_host:
ludolph_xmpp_port:

ludolph_xmpp_use_tls: True
ludolph_xmpp_use_ssl: False
ludolph_xmpp_use_sslv3: False

ludolph_xmpp_users: []
ludolph_xmpp_admins: []

ludolph_xmpp_muc:
ludolph_xmpp_room_users: []
ludolph_xmpp_room_admins: []

ludolph_plugin_base_avatar_dir:

ludolph_plugin_zabbix_enable: False
ludolph_plugin_zabbix_server_url: https://zabbix.example.com
ludolph_plugin_zabbix_username: zabbix
ludolph_plugin_zabbix_password: zabbix

ludolph_plugin_zabbix_http_authentication: False

ludolph_plugin_zabbix_http_username: zabbix
ludolph_plugin_zabbix_http_password: zabbix
```

Example Playbook
----------------

To install Ludolph, use the following snippet:

    - hosts: server
      vars:
        ludolph_xmpp_username: ludolph@company.tld
        ludolph_xmpp_password: VerySecretPassword
      roles:
         - ludolph

License
-------

BSD

Author Information
------------------

[www.erigones.com](https://www.erigones.com)
