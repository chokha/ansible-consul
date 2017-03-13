##Consul Installation

### Prerequisites
- Ansible
- Unzip util in all target systems
- Consul binary in Ansible control node (digitalocean_droplet.consul-1 is the control node in my cluster)

### Installation 
```bash
 ansible-playbook -i /opt/solution/ansible/consul/hosts /opt/solution/ansible/consul/install.yml

```
### Configuration file (template files)
-/root/solution/ansible/consul/group_vars/all
-/opt/solution/ansible/consul/roles/common/templates/server.json.j2
-/opt/solution/ansible/consul/roles/common/templates/client.json.j2


### Notes
- I wanted to make the ansible install script more verbose during installation so that the user knows whats happening when
- I had to open firewall digitalocean_droplet.consul-1
- I didn't have time to explore Consul more
- Ansible rocks!
