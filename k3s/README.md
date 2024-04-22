# Provision k3s

```bash
# Make sure to add in your hosts to the inventory.yaml file
cp inventory-sample.yml inventory.yml
ansible-playbook playbook/site.yml -i inventory.yml --ask-become-pass 
```
