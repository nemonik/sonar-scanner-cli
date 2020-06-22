# Sonar Scanner CLI Ansible role

![Basic role syntax check](https://github.com/nemonik/sonar-scanner-cli-role/workflows/Basic%20role%20syntax%20check/badge.svg)

An Ansible role to install Sonar Scanner CLI. Known to work on CentOS 7, Alpine 3.10 and Ubuntu Bionic instances.

## Requirements

A CentOS 7, Alpine 3.10 and Ubuntu Bionic base image.

## Role Variables

| Variable                 | Required | Default               | Choices             | Comments                                                                    |
|--------------------------|----------|-----------------------|---------------------|-----------------------------------------------------------------------------|
| default_retries          | yes      | 60                    | Integer value       | default number of retries                                                   |
| default_delay            | yes      | 60                    | Integer value       | default delay in seconds between retries                                    |
| sonar_scanner_cli_version| yes      | 4.3.0.2102            | String value        | Releases matching https://github.com/SonarSource/sonar-scanner-cli/releases |
| sonarqube_host           | yes      | not defined           | String value        | IP or FDQN for SonarQube service                                            |
| sonarqube_port           | yes      | 9000                  | Integer value       | integer port value                                                          |

## Example Playbook

An example can be found used in my Hands-on DevOps course's [box/ansible/box-playbook-1.yml](https://github.com/nemonik/hands-on-DevOps/blob/master/box/ansible/box-playbook-1.yml).

```
- hosts: boxes
  connection: local
  remote_user: vagrant
  roles:
    - common
    - sonar-scanner-cli
```

For more information and to see this role put into action checkout my [Hands-on DevOps class](https://github.com/nemonik/hands-on-DevOps) project.

## License

3-Clause BSD License

## Author Information

Michael Joseph Walsh <mjwalsh@nemonik.com>
