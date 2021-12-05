secretsmanager
=========

<code>
molecule init scenario --role-name secretsmanager default -d docker
</code>

And then:
<code>
rm -rf ./meta/
</code>


The structure is generated with:
ansible-galaxy init secretsmanager


It installs consul and vault from hashicorp

It installs certbot and uses it if it found an entry for the provided vaulturl.
Be aware that this process is implented but not tested since I only use /etc/hosts


All Steps exluding the installation (apt instead of downloading of tar.gz) are taken from: https://github.com/b1tsized/vault-tutorial

### Installed Tools

- [x] consul
- [x] vault


### Proven Automatic Updates

- [x] consul
- [x] vault

### local run

<code>
ansible-playbook -i inventory local.yml -K
</code>