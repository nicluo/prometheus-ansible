# Prometheus provisioning with Ansible

Ansible playbooks for setting up Prometheus monitoring system and configuring monitoring nodes.

- Prometheus
- Alertmanager
- node_exporter
- blackbox_exporter
- TODO: postgres_exporter

## Local development setup

The local setup provision a Prometheus server and another server with `node_exporter` installed.

1. Configure the prometheus server and test client server in `vagrant.default.yml`
2. Run `vagrant up`

## Remote setup

For remote setup, an Ubuntu 16.04 Xenial server is required for Prometheus server. Additional servers can be added to the `node` group to install `node_exporter`.

Besides that, remote servers also need to have at least Python installed for Ansible.

1. Configure hosts in `hosts/production`
2. Configure variables in `group_vars/production`
3. Run playbook with `ansible-playbook --inventory-file=hosts/production --sudo -v playbook.yml`
