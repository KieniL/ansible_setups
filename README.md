# ansible_setups


Following roles are there

* [cicdtools](./cicdtools/README.md)
* [secretsmanager](./secretsmanager/README.md)
* [suid-sgid-checker](./suid-sgid-checker/README.md)
* [ansible-pull](./ansible-pull/README.md)
* [kubernetes-install](./kubernetes-install/README.md)

ToDo:

- [ ] Add molecule testing to cicdtools
- [ ] Add molecule testing to secretsmanager (needs to be done on real linux systems since systemd does not work in wsl)
- [x] Add molecule testing to suid-sgid-checker --> Docker based
- [ ] Add molecule testing to ansible-pull
- [ ] Add molecule testing to kubernetes-install