# Provision k3s

```bash
cd k3s-ansible
# Make sure to add in your hosts to the inventory.yaml file
cp inventory-sample.yml inventory.yml
ansible-playbook playbook/site.yml -i inventory.yml --ask-become-pass
```

Install Packages

```bash
cd packages
cp inventory.tpl.yaml inventory.yaml
ansible-playbook install-packages.yaml -i inventory.yaml --ask-become-pass
```
