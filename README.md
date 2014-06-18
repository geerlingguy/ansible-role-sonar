# Ansible Role: SonarQube

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-sonar.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-sonar)

An Ansible Role that installs [SonarQube](http://www.sonarqube.org/) on RedHat/CentOS and Debian/Ubuntu Linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    workspace: /root

Directory where downloaded files will be temporarily stored.

    sonar_version: "3.7.4"

The version of SonarQube to install.

    sonar_mysql_host: localhost
    sonar_mysql_port: 3306
    sonar_mysql_database: sonar
    sonar_mysql_user: sonar
    sonar_mysql_password: sonar

MySQL connection details.

## Dependencies

  - geerlingguy.java
  - geerlingguy.mysql

## Example Playbook

    - hosts: all
      roles:
        - { role: geerlingguy.sonar }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
