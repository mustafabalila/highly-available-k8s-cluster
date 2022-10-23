## Deploying a production-ready highly available Kubernetes cluster 

### About this

This is a guide to deploy a highly available Kubernetes cluster using [haproxy](http://www.haproxy.org/), [keepalived](https://keepalived.readthedocs.io/en/latest/introduction.html) and [kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/#tabs-pod-install-3).
After the playbook is executed, you'll have a join command for adding new nodes to the cluster.
The playbook doesn't handle joining nodes *yet*.
the join commands will be available at ./join_command file.

### Requirements
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- SSH access to at least 2 nodes

### How to use
- Clone this repo
```bash
git clone
```

- Edit the [vars/main.yml](./vars/main.yml) file to your needs

- Edit the [inventory/inventory](./inventory/inventory) hosts IPs.

- Run the playbook

```bash
ansible-playbook playbook.yml -i inventory
```
