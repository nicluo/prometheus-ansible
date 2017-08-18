# Prometheus provisioning with Ansible

Ansible playbooks for setting up Prometheus monitoring system and configuring monitoring nodes.

- Prometheus
- Alertmanager
- node_exporter
- blackbox_exporter
- TODO: postgres_exporter

## Local development setup

1. Configure the prometheus server and test client server in `vagrant.default.yml`
2. Run `vagrant up`