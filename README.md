# Lab Ansible + Cisco IOS sur GNS3

## Description
Automatisation de routeurs Cisco IOS avec Ansible sur GNS3/VMware Workstation.
Lab complet incluant configuration reseau, OSPF et backup automatise.

## Environnement
- Ansible 8.7.0 (core 2.15.13)
- Rocky Linux 9.5
- Cisco IOS 12.4 (2600 / 7200)
- GNS3 2.2.56.1 / VMware Workstation

## Topologie
## Playbooks
| Playbook | Description |
|---|---|
| show_version.yml | Recuperer la version IOS |
| config_interfaces.yml | Configurer interfaces + Loopback |
| backup_config.yml | Backup horodate du running-config |
| ospf_config.yml | Configuration OSPF automatisee |
| show_facts.yml | Rapport complet des routeurs |

## Modules Ansible utilises
- ios_command, ios_config, ios_facts
- copy, file, set_fact, debug

## Lancer un playbook
ansible-playbook -i inventory.ini show_version.yml
