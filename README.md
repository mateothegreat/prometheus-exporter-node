# node_exporter for prometheus ansible role

This role will install & configure node exporter for prometheus.

## Variables

```yaml
prometheus_exporter_node:
  version: "0.18.1"
  user: "exporters"
  group: "exporters"
  install_path: "/usr/local/bin"
  install_binary_name: "prometheus-exporter-node"
  listen_address: "0.0.0.0:9100"
```

## Example Usage

Add the following to a file like `playbook.yaml`:

```yaml
- hosts: monitoring
  roles:
    - role: "mateothegreat.prometheus"
      var:
        prometheus_exporter_node:
          version: "0.18.1"
          user: "exporters"
          group: "exporters"
          install_path: "/usr/local/bin"
          install_binary_name: "prometheus-exporter-node"
          listen_address: "0.0.0.0:9100"
```

Run with `ansible-playbook -i <your inventory file> playbook.yaml`.
