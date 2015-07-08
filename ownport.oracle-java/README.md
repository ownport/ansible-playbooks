# Oracle Java

## Playbook example

```yaml
---
- hosts: localhost
  connection: local
  gather_facts: no
  vars_files:
    - vars/java-versions.yml

  tasks:
    - include: tasks/install-java.yml
      vars:
        java_url: "{{ java_vers.server_jre_7u75.url }}"
        java_archive: "{{ java_vers.server_jre_7u75.url|basename }}"
        java_path: /tmp
```

## Links

- [andershedstrom/playbook-install-jdk8.yml](https://gist.github.com/andershedstrom/7c7d0bb5b9450c54a907), Ansible playbook for installing Oracle Java 8 on CentOS
- [gbirke/install-java.yml](https://gist.github.com/gbirke/8314571), Ansible playbook for installing Oracle Java 7 on Debian
- [vrischmann/ansible-role-java](https://github.com/vrischmann/ansible-role-java), Ansible role to install the Oracle JDK/JRE 
- [silpion/ansible-java](https://github.com/silpion/ansible-java), Ansible role to manage Java installation 

