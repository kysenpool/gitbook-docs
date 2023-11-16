---
description: Using Ansible Playbook to deploy an Agoric nodes
---

# Node Deployment

## Testnet with `state_sync`

```bash
ansible-playbook -i inventory_testnet.ini main.yml \
    -e "protocol=agoric" \
    -e "target=local" \
    -e "state_sync=true"
```

{% hint style="info" %}
If you want node to be running at the end - add `-e launch=true.`  Also state\_sync by default will be false
{% endhint %}

Command above will install:

* prometheus
* agoric (build from source code)
* cosmovisor

## Mainnet without `state_sync`

```bash
ansible-playbook -i inventory_remote_mainnet.ini main.yml \
    -e "protocol=agoric" \
    -e "target=local" \
    -e "state_sync=false" \
    -e "launch=true"
```

## Gathering snapshot and applying on the running node

```bash
ansible-playbook -i inventory_remote_mainnet.ini support_sync_snapshot.yml \
        -e "protocol=agoric" \
        -e "target=local" \
        -e "state_sync=false" \
        -e "launch=true" \
        -e "network_type=mainnet" \
        -e "snapshot_url='<https://snapshots.polkachu.com/snapshots/agoric/agoric_11726547.tar.lz4>'"  \
        -e "snapshot_json_snapshot_name=agoric-upgrade-11"
```

## Cleanup server from the node

```bash
ansible-playbook -i inventory_remote_testnet.ini support_remove_node.yml \
    -e "protocol=agoric" \
    -e "target=local"
```
