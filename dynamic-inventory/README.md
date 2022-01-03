# dynamic inventories

Inventory scripts for:

* docker (needs to end with .docker.yml or .docker.yaml)


## Run the inventories before running the playbook:

<code>
ansible hostname -i inventory.docker.yml -m ansible.builtin.ping
</code>

## Get the grouped inventory
<code>
ansible-inventory -i inventory.docker.yml --list
ansible-inventory -i inventory.docker.yml --graph
</code>

## to find possible keys
<code>
ansible-inventory -i inventory.docker.yml --list
</code>