cicdtools
=========

The structure is generated with:


<code>
ansible-galaxy init cicdtools
molecule init scenario --role-name cicdtools default -d docker
rm -rf ./meta/
</code>
------------

### Installed Tools

Binary installations for cicd and security testing tools which are mostly used here: https://github.com/KieniL/FamilyCluster_Config/blob/main/Makefile

- [x] Dockerlint
- [x] Dockerfile_lint
- [x] dockerfilelint
- [x] Hadolint
- [x] Kubeval
- [x] Kubescore
- [x] Conftest
- [x] Conftest helm
- [x] Datree
- [x] Kubeaudit
- [x] Checkov
- [x] Terrascan
- [x] kubesec
- [x] yara
- [x] yarGen
- [x] kube-linter
- [x] kubescape
- [x] terraform
- [x] tflint
- [x] tfsec
- [x] dockerbench
- [x] trivy
- [x] ffuf
- [x] wafw00f


### Proven Automatic Updates

- [ ] Dockerlint
- [ ] Dockerfile_lint
- [ ] dockerfilelint
- [x] Hadolint
- [ ] Kubeval
- [x] Kubescore
- [x] Conftest
- [ ] Conftest helm
- [x] Datree
- [x] Kubeaudit
- [x] Checkov
- [x] Terrascan
- [x] kubesec
- [ ] yara
- [ ] yarGen
- [x] kube-linter
- [x] kubescape
- [x] terraform
- [x] tflint
- [x] tfsec
- [ ] dockerbench
- [x] trivy
- [ ] ffuf
- [ ] wafw00f


### local run

<code>
ansible-playbook -i inventory local.yml -K
</code>