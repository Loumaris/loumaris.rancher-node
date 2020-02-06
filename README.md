# loumaris.rancher-node

A small playbook to setup a node as rancher node.

## usage

Example inside a playbook:

```yaml
- name: apply common configuration to all nodes
  hosts: all
  roles:
    - { role: loumaris.rancher-node, rancher_server: '1.1.1.1', rancher_token: '1234', rancher_checksum: '4321', rancher_public_ip: '1.2.3.4' }
```
## configuration

Possible parameter with default:

* `rancher_server`
* `rancher_token`
* `rancher_checksum`
* `rancher_public_ip`
* `rancher_default_roles`: _--etcd --controlplane --worker_
* `rancher_container_version`: _rancher/rancher-agent:v2.2.4_