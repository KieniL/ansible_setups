
- [Docker](#docker)
  - [Run the inventories before running the playbook:](#run-the-inventories-before-running-the-playbook)
  - [Get the grouped inventory](#get-the-grouped-inventory)
  - [to find possible keys](#to-find-possible-keys)
Inventory scripts for:

* docker (needs to end with .docker.yml or .docker.yaml)


## Docker 

Add a label with -l at starting the container since the inventory will group it also on that.

E.g.
<code>
ansible-inventory -i inventory.docker.yml --graph
</code>

Will return @labels_webserver_:

### Run the inventories before running the playbook:

<code>
ansible hostname -i inventory.docker.yml -m ansible.builtin.ping
</code>

### Get the grouped inventory
<code>
ansible-inventory -i inventory.docker.yml --list
ansible-inventory -i inventory.docker.yml --graph
</code>

### to find possible keys
<code>
ansible-inventory -i inventory.docker.yml --list
</code>