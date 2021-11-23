# Introduction

This project contains an Ansible playbook that can be used among with Zabbix, Jira and Ansible AWX/Tower to automatically evaluate and blocks IPs with bad reputation on Sophos XG Firewall.

The project used for check the IPs Reputation it's [ AbuseIPDB ](https://www.abuseipdb.com/) in the future other project might be integrated

### Requirements ###

* Zabbix Server with [ Jira Webhook plugin ](https://git.zabbix.com/projects/ZBX/repos/zabbix/browse/templates/media/jira)
* Jira
* Ansible AWX/Tower
* Sophos XG

### How do I get set up? ###

* [Zabbix Configuration](documentations/zabbix-configuration.md)
* [Ansible AWX/Tower Configuration](documentations/ansible-configuration.md)
* [Setup a vault file](documentations/.md)
* [Jira Configuration](documentations/jira-configuration.md)
* [Sophos XG Configuration](documentations/sophos-configuration.md)

### Setup an ansible vault ###

1) Create/edit credentials.yml file under vars/ folder (see credentials-example.yml)

2) Encrypt the file
```
ansible-vault encrypt credentials.yml
```

3) Add password for decrypt the vault on Ansible AWX (Resources > Credentials)